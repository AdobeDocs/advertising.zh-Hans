---
title: 建立 [!UICONTROL Simple Ad Serving] 交易
description: 瞭解如何為建立追蹤畫素 [!UICONTROL Simple Ad Serving] 交易。
feature: DSP Simple Ad Serving
exl-id: 77d5dabd-1a0d-4dce-8a9a-8d54a637e15d
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# 建立 [!UICONTROL Simple Ad Serving] 交易

1. 在主功能表中，按一下 **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. 在資料表格上方，按一下 **[!UICONTROL Create]**，然後選取 **[!UICONTROL Simple Ad Serving]**.

1. 輸入 [交易設定](simple-deal-settings.md)：

   1. 在 [!UICONTROL Select Ad Source] 區段，指定發行者、廣告商和促銷活動以及廣告型別的相關資訊，然後按一下 **[!UICONTROL Next]**.

   1. 在 [!UICONTROL Select Ad(s)] 部分，指定在DSP中當作Proxy使用的廣告：

      1. 執行下列任一項作業：

         * 針對現有廣告，選取要使用的廣告。

         * 對於新廣告，請建立Proxy [協力廠商廣告](/help/dsp/campaign-management/ads/ad-create-multiple.md).
      >[!NOTE]
      > DSP不提供您指定的廣告。 發佈者會提供廣告。

      1. 单击 **[!UICONTROL Next]**.
   1. 在「摘要詳細資料」中，編輯摘要詳細資料，然後按一下 **[!UICONTROL Next]**.

      DSP會自動產生位置，名為「SAS位置 — &lt;*交易名稱*>，」代表廣告。 在刊登版位中，會自動將目標鎖定在 [!UICONTROL Inventory Targets] 區段。 所有其他鎖定目標選項均不適用。



1. 透過下列任一種方式，將事件追蹤畫素傳送給發佈者以進行實作：

   * （選用）從 [!UICONTROL Activate Tag with Publisher] 畫面，傳送交易標籤給發佈者。

      完成上述步驟後，DSP會產生電子郵件訊息，您可傳送給發行者。 該訊息包含交易細節、從中擷取交易標籤的連結，以及連結的授權代碼。

      1. 檢閱交易詳細資料，然後執行下列任一項作業：

         * 若要將資訊貼到裝置上電子郵件應用程式的電子郵件訊息中，請按一下 **[!UICONTROL Email & Done]** 並選取電子郵件應用程式。 此 [!UICONTROL CC:] 欄位已預先填入 [!DNL Adobe] 支援地址。 然後，您可以將訊息傳送給發行者的適當連絡人。

         * 若要將資訊複製到剪貼簿，請按一下 **[!UICONTROL Copy Email].** 然後，您可以手動將內容貼入電子郵件訊息，並傳送給發佈者的適當連絡人。 您必須將副本（副本：）包含到 `publisher-support-global@adobe.com`. 完成訊息複製後，請按一下 **[!UICONTROL Email & Done]**.
      1. （如有必要）請洽詢發佈者，檢視標籤是否包含適當的巨集，讓標籤可與發佈者的廣告伺服器搭配使用。
   * （選用）手動將事件追蹤畫素傳送給發佈者：

      1. 在的交易列中 [!UICONTROL Deals] 檢視，按一下 ![選項功能表](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         事件畫素包括 [!UICONTROL Clickthrough] 畫素和 [!UICONTROL Impression] 畫素。 影片和音訊廣告也包含按四分位數結束的事件畫素(從 [!UICONTROL 25% Complete] 至 [!UICONTROL 100% Complete])。

      1. 複製事件追蹤畫素，並將其提供給您的發佈者。



>[!MORELIKETHIS]
>
>* [關於 [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] 設定](simple-deal-settings.md)
>* [檢視交易的詳細報告](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
