---
title: 自定义报表设置
description: 请参阅对自定义报表设置的描述。
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: b41c1ab857d37d21cf593a8e566b18f2769d47c0
workflow-type: tm+mt
source-wordcount: '1123'
ht-degree: 0%

---

# 自定义报表设置

**[!UICONTROL Name]** 报表名称。 最大长度为180个字符。

**[!UICONTROL Report Type]** 报告的类型： *[!UICONTROL Custom]* （包括大多数可用选项）， *[!UICONTROL Billing]*， *[!UICONTROL Conversion]*， *[!UICONTROL Device]*， *[!UICONTROL Frequency (by Impression)]*，  *[!UICONTROL Frequency (by App/Site)]*， *[!UICONTROL Geo]*， *[!UICONTROL Margin]*， *[!UICONTROL Media Performance]*，  *[!UICONTROL Segment]*， *[!UICONTROL Site]*， *[!UICONTROL Household Reach & Frequency]*，或 *[!UICONTROL Household Conversions]*.

## [!UICONTROL Apply Filters] 章节

**[!UICONTROL Timezone]：** 报表的时区。

**[!UICONTROL Observe Daylight Savings Time]：** 考虑报告时间中的夏令时。

**\[日期范围\]：** 要为其生成数据的日期范围。 可用天数因报表和所选维度而异。 选择一个：

* **[!UICONTROL Previous N days]：** 包括今天之前特定天数的数据。

* **[!UICONTROL Custom]：** 包括特定开始日期和结束日期之间的数据。 要报告前一天的数据，请选择 **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]：** 包括上一个日历月的数据。

**[!UICONTROL Add Filters]：** （可选）用于筛选数据的其他维度，无论这些维度是否作为列包含在报表中。 可用的过滤器因报告类型而异，可能包括： *[!UICONTROL Account]*\*， *[!UICONTROL Ad Type]*， *[!UICONTROL Ads]*， *[!UICONTROL Advertiser]*， *[!UICONTROL Campaign]*， *[!UICONTROL Country]*， * *[!UICONTROL Package]*， *[!UICONTROL Placement]*， *[!UICONTROL Video]*、和 *[!UICONTROL Video Duration]*.

\* *[!UICONTROL Account]* 仅当您的组织配置为以下报表类型时，才可用 [跨帐户报告](report-about.md#cross-account-reporting)：  [!UICONTROL Custom]， [!UICONTROL Site]， [!UICONTROL Segment]， [!UICONTROL Geo]， [!UICONTROL Device]， [!UICONTROL Frequency (by Impression)]、和 [!UICONTROL Conversion]. 请联系您的Adobe客户团队，以获取有关跨帐户报表的更多信息。

要应用一个或多个筛选器，请执行以下操作：

* 选择维，选择运算符(*等于* 或 *不等于*)，然后选择适用的值。 例如，要仅返回前置广告的数据，请指定&quot;[!UICONTROL Ad Type equals Preroll].”
* （可选）向筛选条件添加其他标准。
* （可选）添加其他过滤器，每个过滤器都有一个或多个标准。

## [!UICONTROL Build Your Report] 章节

**[!UICONTROL Select To Add As Report Headers]：**  要包含在报表中的数据列或标题。 要添加列，请展开类别并选中列名旁边的复选框。 可用列因报告而异，并且所有不可用的量度都已禁用。 可用的数据类别包括：

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > 此 [!UICONTROL Household Reach & Frequency] 报表只能包含一个维度。

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >此 [!UICONTROL Household Reach & Frequency] 报表可以包含重叠量度或非重叠量度，但不能同时包含这两个量度。

* [!UICONTROL Conversion Metrics] （按广告商排序）

* [!UICONTROL Custom Goals] （按广告商排序）

参见“[可用报表列](report-columns.md)”以了解所有选项的描述。

**[!UICONTROL Drag to Re-Order Report Headers Below]：** 列标题的顺序。 您可以拖放任何列以自定义顺序。

**[!UICONTROL Format]：** 是否在中生成报告 *[!UICONTROL CSV]* （逗号分隔值）或 *[!UICONTROL Tab]* （制表符分隔值）格式。

**[!UICONTROL Headers]：** 是否要 *[!UICONTROL Include]* 或 *[!UICONTROL Do Not Include]* 列标题。

## [!UICONTROL Multi-Touch Conversion Options] 章节


### [!UICONTROL Attribution Rule Settings]

**\[归因类型\]：** ([!UICONTROL Household Conversion] 报告 [!UICONTROL Conversion Metrics] 或 [!UICONTROL Custom Goals] 列；仅具有Adobe Advertising转化跟踪的广告商)在报表中，如何在一系列导致转化的事件中归因转化数据：

* [!UICONTROL Unique]：（默认）计算维度值（如设备或投放位置）在转化路径上的次数。

* [!UICONTROL Multi-Touch Attribution (MTA)]：根据维度值（如设备或投放位置）在转化路径上的出现频率分配每次转化的点数。 例如，如果在转化前总共有10次展示，其中8次在CTV上展示，2次在移动设备上展示，则信用的80%(0.8)将给予给CTV屏幕，0.2给予移动设备屏幕。

**\[规则类型\]：** (全部 [!UICONTROL Custom]， [!UICONTROL Conversion]， [!UICONTROL Device]， [!UICONTROL Geo]， [!UICONTROL Segment]、和 [!UICONTROL Site] 报告 [!UICONTROL Conversion Metrics] 或 [!UICONTROL Custom Goals] 列；仅具有Adobe Advertising转化跟踪的广告商)在报表中，如何在一系列导致转化的事件中归因转化数据。 如果要比较规则之间的差异，可以选择多个规则。

>[!NOTE]
>
>转化路径包括广告商展示或点击回顾窗口内的任何展示和点击，这些均在中配置 [!DNL Advertising Search, Social, & Commerce]. 在转化归因期间，点击次数优先于展示次数。 根据归因规则，转化路径中的任何点击都将获得完全点数。 只有转化路径中未跟踪任何点击时，展示次数才会获得点数。

* *[!UICONTROL Last Event]：* 将转化归因于转化路径中的最后一次点击或展示。

* *[!UICONTROL Weight Last More]：* 将转化归因于转化路径中的所有事件，但给予最后一个事件的权重最大，给予前一个事件的权重依次较低。

* *[!UICONTROL Even Distribution]：* 将转化同等地归因于转化路径中的每个事件。

* *[!UICONTROL Weight First More]：* 将转化归因于转化路径中的所有事件，但给予第一个事件的权重最大，给予以下事件的权重依次较低。

* *[!UICONTROL First Event]：* 将转化归因于转化路径中的第一次点击或展示。

* *[!UICONTROL U-shaped]：* 将转化归因于转化路径中的所有事件，但给予第一个和最后一个事件的权重最大，给予转化路径中间事件的权重依次较低。

* *[!UICONTROL Display Only]：*  将转化归因于转化路径中的上次DSP点击或展示。 这包括视频和连接的电视广告，并且不包括点击 [!DNL Advertising Search, Social, & Commerce] 广告。

* *[!UICONTROL Social Only]：* 已过时

<!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

**[!UICONTROL Paths as Columns]：**  (全部 [!UICONTROL Custom]， [!UICONTROL Conversion]， [!UICONTROL Device]， [!UICONTROL Geo]， [!UICONTROL Segment]、和 [!UICONTROL Site] 报告 [!UICONTROL Conversion Metrics] 或 [!UICONTROL Custom Goals] 列)当同一设备上发生先前的事件时要报告的转化类型。 您最多可以包含三种类型。 对于每个选定的类型，每个转化量度都包含一个单独的列，该列后附加指定的后缀([!UICONTROL (tl)]， [!UICONTROL (ct)]，或 [!UICONTROL (vt)])：

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]：* 包含归因于点击次数（点进为CT）和展示次数（点进为VT）的转化。 归属于展示的转化次数乘以指定的显示到达权重。 默认显示到达权重为100%，这意味着归因于展示的转化将被计算为归因于点击的转化值的100%。

