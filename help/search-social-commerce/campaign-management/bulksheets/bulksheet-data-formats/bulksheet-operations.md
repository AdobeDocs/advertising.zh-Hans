---
title: 可在批量处理工作表中执行的操作
description: 引用有关使用批量处理工作表添加、编辑和删除营销活动数据的一般信息。
exl-id: 82969bb8-dff8-48e7-b37d-1446a2a90072
feature: Search Bulksheets
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# 可在批量处理工作表中执行的操作

您可以通过的批量处理工作表添加、编辑和删除营销活动数据 [支持的广告网络](../bulksheet-about.md#bulksheet-functionality-by-network).

为您要添加、编辑或删除或者要添加、编辑或删除其属性的每个营销活动组件（营销活动、广告组、关键字或文本广告）添加单独的数据行。 例如，如果要创建一个包含一个广告组、一个关键字和一个广告（共四个组件）的营销活动，则需要四个单独的数据行。 要编辑 [!UICONTROL Ad Group Name] 但是，对于广告组（一个组件），您只需要一行。 同样，要为一个广告组（一个组件）编辑四个不同的属性，您只需要一行。

以下规则适用于使用营销活动组件及其属性。

* 正在添加：

   * 要添加组件，请包含添加该组件所需的所有字段，以及（可选）包含用于任何组件属性的字段。

   * 为现有组件添加属性，例如 [!UICONTROL Ad Group End Date] 对于广告组，请包含编辑该组件（广告组）所需的所有字段，以及属性的字段([!UICONTROL Ad Group End Date])。

* 要编辑现有组件的属性，请包含编辑该组件所需的所有字段以及该属性的字段。

  如果将属性字段留空，则会保留现有值。

* 正在删除：

   * 要删除现有组件，请包含编辑该组件并更改其状态所需的所有字段 [!UICONTROL Deleted]. 例如，删除 [!DNL Google Ads] 广告组，您必须包含 [!UICONTROL Campaign Name]， [!UICONTROL Ad Group Name]， [!UICONTROL Ad Group Status] 值为 <i>[!UICONTROL Deleted]</i>、和 [!UICONTROL Ad Group ID].

   * ([!UICONTROL Param1]， [!UICONTROL Param2]、和 [!UICONTROL Param3] （仅限值）要删除现有 [!DNL paramN] 关键字的值，包括编辑关键字所需的所有字段并删除现有字段 [!DNL paramN] 输入值 `[delete]` （包括括号）。

   * （允许的属性字段）要删除组件的现有属性值，请包含编辑该组件所需的所有字段，还可以通过输入值来删除属性值 `[delete]` 括号)。 允许的字段包括：

      * ([!UICONTROL Google Ads] 仅限) [!UICONTROL Description Line 1]， [!UICONTROL Description Line 2]

      * ([!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 仅限) [!UICONTROL Product Scope Filter]， [!UICONTROL Base URL/Final URL]， [!UICONTROL Tracking Template]

>[!NOTE]
>
>如果将某个值包含在不适用于操作的字段中，则该字段中输入的任何值都会被忽略。

>[!MORELIKETHIS]
>
>* [关于使用批量处理工作表管理营销活动数据](../bulksheet-about.md)
>* [支持的批量处理工作表文件格式](bulksheet-file-formats.md)
>* [附录 — 批量处理工作表错误](../bulksheet-errors.md)
>* [下载/创建批量处理工作表文件](../bulksheet-download.md)
