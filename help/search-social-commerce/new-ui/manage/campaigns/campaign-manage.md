---
title: 管理营销活动
description: 了解如何创建和管理广告营销活动。
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: fc836f17b53a3708bf881dc62a437d391709a050
workflow-type: tm+mt
source-wordcount: 2285
ht-degree: 0%

---

# 管理营销活动

*Beta功能*

营销策划是广告网络帐户的主要组成部分。 对于大多数促销活动类型，它包含一组广告组或广告集。 促销活动设置包括促销活动预算参数、广告目标和促销活动中所有广告的可选跟踪参数。 营销活动级别的跟踪参数将覆盖帐户级别的参数，但跟踪参数本身可能会在较低的级别被覆盖。

一旦您[使广告网络帐户可通过API连接访问](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)，并且Search、Social和Commerce已将该帐户数据与广告网络同步，您就可以使用[支持的营销活动类型](/help/search-social-commerce/introduction/supported-inventory.md)创建新的营销活动。 您还可以编辑和更改营销策划的状态。

有关每个广告网络可用功能的详细信息，请参阅[支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)。

## 关于[!UICONTROL Campaigns]视图 {#campaign-view-about}

[!UICONTROL Manage] > [!UICONTROL Campaigns]视图在筛选视图中列出了选定广告商帐户的所有营销活动。 您可以通过单击促销活动名称，在促销活动中打开广告组列表。

当您在[!UICONTROL Campaigns]视图中添加和编辑促销活动数据时，Search、Social和Commerce会立即将数据更改推送到广告网络。 搜索、Social和Commerce还每天提取营销活动结构数据并单击数据，或者在检测到新营销活动时更频繁地提取数据。 对于所有同步的广告网络，您还可以根据需要按需同步帐户。

