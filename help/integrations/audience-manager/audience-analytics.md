---
title: '''[!DNL Adobe] [!DNL Audience Analytics] 適用於Adobe廣告客戶的'
description: 瞭解如何使用 [!DNL Adobe] [!DNL Audience Analytics] 適用於廣告使用案例
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] 適用於Adobe廣告客戶

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) 是Adobe Audience Manager與Adobe Analytics之間的整合，可讓Audience Manager客戶將區段傳送至 [!DNL Analytics] 以取得有關網站活動的深入分析。

Adobe廣告客戶可藉由使用 [!DNL Audience Analytics]. 整合可讓您：

* 將Adobe廣告曝光度資料直接傳送至 [!DNL Analytics] 以判斷上層漏斗活動對下游網站活動的影響。

* 從上層漏斗曝光度廣告中判斷行銷管道和網站進入點。

* 將整合與分層 [!DNL Analytics for Advertising] 若要從合併協力廠商人口統計區段 [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) 替換為 [!DNL Analytics for Advertising] 以取得使用者個人資料的更多深入分析。

   [!DNL Audience Marketplace] 透過「啟動」訂閱模式提供對第三方資料摘要的存取權，這可讓購買者將資料傳送至目的地。 如果資料用於 [!DNL Analytics] 目的地，則不會收取啟用費。

* (使用Advertising DSP的廣告商)新增其他曝光區段，以獲得整體歷程管理見解。

   Advertising DSP可以透過實作Adobe Experience Platform或Audience Manager曝光追蹤畫素，將曝光資料當作可操作的訊號傳送給Audience Manager。 將相同資料轉送至 [!DNL Analytics] 啟用進階資料分析。 請參閱「[Adobe Advertising Media資料與Adobe Audience Manager整合概述](/help/integrations/audience-manager/media-data-integration/overview.md)」以取得詳細資訊。

如需有關的詳細資訊 [!DNL Audience Analytics]，包括其先決條件和工作流程，請參閱&quot;[Audience Analytics概觀](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).」

## 使用方式範例 [!DNL Audience Analytics] 包含Adobe廣告資料的資料

以下是如何在中使用合併資料的範例。 [!DNL Analytics] [!DNL Analysis Workspace].

### 檢視上層漏斗活動對下游活動的影響

使用Audience Manager曝光區段來檢視上層漏斗網站活動對下游網站活動的影響。 在追蹤畫素中加入Adobe廣告或協力廠商巨集ID，以追蹤對詳細層級的影響，從促銷活動層級到使用者公開所在的網站層級。

主要優點：

* 依漏斗/廣告型別追蹤曝光度並使用 [!DNL Audience Analytics] 以判斷進入率以及與客戶歷程下一階段的重疊。

* 判斷上層漏斗活動對下游網站活動的影響。

* Connect [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> 和 [!DNL Audience Analytics] 資料 <!-- (which includes the user's last exposure event) --> 以決定網站的整體歷程。

以下是您可在中建立的報表範例 [!DNL Analysis Workspace].

![檢視上層漏斗活動對下游網站活動的影響](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### 使用 [!DNL Audience Analytics] 使用者設定檔分析的第三方區段資料

使用協力廠商Audience Manager區段，以更全面分析使用者如何與您的網站互動。 您可以使用資訊，根據來自第三方區段的設定檔與媒體行銷活動網站的關鍵績效指標互動的方式，決定要為其啟用媒體的新第三方對象。

>[!TIP]
> 使用Audience Manager `Audiences ID` 和 `Audiences Name` 維度 [!DNL Analytics]，與其他任何維度一樣， [!DNL Analytics] 收集。

以下是您可在中建立的報表範例 [!DNL Analysis Workspace].

![使用協力廠商區段來豐富使用者設定檔分析](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [AdobeAdvertising與Adobe Audience Manager的整合](/help/integrations/audience-manager/overview.md)

