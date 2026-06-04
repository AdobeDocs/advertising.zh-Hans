---
title: （新UI）上传批量工作表或已更正的错误文件
description: 了解如何在新的Search、Social和Commerce UI中手动上传批量工作表文件或更正的登陆页验证错误文件。
feature: Search Bulksheets
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e58024d1-d6da-420c-80af-6be211808316
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 38fd7ff63b177f13bdfb19b980fb1d1e14edcf56
workflow-type: tm+mt
source-wordcount: 830
ht-degree: 0%

---

# （新UI）上传批量工作表或已更正的错误文件

您可以从设备或网络中为[支持的广告网络](about.md#bulksheet-functionality-by-network)上传批量工作表文件、已更正的登陆页验证错误文件以及其他已更正的错误文件。 上传文件时，会删除文件中的任何自定义列。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**。

1. 在工具栏中，单击&#x200B;**[!UICONTROL Bulk Operations]** \> **[!UICONTROL Upload Bulksheet]**。

1. 在[[!UICONTROL Upload Bulksheet]设置](#bulksheet-upload-settings)中输入或选择信息。

1. 单击&#x200B;**[!UICONTROL Upload]**。

当任务开始时，文件将列在[!UICONTROL Bulksheets]视图中。 如果在[!UICONTROL Notification Center] [&#128279;] (/help/search-social-commerce/new-ui/notifications/notification-manage.md)中启用了批量处理工作表的电子邮件通知，则会在作业完成时发送电子邮件通知，其中包含指向文件的链接。 根据编译的数据量，电子邮件通知可能需要几分钟或更长时间。 如果文件生成失败，则[!UICONTROL Bulksheets]视图中会列出一个错误文件，并会发送电子邮件通知，其中包含指向该错误文件的链接。

>[!NOTE]
>
>如果将批量处理工作表数据发布到广告网络，则可以跟踪[!UICONTROL Bulksheets]视图中[!UICONTROL Progress]列中的文件进度。 大量数据需要更长的时间才能发布。

## 上载批量工作表和已更正错误文件的设置 {#bulksheet-upload-settings}

| 参数 | 描述 |
|----|----|
| [!UICONTROL File to Upload] | 要上传的文件。 通过单击&#x200B;**[!UICONTROL Choose File]**&#x200B;在设备或网络上查找文件来指定文件。<br><br>批量工作表文件最大可达2.5 GB（约250万行），并且必须具有下列文件扩展名之一： *[!UICONTROL .tsv]* （用于制表符分隔的值）、*[!UICONTROL .txt]* （用于符合Unicode的ASCII文本）、*[!UICONTROL .csv]* （用于逗号分隔的值）或&#x200B;*[!UICONTROL .zip]* （用于压缩的ZIP格式，它将解压缩为TSV文件）。 文件名不能包含以下字符： `# % & * \| \ : " < > . ? /`<br><br>**提示：**&#x200B;对于包含国际字符的数据，请使用TSV或TXT格式的文件。 |
| [!UICONTROL Single Account] | 文件适用于一个帐户： *[!UICONTROL Yes]* （适用于一个帐户）还是&#x200B;*[!UICONTROL No]* （适用于多个帐户）。 |
| [!UICONTROL Account (Search Engine)] | （当文件应用于单个帐户时）要将数据上传到的帐户。 |
| [!UICONTROL Search Engine] | （当文件应用于多个帐户时）要将数据上传到的广告网络。<br><br>**注意：**&#x200B;多帐户批量处理工作表不支持对优化项目组合中的关键字进行竞价更改。 |
| [!UICONTROL Scheduling] | 何时或是否将文件发布到指定的广告网络：<ul><li>*[!UICONTROL Post to search engine now]* （默认）：立即开始发布数据。</li><li>*[!UICONTROL Post to search engine on \[specified date\] \[specified time\]]：*&#x200B;在指定的日期和时间开始发布数据；默认为明天02:00 （凌晨2点）。 要更改日期，请以DD/MM/YYYY格式输入日期，或单击日历图标以打开日历并选择日期。 要更改时间，请从列表中选择时间（以15分钟为间隔）。</li><li>*[!UICONTROL Preview only]：*&#x200B;将文件上传到Search、Social和Commerce，而不将数据发布到广告网络；稍后您仍然可以发布文件。 当批量处理工作表文件大于10 MB但小于2 GB时，该文件为ZIP格式；您无需解压缩文件即可发布该文件。</li></ul> |
| [!UICONTROL Generate Tracking URLs] | 是否在具有跟踪模板的帐户中包含跟踪模板和登陆页面后缀（适用于适用的广告网络），或者是否在具有目标URL的帐户中包含嵌入跟踪代码的目标URL，适用于发布中的所有关键词、广告、投放位置、站点链接和[!DNL Google Ads]产品组： *[!UICONTROL Yes]*（默认值）或&#x200B;*[!UICONTROL No]*。 不管组合中是否有竞价单位，都无所谓。<br><br>如果选择&#x200B;*[!UICONTROL Yes]*，则根据相关帐户设置或营销活动设置的[!UICONTROL Tracking Methods]部分中的参数生成URL。 默认情况下，如果存在跟踪URL，则除非需要新URL，否则不会重新生成这些URL。<br><br>如果选择&#x200B;*[!UICONTROL No]*，则以后仍可以通过手动发布上传的文件来生成跟踪URL。<br><br>**注意：**&#x200B;如果广告商使用Adobe Advertising转化跟踪，且基本URL已更改，则必须生成新的跟踪URL，除非将帐户配置为自动生成和上传跟踪URL。 |
| [!UICONTROL Replace Media Optimizer Tracking] | （在[!UICONTROL Generate Tracking URLs]为&#x200B;*[!UICONTROL Yes]*&#x200B;时可用）将上传文件URL中的任何现有Adobe Advertising跟踪替换为新生成的跟踪。 |
| [!UICONTROL Enable budget changes on optimized campaigns] | 允许根据已发布的数据对优化项目组合中的促销活动进行预算更改。 默认情况下，不选中此选项。 如果选择此选项，则在优化功能确定应重新分配预算（通常在下一个竞价周期）之前，任何指定的营销活动预算更改均适用。<br><br>**注意：**&#x200B;在过帐文件时，因非优化项目组合中营销活动的已过帐数据而产生的所有预算更改均会发生。 更改显示在第二天的营销活动管理视图中。 |
| [!UICONTROL Enable bidding on ads within portfolios] | 当包含的促销活动组件位于优化的项目组合中时，此功能会覆盖优化策略，并允许基于批量处理工作表中的数据进行竞价更改，直到指定的结束日期为止。 如果选择此选项，则在&#x200B;**[!UICONTROL Hold bulksheet bids until]**&#x200B;字段中指定介于1-7天之间的结束日期。 |

>[!MORELIKETHIS]
>
>* [（新UI）关于使用批量处理工作表管理营销活动数据](about.md)
>* [（新UI）下载/创建批量处理工作表文件](download.md)
>* [（新UI）发布批量工作表或已更正的错误文件](post.md)
>* [（新UI）验证批量处理工作表文件中的登陆页面](validate-landing-pages.md)
