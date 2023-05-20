---
title: 在Adobe Target中設定AdobeAdvertising Ads的A/B測試
description: 瞭解如何在中設定A/B測試 [!DNL Target] 適用於您的DSP和 [!DNL Search, Social, & Commerce] 廣告。
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '1642'
ht-degree: 0%

---

# 在適用於Advertising DSP和的Adobe Target中設定A/B測試 [!DNL Advertising Search, Social, & Commerce] 廣告

<!-- Add [!UICONTROL and [!DNL tags throughout as needed. -->

<!-- Break into sub-files, or just leave as one? -->

*僅使用Advertising DSP的廣告商*

Adobe Advertising和Adobe Target可讓行銷人員更輕鬆地透過付費媒體和站上訊息提供個人化和連線的體驗。 透過在產品之間共用訊號，您可以：

* 將客戶在DSP促銷活動中的廣告曝光度連結至其網站上的體驗，以降低網站流失率。

* 透過使用Adobe Audience Manager曝光資料和點選摘要目標受眾映象廣告訊息的站上體驗，建立A/B測試。

* 使用Adobe Analytics中的簡單視覺效果來測量整合通訊對網站上的目標提升度的影響，以用於 [!DNL Target].

請參閱下列章節，瞭解必要條件和說明，瞭解如何設定點進和檢視追蹤，以及在DSP和之間實作訊號共用 [!DNL Target] 和設定A/B測試活動，以及設定 [!DNL Analytics] Analysis Workspace以檢視測試資料。

如果您有其他問題，請聯絡adcloud_support@adobe.com。

## 必要條件

此使用案例需要下列產品和整合：

* [!DNL Target]

* [[!DNL Analytics] 適用於廣告](/help/integrations/analytics/overview.md) 整合<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] 的 [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) 整合

* Audience Manager（僅對於閱覽測試為必要）

## 步驟1：設定點進架構 {#click-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![點進框架](/help/integrations/assets/target-ct-framework.png)

當您將DSP巨集新增至點進URL （使用者點按廣告並到達登陸頁面時顯示的URL）時，DSP會透過以下方式自動擷取位置索引鍵： `${TM_PLACEMENT_ID}` 點進URL中的。 此巨集會擷取英數字元版位索引鍵，而非數值版位ID。

![附加至登陸頁面URL的點進URL](/help/integrations/assets/target-ct-url.jpg)

### (僅限DSP)將DSP巨集新增至您的點進URL

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

在Flash交談或Google Campaign Manager 360中，手動更新每個廣告的點進URL，以包含擷取AMO ID變數所需的巨集。 AMO ID變數可用來將點按資料傳送至Adobe Analytics，以及分享A/B測試的放置索引鍵。 如需指示，請參閱下列頁面：

* [附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤](/help/integrations/analytics/macros-flashtalking.md)

* [附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Google Campaign Manager 360] 廣告標籤](/help/integrations/analytics/macros-google-campaign-manager.md)

請聯絡您的Adobe客戶團隊和Advertising Solutions Group (aac-advertising-solutions-group@adobe.com)，以擷取所需的位置索引鍵並完成設定，同時確保每個點進URL皆填入位置索引鍵。

## 步驟2：使用Audience Manager設定瀏覽框架 {#view-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![檢視框架](/help/integrations/assets/targetr-vt-framework.png)

您可以在廣告標籤和版位設定中新增Audience Manager曝光事件畫素，藉此建立測試區段以提供其他閱覽測試機會。

1. 在廣告標籤和DSP版位設定中實作Audience Manager曝光事件畫素。

   如需指示，請參閱&quot;[從Advertising DSP Campaigns收集媒體曝光資料](/help/integrations/audience-manager/media-data-integration/collect.md).」

   請務必新增 [DSP巨集](/help/dsp/campaign-management/macros.md) 擷取您想要曝光事件畫素傳回的所有資料，包括 `${TM_PLACEMENT_ID_NUM}` 以取得數值位置ID。

   >[!NOTE]
   >
   >點選追蹤URL包括 `${TM_PLACEMENT_ID}` 英數字元放置鍵的巨集，而非 `${TM_PLACEMENT_ID_NUM}` 以取得數值位置ID。

