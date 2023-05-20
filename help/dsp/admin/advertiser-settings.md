---
title: 廣告商帳戶設定
description: 請參閱可用廣告商設定的說明。
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 0%

---

# 廣告商帳戶設定

*無法供唯讀使用者使用*

## [!UICONTROL General] 設定

**[!UICONTROL Advertiser Name]：** 廣告商名稱。

**[!UICONTROL Category]：** 廣告商業務營運的類別。 當您競標庫存時，會將類別傳達給發佈者。 請務必選擇符合您廣告的類別，否則發佈者可能會拒絕您的廣告。

>[!NOTE]
>
>如果您選取 *[!UICONTROL Other]*，則廣告商將無法存取DSP [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]：** 廣告商的首頁或主要網站URL (開頭為 `http://` 或 `https://`)。

**[!UICONTROL Share all private exchange feeds into this advertiser]：** （僅限新廣告商帳戶）讓廣告商可以使用為組織的DSP帳戶設定的所有私人Exchange摘要。

### [!UICONTROL Adobe IMS IDs]

具有其他Adobe Experience Cloud產品的廣告商可以使用組織的Experience Cloud唯一ID，在某些產品間共用資料。 您可以在以下位置設定特定的產品整合： [!UICONTROL Integrations] 區段。

**[!UICONTROL Account IMS org and ID]：** (廣告商具有其他Experience Cloud產品，這些產品是透過具有多個廣告商的Experience Cloud帳戶來授權；可選)廣告商的Experience Cloud組織ID。

**[!UICONTROL Advertiser IMS org and ID]：** (具有其他Experience Cloud產品直接授權的廣告商；選用)廣告商的Experience Cloud組織ID。

### [!UICONTROL Integrations]

（選用）連結至DSP帳戶的其他Experience Cloud產品。 產品必須與中提供的相同Experience Cloud組織ID相關聯 [!UICONTROL Adobe IMS IDs] 區段。

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]：** (廣告商使用 [!DNL Advertising Search, Social, & Commerce] 或使用Adobe廣告轉換畫素的使用者) A [!DNL Search, Social, & Commerce] 與DSP交換歸因資料的帳戶。

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]：** (使用Adobe Analytics的廣告商；選用；僅適用於使用Adobe廣告轉換追蹤標籤(包含 [!DNL EF Redirect] 僅限和Token)一或多個 [!DNL Analytics] DSP會將收集自發佈商和供應方合作夥伴的資料傳送至報表套裝。 Analytics也會將其從使用者端網站收集到的資料傳送至DSP。

對於要顯示在報表套裝中的資料， [!DNL Search, Social, & Commerce] 將廣告商層級設定為&quot;[!UICONTROL Enable tracking for SAINT feeds]必須啟用「」。 此外，廣告商的 [!DNL Analytics] 帳戶必須設定為從Adobe廣告接收資料。

>[!WARNING]
>
>如果您移除先前連結的報表套裝，DSP將不再與該套裝交換資料。 預期會看到資料波動。

如需與整合的詳細資訊 [!DNL Analytics]，請參閱「[概述 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).」

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]：** (使用Adobe Audience Manager或Adobe Analytics的廣告商；選用)Audience Manager或 [!DNL Analytics] DSP將從中提取廣告商所有Adobe對象的區段中繼資料、階層資料和唯一對象資料的帳戶。 其中包括以下專案的資料：

* Audience Manager區段
* [!DNL Analytics] 發佈至Adobe Experience Cloud的區段
* 使用Adobe Experience Cloud建立的區段 [!DNL Audience Library]
* 在Adobe Experience Platform中建立並透過Audience Manager傳送至Adobe廣告的區段

初始同步大約需要24小時。 之後，資料會即時同步，延遲一到兩秒。
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] 設定

您可以選擇為廣告商的新版位設定預設目標。 使用者可以覆寫任何新位置的預設目標。

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]：** 每個位置的地理定位的預設國家/地區。 使用者可以變更國家/地區，並為每個位置設定更具體的地理定位。

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]：** 預設要隱藏的任何對象或區段。 使用者可以變更每個位置的排除專案。

### [!UICONTROL Media Quality]

#### [!UICONTROL Contextual Filtering]

