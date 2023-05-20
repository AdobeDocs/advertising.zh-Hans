---
title: 實作的必要條件和關鍵資訊 [!DNL Analytics for Advertising]
description: 實作的必要條件和關鍵資訊 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# 實作的必要條件和關鍵資訊 [!DNL Analytics for Advertising]

*使用Advertising DSP和的廣告商[!DNL Advertising Search, Social, & Commerce]*

在將Adobe Advertising與Adobe Analytics整合之前，請先檢閱下列資訊。

## 在中報告Adobe廣告資料的需求 [!DNL Analytics]

* 下列其中一項：
   * Adobe Experience Platform Web SDK： `alloy.js`
   * Experience Cloud身分識別服務： `visitorAPI.js` 2.0版或更新版本
* 任何版本的Adobe Analytics (包括 [!DNL Prime]， [!DNL Premium]，或 [!DNL Ultimate])
* Adobe Analytics： `appMeasurement.js` 2.1版或更新版本

>[!TIP]
>
>若要改善資料保真度，請使用每個程式庫的最新版本。

## 與Adobe廣告共用Analytics區段的要求

* Experience Cloud身分識別服務： `visitorAPI.js` 2.1版或更新版本
* Adobe Analytics： `appMeasurement.js` 1.8版或更新版本

## 報告需求 [!DNL Analytics] Adobe廣告中的資料

向Adobe Advertising實作團隊提供下列內容：

* 此 [!DNL Analytics] 報表套裝ID將用於付費媒體活動的報表，以及用於饋送網站活動，以最佳化及報告Adobe廣告
* 公司的Experience Cloud組織ID （組織ID）。

您可以在以下網址找到這兩個ID： [Adobe Experience Cloud Debugger的「摘要」標籤](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Experience Cloud Debugger摘要畫面](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Adobe廣告中的資料 {#lookback-a4adc}

因為 [!DNL Analytics] 資料會傳送至Adobe Advertising以進行報告和最佳化，資料受限於為Adobe Advertising中的廣告商設定的歸因規則，包括曝光次數和點選回顧期間。

![Adobe廣告中的廣告商層級回顧期間設定](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe廣告歸因點按回顧視窗：首次點按發生後的天數，在此期間點按可歸因於轉換。 預設值為60天，最大值為90天
* Adobe廣告歸因曝光回顧期間：發生廣告曝光後的天數，該曝光可歸因於轉換。 預設值為14天，最大值為30天

   >[!NOTE]
   >
   > 曝光回顧期間專屬於Adobe廣告，而非 [!DNL Analytics for Advertising]，報告。

此 [!DNL Analytics for Advertising] JavaScript會使用這些設定來判斷多早會將瀏覽進入專案或網站的點進專案視為有效。 如需如何決定閱覽和點進的詳細資訊，請參閱「[AdobeAnalytics使用的廣告ID](ids.md).」

## 將廣告資料Adobe於 [!DNL Analytics]

[!DNL Analytics] 在Analytics點選中設定Adobe廣告ID (AMO ID)，受廣告商的eVar持續性設定限制，此設定同時適用於點進和檢視。 持續性設定是在AdobeAdvertising後端上設定，您的Adobe帳戶團隊可以加以變更。

* [!DNL Analytics for Advertising] eVar有效期：AMO ID預設為60天

>[!NOTE]
>
>若要針對不同時間範圍分段資料，您可以 [設定自訂區段](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) Analysis Workspace中的不同回顧期間。

## 支援的廣告環境

* 搜尋
* 顯示
* 視訊
* 線上視訊
* 原生

如需每個頻道中最新支援的廣告環境，請聯絡您的Adobe客戶團隊。

## 實作前須知

* Adobe Advertising實作團隊將設定整合。

* 此整合不需額外付費，伺服器呼叫也不會產生額外費用 [!DNL Analytics] 或Adobe廣告費用。

* [!DNL Analytics for Advertising] 與廣告伺服器無關：任何廣告伺服器都可發生瀏覽或點進，而網站專案時會產生適當的ID。

* 整合只會通過 [!DNL Analytics] 標準和自訂事件，用於Adobe廣告以最佳化後續付費媒體和廣告工作的競標。 未通過 [!DNL Analytics] 區段、計算量度和eVar來Adobe廣告以最佳化競標。

* Adobe廣告會在以下位置建立永久ID： [!DNL Analytics] 根據使用者進入網站前最後點選或檢視的廣告，根據 [點按和檢視回顧期間](#lookback-a4adc) 在Adobe Advertising中設定。 如果網站訪客的設定檔中同時具有兩種型別的網站專案互動，且點按在回顧期間內，則訪客的點進ID會覆寫網站報表的檢視ID。

* [!DNL Analytics for Advertising] Adobe Analytics中的轉換追蹤使用可設定的追蹤回顧期間（預設為60天）。 Adobe廣告報表會反映在此追蹤回顧期間結束時的網站轉換和參與。

* 支援所有廣告型別。 不過，並非所有廣告環境都受到支援。

   例如，不會追蹤已連線的TV (CTV)廣告，因為CTV中不會發生點按，而且同一部裝置上也不會發生轉換。 不過，如果在案頭環境中檢視廣告，則可能會追蹤某些瀏覽網站專案資料。

* [!DNL Analytics] 目前只會追蹤並歸因相同裝置上的訪客，才會轉換次數。

* [!DNL Analytics for Advertising] 不支援應用程式內閱覽轉換。

* 使用伺服器端轉送實作的廣告商不支援瀏覽追蹤 [!DNL Analytics].

### 補充ID

為網站實作Experience CloudIdentity服務後，包含來自下列專案的資料的點選 [!DNL Analytics] 或Adobe廣告包含補充ID。

範例： `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

為了進行準確的資料整合，使用者使用的所有Adobe廣告呼叫 [!DNL Analytics for Advertising] 傳送內容或記錄目標量度的活動必須具有對應的 [!DNL Analytics] 共用相同補充ID的點選。

當您在中進行疑難排解時 [!DNL Analytics]，請務必確認有適用的補充ID [!DNL Analytics] 點選。 在 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)，您可以在「Adobe廣告」標籤中看到此ID為 `sdid` 引數。

>[!NOTE]
>
> 此實作的運作方式類似於 [!DNL Analytics for Target] 整合。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [Analytics for Advertising的JavaScript程式碼](/help/integrations/analytics/javascript.md)

