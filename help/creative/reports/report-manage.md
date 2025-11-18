---
title: 管理自定义报表
description: 了解如何生成和管理跨体验[!UICONTROL Custom Creative Report]。
feature: Creative Reporting
source-git-commit: 41b8d295436bdbe6cea402e5bb234caa7a36f4df
workflow-type: tm+mt
source-wordcount: '1477'
ht-degree: 0%

---

# [!UICONTROL Manage custom reports]

您可以创建、复制、编辑、运行、下载和删除自定义报表。

## 创建自定义报表 {#report-create}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**。

1. 单击右上角的&#x200B;**[!UICONTROL Create]**。

1. 指定[报表设置](#report-settings)。

1. 单击&#x200B;**[!UICONTROL Create Custom Report]**。

## 复制自定义报表

复制自定义报告以使用类似设置创建新报告。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**。

1. 在报表名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Copy]**。

1. （可选）根据需要编辑[报告设置](#report-settings.md)。

   默认情况下，报表名称为“\&lt;*现有报表名称*\> \#2”（或序列中的下一个编号）。

## 编辑自定义报告 {#report-edit}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**。

1. 在报表名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit]**。

1. 编辑[报告设置](#report-settings.md)。

1. 单击&#x200B;**[!UICONTROL Edit Custom Report]**。

## 运行自定义报表 {#report-run-now}

您可以运行任何未过期且当前未运行的报表。

>[!NOTE]
>
>您还可以在您[创建](#report-create)或[编辑](#report-edit)自定义报表时运行该报表。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**。

1. 在报表名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Run Now]**。

   报表完成后，将会发送到报表设置中指定的目标。

## 下载自定义报表

您可以下载过去四个月内任何已完成的报表实例，其状态为“[!UICONTROL Ready to Download]”或“[!UICONTROL Completed]”。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**。

1. 在报表行的[!UICONTROL Download Report]列中，执行以下操作：

   * 要下载报告的最新实例，请单击&#x200B;**[!UICONTROL Download]**。

   * （具有多个实例的报告）单击![旁边的](/help/dsp/assets/chevron-down.png "向下箭头")向下箭头[!UICONTROL Download]，然后单击要下载的报告的完成日期。 可下载的报表实例以下载图标(![下载图标](/help/dsp/assets/indicator-downloadable.png "下载图标"))表示。

     当有多个实例可用时，如有必要，请单击列表底部的&#x200B;**[!UICONTROL Load More]**。

     当报表在同一天运行多次时，该天的报表实例将按时间顺序列出，最近的实例位于顶部。

     失败的报表作业以错误图标（![错误指示器](/help/dsp/assets/indicator-critical.png "错误指示器")）指示，无法下载。 将光标悬停在错误图标上可查看错误说明。

## 删除自定义报表

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**。

1. 在报表名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Delete]**。

## 报表设置 {#report-settings}

**[!UICONTROL Name]：**&#x200B;报告名称。 最大长度为180个字符。

**[!UICONTROL Report Type]：**&#x200B;报告的类型。

### [!UICONTROL Report Range]节

此部分确定报表中包含的数据。 要设置报表计划的日期，请参阅“[!UICONTROL Report run schedule]”部分。

**[!UICONTROL Timezone]：**&#x200B;报告的时区。

**[!UICONTROL Observe Daylight Savings Time]：**&#x200B;考虑报告时间的夏令时。

**范围：**&#x200B;要生成数据的日期范围。 可用天数因报表和所选维度而异。 选择一项：

* **[!UICONTROL Previous Calendar Week]：**&#x200B;包含上一个日历周的数据。

* **[!UICONTROL Previous Calendar Month]：**&#x200B;包含上一个日历月的数据。

* **[!UICONTROL Custom Range]：**&#x200B;包含特定开始日期和结束日期之间的数据。 要报告前一天的数据，请选择&#x200B;**[!UICONTROL Present]**。

### [!UICONTROL Report Run schedule]节

此部分确定运行报告的日期。 要设置包含报表数据的日期，请参阅“[!UICONTROL Report range]”部分。

**\[计划\]：**&#x200B;何时生成报告：

