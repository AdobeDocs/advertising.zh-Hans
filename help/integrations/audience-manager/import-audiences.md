---
title: 匯入Adobe Audience Manager區段以鎖定廣告
description: 瞭解如何匯入 [!DNL Adobe] Advertising DSP和使用Adobe Audience Manager搜尋的對象
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---

# 匯入Adobe Audience Manager區段以鎖定廣告

Advertising DSP和 [!DNL Advertising Search, Social, & Commerce] 每個系統都能提取廣告商或機構的所有中繼資料、階層資料和不重複受眾資料 [!DNL Adobe] 對象<!-- segments or audiences? Standardize terms per AAM's docs -->. 其中包括以下專案的資料：

* Adobe Audience Manager區段

* 發佈至Adobe Experience Cloud的Adobe Analytics區段

* 使用Adobe Experience Cloud建立的區段 [!DNL Audience Library]

* 在Adobe Experience Platform中建立並透過Audience Manager傳送至Adobe廣告的區段

若要存取 [!DNL Adobe] DSP中的對象或 [!DNL Creative]，您必須將對象匯入DSP。 若要存取 [!DNL Adobe] 中的對象 [!DNL Search, Social, & Commerce]，您必須將對象匯入 [!DNL Search, Social, & Commerce].

## 必要條件

* 廣告商必須實作 [此 [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) 2.0版或更新版本。 此 [!DNL Identity Service] 提供永續性的通用ID，可識別Experience Cloud所有解決方案的訪客。

   實作包括新增 [!DNL Identity service] 廣告商網站上每個網頁的程式碼。

* 組織必須是 [已啟用Experience Cloud服務](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html) 並擁有Experience Cloud [!DNL Organization ID] (先前稱為 [!DNL IMS org ID])。

   此 [!UICONTROL Organization ID] 可讓擁有多個Adobe Experience Cloud產品的組織在某些產品之間共用資料。

* (廣告商使用 [!DNL Analytics])廣告商必須 [實作 [!DNL Analytics] 使用 `appMeasurement.js`](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) 1.6.4版或更新版本。

* 廣告商的網站訪客不包含大量的 [!DNL Apple Safari] 使用者。

* (建議廣告商同時使用Audience Manager和 [!DNL Analytics])若要減少每個網頁的呼叫，請移除現有Audience Manager [!DNL Data Integration Library] 資料收集程式碼，並為每個程式碼啟用伺服器端轉送 [!DNL Analytics] 報表套裝則相反。 如需詳細資訊，請參閱「[伺服器端轉送概觀](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

* （建議）若符合率較高，請只傳送第一方網站資料至Adobe廣告。 如果廣告商捆綁來自客戶關係管理系統的第三方資料或離線資料，資料洩漏可能會降低匹配率。

## 將Audience Manager對象匯入至DSP

### 將受眾匯入至DSP的步驟

此 [!DNL Adobe] 帳戶與資料作業團隊將執行下列步驟。

1. Adobe帳戶團隊應設定廣告商層級的設定»[!UICONTROL Adobe Analytics Cloud].」

1. Adobe帳戶團隊應提交請求<!-- Submit a request as a JIRA task? --> 至資料作業團隊<!-- implementation team? --> 使用Advertising DSP原生API整合匯入組織的Audience Manager區段。

### 哪些變更會產生Audience Manager？

API會自動執行下列動作：

* 在Audience Manager中建立兩個DSP目的地：

   * **[!UICONTROL Adobe Ad Cloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)])**

* 將兩個目的地對應至所有Audience Manager區段，讓Audience Manager可與與同一Experience Cloud相關聯的DSP廣告商帳戶共用區段 [!DNL Organization ID] 用於Audience Manager。 <!-- Verify -->

   組織可選擇性地從Audience Manager內的目的地移除不需要的區段。

* 將下列Exchange Cookie同步畫素新增至組織的Audience Manager容器，以改善客戶促銷活動的觸及範圍：

   * AdobeAdCloud： 411 （這是標準配備，並自動作為的一部分） [!DNL Identity Service] 2.0版。組織： [!DNL Identity Service] 低於2.0的版本應將此畫素新增至其Audience Manager容器。

