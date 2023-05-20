---
title: 建立及實作自訂區段
description: 瞭解如何建立和實施自訂區段，以追蹤對廣告公開的使用者或造訪您網頁的使用者。
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# 建立及實作自訂區段

您可以建立並實作自訂DSP區段，藉此收集您自己的第一方對象資料。 您可以使用區段來追蹤a)從案頭、行動裝置和CTV裝置接觸到廣告的使用者，以及b)造訪特定網頁的使用者。 您稍後可以使用其他廣告重新鎖定區段中的使用者，或避免區段中的使用者收到其他廣告。

>[!NOTE]
>
>若要追蹤網站上消費者選擇退出銷售請求的使用者ID，請根據加州消費者隱私法(CCPA)，建立 [CCPA選擇退出銷售區段](ccpa-opt-out-segment-create.md).

1. 建立區段：

   1. 在主功能表中，按一下 **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. 在資料表格上方，按一下 **[!UICONTROL Create]**.

   1. 輸入唯一值 **[!UICONTROL Segment Name]**.

   1. 對於 **[!UICONTROL Segment Type]**，選取 *[!UICONTROL Custom]*.

   1. 輸入 **[!UICONTROL Segment Window]**，即使用者的Cookie在區段中保留的天數。

      預設期間為45天。 輸入從一(1)到365的值。

   1. 单击 **[!UICONTROL Save]**.

1. 視需要複製並實作標籤以追蹤區段：

   1. 返回至 **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. 將游標停留在區段列上並按一下 **[!UICONTROL Get Pixel]**.

      * 若要追蹤網頁的案頭和行動訪客：

         1. 複製標示為「 」的頁面檢視追蹤標籤[!UICONTROL Desktop or mobile websites].」

         1. 為廣告商或網站連絡人提供標籤以進行部署。

            廣告商的IT部門或其他群組可能需要排程標籤部署，或通知標籤部署。
      * 若要追蹤在桌上型電腦、行動裝置或CTV裝置上向廣告單元公開的使用者：

         1. 複製標示為「 」的曝光追蹤標籤[!UICONTROL Desktop or mobile ads].」


1. 將標籤新增至 [!UICONTROL Pixel] 標籤內的每個相關廣告或至 [!UICONTROL Event Pixels] 部分 [[!UICONTROL Tracking] 每個相關位置的設定](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

實施追蹤標籤後，您便可以在任何位置的對象目標或排除專案中使用區段。

>[!TIP]
>
>在追蹤使用者時追蹤區段大小。

>[!MORELIKETHIS]
>
>* [關於對象管理](audience-about.md)
>* [編輯區段資訊](segment-edit.md)
>* [刪除區段](segment-delete.md)
>* [檢視區段的追蹤畫素](segment-view-pixels.md)
>* [共用或停止共用區段](segment-share.md)
>* [建立及實作 [!UICONTROL CCPA Opt-Out-of-Sale] 區段](ccpa-opt-out-segment-create.md)
>* [建立可重複使用的對象](reusable-audience-create.md)
>* [可用的第三方資料提供者](third-party-data-providers.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)

