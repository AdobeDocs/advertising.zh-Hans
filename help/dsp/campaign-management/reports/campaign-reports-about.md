---
title: 关于Campaign Management视图中的性能报表
description: 了解营销活动管理视图中包含的报表数据。
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: 3f1095fe08e6bc6bf9c942b70295ac06d64ff852
workflow-type: tm+mt
source-wordcount: '937'
ht-degree: 0%

---

# 关于Campaign Management视图中的性能报表

营销活动管理视图包括全面的报告数据。 可用报告可帮助您识别性能良好的资源包和投放位置以及需要您关注的资源包和投放位置。 快速操作按钮还可提高您的工作效率。

## 所有营销活动视图

此 [!UICONTROL Campaigns] 视图打开以显示一组性能数据图表和您的帐户中所有营销活动的列表。

### 图表视图 {#chart-view}

您可以 [自定义时间序列趋势图](campaign-data-views-manage.md#data-visualizations-manage) 使用三个量度在所有营销活动中均可用。 默认情况下，数据 [!UICONTROL Net Spend]， [!UICONTROL Impressions]、和 [!UICONTROL Net CPM] 都包含在单独的图表（网格图）中。 您可以选择更改量度。 要在时间序列趋势图中启用每小时数据，请将日期选择更改为一天([!UICONTROL Today]， [!UICONTROL Yesterday]或特定日期)。

![三个量度的独立趋势图](/help/dsp/assets/trend-chart-separate.png)

您还可以选择叠加三个量度，以便轻松检测异常和用于改进规模或性能的区域。

![带叠加图的趋势图](/help/dsp/assets/trend-chart.png)

### 表格视图

![营销活动列表](/help/dsp/assets/campaigns-list.png)

默认情况下，每个营销活动行都包含步调和投放量度。 步调指标包括 [!UICONTROL Gross Spend (Lifetime)]，包括对营销活动中所有包的实际目标销售额与预期目标销售额的衡量，因此您可以一眼就识别表现不佳的营销活动。 您可以选择 [更改列视图](campaign-data-views-manage.md#column-view-change) 甚至 [创建自定义列视图](campaign-data-views-manage.md#column-view-create).

您可以进一步了解 [自定义数据表](campaign-data-views-manage.md#data-tables-manage) 以其他方式和 [筛选可见数据](campaign-data-views-manage.md#filter-data-tables).

<!--
An "Alerts" column indicates when a campaign (or any child entity under it) has an issue. Alert indicators include "Critical" (![Critical](/help/dsp/assets/indicator-critical.png "Critical")) and "Warning" (![Warning](/help/dsp/assets/indicator-warning.png "Warning")). See "[View Alerts and Notifications](campaign-alerts.md) for more information.
-->

要查看促销活动的详细信息，请单击促销活动名称。

## 单个营销活动报告 {#single-campaign-reporting}

在营销策划中，您可以根据营销策划实体过滤数据： [!UICONTROL Packages]， [!UICONTROL Placements]、和 [!UICONTROL Ads]. 您可以进一步了解 [筛选可见数据](campaign-data-views-manage.md#filter-data-tables) 以仅包含您要查看的包、投放位置或广告。

![营销活动实体选项卡](/help/dsp/assets/campaign-subtabs.png)

### 图表视图

对于每个活动，您可以 [自定义时间序列趋势图](campaign-data-views-manage.md#data-visualizations-manage) 提供了三个量度，这些量度在每个实体视图中均可用。 促销活动的所有趋势图中都保留相同的量度。

请参阅 [关于跨营销活动量度的“图表视图”部分](#chart-view) 以了解更多信息。

### 表格视图

在每个实体选项卡中，默认情况下，每行都包含步调和投放量度，但您可以 [更改列视图](campaign-data-views-manage.md#column-view-change) 甚至 [创建自定义列视图](campaign-data-views-manage.md#column-view-create) 以应用于营销活动的所有子选项卡。 您可以进一步了解 [自定义数据表](campaign-data-views-manage.md#data-tables-manage) 以其它方式。 每个数据表包括 [!UICONTROL Subtotals] 行，其中显示所有可见行中每个量度的总和或平均值。

<!--
An "Alerts" column indicates when a package, placement, or ad &mdash; or any child entity under a package or placement &mdash; has an issue. Alert indicators include "Critical" (![Critical](/help/dsp/assets/indicator-critical.png "Critical")) and "Warning" (![Warning](/help/dsp/assets/indicator-warning.png "Warning")). See "[View Alerts and Notifications](campaign-alerts.md) for more information.
-->

### 投放 [!UICONTROL Inspector] {#placement-inspector}

对于每个投放位置，您可以 [打开（详细信息视图） [!UICONTROL Inspector])](placement-details-view.md)，其中包括以下深入数据：

* **[!UICONTROL Sites]：** 投放位置上已有印象的所有网站。

  此 [!UICONTROL Sites] 选项卡包括搜索和筛选功能，与主页上相同的标准和自定义列视图选项，以及 [!UICONTROL Exclude] 按钮，以便快速从投放位置中排除网站。

* **[!UICONTROL Ads]：** 投放位置中的所有广告。

  此 [!UICONTROL Ads] 选项卡包括搜索和筛选功能，与主页上相同的标准和自定义列视图选项，以及每行中的快速操作按钮，例如 [!UICONTROL Pause] （以便快速暂停广告）。

* **[!UICONTROL Frequency]：** 投放的每个广告频率级别的数据，包括：
   * 广告频率级别（例如“1”，适用于用户一次看到广告的所有实例）
   * 设备/浏览器或人员的预计唯一数量(取决于指定的 [!UICONTROL Cross Device Level] （对于营销活动）在指定频率级别接收展示次数
   * 指定频率级别的预计展示次数
   * 指定频率级别的估计平均频率。 此值等于（预计展示次数）/（预计独特次数）。

* **[!UICONTROL Inventory]：** 有关投放位置定向的所有交易的信息。

  此 [!UICONTROL Inventory] 选项卡通过显示性能统计信息(例如 [!UICONTROL Auctions]， [!UICONTROL Bids]、和 [!UICONTROL Win Rate]. 选项卡包括搜索和筛选功能、主页上提供的相同标准和自定义列视图选项以及每行中的快速操作按钮，包括 [!UICONTROL Edit]， [!UICONTROL View Report]、和 [[!UICONTROL Auction Insights] 以进行进一步的故障排除](/help/dsp/inventory/private-deal-auction-insights.md).

#### 清单疑难解答

| 问题 | 可能的原因 | 要采取的操作 |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | 发布者尚未开始发送竞价请求。 | 联系发布者以激活交易。 |
| | 交易设置不正确，例如输入错误的外部交易ID。 | 确认交易详细信息并编辑交易。 |
| [!UICONTROL Auctions but no Bids] | 投放位置定位与交易的传入竞价请求不匹配。 <br><br> 例如，投放位置可能定向到不符合交易条件的地理位置。 | 根据需要编辑投放位置目标，以避免定位不匹配。 |
| | 投放位置没有具有交易所需的媒体类型的活动广告。 | 创建具有正确媒体类型的广告并将其附加到投放位置。 |
| | 该职位预算不足。 | 增加投放预算以允许对传入请求投标。 |
| | 投放投放日期与交易的展示投放日期不重叠。 | 根据需要编辑投放位置的投放日期。 |
| [!UICONTROL Low Win Rate] | 投放位置的最高出价（下限或固定）低于交易要求的最低出价。 | 增加投放位置的 [!UICONTROL Max Bid] 根据需要。 |
| | 投放位置使用限制竞价的预竞价过滤器。 | 降低预竞价筛选器的阈值以允许进行更多竞价。 |
| | 投放的受众定位过于严格。 | 检查指定的受众目标是否有足够的活动用户，如果可能，请展开受众。 |

![放置检查器](/help/dsp/assets/placement-inspector.png)

您可以将 [!UICONTROL Sites]， [!UICONTROL Ads]，或 [!UICONTROL Frequency] 导航到浏览器的默认下载文件夹，作为XLSM格式的报表。

### 其他类型的营销活动级别报告

对于其他数据划分，查看 [营销活动级别的报表页面](/help/dsp/campaign-management/campaigns/campaign-view-report.md). 此 <!--legacy --> 报告包含以下部分 [!UICONTROL Geography]， [!UICONTROL Device]， [!UICONTROL Viewability]、和 [!UICONTROL Audience Performance] 数据。

>[!MORELIKETHIS]
>
>* [查看投放位置的网站、广告和频率详细信息](placement-details-view.md)
>* [管理Campaign数据视图](campaign-data-views-manage.md)
>* [从Campaign Management视图中导出数据](campaign-export-data.md)
>* [查看营销活动的详细报告](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
