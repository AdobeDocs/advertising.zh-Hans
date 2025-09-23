---
title: 管理广告组的限制分配
description: 了解如何将限制分配给广告组。
feature: Search Optimization, Search Campaign Management
hide: true
exl-id: c9960b5a-4b6c-4ef0-8501-5478af2c40da
source-git-commit: df5d34c7d86174107278e0cd4f5a99329a21ca61
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 0%

---

# （新UI）管理广告组的限制分配

*Beta功能*

您可以为以下搜索实体分配和移除竞价约束：营销活动、广告组、关键词、版面、单位级别产品组和动态搜索目标。 每个图元只能有一个约束。

约束由子实体继承，因此除非要覆盖继承的值，否则无需为子实体分配约束。

取消指定约束会删除与帐户组件及其所有子组件的关联，并且这些组件不再能使用该约束的报告数据。 取消指定约束并不会删除约束或帐户组件本身。

## 从新[!UICONTROL Ad Groups]视图将限制分配给选定的广告组

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 选中要为其分配单个约束的每个广告组旁边的复选框。

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

## 从新[!UICONTROL Ad Groups]视图中取消分配选定广告组的约束

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 选中要从中取消分配约束的每个广告组旁边的复选框。

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
