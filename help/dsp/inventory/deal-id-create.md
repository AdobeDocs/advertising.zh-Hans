---
title: 手動建立交易識別碼詳細資料
description: 瞭解如何手動輸入交易ID的詳細資料。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 20a57919-c68f-4c9d-a8e1-f49484f74655
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# 手動建立交易識別碼詳細資料

1. 在主功能表中，按一下 **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. 在資料表格上方，按一下 **[!UICONTROL Create]**，然後選取 **[!UICONTROL Deal ID]**.

1. 輸入 [交易設定](deal-id-settings.md)：

   1. 在 [!UICONTROL Deal ID basics] 區段，指定交易詳細資訊以及可存取交易的廣告商。 對於保證交易，您還必須指定計畫的投放日期和預估的曝光次數，僅供追蹤之用。

      您可以在「詳細目錄>交易」檢視中加入「PG曝光步調」支出欄，以追蹤保證交易的步調。

   1. （僅限管理員使用者；選擇性）在 [!UICONTROL Technical] 區段，視需要編輯預設設定。

   1. 单击 **[!UICONTROL Save]**.

1. （僅限保證交易）選取要用於交易的廣告，並建立預設程式化保證(PG)位置。

   預設PG位置可確保您的交易一律傳回每個競標請求的競標。 如果您未建立預設的PG位置，則任何以交易為目標的位置都不會投標，除非其設定正確。 您應一律建立預設的PG位置。 在 [!UICONTROL Placements] 檢視，預設PG位置有 [!UICONTROL Sub-type] 「 」的欄值[!UICONTROL PG Default].」

   您可以選擇將交易用作其他位置的詳細目錄目標，但必須正確設定才能進行競標。

   1. 在 [!UICONTROL Ad & Campaign Selection] 設定，選取將用於交易的廣告：

      1. 選取廣告商、行銷活動和廣告型別。 選擇性地選取廣告狀態，以篩選廣告。

      1. 從可用廣告清單中，選取要用於交易的每個廣告旁的核取方塊。

      1. 单击 **[!UICONTROL Apply]**.
   1. 在位置設定畫面中：

      1. 輸入位置名稱。

      1. （可選）編輯 [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)，包括覆寫預設競標（自動以交易的CPM值填入）、變更日期範圍，或附加更多廣告。

      交易會自動在詳細目錄目標區段中定位。 所有其他鎖定目標選項均不適用。

      1. 单击 **[!UICONTROL Create placement]**.



建立交易後，您可以將交易作為多個位置的詳細目錄目標。

>[!NOTE]
>
> 您不需要將交易標籤傳送給發行者進行驗證。

>[!TIP]
>
>* 在 [!UICONTROL Inventory] > [!UICONTROL Deals] 檢視， [!UICONTROL Pacing & Budget] 欄顯示交易如何步調到指定的投放日期和曝光目標。
>
>* 如果傳送速度不佳或速度過快，請聯絡您的發佈商，以調整透過交易傳送的傳送量。


>[!MORELIKETHIS]
>
>* [手動交易識別碼設定](deal-id-settings.md)
>* [設定程式化保證交易](programmatic-guaranteed-set-up.md)
>* [提交程式化保證交易的廣告 [!DNL FreeWheel]](freewheel-submit.md)
>* [關於程式化預留交易](programmatic-guaranteed-about.md)

   <!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->

