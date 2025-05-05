---
title: '[!DNL Analytics]数据Adobe Advertising'
description: '[!DNL Analytics]数据Adobe Advertising'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Adobe Advertising中的[!DNL Analytics]数据

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

## Analytics区段

在[!DNL Analytics]中创建并发布到Experience Cloud的所有区段。

新区段需要24-48小时才能在Adobe Advertising中显示。 现有区段的更新会在大约八小时内同步。

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## 网站参与量度

>[!NOTE]
>
>* [!DNL Analytics]将EF ID [!DNL eVar]的事件传递到Adobe Advertising。  默认集成不支持将计算量度或其他维度([!DNL eVars])发送到Adobe Advertising中。 但是，如果计算指标可以在自定义事件中完全捕获，则Adobe Advertising可以摄取自定义事件。
>* [!DNL Analytics]每小时将数据传递给Adobe Advertising。

* [!UICONTROL Timespent_secs_1stvisit]：访客首次访问期间在网站上逗留的秒数。
* [!UICONTROL Timespent_secs_total]：在点击回顾时间范围内，所有访问在网站上花费的总秒数。
* [!UICONTROL Pageviews_1stvisit]：访客首次访问期间网站上的页面查看次数。
* [!UICONTROL Pageviews_total]：在点击回顾时间范围内，网站上所有访问的总页面查看次数。
* [[!UICONTROL Bounces]量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html?lang=zh-Hans)
* [[!UICONTROL Visits]量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html?lang=zh-Hans)
* [!UICONTROL ef_id_instances]： [!DNL Analytics]收集[!UICONTROL EF ID]的次数。

## 转化量度

[!DNL Analytics]每天将转化指标传递给Adobe Advertising。

### 标准转化量度

* [[!UICONTROL Revenue]量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html?lang=zh-Hans)
* [[!UICONTROL Orders]量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html?lang=zh-Hans)
* [[!UICONTROL Units]量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html?lang=zh-Hans)
* [[!UICONTROL Carts]量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html?lang=zh-Hans)
* [[!UICONTROL Cart Views]量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html?lang=zh-Hans)
* [[!UICONTROL Checkouts]量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html?lang=zh-Hans)
* [[!UICONTROL Cart Additions]量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html?lang=zh-Hans)
* [[!UICONTROL Cart Removals]量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html?lang=zh-Hans)

### 自定义转化量度

这些指标特定于报表包，因此每个客户和报表包的可用指标会有所不同。

### 从[!DNL eVars]和[!DNL Props]创建的自定义转化量度

每个客户的可用量度各不相同。 请参阅“[从Adobe Analytics创建转化量度 [!DNL eVars] 和 [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)”。

### 保留的转化量度

这些指标特定于报表包，因此每个客户和报表包的可用指标会有所不同。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* 在Analysis Workspace中[Adobe Advertising指标](/help/integrations/analytics/advertising-metrics-in-analytics.md)
