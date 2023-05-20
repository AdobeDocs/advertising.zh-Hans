---
title: Campaign設定
description: 請參閱可用行銷活動設定的說明。
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 4085c1b21c0fe84653978e449321868921841367
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 0%

---

# Campaign設定

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]：** 行銷活動名稱。

**[!UICONTROL Advertiser]：** （現有行銷活動的唯讀）適用的廣告商（品牌）。 選取現有廣告商或建立新廣告商。

**[!UICONTROL Advertiser URL]：** 廣告商的官方頁面。 此欄位可加快您與詳細目錄合作夥伴的廣告核准流程。

**[!UICONTROL Timezone]：** （現有行銷活動的唯讀）報告和投標的時區。

**[!UICONTROL Customer PO]：** （選擇性）插入訂單/採購單的客戶採購單。

**[行銷活動日期]：** 行銷活動的開始和結束日期。

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]：** 是否要管理行銷活動的邊界： *[!UICONTROL Yes]* 或 *[!UICONTROL No]* （預設）。

當您選擇 *[!UICONTROL Yes]，* 指定利潤型別和金額：

* **[!UICONTROL Margin Type]：** 邊界型別。 啟用利潤管理並儲存行銷活動後，您就無法變更利潤型別。

   * *[!UICONTROL Fixed]：* （預設）允許DSP根據的固定利潤百分比自動計算和限制支出 [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]：* 可讓您透過指定個別的「 」來管理下至版位層級的邊界 [!UICONTROL Budget Reserve %] 和 [!UICONTROL Gross Budget] 行銷活動中的每個套件和位置。 DSP會根據每個位置的財務效率進行最佳化，而不保證特定的利潤。 對於由多個明細行專案組成的插入訂單，請使用此選項，您已同意以固定費率傳送固定數量的單位或單位型態。

* **[!UICONTROL Fixed Margin %]：** （僅限具有固定邊界的行銷活動）每個插入訂單的預設加成 <!-- impression? -->，以百分比表示。 此金額已從下列專案扣除： [!UICONTROL Gross Budget] 以定義淨促銷活動預算。

* **[!UICONTROL Budget Reserve %]：** （僅限具有固定邊界的行銷活動；選用）保留指定的百分比 [!UICONTROL Gross Budget] 作為安全保障。 此金額已從下列專案扣除： [!UICONTROL Gross Budget] 以定義淨促銷活動預算。

**[!UICONTROL Gross Budget]：** （僅限具有利潤管理的行銷活動）套用指定邊際調整前的行銷活動預算總額。

您可以選擇新增額外的每日、每週或每月毛額預算：

1. 单击 **[!UICONTROL Add an additional Gross Budget]**.

1. 輸入 **[!UICONTROL Gross Budget]** 並選取預算間隔： *[!UICONTROL Daily]，* *[!UICONTROL Weekly]，* 或 *[!UICONTROL Monthly]*.

總淨預算（促銷活動的支出上限）會根據利潤設定自動計算，並顯示在此值下方。

**[!UICONTROL Budget]：** （沒有利潤管理的行銷活動）整體行銷活動預算。

**[!UICONTROL Estimated Tax Withholding]：** 針對國家/地區或地方稅種，在帳戶層級預扣廣告費用、廣告服務費用及/或資料費用中的總支出百分比。 費率是預算編列與調整用途的估計值，因此發票稅率可能有所不同。

若要預估要預扣的稅捐，請執行下列步驟：

1. 单击 **[!UICONTROL Update rates here]**.

1. 指定 **[!UICONTROL Estimated tax rate]**，以百分比表示。

1. 選取要預扣稅捐之各費用型別旁的核取方塊。 費用型別包括：

   * *[!UICONTROL Include estimated tax - ads fee]：* 適用於所有Advertising DSP媒體支出，包括促銷活動管理費用稅捐。

   * *[!UICONTROL Include estimated tax - ad serving fee]：* 適用於除媒體與資料以外的所有在Advertising DSP上的支出。 不含行銷活動管理費用的稅項

   * *[!UICONTROL Include estimated tax - data fee]：* 套用至Advertising DSP上所有花費的資料。

1. 单击 **[!UICONTROL Submit]**.

>[!NOTE]
>
>* 在美國，各州在包含跨廣告、廣告服務和資料的稅務費用方面可能有所不同。 若為其他國家中的組織，請包含所有三種類別的稅捐費用，以說明VAT。
>
>* 您也可以在帳戶的費用設定中設定這些值。<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->


