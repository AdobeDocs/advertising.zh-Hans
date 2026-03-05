---
title: 管理广告的限制分配
description: 了解如何将限制分配给广告。
feature: Search Optimization, Search Campaign Management
hide: true
exl-id: 9755abb2-a62f-4292-a6b4-314b49de3edd
source-git-commit: aed5f6db36b1aab4d7b4f7d40812a361f0363440
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# （新UI）管理广告的限制分配

*Beta功能*

您可以为以下搜索实体分配和移除竞价约束：营销活动、广告组、关键词、版面、单位级别产品组和动态搜索目标。 每个图元只能有一个约束。

约束由子实体继承，因此除非要覆盖继承的值，否则无需为子实体分配约束。

取消指定约束会删除与帐户组件及其所有子组件的关联，并且这些组件不再能使用该约束的报告数据。 取消指定约束并不会删除约束或帐户组件本身。

>[!NOTE]
>
>* 如果您稍后编辑广告的关键字或广告副本（从而创建新关键字或广告），则约束不会分配给新实体。
>* 活动约束仅限制优化旧关键词级别项目组合中已分配竞价单位的竞价。 对于活跃项目组合中的竞价单位、混合项目组合中的竞价单位或不在项目组合中的竞价单位，它们将被忽略。

## 从新[!UICONTROL Ads]视图为所选广告分配限制

您可以向一个或多个营销活动分配单个限制。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ads]**。

1. 选中要为其分配单个约束的每个广告旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**。

1. 选择约束。

1. 单击&#x200B;**[!UICONTROL Assign Now]**。

## 为旧版[!UICONTROL Campaigns]视图中的选定搜索竞价单位分配限制

1. 在&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;中，选择帐户组件视图。

1. 选中每个相关行旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL More]**，然后单击&#x200B;**[!UICONTROL Assign]** > **[!UICONTROL Constraint]**。

1. 选择适用的约束。

1. （可选）输入其他详细信息：

   1. 在[!UICONTROL Additional Details]旁边，单击&#x200B;**[!UICONTROL Open]**&#x200B;展开详细信息。

   1. 输入可选的&#x200B;**[!UICONTROL Project Name]**&#x200B;和/或可选的&#x200B;**[!UICONTROL Description]**。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 从新[!UICONTROL Ads]视图中取消分配选定营销活动的约束

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ads]**。

1. 选中每个广告旁边的复选框，您将从中取消分配约束。

1. 在批量操作工具栏中，单击&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 单击&#x200B;**[!UICONTROL Confirm]**。

## 从旧版[!UICONTROL Campaigns]视图中的搜索竞价单位取消分配约束

>[!NOTE]
>
>要删除约束条件，使其不可用于将来使用，请参阅优化指南中有关“竞价约束条件”的一章中的“删除搜索竞价单位的约束条件”，该章节可从搜索、社交和Commerce中获取。<!-- verify convention for referencing Optimization Guide here -->

1. 在&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;中，选择帐户组件视图。

1. 选中要从中移除约束的每个元件旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL More]**，然后单击&#x200B;**[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 在确认对话框中，选择&#x200B;**[!UICONTROL Yes, Unassign]**。

>[!MORELIKETHIS]
>
>* [管理营销活动的限制分配](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [管理广告组的限制分配](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
[管理关键字的约束分配](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md)
