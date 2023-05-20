---
title: 關於Advertising DSP中的對象管理
description: 瞭解對象管理功能。
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# 關於Advertising DSP中的對象管理

在DSP中，您可以建立和管理受眾區段和受眾集，並可將它們當作您的刊登版位目標：

* 您可以透過建立及實作區段來收集您自己的第一方對象資料。 您稍後可以使用廣告重新鎖定區段中的使用者，或避免區段中的使用者接收廣告。 您可以建立下列型別的區段：

   * [自訂區段](/help/dsp/audiences/custom-segment-create.md) 追蹤a)從桌上型電腦、行動裝置和CTV裝置接觸到廣告的使用者，以及b)造訪特定網頁的使用者。

   * [CCPA選擇退出銷售區段](/help/dsp/audiences/ccpa-opt-out-segment-create.md) 若要根據加州消費者隱私法(CCPA)追蹤網站上消費者選擇退出銷售請求的使用者ID。 您可以從選擇退出銷售請求中擷取使用者ID的每月報表。

      如需有關CCPA選擇退出銷售請求的Adobe廣告支援的詳細資訊，請參閱 [加州消費者隱私法的Adobe廣告支援：消費者選擇退出支援](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* 您可以建立的對象庫 [可重複使用的對象](/help/dsp/audiences/reusable-audience-create.md). 已儲存的對象是由任何可用的對象區段和任何其他已儲存的對象所組成。 您對已儲存對象所做的任何變更，都會自動套用至鎖定或排除對象的所有位置，以及包括已儲存對象的所有其他對象。

   儲存的對象可讓媒體計畫人員視需要將對象分組，方法是使用複雜的布林邏輯包含和排除多個區段。 當您建立受眾時，會指出每個個別區段的大小和受眾總人數。 然後，Campaign執行者只需選取一或多個儲存的對象作為位置目標，而非手動設定每個位置的對象目標。

位置鎖定目標也可使用其他對象型別。

## 匯入第一方和第三方資料區段

DSP可從您的資料管理平台(DMP)匯入您自己的第一方資料區段，並視需要將其提供給任何一組廣告商。

DSP是以下的整合目的地 [此 [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=zh-Hans)，可讓您與核准的廣告商和使用者共用已驗證的第一方區段，以利行銷活動啟動。 若要進一步瞭解Real-Time CDP整合，請參閱 [來源區段](/help/dsp/audiences/sources/source-about.md).

DSP也可以匯入自訂的第三方區段，包括第三方區段的複雜組合。 您可以視需要將這些區段提供給任何一組廣告商。

如需詳細資訊，請聯絡您的Adobe客戶團隊。

## 可作為放置目標的對象

您可以將版位鎖定在下列所有型別的對象上。

* 所有使用者建立且儲存在DSP中的對象集。

* 在DSP中建立的所有使用者建立的受眾區段：

   * 造訪特定網頁的使用者和接觸到特定廣告曝光次數的使用者的自訂區段。

   * CCPA選擇退出銷售對象區段，適用於根據加州消費者隱私法(CCPA)在網站上提交選擇退出銷售請求的使用者。

* 所有匯入的第一方資料區段。

* 所有匯入的自訂第三方資料區段。

* （僅限美國地區的位置） [30多家供應商的DSP客戶可使用所有協力廠商資料區段](/help/dsp/audiences/third-party-data-providers.md)，包括 [!DNL Acxiom]， [!DNL Datalogix]， [!DNL eXelate] ([!DNL Nielsen])， [!DNL Lotame]， [!DNL Oracle]， [!DNL Quantcast]、以及其他更多專案。

   您可以鎖定特定區段，根據對象資料鎖定使用者（例如，具有特定人口統計、興趣或意圖和/或行為設定檔的使用者）。 您可以依資料提供者和類別瀏覽、依名稱或區段ID搜尋區段，或依資料提供者、區段總大小、網頁瀏覽器計數或裝置計數篩選結果。

   第三方區段會產生額外費用，這些費用會顯示在每個區段名稱旁邊。

* (使用Adobe Experience Platform和的廣告商 [!DNL Real-Time CDP]、Adobe Audience Manager或Adobe Analytics (僅使用AdobeAdvertising JavaScript轉換標籤)您所有可用的第一方、第二方或第三方受眾區段，建立於 [!DNL Real-Time CDP]，在Audience Manager中建立，或從Audience Manager發佈至Adobe Experience Cloud或 [!DNL Analytics].

   使用區段的定價是預先議定的，在DSP中不可見。

   區段來源 [!DNL Analytics] 會在您建立或發佈為Experience Cloud對象約一小時後提供。 直接來自Audience Manager或的區段 [!DNL Real-Time CDP] 共用後24小時內即可使用。

   >[!NOTE]
   >
   >請參閱以下檔案： [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html)， [分析](https://experienceleague.adobe.com/docs/analytics.html)、和 [此 [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) 瞭解如何為這些解決方案中的區段設定和收集資料。

## 對象人數資料

在儲存的對象設定和位置設定中，您可以檢視詳細的對象人數資料：

* 系統會顯示所有選定區段和儲存對象中的總計和作用中重複資料刪除對象人數，您可以依裝置型別（瀏覽器、行動或連線電視）檢視詳細資料。

   ![合併的對象人數](/help/dsp/assets/audience-size.png)

* 若為個別區段和儲存的對象，對象總人數和CPM （若適用）會顯示在區段名稱旁。 您可以檢視區段的詳細資訊，包括依裝置型別（瀏覽器、行動或連線電視）區分的大小。 對於儲存的對象，總大小是重複資料刪除總數。

   ![個別區段大小](/help/dsp/assets/audience-size-segment.png)

## 對象檢視

### 所有對象檢視

在 [!UICONTROL All Audiences] 檢視或對象庫，您可以儲存和管理可重複使用的對象，其中包括對象區段群組，甚至其他儲存的對象。 您可以使用對象作為多個版位的目標。 版位名稱旁會指出使用每個對象的版位數量。

您可以編輯、複製、刪除、匯出或共用任何對象。

### 區段檢視

在 [!UICONTROL Segments] 檢視，所有使用者都可以建立其他自訂區段。

此 [!UICONTROL Segments] 「檢視」也會列出下列區段型別：

* 所有使用者建立的自訂區段皆可供使用者使用。

   您可以檢視您建立的任何自訂區段的追蹤標籤，並和其他使用者共用這些區段。 您也可以編輯或刪除您建立的自訂區段。

   您無法編輯或共用其他使用者與您共用的自訂區段。

* 使用者可以使用所有匯入的第一方區段。

   您無法編輯或共用與您共用的第一方區段。 如果您需要與其他使用者共用第一方區段，請聯絡您的Adobe客戶團隊。

* 所有可供使用者使用的自訂第三方區段。

   您無法編輯或共用與您共用的第三方區段。 如果您需要與其他使用者共用協力廠商區段，請聯絡您的Adobe客戶團隊。

>[!MORELIKETHIS]
>
>* [建立可重複使用的對象](reusable-audience-create.md)
>* [對象設定](audience-settings.md)
>* [對象區段邏輯的語法](audience-segment-logic-syntax.md)
>* [建立及實作自訂區段](custom-segment-create.md)
>* [建立及實作 [!UICONTROL CCPA Opt-Out-of-Sale] 區段](ccpa-opt-out-segment-create.md)
>* [可用的第三方資料提供者](third-party-data-providers.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)

