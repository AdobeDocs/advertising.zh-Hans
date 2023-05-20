---
title: '''[!UICONTROL Simple Ad Serving] 交易設定'
description: 瞭解可用的設定 [!UICONTROL Simple Ad Serving] 交易。
feature: DSP Simple Ad Serving
exl-id: 20e23182-d3d0-457f-a821-0ad4770a138d
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] 交易設定

## 新增 [!UICONTROL Simple Ad Serving] 交易

### [!UICONTROL Select Ad Source]

| 引數 | 描述 |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | 此交易的媒體型別： *[!UICONTROL Video]，* *[!UICONTROL Display]，* 或 *[!UICONTROL Audio].* |
| **[!UICONTROL Publisher Site Served On]** | 銷售此詳細目錄的發行者名稱。 在名稱中至少輸入前兩個字元，以搜尋發行者。 若要新增未列出的發行者，請聯絡您的Adobe帳戶團隊。 |
| **[!UICONTROL Advertiser]** | 帳戶中可存取此交易的單一廣告商。 同時選取行銷活動，以及（選擇性）可從中取得交易的套件。 |
| **[!UICONTROL Media Quality Assessment?]** | （部分使用者）讓廣告可在其他DSP上執行以進行協力廠商驗證。 <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | 唯一的選項是 *[!UICONTROL Site Serve (Event Pixels)]*. |
| **[!UICONTROL Ad Creation]** | （僅限新交易）是否：<ul><li>*[!UICONTROL Create New]：* 為此交易建立廣告的方式。</li><li>*[!UICONTROL Select Ads]：* 使用此交易的現有廣告。</li></ul> |
| **[!UICONTROL Ad Type]** | 此交易的廣告型別。 如果您要為交易建立廣告，請根據要求包含廣告大小或持續時間。 可用選項會因媒體型別而異。 |

{style="table-layout:auto"}

### [!UICONTROL Select Ad(s)]

（當您使用現有廣告時）要包含在交易中的廣告。 選取每個要包含的廣告旁的核取方塊。

### [!UICONTROL Select & Upload [Media Type]]

（僅限新廣告）建立新廣告的畫面 [協力廠商廣告](/help/dsp/campaign-management/ads/ad-create-multiple.md).

### [!UICONTROL Feed Details]

| 引數 | 描述 |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | 每1000次曝光的成本(CPM)，如您合約的費率卡所反映。 如需此值，請聯絡您的Adobe客戶團隊。 <br><br>同時指定交易的貨幣。 所有使用者都可以選取USD，或者，如果SSP支援其他貨幣，則選取DSP帳戶的貨幣。 |
| **[!UICONTROL Third Party Billed Fees]** | （選用）要作為不可記帳成本追蹤的靜態第三方費用，以及交易的貨幣。<br><br>所有使用者都可以選取USD，或者，如果SSP支援其他貨幣，則選取DSP帳戶的貨幣。 **注意：** 可記帳費用會反映在 [!UICONTROL Net CPM] 量度。 |
| **[!UICONTROL Third Party Fee Description]** | （選用）協力廠商費用的說明。 |
| **[!UICONTROL Flight Dates]** | 使用此交易的流量的開始和結束日期。 投放日期必須包含在行銷活動投放日期中。 廣告標籤只會在指定的投放期間傳回回應。<br><br> 建立獨立簡易廣告服務行銷活動（持續時間為一年）並在其中建立追蹤畫素的最佳實務。 |
| **[!UICONTROL Impressions]** | （選用）您預計使用此交易執行的預估曝光次數。 此值僅用於追蹤目的，並用於標幟何時達到傳送目標；發佈者控制實際的廣告傳送。 最佳實務是輸入大量曝光次數，讓標籤在DSP中保持作用中，以便可視需要更新或延伸。 |
| **[!UICONTROL Deal Name]** | 交易名稱。 輸入名稱或選取 *[!UICONTROL Auto Generate Deal Name]* 讓DSP根據交易詳細資料產生名稱。<br><br>自動產生的名稱範例： `Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | （唯讀）屬於交易的廣告。 若要編輯廣告，請按一下廣告名稱。 若要從交易移除廣告，請按一下 **[!UICONTROL X]** 位於廣告名稱旁。 |

{style="table-layout:auto"}

<!-- 
## Existing Simple Ad Serving Deals

Changes aren't applied retroactively.
-->

<!-- completely different settings layout, so need a separate section for them -->

<!-- From Abhinav: Editable fields are Name, Start & End date, Impressions & CPM. Changes are not applied retroactively.

But I see:

| Parameter | Description |
|-----------|-------------|

| **[!UICONTROL Are you using Deal ID?] | (Read-only) Whether the deal was set up as a [!UICONTROL Deal ID] (*[!DNL Yes]*)  or a [!UICONTROL Simple Ad Serving] deal (*[!DNL No]*). |
| **[!UICONTROL Inventory Type] | (Read-only) The inventory type for the deal. |
| **[!UICONTROL Feed Name] | The name of the [!UICONTROL Simple Ad Serving] deal. |
| **[!UICONTROL Publisher Ad Server] | (Read-only)  |
| **[!UICONTROL Publisher maximum ad length] | The maximum length of the ad, per the publisher. |
| **[!UICONTROL Publisher minimum ad length] | The minimum length of the ad, per the publisher. |
| **[!UICONTROL Fill Type] | (Read-only)  |
| **[!UICONTROL Contracted CPM] | This field is required if billing through TubeMogul, but enter your CPM in this field to track your actual spend. |
| **[!UICONTROL 3rd party technology CPM] | (Optional)  |
| **[!UICONTROL Planned Flight Dates] | The beginning and end dates for the deal flight. These dates don't control ad delivery but are used to track delivery pacing. **THIS IS CONTRARY TO WHAT THE NEW DEAL SETTINGS ABOVE, FROM ABHINAV, SAY**> |
| **[!UICONTROL Target Impressions] | (Optional) The estimated number of impressions you expect to run using this deal. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
 -->

>[!MORELIKETHIS]
>
>* [關於 [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [建立 [!UICONTROL Simple Ad Serving] 交易](simple-deal-create.md)
>* [編輯 [!UICONTROL Simple Ad Serving] 交易設定](simple-deal-edit.md)
>* [檢視交易的詳細報告](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
