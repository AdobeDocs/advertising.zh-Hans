---
title: '[!UICONTROL Custom Creative Report]'
description: 了解如何生成跨体验[!UICONTROL Custom Creative Report]。
feature: Creative Reporting
exl-id: 13687d9d-6283-40ac-86a2-bb88b9fdfcc3
source-git-commit: bf969c1b3cc57e2ef83087952a9bac530b276916
workflow-type: tm+mt
source-wordcount: '2021'
ht-degree: 0%

---

# [!UICONTROL Custom Creative Report]

*Beta功能*

[!UICONTROL Custom Creative Report]允许您自定义所有广告体验的内容和报表数据的交付。

您可以生成报告一次，也可以根据指定条件（例如每15天或每月第一天），在指定时区的03:00计划每日、每周或每月生成报告。 生成报告后，您可以从[!UICONTROL Reports] > [!UICONTROL Custom Reports]或链接的[报告目标](/help/dsp/reports/report-destinations/report-destination-about.md)以下类型下载报告：

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* FTP SSL <!-- (in beta) -->
* SFTP

## 创建[!UICONTROL Custom Creative Report]

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**。

1. 单击右上角的&#x200B;**[!UICONTROL Create]**。

1. 指定[报表设置](#report-settings)。

1. 单击&#x200B;**[!UICONTROL Create Custom Report]**。

## 报表设置 {#report-settings}

**[!UICONTROL Name]：**&#x200B;报告名称。 最大长度为180个字符。

**[!UICONTROL Report Type]：**&#x200B;报告类型： *[!UICONTROL Custom Creative Beta]*。

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
  >您还可以随时[从](/help/dsp/reports/report-run-now.md)视图中[!UICONTROL Reports]运行自定义报表。

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

**[!UICONTROL Select To Add As Report Headers]：**&#x200B;要包含在报告中的数据列或标头。 要添加列，请展开类别并选中列名旁边的复选框。 可用列因报告而异，并且所有不可用量度都已禁用。 有关所有选项的说明，请参阅[可用报表列](#report-custom-creative-columns)。

**[!UICONTROL Drag to Re-Order Report Headers Below]：**&#x200B;列标题的顺序。 您可以拖放任何列以自定义顺序。

**[!UICONTROL Format]：**&#x200B;是以&#x200B;*[!UICONTROL CSV]* （逗号分隔值）还是&#x200B;*[!UICONTROL Tab]* （制表符分隔值）格式生成报告。

**[!UICONTROL Headers]：**&#x200B;是&#x200B;*[!UICONTROL Include]*&#x200B;还是&#x200B;*[!UICONTROL Do Not Include]*&#x200B;列标题。

### [!UICONTROL Multi-Touch Conversion Options]节

**[!UICONTROL Attribution Rule Settings]：**&#x200B;设置因报告类型而异：

* **\[归因类型\]：** (仅具有Adobe Advertising转化跟踪的广告商)在报表中，如何在一系列导致转化的事件中归因转化数据：

   * *[!UICONTROL Unique]：* （默认值）计算维度值（如设备或投放位置）在转化路径上的次数。

   * *[!UICONTROL Multi-Touch Attribution (MTA)]：*&#x200B;根据维度值（如设备或投放位置）在转化路径上的出现频率分配每次转化的点数。 例如，如果在转化前总共有10次展示，其中8次在CTV上，2次在移动设备上，则80%的点数(0.8)将授予CTV屏幕，0.2次授予Mobile。

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

## 可用报表列 {#report-custom-creative-columns}

| 量度类型 | 子类型 | 列名称 | 描述 |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Size] | 已发布广告的维度。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Is Default] | 投放的广告是体验的默认图像广告还是视频广告。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Rotation Type] | 广告是根据相对权重（*加权*）还是算法（*算法*）旋转。 |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative ID] | [!UICONTROL Creative]分配给创意的ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Name] | 创意内容的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Type] | 创意的类型（如[!UICONTROL HTML5]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative ID] | [!UICONTROL Creative]分配给父创意内容的ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Name] | 父级创意内容的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Type] | 父级创意内容的类型（如[!UICONTROL HTML5]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Ad Link] | 登陆页面URL。 |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Click Type] | 用户交互的特定类型。 |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Direction] | 创意体验中用户点击交互的定向流或导航路径。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Browser] | 显示广告的浏览器（如[!UICONTROL Chrome]或[!UICONTROL Firefox]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device OS] | 显示广告的操作系统（如[!UICONTROL Windows]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Type] | 显示广告的设备类型（如[!UICONTROL Desktop]）。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Name] | 运行广告的DSP的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement ID] | 运行广告的投放位置的ID。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement Name] | 运行广告的投放位置的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site ID] | 运行广告的网站的ID。 |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site Name] | 运行广告的网站的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Ad Tag Id] | [!UICONTROL Creative]分配给广告体验标记的ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Advertiser Name] | 广告商的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Date/Time] | 事件的日期和时间。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience ID] | [!UICONTROL Creative]分配给体验的ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience Name] | 体验的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Targeting Branch Value] | 通过定位决策树的特定路径，用于确定向用户提供哪个创意体验变体。 |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Trafficking Line] | 广告标记的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL City] | 报告的数据所属的城市。 |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Country Code] | 报告数据归属于的国家/地区的国家/地区代码。 |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL DMA] | 报告数据所属的指定市场区域(DMA)。 |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL State Code] | 报告数据归因的省/自治区/直辖市的省/自治区/直辖市代码。 |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Zip Code] | 报告数据归因的邮政编码。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category ID] | （动态广告）目标产品类别ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category Name] | （动态广告）目标产品类别名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 1] | （动态广告）第一个创意属性。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 2] | （动态广告）第二个创意属性。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 3] | （动态广告）第三个创意属性。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 4] | （动态广告）第四个创意属性。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 5] | （动态广告）第五个创意属性。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product ID] | （动态广告）目标产品ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product Name] | （动态广告）目标产品名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Matched Audience Segment ID] | 最多五个与广告主题匹配的用户区段的ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment ID] | 报告数据所属的重定向像素的ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment Name] | 报告数据归因的重定向像素的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Values] | 已报告数据归因的受众区段的属性。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks] | 广告所有点击次数总和。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL CTR] | 点进率，即点击次数百分比除以广告展示次数。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagement Rate] | 提供并导致用户参与的展示次数百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | 投放广告的交互次数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | 广告展示总数。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Media Match Rate] | 展示次数与重新定位的Cookie的百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Clicks] | （仅限动态广告）产品广告的所有点击总和。 当产品为null时，该值为零(0)。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion] | （仅限动态广告）产品的广告上所有转化次数的总和。 当产品为null时，该值为零(0)。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion Rate] | （仅限动态广告）某个产品中导致转化的广告百分比。 当产品为null时，该值为零(0)。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product CTR] | （仅限动态广告）产品广告的点进率，即点击次数百分比除以广告展示次数。 当产品为null时，该值为零(0)。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Impressions] | （仅限动态广告）产品的展示总数。 当产品为null时，该值为零(0)。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Revenue] | （仅限动态广告）为产品提供的广告的总收入。 当产品为null时，该值为零(0)。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Revenue] | 投放广告的总收入。 |
| [!UICONTROL Conversion Metrics] | [在报告设置中按广告商分组] | [广告商特定转化] | 指定的特定于广告商的转化量度或Adobe Analytics事件的总数。 |
| [!UICONTROL Custom Goals] | [在报告设置中按广告商分组] | [特定于广告商的自定义目标] | (具有Advertising DSP的广告商)指定[Advertising DSP自定义目标](/help/dsp/optimization/custom-goal.md)中包含的所有转化的加权总和。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [体验级性能报告](/help/creative/experiences/experience-performance-details.md)
>* [关于DSP自定义报告](/help/dsp/reports/report-about.md){target="_blank"}
>* [关于[!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