型別 [!DNL Comscore]， [!DNL DoubleVerify]， [!DNL Integral Ad Science]、和 [!DNL Peer39] 要套用的內容篩選器。 您可以在以下位置覆寫廣告商層級設定： [位置層級](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]：** （選擇性）預設要封鎖的一或多個存貨內容型別。 可能需支付額外費用。

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]：** （選擇性）預設要定位的一或多個存貨屬性型別。 可能需支付額外費用。

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]：** （選擇性）預設要封鎖的一或多個存貨屬性型別。 可能需支付額外費用。

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]：** （選用）預設要封鎖廣告的成人內容程度： *[!UICONTROL Do Not Block]* （預設）， *[!UICONTROL Standard]*，或 *[!UICONTROL Strict]*. 可能需支付額外費用。

**[!UICONTROL Alcohol Content]：** （選用）預設要封鎖廣告的酒精含量等級： *[!UICONTROL Do Not Block]* （預設）， *[!UICONTROL Standard]*，或 *[!UICONTROL Strict]*. 可能需支付額外費用。

#### [!UICONTROL Pre-Bid Fraud Blocking]

根據詐騙流量和透過測量的可疑活動封鎖的網站型別 [!DNL DoubleVerify]， [!DNL Integral Ad Science]、和 [!DNL Peer39]. 您可以在以下位置覆寫廣告商層級設定： [位置層級](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]：** 依預設，會針對新位置封鎖所有100%無效流量，包括被劫持裝置上的流量。 可能需支付額外費用。

**[!UICONTROL Also block sites with]：** （選用）額外的詐騙和無效流量層級，會導致DSP依預設封鎖廣告：  *[!UICONTROL None]* （預設值，不會封鎖其他流量）， *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*， *[!UICONTROL >4% Average Fraud/IVT levels]*， *[!UICONTROL >6% Average Fraud/IVT levels]*， *[!UICONTROL >10% Average Fraud/IVT levels]*，或 *[!UICONTROL >25% Average Fraud/IVT levels]*. 可能需支付額外費用。

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]：** （選用）一或多個詐騙型別，預設會導致DSP封鎖廣告： *[!UICONTROL Fraud]* （會封鎖所有詐騙網站）、 *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*、和/或 *[!UICONTROL Fraud: Zero Ads]*. 可能需支付額外費用。

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]：** （選用）一種可疑的網站或應用程式活動，預設會導致DSP封鎖廣告： *[!UICONTROL None]* （預設值，不會根據可疑活動封鎖廣告）， *[!UICONTROL Suspicious Activity - High Risk]*，或 *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. 可能需支付額外費用。

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]：** 根據預設，哪一個層級 [[!DNL Ads.txt] 競標前篩選](https://iabtechlab.com/ads-txt-about/) 以運用每個發佈者的 [!DNL Authorized Digital Sellers] 清單：
* *[!UICONTROL Opt out of ads.txt (default)]*：從所有賣家購買詳細目錄。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*：優先從網域的授權直接銷售者和經銷商購買詳細目錄。
* *[!UICONTROL Ads.txt sellers only]*：僅向網域的授權直接銷售者和經銷商購買詳細目錄。
* *[!UICONTROL Ads.txt sellers only]*：僅從網域的授權直接銷售者購買詳細目錄。

您可以在以下位置覆寫廣告商層級設定： [位置層級](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]：** 依預設，會啟用即時競標後篩選器，以確保廣告可在廣告商鎖定的網站上提供。 <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Safety]

**[!UICONTROL DoubleVerify Account]：** ([!DNL DoubleVerify] 僅限客戶；選用)與組織的品牌安全區段ID相關聯 [!DNL DoubleVerify] 帳戶。

**[!UICONTROL Enable Authentic Brand Safety]：** （選用）依預設，啟用 [!DNL DoubleVerify] 正版品牌安全：會使用針對指定區段ID設定的自訂品牌安全規則，封鎖出價後的曝光數。 DSP會針對節段ID的用途來開立科目帳單。

您可以在版位層級覆寫廣告商層級設定。

>[!MORELIKETHIS]
>
>* [建立廣告商帳戶](/help/dsp/admin/advertiser-create.md)


<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
