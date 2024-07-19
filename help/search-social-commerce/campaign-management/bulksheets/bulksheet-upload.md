---
title: 上传批量工作表或已更正的错误文件
description: 了解如何手动上传批量工作表文件或更正登陆页面验证错误文件。
exl-id: 44c76ca3-1d3e-43c2-868a-4868157d32b0
feature: Search Bulksheets
source-git-commit: 6b3c876f17d0e30dcce69048bb4041fc8cd29902
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 0%

---

# 上传批量工作表或已更正的错误文件

您可以从设备或网络中为[支持的广告网络](bulksheet-about.md#bulksheet-functionality-by-network)上传批量工作表文件、已更正的登陆页验证错误文件以及其他已更正的错误文件。 上传文件时，会删除文件中的任何自定义列。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Upload Bulksheet]**。

1. 在[[!UICONTROL Upload Bulksheet]设置](#bulksheet-upload-settings)中输入或选择信息。

1. 单击&#x200B;**[!UICONTROL Apply]**。

当任务开始时，文件将列在[!UICONTROL Bulksheets]视图中。 文件完成后，将发送电子邮件通知，其中包含指向文件的链接。 根据编译的数据量，电子邮件通知可能需要几分钟或更长时间。 但是，如果文件生成失败，则会在[!UICONTROL Bulksheets]视图上列出一个错误文件，并发送带有错误文件链接的电子邮件通知。

>[!NOTE]
>
>如果将批量处理工作表数据发布到广告网络，则可以跟踪[!UICONTROL Bulksheets]视图中[!UICONTROL Progress]列中的文件进度。 大量数据需要更长的时间才能发布。

## 上载批量工作表和已更正错误文件的设置 {#bulksheet-upload-settings}

| 参数 | 描述 |
|----|----|
| [!UICONTROL File to Upload] | 要上传的文件。 通过输入完整路径和文件名或单击<b>[!UICONTROL Browse]</b>在设备或网络上查找文件来指定文件。<br><br>批量工作表文件最大可达2.5 GB（约250万行），并且必须具有下列文件扩展名之一： <i>[!UICONTROL .tsv]</i> （用于制表符分隔的值）、<i>[!UICONTROL .txt]</i> （用于符合Unicode的ASCII文本）、<i>[!UICONTROL .csv]</i> （用于逗号分隔的值）或<i>[!UICONTROL .zip]</i> （用于压缩的ZIP格式，它将解压缩为TSV文件）。 文件名不能包含以下字符： `# % &amp; * | \ : &quot; &lt; &gt; . ? /`<br><br><b>提示：</b>对于包含国际字符的数据，请使用TSV或TXT格式的文件。 |
| [!UICONTROL Single Account] | 文件适用于一个帐户： <i>[!UICONTROL Yes]</i>（适用于一个帐户）还是<i>[!UICONTROL No]</i>（适用于多个帐户）。 |
| [!UICONTROL Account (Search Engine)] | （当文件应用于单个帐户时）要将数据上传到的帐户。 |
| [!UICONTROL Search Engine] | （当文件应用于多个帐户时）要将数据上传到的广告网络。 |
| [!UICONTROL Scheduling] | 何时或是否将文件发布到指定的广告网络：<ul><li><i>[!UICONTROL Post to ad network now]</i> （默认）：立即开始发布数据。</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]：</i>开始在指定的日期和时间发布数据；默认为明天02:00 （凌晨2点）。 若要更改日期，请以DD/MM/YYYY或D/M/YYYY格式输入日期，或单击![日历](/help/search-social-commerce/assets/calendar.png "日历")以打开日历，然后[选择日期](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md)。 要更改时间，请以HH/MM或H/M格式输入时间，或从列表中选择时间（以15分钟为间隔）。</li><li><i>[!UICONTROL Preview only]：</i>若要将文件上传到Search、Social和Commerce而不将数据发布到广告网络，您以后仍可以发布该文件。 当批量处理工作表文件大于10 MB但小于2 GB时，该文件为ZIP格式；您无需解压缩文件即可发布该文件。</li></ul> |
| [!UICONTROL Generate Tracking URLs] | 是否在具有跟踪模板的帐户中包含跟踪模板和登陆页面后缀（适用于适用的广告网络），或者是否在具有目标URL的帐户中包含嵌入跟踪代码的目标URL，适用于发布中的所有关键词、广告、投放位置、站点链接和[!DNL Google Ads]产品组： <i>[!UICONTROL Yes]</i>（默认值）或<i>[!UICONTROL No]</i>。 不管组合中是否有竞价单位，都无所谓。<br><br>如果选择<i>[!UICONTROL Yes]</i>，则根据相关帐户设置或营销活动设置的[!UICONTROL Tracking Methods]部分中的参数生成URL。 默认情况下，如果跟踪URL存在，则除非需要新的URL，否则不会重新生成这些URL（例如，如果关键词匹配类型、广告文本或相关帐户的跟踪参数已更改）。<br><br>如果选择<i>[!UICONTROL No]</i>，则以后仍可通过手动发布上传的文件来生成跟踪URL。<br><br><b>注意：</b>如果广告商使用Adobe Advertising转化跟踪，且基本URL已更改，则必须生成新的跟踪URL，除非将该帐户配置为自动生成和上传跟踪URL。 |
| [!UICONTROL Enable budget changes on optimized campaigns] | 允许根据已发布的数据对优化项目组合中的促销活动进行预算更改。 默认情况下，不选中此选项。 如果选择此选项，则在优化功能确定应重新分配预算（通常在下一个竞价周期）之前，任何指定的营销活动预算更改均适用。<br><br><b>注意：</b>在发布文件时，因非优化项目组合中的促销活动发布数据而导致的任何预算更改都会发生。 更改显示在第二天的营销活动管理视图中。 |
| [!UICONTROL Enable bidding on ads within portfolios] | 当包含的促销活动组件位于优化的项目组合中时，此功能会覆盖优化策略，并允许基于批量处理工作表中的数据进行竞价更改，直到指定的结束日期为止。 如果选择此选项，请在&#x200B;**[!UICONTROL Hold bulksheet bids until]**&#x200B;字段中指定介于1-7天之间的结束日期。 |

>[!MORELIKETHIS]
>
>* [关于使用批量处理工作表管理营销活动数据](bulksheet-about.md)
>* [下载/创建批量处理工作表文件](bulksheet-download.md)
>* [发布批量工作表或已更正的错误文件](bulksheet-post.md)
>* [验证批量处理工作表文件中的登陆页面](bulksheet-validate-landing-pages.md)
>* [导出生成或上载的批量工作表文件](bulksheet-export.md)
