---
title: 查看从馈送生成的数据
description: 了解如何查看从清单数据馈送生成的数据。
exl-id: 961155ac-a9d3-42e4-904b-b968e9f3383b
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# 查看从馈送生成的数据

*[!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan Ads] （仅删除操作），以及 [!DNL Yandex] 仅限帐户*

如果传播馈送数据时没有同时将其发布到广告网络，则可以使用以下方法之一预览数据。 您稍后可以选择 [发布数据](propagated-data-post.md) 从任一位置到相关广告网络。

* 如果您将选项用于&quot;[!UICONTROL Propagate and Preview]，”然后查看生成的批量工作表(名为“`<feed file name>_<template name>`“)从 [!UICONTROL Bulksheets] 视图。 上不包含任何数据 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 选项卡。 此选项允许您 [验证登陆页面](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) 在发布数据之前与广告和关键字相关联。

* 如果您将选项用于&quot;[!UICONTROL Propagate only]，”然后从查看营销活动层次结构视图中生成的数据 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 选项卡。

  Campaign层次结构视图仅显示从信息源文件生成的数据，而不显示现有帐户组件。 将组件及其所有子组件的数据发布到广告网络后，该数据将不再列在营销活动层次结构视图中。

   1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，此时将打开 [!UICONTROL Templates] 选项卡。

   1. （可选）要仅显示为特定模板创建的促销活动组件，请执行以下操作：

      1. 单击模板名称。

      1. 在 [!UICONTROL Accounts] 在左侧导航窗格中展开广告网络节点和广告网络帐户节点，然后选中模板名称旁边的复选框。

   1. 单击 **[!UICONTROL Campaigns]**， **[!UICONTROL Ad Groups]**， **[!UICONTROL Keywords]**，或 **[!UICONTROL Ads]** 选项卡，具体取决于要查看的组件。

      >[!NOTE]
      >
      >* 除非您查看特定模板的数据，否则 [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 选项卡列出了从所有模板和馈送文件创建的所有广告组、关键字和广告。 使用的产品组 [!DNL Google Ads] 购物广告列在 [!UICONTROL Keywords] 选项卡。
      >* 要仅查看特定促销活动的子组件，请先查看 [!UICONTROL Campaigns] 选项卡。 同样，要仅查看特定广告组的子组件，请从查看 [!UICONTROL Ad Groups] 选项卡。

   1. （可选）要查看详细信息，请执行以下任一操作：

      * 要查看任何促销活动、广告组、关键字或广告的设置，请单击 [查看/编辑设置图标](/help/search-social-commerce/assets/settings.png "查看/编辑设置图标") 在名称旁边。

      * 要查看营销活动或广告组的子组件，请执行以下操作：

         * 要列出营销活动中的所有广告组，请单击营销活动名称。

         * 要列出广告组中的所有关键字或产品目标，请单击广告组名称。

         * 要列出广告组中的所有广告，请单击广告组名称，然后单击 [!UICONTROL Ads] 选项卡。

>[!MORELIKETHIS]
>
>* [关于清单信息源](inventory-feeds-about.md)
>* [编辑从馈送生成的数据](propagated-data-edit.md)
>* [从馈送生成的将营销活动数据发布到广告网络](propagated-data-post.md)
>* [停止库存馈送数据的发布作业](stop-job.md)
>* [从馈送生成的数据的状态](propagated-data-status.md)
