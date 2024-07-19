---
title: 自定义报表设置
description: 请参阅自定义报表设置的描述。
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1261'
ht-degree: 0%

---

# 自定义报表设置

**[!UICONTROL Name]**&#x200B;报告名称。 最大长度为180个字符。

**[!UICONTROL Report Type]**&#x200B;报告的类型： *[!UICONTROL Custom]* （包括大多数可用选项）、*[!UICONTROL Billing]*、*[!UICONTROL Conversion]*、*[!UICONTROL Device]*、*[!UICONTROL Frequency (by Impression)]*、*[!UICONTROL Frequency (by App/Site)]*、*[!UICONTROL Geo]*、*[!UICONTROL Margin]*、*[!UICONTROL Media Performance]*、*[!UICONTROL Segment]*、*[!UICONTROL Site]*、*[!UICONTROL Household Reach & Frequency]*&#x200B;或&#x200B;*[!UICONTROL Household Conversions]*。

## [!UICONTROL Apply Filters]节

**[!UICONTROL Timezone]：**&#x200B;报告的时区。

**[!UICONTROL Observe Daylight Savings Time]：**&#x200B;考虑报告时间的夏令时。

**\[日期范围\]：**&#x200B;要生成数据的日期范围。 可用天数因报表和所选维度而异。 选择一项：

* **[!UICONTROL Previous N days]：**&#x200B;包含今天之前特定天数的数据。

* **[!UICONTROL Custom]：**&#x200B;包含特定开始日期和结束日期之间的数据。 要报告前一天的数据，请选择&#x200B;**[!UICONTROL Present]**。

* **[!UICONTROL Last Calendar Month]：**&#x200B;包含上一个日历月的数据。

**[!UICONTROL Add Filters]：**（可选）用于筛选数据的其他维度，无论这些维度是否作为列包含在报表中。 可用过滤器因报告类型而异，可能包括：*[!UICONTROL Account]*\*、*[!UICONTROL Ad Type]*、*[!UICONTROL Ads]*、*[!UICONTROL Advertiser]*、*[!UICONTROL Campaign]*、*[!UICONTROL Country]*、* *[!UICONTROL Package]*、*[!UICONTROL Placement]*、*[!UICONTROL Video]*&#x200B;和&#x200B;*[!UICONTROL Video Duration]*。

\* *[!UICONTROL Account]*&#x200B;仅在您的组织配置了[跨帐户报告](report-about.md#cross-account-reporting)时才可用于以下报告类型： [!UICONTROL Custom]、[!UICONTROL Site]、[!UICONTROL Segment]、[!UICONTROL Geo]、[!UICONTROL Device]、[!UICONTROL Frequency (by Impression)]和[!UICONTROL Conversion]。 请联系您的Adobe客户团队，以获取有关跨帐户报表的更多信息。

要应用一个或多个筛选器，请执行以下操作：

* 选择一个维度，选择运算符（*等于*&#x200B;或&#x200B;*不等于*），然后选择适用的值。 例如，要仅返回前置广告的数据，请指定“[!UICONTROL Ad Type equals Preroll]”。
* （可选）向过滤器添加其他标准。
* （可选）添加其他过滤器，每个过滤器具有一个或多个标准。

## [!UICONTROL Build Your Report]节

**[!UICONTROL Select To Add As Report Headers]：**&#x200B;要包含在报告中的数据列或标头。 要添加列，请展开类别并选中列名旁边的复选框。 可用列因报告而异，并且所有不可用量度都已禁用。 可用的数据类别包括：

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > [!UICONTROL Household Reach & Frequency]报表只能包含一个维度。

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >[!UICONTROL Household Reach & Frequency]报表可以包含重叠量度或非重叠量度，但不能同时包含这两个量度。

* [!UICONTROL Conversion Metrics] （按广告商排序）

* [!UICONTROL Custom Goals] （按广告商排序）

有关所有选项的说明，请参阅[可用报表列](report-columns.md)。

