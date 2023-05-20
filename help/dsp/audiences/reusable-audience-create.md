---
title: 建立可重複使用的對象
description: 瞭解如何建立可重複使用的對象，其中包含對象區段和其他已儲存的對象。
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# 建立可重複使用的對象

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

您可以儲存和管理可重複使用的對象，這些對象是對象區段群組，甚至是其他儲存的對象，您可以將其用作多個位置的目標或排除專案。

1. 在主功能表中，按一下 **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. 在資料表格上方，按一下 **[!UICONTROL Create]**.

1. 輸入唯一值 [!UICONTROL Audience Name].

1. （選用）取消選取選項，以 **[!UICONTROL Share with all advertisers in my account]**.

   當您共用對象時，該對象會成為帳戶內所有廣告商的目標或排除專案。 不過，對象中的個別區段僅適用於共用區段的使用者。 例如，如果您將包含Adobe Analytics區段的對象與未對應至相同區段的廣告商共用 [!DNL Analytics] 則區段不會在該廣告商的對象中預覽。 只有該廣告商可用的區段才會預覽在對象中。

1. 单击 **[!UICONTROL Save]**.

1. 建立對象：

   >[!NOTE]
   >
   >當您建立對象時，請詳細 [對象人數資料](audience-about.md) 在右側面板中更新

   * 若要手動建立區段邏輯，請使用 [[!UICONTROL Third Party Segments]， [!UICONTROL First Party Segments]， [!UICONTROL Adobe Segments]， [!UICONTROL Custom Segments]、和 [!UICONTROL Saved Audiences] 索引標籤](audience-settings.md)，請執行下列動作。

      * 若要新增第一個區段，請在左側面板中找出該區段，然後選取區段名稱旁的核取方塊。

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




1. 单击 **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [關於對象管理](audience-about.md)
>* [對象設定](audience-settings.md)
>* [對象區段邏輯的語法](audience-segment-logic-syntax.md)
>* [可用的第三方資料提供者](third-party-data-providers.md)
>* [建立及實作自訂區段](custom-segment-create.md)
>* [建立及實作 [!UICONTROL CCPA Opt-Out-of-Sale] 區段](ccpa-opt-out-segment-create.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)

