---
title: JavaScript代码 [!DNL Analytics for Advertising]
description: JavaScript代码 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# JavaScript代码 [!DNL Analytics for Advertising]

*仅使用Advertising DSP的广告商*

对于Advertising DSP， [!DNL Analytics for Advertising] 集成跟踪浏览和点进网站交互。 点进访问由您网页上的标准Adobe Analytics代码进行跟踪； [!DNL Analytics] 代码捕获登陆页面URL中的AMO ID和EF ID参数，并在它们各自的保留中跟踪它们 [!DNL eVars]. 您可以在网页中部署JavaScript代码片段，从而跟踪浏览访问。

在访问网站后的第一个页面查看中，Adobe AdvertisingJavaScript代码会检查访客以前是否查看过或点击过广告。 如果用户之前通过点进进入网站或者没有看到广告，则会忽略该访客。 如果访客在访问期间看到广告，但未通过点进进入网站 [单击回顾窗口](/help/integrations/analytics/prerequisites.md#lookback-a4adc) 在Adobe Advertising中设置，则Adobe AdvertisingJavaScript代码(a)使用 [Experience CloudID服务](https://experienceleague.adobe.com/docs/id-service/using/home.html) 生成补充ID (`SDID`)或b)使用Adobe Experience Platform [!DNL Web SDK] `generateRandomID` 用于生成 `[!DNL StitchID]`. 其中任一ID都可用于将Adobe Advertising中的数据拼合到访客的Adobe Analytics点击中。 然后，Adobe Analytics会查询Adobe Advertising与广告曝光度关联的AMO ID和EF ID。 然后，将AMO ID和EF ID填充到它们各自的中 [!DNL eVars]. 这些值会在指定的时间段内保留（默认情况下，为60天）。

[!DNL Analytics] 发送网站流量量度（如页面查看次数、访问次数和逗留时间）和 [!DNL Analytics] 使用EF ID作为键每小时Adobe Advertising的自定义或标准事件。 这些 [!DNL Analytics] 量度然后通过Adobe Advertising归因系统，将转化连接到点击和曝光历史记录。

>[!NOTE]
>
>Adobe AdvertisingJavaScript跟踪逻辑发生在Adobe端，因此对页面加载时间几乎没有影响。
>
>相比之下， [!DNL DCM] 数据连接器至 [!DNL Analytics] (使用 [!DNL Google Campaign Manager 360]DSP )。 客户端拼接会减慢页面加载速度并增加数据丢失的风险。 出现这种情况是因为 [!DNL Analytics] JavaScript必须ping [!DNL DoubleClick] 并等待 [!DNL DoubleClick] 以将最后一次点击/展示数据传递回 [!DNL Analytics]. 当 [!DNL DSP] 团队设置 [!DNL DCM] data connector中，您必须指定愿意将页面延迟多长时间。

## 部署JavaScript代码

JavaScript库包含两行，它们允许 [!DNL Analytics] 和Adobe Advertising相互沟通。 如果 [!DNL Analytics for Advertising] 集成已在Adobe Advertising实施期间完成，则您应该已经收到此代码及其部署说明。

### 代码

#### 使用Experience CloudIdentity服务的实施 `visitorAPI.js` 代码

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### 使用Experience Platform的实施 [!DNL Web SDK] `alloy.js`代码

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### 代码放置位置

此 [!DNL Analytics for Advertising] JavaScript函数必须在Experience CloudID服务之后、Analytics App Measurement代码之前。 这可确保补充ID (`SDID`)或 `[!DNL StitchID]` 包含在您的Analytics调用中。

![代码放置](/help/integrations/assets/a4adc-code-placement.png)

### 验证代码部署

您可以使用任何数据包探查器类型的工具(例如 [!DNL Charles]， [!DNL Fiddler]，或 [!DNL Chrome Developer Tools])，比较即将请求和即将请求Adobe Advertising之间的四个ID值 [!DNL Analytics]，如下所述。

#### 如何使用确认代码 [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. 打开 [!DNL Chrome Developer Tools] 然后单击 **网络** 选项卡。

1. 加载包含 [!DNL Analytics for Advertising] JavaScript。

1. 筛选 [!UICONTROL Network] 制表方式 `last` 并查看两行：

   ![在上次筛选](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * 第一行是对JavaScript库的调用，其标题为 `last-event-tag-latest.min.js`.
   * 第二行是将请求发送到Adobe Advertising的调用。 其开头如下： `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     如果您没有看到对Adobe Advertising的调用，则该调用可能不是您访问的第一个页面查看。 出于测试目的，您可以删除Cookie，以便下次调用是相应访问的第一个页面查看：

   1. 在“应用程序”选项卡上，找到 `adcloud` Cookie，并确认Cookie包含 `_les_v` （上次访问）且值为 `y` 以及30分钟后过期的UTC纪元时间戳。
      1. 删除 `adcloud` cookie并刷新页面。

1. (使用Experience CloudIdentity服务的实施 `visitorAPI.js` 代码)筛选依据 `/b/ss` 以查看Analytics点击。

   ![过滤于 `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (使用Experience Platform的实施 [!DNL Web SDK] `alloy.js`代码)筛选依据 `/interact` 验证发送给Edge Network的请求有效负载是否包含 `advertisingStitchID`.

   ![过滤于 `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. 比较两次点击之间的ID值。 所有值都应位于查询字符串参数中，但Analytics点击中的报表包ID（紧随其后的URL路径）除外 `/b/ss/`.

   | ID | Analytics参数 | Edge Network | Adobe Advertising参数 |
   | --- | --- | --- | --- |
   | Experience CloudIMS组织 | `mcorgid` |  | `_les_imsOrgid` |
   | 补充数据ID | sdid |  | `_les_sdid` |
   | 拼接ID | stitchId | `advertisingStitchID` 在 `_adcloud` 属性 |  |
   | Analytics报表包 | 之后的值 `/b/ss/` | | `_les_rsid` |
   | Experience Cloud访客ID | mid |  | `_les_mid` |

   如果ID值匹配，则会确认JavaScript实施。 Adobe Advertising将发送 [!DNL Analytics] 提供所有点进或浏览跟踪详细信息（如果存在）。

#### 如何使用确认代码 [!DNL Adobe Experience Cloud Debugger]

1. 打开 [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) 在你的主页上。
1. 转到 [!UICONTROL Network] 选项卡。
1. 在 [!UICONTROL Solutions Filter] 工具栏，单击 [!UICONTROL Adobe Advertising] 和 [!UICONTROL Analytics].
1. 在 [!UICONTROL Request URL - Hostname] 参数行，查找 `lasteventf-tm.everesttech.net`.
1. 在 [!UICONTROL Request - Parameters] 行，审核生成的信号，类似于&quot;[如何使用确认代码 [!DNL Chrome Developer Tools]](#validate-js-chrome)“
   * (使用Experience CloudIdentity服务的实施 `visitorAPI.js` 代码)确保 `Sdid` 参数匹配 `Supplemental Data ID` 在Adobe Analytics过滤器中。
   * (使用Experience Platform的实施 [!DNL Web SDK] `alloy.js`代码)确保 `advertisingStitchID` 参数匹配 `Sdid` 发送到Experience Platform边缘网络。
   * 如果代码未生成，请检查以确保在中删除了Adobe AdvertisingCookie [!UICONTROL Application] 选项卡。 删除页面后，请刷新页面并重复此过程。

   ![审核 [!DNL Analytics for Advertising] 中的JavaScript代码 [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [实施的先决条件和关键信息 [!DNL Analytics for Advertising]](prerequisites.md)
