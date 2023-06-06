---
title: "[!UICONTROL Forecast Accuracy (Actuals) Report]"
description: 了解 [!UICONTROL Forecast Accuracy (Actuals) Report]，包括数据列。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# 此 [!UICONTROL Forecast Accuracy (Actuals) Report]

此报表可按天显示每个项目组合的实际广告展示次数、点击次数、成本和收入数据。

## 可用列

以下是自动包含在每个报表中的列。 无法添加其他列。

| 列 | 默认？ | 描述 |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | 默认 | 项目组合所属的项目组合组的名称。 |
| [!UICONTROL Portfolio ID] | 默认 | 数值项目组合ID。 |
| [!UICONTROL EF Portfolio Group ID] | 默认 | 项目组合所属的项目组合组的数值ID。 |
| [!UICONTROL Portfolio] | 默认 | 项目组合。 |
| [!UICONTROL Portfolio Status] | 默认 | 项目组合状态：<ul><li><i>[!UICONTROL Optimize]：</i> 优化能力是收集相关营销活动的点击和收入数据，建模数据以优化竞价，以及优化竞价和/或营销活动预算（取决于优化类型和营销活动竞价策略）。</li><li><i>[!UICONTROL Active]：</i> 优化功能正在收集相关营销活动的点击和收入数据并对数据进行建模，但不是优化竞价或营销活动预算。</li><li><i>[!UICONTROL Inactive]：</i> 优化功能会收集相关营销活动的点击数据以便进行报告，但它不会建模数据，也不会优化竞价或营销活动预算。 |
| [!UICONTROL Day of Week] | 默认 | 报告的一周中的日期： <i>[!UICONTROL Sunday]</i>， <i>[!UICONTROL Monday]</i>， <i>[!UICONTROL Tuesday]</i>， <i>[!UICONTROL Wednesday]</i>， <i>[!UICONTROL Thursday]</i>， <i>[!UICONTROL Friday]</i>，或 <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Event Date] | 默认 | 报告的日期。 |
| [!UICONTROL Device] | 默认 | (Google Ads、Microsoft®Advertising、Yahoo！ Display Network， Yahoo！ Japan Ads和Yahoo Native campaigns)显示广告的设备类型： <i>[!UICONTROL Computers]</i>， <i>[!UICONTROL Mobile]</i>， <i>[!UICONTROL Tablets]</i>， <i>[!UICONTROL Other]</i>，或 <i>[!UICONTROL N/A]</i> （无值）。 其他广告网络的行具有值 <i>[!UICONTROL N/A]</i>.<br><br>在搜索营销活动中，如果关键词、广告和/或广告扩展的跟踪模板或目标URL包含用于按设备跟踪数据的参数(&amp;ev_dvc={device}&amp;ev_dvm={devicemodel})</code>)时，转化数据也会包含在每种设备类型的行中。 否则，如果转化数据无法归因于某个设备类型，则会汇总到单独的一行中，其中包含“[!UICONTROL Device]的“ ”值 <i>[!UICONTROL N/A]</i>. |
| [!UICONTROL Revenue] | 默认 | 总收入。 |
| [!UICONTROL Impressions] | 默认 | 总展示次数。 |
| [!UICONTROL Clicks] | 默认 | 总点击次数。 |
| [!UICONTROL Cost] | 默认 | 总成本。 |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [关于模型精度报告](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [此 [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [生成模型准确性报告](model-accuracy-report-generate.md)
>* [模型准确性报表设置](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)

