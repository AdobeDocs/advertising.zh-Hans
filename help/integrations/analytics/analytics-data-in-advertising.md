---
title: ’[!DNL Analytics] Adobe Advertising中的数据
description: ’[!DNL Analytics] Adobe Advertising中的数据
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# [!DNL Analytics] Adobe Advertising中的数据

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

## Analytics区段

在中创建的所有区段 [!DNL Analytics] 并发布到Experience Cloud。

新区段需要24-48小时才能在Adobe Advertising中显示。 现有区段的更新会在大约八小时内同步。

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## 网站参与量度

>[!NOTE]
>
>* [!DNL Analytics] 传递EF ID的事件 [!DNL eVar] Adobe Advertising。  默认集成不支持发送计算量度或其他维度([!DNL eVars])到Adobe Advertising中。 但是，如果计算指标可以在自定义事件中完全捕获，则Adobe Advertising可以摄取自定义事件。
>* [!DNL Analytics] 每小时将数据传递给Adobe Advertising。

* [!UICONTROL Timespent_secs_1stvisit]：访客首次访问期间在网站上逗留的秒数。
* [!UICONTROL Timespent_secs_total]：在点击回顾时间范围内，所有访问在网站上逗留的总秒数。
* [!UICONTROL Pageviews_1stvisit]：访客首次访问期间网站上的页面查看次数。
* [!UICONTROL Pageviews_total]：在点击回顾窗口内网站所有访问的总页面查看次数。
* [[!UICONTROL Bounces] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]：表示该事件发生的次数 [!DNL Analytics] 已收集 [!UICONTROL EF ID].

## 转化量度

[!DNL Analytics] 将转化指标传递到每日Adobe Advertising。

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

### 自定义转化量度创建自 [!DNL eVars] 和 [!DNL Props]

每个客户的可用量度各不相同。 请参阅&quot;[从Adobe Analytics创建转化量度 [!DNL eVars] 和 [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)“

### 保留的转化量度

这些指标特定于报表包，因此每个客户和报表包的可用指标会有所不同。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [Analysis Workspace中的Adobe Advertising指标](/help/integrations/analytics/advertising-metrics-in-analytics.md)
