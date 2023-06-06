---
title: 编辑从馈送生成的数据
description: 了解如何编辑从清单数据馈送生成的数据。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# 编辑从馈送生成的数据

*[!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan Ads] （仅删除操作），以及 [!DNL Yandex] 仅限帐户*

如果传播馈送数据时没有同时将其发布到广告网络，则可以通过以下任一方式编辑数据。 您稍后可以选择执行以下操作 [帖子数据](propagated-data-post.md) 从任一位置到相关广告网络：

* 如果您将选项用于&quot;[!UICONTROL Propagate and Preview]，”然后您可以编辑生成的批量处理工作表文件(名为“`<feed file name>_<template name>`“)，方法是从 [!UICONTROL Bulksheets] 查看、编辑文件并重新上传。 上不包含任何数据 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 选项卡。

* 如果您将选项用于&quot;[!UICONTROL Propagate only]，”然后可以使用编辑为组件生成的数据 [[!UICONTROL New] 状态](propagated-data-status.md) 在促销活动层次结构视图中，从 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 选项卡。

   Campaign层次结构视图仅显示从信息源文件生成的数据，而不显示现有帐户组件。 将组件及其所有子组件的数据发布到广告网络后，该组件数据将不再列在营销活动层次结构中。

   1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，此时将打开 [!UICONTROL Templates] 选项卡。

   1. （可选）要仅显示为特定模板创建的促销活动组件，请执行以下操作：

      1. 单击模板名称。

      1. 在 [!UICONTROL Accounts] 左侧导航窗格中的菜单，展开ad network节点和ad network account节点，然后选中模板名称旁边的复选框。
   1. 单击 **[!UICONTROL Campaigns]**， **[!UICONTROL Ad Groups]**， **[!UICONTROL Keywords]**，或 **[!UICONTROL Ads]** 选项卡，具体取决于要查看的组件。

      >[!NOTE]
      >
      >* 除非您查看特定模板的数据，否则 [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 选项卡列出从所有模板和馈送文件创建的所有广告组、关键字和广告。 使用的产品组 [!DNL Google Ads] 购物广告列于 [!UICONTROL Keywords] 选项卡。
      >* 要仅查看特定促销活动的子组件，请从查看 [!UICONTROL Campaigns] 选项卡。 同样，要仅查看特定广告组的子组件，请从查看 [!UICONTROL Ad Groups] 选项卡。


   1. （可选；要仅编辑广告组、关键字或广告）请筛选列表以仅包含特定营销活动或广告组的子组件：

      * 要列出营销策划中的所有广告组，请单击营销策划名称。

      * 要列出广告组中的所有关键字，请单击广告组名称。

      * 要将所有内容列为广告组中的，请单击广告组名称，然后单击 [!UICONTROL Ads] 选项卡。
   1. 单击 [查看/编辑设置图标](/help/search-social-commerce/assets/settings.png "查看/编辑设置图标") 位于营销活动、广告组、关键字或广告名称旁边。

   1. 编辑设置，然后单击 **[!UICONTROL Save]**.



>[!MORELIKETHIS]
>
>* [关于库存信息源](inventory-feeds-about.md)
>* [查看从馈送生成的数据](propagated-data-view.md)
>* [从馈送生成的促销活动数据发布到广告网络](propagated-data-post.md)
>* [停止库存馈送数据的发布作业](stop-job.md)
>* [从馈送生成的数据的状态](propagated-data-status.md)

