---
title: 从馈送生成的促销活动数据发布到广告网络
description: 了解如何将从清单数据馈送生成的数据发布到广告网络。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# 从馈送生成的促销活动数据发布到广告网络

*[!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan Ads] （仅删除操作），以及 [!DNL Yandex] 仅限帐户*

您可以在通过相关模板传播数据时发布从信息源生成的促销活动数据，也可以将其作为单独的流程进行传播。 发布数据后，任何现有的已传播数据都会从 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 列表。

为了成功发布，必须将所有广告组分配给营销活动，将所有关键字和广告分配给广告组，并且必须包含所有必需的信息，且不得违反任何长度。

* 如果您将选项用于&quot;[!UICONTROL Propagate and Preview]，”然后 [发布生成的批量工作表文件](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) (已命名&quot;`<feed file name>_<template name>`“)来自 [!UICONTROL Bulksheets] 视图。

   如果您之前没有 [验证登陆页面](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md)，则可以在发布文件之前执行此操作。

* 如果您将选项用于&quot;[!UICONTROL Propagate only]，”然后可以使用发布为组件生成的数据 [[!UICONTROL New] 状态](propagated-data-status.md) 在促销活动层次结构视图中，从 [!UICONTROL Templates] 选项卡。

   >[!NOTE]
   >
   >活动或已删除的组件可能包括新的子组件，如果数据有效，则可以发布子组件。

   >[!TIP]
   >
   >如果您之前未验证登陆页面并希望进行验证，则 [传播数据并预览](feed-data-propagate.md) 从 [!UICONTROL Bulksheets] 查看，而不是将其发布到广告网络。 然后，您可以 [验证URL](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) 手动将文件发布到广告网络之前。

   1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，此时将打开 [!UICONTROL Templates] 选项卡。

   1. 选中模板旁边的复选框。

   1. 在工具栏中，单击 **[!UICONTROL Post]**.

   1. 在过帐设置中，在字段中输入或选择信息，然后单击 **[!UICONTROL Post]**.

      * **[!UICONTROL Selection]：** 过帐哪些帐户组件。

      * **[!UICONTROL Scheduling]：** 何时发布文件：

         * *[!UICONTROL Post to search engine now]* （默认）：根据传播的信息源数据创建批量工作表文件，然后立即开始发布该文件。

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]：* 创建批量工作表文件并在稍后发布该文件。 指定以下内容：

            * **[!UICONTROL Start Time]：** 批量处理工作表文件应发布到广告网络的未来日期和时间。 默认情况下，文件在隔天的00:00 (12:00 a.m.)发送。 **注意：** 对于需要较长处理时间的大型文件，无法立即在营销活动管理视图或网络的广告管理器中获取发布的数据。

            * **[!UICONTROL End Time]：** 可根据以下日期暂停或删除已发布广告的未来日期和时间： [馈送数据设置](feed-settings-manage.md#feed-data-settings) 对于&quot;[!UICONTROL When the Scheduled End Date is reached].” 默认情况下，结束时间是从今天开始的30天的00:00 (12:00 a.m.)。 选择 **[!UICONTROL None]** 无限期地保持数据活动（或在您为模板传播新数据之前），或指定日期和时间。

               要指定日期，请使用DD/MM/YYYY或D/M/YYYY格式或单击 [日历](/help/search-social-commerce/assets/calendar.png "日历") 打开日历和 [选择日期](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). 要更改时间，请以24小时制HH/MM或H/M输入时间，或从列表中选择时间（以30分钟为间隔）。
         * *[!UICONTROL Preview in Bulksheet Management Area only, post later]：**创建可从以下位置访问的批量工作表文件： [!UICONTROL Search] > [!UICONTROL Bulksheets] 视图。 您可以选择从此处发布文件。

            当生成的批量工作表文件大于2 MB时，该文件为ZIP格式。 您无需解压缩文件即可发布它。
      * **[!UICONTROL Generate Tracking URLs]：** 是否在批量工作表文件中包含关键字和广告变体的跟踪URL： *[!UICONTROL Yes]* （默认）或 *[!UICONTROL No]*.

         如果您选择 *[!UICONTROL Yes]*，则根据关键字和广告的基本URL生成URL [!UICONTROL Tracking Methods] 中的参数 [帐户设置](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) 或者，如果您要将数据映射到现有营销策划，则映射到 [!UICONTROL Tracking Methods] 现有参数中的参数 [campaign设置](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

         如果相关项目存在跟踪URL，则它们不会重新生成，除非需要新项目（例如，如果关键词匹配类型、创意文本或帐户的跟踪参数已更改）。

      * **[!UICONTROL Bulksheet Name]：** 要从传播的信息源数据创建的批量处理工作表文件的名称。 默认情况下，该文件名为 `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. 您可以根据需要重命名文件，但该文件必须以以下文件扩展名之一结尾： `.tsv` （对于制表符分隔的值）， `.txt` （对于ASCII文本）， `.csv` （对于逗号分隔的值），或 `.zip` （对于压缩的TSV文件）。 对于包含国际字符的数据，请使用TSV或TXT格式。

         发布的文件位于 [!UICONTROL Bulksheets] 查看30天，无论您是否将其发布到广告网络。



“[!UICONTROL Last Prop. Status]“”列显示适用模板的作业状态。

创建批量工作表时，它会列在 [!UICONTROL Bulksheets] 视图。 发布文件后，将发送一封电子邮件通知，其中包含指向文件的链接。 但是，如果无法发布全部或部分数据，则会在 [!UICONTROL Bulksheets] 视图，并发送包含错误文件链接的电子邮件通知。

>[!NOTE]
>
>* 无论您选择什么计划选项，指定的数据都会从 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 列表。
>* 处理大量数据需要更长的时间。 您可以在此过程中跟踪文件的进度。
>* 所有发布的数据都受该网络的编辑流程约束。
>* 在发布批量处理工作表文件之前，您可以 [取消过帐](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).


>[!MORELIKETHIS]
>
>* [关于库存信息源](inventory-feeds-about.md)
>* [查看从馈送生成的数据](propagated-data-view.md)
>* [编辑从馈送生成的数据](propagated-data-edit.md)
>* [停止库存馈送数据的发布作业](stop-job.md)
>* [从馈送生成的数据的状态](propagated-data-status.md)

