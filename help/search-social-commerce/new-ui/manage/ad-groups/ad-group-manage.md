---
title: 管理广告组
description: 了解如何创建和管理广告组。
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: e120af366651028227306e993e73f125f29a431f
workflow-type: tm+mt
source-wordcount: 1676
ht-degree: 0%

---

# 管理广告组

<!-- Go through all -->

*Beta功能*

广告组包括一组广告及其相关关键词。 在营销活动中定位显示网络的广告组还可以包括投放位置，投放位置是显示网络中广告可以出现的位置。 适用于广告组所有组件的广告组设置因广告网络而异。

一旦您[使广告网络帐户可通过API连接访问](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)，并且Search、Social和Commerce已将帐户数据与广告网络同步，您即可为[支持的营销活动类型](/help/search-social-commerce/introduction/supported-inventory.md)创建广告组。 您还可以编辑和更改广告组的状态。

有关每个广告网络可用功能的详细信息，请参阅[支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)。

## 关于[!UICONTROL Ad Groups]视图 {#ad-group-view-about}

[!UICONTROL Manage] > [!UICONTROL Ad Groups]视图在筛选视图中列出了选定广告商帐户的所有广告组。

### 可用操作

* [创建广告组](#ad-group-create)

* [从行中重命名广告组](#ad-group-rename)

* [编辑广告组设置](#ad-group-edit)

* [在行中更改广告组的状态或删除广告组](#ad-group-status)

* [在[!UICONTROL Ad Groups]视图中查看性能图](#ad-group-performance-graph)

* [将竞价约束分配给广告组，取消分配广告组的约束](#ad-group-constraints)

* [将标签分类分配给广告组，并从广告组中删除标签分类](#ad-group-classifications)

* [从[!UICONTROL Ad Groups]视图管理数据视图报告](#ad-group-reports)

## 创建广告组 {#ad-group-create}

>[!TIP]
>
>若要同时创建大量广告组，请使用<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [营销活动批量处理工作表](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 单击&#x200B;**[!UICONTROL Create Ad Group]**。

1. 指定[百度](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-baidu.md)、[Google广告](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-google.md)、[LY广告](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yahoo-japan.md)、[Microsoft Advertising](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-microsoft.md)或[Yandex](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yandex.md)广告组设置。

1. 单击&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，请单击![编辑](/help/search-social-commerce/assets/edit-new.png "编辑")并更改广告组设置。

1. 单击&#x200B;**[!UICONTROL Create]**。

之后，您可以选择通过为广告组中的各个关键字或投放位置设置竞价来覆盖广告组级别的竞价。

## 重命名广告组 {#ad-group-rename}

快速重命名广告组，而无需打开完整的广告组设置。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 将光标悬停在广告组行上并单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Rename]**。

1. 编辑名称，然后单击&#x200B;**[!UICONTROL Apply]**。

## 编辑广告组设置 {#ad-group-edit}

您可以编辑单个广告组的设置。 您还可以同时编辑多个广告组的某些字段，包括所有选定广告组通用的某些广告组详细信息、预算选项和URL选项。

>[!TIP]
>
>您还可以使用<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or-->批量编辑数据 [营销活动批量处理工作表](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 执行以下任一操作：

   * 将光标悬停在实体名称上并单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Edit]**。

   * 选中广告组旁边的复选框。 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Edit]**。

1. 编辑[百度](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-baidu.md)、[Google广告](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-google.md)、[LY广告](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yahoo-japan.md)、[Microsoft Advertising](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-microsoft.md)或[Yandex](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yandex.md)广告组设置。

1. 单击&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，请单击![编辑](/help/search-social-commerce/assets/edit-new.png "编辑")并更改广告组设置。

1. 单击&#x200B;**[!UICONTROL Update]**。

## 更改广告组的状态 {#ad-group-status}

无需打开完整的广告组设置，即可快速更改广告组的状态。

您可以暂停受支持广告网络上的任何活动广告组以禁止对其投标。 您稍后可以通过将状态更改回“活动”来恢复竞价。

您还可以删除任何活动或暂停的广告组。 已删除的广告组将从广告网络删除。 当您将其包含在数据过滤器中时，它们仍可见，但无法进行更改。

### 激活或暂停广告组

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 将光标悬停在广告组行上并单击[!UICONTROL Status]列旁边的![编辑](/help/search-social-commerce/assets/edit.png "编辑")。

1. 更改状态：

   * 要激活暂停的广告组，请选择&#x200B;**[!UICONTROL Active]**。

   * 要暂停活动的广告组，请选择&#x200B;**[!UICONTROL Paused]**。

### 删除广告组

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 执行以下任一操作：

   * 将光标悬停在广告组行上并单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Delete]**。

   * 将光标悬停在广告组行上并单击[!UICONTROL Status]列旁边的![编辑](/help/search-social-commerce/assets/edit.png "编辑")。 选择&#x200B;**[!UICONTROL Deleted]**。

## 管理广告组的竞价限制分配 {#ad-group-constraints}

每个图元只能有一个约束。 约束由子实体继承，因此除非要覆盖继承的值，否则无需为子实体分配约束。

取消指定约束会删除与帐户组件及其所有子组件的关联，并且这些组件不再能使用该约束的报告数据。 取消指定约束并不会删除约束或帐户组件本身。

### 从新[!UICONTROL Ad Groups]视图为选定的广告组分配竞价限制

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 选中要为其分配单个约束的每个广告组旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**。

1. 选择约束。

1. 单击&#x200B;**[!UICONTROL Assign Now]**。

### 为旧版[!UICONTROL Campaigns]视图中的选定搜索竞价单位分配竞价限制

1. 在&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;中，选择帐户组件视图。

1. 选中每个相关行旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL More]**，然后单击&#x200B;**[!UICONTROL Assign]** > **[!UICONTROL Constraint]**。

1. 选择适用的约束。

1. （可选）输入其他详细信息：

   1. 在[!UICONTROL Additional Details]旁边，单击&#x200B;**[!UICONTROL Open]**&#x200B;展开详细信息。

   1. 输入可选的&#x200B;**[!UICONTROL Project Name]**&#x200B;和/或可选的&#x200B;**[!UICONTROL Description]**。

1. 单击&#x200B;**[!UICONTROL Save]**。

### 从新[!UICONTROL Ad Groups]视图中删除所选广告组的竞价约束

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 选中要从中取消分配约束的每个广告组旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 单击&#x200B;**[!UICONTROL Confirm]**。

### 从旧版[!UICONTROL Campaigns]视图的搜索竞价单位中删除竞价限制

>[!NOTE]
>
>要删除约束条件，使其不可用于将来使用，请参阅优化指南中有关“竞价约束条件”的一章中的“删除搜索竞价单位的约束条件”，该章节可从搜索、社交和Commerce中获取。

1. 在&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;中，选择帐户组件视图。

1. 选中要从中移除约束的每个元件旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL More]**，然后单击&#x200B;**[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 在确认对话框中，选择&#x200B;**[!UICONTROL Yes, Unassign]**。

## 将标签分类分配给广告组 {#ad-group-classifications}

>[!NOTE]
>
>标签值由子实体继承，因此除非要覆盖继承的值，否则不要为子实体输入值。

### 将分类值分配给广告组

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 选中要为其分配标签值的每个广告组旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在批量操作工具栏中，单击&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**。

1. 对于每个适用的分类值，执行以下操作：

   1. 在&#x200B;**[!UICONTROL Classifications]**&#x200B;列中，指定分类：

      * 要使用现有分类，请单击分类名称以将其展开。

      * 要创建分类，请单击列标题中的[!UICONTROL +]。 在输入字段中，输入分类名称，然后单击![保存](/help/search-social-commerce/assets/save-checkmark.png "保存")以立即保存分类。 要使用新分类，请单击分类名称以将其展开。

        名称必须包含[个32-126](https://www.asciitable.com/)的ASCII字符，最大长度为27个单字节字符。

   1. 在&#x200B;**[!UICONTROL Value Name]**&#x200B;列中，指定所选分类的值：

      * 要使用现有值，请选择该值。

      * 要创建值，请在列标题中单击[!UICONTROL +]。 在输入字段中，输入值，然后单击![保存](/help/search-social-commerce/assets/save-checkmark.png "保存")以立即保存该值并默认选择它。

        最大长度为100个字符，可包含ASCII和非ASCII字符。

1. 单击&#x200B;**+[!UICONTROL Assign Now]**。

### 从广告组中删除标签分类值

删除分类值将删除与帐户组件及其所有子组件的关联。 分类值的报表数据不再可用于这些组件。 删除分类值不会删除该值，也不会删除帐户组件。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 选中将从中删除标签值的每个广告组旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**。

1. 选中要从所选实体中移除的每个分类值旁边的复选框。

   要选择所有分配的值，请单击&#x200B;**[!UICONTROL Select All]**。 要取消选择所有分配的值，请单击&#x200B;**[!UICONTROL Deselect All]**。

1. 单击&#x200B;**[!UICONTROL Unassign Selected]**。

## 在[!UICONTROL Ad Groups]视图中查看性能图 {#ad-group-performance-graph}

打开性能图并配置该图表，其中最多包含指定日期范围内视图中所有广告组的三个合计量度。

### 查看性能图

1. 在数据表的上方，单击![图表](/help/search-social-commerce/assets/charts.png "图表")。

1. （可选）指定要包含在图表中的货币和最多三个量度。

### 隐藏可见的性能图

* 在数据表的上方，单击![图表](/help/search-social-commerce/assets/charts.png "图表")。

## 从[!UICONTROL Ad Groups]视图管理数据视图报告 {#ad-group-reports}

生成一份报表，其中包含[!UICONTROL Ad Groups]视图中一个或多个广告组的数据行，然后以Microsoft Excel工作表文件（XLXS格式）的形式下载该报表。 报告包含视图中的所有可见列。

您可以删除任何生成的报表。

另请参阅&quot;>* [（旧版UI）从营销活动管理视图](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)下载数据&quot;和&quot;[（旧版UI）从[!UICONTROL Downloads]菜单](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)删除性能数据报告或批量处理工作表文件&quot;。

### 生成具有已过滤数据行的报告

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 指定要下载其数据的广告组：

   * 要下载特定广告组的数据，请选中广告组旁边的复选框。

   * 要下载所有广告组的数据，您无需选中任何复选框。 默认情况下包含所有广告组。

1. 在数据表上方的工具栏中，单击![下载报表](/help/search-social-commerce/assets/download.png "下载报表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]设置中，输入唯一的报表名称，然后单击&#x200B;**[!UICONTROL Generate]**。

   默认情况下，该文件名为“ad group_YYYYYMMDD_NNNN”，其中“NNNN”是连续的作业编号（如“ad group_20250402_1326）。

   文件已添加到[!UICONTROL Recently Generated]列表。

1. （可选）要在文件完成后下载文件，请单击文件名旁边的![下载](/help/search-social-commerce/assets/download.png "下载")。

   将按照浏览器的正常过程下载文件。

### 下载已完成的报表

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 在数据表上方的工具栏中，单击![下载报表](/help/search-social-commerce/assets/download.png "下载报表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]对话框的[!UICONTROL Recently Generated]列表中，单击文件名旁边的![下载](/help/search-social-commerce/assets/download.png "下载")。

   将按照浏览器的正常过程下载文件。

### 删除已完成的报告

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ad Groups]**。

1. 在数据表上方的工具栏中，单击![下载报表](/help/search-social-commerce/assets/download.png "下载报表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]对话框的[!UICONTROL Recently Generated]列表中，单击文件名旁边的![删除](/help/search-social-commerce/assets/delete-new.png "删除")。

>[!MORELIKETHIS]
>
>* [管理搜索竞价单位的约束](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [管理营销活动的限制分配](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [管理关键字的约束分配](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [管理投放位置的约束分配](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [（旧版UI）从营销活动管理视图下载数据](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)
>* [（旧版UI）从[!UICONTROL Downloads]菜单删除性能数据报告或批量处理工作表文件](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [[!DNL Baidu] 广告组设置](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-baidu.md)
>* [[!DNL Google Ads] 广告组设置](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-google.md)
>* [[!DNL LY Ads] 广告组设置](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yahoo-japan.md)
>* [[!DNL Microsoft Advertising] 广告组设置](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-microsoft.md)
>* [[!DNL Yandex] 广告组设置](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings/ad-group-settings-yandex.md)
