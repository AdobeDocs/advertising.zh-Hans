---
title: 概述 [!DNL Analytics for Advertising]
description: 概述 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 0%

---

# 概述 [!DNL Analytics for Advertising]

*使用Advertising DSP和的廣告商[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] 整合Adobe Analytics和Adobe廣告，以擴充和增強每個產品的功能。

整合可讓廣告商追蹤其網站中的點進和檢視互動 [!DNL Analytics] 例項，讓品牌瞭解其廣告支出如何帶來網站參與度和關鍵業務目標。

此外，Adobe廣告可存取大量第一方資料，而且 [!DNL Analytics] 收集使用 [!DNL Analytics] 標籤已存在於網站上。 這可提供更強大的歷程管理、第一方再行銷和付費媒體網站報告。 Adobe廣告可進一步使用 [!DNL Analytics] 支出和競標最佳化的資料。

若僱用得當， [!DNL Analytics for Advertising] 模糊兩個傳統角色之間的界限：廣告歷程管理（透過廣告將使用者送往網站的行為）和透過網站分析瞭解網站參與。

主要優點：

* 傳送 [!DNL Analytics] 區段直接Adobe廣告以進行第一方網站再行銷。
* 使用 [!DNL Analytics] 自訂和標準事件作為轉換訊號，用於最佳化付費媒體廣告。
* 充分利用 [!DNL Analytics] Analysis Workspace以更清楚瞭解網站進入點和造訪行為。
* 讓網頁分析人員與付費媒體團隊之間更緊密地共同作業。
* 在中使用永久AdobeAdvertising瀏覽和點進ID [!DNL Analytics] 以瞭解網站參與度。
* 將資料或畫素匯出至廣告伺服器或其他DSP時，無法透過自訂量度、自訂維度和網站活動來增強Analysis Workspace中的傳統付費媒體報表。
* 充分利用 [!DNL Analytics] 程式碼，用於Adobe廣告中的追蹤和最佳化。

