---
title: 編輯可重複使用的對象
description: 瞭解如何編輯可重複使用的對象。
feature: DSP Audiences
exl-id: 4de6b9a4-2907-474d-92bf-83686a1f0b31
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# 編輯可重複使用的對象

當您編輯用於任何版位或其他可重複使用對象的對象時，變更會立即套用至這些版位和對象。<!-- verify -->

1. 在主功能表中，按一下 **[!UICONTROL Audiences]** > **[!UICONTROL All audiences]**.

1. 將游標停留在對象列上並按一下 **[!UICONTROL Edit]**.

1. 透過下列任一方式編輯對象設定：

   >[!NOTE]
   >
   >如果您編輯對象區段邏輯，請詳細 [對象人數資料](audience-about.md) 即會在右側面板中更新。

   * （可選）若要編輯 **[!UICONTROL Audience Name]** 按一下 ![編輯](/help/dsp/assets/edit.png) 在對象名稱旁邊，輸入唯一的對象名稱，然後按一下 **[!UICONTROL Apply]**.

   * （可選）若要手動編輯區段邏輯，請使用 [[!UICONTROL Third Party Segments]， [!UICONTROL First Party Segments]， [!UICONTROL Adobe Segments]， [!UICONTROL Custom Segments]、和 [!UICONTROL Saved Audiences] 索引標籤](audience-settings.md)，請執行下列動作。

      * 若要將區段新增至現有區段群組，請執行下列動作：
      1. 按一下右側面板中的區段群組。

      1. （選用）將群組邏輯變更為 *[!UICONTROL Include Any]*， *[!UICONTROL Include All]*，或 *[!UICONTROL Exclude All]*，視需要而定。

         *[!UICONTROL Exclude All]* 不適用於第一個區段群組。 對於僅包含排除專案的對象，請將此對象建置為 *[!UICONTROL Include Any]* 然後，在位置中，從「排除的對象」選單中選取該對象。

      1. 在左側面板中找出新區段，然後選取區段名稱旁的核取方塊。

         區段群組會自動更新為新區段。
   * 若要新增區段群組：

      1. 按一下 **[!UICONTROL + New Group]** 在右側面板中。

      1. （可選）將上一個群組與新群組之間的邏輯變更為 *[!UICONTROL And]* 或 *[!UICONTROL Or]*，視需要而定。

      1. 在左側面板中找出新群組的區段，並選取區段名稱旁的核取方塊。

      1. （選用）將群組邏輯變更為 *[!UICONTROL Include Any]*， *[!UICONTROL Include All]*，或 *[!UICONTROL Exclude All]*，視需要而定。
   * 若要使用現有對象中的區段邏輯：

      1. 透過下列任一方式，從現有對象複製區段邏輯：

         * 在「所有對象」檢視中，將游標停留在對象列上，然後按一下 **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * 在現有對象的設定中，在區段邏輯面板頂端，按一下 **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * 在文字編輯器中，使用英數字元區段ID手動建立區段邏輯，並且 [布林值語法](audience-segment-logic-syntax.md)，並將其複製到剪貼簿。
      1. 按一下 **[!UICONTROL paste in an audience rule to begin building]**，將現有區段邏輯貼入輸入欄位，然後按一下 **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >如果對象已包含任何區段邏輯，則貼入新區段邏輯會覆寫現有邏輯。





1. 单击 **[!UICONTROL Save]**.

1. 在確認訊息中，按一下 **[!UICONTROL Continue]**.

>[!MORELIKETHIS]
>
>* [關於對象管理](audience-about.md)
>* [建立可重複使用的對象](reusable-audience-create.md)
>* [複製可重複使用的對象](reusable-audience-duplicate.md)
>* [檢視可重複使用對象的詳細資訊](reusable-audience-view-details.md)
>* [共用可重複使用的對象](reusable-audience-share.md)
>* [匯出可重複使用的對象](reusable-audience-export.md)
>* [將可重複使用對象的區段金鑰複製到剪貼簿](reusable-audience-clipboard.md)
>* [刪除可重複使用的對象](reusable-audience-delete.md)
>* [對象設定](audience-settings.md)
>* [對象區段邏輯的語法](audience-segment-logic-syntax.md)
>* [可用的第三方資料提供者](third-party-data-providers.md)

