---
title: Customer Journey Analytics使用的Adobe Advertising ID
description: Customer Journey Analytics使用的Adobe Advertising ID
feature: Integration with Adobe Customer Journey Analytics
exl-id: af60dcb4-4d1a-4097-ac30-688bd8b9f644
TQID: https://experienceleague.adobe.com/q1298GdnFUQBJGy-slOfy5-XJLXuJmojHErwJaxTX2A
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 0%

---

# Customer Journey Analytics使用的Adobe Advertising ID

*仅集成Adobe Advertising-Adobe Customer Journey Analytics的广告商*

*适用于Advertising DSP和[!DNL Advertising Search, Social, & Commerce]*

*Beta功能*

Adobe Advertising使用两个ID进行现场性能跟踪： *EF ID*&#x200B;和&#x200B;*AMO ID*。

<!--
 Rewrite for CJA:

When an ad impression occurs, Adobe Advertising creates the AMO ID and EF ID values and stores them. For click-through traffic, these IDs are included in the landing page URL using the `ef_id` and `s_kwcid` (for the AMO ID) query string parameters.

Adobe Advertising distinguishes between a click-through or view-through entry to the website using the following criteria:

* A view-through entry is captured when a user visits the site after viewing an ad but not clicking it. [!DNL Analytics] or Web SDK records a view-through if two conditions are met:

    * The visitor has no click-throughs for a [!DNL DSP] or [!DNL Search, Social, & Commerce] ad during the [click lookback window](/help/integrations/analytics/prerequisites.md#lookback-a4adc).

    * The visitor has seen at least one [!DNL DSP] ad during the [impression lookback window](/help/integrations/analytics/prerequisites.md#lookback-a4adc). The last impression is passed as the view-through.

* A click-through entry is captured when a site visitor clicks an ad before entering the site. [!DNL Analytics] or Web SDK captures a click-through when either of the following conditions occurs:

    * The URL includes an EF ID and AMO ID as added to the landing page URL by Adobe Advertising.

    * The URL contains no tracking codes, but the Adobe Advertising JavaScript code detects a click within the last two minutes.

![Adobe Advertising view-based [!DNL Analytics] integration](/help/integrations/assets/a4adc-view-through-process.png)

*Figure 1: Adobe Advertising view-based [!DNL Analytics] integration*

![Adobe Advertising click URL-based [!DNL Analytics] integration](/help/integrations/assets/a4adc-click-through-process.png)

*Figure 2: Adobe Advertising click URL-based [!DNL Analytics] integration*

-->

<!-- ## Adobe Advertising EF IDs {#ef-id} -->

{{$include /help/_includes/ef-id.md}}

<!-- ## Adobe Advertising AMO IDs {#amo-id} -->

{{$include /help/_includes/amo-id.md}}

<!--
 rewrite for CJA:

### AMO ID Dimension in [!DNL Customer Journey Analytics]

In Analytics reports, you can find AMO ID data by searching for the [!UICONTROL AMO ID] dimension and using the [!UICONTROL AMO ID Instances] metric. The [!UICONTROL AMO ID] dimension houses all AMO ID values captured, whereas the [!UICONTROL AMO ID Instances] metric indicates how often an AMO ID value was captured by the site. For example, if the same search ad was clicked four times but Analytics tracked seven site entries, then [!UICONTROL AMO ID Instances] would be seven (7) and [!UICONTROL Clicks] would be four (4).

For any reporting or auditing within [!DNL Analytics], the best practice is to use the AMO ID along with its corresponding instance. For more information, see "[Click-through data validation for [!DNL Analytics for Advertising]](data-variances.md#data-validation)" in "Expected data variances between [!DNL Analytics] and Adobe Advertising."

-->

>[!MORELIKETHIS]
>
>* [概述](overview.md)
>* [先决条件](prerequisites.md)
>* [设置数据收集、数据传输和报告](set-up.md)
>* Customer Journey Analytics中的[Adobe Advertising指标和维度](advertising-data-in-cja.md)
