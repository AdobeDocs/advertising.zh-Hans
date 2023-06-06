---
title: 使用批量处理工作表将分类值分配给帐户组件
description: 了解如何使用批量工作表将分类值分配给帐户组件。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 7%

---

# 使用批量处理工作表将分类值分配给帐户组件

您可以使用批量处理工作表将标签分类与以下搜索实体的值相关联：促销活动、广告组、关键字、广告、版面、单元级别的产品组以及动态搜索目标。 每个标签分类最多可以具有2000个值。

每个实体在每个分类中可以有一个标签值。 例如，Shoes_Campaign的“颜色”值可以是“红色”，而“地域”值可以是“洛杉矶”，但“颜色”或“地域”不能有多个值。

标签值由子实体继承，因此除非要覆盖继承的值，否则不要为子实体输入值。

>[!NOTE]
>
>您的某些广告网络和促销活动类型的关键字和广告文案包括 [不可变](/help/search-social-commerce/campaign-management/faqs-campaigns.md)，这意味着编辑它们会删除现有实体并创建新实体。 以这种方式删除现有实体时，标签分类未分配给新实体。

1. [下载批量处理工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) 其中包括要为其分配标签分类值的实体：

   * 在 [!UICONTROL Rows and Columns] 选项卡，展开 [!UICONTROL Campaign] 中的列表 [!UICONTROL Bulksheet Columns] 窗格。

   * 展开 [!UICONTROL Label Classification] 列表。

   * 选择要在Bulksheet文件中包含列的每个分类。

      例如，如果您包含标签分类“颜色”和“地域”，则批量工作表将包含“颜色”和“地域”列。

1. 在编辑器中打开文件，并将标签值添加到要与标签值关联的实体的标签分类列中。 每个值的最大长度为100个字符，可以包含ASCII和非ASCII字符。

   请参阅下一节中的示例值。

   除了添加值之外，您还可以通过从相关行中删除现有值来删除这些值。 要从父实体及其子实体中移除值，请a)仅包含父实体行并移除现有分类值，或者b)同时包含父实体及其子实体，并从所有父实体和子行移除现有分类值。

1. [上传文件](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) 创建关联。

上传的标签值在相关实体视图中可见。

## 要在批量处理工作表中上载的标签分类值示例

此示例包括标签分类“颜色”和“地域”的列。 对于您自己的批量处理工作表，请将列替换为您自己的标签分类名称。

| 帐户 | Campaign | 广告组 | 关键词 | 广告 | 投放位置 | 标签 | 颜色 | 地域 |
|---|---|---|---|---|---|---|---|---|
| Acct1 | C1 |  |  |  |  |  | 绿色 |  |
| Acct1 | C1 | AG1 |  |  |  |  |  |  |
| Acct1 | C1 | AG1 | K1 |  |  |  |  | 英国 |
| Acct1 | C1 | AG1 | K2 |  |  |  | 红色 | AU |
| Acct1 | C1 | AG1 | K3 |  |  |  | 蓝色 | DE |
| Acct1 | C1 | AG1 |  | A1 |  |  |  |  |
| Acct1 | C1 | AG1 |  | A1 |  |  | 红色 |  |
| Acct1 | C1 | AG1 |  |  | P1 |  | 红色 | AU |
| Acct1 | C1 | AG1 |  |  | P2 |  | 蓝色 | DE |

>[!MORELIKETHIS]
>
>* [关于标签分类](classification-about.md)
>* [创建标签分类](classification-create.md)
>* [从营销活动管理视图将分类值分配给帐户组件](classification-values-assign-campaign-management.md)
>* [从帐户组件中删除标签分类值](classification-values-remove.md)
>* [删除标签分类值](classification-values-delete.md)
>* [删除标签分类](classification-delete.md)

