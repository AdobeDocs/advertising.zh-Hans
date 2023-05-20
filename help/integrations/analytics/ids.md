---
title: 使用的Adobe廣告ID [!DNL Analytics]
description: 使用的Adobe廣告ID [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 0%

---

# 使用的Adobe廣告ID [!DNL Analytics]

*僅具有AdobeAdvertising-Adobe Analytics整合的廣告商*

*適用於Advertising DSP和[!DNL Advertising Search, Social, & Commerce]*

Adobe廣告使用兩個ID進行網站上的效能追蹤： *EF ID* 和 *AMO ID*.

當廣告曝光發生時，Adobe廣告會建立AMO ID和EF ID值並加以儲存。 當看過廣告的訪客未點按廣告即進入網站時， [!DNL Analytics] 從Adobe廣告呼叫這些值，透過 [!DNL Analytics for Advertising] JavaScript程式碼。 若為檢視流量， [!DNL Analytics] 產生補充ID (`SDID`)，用於將EF ID和AMO ID彙整至 [!DNL Analytics]. 針對點進流量，這些ID會使用包含在登陸頁面URL中 `s_kwcid` 和 `ef_id` 查詢字串引數。

Adobe廣告會使用下列條件來區分網站的點進或檢視專案：

* 當使用者在檢視廣告但未按一下網站後造訪網站時，會擷取檢視專案。 [!DNL Analytics] 如果符合兩個條件，則會記錄檢視：
   * 訪客沒有的點進次數 [!DNL DSP] 或 [!DNL Search, Social, & Commerce] 廣告時段 [按一下回顧視窗](#lookback-a4adc).
   * 訪客已看到至少一個 [!DNL DSP] 廣告時段 [曝光回顧期間](#lookback-a4adc). 最後一次曝光會以檢視的方式傳遞。
* 網站訪客在進入網站前點選廣告時，會擷取點進專案。 [!DNL Analytics] 會在發生下列任一情況時擷取點進：
   * URL包含EF ID和AMO ID，由Adobe廣告新增至登陸頁面URL。
   * URL未包含追蹤代碼，但AdobeAdvertising JavaScript代碼會在過去兩分鐘內偵測到點選。

![以Adobe廣告檢視為基礎 [!DNL Analytics] 整合](/help/integrations/assets/a4adc-view-through-process.png)

*圖1：Adobe廣告檢視型 [!DNL Analytics] 整合*

![Adobe廣告點選URL型 [!DNL Analytics] 整合](/help/integrations/assets/a4adc-click-through-process.png)

*圖2：Adobe廣告點選的URL型 [!DNL Analytics] 整合*

## Adobe廣告EF ID

EF ID是不重複Token，AdobeAdvertising可用來將活動與線上點選或廣告曝光度建立關聯。 EF ID會儲存在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar (保留的eVar)維度(Adobe廣告EF ID)，並追蹤個別瀏覽器或裝置層級的每個廣告點選或曝光。 EF ID主要作為傳送的金鑰 [!DNL Analytics] Adobe廣告的資料，以便在Adobe廣告中製作報表和最佳化出價。

### EF ID格式

>[!NOTE]
>
>EF ID區分大小寫。 如果 [!DNL Analytics] 實作會強制將URL追蹤轉換為小寫，然後Adobe廣告將無法辨識EF ID。 這會影響Adobe廣告的投標和報告，但不會影響內的Adobe廣告報告 [!DNL Analytics].

#### [!DNL Google Ads] 搜尋廣告

```
{gclid}:G:s
```

其中：

* `gclid` 是 [!DNL Google Click ID] (GCLID)。
* `s` 是網路型別（「s」代表搜尋）。

#### Microsoft Advertising搜尋廣告

```
{msclkid}:G:s
```

其中：

* `msclkid` 是 [!DNL Microsoft Click ID] (MSCLKID)。
* `s` 是網路型別（「s」代表搜尋）。

#### 在其他搜尋引擎上顯示廣告和搜尋廣告

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

其中：

* &lt;*Adobe廣告訪客ID*>是每位訪客的不重複ID （例如UhKVaAAABCkJ0mDt）。 也稱為 *瀏覽者ID*.

* &lt;*timestamp*>是YYYYMMDDHHMMSS格式的時間(例如2019年20190821192533、月08、第21天、時間19:25:33)。

* &lt;*頻道型別*>是造成點按或曝光的管道型別：

   * `d` （顯示廣告點進） DSP顯示廣告上的點按
   * `i` 針對DSP顯示廣告（顯示瀏覽次數）的曝光
   * `s` （搜尋）廣告的點按（點進）。

範例 `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### 中的EF IDDimension [!DNL Analytics]

在 [!DNL Analytics] 報表中，您可以透過搜尋 [!UICONTROL EF ID] 維度和使用 [!UICONTROL EF ID Instance] 量度。

EF ID必須遵守Analysis Workspace中500,000的唯一識別碼限制。 一旦達到500k值，所有新的追蹤程式碼都會報告在單行專案標題下&quot;[!UICONTROL Low Traffic].」 由於可能會遺失報表精確度，EF ID不會進行分類，您不應將其用於中的區段或報表 [!DNL Analytics].

## AdobeAdvertising AMO ID

AMO ID會在較不精細的層級追蹤每個獨特的廣告組合，並用於 [!DNL Analytics] 資料分類以及從Adobe廣告擷取的廣告量度（例如曝光數、點按數和成本）。 AMO ID會儲存在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar維度(AMO ID)，僅用於報表： [!DNL Analytics].

AMO ID也稱為 `s_kwcid`，有時發音為「[!DNL the squid].」

### AMO ID格式 [!DNL DSP]

```
<Channel ID>!<Ad ID>!<Placement ID>
```

其中：

* &lt;*管道ID*>可以是：

   * `AC` = Advertising DSP
   * `AL` 的 [!DNL Advertising Search, Social, & Commerce]

* &lt;*廣告ID*>是Adobe廣告產生的廣告唯一識別碼。 它可當作將Adobe廣告實體中繼資料轉譯為可讀取的索引鍵 [!DNL Analytics] 維度。

* &lt;*刊登ID*>是Adobe Advertising為位置產生的唯一識別碼。 它可當作將Adobe廣告實體中繼資料轉譯為可讀取的索引鍵 [!DNL Analytics] 維度。

範例AMO ID： AC！iIMvXqlOa6Nia2lDvtgw！GrVv6o2oV2qQLjQiXLC7

### AMO ID格式 [!DNL Search, Social, & Commerce]

的AMO ID [!DNL Search, Social, & Commerce] 請遵循每個搜尋引擎的不同格式。 所有搜尋引擎的格式都以下列專案開頭：

```
AL!{userid}!{sid}
```

其中：

* `AL` 是廣告網路的管道ID。
* `{userid}` 是Adobe廣告指派給廣告商的不重複數值使用者ID。
* `{sid}` 是Adobe廣告用於指定廣告網路的數值ID，例如 `3` 的 [!DNL Google Ads] 或 `10` 的 [!DNL Microsoft Advertising].

以下是幾個廣告網路的完整AMO ID格式。 如需其他廣告網路的AMO ID格式，請聯絡您的Adobe客戶團隊。

AMO ID格式 [!DNL Google Ads]：

```
AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

其中：

* `{creative}` 是 [!DNL Google Ads] 創意內容的不重複數值ID。
* `{matchtype}` 是觸發廣告之關鍵字的matchtype： `e` 確切地說， `p` 代表片語，或 `b` 廣泛使用。
* `{placement}` 是廣告被點按所在網站的網域名稱。 值適用於以位置為目標的行銷活動中的廣告，以及內容網站上顯示之以關鍵字為目標的行銷活動中的廣告。
* `{network}` 表示發生點按的網路：  `g` 的 [!DNL Google] 搜尋（僅適用於以關鍵字為目標的廣告）， `s` （僅適用於關鍵字鎖定目標的廣告），或 `d` 針對「顯示網路」（針對關鍵字或位置定位的廣告）。
* `{keyword}` 是觸發您廣告的特定關鍵字（在搜尋網站上）或最佳比對關鍵字（在內容網站上）。

AMO ID格式 [!DNL Microsoft Advertising]：

```
AL!{userid}!{sid}!{AdId}!{OrderItemId}
```

其中：

* `{AdId}` 是 [!DNL Microsoft Advertising] 創意內容的不重複數值ID。
* `{OrderItemId}` 是 [!DNL Microsoft Advertising] 關鍵字的數值ID。

### 中的AMO IDDimension [!DNL Analytics]

在Analytics報表中，您可以透過搜尋 [!UICONTROL AMO ID] 維度和使用 [!UICONTROL AMO ID Instance] 量度。 此 [!UICONTROL AMO ID] 維度會儲存所有擷取的AMO ID值，而 [!UICONTROL AMO ID Instance] 量度會指出網站擷取AMO ID值的頻率。 例如，如果同一個搜尋廣告被點按四次，但Analytics追蹤了七個網站專案，則 [!UICONTROL AMO ID Instance] 將會是七(7)和 [!UICONTROL Clicks] 將會是四(4)。

對於中的任何報告或稽核，在 [!DNL Analytics]，最佳實務是搭配使用AMO ID及其對應的例項。 如需詳細資訊，請參閱「[資料驗證： [!DNL Analytics for Advertising]](data-variances.md#data-validation)「預期資料差異」介於 [!DNL Analytics] 和Adobe廣告。」

## 關於Analytics分類

在 [!DNL Analytics]， a [分類](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) 是指定追蹤代碼（例如「帳戶」、「促銷活動」或「廣告」）的中繼資料。 「Adobe廣告」會使用分類來分類原始Adobe廣告資料，以便在您產生報表時能以不同方式顯示資料（例如依廣告型別或促銷活動）。 分類構成中的Adobe廣告報表基礎 [!DNL Analytics] 和，可搭配AMO量度使用，例如 [!UICONTROL AMO Cost]， [!UICONTROL AMO Impressions]、和 [!UICONTROL AMO Clicks]，以及自訂和標準的站上事件，例如 [!UICONTROL Visits]， [!UICONTROL Leads]， [!UICONTROL Orders]、和 [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [預期資料差異： [!DNL Analytics] 和Adobe廣告](data-variances.md)

