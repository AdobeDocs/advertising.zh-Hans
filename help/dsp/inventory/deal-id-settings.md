---
title: 手動交易識別碼設定
description: 請參閱手動輸入交易ID的設定說明。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 9d3417cb-8b44-4f1c-afc4-eea6a2e5b9d7
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# 手動交易識別碼設定

| 章節 | 引數 | 描述 | 必填 | 可編輯 |
|---------|-----------|-------------|----------|----------|
| [交易詳細資料] | [!UICONTROL Deal name] | 用以識別 [!UICONTROL Deal ID] Advertising DSP中的。 輸入名稱或選取 **[!UICONTROL Auto-name]** 讓DSP根據交易詳細資料產生名稱。<br><br>自動產生的名稱範例： `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | 是 | 是 |
|  | [!UICONTROL External deal ID] | 您的發佈者和SSP用來識別此交易的ID。 | 是 | 否 |
|  | [!UICONTROL Publisher] | 銷售此詳細目錄的發行者名稱。 | 是 | 否 |
|  | [!UICONTROL SSP] | 執行此交易的供給端平台(SSP)。 | 是 | 否 |
|  | [!UICONTROL Media type] | 透過此交易購買的媒體型別： *[!UICONTROL Desktop video]*， *[!UICONTROL Mobile video]*， *[!UICONTROL Connected TV]*， *[!UICONTROL Display]*，或 *[!UICONTROL Audio]*. 選項因SSP而異。<br><br> 如果交易允許多種媒體型別，請在建立交易時選取預設位置的媒體型別。 稍後，您可以變更值，或只要 [附加具有其他媒體型別的新版位](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | 是 | 否 |
|  | [!UICONTROL Deal type] | 交易承諾與定價結構：<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*：您和發佈者尚未承諾固定數量的曝光傳送。 交易會指定存貨的最低價格，不過CPM可能會隨著市況而波動和增加。</li><li>*[!UICONTROL Non guaranteed (fixed)]*：您和發佈者尚未承諾固定數量的曝光傳送。 訂價是以議定的固定費率進行。</li><li>*[!UICONTROL Guaranteed (fixed)]*：您和發佈商已同意預先定義的曝光次數、目標定位、投放日期和固定價格。<br><br><b>注意：</b> 有保證的交易需要投放日期和中的指定曝光次數 [!UICONTROL Tracking] 區段。 您也必須為交易建立預設程式化預留(PG)位置，且您可以選擇將交易用於其他位置。</li></ul> | 是 | 否 |
|  | [!UICONTROL CPM] | 每1000次曝光的議定成本(CPM)。 | 是 | 是 |
|  | [貨幣] | 交易的貨幣。<br><br>所有SSP都接受美元交易。 當SSP接受您DSP帳戶的貨幣時，該貨幣也可供使用。 | 是 | 否 |
|  | [!UICONTROL Billing method] | 所有交易識別碼為 [!DNL Adobe]-finished與 — invoiced。 DSP會根據使用情況向所有可用的媒體供應商付款、管理與供應商的不一致，並向該帳戶傳送一張合併發票。 此選項會產生額外費用，如帳戶的費率卡中所述。 | 是 | 否 |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | 可存取交易的使用者帳戶的電子郵件地址。 | 否 | 是 |
|  | [!UICONTROL Advertisers that can access this deal] | 帳戶中可存取此交易的特定廣告商。<br><br><b>注意：</b> 您可以從以下位置的其他帳戶與廣告商共用交易： [!UICONTROL Deals] 檢視。 在交易列中，按一下 **[!UICONTROL #]**，按一下 **[!UICONTROL share]**，然後與電子郵件地址共用該交易。 | 是 | 是 |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | 使用此交易的流量的開始和結束日期。 這些日期僅供追蹤用途，不會影響廣告傳送。<br><br><b>秘訣：</b> 在 [!UICONTROL Inventory] > [!UICONTROL Deals] 檢視， [!UICONTROL Pacing & Budget] 欄顯示交易如何步調到指定的投放日期和曝光目標。 如果傳送速度不佳或速度過快，請聯絡您的發佈商，以調整透過交易傳送的傳送量。 | 保證交易：是<br>非保證交易：否 | 是 |
|  | [!UICONTROL Impressions] | （非保證交易的選擇性）您預期使用此交易執行的預估曝光次數。 此值僅供追蹤之用；發行者可控制廣告傳送。 | 保證交易：是<br>非保證交易：否 | 是 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [手動建立交易識別碼詳細資料](deal-id-create.md)
>* [SSP合作夥伴](ssp-partners.md)
>* [關於私人詳細目錄](private-inventory-about.md)

