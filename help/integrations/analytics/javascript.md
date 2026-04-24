---
title: JavaScript code for [!DNL Analytics for Advertising]
description: JavaScript code for [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
TQID: https://experienceleague.adobe.com/g9onwe1IQl1kbyQ82W2KmODPGUAReKiotxy65yCZcNY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 941
ht-degree: 0%

---

# JavaScript code for [!DNL Analytics for Advertising]

*仅使用Advertising DSP的广告商*

For Advertising DSP, the [!DNL Analytics for Advertising] integration tracks view-through and click-through site interactions. Click-through visits are tracked by the standard Adobe Analytics code on your webpages; the [!DNL Analytics] code captures the AMO ID and EF ID parameters in the landing page URL and tracks them in their respective reserved [!DNL eVars]. You can track view-through visits by deploying a JavaScript snippet in your webpages.

On the first page view of a visit to the site, the Adobe Advertising JavaScript code checks to see if the visitor has previously seen or clicked on an ad. If the user has previously entered the site via a click-through or hasn&#39;t seen an ad, then the visitor is ignored. If the visitor has seen an ad and hasn&#39;t entered the site via a click-through during the [click lookback window](/help/integrations/analytics/prerequisites.md#lookback-a4adc) set within Adobe Advertising, then the Adobe Advertising JavaScript code either a) uses the [Experience Cloud ID Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) to generate a supplemental ID (`SDID`) or b) uses the Adobe Experience Platform [!DNL Web SDK] `generateRandomID` method to generate a `[!DNL StitchID]`. Either ID is used to stitch data from Adobe Advertising to the visitor&#39;s Adobe Analytics hit. Adobe Analytics then queries Adobe Advertising for the AMO ID and EF ID associated with the ad exposure. The AMO ID and EF IDs are then populated in their respective [!DNL eVars]. These values persist for a designated period (by default, 60 days).

[!DNL Analytics] sends site traffic metrics (such as page views, visits, and time spent) and any [!DNL Analytics] custom or standard events to Adobe Advertising hourly, using the EF ID as the key. These [!DNL Analytics] metrics then run through the Adobe Advertising attribution system to connect the conversions to the click and exposure history.

>[!NOTE]
>
>The Adobe Advertising JavaScript tracking logic occurs on the Adobe side and thus has virtually no impact to the page load time.
>
>In contrast, the logic for the [!DNL DCM] data connector to [!DNL Analytics] (using [!DNL Google Campaign Manager 360]) for Advertising DSP occurs on the client side. Client-side stitching slows down the page load and increases the risk of data loss. This occurs because the [!DNL Analytics] JavaScript must ping [!DNL DoubleClick] and wait for [!DNL DoubleClick] to pass back the last click/impression data to [!DNL Analytics]. When your [!DNL DSP] team sets up the [!DNL DCM] data connector, you must specify how long you&#39;re willing to delay the page.

<!--
## Deploying the JavaScript code

All users must deploy the standard JavaScript code.

Users who want to convert first-party segments from their customer data platforms to [!DNL RampIDs] or [!DNL ID5] IDs [!!!!VERIFY that it's not needed for importing segments directly from LiveRamp] must also deploy ID partner-specific JavaScript code to match conversions to view-throughs.

### The standard code

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

### Additional code to import first-party segments to [!DNL RampIDs] and [!DNL ID5] IDs

   * For [!DNL RampIDs], Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

    [MAYBE PUT THIS BELOW] Place the [!DNL LaunchPad] tag on every page of your website, preferably as the first script within the page head tags but as high within the page head tags as possible.

   * For [!DNL ID5] IDs: Contact your Adobe Account Team, who will give you instructions to register for the tag with ID5. Registration is free, but you must sign an agreement. Once you register, a member of ID5's technical team will provide a unique tag for your organization to implement on your webpages.
-->

## Deploying the JavaScript code

The JavaScript library consists of two lines that allow [!DNL Analytics] and Adobe Advertising to communicate with each other. 如果[!DNL Analytics for Advertising]集成已在Adobe Advertising实施期间完成，则您应该已经收到此代码，其中包含有关如何部署此代码的说明。

### 代码

#### 使用Experience Cloud Identity Service `visitorAPI.js`代码的实施

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### 使用Experience Platform [!DNL Web SDK] `alloy.js`代码的实施

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### 代码放置位置

[!DNL Analytics for Advertising] JavaScript函数必须在Experience Cloud ID服务之后、Analytics App Measurement代码之前。 这可以确保在您的Analytics调用中包含补充ID (`SDID`)或`[!DNL StitchID]`。

![代码位置](/help/integrations/assets/a4adc-code-placement.png)

### 验证代码部署

您可以使用任何数据包探查器类型的工具（如[!DNL Charles]、[!DNL Fiddler]或[!DNL Chrome Developer Tools]）执行验证，方法是比较发往Adobe Advertising的请求和发往[!DNL Analytics]的请求之间的四个ID的值，如下所述。

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

1. （使用Experience Cloud Identity服务`visitorAPI.js`代码的实施）筛选`/b/ss`以查看Analytics点击。

   ![在`/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)上筛选

1. （使用Experience Platform [!DNL Web SDK] `alloy.js`代码的实施）在`/interact`上筛选以验证发送到Edge Network的请求有效负载是否包含`advertisingStitchID`。

   ![在`/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)上筛选

1. 比较两次点击之间的ID值。 所有值都应位于查询字符串参数中，但Analytics点击中的报表包ID（紧接`/b/ss/`之后的URL路径）除外。

   | ID | Analytics参数 | Edge Network | Adobe Advertising参数 |
   | --- | --- | --- | --- |
   | Experience Cloud IMS组织 | `mcorgid` |  | `_les_imsOrgid` |
   | 补充数据ID | sdid |  | `_les_sdid` |
   | 拼接ID | stitchId | `_adcloud`属性下的`advertisingStitchID` |  |
   | Analytics报表包 | `/b/ss/`之后的值 | | `_les_rsid` |
   | Experience Cloud访客ID | mid |  | `_les_mid` |

   如果ID值匹配，则会确认JavaScript实施。 Adobe Advertising向[!DNL Analytics]服务器发送任何点进或浏览跟踪详细信息（如果存在）。

#### 如何使用[!DNL Adobe Experience Platform Debugger]确认代码

1. 在主页中打开[该 [!DNL Adobe Experience Platform Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)。
1. 转到[!UICONTROL Network]选项卡。
1. 在[!UICONTROL Solutions Filter]工具栏中，单击[!UICONTROL Adobe Advertising]和[!UICONTROL Analytics]。
1. 在[!UICONTROL Request URL - Hostname]参数行中，找到`lasteventf-tm.everesttech.net`。
1. 在[!UICONTROL Request - Parameters]行中，审核生成的信号，类似于“[如何使用 [!DNL Chrome Developer Tools]](#validate-js-chrome)确认代码”中的步骤3。
   * （使用Experience Cloud Identity Service `visitorAPI.js`代码的实施）确保`Sdid`参数与Adobe Analytics筛选器中的`Supplemental Data ID`匹配。
   * （使用Experience Platform [!DNL Web SDK] `alloy.js`代码的实施）确保`advertisingStitchID`参数的值与发送到Experience Platform Edge Network的`Sdid`匹配。
   * 如果代码未生成，则检查以确保已在[!UICONTROL Application]选项卡中删除Adobe Advertising Cookie。 删除页面后，请刷新页面并重复此过程。

   ![在[!DNL Platform Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)中审核[!DNL Analytics for Advertising]个JavaScript代码

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [实施的先决条件和关键信息 [!DNL Analytics for Advertising]](prerequisites.md)
