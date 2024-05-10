---
title: 通过模板传播库存馈送数据
description: 了解如何通过广告模板从库存馈送传播数据，以管理帐户结构和投放动态广告。
exl-id: 9660af19-a517-4593-9a99-da600a0285a5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 0%

---

# 通过模板传播库存馈送数据

*[!DNL Google Ads]， [!DNL Microsoft Advertising]， [!DNL Yahoo! Japan Ads] （仅删除操作），以及 [!DNL Yandex] 仅限帐户*

创建特定于广告网络的信息源模板并关联信息源文件或 [!DNL Google] 或 [!DNL Microsoft] 借助商户中心帐户，您可以根据以下内容通过模板传播馈送数据来动态创建广告 [馈送数据设置](feed-settings-manage.md). 在传播过程中，模板中的列名称会被替换为馈送中的数据值，并且生成的营销活动及其组件具有默认设置，除非模板另外指定。 根据模板选项，Search、Social和Commerce会为广告创建新帐户结构（促销活动、广告组、关键词）或将广告映射到现有帐户结构。

当新馈送数据包含项目的新数据值，或者模板发生更改时，将删除现有广告并创建新广告。 如果唯一更改是指 [!DNL Google Ads] Param 1和Param 2 ，然后只更新这些值。 绝不会创建重复的广告（相同的广告文案和登陆页面）。

在传播数据时，您可以选择在促销活动层次结构视图中预览生成的数据，生成批量处理工作表文件以供审阅，或生成批量处理工作表文件以立即发布到广告网络。 完成每个传播操作后，将在“传播”选项卡中添加传播摘要，以指示已创建、暂停或删除的每个实体类型的数量。 如果不立即发布数据，则可以在稍后预览和发布数据。

## 从传播信息源文件 [!UICONTROL Templates] 选项卡

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，此时将打开 [!UICONTROL Templates] 选项卡。

1. 选中要传播的模板旁边的复选框。

1. 在工具栏中，单击 **[!UICONTROL Propagate]**，然后选择以下选项之一：

   * **[!UICONTROL Propagate Only]：** 要在以下位置显示传播的数据，请 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 选项卡。 您仍然可以在以后从发布任何组件及其子组件的数据 [!UICONTROL Templates] 选项卡。

   * **[!UICONTROL Propagate and Preview]：** 创建批量处理工作表文件(名为&quot;`<feed file name>_<template name>`&quot;)，该页面请参见 [!UICONTROL Bulksheets] 查看以进行审核(但不在 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 选项卡)。 您稍后可以从以下位置发布批量工作表文件： [!UICONTROL Bulksheets] 视图。

     当生成的批量处理工作表文件大于2 MB时，该文件为ZIP格式。 您无需解压缩文件即可发布该文件。

   * **[!UICONTROL Propagate and Post to SE]：** 创建批量处理工作表文件(名为&quot;`<feed file name>_<template name>`“)立即排队等候发布到广告网络。 批量工作表文件可在 [!UICONTROL Bulksheets] 视图，但它在 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 选项卡。

     当生成的批量处理工作表文件大于2 MB时，该文件为ZIP格式。

   “最后一个Prop。 “状态”列显示适用模板的作业状态。

   完成每个传播操作后，传播摘要将添加到 [!UICONTROL Propagations] 选项卡，指示根据传播已创建、暂停或删除的每个实体类型的数量。 预计值不包括从广告网络自己的广告编辑器中进行的更改。

## 从传播信息源文件 [!UICONTROL Feeds] 列表

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. 在数据表上方的工具栏中，单击 **[!UICONTROL Feeds]**.

1. 选中馈送文件旁边的复选框。

1. 在数据表的上方，单击 **[!UICONTROL Propagate/Post Feed Data]**，然后选择以下选项之一：

   * **[!UICONTROL Propagate Only]：** 要在以下位置显示传播的数据，请 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 选项卡。 您仍然可以在以后从发布任何组件及其子组件的数据 [!UICONTROL Templates] 选项卡。

   * **[!UICONTROL Propagate and Preview]：** 创建批量处理工作表文件(名为&quot;`<feed file name>_<template name>`&quot;)，该页面请参见 [!UICONTROL Bulksheets] 查看以进行审核(但不在 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 选项卡)。 您稍后可以从以下位置发布批量工作表文件： [!UICONTROL Bulksheets] 视图。

     当生成的批量处理工作表文件大于2 MB时，该文件为ZIP格式。 您无需解压缩文件即可发布该文件。

   * **[!UICONTROL Propagate and Post to SE]：** 创建批量处理工作表文件(名为&quot;`<feed file name>_<template name>`“)立即排队等候发布到广告网络。 批量工作表文件可在 [!UICONTROL Bulksheets] 视图，但它在 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 选项卡。

     当生成的批量处理工作表文件大于2 MB时，该文件为ZIP格式。

1. 在弹出窗口中，选中每个模板旁边的复选框，以便通过每个模板从馈送文件传播数据，然后单击 **[!UICONTROL Propagate Feed]**.

   将列出与文件关联的所有模板。

此 [!UICONTROL Templates] 选项卡将打开，并且&#39;&#39;[!UICONTROL Last Prop. Status]“”列显示适用模板的作业状态。

完成每个传播操作后，传播摘要将添加到 [!UICONTROL Propagations] 选项卡，指示根据传播已创建、暂停或删除的每个实体类型的数量。 预计值不包括从广告网络自己的广告编辑器中进行的更改。

## 查看传播摘要

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. 单击 **[!UICONTROL Propagations]** 选项卡。

1. 在模板名称旁边，单击 ![查看/编辑设置图标](/help/search-social-commerce/assets/settings.png "查看/编辑设置图标") .

## 停止传播作业

您可以在作业仍在排队时停止库存馈送数据的传播作业。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，此时将打开 [!UICONTROL Templates] 选项卡。

1. 在&quot;[!UICONTROL Last Prop. Status]”列，单击 **[!UICONTROL Cancel]**.

>[!MORELIKETHIS]
>
>* [关于清单信息源](inventory-feeds-about.md)
>* [管理库存馈送的广告模板](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [查看从馈送生成的数据](propagated-data-view.md)
>* [编辑从馈送生成的数据](propagated-data-edit.md)
>* [从馈送生成的将营销活动数据发布到广告网络](propagated-data-post.md)
>* [停止库存馈送数据的发布作业](stop-job.md)
>* [从馈送生成的数据的状态](propagated-data-status.md)