* *[!UICONTROL With Clicks (CT)]：* 仅包含归因于点击的转化。

* *[!UICONTROL Impressions Only (VT)]：* 仅包括归因于展示的转化，因为转化路径中未跟踪任何点击。

**[!UICONTROL Conversion Reporting Based On]：**  如何报告转化数据：

* *[!UICONTROL Conversion Timestamp]：* （默认）转化将与转化日期关联。

* *[!UICONTROL Event Timestamp]：* 将根据导致转化的展示或点击的日期报告转化，具体日期由指定的决定 [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Report Destinations] 章节

**[!UICONTROL Destination Type]：** 选择以下目标类型之一：

* *[!UICONTROL S3]：* 将完成的报表发送给一个或多个 [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3])位置，您将在 **[!UICONTROL Destination Name]** 字段。
* *[!UICONTROL sFTP]：* 要将完成的报表发送到一个或多个SFTP位置，您将在 **[!UICONTROL Destination Name]** 字段。
* *[!UICONTROL FTP]：* 要将完成的报表发送到一个或多个FTP位置，您将在 **[!UICONTROL Destination Name]** 字段。
* *[!UICONTROL FTP SSL]（目前为测试版）：* 要将完成的报表发送到一个或多个FTP SSL位置，您将在 **[!UICONTROL Destination Name]** 字段。
* *[!UICONTROL Email]：* 指定在报告因错误而被取消时将已完成报告或通知发送到的电子邮件地址。 要指定多个地址，请用逗号或空格分隔。

>[!NOTE]
>
> 保存报告后，就无法更改目标类型。

**[!UICONTROL Destination Name]：** （仅限S3、FTP、sFTP和FTP SSL目标类型）将向其发送自定义报表的报表目标的名称。

* 要指定现有目标，请从列表中选择目标名称。 您可以分别选择多个目标名称。

* 要创建新目标，请执行以下操作：

   1. 单击 **添加新目标**.

   1. 输入 [报表目标设置](/help/dsp/reports/report-destinations/report-destination-settings.md)，然后单击 **保存**.

   1. 返回报表设置，单击 **刷新目标名称。**

      新目标现在可以从现有目标列表中获得，并且您可以选择将其添加到报表中。

**[!UICONTROL Frequency]：** (对于每个 [!UICONTROL Destination Name] 将报告发送到目标的频率： *[!UICONTROL Once]*， *[!UICONTROL Daily]*， *[!UICONTROL Weekly]*，或 *[!UICONTROL Monthly]*.

## [!UICONTROL Save Report] 章节

**[!UICONTROL Send & Save]：** 何时发送报告： *[!UICONTROL On Schedule]* 或 *[!UICONTROL Run Now]*. 计划报表将于9:00之前在帐户所在时区传送。

>[!NOTE]
>
>您可以 [随时运行自定义报表](report-run-now.md) 从 [!UICONTROL Reports] 视图。

>[!MORELIKETHIS]
>
>* [关于自定义报表](/help/dsp/reports/report-about.md)
>* [创建自定义报表](/help/dsp/reports/report-create.md)
>* [复制自定义报表](/help/dsp/reports/report-copy.md)
>* [编辑自定义报告](/help/dsp/reports/report-edit.md)
>* [运行自定义报表](/help/dsp/reports/report-run-now.md)
>* [自定义报表设置](/help/dsp/reports/report-settings.md)
>* [关于报表目标](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [可用报表列](/help/dsp/reports/report-columns.md)
