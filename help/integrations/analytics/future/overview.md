---
title: AdobeAdvertising與Adobe Analytics的整合
description: 瞭解Adobe廣告如何與Adobe Analytics交換資料，以及如何在Search、Social和Commerce中使用資料。
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 06996ee9eb635fe204c0c3938e6937e8871c8a90
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# AdobeAdvertising與Adobe Analytics的整合

您可以透過下列方式整合Adobe Advertising與Analytics。

## 在之間交換資料 [!DNL Analytics] 和Adobe廣告

### 提取 [!DNL Analytics] 將資料匯入Adobe廣告

替換為 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)，[!DNL Search, Social, & Commerce] 和DSP拉入：

* **[!DNL Analytics]區段：**  在中建立之所有廣告商或代理商區段的中繼資料、階層資料和唯一受眾資料 [!DNL Analytics] 並發佈至Experience Cloud。

* **[!DNL Analytics]網站參與量度**

* **[!DNL Analytics]標準、自訂和保留量度**

### 傳送Adobe廣告資料至 [!DNL Analytics]

* **Adobe廣告的流量量度**

* **來自Adobe廣告的Dimension**

>[!NOTE]
>
>對象 [!DNL Search, Social, & Commerce]，大部分的廣告網路和行銷活動型別都支援此功能。 請參閱「 」中的「支援的詳細目錄」 [!DNL Search, Social, & Commerce] 指南，以取得詳細資訊。<!-- add link when that's published in ExL -->

### 使用 [!DNL Analytics] 要建立的區段 [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*選擇加入的廣告商，搭配 [!DNL Advertising Search, Social, & Commerce] 僅限*

<!-- Verify all -->

範圍 [!DNL Search, Social, & Commerce]，您可以建立 [!DNL Google Ads] Google客戶使用您現有的從使用者ID比對對象 [!DNL Analytics] 區段。 這包括發佈至Adobe Experience Cloud的Adobe Analytics區段，以及使用Adobe Experience Cloud建立的區段 [!DNL Audience Library]. 如需詳細資訊，請參閱產品內說明： [!DNL Search, Social, & Commerce].

[來自使用者ID的客戶比對對象](https://support.google.com/google-ads/answer/9199250) 類似網站標籤型受眾的運作方式，但會將非PII ID指派給不重複受眾成員，以獲得比標準客戶比對和網站標籤型受眾更鮮明的好處。

若要建立必要的使用者ID，您必須使用Adobe廣告JavaScript標籤 <!-- with a user ID parameter -->在您的網站上。 如需詳細資訊，請聯絡您的Adobe客戶團隊。

![區段建立流程](/help/integrations/assets/ad_search_user_id_pic.png)

建立受眾後，您便可以在以下位置使用它們： [!DNL Google Ads] 行銷活動為 [行銷活動層級或廣告群組層級目標或排除專案](#audience-manager-targets).

### 使用 [!DNL Analytics] 要鎖定或排除廣告的區段 {#analytics-targets}

* (選擇加入的廣告商，搭配 [!DNL Search, Social, & Commerce])您可以使用任何 [!DNL Google Ads] 曾經是 [建立方式 [!DNL Analytics] 區段](#audience-manager-google-audiences) 作為中的行銷活動層級或廣告群組層級目標或排除專案 [!DNL Google Ads] 行銷活動。

* (使用DSP的廣告商)您可以使用現有的 [!DNL Analytics] 區段作為廣告投放的目標。 您可以選擇將區段納入可重複使用的對象中，將其用作多個位置的目標或排除專案。

* （廣告商與Advertising Creative）您可以使用現有的 [!DNL Analytics] 區段作為廣告體驗中特定創意專案的目標。