>[!TIP]
>
> 觀看 [簡介影片 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## 使用Analytics製作付費媒體報表

[!DNL Analytics for Advertising] 允許您：

* 在中使用永久AdobeAdvertising瀏覽和點進ID [!DNL Analytics] 以瞭解網站參與度。
* 運用Analysis Workspace深入瞭解網站登入點和造訪行為。 您可以存取付費媒體維度和事件資料，其中包括Adobe廣告行銷活動實體名稱（包括版位和廣告）及其相關量度，例如點按數、曝光數和成本。

使用 [!DNL Analytics] 作為您的付費媒體報告工具，您的組織需要Experience Cloud登入才能存取Analysis Workspace。 您的Adobe廣告團隊將幫助您將Adobe廣告資料對應到Analysis Workspace中的個別報表套裝。 您可以將Adobe Advertising資料傳送至任何報表套裝，但您應留意已對應至Adobe Advertising及尚未對應的報表套裝。依報表套裝而定，這可能會變更報告的資料。

[Adobe廣告ID於 [!DNL Analytics]](ids.md) 其運作方式與其他eVar類似，具有自訂的持續有效期。 根據預設，歸因回顧期間會設定為60天(在Adobe廣告實施期間)。 若要變更此設定，請與您的Adobe帳戶團隊合作。

Adobe廣告維度會附加尾碼「(AMO ID)」(例如「廣告型別(AMO ID)」)。 請參閱「[在Analysis Workspace中Adobe廣告量度](advertising-metrics-in-analytics.md)」以取得可用維度的清單。

>[!NOTE]
>
> 當您在中檢視Adobe廣告資料（或任何資料集）時 [!DNL Analytics]，請注意，量度和報表是根據在中設定的規則 [!DNL Analytics]. 資料可能會與您在其他報表系統中看到的不同，例如廣告伺服器報表、 [!DNL DSP] 報表或搜尋引擎報表。 若要瞭解中的資料差異 [!DNL Analytics]，您必須知道eVar資料何時過期、造訪的定義專案、被視為上次接觸歸因與總持續歸因的專案，以及其他因素。 如需詳細資訊，請參閱 [預期資料差異： [!DNL Analytics] 和Adobe廣告](data-variances.md).

## 使用Analytics來增強Adobe廣告促銷活動和Portfolio

不需要任何額外的畫素， [!DNL Analytics for Advertising] 透過傳送兩個主要訊號至Adobe廣告，實現更佳的最佳化及更輕鬆的受眾細分：

* 要當作競標訊號使用的轉換量度：
   * 標準量度，例如 [!UICONTROL Revenue] 和 [!UICONTROL Cart Views].
   * 網站參與量度，例如頁面檢視和造訪量度。
   * 自訂收入量度。
   * 保留的收入量度。
* 在中建立的區段 [!DNL Analytics] 並發佈至Experience Cloud。

   您可以使用 [!DNL Analytics] 中用於第一方網站重新定位的區段 [!DNL DSP] 和付費搜尋廣告。

   ([!DNL Search, Social, & Commerce] 僅限)廣告商，具有 [!DNL Analytics] 但非Audience Manager也可以從以下專案建立Google網站標籤型對象（再行銷清單）和客戶比對對象（客戶清單） [!DNL Analytics] 與Experience Cloud共用的區段。

### 網站轉換量度做為競標訊號

標準事件和自訂事件可使用來自 [!DNL Analytics] 在Adobe廣告中建立加權目標。 目標為下列專案的競標決策提供資訊： [!DNL DSP] 套件和搜尋產品組合。

>[!NOTE]
>
> 您無法從對應計算量度 [!DNL Analytics] Adobe廣告。

您的Adobe廣告團隊將協助您識別適用於付費媒體效能的事件，並將其對應至Adobe廣告，這些事件會顯示於 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

請參閱「[Adobe廣告中的Analytics量度](analytics-data-in-advertising.md)」以取得可用量度的清單。

### 網站重新目標定位的Analytics區段

Adobe廣告可以內嵌 [!DNL Analytics] Advertising DSP和再行銷用途的區段 [!DNL Search, Social, & Commerce] 使用原生Experience Cloud的廣告受眾整合，介於 [!DNL Analytics] 和Experience Cloud。

若要存取 [!DNL Analytics] 區段，廣告商帳戶必須具備 [Experience CloudID服務](https://experienceleague.adobe.com/docs/id-service/using/home.html) 已啟用。 ID服務啟用時，所有Experience Cloud區段(包括在 [!DNL Analytics] 並發佈至Experience Cloud、在Adobe Audience Manager中建立的區段，以及使用在Experience Cloud中建立的區段 [!DNL People core service]、以及在Adobe Experience Platform中建立並透過Audience Manager傳送至Adobe廣告的區段)一經處理，即可在Adobe廣告中使用。

[!DNL Analytics] 區段可在24小時內使用，並每日更新。

如需Experience Cloud Audiences服務的詳細資訊，請參閱 [Experience Cloud對象](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## 如何使用整合的範例

### 在Analysis Workspace中使用Adobe廣告資料

若要瞭解如何使用Adobe廣告資料在Analysis Workspace中建立視覺報表，請參閱影片」[Workspace和報表簡介](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).」

### 建立AdobeAdvertising儀表板

若要瞭解如何根據Analysis Workspace中的目標追蹤您的Adobe廣告資料，請參閱影片」[使用Adobe Analytics建立Adobe Advertising儀表板](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html).」

### 將Adobe廣告ID用於網站專案分析

若要瞭解如何建立Adobe廣告網站專案報告，以監控一週中的某天、一天中的某一時刻、瀏覽器和地理影響，請參閱影片」[建立Adobe廣告網站專案報表](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html).」

>[!MORELIKETHIS]
>
>* [影片：簡介 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [實作的必要條件和關鍵資訊 [!DNL Analytics for Advertising]](prerequisites.md)
>* [AdobeAnalytics使用的廣告ID](ids.md)
>* [Analytics for Advertising的JavaScript程式碼](/help/integrations/analytics/javascript.md)
>* [預期資料差異： [!DNL Analytics] 和Adobe廣告](data-variances.md)
>* [在Analysis Workspace中Adobe廣告量度](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe廣告中的資料](/help/integrations/analytics/analytics-data-in-advertising.md)

