---
title: 管理标签分类
description: 了解如何使用标签分类对帐户组件进行分组。
feature: Search Label Classifications
source-git-commit: 84eb5f060a696e057f706c0066c18c9afc1511e1
workflow-type: tm+mt
source-wordcount: '1515'
ht-degree: 0%

---

# 管理标签分类

标签分类可帮助您将帐户组件分组为有意义的集。 例如，您可以创建一个名为“地域”的父标签分类，为分类中的每个地理区域（例如“英国”和“日本”）创建不同的标签值，然后将标签值分配给您的[竞价单位](/help/search-social-commerce/glossary.md#a-b)或父促销活动。 然后，您可以将任何标签值作为单独的列包含在视图和报表中，并根据不同的分类组和值对报表进行子透视。

## 标签分类的组件

### 标签分类

每个广告商最多可以具有30个标签分类，这些分类属于顶级类别。 创建标签分类后，即可为该分类创建特定的标签值。

### 标签值

每个标签分类最多可以具有2000个值。 为分类创建特定标签值后，您可以使用批量处理工作表](#classification-values-assign-bulksheets)从促销活动管理视图](#classification-values-assign-campaign-management)或[将标签值分配给促销活动、广告组、关键字、广告、投放位置和产品组[。

每个符合条件的实体都可以拥有多个分类的标签值，但每个分类只能有一个标签值。 标签值由子实体继承，但可以覆盖。 在最低层分配的值始终会覆盖在父层分配的值。

## “标签分类”视图

[!UICONTROL Reports] > [!UICONTROL Labels Classifications]视图包含[!UICONTROL Classifications]和[!UICONTROL Label Values]个子视图。 默认情况下，将显示关键词级别标签分类和值的数据，但您可以选择查看广告级别分类和值的数据。

## 可用操作

* 查看标签分类的数据。

* 查看标签分类值的数据。

* [创建标签分类](#classification-create)。

* 使用批量处理工作表](#classification-values-assign-bulksheets)从营销活动管理视图](#classification-values-assign-campaign-management)或[将分类值分配给帐户组件[。

* [从帐户组件中删除标签分类值](#classification-values-remove)。

* [删除标签分类值](#classification-values-delete)。

* [删除标签分类](#classification-delete)。

## 创建标签分类 {#classification-create}

<!-- Update links to bulksheet columns once I have new files/paths -->

1. 单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Label Classifications]**。

1. 单击右上角的&#x200B;**[!UICONTROL Create Classification]**。

1. 输入唯一的标签分类名称，然后单击&#x200B;**[!UICONTROL Create]**。

   该名称对于广告商帐户必须是唯一的，且包含[个32-126](https://www.asciitable.com/)的ASCII字符，最大长度为27个单字节字符。 名称不能与现有报表列或现有批量处理工作表列的名称相同。 查看[百度](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md)、[Google广告](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)、[Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)、[Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)、[Yahoo！的批量工作表列的名称 日本广告](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md)，[Yahoo！ 显示网络](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md)和[Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md)。

## 从营销活动管理视图将分类值分配给帐户组件 {#classification-values-assign-campaign-management}

您可以从营销活动管理视图中分配和移除以下搜索实体的分类值：营销活动、广告组、关键词、广告、投放位置、单位级别产品组和动态搜索目标。 如有必要，您可以在分配过程中创建分类和分类值。 每个标签分类最多可以具有2000个值。

每个实体在每个分类中可以有一个标签值。 例如，Shoes_Campaign的“颜色”值可以为“红色”，“地域”值可以为“洛杉矶”，但不能为“颜色”或“地域”具有多个值。

标签值由子实体继承，因此除非要覆盖继承的值，否则不要为子实体输入值。

>[!NOTE]
>
>您为某些广告网络和促销活动类型创建的关键字和广告副本的时间是[不可变的](/help/search-social-commerce/campaign-management/faqs-campaigns.md)，这意味着编辑它们会删除现有实体并创建一个新实体。 以这种方式删除现有实体时，标签分类不会分配给新实体。

1. 从&#x200B;**[!UICONTROL Manage]**&#x200B;或&#x200B;**[!UICONTROL Target]**&#x200B;菜单打开实体视图。

1. 选中每个相关行旁边的复选框。

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

## 使用批量处理工作表将分类值分配给帐户组件 {#classification-values-assign-bulksheets}

<!-- Update bulksheet references to ones in new UI -->

您可以使用批量处理工作表将标签分类与以下搜索实体的值相关联：促销活动、广告组、关键词、广告、投放位置、单位级别产品组和动态搜索目标。 每个标签分类最多可以具有2000个值。

每个实体在每个分类中可以有一个标签值。 例如，Shoes_Campaign的“颜色”值可以为“红色”，“地域”值可以为“洛杉矶”，但不能为“颜色”或“地域”具有多个值。

标签值由子实体继承，因此除非要覆盖继承的值，否则不要为子实体输入值。

>[!NOTE]
>
>您为某些广告网络和促销活动类型创建的关键字和广告副本的时间是[不可变的](/help/search-social-commerce/campaign-management/faqs-campaigns.md)，这意味着编辑它们会删除现有实体并创建一个新实体。 以这种方式删除现有实体时，标签分类不会分配给新实体。

1. [下载包含要为其分配标签分类值的实体的批量工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)：

   * 在[!UICONTROL Rows and Columns]选项卡上，展开[!UICONTROL Bulksheet Columns]窗格中的[!UICONTROL Campaign]列表。

   * 展开[!UICONTROL Label Classification]列表。

   * 选择要在批量处理工作表文件中包含列的每个分类。

     例如，如果您包含标签分类“颜色”和“地域”，则批量工作表将包含“颜色”和“地域”列。

1. 在编辑器中打开文件，并将标签值添加到要与其关联的实体的标签分类列中。 每个值的最大长度为100个字符，可包含ASCII和非ASCII字符。

   请参阅下一节中的示例值。

   除了添加值之外，您还可以通过从相关行中删除现有值来删除这些值。 要从父实体及其子实体中移除值，请a)仅包含父实体行并移除现有的分类值，或者b)同时包含父实体及其子实体，并从所有父行和子行移除现有的分类值。

1. [上载文件](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md)以创建关联。<!-- Update once the new bulksheet UI is GA -->

上传的标签值在相关的实体视图中可见。

### 要在批量处理工作表中上载的标签分类值示例

此示例包括标签分类“颜色”和“地域”的列。 对于您自己的批量处理工作表，请将列替换为您自己的标签分类名称。

| 帐户 | 营销活动 | 广告组 | 关键词 | 广告 | 投放 | 标签 | 颜色 | 地域 |
|---|---|---|---|---|---|---|---|---|
| Acct1 | C1 | | | | | | 绿色 | |
| Acct1 | C1 | AG1 | | | | | | |
| Acct1 | C1 | AG1 | K1 | | | | | UK |
| Acct1 | C1 | AG1 | K2 | | | | 红色 | AU |
| Acct1 | C1 | AG1 | K3 | | | | 蓝色 | DE |
| Acct1 | C1 | AG1 | | A1 | | | | |
| Acct1 | C1 | AG1 | | A1 | | | 红色 | |
| Acct1 | C1 | AG1 | | | P1 | | 红色 | AU |
| Acct1 | C1 | AG1 | | | P2 | | 蓝色 | DE |

## 从帐户组件中删除标签分类值 {#classification-values-remove}

删除分类值将删除与帐户组件及其所有子组件的关联。 分类值的报表数据不再可用于这些组件。 删除分类值不会删除该值，也不会删除帐户组件。

>[!NOTE]
>
>若要从标签分类中删除值，请参阅&quot;[删除标签分类值](#classification-values-delete)&quot;。

1. 从&#x200B;**[!UICONTROL Manage]**&#x200B;或&#x200B;**[!UICONTROL Target]**&#x200B;菜单打开实体视图。

1. 选中每个相关行旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在批量操作工具栏中，单击&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**。

1. 选中要从所选实体中删除的每个分类值旁边的复选框。<!-- As of 2/24/26, no way to tell which entity each value is assigned to -->

   要选择所有分配的值，请单击&#x200B;**[!UICONTROL Select All]**。 要取消选择所有分配的值，请单击&#x200B;**[!UICONTROL Deselect All]**。

1. 单击&#x200B;**[!UICONTROL Unassign Selected]**。

## 删除标签分类值 {#classification-values-delete}

删除标签分类值会使其在将来不可用，并且报表数据不再可用于这些值。 虽然删除了值及其父标签分类和特定帐户组件之间的所有分配，但不会删除父标签分类和促销活动组件。

>[!NOTE]
>
>若要取消分类值与帐户组件的关联，请参阅“[从帐户组件中删除标签分类值](#classification-values-remove)”。

1. 单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Label Classifications]**。

1. 单击&#x200B;**[!UICONTROL Label Values]**&#x200B;选项卡。

1. （可选）筛选列表以包含特定的标签值。

1. 选中要删除的每个标签值旁边的复选框。

   一次最多可以删除200行。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在批量操作工具栏中，单击![删除](/help/search-social-commerce/assets/delete.png "删除")。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。

## 删除标签分类

删除分类会删除其子值与帐户组件之间的所有关联。 已删除的分类及其值不可供将来使用。 分类值的报表数据不再可用。

>[!NOTE]
>
>若要取消分类值与帐户组件的关联，请参阅“[从帐户组件中删除标签分类值](#classification-values-remove)”。

1. 单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Label Classifications]**。

1. （可选）筛选列表以包含特定的标签分类。

1. 选中要删除的每个标签分类旁边的复选框。

   一次最多可以删除200行。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在批量操作工具栏中，单击![删除](/help/search-social-commerce/assets/delete.png "删除")。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。
