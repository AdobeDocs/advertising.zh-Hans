---
title: 設定程式化保證交易
description: 瞭解如何設定您已和發佈商洽談過的程式化預留(PG)交易。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# 設定程式化保證交易

*[僅支援的供應端平台](programmatic-guaranteed-about.md)*

在與支援的發行者協商程式化保證(PG)交易後，您可以在DSP中設定交易，方法為使用 [!DNL Deal ID inbox] 或手動輸入交易詳細資料。

>[!NOTE]
>
> 對於PG交易，發佈商會處理所有預算步調、預算上限和定位。 所有允許透過DSP使用PG的SSP都確認發行者可以設定預算上限。
>
> 與發佈商建立程式化預留交易，於 [!DNL FreeWheel] 需要額外的許可權和步驟。 請參閱「[設定程式化預留交易的概述 [!DNL FreeWheel]](freewheel-overview.md)」以取得詳細資訊。

## 使用設定程式化保證交易 [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

下列方法為的偏好程式 [!DNL FreeWheel]， [!DNL Google Authorized Buyers]、和 [!DNL Magnite DV+].

1. [接受交易](deal-id-inbox-accept.md).

1. 儲存交易後，選取將用於交易的廣告，並根據提示建立程式化預留(PG)預設位置。

   建立交易的預設PG投放位置是交付您100%購買的必備條件。 此型別的刊登位置沒有鎖定目標，因此DSP可以傳回對發佈商提出之每個競標要求的競標。

   * 如果您接受單一交易，系統會自動將您重新導向至PG預設位置建立工作流程。

      全部 [!DNL FreeWheel] 交易建議為單一交易。

   * 如果您接受具有多個PG交易ID的提案，請確定您需要建立的每個PG預設位置。 建立所有必要版位後，「繼續」按鈕就會啟用。

1. （選用）按一下「 」，將PG交易鎖定在其他PG或非PG位置 ![選項功能表](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   交易可以鎖定支援任何媒體型別組合（例如連線電視、桌上型電腦和音訊）的多個位置。

## 手動設定程式化保證交易

請將此方法用於所有其他SSP。

1. [手動設定交易識別碼詳細資料](deal-id-create.md).

1. 儲存交易後，根據提示選取將用於交易的廣告並建立PG預設位置。

   建立交易的PG預設投放位置是交付您100%購買的必備條件。 此型別的刊登位置沒有鎖定目標，因此DSP可以傳回對發佈商提出之每個競標要求的競標。

1. （選用）按一下「 」，將PG交易鎖定在其他PG或非PG位置 ![選項功能表](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   交易可以鎖定支援任何媒體型別組合（例如連線電視、桌上型電腦和音訊）的多個位置。

>[!MORELIKETHIS]
>
>* [關於程式化預留交易](programmatic-guaranteed-about.md)
>* [商議程式化保證交易的秘訣](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [提交程式化保證交易的廣告 [!DNL FreeWheel]](freewheel-submit.md)
>* [在交易ID收件匣中接受交易](deal-id-inbox-accept.md)
>* [手動建立交易識別碼詳細資料](deal-id-create.md)
>* [SSP合作夥伴](ssp-partners.md)
>* [庫存功能概要](inventory-overview.md)

