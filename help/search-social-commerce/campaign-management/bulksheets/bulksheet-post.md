---
title: 发布批量工作表或已更正的错误文件
description: 了解如何将批量工作表文件发布到广告网络。
exl-id: 49b930ba-71b3-442d-a162-67cf7ae14e14
feature: Search Bulksheets
source-git-commit: e5102132a1e4ce25adb297f863db439b583b3ebe
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 0%

---

# 发布批量工作表或已更正的错误文件

您可以将现有的批量工作表文件或更正的错误文件发布到相关帐户 [支持的广告网络](bulksheet-about.md#bulksheet-functionality-by-network). 如果文件为ZIP格式，则无需先解压缩。

批量工作表文件和错误文件在上传或生成后30天会自动删除。

>[!NOTE]
>您还可以在上传文件时发布批量工作表文件或错误文件。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. 选中每个要发布的文件旁边的复选框。

1. 在数据表上方的工具栏中，单击 **[!UICONTROL Post]**.

1. 在对话框中，输入或选择 [[!UICONTROL Post Bulksheet] 设置](#bulksheet-post-settings)，然后单击 **[!UICONTROL Post]**.

   相同的设置适用于您发布的所有文件。

任务开始时，行的状态和计划发布日期将在 [!UICONTROL Bulksheets] 视图。 发布文件时，将发送一封包含文件链接的电子邮件通知。 根据编译的数据量，电子邮件通知可能需要几分钟或更长时间。 但是，如果有任何数据无法发布，则会在 [!UICONTROL Bulksheets] ，并会发送电子邮件通知，其中包含指向错误文件的链接。

>[!NOTE]
>
>* 大量数据需要更长的时间才能发布。 您可以在以下位置关注文件的进度： [!UICONTROL Progress] 中的列 [!UICONTROL Bulksheets] 视图。
>* 所有发布的数据都受制于网络的编辑流程。
* 在发布批量工作表文件之前，您可以取消发布。

## 批量工作表和已更正错误文件的发布设置 {#bulksheet-post-settings}

| 参数 | 描述 |
|----|----|
| [!UICONTROL Account (Search Engine)] | 为其发布数据的广告网络帐户。 如果同时发布多个文件或一个应用于多个帐户的文件，则值为 <i>已选择多个帐户</i>.<br><br>广告网络名称的第一个字母在帐户名称后面的括号中(例如， [!DNL Google Ads] 帐户)。 |
| [!UICONTROL Scheduling] | 何时将文件发布到指定的广告网络：<ul><li><i>[!UICONTROL Post to ad network now]</i> （默认）：立即开始发布数据。</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]：</i> 开始在指定的日期和时间发布数据；默认为明天02:00 （凌晨2点）。 要更改日期，请以DD/MM/YYYY或D/M/YYYY格式输入日期，或单击 ![日历](assets/calendar.png "日历") 打开日历并 [选择日期](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). 要更改时间，请以HH/MM或H/M格式输入时间，或从列表中选择时间（以15分钟为间隔）。</li></ul> |
| [!UICONTROL Generate Tracking URLs] | 是否在具有跟踪模板的帐户中包含跟踪模板和登陆页面后缀（适用于适用的广告网络），或者是否在具有目标URL的帐户中包含嵌入跟踪代码的目标URL(适用于所有关键词、广告、投放位置、站点链接和 [!DNL Google Ads] 过帐中的产品组： <i>[!UICONTROL Yes]</i> （默认）或 <i>[!UICONTROL No]</i>. 不管组合中是否有竞价单位，都无所谓。<br><br>如果您选择 <i>[!UICONTROL Yes]</i>，然后根据 [!UICONTROL Tracking Methods] 相关的帐户设置或campaign设置的部分。 默认情况下，如果跟踪URL存在，则除非需要新的URL，否则不会重新生成这些URL（例如，如果关键词匹配类型、广告文本或相关帐户的跟踪参数已更改）。<br><br>如果您选择 <i>[!UICONTROL No]</i>之后，您仍然可以通过手动发布上传的文件来生成跟踪URL。<br><br><b>注意：</b> 如果广告商使用Adobe Advertising转化跟踪，并且基本URL已更改，则必须生成新的跟踪URL，除非将帐户配置为自动生成和上传跟踪URL。 |
| [!UICONTROL Enable budget changes on optimized campaigns] | 允许根据已发布的数据对优化项目组合中的促销活动进行预算更改。 默认情况下，不选中此选项。 如果选择此选项，则在优化功能确定应重新分配预算（通常在下一个竞价周期）之前，任何指定的营销活动预算更改均适用。<br><br><b>注意：</b> 在发布文件时，因非优化项目组合中的促销活动已发布数据而导致任何预算更改。 更改显示在第二天的营销活动管理视图中。 |
| [!UICONTROL Enable bidding on ads within portfolios] | 当包含的促销活动组件位于优化的项目组合中时，此功能会覆盖优化策略，并允许基于批量处理工作表中的数据进行竞价更改，直到指定的结束日期为止。 如果选择此选项，请在 **[!UICONTROL Hold bulksheet bids until]** 字段。 |

>[!MORELIKETHIS]
>
>* [关于使用批量处理工作表管理营销活动数据](bulksheet-about.md)
>* [下载/创建批量处理工作表文件](bulksheet-download.md)
>* [上传批量工作表或已更正的错误文件](bulksheet-upload.md)
>* [验证批量处理工作表文件中的登陆页面](bulksheet-validate-landing-pages.md)
>* [导出生成或上传的批量处理工作表文件](bulksheet-export.md)