**[!UICONTROL Drag to Re-Order Report Headers Below]：**&#x200B;列标题的顺序。 您可以拖放任何列以自定义顺序。

**[!UICONTROL Format]：**&#x200B;是以&#x200B;*[!UICONTROL CSV]* （逗号分隔值）还是&#x200B;*[!UICONTROL Tab]* （制表符分隔值）格式生成报告。

**[!UICONTROL Headers]：**&#x200B;是&#x200B;*[!UICONTROL Include]*&#x200B;还是&#x200B;*[!UICONTROL Do Not Include]*&#x200B;列标题。

## [!UICONTROL Multi-Touch Conversion Options]节

**[!UICONTROL Attribution Rule Settings]：**&#x200B;设置因报告类型而异：

* **\[归因类型\]：** ([!UICONTROL Household Conversion]个包含[!UICONTROL Conversion Metrics]或[!UICONTROL Custom Goals]列的报告；仅包含Adobe Advertising转化跟踪的广告商)在报告中，如何在一系列导致转化的事件中归因转化数据：

   * *[!UICONTROL Unique]：* （默认值）计算维度值（如设备或投放位置）在转化路径上的次数。

   * *[!UICONTROL Multi-Touch Attribution (MTA)]：*&#x200B;根据维度值（如设备或投放位置）在转化路径上的出现频率分配每次转化的点数。 例如，如果在转化前总共有10次展示，其中8次在CTV上，2次在移动设备上，则80%的点数(0.8)将授予CTV屏幕，0.2次授予Mobile。

* **\[规则类型\]：** (包含[!UICONTROL Conversion Metrics]或[!UICONTROL Custom Goals]列的所有[!UICONTROL Custom]、[!UICONTROL Conversion]、[!UICONTROL Device]、[!UICONTROL Geo]、[!UICONTROL Segment]和[!UICONTROL Site]报表；仅包含Adobe Advertising转化跟踪的广告商)在报表中，如何在一系列导致转化的事件中归因转化数据。 如果要比较规则之间的差异，可以选择多个规则。

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

  <!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

* **回顾：** ([!UICONTROL Household Conversion]个包含[!UICONTROL Conversion Metrics]或[!UICONTROL Custom Goals]列的报表；仅包含Adobe Advertising转化跟踪的广告商)在报表中，转化事件可归因于展示事件后的最大天数。 默认值为&#x200B;*[!UICONTROL 30 days]*，最大值为92天。

**[!UICONTROL Paths as Columns]：** （所有[!UICONTROL Custom]、[!UICONTROL Conversion]、[!UICONTROL Device]、[!UICONTROL Geo]、[!UICONTROL Segment]和[!UICONTROL Site]报告具有[!UICONTROL Conversion Metrics]或[!UICONTROL Custom Goals]列）当同一设备上发生先前事件时要报告的转化类型。 您最多可以包含三种类型。 对于每个选定的类型，每个转化量度都包含一个单独的列，该列将附加指定的后缀（[!UICONTROL (tl)]、[!UICONTROL (ct)]或[!UICONTROL (vt)]）：

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]：*&#x200B;包含归因于点击（点进为CT）和展示次数（显示到达为VT）的转化。 归因于展示的转化次数乘以指定的显示到达权重。 默认显示到达权重为100%，这意味着由展示产生的转化将被计算为由点击产生的转化值的100%。

* *[!UICONTROL With Clicks (CT)]：*&#x200B;仅包含归因于点击的转化。

* *[!UICONTROL Impressions Only (VT)]：*&#x200B;仅包含归因于展示的转化，因为转化路径中未跟踪任何点击。

**[!UICONTROL Conversion Reporting Based On]：**&#x200B;如何报告转化数据：

* *[!UICONTROL Conversion Timestamp]：*（默认）转化与转化日期关联。

* *[!UICONTROL Event Timestamp]：*&#x200B;转化是根据引起转化的展示或点击的日期报告的，具体日期由指定的[!UICONTROL Attribution Rule Settings]确定。

## [!UICONTROL Add Report Destinations]节

**[!UICONTROL Destination Type]：**&#x200B;选择以下目标类型之一：