* *[!UICONTROL Immediately]*：立即将报表添加到报表队列。

  >[!NOTE]
  >
  >您还可以随时[从](#report-run-now)视图中[!UICONTROL Reports]运行自定义报表。

* *[!UICONTROL On]\&lt;Date\>：*&#x200B;在指定的日期运行报告，完成日期为帐户时区中的09:00。

* *[!UICONTROL Recurring]：*&#x200B;在指定的时间段内根据计划运行报告。

   * **\[计划\]：**&#x200B;运行报告的频率：

      * *每日*&#x200B;运行报告，每N天运行一次。 例如，要每两周（14天）运行一次报表，请选择此选项并输入&#x200B;**14**。

      * *每周*，在每周的指定日期运行报告。 例如，要每周一和周五运行一次报表，请选择此选项，然后选中&#x200B;**周一**&#x200B;和&#x200B;**周五**&#x200B;旁边的复选框。

      * *每月*&#x200B;运行该月特定数字日（从1到30）的报表。 例如，在每月的第一天运行报告，选择此选项并输入&#x200B;**1**。

   * **从**：报表可以运行的第一个日期。 根据指定的计划，第一个报表实例可能会出现在此日期之后。

   * **截止日期**：报告到期日期，最长可为4个日历月之后。 在报告过期之前，所有指定的电子邮件目标都会在过期日期的前七天零一天收到电子邮件警报。 若要保留较长的报表，请更改此日期。

### [!UICONTROL Apply Filters]节

**[!UICONTROL Filter by]：**（可选）用于筛选数据的其他维度，无论这些维度是否作为列包含在报表中。 可用过滤器因报告类型而异，可能包括： *[!UICONTROL Advertiser]*、*[!UICONTROL Experience]*、*[!UICONTROL Creative Library]*&#x200B;和&#x200B;*[!UICONTROL DSP]*<!-- Clarify what this is for, Advertising DSP or whatever DSP the ads were run from? -->。

要应用一个或多个筛选器，请执行以下操作：

* 选择一个维度，选择运算符（*等于*&#x200B;或&#x200B;*不等于*），然后选择适用的值。 例如，要仅返回前置广告的数据，请指定“[!UICONTROL Ad Type equals Preroll]”。
* （可选）向过滤器添加其他标准。
* （可选）添加其他过滤器，每个过滤器具有一个或多个标准。

### [!UICONTROL Build Your Report]节

**[!UICONTROL Select To Add As Report Headers]：**&#x200B;要包含在报告中的数据列或标头。 要添加列，请展开类别并选中列名旁边的复选框。 可用列因报告而异，并且所有不可用的量度都已禁用。<!-- Add back once I have this completed, and reconsider wording of link/anchor:  See "[Available Report Columns](#report-custom-creative-columns)" for descriptions of all options. -->

**[!UICONTROL Drag to Re-Order Report Headers Below]：**&#x200B;列标题的顺序。 您可以拖放任何列以自定义顺序。

**[!UICONTROL Format]：**&#x200B;是以&#x200B;*[!UICONTROL CSV]* （逗号分隔值）还是&#x200B;*[!UICONTROL Tab]* （制表符分隔值）格式生成报告。

**[!UICONTROL Headers]：**&#x200B;是&#x200B;*[!UICONTROL Include]*&#x200B;还是&#x200B;*[!UICONTROL Do Not Include]*&#x200B;列标题。

### [!UICONTROL Multi-Touch Conversion Options]节

**[!UICONTROL Attribution Rule Settings]：**&#x200B;设置因报告类型而异：

* **\[规则类型\]：** (仅具有Adobe Advertising转化跟踪的广告商)在报表中，如何在一系列导致转化的事件中归因转化数据。 如果要比较规则之间的差异，可以选择多个规则。

  >[!NOTE]
  >
  >转化路径包括在[!DNL Advertising Search, Social, & Commerce]中配置的广告商展示或点击回顾窗口内的任何展示和点击。 在转化归因期间，点击次数优先于展示次数。 根据归因规则，转化路径中的任何点击都将获得完全点数。 仅当转化路径中未跟踪任何点击时，展示次数才会获得点数。

   * *[!UICONTROL Last Event]：*&#x200B;将转化归因于转化路径中的最后一次点击或展示。

   * *[!UICONTROL Weight Last More]：*&#x200B;将转化归因于转化路径中的所有事件，但给予最后一个事件的权重最大，而给予上一个事件的权重依次降低。

   * *[!UICONTROL Even Distribution]：*&#x200B;将转化平均归因于转化路径中的每个事件。

   * *[!UICONTROL Weight First More]：*&#x200B;将转化归因于转化路径中的所有事件，但给予第一个事件的权重最大，给予以下事件的权重依次降低。

   * *[!UICONTROL First Event]：*&#x200B;将转化归因于转化路径中的第一次点击或展示。

   * *[!UICONTROL U-shaped]：*&#x200B;将转化归因于转化路径中的所有事件，但是将最大权重赋予第一个和最后一个事件，将连续降低权重赋予转化路径中间的事件。

   * *[!UICONTROL Display Only]：*&#x200B;将转化归因于转化路径中的上次DSP点击或展示。 这包括视频和连接的电视广告，并排除[!DNL Advertising Search, Social, & Commerce]广告的点击次数。

   * *[!UICONTROL Social Only]：*&#x200B;已过时

另请参阅&quot;[如何为Adobe Advertising](/help/search-social-commerce/reports/attribution-rules.md)计算归因规则。&quot;

**[!UICONTROL Paths as Columns]：**&#x200B;当同一设备上发生先前事件时要报告的转化类型。 您最多可以包含三种类型。 对于每个选定的类型，每个转化量度都包含一个单独的列，该列将附加指定的后缀（[!UICONTROL (tl)]、[!UICONTROL (ct)]或[!UICONTROL (vt)]）：

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]：*&#x200B;包含归因于点击（点进为CT）和展示次数（显示到达为VT）的转化。 归因于展示的转化次数乘以指定的显示到达权重。 默认显示到达权重为100%，这意味着由展示产生的转化将被计算为由点击产生的转化值的100%。

