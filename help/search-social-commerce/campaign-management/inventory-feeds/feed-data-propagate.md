---
title: 通过模板传播库存馈送数据
description: 了解如何通过广告模板从库存馈送传播数据，以管理帐户结构和投放动态广告。
exl-id: 9660af19-a517-4593-9a99-da600a0285a5
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 0%

---

# 通过模板传播库存馈送数据

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （仅删除操作）和仅[!DNL Yandex]帐户*

在创建特定于广告网络的馈送模板并将馈送文件或[!DNL Google]或[!DNL Microsoft]商家中心帐户与其关联后，您可以根据[馈送数据设置](feed-settings-manage.md)，通过模板传播馈送数据来动态创建广告。 在传播过程中，模板中的列名称会被替换为馈送中的数据值，并且生成的营销活动及其组件具有默认设置，除非模板另外指定。 根据模板选项，Search、Social和Commerce会为广告创建新帐户结构（促销活动、广告组、关键词）或将广告映射到现有帐户结构。

当新馈送数据包含项目的新数据值，或者模板发生更改时，将删除现有广告并创建新广告。 如果唯一的更改是[!DNL Google Ads] Param 1和Param 2的指定，则仅更新这些值。 绝不会创建重复的广告（相同的广告文案和登陆页面）。

在传播数据时，您可以选择在促销活动层次结构视图中预览生成的数据，生成批量处理工作表文件以供审阅，或生成批量处理工作表文件以立即发布到广告网络。 完成每个传播操作后，将在“传播”选项卡中添加传播摘要，以指示已创建、暂停或删除的每个实体类型的数量。 如果不立即发布数据，则可以在稍后预览和发布数据。

## 从[!UICONTROL Templates]选项卡传播信息源文件

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，这将打开到[!UICONTROL Templates]选项卡。

1. 选中要传播的模板旁边的复选框。

1. 在工具栏中，单击&#x200B;**[!UICONTROL Propagate]**，然后选择以下选项之一：

   * **[!UICONTROL Propagate Only]：**&#x200B;显示[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]选项卡上的传播数据。 您稍后仍可以从[!UICONTROL Templates]选项卡发布任何组件及其子组件的数据。

   * **[!UICONTROL Propagate and Preview]：**&#x200B;创建批量工作表文件（名为“`<feed file name>_<template name>`”），该文件可在[!UICONTROL Bulksheets]视图中查看（但不在[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]选项卡中）。 您稍后可以从[!UICONTROL Bulksheets]视图发布批量处理工作表文件。

     当生成的批量处理工作表文件大于2 MB时，该文件为ZIP格式。 您无需解压缩文件即可发布该文件。

   * **[!UICONTROL Propagate and Post to SE]：**&#x200B;创建立即排队等候发布到广告网络的批量处理工作表文件（名为“`<feed file name>_<template name>`”）。 批量工作表文件在[!UICONTROL Bulksheets]视图中可用，但在[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]选项卡上不可用。

     当生成的批量处理工作表文件大于2 MB时，该文件为ZIP格式。

   “最后一个Prop。 “状态”列显示适用模板的作业状态。

   完成每个传播操作后，将在[!UICONTROL Propagations]选项卡中添加一个传播摘要，以指示基于传播已创建、暂停或删除的每个实体类型的数量。 预计值不包括从广告网络自己的广告编辑器中进行的更改。

## 从[!UICONTROL Feeds]列表传播信息源文件

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Feeds]**。

1. 选中馈送文件旁边的复选框。

1. 在数据表上方单击&#x200B;**[!UICONTROL Propagate/Post Feed Data]**，然后选择以下选项之一：

   * **[!UICONTROL Propagate Only]：**&#x200B;显示[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]选项卡上的传播数据。 您稍后仍可以从[!UICONTROL Templates]选项卡发布任何组件及其子组件的数据。

   * **[!UICONTROL Propagate and Preview]：**&#x200B;创建批量工作表文件（名为“`<feed file name>_<template name>`”），该文件可在[!UICONTROL Bulksheets]视图中查看（但不在[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]选项卡中）。 您稍后可以从[!UICONTROL Bulksheets]视图发布批量处理工作表文件。

     当生成的批量处理工作表文件大于2 MB时，该文件为ZIP格式。 您无需解压缩文件即可发布该文件。

   * **[!UICONTROL Propagate and Post to SE]：**&#x200B;创建立即排队等候发布到广告网络的批量处理工作表文件（名为“`<feed file name>_<template name>`”）。 批量工作表文件在[!UICONTROL Bulksheets]视图中可用，但在[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]选项卡上不可用。

     当生成的批量处理工作表文件大于2 MB时，该文件为ZIP格式。

1. 在弹出窗口中，选中每个模板旁边的复选框，以便通过它们传播源文件中的数据，然后单击&#x200B;**[!UICONTROL Propagate Feed]**。

   将列出与文件关联的所有模板。

[!UICONTROL Templates]选项卡打开，“[!UICONTROL Last Prop. Status]”列显示适用模板的作业状态。

完成每个传播操作后，将在[!UICONTROL Propagations]选项卡中添加一个传播摘要，以指示基于传播已创建、暂停或删除的每个实体类型的数量。 预计值不包括从广告网络自己的广告编辑器中进行的更改。

## 查看传播摘要

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**。

1. 单击&#x200B;**[!UICONTROL Propagations]**&#x200B;选项卡。

1. 在模板名称旁边，单击![查看/编辑设置图标](/help/search-social-commerce/assets/settings.png "查看/编辑设置图标") 。

## 停止传播作业

您可以在作业仍在排队时停止库存馈送数据的传播作业。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，这将打开到[!UICONTROL Templates]选项卡。

1. 在模板名称旁边的“[!UICONTROL Last Prop. Status]”列中，单击&#x200B;**[!UICONTROL Cancel]**。

>[!MORELIKETHIS]
>
>* [关于清单信息源](inventory-feeds-about.md)
>* [管理库存馈送的广告模板](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [查看从馈送生成的数据](propagated-data-view.md)
>* [编辑从馈送生成的数据](propagated-data-edit.md)
>* [从馈送生成的促销活动数据发布到广告网络](propagated-data-post.md)
>* [停止库存馈送数据的发布作业](stop-job.md)
>* [从馈送生成的数据的状态](propagated-data-status.md)
