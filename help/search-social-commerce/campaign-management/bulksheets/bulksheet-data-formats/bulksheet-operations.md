---
title: 可在批量处理工作表中执行的操作
description: 引用有关使用批量处理工作表添加、编辑和删除营销活动数据的一般信息。
exl-id: 17ec9307-6dfd-45cb-b8bd-d0d7fcbf2d41
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# 可在批量处理工作表中执行的操作

您可以通过批量工作表为[支持的广告网络](../bulksheet-about.md#bulksheet-functionality-by-network)添加、编辑和删除促销活动数据。

为您要添加、编辑或删除或者要添加、编辑或删除其属性的每个营销活动组件（营销活动、广告组、关键字或文本广告）添加单独的数据行。 例如，如果要创建一个包含一个广告组、一个关键字和一个广告（共四个组件）的营销活动，则需要四个单独的数据行。 但是，要编辑广告组（一个组件）的[!UICONTROL Ad Group Name]，您只需要一行。 同样，要为一个广告组（一个组件）编辑四个不同的属性，您只需要一行。

以下规则适用于使用营销活动组件及其属性。

* 正在添加：

   * 要添加组件，请包含添加该组件所需的所有字段，以及（可选）包含用于任何组件属性的字段。

   * 要为现有组件（如广告组的[!UICONTROL Ad Group End Date]）添加属性，请包含编辑该组件（广告组）所需的所有字段以及属性([!UICONTROL Ad Group End Date])的字段。

* 要编辑现有组件的属性，请包含编辑该组件所需的所有字段以及该属性的字段。

  如果将属性字段留空，则会保留现有值。

* 正在删除：

   * 要删除现有组件，请包含编辑该组件所需的所有字段，并将其状态更改为[!UICONTROL Deleted]。 例如，要删除一个[!DNL Google Ads]广告组，您必须包含值为<i>[!UICONTROL Deleted]</i>的[!UICONTROL Campaign Name]、[!UICONTROL Ad Group Name]、[!UICONTROL Ad Group Status]和[!UICONTROL Ad Group ID]。

   * （仅限[!UICONTROL Param1]、[!UICONTROL Param2]和[!UICONTROL Param3]值）要删除关键字的现有[!DNL paramN]值，请包含编辑关键字所需的所有字段，并通过在相应字段中输入值`[delete]`（包括括号）来删除现有[!DNL paramN]值。

   * （允许的属性字段）要删除组件的现有属性值，请包含编辑该组件所需的所有字段，还可以通过输入值`[delete]`（包括括号）来删除属性值。 允许的字段包括：

      * （仅限[!UICONTROL Google Ads]） [!UICONTROL Description Line 1]，[!UICONTROL Description Line 2]

      * （仅限[!DNL Google Ads]和[!DNL Microsoft Advertising]） [!UICONTROL Product Scope Filter]、[!UICONTROL Base URL/Final URL]、[!UICONTROL Tracking Template]

>[!NOTE]
>
>如果将某个值包含在不适用于操作的字段中，则该字段中输入的任何值都会被忽略。

>[!MORELIKETHIS]
>
>* [关于使用批量处理工作表管理营销活动数据](../bulksheet-about.md)
>* [支持的批量处理工作表文件格式](bulksheet-file-formats.md)
>* [附录 — 批量处理工作表错误](../bulksheet-errors.md)
>* [下载/创建批量处理工作表文件](../bulksheet-download.md)
