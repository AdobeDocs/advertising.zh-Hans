---
title: 从馈送生成的将营销活动数据发布到广告网络
description: 了解如何将清单数据馈送生成的数据发布到广告网络。
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# 从馈送生成的将营销活动数据发布到广告网络

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （仅删除操作）和仅[!DNL Yandex]帐户*

您可以在通过相关模板传播数据时发布从信息源生成的营销活动数据，也可以将其作为单独的流程进行传播。 发布数据后，将从[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]列表中删除任何现有的传播数据。

要成功发布，必须将所有广告组分配给营销活动，将所有关键词和广告分配给广告组，并且必须包括所有必需的信息，且不得出现任何长度冲突。

* 如果您使用选项“[!UICONTROL Propagate and Preview]”，则[从[!UICONTROL Bulksheets]视图发布生成的批量处理工作表文件](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) （名为“`<feed file name>_<template name>`”）。

  如果您之前未[验证登陆页面](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md)，则可以在发布文件之前进行验证。

* 如果您将选项用于“[!UICONTROL Propagate only]”，则可以从[!UICONTROL Templates]选项卡在营销活动层次结构视图中发布状态为[[!UICONTROL New]的组件的生成数据](propagated-data-status.md)。

  >[!NOTE]
  >
  >活动或已删除的组件可能包括新的子组件，如果数据有效，则可以发布子组件。

  >[!TIP]
  >
  >如果您之前未验证登陆页面，但希望验证登陆页面，请[传播数据并从[!UICONTROL Bulksheets]视图中预览它](feed-data-propagate.md)，而不是将数据发布到广告网络。 然后，您可以在手动将文件发布到广告网络之前[验证URL](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md)。

   1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，这将打开到[!UICONTROL Templates]选项卡。

   1. 选中模板旁边的复选框。

   1. 单击工具栏中的&#x200B;**[!UICONTROL Post]**。

   1. 在过帐设置中，在字段中输入或选择信息，然后单击&#x200B;**[!UICONTROL Post]**。

      * **[!UICONTROL Selection]：**&#x200B;哪些帐户组件已过帐。

      * **[!UICONTROL Scheduling]：**&#x200B;何时发布文件：

         * *[!UICONTROL Post to search engine now]* （默认）：从传播的信息源数据创建批量工作表文件，并立即开始发布该文件。

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]：*&#x200B;创建批量处理工作表文件并稍后发布。 指定以下内容：

            * **[!UICONTROL Start Time]：**&#x200B;将来应将批量处理工作表文件发布到广告网络的日期和时间。 默认情况下，会在第二天00:00（中午12:00）发送文件。 **注意：**&#x200B;对于需要更长时间处理的大型文件，发布的数据无法立即在营销活动管理视图或网络的广告管理器中获取。

            * **[!UICONTROL End Time]：**&#x200B;根据“[!UICONTROL When the Scheduled End Date is reached]”的[信息源数据设置](feed-settings-manage.md#feed-data-settings)，可以暂停或删除已发布广告的未来日期和时间。 默认情况下，结束时间是从今天开始的00:00(12:00 a. m.) 30天。 选择&#x200B;**[!UICONTROL None]**&#x200B;以无限期地保持数据活动（或在您为模板传播新数据之前），或指定日期和时间。

              要指定日期，请使用DD/MM/YYYY或D/M/YYYY格式，或单击![日历](/help/search-social-commerce/assets/calendar.png "日历")以打开日历，并[选择日期](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md)。 要更改时间，请以24小时制HH/MM或H/M输入时间，或从列表中选择时间（以30分钟为间隔）。

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]：**&#x200B;创建可从[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Bulksheets]视图访问的批量工作表文件。 您可以选择从此处发布文件。

           当生成的批量处理工作表文件大于2 MB时，该文件为ZIP格式。 您无需解压缩文件即可发布该文件。

      * **[!UICONTROL Generate Tracking URLs]：**&#x200B;是否在批量处理工作表文件中包含关键字和广告变体的跟踪URL： *[!UICONTROL Yes]*（默认值）或&#x200B;*[!UICONTROL No]*。

        如果选择&#x200B;*[!UICONTROL Yes]*，则根据[帐户设置](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)中的[!UICONTROL Tracking Methods]参数或从关键字和广告的基本URL生成URL，如果将数据映射到现有营销活动，则从现有[营销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)中的[!UICONTROL Tracking Methods]参数生成URL。

        如果相关项目存在跟踪URL，则不会重新生成这些URL，除非需要新的URL（例如，如果关键词匹配类型、创意文本或帐户的跟踪参数已更改）。

      * **[!UICONTROL Bulksheet Name]：**&#x200B;要从传播的信息源数据创建的批量处理工作表文件的名称。 默认情况下，该文件名为`<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`。 您可以根据需要重命名文件，但文件必须以下列文件扩展名之一结尾： `.tsv` （对于制表符分隔的值）、`.txt` （对于ASCII文本）、`.csv` （对于逗号分隔的值）或`.zip` （对于压缩的TSV文件）。 对于包含国际字符的数据，请使用TSV或TXT格式。

        发布的文件在[!UICONTROL Bulksheets]视图中可用30天，无论您是否将其发布到广告网络。

“[!UICONTROL Last Prop. Status]”列显示适用模板的作业状态。

创建批量工作表后，它将列在[!UICONTROL Bulksheets]视图中。 发布文件时，将发送一封包含文件链接的电子邮件通知。 但是，如果无法发布全部或部分数据，则会在[!UICONTROL Bulksheets]视图中列出一个错误文件，并发送一封包含指向错误文件链接的电子邮件通知。

>[!NOTE]
>
>* 无论您选择何种计划选项，都会从[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]列表中删除指定的数据。
>* 处理大量数据需要更长的时间。 您可以在此过程中跟踪文件的进度。
>* 所有发布的数据都受制于网络的编辑流程。
>* 在发布批量工作表文件之前，您可以[取消发布](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md)。

>[!MORELIKETHIS]
>
>* [关于清单信息源](inventory-feeds-about.md)
>* [查看从馈送生成的数据](propagated-data-view.md)
>* [编辑从馈送生成的数据](propagated-data-edit.md)
>* [停止库存馈送数据的发布作业](stop-job.md)
>* [从馈送生成的数据的状态](propagated-data-status.md)
