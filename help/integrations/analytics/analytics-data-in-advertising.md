---
title: '[!DNL Analytics] Data in  Adobe Advertising'
description: '[!DNL Analytics] Data in Adobe Advertising'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
TQID: https://experienceleague.adobe.com/Op96b-n8lH2vLwBfUjlJdunp65Y5o2-gYxaEWFwH2m8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: c4d69b3aac9c963d13e3083f71931e507e58e616
workflow-type: tm+mt
source-wordcount: 345
ht-degree: 0%

---

# [!DNL Analytics] Data in Adobe Advertising

*仅集成Adobe Advertising-Adobe Analytics的广告商*

## Analytics segments

All segments created in [!DNL Analytics] and published to Adobe CX Enterprise (formerly Adobe) Experience Cloud).

New segments take 24-48 hours to appear in Adobe Advertising. Updates to existing segments are synchronized within about eight hours.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Site engagement metrics

>[!NOTE]
>
>* [!DNL Analytics] passes events for the EF ID [!DNL eVar] into Adobe Advertising.  The default integration doesn&#39;t support sending calculated metrics or other dimensions ([!DNL eVars]) into Adobe Advertising. If the calculated metric can be wholly captured in a custom event, however, then Adobe Advertising can ingest the custom event.
>* [!DNL Analytics] passes data to Adobe Advertising hourly.

* [!UICONTROL Timespent_secs_1stvisit]: The number of seconds spent on the site during the visitor&#39;s first visit.
* [!UICONTROL Timespent_secs_total]: The total number of seconds spent on the site across all visits within the click lookback window.
* [!UICONTROL Pageviews_1stvisit]: The number of page views on the site during the visitor&#39;s first visit.
* [!UICONTROL Pageviews_total]: The total number of page views on the site across all visits within the click lookback window.
* [[!UICONTROL Bounces] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: The number of times that [!DNL Analytics] collected an [!UICONTROL EF ID].

## 转化量度

[!DNL Analytics] passes conversion metrics to Adobe Advertising daily.

### Standard conversion metrics

* [[!UICONTROL Revenue] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### Custom conversion metrics

These metrics are specific to the report suite, so the available metrics vary for each customer and report suite.

### Custom conversion metrics created from [!DNL eVars] and [!DNL Props]

The available metrics vary for each customer. See &quot;[Create Conversion Metrics from Adobe Analytics [!DNL eVars] and [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md).&quot;

### Reserved conversion metrics

These metrics are specific to the report suite, so the available metrics vary for each customer and report suite.

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising Metrics in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