* *[!UICONTROL With Clicks (CT)]：*&#x200B;仅包含归因于点击的转化。

* *[!UICONTROL Impressions Only (VT)]：*&#x200B;仅包含归因于展示的转化，因为转化路径中未跟踪任何点击。

### [!UICONTROL Add Report Destinations]节

**[!UICONTROL Destination Type]：**&#x200B;完成报告和错误通知的传送位置。 保存报表后，就无法更改目标类型。

>[!NOTE]
>
>您始终可以从[!UICONTROL Reports] > [!UICONTROL Custom Reports]视图下载已完成的报表。

* *[!UICONTROL None]：*&#x200B;不提交任何报告或通知。

* *[!UICONTROL S3]：*&#x200B;若要将已完成的报告发送到一个或多个[!DNL Amazon Simple Storage Service] ([!DNL Amazon S3])位置，您必须在&#x200B;**[!UICONTROL Destination Name]**&#x200B;字段中选择该位置。

* *[!UICONTROL sFTP]：*&#x200B;若要将已完成的报告发送到一个或多个SFTP位置，您必须在&#x200B;**[!UICONTROL Destination Name]**&#x200B;字段中选择这些位置。

* *[!UICONTROL FTP]：*&#x200B;若要将已完成的报告发送到一个或多个FTP位置，您必须在&#x200B;**[!UICONTROL Destination Name]**&#x200B;字段中选择这些位置。

* *[!UICONTROL FTP SSL](当前在Beta中)：*&#x200B;要将已完成的报告发送到一个或多个FTP SSL位置，您必须在&#x200B;**[!UICONTROL Destination Name]**&#x200B;字段中选择该位置。

* *[!UICONTROL Email]：*&#x200B;若要指定电子邮件地址，在报告因错误而被取消时，将已完成的报告或通知发送到这些地址。

**[!UICONTROL Email]：** （仅限电子邮件目标类型）对于每个地址，请输入地址并单击&#x200B;**+**。

**[!UICONTROL Destination Name]：** （仅限S3、FTP、sFTP和FTP SSL目标类型）将自定义报告发送到的[报告目标](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}的名称。

* 要指定现有目标，请从列表中选择目标名称。 您可以分别选择多个目标名称。

* 要创建新目标，请执行以下操作：

   1. 单击&#x200B;**添加新目标**。

   1. 输入[报表目标设置](/help/dsp/reports/report-destinations/report-destination-settings.md){target="_blank"}，然后单击&#x200B;**保存**。

   1. 返回报表设置，单击&#x200B;**刷新目标名称。**

      现在，可以从现有目标的列表中找到新目标，并且您可以选择将其添加到报表中。


<!-- This needs a lot of updating for new report:

## Available Report Columns {#report-custom-creative-columns}