**[!UICONTROL Cross Device Level]：** （自2020年6月22日起建立的現有行銷活動為唯讀；2020年6月22日之前建立的行銷活動不適用） DSP將目標鎖定廣告並套用頻率上限的層級： *相同裝置* 以裝置為目標或 *人員* 跨所有已知裝置鎖定使用者。

**[!UICONTROL Device Graph]：** （現有行銷活動為唯讀；僅適用以人物為基礎的跨裝置目標定位行銷活動）用於跨裝置目標定位和頻率管理的裝置圖表：

* *[!UICONTROL LiveRamp - U.S. only]：* 跨裝置目標定位向所有廣告商提供$0.35 CPM的價格，適用於透過以下網址提供的曝光數： [!DNL LiveRamp] 裝置圖表（即目標受眾區段中找不到的裝置）。 您可以在位置層級設定跨裝置目標定位。

   此選項也可供所有廣告商使用（不需支付任何費用），以進行頻率管理和歸因測量。

**[!UICONTROL Frequency Cap]：** （選用）不重複裝置或個人的次數（視指定的而定） [!UICONTROL Cross Device Level])將會收到來自行銷活動的廣告。 選項包括 *[!UICONTROL Unlimited]* 或每日、周或月的特定金額。

>[!NOTE]
>
> 您可以在行銷活動、套件和位置層級設定頻率上限。 DSP會遵循行銷活動階層中最嚴格的頻率上限。

**[!UICONTROL Packages]：** 此 [套件](/help/dsp/campaign-management/packages/package-about.md) 以包含在行銷活動中。 選取現有套件和/或建立要包含的套件。 如果您建立套裝程式，請參閱關於 [封裝設定](/help/dsp/campaign-management/packages/package-settings.md) 以取得詳細資訊。

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>下列設定只會啟用測量和報告功能。 效能最佳化只會在套件和位置層級執行。

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]：** （選用）啟用 [!DNL IAS] 使用指定設定來測量及報告可檢視度、詐騙、品牌安全和對象驗證。 需支付額外費用。

* **[!UICONTROL Measure On]：** 要測量的存貨： *[!UICONTROL Display and VPAID video inventory]* （預設）或 *[!UICONTROL Display, VPAID & VAST video inventory]*.

   >[!NOTE]
   >
   >視訊可檢視度只能在VPAID詳細目錄中測量。

* **[!UICONTROL IAS Account ID (AnID)]：** (有自己的廣告商 [!DNL IAS] 帳戶；選擇性)組織的 [!DNL IAS] 帳戶ID，其中 [!DNL IAS] 將直接收取使用費。

* **[!UICONTROL IAS Team ID]：** (有自己的廣告商 [!DNL IAS] 帳戶；選用)組織的團隊ID [!DNL IAS] 帳戶，其中 [!DNL IAS] 將直接收取使用費。 <!-- verify -->

**[!UICONTROL MOAT]：** （選用）啟用 [!DNL MOAT] 可檢視度、詐騙、品牌安全和對象驗證的測量與報告。 需支付額外費用。

#### 對象驗證

**[!UICONTROL Nielsen]：** （選用）啟用 [!DNL Nielsen] 使用指定設定測量及報告對象驗證。 需支付額外費用。

* **[!UICONTROL Target Gender]：** 目標性別： *[!UICONTROL Both]* （預設）， *[!UICONTROL Male]*，或 *[!UICONTROL Female]*

* **[!UICONTROL Target Age]：** 要鎖定的年齡範圍。 視需要使用左右滑桿來縮小範圍。

* **[!UICONTROL Target Country]：** （選用）要鎖定的國家/地區。 [!DNL Nielsen] 只會測量支援國家/地區的曝光數。

**[!UICONTROL comScore vCE]：** （選用）啟用 [!DNL Comscore validated Campaign Essentials (vCE)] 使用指定設定測量及報告對象驗證。 需支付額外費用。

* **[!UICONTROL Target Gender]：** 目標性別： *[!UICONTROL Both]* （預設）， *[!UICONTROL Male]*，或 *[!UICONTROL Female]*

* **[!UICONTROL Target Age]：** 要鎖定的年齡範圍。 視需要使用左右滑桿來縮小範圍。

* **[!UICONTROL Target Country]：** （選用）要鎖定的國家/地區。 [!DNL Comscore] 只會測量支援國家/地區的曝光數。

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]：** 啟用第一方可檢視度測量及報告，使用 [!DNL IAB Open Video Viewability (OpenVV)] 技術，根據指定的敏感度等級：

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [關於Campaign Management](campaign-about.md)
>* [建立行銷活動](campaign-create.md)
>* [編輯行銷活動](campaign-edit.md)
>* [檢視行銷活動的變更記錄](campaign-change-log.md)

