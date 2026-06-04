---
title: （新UI）发布批量工作表或已更正的错误文件
description: 了解如何在新的Search、Social和Commerce UI中将批量工作表文件发布到广告网络。
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
source-git-commit: 739034010787c2016720bef37fb75dc8efbae58b
workflow-type: tm+mt
source-wordcount: 752
ht-degree: 0%

---

# （新UI）发布批量工作表或已更正的错误文件

您可以将现有的批量工作表文件或更正的错误文件发布到[支持的广告网络](about.md#bulksheet-functionality-by-network)的相关帐户。 如果文件为ZIP格式，则无需先解压缩。

批量工作表文件和错误文件在上传或生成后30天会自动删除。

>[!NOTE]
>
>您还可以在上传文件时发布批量工作表文件或错误文件。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**。

1. 选中每个要发布的文件旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Post]**。

1. 在[[!UICONTROL Post Bulksheet]设置](#bulksheet-post-settings)中输入或选择信息，然后单击&#x200B;**[!UICONTROL Post]**。

   相同的设置适用于您发布的所有文件。

任务开始时，[!UICONTROL Bulksheets]视图中行的状态和计划发布日期将更新。 如果在[!UICONTROL Notification Center] [&#128279;] (/help/search-social-commerce/new-ui/notifications/notification-manage.md)中启用了批量处理工作表的电子邮件通知，则在发布文件时会发送一封电子邮件通知，其中包含指向文件的链接。 根据编译的数据量，电子邮件通知可能需要几分钟或更长时间。 如果有任何数据无法发布，则错误文件将列在[!UICONTROL Bulksheets]视图中，并且会发送电子邮件通知，其中包含指向错误文件的链接。

>[!NOTE]
>
>* 大量数据需要更长的时间才能发布。 您可以在[!UICONTROL Bulksheets]视图的[!UICONTROL Progress]列中跟踪文件的进度。
>* 所有发布的数据都受制于网络的编辑流程。
>* 在发布批量工作表文件之前，您可以取消发布。

## 批量工作表和已更正错误文件的发布设置 {#bulksheet-post-settings}

| 参数 | 描述 |
|----|----|
| [!UICONTROL Account (Search Engine)] | 为其发布数据的广告网络帐户。 如果同时发布多个文件或一个应用到多个帐户的文件，则值为&#x200B;*已选择多个帐户*。<br><br>广告网络名称的第一个字母在帐户名称后面用括号括起来(如[!DNL Google Ads]帐户的“Acme Realty (G)”)。 |
| [!UICONTROL Scheduling] | 何时将文件发布到指定的广告网络：<ul><li>*[!UICONTROL Post to ad network now]* （默认）：立即开始发布数据。</li><li>*[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]：*&#x200B;在指定的日期和时间开始发布数据；默认为明天02:00 （凌晨2点）。 要更改日期，请以DD/MM/YYYY格式输入日期，或单击日历图标以打开日历并选择日期。 要更改时间，请从列表中选择时间（以15分钟为间隔）。</li></ul> |
| [!UICONTROL Generate Tracking URLs] | 是否在具有跟踪模板的帐户中包含跟踪模板和登陆页面后缀（适用于适用的广告网络），或者是否在具有目标URL的帐户中包含嵌入跟踪代码的目标URL，适用于发布中的所有关键词、广告、投放位置、站点链接和[!DNL Google Ads]产品组： *[!UICONTROL Yes]*（默认值）或&#x200B;*[!UICONTROL No]*。 不管组合中是否有竞价单位，都无所谓。<br><br>如果选择&#x200B;*[!UICONTROL Yes]*，则根据相关帐户设置或营销活动设置的[!UICONTROL Tracking Methods]部分中的参数生成URL。 默认情况下，如果存在跟踪URL，则除非需要新URL，否则不会重新生成这些URL。<br><br>如果选择&#x200B;*[!UICONTROL No]*，则以后仍可以通过手动发布上传的文件来生成跟踪URL。<br><br>**注意：**&#x200B;如果广告商使用Adobe Advertising转化跟踪，且基本URL已更改，则必须生成新的跟踪URL，除非将帐户配置为自动生成和上传跟踪URL。 |
| [!UICONTROL Replace Media Optimizer Tracking] | （在[!UICONTROL Generate Tracking URLs]为&#x200B;*[!UICONTROL Yes]*&#x200B;时可用）将上传文件URL中的任何现有Adobe Advertising跟踪替换为新生成的跟踪。 |
| [!UICONTROL Enable budget changes on optimized campaigns] | 允许根据已发布的数据对优化项目组合中的促销活动进行预算更改。 默认情况下，不选中此选项。 如果选择此选项，则在优化功能确定应重新分配预算（通常在下一个竞价周期）之前，任何指定的营销活动预算更改均适用。<br><br>**注意：**&#x200B;在过帐文件时，因非优化项目组合中营销活动的已过帐数据而产生的所有预算更改均会发生。 更改显示在第二天的营销活动管理视图中。 |
| [!UICONTROL Enable bidding on ads within portfolios] | 当包含的促销活动组件位于优化的项目组合中时，此功能会覆盖优化策略，并允许基于批量处理工作表中的数据进行竞价更改，直到指定的结束日期为止。 如果选择此选项，请在&#x200B;**[!UICONTROL Hold bulksheet bids until]**&#x200B;字段中指定介于1-7天之间的结束日期。 |

>[!MORELIKETHIS]
>
>* [（新UI）关于使用批量处理工作表管理营销活动数据](about.md)
>* [（新UI）下载/创建批量处理工作表文件](download.md)
>* [（新UI）上载批量工作表或已更正的错误文件](upload.md)
>* [（新UI）验证批量处理工作表文件中的登陆页面](validate-landing-pages.md)
>* [（新UI）删除上传的批量工作表和错误文件](delete.md)
