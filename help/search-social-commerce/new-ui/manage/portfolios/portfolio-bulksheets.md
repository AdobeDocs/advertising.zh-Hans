---
title: 使用批量工作表文件批量编辑项目组合设置
description: 了解如何使用批量处理工作表文件编辑多个项目组合的设置。
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 20f7419d-9f5e-4477-ae8d-8b85a79b1e81
source-git-commit: 04b6fbaf4a8b360bc3a60bdad4871694d50f1bf9
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# 使用批量工作表文件批量编辑项目组合设置

*Beta功能*

项目组合批量工作表是一个文件，其中包含以特定格式显示的项目组合设置，可用于快速查看和修改设置。 您可以使用一个或多个项目组合的设置生成（下载）批量工作表。 该文件下载为带有两个工作表（XLSX格式）的[!DNL Excel]工作簿。 工作簿包括：

* 只读的[!UICONTROL Instructions]工作表，其中包含有关编辑字段的信息。

* [!UICONTROL Portfolio Settings Edit]选项卡，每个包含的项目组合占一行。 您可以选择根据需要编辑字段，将文件保存在本地，然后[将编辑后的文件](#portfolio-bulksheet-upload)上传到Search、Social和Commerce。 可编辑字段以颜色突出显示。

## 下载包含项目组合设置的批量工作表文件

1. （可选）选中要包含在批量处理工作表中的每个项目组合旁边的复选框。

   如果您未选择特定的项目组合，则可以下载所有项目组合的设置。

1. 在数据表上方的工具栏中，单击：

   * （对于所有项目组合） **[!UICONTROL Bulk Operations]** > **[!UICONTROL Export All Portfolios]**。

   * （对于选定的项目组合） **[!UICONTROL Bulk Operations]** > **[!UICONTROL Export Selected Portfolios]**。

1. 输入要创建的批量处理工作表文件的名称，然后单击&#x200B;**[!UICONTROL Export Now]**。

   该文件将保存到浏览器的默认“下载”文件夹中。

## 上传具有更新的项目组合设置的批量处理工作表文件 {#portfolio-bulksheet-upload}

文件必须为XLSX格式。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Bulk Operations]** > **[!UICONTROL Import Portfolio Details]**。 &lt;！ — 应为“导入Portfolio设置” — “详细信息”可能过于模糊，并表明它可能包含其他内容。—>

1. 在[!UICONTROL Import Portfolio Details File]对话框中：<!-- reword if we change the name of the operation -->

   1. 将文件拖放到框中，或单击&#x200B;**[!UICONTROL Browse File]**<!-- "Browse for file" or just "Browse"??? -->从设备或网络中选择文件。

   1. 单击&#x200B;**[!UICONTROL Import]**。

您可以通过日期范围选择器旁边的[!UICONTROL Global Sync Status]按钮（![全局同步状态](/help/search-social-commerce/assets/global-sync-status.png "全局同步状态")）检查上载状态。<!-- icon similar to Refresh -->。 如果有任何更改不成功，则可以下载一个错误文件，其中显示失败的内容。

通知也会添加到通知中心，您可以从![按钮(](/help/search-social-commerce/assets/notifications-new.png ")旁边的")通知[!UICONTROL Global Sync Status]通知![全局同步状态](/help/search-social-commerce/assets/global-sync-status.png "全局同步状态")图标打开通知窗格。

## 已上传批量处理工作表文件的数据要求

所有批量工作表文件都必须包含列[!UICONTROL Portfolio ID]，并且每个数据行都必须包含值，以使[!UICONTROL Portfolio ID]可操作。 有关数据要求的更多信息，请参阅下载的批量处理工作表文件上的[!UICONTROL Instructions]选项卡。

有关[!UICONTROL Portfolio Settings Edit]选项卡上项目组合设置列的说明，请参阅《优化指南》，该指南可在Search、Social和Commerce中找到。

<!--
## Data fields on the [!UICONTROL Portfolio Settings Edit] tab

| Field | Required to import data? | Description |
| ----- | ------------------------ | ----------- |
| Portfolio ID |  |  |
| Portfolio Name |  |  |
| Status |  |  |
| Spend Strategy |  |  |
| Target |  |  |
| Hybrid |  |  |
| Auto adjust campaign budgets |  |  |
| Spend Multiple |  |  |
| Minimum Campaign Budget |  |  |
| Objective |  |  |
| Cost Half-Life |  |  |
| Revenue Half-Life |  |  |
| Min. Target CPA |  |  |
| Max. Target CPA |  |  |
| Min. Target ROAS |  |  |
| Max. Target ROAS |  |  |

-->

>[!MORELIKETHIS]
>
>* [（新UI）编辑项目组合](portfolio-edit.md)
>* [创建项目组合](portfolio-create.md)
>* [（新UI）关于项目组合](portfolio-about.md)