Search、Social和Commerce每小时从同步的[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户中提取一次性能数据，每天从其他同步的广告网络帐户中提取一次性能数据。

### 可用操作

* [创建营销活动](#campaign-create)

* [从行中重命名营销活动](#campaign-rename)

* [编辑Campaign设置](#campaign-edit)

* [在行中更改营销活动的状态或删除营销活动](#campaign-status)

* [将营销活动分配给项目组合，并从项目组合中删除营销活动](#campaign-portfolio)

* [在[!UICONTROL Campaigns]视图中查看性能图](#campaign-performance-graph)

* [将竞价限制分配给活动，并取消分配活动中的限制](#campaign-constraints)

* [将目标限制分配给活动，并从活动中取消分配目标限制](#campaign-target-constraints)

* [将标签分类分配给促销活动，并从促销活动中移除标签分类](#campaign-classifications)

* [从[!UICONTROL Campaigns]视图管理数据视图报告](#campaign-reports)

## 创建营销活动 {#campaign-create}

>[!NOTE]
>
>* 在创建营销活动之前，请在广告商的网页中[实施转化跟踪标记](/help/search-social-commerce/tracking/conversion-tracking-about.md)。
>* 若要同时创建大量营销活动，请使用<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [营销活动批量处理工作表](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 单击&#x200B;**[!UICONTROL Create Campaign]**。

1. 指定[百度](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md)、[Google广告](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md)、[LY广告](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md)、[Microsoft Advertising](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md)或[Yandex](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md)促销活动设置。

1. 单击&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，请单击![编辑](/help/search-social-commerce/assets/edit-new.png "编辑")**[!UICONTROL Edit]**&#x200B;并更改促销活动设置。

1. 单击&#x200B;**[!UICONTROL Create]**。

根据创建促销活动的广告网络的不同，在将促销活动推送到广告网络之前，您可能需要创建关联的广告组和广告。

## 重命名营销活动 {#campaign-rename}

快速重命名营销活动，无需打开完整的营销活动设置。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 将光标悬停在促销活动行上并单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Rename]**。

1. 编辑名称，然后单击&#x200B;**[!UICONTROL Apply]**。

## 编辑Campaign设置 {#campaign-edit}

您可以编辑各个营销活动的设置。 您还可以同时编辑多个营销活动的某些字段，包括所有选定营销活动通用的某些营销活动详细信息、预算选项和URL选项。

>[!TIP]
>
>您还可以使用<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or-->批量编辑数据 [营销活动批量处理工作表](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 执行以下任一操作：

   * 将光标悬停在实体名称上并单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Edit]**。

   * 选中营销活动旁边的复选框。 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Edit]**。

1. 编辑[百度](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md)、[Google广告](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md)、[LY广告](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md)、<!-- [Meta Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-meta.md), --> [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md)或[Yandex](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md)营销活动设置。

1. 单击&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，请单击![编辑](/help/search-social-commerce/assets/edit-new.png "编辑")**[!UICONTROL Edit]**&#x200B;并更改促销活动设置。

1. 单击&#x200B;**[!UICONTROL Update]**。

根据创建该营销活动的广告网络，营销活动可能需要在推送到广告网络之前包含广告组和广告。

## 更改营销活动的状态 {#campaign-status}

快速更改营销活动的状态，而无需打开完整的营销活动设置。

您可以暂停受支持广告网络上的任何活动营销活动以禁止对其投标。 您稍后可以通过将状态更改回“活动”来恢复竞价。

您还可以删除任何活动或暂停的营销活动。 已删除的营销活动会从广告网络中删除。 当您将其包含在数据过滤器中时，它们仍可见，但无法进行更改。

### 激活或暂停营销活动

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 将光标悬停在促销活动行上，然后单击[!UICONTROL Status]列旁边的![编辑](/help/search-social-commerce/assets/edit.png "编辑")。

1. 更改状态：

   * 要激活暂停的营销活动，请选择&#x200B;**[!UICONTROL Active]**。

   * 要暂停活动的营销活动，请选择&#x200B;**[!UICONTROL Paused]**。

### 删除活动

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 执行以下任一操作：

   * 将光标悬停在促销活动行上并单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Delete]**。

   * 将光标悬停在促销活动行上，然后单击[!UICONTROL Status]列旁边的![编辑](/help/search-social-commerce/assets/edit.png "编辑")。 选择&#x200B;**[!UICONTROL Deleted]**。

## 将营销活动分配给项目组合 {#campaign-portfolio}

将促销活动分配到优化的产品组合可让Search、Social和Commerce优化促销活动中关键词和广告的竞价、促销活动预算和竞价策略目标。 您可以在创建项目组合时，或编辑项目组合的设置，从[!UICONTROL Campaigns]视图将营销活动分配给项目组合。

并非所有营销活动类型和广告网络都符合优化条件；请查看可包含在项目组合中的[支持的营销活动类型](/help/search-social-commerce/introduction/supported-inventory.md)列表。 此外，请验证每个营销活动竞价策略](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy)的[优化支持。

>[!NOTE]
>
>每个营销活动只能分配给一个项目组合。 如果您将已与其他项目组合关联的促销活动分配给新项目组合，则会将其从原始项目组合中删除。

### 从[!UICONTROL Campaigns]视图将营销活动分配给现有项目组合

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 选中要分配给单个项目组合的每个营销活动旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Existing Portfolio]**。

1. 选择项目组合。

1. 单击&#x200B;**[!UICONTROL Assign Now]**。

### 从[!UICONTROL Campaigns]视图将营销活动分配给新项目组合

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 选中要为其创建新项目组合的每个营销活动旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL New Portfolio]**。

1. 在[!UICONTROL Create Portfolio]屏幕中，指定项目组合设置。

   您之前选择的营销活动已分配给该营销活动。 您可以选择编辑项目组合的营销活动列表。

   有关项目组合设置的更多信息，请参阅可在搜索、社交和Commerce中找到的“优化指南” 。

1. 单击&#x200B;**[!UICONTROL Review and Save]**。

### 从[!UICONTROL Portfolios]视图更改项目组合的营销活动分配

当您从项目组合中删除某个营销活动时，“搜索”、“社交”和“Commerce”无法优化该营销活动的出价、营销活动预算和竞价策略目标。

该操作将记录在该项目组合的更改历史记录中。

有关优化的更多信息，请参阅优化指南，该指南可从搜索、社交和Commerce中获取。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Portfolios]**。

1. 选中项目组合旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Edit]**。

1. 在项目组合设置中，转到[!UICONTROL Assign Campaigns]部分并更改营销活动分配。

   有关项目组合设置的更多信息，请参阅可在搜索、社交和Commerce中找到的“优化指南” 。

1. 单击&#x200B;**[!UICONTROL Review and Save]**。

1. 查看设置并根据需要进行更改，然后单击&#x200B;**[!UICONTROL Save]**。

## 管理营销活动的竞价限制分配 {#campaign-constraints}

每个图元只能有一个约束。 约束由子实体继承，因此除非要覆盖继承的值，否则无需为子实体分配约束。

取消指定约束会删除与帐户组件及其所有子组件的关联，并且这些组件不再能使用该约束的报告数据。 取消指定约束并不会删除约束或帐户组件本身。

>[!NOTE]
>
>活动约束仅限制优化旧关键词级别项目组合中已分配竞价单位的竞价。 对于活跃项目组合中的竞价单位、混合项目组合中的竞价单位或不在项目组合中的竞价单位，它们将被忽略。

### 从新[!UICONTROL Campaigns]视图为所选营销活动分配竞价限制

您可以向一个或多个营销活动分配单个限制。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 选中要为其分配单个限制条件的每个营销活动旁边的复选框。

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

### 从新[!UICONTROL Campaigns]视图中删除所选营销活动的竞价限制

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 选中要从中取消分配约束的每个营销活动旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 单击&#x200B;**[!UICONTROL Confirm]**。

### 从旧版[!UICONTROL Campaigns]视图的搜索竞价单位中删除竞价限制

>[!NOTE]
>
>要删除约束条件，使其不可用于将来使用，请参阅优化指南中有关“竞价约束条件”的一章中的“删除搜索竞价单位的约束条件”，该章节可从搜索、社交和Commerce中获取。<!-- verify convention for referencing Optimization Guide here -->

1. 在&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;中，选择帐户组件视图。

1. 选中要从中移除约束的每个元件旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL More]**，然后单击&#x200B;**[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 在确认对话框中，选择&#x200B;**[!UICONTROL Yes, Unassign]**。

## 管理营销活动的目标限制分配 {#campaign-target-constraints}

### 从新[!UICONTROL Campaigns]视图为所选营销活动分配目标限制

您可以向一个或多个营销活动分配单个目标限制。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 选中要为其分配单个目标限制条件的每个营销活动旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Target Constraint]**。

1. 选择约束。

1. 单击&#x200B;**[!UICONTROL Assign Now]**。

### 从新[!UICONTROL Campaigns]视图中删除选定营销活动的目标限制

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 选中每个营销活动旁边的复选框，您将从中取消分配目标限制。

1. 在批量操作工具栏中，单击&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Target Constraint]**。

1. 单击&#x200B;**[!UICONTROL Confirm]**。

## 将标签分类分配给营销活动 {#campaign-classifications}

>[!NOTE]
>
>标签值由子实体继承，因此除非要覆盖继承的值，否则不要为子实体输入值。

### 将分类值分配给营销活动

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 选中要为其分配标签值的每个营销活动旁边的复选框。

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

### 从营销活动中删除标签分类值

删除分类值将删除与帐户组件及其所有子组件的关联。 分类值的报表数据不再可用于这些组件。 删除分类值不会删除该值，也不会删除帐户组件。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 选中每个营销活动旁边的复选框，您将从中删除标签值。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**。

1. 选中要从所选实体中移除的每个分类值旁边的复选框。

   要选择所有分配的值，请单击&#x200B;**[!UICONTROL Select All]**。 要取消选择所有分配的值，请单击&#x200B;**[!UICONTROL Deselect All]**。

1. 单击&#x200B;**[!UICONTROL Unassign Selected]**。

## 在[!UICONTROL Campaigns]视图中查看性能图 {#campaign-performance-graph}

打开并配置一个性能图，其中包含指定日期范围内视图中所有促销活动的总计最多三个量度。

### 查看性能图

1. 在数据表的上方，单击![图表](/help/search-social-commerce/assets/charts.png "图表")。

1. （可选）指定要包含在图表中的货币和最多三个量度。

### 隐藏可见的性能图

* 在数据表的上方，单击![图表](/help/search-social-commerce/assets/charts.png "图表")。

## 从[!UICONTROL Campaigns]视图管理数据视图报告 {#campaign-reports}

<!-- Wording??????  Filtered data reports? -->

在[!UICONTROL Campaigns]视图中生成包含一个或多个促销活动数据行的报表，然后以Microsoft Excel工作表文件（XLXS格式）的形式下载该报表。 报告包含视图中的所有可见列。

您可以删除任何生成的报表。

另请参阅&quot;>* [（旧版UI）从营销活动管理视图](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)下载数据&quot;和&quot;[（旧版UI）从[!UICONTROL Downloads]菜单](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)删除性能数据报告或批量处理工作表文件&quot;。

### 生成具有已过滤数据行的报告

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 指定要下载其数据的营销活动：

   * 要下载特定营销活动的数据，请选中营销活动旁边的复选框。

   * 要下载所有营销活动的数据，您无需选中任何复选框。 默认情况下包含所有营销活动。

1. 在数据表上方的工具栏中，单击![下载报表](/help/search-social-commerce/assets/download.png "下载报表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]设置中，输入唯一的报表名称，然后单击&#x200B;**[!UICONTROL Generate]**。

   默认情况下，该文件名为“campaign_YYYYMMDD_NNNN”，其中“NNNN”是连续的作业编号（如“campaign_20250402_1326）。

   文件已添加到[!UICONTROL Recently Generated]列表。

1. （可选）要在文件完成后下载文件，请单击文件名旁边的![下载](/help/search-social-commerce/assets/download.png "下载")。

   将按照浏览器的正常过程下载文件。

### 下载已完成的报表

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 在数据表上方的工具栏中，单击![下载报表](/help/search-social-commerce/assets/download.png "下载报表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]对话框的[!UICONTROL Recently Generated]列表中，单击文件名旁边的![下载](/help/search-social-commerce/assets/download.png "下载")。

   将按照浏览器的正常过程下载文件。

### 删除已完成的报告

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Campaigns]**。

1. 在数据表上方的工具栏中，单击![下载报表](/help/search-social-commerce/assets/download.png "下载报表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]对话框的[!UICONTROL Recently Generated]列表中，单击文件名旁边的![删除](/help/search-social-commerce/assets/delete-new.png "删除")。

>[!MORELIKETHIS]
>
>* [管理搜索竞价单位的约束](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [管理广告组的限制分配](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [管理关键字的约束分配](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [管理投放位置的约束分配](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [（旧版UI）从营销活动管理视图下载数据](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)
>* [（旧版UI）从[!UICONTROL Downloads]菜单删除性能数据报告或批量处理工作表文件](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [[!DNL Baidu] 营销活动设置](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md)
>* [[!DNL Google Ads] 营销活动设置](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md)
>* [[!DNL LY Ads] 营销活动设置](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md)
>* [[!DNL Microsoft Advertising] 营销活动设置](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md)
>* [[!DNL Yandex] 营销活动设置](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md)

<!-- >* [[!DNL Meta Ads] campaign settings](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-meta.md) -->