|Metric Type|Subtype|Column Name|Description|
|-----------|-------|-----------|-----------|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Ad Size]|The dimensions of the published ad.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Is Default]|Whether the served ad was a default image ad or video ad for the experience.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Rotation Type]| Whether ads were rotated algorithmically (*Algorithmic*), in a specified sequence (*Sequenced*), or according to relative weights (*Weighted*).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative ID]| The ID that [!UICONTROL Creative] assigned to the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Name]| The name of the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Type]| The type of creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative ID]| The ID that [!UICONTROL Creative] assigned to the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Name]| The name of the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Type]| The type of parent creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Ad Link]| The landing page URL.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Click Type]| The specific type of user interaction.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Direction]| The directional flow or navigation path of the user's click interaction within the creative experience. |
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 1]| The value of Attribute 1 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 2]| The value of Attribute 2 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 3]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 4]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 5]| The value of Attribute 5 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Browser]|The browser in which the ad was shown (such as [!UICONTROL Chrome] or [!UICONTROL Firefox]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device OS]|The operating system on which the ad was shown (such as [!UICONTROL Windows]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Type]|The type of device on which the ad was shown (such as [!UICONTROL Desktop]).|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Name]| The name of the DSP on which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement ID]| The ID of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement Name]| The name of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site ID]| The ID of the site on which ads were run.|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site Name]| The name of the site on which ads were run. |
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Ad Tag Id]|The ID that [!UICONTROL Creative] assigned to the ad experience tag.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Advertiser Name]| The name of the advertiser.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Date/Time]|The date and time of the event.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience ID]| The ID that [!UICONTROL Creative] assigned to the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience Name]| The name of the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Targeting Branch Value]| The specific path through the targeting decision tree that determined which creative experience variant was served to the user.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Trafficking Line]| The name of the ad tag. |
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL City]|The city to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Country Code]|The country code for the country to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL DMA]|The Designated Market Area (DMA) to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL State Code]|The state code for the state to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Zip Code]|The zip code to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category ID]|(Dynamic ads) The target product category ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category Name]|(Dynamic ads) The target product category name.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 1]|(Dynamic ads) The first creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 2]|(Dynamic ads) The second creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 3]|(Dynamic ads) The third creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 4]|(Dynamic ads) The fourth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 5]|(Dynamic ads) The fifth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product ID]|(Dynamic ads) The target product ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product Name]|(Dynamic ads) The target product name.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Matched Audience Segment ID]|The IDs for up to five user segments that matched the ad theme.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment ID]|The ID for a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment Name]|The name of a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Segment Values]|The attributes for an audience segment to which the reported data is attributed.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Clicks]|The sum of all clicks on an ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL CTR]|The click-through rate, which is the percentage of clicks divided by ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagement Rate]|The percentage of impressions served that resulted in user engagements.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagements]|The number of interactions on a served ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Impressions]|The total number of ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Media Match Rate]| The percentage of impressions with a retargeted cookie. |
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Clicks]|(Dynamic ads only) The sum of all clicks on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion]|(Dynamic ads only) The sum of all conversions on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion Rate]|(Dynamic ads only) The percentage of ads for a product that resulted in conversions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product CTR]|(Dynamic ads only) The click-through rate for ads for a product, which is the percentage of clicks divided by ad impressions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Impressions]|(Dynamic ads only) The total number of impressions for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Revenue]|(Dynamic ads only) The total revenue on served ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Revenue]|The total revenue on served ads.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completion Rate]|The percentage of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completion Rate]|The percentage of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completion Rate]|The percentage of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completion Rate]|The percentage of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completions]|The number of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completions]|The number of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completions]|The number of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completions]|The number of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Avg Percent Viewed]|The average percentage an ad was watched to completion, accounting for all views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Play Rate]|The percentage of impressions served that resulted in video views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Playtime per View]|The average duration of a video view, measured in seconds.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Viewed Minutes]|The total number of minutes a video ad was viewed.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Views]|The total number of video ad views.




|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 100% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 50% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewability Rate (%)]|The percentage of viewable impressions out of all measurable impressions, calculated as <code>[!UICONTROL Viewable Impressions] / [!UICONTROL Measurable Impressions]</code>.|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewable Impressions]|The number of ad impressions considered viewable.|
|[!UICONTROL Conversion Metrics]|[Grouped by advertiser in report settings]|[Advertiser-specific conversion]| The total for a specified advertiser-specific conversion metric or Adobe Analytics event.|
|[!UICONTROL Custom Goals]|[Grouped by advertiser in report settings]|[Advertiser-specific custom goal]|(Advertisers with Advertising DSP) The weighted sum of all conversions that are included in the specified [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).|

{style="table-layout:auto"}

-->

>[!MORELIKETHIS]
>
>* [体验级性能报告](/help/creative/experiences/experience-performance-details.md)
>* [关于DSP自定义报告](/help/dsp/reports/report-about.md){target="_blank"}
>* [关于[!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
