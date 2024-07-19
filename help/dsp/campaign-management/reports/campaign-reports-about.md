---
title: Campaign Management视图中的性能报表类型
description: 了解营销活动管理视图中包含的报表数据。
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: 4e82caa995286635b4a181f186d6a1fabb09847d
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Campaign Management视图中的性能报表类型

营销活动管理视图包括全面的报告数据。 可用报告可帮助您识别性能良好的资源包和投放位置以及需要您关注的资源包和投放位置。 快速操作按钮还可提高您的工作效率。

## 所有营销活动视图

[!UICONTROL Campaigns]视图会打开一组性能数据图表和您的帐户中所有营销活动的列表。

### 图表视图 {#chart-view}

您可以使用三个量度在所有营销活动中[自定义时间序列趋势图](campaign-data-views-manage.md#data-visualizations-manage)。 默认情况下，[!UICONTROL Net Spend]、[!UICONTROL Impressions]和[!UICONTROL Net CPM]的数据包含在单独的图表（网格图）中。 您可以选择更改量度。 要在时间序列趋势图中启用每小时数据，请将日期选择更改为一天（[!UICONTROL Today]、[!UICONTROL Yesterday]或特定日期）。

针对三个量度![单独的趋势图](/help/dsp/assets/trend-chart-separate.png)

您还可以选择叠加三个量度，以便轻松检测异常和用于改进规模或性能的区域。

![趋势图，带有叠加](/help/dsp/assets/trend-chart.png)

### 表格视图

![营销活动列表](/help/dsp/assets/campaigns-list.png)

默认情况下，每个营销活动行都包含步调和投放量度。 步调量度包括[!UICONTROL Gross Spend (Lifetime)]，其中包括对营销活动中所有包的实际目标上支出与预期目标上支出的衡量，因此您可以一目了然地识别表现不佳的营销活动。 您可以选择更改列视图](campaign-data-views-manage.md#column-view-change)，甚至[创建自定义列视图](campaign-data-views-manage.md#column-view-create)。[

您可以进一步[以其他方式自定义数据表](campaign-data-views-manage.md#data-tables-manage)和[筛选可见数据](campaign-data-views-manage.md#filter-data-tables)。

要查看促销活动的详细信息，请单击促销活动名称。

#### 警报指示器

*Beta功能*

“[!UICONTROL Alerts]”列指示营销活动或其下的任何子实体何时出现问题。 工具栏右侧的[!UICONTROL Pulse Panel]图标还指示列出的实体是否有任何警报可用。 有关详细信息，请参阅&quot;[查看警报](campaign-alerts.md)&quot;。

## 单个营销活动报告 {#single-campaign-reporting}

在营销策划中，您可以根据营销策划实体来筛选数据： [!UICONTROL Packages]、[!UICONTROL Placements]和[!UICONTROL Ads]。 您可以进一步[筛选可见数据](campaign-data-views-manage.md#filter-data-tables)以仅包含要查看的包、投放位置或广告。

![营销活动实体选项卡](/help/dsp/assets/campaign-subtabs.png)

### 图表视图

对于每个营销活动，您可以[使用三个量度（可在每个实体视图中找到）自定义时间序列趋势图](campaign-data-views-manage.md#data-visualizations-manage)。 促销活动的所有趋势图中都保留相同的量度。

有关详细信息，请参阅跨营销活动量度](#chart-view)上的[“图表视图”部分。

### 表格视图

默认情况下，每个实体选项卡中的每一行都包含步调和投放量度，但您可以[更改列视图](campaign-data-views-manage.md#column-view-change)，甚至[创建自定义列视图](campaign-data-views-manage.md#column-view-create)，以将其应用于营销活动的所有子选项卡。 您可以进一步通过其他方式[自定义数据表](campaign-data-views-manage.md#data-tables-manage)。 每个数据表都包含一个[!UICONTROL Subtotals]行，该行显示所有可见行中每个量度的总和或平均值。

#### 警报指示器

*Beta功能*

“[!UICONTROL Alerts]”列指示包、投放位置或广告（或包或投放位置下的任何子实体）何时出现问题。 “[!UICONTROL Alerts]”列指示营销活动或其下的任何子实体何时出现问题。 工具栏右侧的[!UICONTROL Pulse Panel]图标还指示列出的实体是否有任何警报可用。 有关详细信息，请参阅&quot;[查看警报](campaign-alerts.md)&quot;。

### 其他类型的营销活动级别报告

对于其他数据划分，请查看[营销活动级别的报表页面](/help/dsp/campaign-management/campaigns/campaign-view-report.md)。 该报告包含有关[!UICONTROL Geography]、[!UICONTROL Device]、[!UICONTROL Viewability]和[!UICONTROL Audience Performance]数据的部分。

### 其他类型的职位级别报表

对于其他数据划分，请查看[位置级报表页面](/help/dsp/campaign-management/placements/placement-view-report.md)。 该报告包含有关[!UICONTROL Geography]、[!UICONTROL Device]、[!UICONTROL Viewability]、[!UICONTROL Audience Performance]、[!UICONTROL Notifications]和[!UICONTROL Ads]数据的节。

此外，还可以在版面设置中查看以下数据：

* [A （详细信息视图[!UICONTROL Inspector]）](placement-details-view.md)，其中显示投放位置的所有目标网站、广告、频率数据和交易。

* [投放预测报告](/help/dsp/campaign-management/reports/placement-forecast.md)。

* [放置诊断报告](/help/dsp/campaign-management/reports/placement-diagnostics.md)。


### 其他类型的广告级别报表

对于其他数据划分，请查看[广告级别的报表页面](/help/dsp/campaign-management/ads/ad-view-report.md)。 该报告包含[!UICONTROL Overview]、[!UICONTROL Geography]和[!UICONTROL Viewability]数据。

>[!MORELIKETHIS]
>
>* [查看投放位置的网站、广告和频率详细信息](placement-details-view.md)
>* [管理您的Campaign数据视图](campaign-data-views-manage.md)
>* [从Campaign Management视图中导出数据](campaign-export-data.md)
>* [查看营销活动的详细报告](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
>* [查看警报](campaign-alerts.md)