* *[!UICONTROL S3]：*&#x200B;若要将已完成的报告发送到一个或多个[!DNL Amazon Simple Storage Service] ([!DNL Amazon S3])位置，您必须在&#x200B;**[!UICONTROL Destination Name]**&#x200B;字段中指定这些位置。
* *[!UICONTROL sFTP]：*&#x200B;若要将已完成的报告发送到一个或多个SFTP位置，必须在&#x200B;**[!UICONTROL Destination Name]**&#x200B;字段中指定这些位置。
* *[!UICONTROL FTP]：*&#x200B;若要将已完成的报告发送到一个或多个FTP位置，必须在&#x200B;**[!UICONTROL Destination Name]**&#x200B;字段中指定这些位置。
* *[!UICONTROL FTP SSL](当前在Beta中)：*&#x200B;要将已完成的报表发送到一个或多个FTP SSL位置，必须在&#x200B;**[!UICONTROL Destination Name]**&#x200B;字段中指定这些位置。
* *[!UICONTROL Email]：*&#x200B;若要指定电子邮件地址，在报告因错误而被取消时，将已完成的报告或通知发送到这些地址。

>[!NOTE]
>
> 保存报表后，就无法更改目标类型。

**[!UICONTROL Email]：** （仅限电子邮件目标类型）对于每个地址，请输入地址并单击&#x200B;**+**。

**[!UICONTROL Destination Name]：**（仅限S3、FTP、sFTP和FTP SSL目标类型）将自定义报告发送到的目标报告名称。

* 要指定现有目标，请从列表中选择目标名称。 您可以分别选择多个目标名称。

* 要创建新目标，请执行以下操作：

   1. 单击&#x200B;**添加新目标**。

   1. 输入[报表目标设置](/help/dsp/reports/report-destinations/report-destination-settings.md)，然后单击&#x200B;**保存**。

   1. 返回报表设置，单击&#x200B;**刷新目标名称。**

      现在，可以从现有目标的列表中找到新目标，并且您可以选择将其添加到报表中。

**[!UICONTROL Frequency]：** （对于每个[!UICONTROL Destination Name]）将报告发送到目标的频率： *[!UICONTROL Once]*、*[!UICONTROL Daily]*、*[!UICONTROL Weekly]*&#x200B;或&#x200B;*[!UICONTROL Monthly]*。

**[!UICONTROL Start Day]：** （对于具有&#x200B;*[!UICONTROL Weekly]*&#x200B;或&#x200B;*[!UICONTROL Monthly]*&#x200B;的[!UICONTROL Frequency]的每个[!UICONTROL Destination Name]）生成报告的日期。 对于每周报告，请选择一周中的某一天。 对于月度报表，请选择月份的日期数字。

## [!UICONTROL Save Report]节

**[!UICONTROL When to Generate]：**&#x200B;何时生成报告： *[!UICONTROL On Schedule]*&#x200B;或&#x200B;*[!UICONTROL Run Now]*。 计划报表在帐户时区的09:00之前交付。

**[!UICONTROL End Date]：**&#x200B;报告到期日期，最长可为4个月之后。 在报告过期之前，所有指定的电子邮件收件人都会在过期日期的前七天零一天收到电子邮件警报。 要延长报表保留时间，请在报表设置中更改到期日期。

>[!NOTE]
>
>您可以随时从[!UICONTROL Reports]视图[运行自定义报表](report-run-now.md)。

>[!MORELIKETHIS]
>
>* [关于自定义报告](/help/dsp/reports/report-about.md)
>* [创建自定义报告](/help/dsp/reports/report-create.md)
>* [复制自定义报告](/help/dsp/reports/report-copy.md)
>* [编辑自定义报告](/help/dsp/reports/report-edit.md)
>* [运行自定义报告](/help/dsp/reports/report-run-now.md)
>* [自定义报表设置](/help/dsp/reports/report-settings.md)
>* [关于报表目标](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [可用报告列](/help/dsp/reports/report-columns.md)
