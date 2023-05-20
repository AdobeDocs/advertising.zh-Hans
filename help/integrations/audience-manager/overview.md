---
title: AdobeAdvertising與Adobe Audience Manager的整合
description: 瞭解Adobe廣告與Adobe Audience Manager交換資料的各種方式。
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# AdobeAdvertising與Adobe Audience Manager的整合

您可以透過下列方式整合Adobe廣告與Audience Manager。

## 同步Audience Manager和其他 [!DNL Adobe] 廣告定位的區段

[!DNL Search, Social, & Commerce] 和DSP可以為廣告商或機構的所有廣告和其他來源提取中繼資料、階層資料和不重複受眾Audience Manager [!DNL Adobe] 對象。 此唯一連線僅適用於使用Adobe廣告的行銷人員。 請參閱「[匯入Adobe Audience Manager區段以鎖定廣告](/help/integrations/audience-manager/import-audiences.md).」

### 使用Audience Manager和其他 [!DNL Adobe] 要建立的區段 [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*選擇加入的廣告商，搭配 [!DNL Advertising Search, Social, & Commerce] 僅限*

範圍 [!DNL Search, Social, & Commerce]，您可以建立 [!DNL Google Ads] Google客戶會使用您現有Audience Manager區段，從使用者ID比對對象，且該區段具有 [!UICONTROL Adobe Media Optimizer (HTTP)] 和 [!UICONTROL Adobe Media Optimizer Batch Destination] 作為目的地。 ([!DNL Media Optimizer] 是以前的名稱 [!DNL Search, Social, & Commerce].) 這包括發佈至Adobe Experience Cloud的Adobe Analytics區段，以及使用Adobe Experience Cloud建立的區段 [!DNL Audience Library]. 如需詳細資訊，請參閱產品內說明： [!DNL Search, Social, & Commerce].

[來自使用者ID的客戶比對對象](https://support.google.com/google-ads/answer/9199250) 類似網站標籤型受眾的運作方式，但會將非PII ID指派給不重複受眾成員，以獲得比標準客戶比對和網站標籤型受眾更鮮明的好處。

若要建立必要的使用者ID，您必須使用Adobe廣告JavaScript標籤 <!-- with a user ID parameter -->在您的網站上。 如需詳細資訊，請聯絡您的Adobe客戶團隊。

![區段建立流程](/help/integrations/assets/ad_search_user_id_pic.png)

建立受眾後，您便可以在以下位置使用它們： [!DNL Google Ads] 行銷活動為 [行銷活動層級或廣告群組層級目標或排除專案](#audience-manager-targets).

### 使用Audience Manager和其他 [!DNL Adobe] 要鎖定或排除廣告的區段 {#audience-manager-targets}

* (選擇加入的廣告商，搭配 [!DNL Search, Social, & Commerce])您可以使用任何 [!DNL Google Ads] 曾經是 [建立方式 [!DNL Adobe] 區段](#audience-manager-google-audiences) 作為中的行銷活動層級或廣告群組層級目標或排除專案 [!DNL Google Ads] 行銷活動。

* (使用DSP的廣告商)您可以使用現有的 [!DNL Adobe] 區段作為廣告投放的目標。 您可以選擇將區段納入可重複使用的對象中，將其用作多個位置的目標或排除專案。

* （廣告商與Advertising Creative）您可以使用現有的 [!DNL Adobe] 區段作為廣告體驗中特定創意專案的目標。

>[!NOTE]
>
>如需如何在Audience Manager和Experience Cloud中建立對象的詳細資訊 [!DNL Audience Library] 介面以及不同對象型別的常見使用案例，請參閱&quot;[對象建立選項](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).」

## 將DSP媒體曝光資料傳送至Audience Manager

*僅使用DSP的廣告商*

具有Adobe Audience Manager的DSP客戶可使用畫素呼叫來Audience Manager，從廣告促銷活動擷取資料。 然後，您可以使用行銷活動資料來建立規則型特徵，您可將其用於定義新區段，以啟用各種DSP使用案例，例如更進階分段、頻率管理、行銷分析和報表深入分析。

請參閱「[傳送DSP Media Exposure資料至Adobe Audience Manager概述](/help/integrations/audience-manager/media-data-integration/overview.md)」以取得詳細資訊。

## 透過Audience Analytics獲得更豐富的網站活動見解

使用AdobeAdvertising客戶 [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) 可傳送追蹤Adobe廣告的資料和Audience Manager區段至 [!DNL Analytics] 以取得有關網站活動的深入分析。

如需詳細資訊，請參閱「[[!DNL Adobe Audience Analytics] 適用於Adobe廣告客戶](/help/integrations/audience-manager/audience-analytics.md).」
