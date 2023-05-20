---
title: 將PG交易的廣告提交至 [!DNL FreeWheel]
description: 瞭解如何在上向發佈者請求程式化預留交易的廣告核准 [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# 提交程式化保證交易的廣告至 [!DNL Freewheel]

*帳戶具有 [!DNL FreeWheel] 僅限程式化保證許可權*

一旦您 [接受與FreeWheel上的發行者之間的程式化保證交易](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)，包括選取廣告和建立用於交易的程式化預留預設位置，您必須將廣告提交至 [!DNL Freewheel] 以取得核准。

>[!PREREQUISITES]
>
>與您的Adobe客戶團隊合作，確保 [!DNL DSP] 帳戶具有使用 [!DNL FreeWheel] 程式化保證工作流程。

1. 複製搭配使用的廣告的廣告金鑰 [!DNL Freewheel] 交易：

   1. 按一下行銷活動的名稱。

   1. 在子功能表中，按一下 **[!UICONTROL Ads]**.

   1. 按一下  **[!UICONTROL ...]** > **[!UICONTROL Edit]** 位於廣告名稱旁。

   1. 開啟廣告設定後，複製瀏覽器位址列中所顯示URL中的英數字元廣告金鑰。

      例如，在以下URL中，廣告金鑰為 `3NtNC5ZbaGZtqbei8jD3`

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. 將廣告提交至 [!DNL Freewheel]：

   1. 執行下列任一項作業：

      * 在廣告名稱旁邊，按一下  **[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**.

      * 在主功能表中，按一下 **[!UICONTROL Inventory]** > **[!UICONTROL Deals]**. 在交易列中，按一下 ![選項功能表](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**.
   1. 驗證交易ID，輸入 **[!UICONTROL Ad Key]** 您已複製步驟1，然後按一下 **[!UICONTROL Submit]**.

   廣告必須先提交並核准，才能執行。

1. [檢查廣告提交狀態](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [設定程式化預留交易的概述 [!DNL Freewheel]](freewheel-overview.md)
>* [在交易ID收件匣中接受交易](deal-id-inbox-accept.md)
>* [檢查廣告的狀態 [!DNL FreeWheel] 程式化預留交易](freewheel-check-status.md)
>* [的錯誤代碼 [!DNL Freewheel] 廣告提交](freewheel-error-codes.md)

