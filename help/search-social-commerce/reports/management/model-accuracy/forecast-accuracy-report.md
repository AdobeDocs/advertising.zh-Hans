---
title: '[!UICONTROL Forecast Accuracy Report]'
description: 了解预测准确度报表，包括数据列。
exl-id: 2bb36728-ae14-441b-bcda-fa457f5cf664
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# 此 [!UICONTROL Forecast Accuracy Report]

此报表可按天显示指定项目组合的成本和收入模型的准确性。 默认情况下，它包括每个产品组合的每日预测和实际收入、成本和点击次数，以及预测的准确性。 它包括当前映射到项目组合的市场活动数据。

您可以查看前18个月的数据。

>[!NOTE]
>
>* 此报表提供与项目组合级别相同的数据 [!UICONTROL Model Accuracy Report] 但前提是您可以在多个项目组合中运行它，并且您可以更改归因规则。 您还可以使用自定义参数运行和计划报表，并使用该报表创建电子表格馈送。
>
>* 最佳做法是查看 [!UICONTROL Forecast Accuracy Report] 至少在过去7天里，因为无论投资组合的支出策略如何，大多数投资组合都看到了固有的“每周工作日”趋势。 优化能力将这一趋势考虑在内，并相应地分配支出。
>
>* 对于成本预测，过去7天中偏差10%被认为是可接受的，因此预测支出的90%至110%之间的实际支出是合适的。 对于收入预测，过去七天中出现15%的偏差被认为是可接受的，因此预测支出的85%到115%之间的实际收入是合适的。 应该调查偏差较大的预测。
>
>* 当项目组合中的关键字与竞价班次约束相关联时，项目组合因竞价班次导致的总支出过多或过少。 结果，预测的成本列偏离目标支出，增加或减少支出。

## 可用列

以下是可用于每个报表的列。 默认自动包括默认列。 您可以从以下位置添加可用的自定义列 [!UICONTROL Columns] 报告设置的部分。

| 列 | 默认？ | 描述 |
|----|----|----|
| [!UICONTROL Portfolio] | 默认 | 项目组合。 |
| [!UICONTROL Day of Week] | 默认 | 报告的一周中的某一天： <i>[!UICONTROL Sunday]</i>， <i>[!UICONTROL Monday]</i>， <i>[!UICONTROL Tuesday]</i>， <i>[!UICONTROL Wednesday]</i>， <i>[!UICONTROL Thursday]</i>， <i>[!UICONTROL Friday]</i>，或 <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Start Date] | 默认 | 报告的第一天。 |
| [!UICONTROL End Date] | 默认 | 报告的最后一天。 |
| [!UICONTROL Predicted Revenue] | 默认 | 投资组合的预测收入。 |
| [!UICONTROL Revenue] | 默认 | 项目组合的实际收入。 |
| [!UICONTROL Revenue Accuracy] | 默认 | 收入预测的准确性，以百分比表示。 |
| [!UICONTROL Predicted Cost] | 默认 | 投资组合的预测成本。 |
| [!UICONTROL Cost] | 默认 | 项目组合的实际成本。 |
| [!UICONTROL Cost Accuracy] | 默认 | 成本预测的准确性，以百分比表示。 |
| [!UICONTROL Predicted Clicks] | 默认 | 项目组合预测的点击次数。 |
| [!UICONTROL Clicks] | 默认 | 项目组合的实际点击次数。 |
| [!UICONTROL Click Accuracy] | 默认 | 点击预测的准确性，以百分比表示。 |
| [!UICONTROL EF Portfolio Group ID] | 默认 | 项目组合所属的项目组合组的数值ID。 |
| [!UICONTROL Portfolio Group Name] | 默认 | 项目组合所属的项目组合组的名称。 |
| [!UICONTROL Portfolio ID] | 默认 | 数值项目组合ID。 |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [关于模型精度报告](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [此 [!UICONTROL Forecast Accuracy (Actuals) Report]](forecast-accuracy-actuals-report.md)
>* [生成模型准确度报告](model-accuracy-report-generate.md)
>* [模型精度报表设置](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
