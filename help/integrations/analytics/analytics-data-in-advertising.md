---
title: '''[!DNL Analytics] Adobe廣告中的資料'
description: '''[!DNL Analytics] Adobe廣告中的資料'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# [!DNL Analytics] Adobe廣告中的資料

*僅具有AdobeAdvertising-Adobe Analytics整合的廣告商*

## Analytics區段

在中建立的所有區段 [!DNL Analytics] 並發佈至Experience Cloud。

新區段需要24到48小時才會出現在Adobe廣告中。 現有區段的更新會在約八小時內同步。

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## 網站參與量度

>[!NOTE]
>
>* [!DNL Analytics] 會將EF IDeVar的事件傳遞至Adobe廣告。  預設整合不支援將計算量度或其他維度(eVar)傳送至Adobe廣告。 不過，如果計算量度可完全擷取在自訂事件中，則Adobe廣告可擷取自訂事件。
>* [!DNL Analytics] 會每小時傳遞資料給Adobe廣告。


* [!UICONTROL Timespent_secs_1stvisit]：訪客首次造訪期間在網站上逗留的秒數。
* [!UICONTROL Timespent_secs_total]：點按回顧期間所有造訪在網站上逗留的總秒數。
* [!UICONTROL Pageviews_1stvisit]：訪客首次造訪期間網站上的頁面檢視次數。
* [!UICONTROL Pageviews_total]：點按回顧期間所有造訪的網站頁面檢視總次數。
* [[!UICONTROL Bounces] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]：相較於上次更新的 [!DNL Analytics] 已收集一個 [!UICONTROL EF ID].

## 轉換量度

[!DNL Analytics] 將轉換量度傳遞至每日Adobe廣告。

### 標準轉換量度

* [[!UICONTROL Revenue] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### 自訂轉換量度

這些量度是報表套裝專用，因此每個客戶和報表套裝的可用量度會有所不同。

### 保留的轉換量度

這些量度是報表套裝專用，因此每個客戶和報表套裝的可用量度會有所不同。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [在Analysis Workspace中Adobe廣告量度](/help/integrations/analytics/advertising-metrics-in-analytics.md)