## 將Audience Manager對象匯入 [!DNL Search, Social, & Commerce]

### 將受眾匯入到的步驟 [!DNL Search, Social, & Commerce]

[!DNL Adobe] 人員將執行以下大部分或全部步驟。

1. Adobe客戶團隊應提交請求給資料營運團隊，以設定以下兩者之間的整合： [!DNL Search, Social, & Commerce] 和Audience Manager。 包含您要匯出至的Audience Manager區段名稱 [!DNL Search, Social, & Commerce].

1. 在Audience Manager中，設定目的地 [!DNL Search, Social, & Commerce]：

   1. 建立兩個新目的地： `[!UICONTROL Adobe Media Optimizer (HTTP)]` 和 `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] 是以前的名稱 [!DNL Search, Social, & Commerce].

   1. 指定每個目的地的區段。

      使用 [!UICONTROL Automatically map all current and future segments] 選項，所有區段都會每日對應及同步。

      此 [!UICONTROL Manually map segments] 選項可讓您手動對應區段以與批次目的地同步(`[!UICONTROL Adobe Media Optimizer Batch Destination]`)。 不需要手動將任何區段對應至HTTP目的地。

1. 範圍 [!DNL Search, Social, & Commerce]，則 [!DNL Search, Social, & Commerce] 實作團隊或具有直接存取使用者端管理員角色的使用者應該從起始匯入 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   您必須輸入組織的Experience Cloud [!DNL Organization ID] ([!DNL IMS org ID])。 ID必須與用於組織Audience Manager帳戶的ID相同。

### 哪些變更會產生Audience Manager？

組織將看到兩個 [!DNL Search, Social, & Commerce] Audience Manager中的目的地：

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination])**

## 資料同步

初始匯入大約需要24小時。 初次匯入後，資料會即時同步，延遲一到兩秒。

<!--
### How DSP Syncs the Data

DSP syncs the data automatically using the [!DNL Adobe Experience Cloud Identity (ECID) Service]. During synchronization, the [!DNL ECID Service] calls Adobe Advertising at [!DNL cm.eversttech.net]. Because Adobe Advertising is a trusted domain, ID syncs take place from parent pages rather than within the destination publishing iframes, as they do with most third-party activation partners. Audience Manager identifies unique users by device IDs, using the [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html#global-device-ids), also called the [!DNL Device ID].

![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)

### How Search Syncs the Data
-->

<!-- 
Segment membership data is sent only after one of the following events occurs:

* (Advertisers with DSP):

  * The segment is targeted in an Adobe Advertising display ad.

  * The segment is added to the [!DNL Adobe AdCloud Cross-Channel] batch and real-time destinations within the Audience Manager user interface.

* (Advertisers with [!DNL Search, Social, & Commerce]):

  * The segment is targeted in an Adobe Advertising search ad.

  * The segment is added to the [!DNL Adobe Media Optimizer] batch and HTTP destinations within the Audience Manager user interface.
 -->
<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

## 在何處尋找同步的區段

### 在DSP中

在DSP中，區段名稱會依Audience Manager分類法來整理，並可在以下位置與對應的區段會籍計數一併取得：

* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting)：在 [!UICONTROL Adobe Segments] 的標籤 [!UICONTROL Audience Targeting] 區段。

* 在 [對象設定](/help/dsp/audiences/audience-settings.md)：在 [!UICONTROL Adobe Segments] 標籤。

### Advertising Creative內容

在 [!DNL Creative]中，這些區段會顯示在target節點的體驗設定中。

### 在 [!DNL Advertising Search, Social, & Commerce]

在 [!DNL Search, Social, & Commerce]，則區段可在您建立 [!DNL Google] 對象使用 [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]」從 [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

針對每個 [!DNL Google] 您建立的對象， [!DNL Google] 提供對象人數。

>[!MORELIKETHIS]
>
>* [AdobeAdvertising與Adobe Audience Manager的整合](/help/integrations/audience-manager/overview.md)

