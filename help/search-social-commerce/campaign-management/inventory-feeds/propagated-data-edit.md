---
title: 编辑从馈送生成的数据
description: 了解如何编辑从清单数据馈送生成的数据。
exl-id: d43b593d-758d-4561-9cda-33b235099cc6
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# 编辑从馈送生成的数据

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （仅删除操作）和仅[!DNL Yandex]帐户*

如果传播馈送数据时没有同时将其发布到广告网络，则可以使用以下任一方式编辑数据。 您稍后可以选择从任一位置[将数据发布到相关广告网络：](propagated-data-post.md)

* 如果您使用了选项“[!UICONTROL Propagate and Preview]”，则可以通过从[!UICONTROL Bulksheets]视图下载生成的批量处理工作表文件（名为“`<feed file name>_<template name>`”）、编辑该文件并再次上传来编辑该文件。 [!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]选项卡上不包含任何数据。

* 如果您使用选项“[!UICONTROL Propagate only]”，则可以从[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]选项卡编辑营销活动层次结构视图中状态为[[!UICONTROL New]的组件的生成数据](propagated-data-status.md)。

  Campaign层次结构视图仅显示从信息源文件生成的数据，而不显示现有帐户组件。 将组件及其所有子组件的数据发布到广告网络后，该数据将不再列在促销活动层级中。

   1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，这将打开到[!UICONTROL Templates]选项卡。

   1. （可选）要仅显示为特定模板创建的促销活动组件，请执行以下操作：

      1. 单击模板名称。

      1. 在左侧导航窗格的[!UICONTROL Accounts]菜单中，展开广告网络节点和广告网络帐户节点，然后选中模板名称旁边的复选框。

   1. 根据要查看的组件，单击&#x200B;**[!UICONTROL Campaigns]**、**[!UICONTROL Ad Groups]**、**[!UICONTROL Keywords]**&#x200B;或&#x200B;**[!UICONTROL Ads]**&#x200B;选项卡。

      >[!NOTE]
      >
      >* 除非您查看特定模板的数据，否则[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]选项卡将列出所有从所有模板和馈送文件创建的广告组、关键字和广告。 用于[!DNL Google Ads]购物广告的产品组列在[!UICONTROL Keywords]选项卡上。
      >* 要仅查看特定营销活动的子组件，请首先查看[!UICONTROL Campaigns]选项卡。 同样，要仅查看特定广告组的子组件，请首先查看[!UICONTROL Ad Groups]选项卡。

   1. （可选；要仅编辑广告组、关键字或广告）请筛选列表以仅包含特定营销活动或广告组的子组件：

      * 要列出营销活动中的所有广告组，请单击营销活动名称。

      * 要列出广告组中的所有关键字，请单击广告组名称。

      * 要将所有内容列为一个广告组，请单击该广告组的名称，然后单击“[!UICONTROL Ads]”选项卡。

   1. 单击促销活动、广告组、关键字或广告名称旁边的[查看/编辑设置图标](/help/search-social-commerce/assets/settings.png "查看/编辑设置图标")。

   1. 编辑设置，然后单击&#x200B;**[!UICONTROL Save]**。

>[!MORELIKETHIS]
>
>* [关于清单信息源](inventory-feeds-about.md)
>* [查看从馈送生成的数据](propagated-data-view.md)
>* [从馈送生成的促销活动数据发布到广告网络](propagated-data-post.md)
>* [停止库存馈送数据的发布作业](stop-job.md)
>* [从馈送生成的数据的状态](propagated-data-status.md)
