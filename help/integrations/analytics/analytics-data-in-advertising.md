---
title: ‘[!DNL Analytics] Adobe广告中的数据
description: ‘[!DNL Analytics] Adobe广告中的数据
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: c6ed3277873f5c4a75fc19480b0ec77ab4110d7b
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# [!DNL Analytics] Adobe广告中的数据

*仅具有AdobeAdvertising-Adobe Analytics集成的广告商*

## Analytics区段

在中创建的所有区段 [!DNL Analytics] 并发布到Experience Cloud。

新区段需要24到48小时才能在Adobe广告中显示。 现有区段的更新会在大约8小时内同步。

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## 网站参与量度

>[!NOTE]
>
>* [!DNL Analytics] 将EF IDeVar的事件传递到Adobe广告中。  默认集成不支持将计算量度或其他维度(eVar)发送到Adobe广告中。 但是，如果计算量度可以完全捕获到自定义事件中，则Adobe广告可以摄取自定义事件。
>* [!DNL Analytics] 每小时将数据传递给Adobe广告。


* [!UICONTROL Timespent_secs_1stvisit]：访客首次访问期间在网站上逗留的秒数。
* [!UICONTROL Timespent_secs_total]：在点击回顾时间范围内，所有访问在网站上逗留的总秒数。
* [!UICONTROL Pageviews_1stvisit]：访客首次访问期间网站上的页面查看次数。
* [!UICONTROL Pageviews_total]：在点击回顾时间范围内，网站上所有访问的页面查看总数。
* [[!UICONTROL Bounces] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]：表示该事件发生的次数 [!DNL Analytics] 已收集 [!UICONTROL EF ID].

## 转化量度

[!DNL Analytics] 每天将转化量度传递到Adobe广告。

### 标准转化量度

* [[!UICONTROL Revenue] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### 自定义转化量度

这些指标特定于报表包，因此每个客户和报表包的可用指标会有所不同。

### 保留的转化量度

这些指标特定于报表包，因此每个客户和报表包的可用指标会有所不同。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [Analysis Workspace中的Adobe广告量度](/help/integrations/analytics/advertising-metrics-in-analytics.md)

