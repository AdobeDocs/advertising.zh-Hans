---
title: 使用批量处理工作表将分类值分配给帐户组件
description: 了解如何使用批量工作表将分类值分配给帐户组件。
exl-id: b2dfd487-097c-45f8-a6a5-24395fdb2b85
feature: Search Label Classifications
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---

# 使用批量处理工作表将分类值分配给帐户组件

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

1. [上载文件](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md)以创建关联。

上传的标签值在相关的实体视图中可见。

## 要在批量处理工作表中上载的标签分类值示例

此示例包括标签分类“颜色”和“地域”的列。 对于您自己的批量处理工作表，请将列替换为您自己的标签分类名称。

| 帐户 | 营销活动 | 广告组 | 关键词 | 广告 | 投放位置 | 标签 | 颜色 | 地域 |
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

>[!MORELIKETHIS]
>
>* [关于标签分类](classification-about.md)
>* [创建标签分类](classification-create.md)
>* [从营销活动管理视图将分类值分配给帐户组件](classification-values-assign-campaign-management.md)
>* [从帐户组件中删除标签分类值](classification-values-remove.md)
>* [删除标签分类值](classification-values-delete.md)
>* [删除标签分类](classification-delete.md)
