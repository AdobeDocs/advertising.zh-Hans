---
title: ' [!DNL Analytics for Advertising]的JavaScript代码'
description: ' [!DNL Analytics for Advertising]的JavaScript代码'
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 5d07300ab49b96daf392cb51f8936fa4c0cd20ce
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 0%

---

# [!DNL Analytics for Advertising]的JavaScript代码

*仅使用Advertising DSP的广告商*

对于Advertising DSP，[!DNL Analytics for Advertising]集成跟踪显示到达和点进网站交互。 点进访问由您网页上的标准Adobe Analytics代码进行跟踪；[!DNL Analytics]代码捕获登陆页面URL中的AMO ID和EF ID参数，并在它们各自的保留[!DNL eVars]中跟踪它们。 您可以通过在网页中部署JavaScript代码片段来跟踪浏览访问。

在访问网站后的第一个页面查看中，Adobe AdvertisingJavaScript代码会检查访客以前是否查看过或点击过广告。 如果用户之前通过点进进入网站或者没有看到广告，则会忽略该访客。 如果访客在Adobe Advertising中设置的[点击回顾窗口](/help/integrations/analytics/prerequisites.md#lookback-a4adc)期间看到广告而没有通过点进进入网站，则Adobe AdvertisingJavaScript代码a)使用[Experience CloudID服务](https://experienceleague.adobe.com/docs/id-service/using/home.html)生成补充ID (`SDID`)，或b)使用Adobe Experience Platform [!DNL Web SDK] `generateRandomID`方法生成`[!DNL StitchID]`。 其中任一ID都可用于将Adobe Advertising中的数据拼合到访客的Adobe Analytics点击中。 然后，Adobe Analytics会查询Adobe Advertising与广告曝光度关联的AMO ID和EF ID。 随后，AMO ID和EF ID将填充到它们各自的[!DNL eVars]中。 这些值会在指定的时间段内保留（默认情况下，为60天）。

[!DNL Analytics]使用EF ID作为键，将网站流量量度（如页面查看次数、访问次数和逗留时间）和任何[!DNL Analytics]自定义或标准事件每小时Adobe Advertising一次。 然后，这[!DNL Analytics]个指标将通过Adobe Advertising归因系统运行，以将转化连接到点击和曝光历史记录。

>[!NOTE]
>
>Adobe AdvertisingJavaScript跟踪逻辑发生在Adobe端，因此对页面加载时间几乎没有任何影响。
>
>相反，用于Advertising DSP的[!DNL DCM]数据连接器到[!DNL Analytics]（使用[!DNL Google Campaign Manager 360]）的逻辑发生在客户端。 客户端拼接会减慢页面加载速度并增加数据丢失的风险。 发生这种情况是因为[!DNL Analytics] JavaScript必须ping [!DNL DoubleClick]，并等待[!DNL DoubleClick]将上次点击/展示数据传递回[!DNL Analytics]。 当您的[!DNL DSP]团队设置[!DNL DCM]数据连接器时，您必须指定愿意将页面延迟多长时间。

<!--
## Deploying the JavaScript Code

All users must deploy the standard JavaScript code.

Users who want to convert first-party segments from their customer data platforms to [!DNL RampIDs] or [!DNL ID5] IDs [!!!!VERIFY that it's not needed for importing segments directly from LiveRamp] must also deploy ID partner-specific JavaScript code to match conversions to view-throughs.

### The Standard Code

The standard JavaScript library consists of two lines that allow [!DNL Analytics] and Adobe Advertising to communicate with each other. If the [!DNL Analytics for Advertising] integration was completed during the Adobe Advertising implementation, then you should have already received this code with instructions on how to deploy it.

#### Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code

### Additional Code to Import First-Party Segments to [!DNL RampIDs] and [!DNL ID5] IDs

   * For [!DNL RampIDs], Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

    [MAYBE PUT THIS BELOW] Place the [!DNL LaunchPad] tag on every page of your website, preferably as the first script within the page head tags but as high within the page head tags as possible.

   * For [!DNL ID5] IDs: Contact your Adobe Account Team, who will give you instructions to register for the tag with ID5. Registration is free, but you must sign an agreement. Once you register, a member of ID5’s technical team will provide a unique tag for your organization to implement on your webpages.
-->

## 部署JavaScript代码

JavaScript库包含两行，允许[!DNL Analytics]和Adobe Advertising相互通信。 如果[!DNL Analytics for Advertising]集成已在Adobe Advertising实施期间完成，则您应该已经收到此代码，其中包含有关如何部署此代码的说明。

### 代码

#### 使用Experience Cloud标识服务`visitorAPI.js`代码的实现

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### 使用Experience Platform[!DNL Web SDK] `alloy.js`代码的实施

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### 代码放置位置

[!DNL Analytics for Advertising] JavaScript函数必须在Experience CloudID服务之后、Analytics App Measurement代码之前。 这可以确保在您的Analytics调用中包含补充ID (`SDID`)或`[!DNL StitchID]`。

![代码位置](/help/integrations/assets/a4adc-code-placement.png)

### 验证代码部署

您可以使用任何数据包探查器类型的工具（如[!DNL Charles]、[!DNL Fiddler]或[!DNL Chrome Developer Tools]）执行验证，方法是：比较即将发送的请求与即将发送至[!DNL Analytics]的Adobe Advertising之间的四个ID的值，如下所述。

#### 如何使用[!DNL Chrome Developer Tools]确认代码 {#validate-js-chrome}

1. 打开[!DNL Chrome Developer Tools]并单击&#x200B;**网络**&#x200B;选项卡。

1. 加载包含[!DNL Analytics for Advertising] JavaScript的网站页面。

1. 按`last`筛选[!UICONTROL Network]选项卡并查看两行：

   ![在上次](/help/integrations/assets/a4adc-code-validation-filter-last.png)筛选

   * 第一行是对JavaScript库的调用，标题为`last-event-tag-latest.min.js`。
   * 第二行是将请求发送到Adobe Advertising的调用。 其开头如下： `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     如果您没有看到对Adobe Advertising的调用，则该调用可能不是您访问的第一个页面查看。 出于测试目的，您可以删除Cookie，以便下次调用是相应访问的第一个页面查看：

   1. 在“应用程序”选项卡上，找到`adcloud` Cookie，并验证Cookie是否包含值为`y`的`_les_v`（上次访问）以及30分钟后过期的UTC纪元时间戳。
      1. 删除`adcloud` Cookie并刷新页面。

1. (使用Experience Cloud标识服务`visitorAPI.js`代码的实施)筛选`/b/ss`以查看Analytics点击。

   ![在`/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)上筛选

1. (使用Experience Platform[!DNL Web SDK] `alloy.js`代码的实施)筛选`/interact`，以验证请求有效负载是否包含`advertisingStitchID`Edge Network。

   ![在`/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)上筛选

1. 比较两次点击之间的ID值。 所有值都应位于查询字符串参数中，但Analytics点击中的报表包ID（紧接`/b/ss/`之后的URL路径）除外。

   | ID | Analytics参数 | Edge Network | Adobe Advertising参数 |
   | --- | --- | --- | --- |
   | Experience CloudIMS组织 | `mcorgid` |  | `_les_imsOrgid` |
   | 补充数据ID | sdid |  | `_les_sdid` |
   | 拼接ID | stitchId | `_adcloud`属性下的`advertisingStitchID` |  |
   | Analytics报表包 | `/b/ss/`之后的值 | | `_les_rsid` |
   | Experience Cloud访客ID | mid |  | `_les_mid` |

   如果ID值匹配，则会确认JavaScript实施。 Adobe Advertising向[!DNL Analytics]服务器发送任何点进或浏览跟踪详细信息（如果存在）。

#### 如何使用[!DNL Adobe Experience Cloud Debugger]确认代码

1. 打开主页上的[[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)。
1. 转到[!UICONTROL Network]选项卡。
1. 在[!UICONTROL Solutions Filter]工具栏中，单击[!UICONTROL Adobe Advertising]和[!UICONTROL Analytics]。
1. 在[!UICONTROL Request URL - Hostname]参数行中，找到`lasteventf-tm.everesttech.net`。
1. 在[!UICONTROL Request - Parameters]行中，审核生成的信号，类似于“[如何使用 [!DNL Chrome Developer Tools]](#validate-js-chrome)确认代码”中的步骤3。
   * (使用Experience Cloud标识服务`visitorAPI.js`代码的实施)确保`Sdid`参数与Adobe Analytics筛选器中的`Supplemental Data ID`匹配。
   * (使用Experience Platform[!DNL Web SDK] `alloy.js`代码的实施)确保`advertisingStitchID`参数的值与发送到Experience PlatformEdge Network的`Sdid`匹配。
   * 如果代码未生成，则检查以确保已在[!UICONTROL Application]选项卡中删除了Adobe AdvertisingCookie。 删除页面后，请刷新页面并重复此过程。

   ![在[!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)中审核[!DNL Analytics for Advertising]个JavaScript代码

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [实施的先决条件和关键信息 [!DNL Analytics for Advertising]](prerequisites.md)