1. 從DSP曝光資料設定Audience Manager區段：

   1. 前往 **Audience Manager** > **對象資料** > **訊號**，然後選取 **搜尋** tab鍵。

   1. 輸入 **金鑰** 和 **值** 用於決定要將區段使用者分組到哪個層級的訊號。 使用 [支援的金鑰](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=en) 值與新增至Audience Manager曝光事件畫素的巨集相對應。

      例如，若要針對特定位置將使用者分組，請使用 `d_placement` 金鑰。 對於此值，請使用DSP巨集擷取的實際數值位置ID (例如上方熒幕擷取畫面中的2501853) `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

      如果「總計數」欄位顯示索引鍵/值組的使用者計數（這表示畫素已正確放置且資料正在流動），則您可以繼續下一個步驟。
   ![搜尋訊號](/help/integrations/assets/target-am-signals.png)

1. [建立規則型特徵](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) 用於在Audience Manager中建立區段。

   1. 為特徵命名，以便在測試活動中易於識別。 將特徵儲存在您偏好的任一資料夾中。

   1. 從 **資料來源** 下拉式功能表，選取 **Ad Cloud**.

   1. 在運算式產生器中，新增 `d_event` （在「金鑰」欄位中）及 `imp` 在 **值** 欄位，選取 **新增規則**，然後儲存特徵。

   ![規則型特徵熒幕擷圖](/help/integrations/assets/target-am-trait.png)

1. 設定Audience Manager的測試區段：

   1. 前往頁面頂端的 **對象資料** > **特徵** 和搜尋完整特徵名稱。 選取特徵名稱旁的核取方塊，然後按一下 **建立區段**.

   1. 為區段命名，選取 `Ad Cloud` 作為 **資料來源**，然後儲存區段。

      Audience Manager會自動將區段分割成控制群組，該控制群組接收標準登陸頁面體驗，而測試群組接收個人化的現場體驗。
   ![測試區段的熒幕擷圖](/help/integrations/assets/target-am-segment.png)

## 步驟3：在Target中設定「A/B測試」活動

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

下列指示會醒目提示與DSP使用案例相關的資訊。 如需完整指示，請參閱&quot;[建立A/B測試](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)「。

1. [登入Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. 從 **活動** 清單，按一下 **建立活動** > **A/B測試**.

   ![建立A/B測試活動](/help/integrations/assets/target-create-ab.png)

1. 在 **輸入活動URL***欄位，輸入測試的登入頁面URL。

   ![輸入活動URL欄位](/help/integrations/assets/target-create-ab-url.png)

   >[!NOTE]
   >
   >您可以使用多個URL來測試閱覽網站專案。 如需詳細資訊，請參閱「[多頁活動](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).」 您可以透過建立頁面URL輕鬆識別熱門專案 [網站專案報告](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) （在Analytics中）。

1. 在 **目標** 欄位中，輸入測試的成功量度。

   >[!NOTE]
   >
   >請確定 [!DNL Analytics] 在中啟用為資料來源 [!DNL Target]，且已選取正確的報表套裝。

1. 設定 **優先順序** 至 `High` 或 `999` 以防止測試區段中的使用者收到錯誤的站上體驗時發生衝突。

1. 範圍 **報表設定**，選取 **公司名稱** 和 **報表套裝** 已連線至您的DSP帳戶。

   如需其他報表秘訣，請參閱「[報告最佳實務與疑難排解](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).」

1. 在 **日期範圍** 欄位，輸入適當的測試開始與結束日期。

1. 將對象新增至活動：

   1. 選擇 [您先前在Audience Manager中建立的區段，用來測試閱覽對象](#view-through-framework).

      ![將對象新增至活動](/help/integrations/assets/target-create-ab-audiences.png)

   1. 選取 **網頁** > **登陸頁面** > **查詢**，然後輸入DSP放置索引鍵，在 **值** 欄位來使用點進對象的Target查詢字串引數。

      ![目標點按對象熒幕擷圖](/help/integrations/assets/target-click-audience.jpg)

1. 對於 **流量分配方法**，選取 **手動（預設）** 並以50/50的比例分割對象。

1. 儲存活動。

1. 使用 [!DNL Target] [視覺化體驗撰寫器](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) 以變更A/B測試登入頁面範本的設計。

   * 體驗A：請勿編輯，因為這是沒有個人化的預設/控制登陸頁面體驗。

   * 體驗B：使用 [!DNL Target] 使用者介面，可根據測試中包含的資產自訂登入頁面範本（例如標題、復本、按鈕位置和創意）。
   >[!NOTE]
   >
   >例如，創意測試使用案例，請聯絡您的Adobe客戶團隊。

## 步驟4：設定您的 [!DNL Analytics for Target] Analysis Workspace於 [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T)是跨解決方案的整合，可讓廣告商建立 [!DNL Target] 活動依據 [!DNL Analytics] 轉換量度和受眾區段，然後使用測量結果 [!DNL Analytics] 作為報表來源。 該活動的所有報告和區段都根據 [!DNL Analytics] 資料彙集。

如需有關的詳細資訊 [!DNL Analytics for Target]，包括實作指示的連結，請參閱&#39;[Adobe Analytics作為Adobe Target (A4T)的報表來源](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)「。

### 設定 [!DNL Analytics for Target] 面板

在Analysis Workspace中，設定 [!DNL Analytics for Target panel] 分析 [!DNL Target] 活動和體驗。 請牢記以下有關報表的重要指標與資訊。

#### 量度

* 在執行測試的Adobe廣告行銷活動、套件或版位專屬的工作區中建立面板。 使用摘要視覺效果，在與Target測試效能相同的報表中顯示Adobe廣告量度。

* 優先使用網站上的量度（例如造訪和轉換）來測量效能。

* 瞭解Adobe廣告的彙總媒體量度（例如曝光數、點按數和成本）無法與Target量度比對。

#### Dimension

下列維度與 [!DNL Analytics for Target]：

* **Target活動**： A/B測試的名稱

* **Target體驗**：活動內使用的登陸頁面體驗名稱

* **Target活動** > **體驗**：相同列中的活動名稱和體驗名稱

### 疑難排解Analytics for [!DNL Target] 資料

在Analysis Workspace中，如果您發現活動和體驗資料很少或未填入，請執行以下操作：

* 確認Target和Analytics使用相同的補充資料ID (SDID)。 您可以使用驗證SDID值 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) 在促銷活動帶動使用者的登陸頁面上。

[Adobe Debugger中的補充資料ID (SDID)值](/help/integrations/assets/target-troubleshooting-sdid.png)

* 在相同的登陸頁面上，確認a) 「解決方案> Target」底下「Adobe除錯程式」中顯示的主機名稱符合b)中顯示的追蹤伺服器 [!DNL Target] （在「目標與設定>報表設定」底下）。

   [!DNL Analytics For Target] 需要 [!DNL Analytics] 要透過呼叫傳送的追蹤伺服器 [!DNL Target] 至 [!DNL Modstats] Analytics的資料收集伺服器。<!-- just "to Analytics?"-->

[Adobe偵錯工具中的主機名稱值](/help/integrations/assets/target-troubleshooting-hostname.png)

[Target中的追蹤伺服器值](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 進一步閱讀

* [將Target與Analytics整合](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) — 說明如何在Analysis Workspace中設定Target報表。
* [A/B測試概覽](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html)  — 說明可搭配DSP廣告使用的A/B測試活動。
* [體驗與選件](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html)  — 說明 [!DNL Target] 用於判斷DSP測試使用者會接觸到哪些網站內容的工具。
* [訊號、特徵和區段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html)  — 定義有助於進行DSP閱覽測試的一些Audience Manager工具。
* [Analytics for Advertising概述](/help/integrations/analytics/overview.md)  — 引進Analytics for Advertising，可讓您追蹤Analytics執行個體中的點進和檢視網站互動。

<!-- 
>[!MORELIKETHIS]
>
>* 
-->
