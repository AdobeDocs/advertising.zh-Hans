---
title: 收集來自Advertising DSP Campaigns的點選和曝光資料
description: 瞭解如何使用Audience Manager畫素從Advertising DSP廣告擷取Cookie型曝光次數和點選事件
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 0%

---

# 從Advertising DSP Campaigns收集媒體曝光資料

*僅使用Advertising DSP的廣告商*

*僅具有AdobeAdvertising-Adobe Audience Manager整合的廣告商*

本檔案說明如何標籤Advertising DSP廣告，以使用Audience Manager畫素擷取Cookie型曝光次數和點選事件，以及使用資料所需的其他工作。

事件畫素不會擷取在無Cookie環境中發生的事件，例如行動應用程式和連線電視(CTV)。

## 步驟1：設定Audience Manager中的資料來源 {#set-up-data-source}

在Audience Manager中，建立 [資料來源](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) 針對DSP曝光次數和點選資料。 包含資料來源ID [在每個事件標籤中](#implement-dsp-pixels) 以便將所有追蹤的事件歸因到資料來源。

>[!NOTE]
> 可以在單一資料來源中，針對在多個DSP上執行的廣告行銷活動，收集其所有曝光次數和點選資料。

## 步驟2：在網頁上實作曝光和點選事件畫素 {#implement-dsp-pixels}

廣告商可以為自己的品牌建立和實施事件標籤。 如有需要，請聯絡您的Adobe Audience Manager顧問或Adobe客戶團隊以尋求支援。

>[!NOTE]
>
>如果您的組織使用 [!DNL Analytics] ，則您可能不需要Audience Manager點選追蹤。 Adobe Analytics會擷取點選訊號，並透過將其傳送給Audience Manager [伺服器端轉送](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

### 畫素語法

事件畫素必須包括下列引數。

**曝光追蹤畫素：**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

替換為 [選擇性其他引數](#parameters) 前置詞為 `&`

**點選追蹤畫素：**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

替換為 [選擇性其他引數](#parameters) 前置詞為 `&`

其中：

* `[Audience Manager customer domain]` 是將曝光或點選事件傳送至的網域名稱 [!DNL Adobe].

* `[source id]` 是的ID [資料來源](#set-up-data-source) 其中您將追蹤DSP曝光次數和點按資料。

* `[redirect URL]` 是雙重編碼的重新導向URL。 如果您使用線上編碼工具(例如www.urlencoder.org)，請透過編碼器執行字串並重新編碼結果。

* `${TM_CAMPAIGN_ID_NUM}` 是DSP中的數值促銷活動ID。 如果您想要以硬式編碼個別促銷活動ID，而不使用DSP巨集，請在促銷活動設定中找出該ID。

* 每個 [引數](#key-value-pairs) 前置詞為 `&` 和的格式為 `d_parameter=parameter_id`，其中 `parameter` 將由新欄位的機碼值組取代。 範例： `&d_placement=${TM_PLACEMENT_ID_NUM}`

### 索引鍵值配對的引數 {#parameters}

**格式：**  `d_parameter=parameter_id`

    其中：
    
    *引數的前置詞為&#39;&amp;&#39;
    
    * &#39;parameter&#39;會由新欄位的機碼值組取代
    
    範例： &#39;&amp;d_placement=${TM_PLACEMENT_ID_NUM}&#39;

兩種型別的畫素都可包含其他引數，例如 *機碼值組* 收集特徵或提供其他報表的行銷活動中繼資料（例如版位名稱或行銷活動名稱）。 機碼 — 值組包含兩個相關元素：a *金鑰*，此常數會定義資料集，而 *值*，此變數屬於該集。

在機碼 — 值組中，值變數可以是硬式編碼ID或 *巨集*，這是內含程式碼的小單位，當廣告標籤載入促銷活動和使用者追蹤時，會動態取代為對應的值。 對於促銷活動相關引數，您可以使用 [DSP巨集](/help/dsp/campaign-management/macros.md) 不要使用Audience Manager巨集來傳送行銷活動屬性以及對應的曝光數或點按資料來Audience Manager，而是在所有廣告中使用單一畫素。 您插入事件畫素的DSP巨集必須是包含在畫素中的機碼值組的適當值。 例如，對於 `d_placement` 鍵，您會使用DSP巨集 `${TM_PLACEMENT_ID_NUM}` 當做值，擷取Adobe廣告巨集產生的版位ID。

如需Audience Manager支援曝光事件畫素的巨集清單，請參閱&quot;[透過畫素呼叫擷取行銷活動的曝光資料](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs).」

如需Audience Manager支援點選事件畫素的巨集清單，請參閱「[透過畫素呼叫擷取行銷活動的點按資料](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html).」

>[!TIP]
>
>* 最佳實務是納入行銷活動、版位、創意（廣告）和網站ID，讓您能夠使用行銷活動屬性來建立Audience Manager特徵。
>* 若要建立Audience Optimization報表，需要其他引數。
>* 在索引鍵值配對中，將值取代為相關的 [DSP巨集](/help/dsp/campaign-management/macros.md) 因此，您可以在所有行銷活動的所有廣告中使用單一畫素。 例如，變更 `d_campaign=[%campaignID%]`至 `d_campaign=${TM_CAMPAIGN_ID_NUM}` 擷取Adobe廣告巨集產生的促銷活動ID。
>* 如有需要，您可以使用硬式編碼值建立自己的引數。 範例： `d_DSP=AdCloud`


曝光事件畫素的範例：

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### 增加畫素的位置

#### 曝光追蹤畫素

將曝光事件追蹤畫素附加至中的所有廣告 [!DNL DSP] 行銷活動。 您可以在下列任何位置執行此操作：

* 在版位層級，預設會將畫素套用至版位中的所有廣告。 在位置設定的「追蹤」區段中，將畫素新增至 [[!UICONTROL Event pixels] 欄位](/help/dsp/campaign-management/placements/placement-settings.md).

* 在廣告層級，會覆寫任何位置層級事件畫素。 在廣告設定中， [在上建立事件畫素 [!UICONTROL Pixel] 標籤](/help/dsp/campaign-management/ads/ad-edit.md).

* （適用於協力廠商廣告伺服器上的廣告）在廣告伺服器內的廣告層級。

#### 點選追蹤畫素

在廣告伺服器中，將點選事件畫素插入（附加編碼URL）廣告點進URL的正常插入位置。

## 步驟3：實作後工作

實作事件標籤後，資料會流入Audience Manager資料收集伺服器。 請先完成下列工作，您才能在報表中使用資料。

### 建立 [!DNL Amazon S3] 貯體和資料來源

一旦您的資料在Audience Manager伺服器上，您必須建立 [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3])貯體，然後是資料來源，所有畫素資料都會傳送至該資料來源。 請聯絡您的Audience Manager顧問或 [客戶服務](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) 如果您需要支援。

### 建立Audience Manager特徵和區段

您的事件資料將以下列方式流入Audience Manager： [未使用的訊號](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html). 手動建立 [規則型特徵](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) 從擷取的資料中，然後建立 [區段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) 使用這些特徵，您才能在報表中使用資料。

為在DSP中接觸到特定創意內容的使用者填入使用者層級資料的範例特徵：

1. 將事件識別為 `d_event = imp`.
1. 識別DSP促銷活動中的創作ID，然後將它對應至特徵，如下所示 `d_creative=[Creative ID]`.

![特徵建立畫面](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [DSP巨集](/help/dsp/campaign-management/macros.md)
>* [傳送DSP Media Exposure資料至Adobe Audience Manager概述](overview.md)
>* [使用案例](use-cases.md)

