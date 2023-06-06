---
title: "[!UICONTROL Forecast Accuracy Report]"
description: 了解预测准确度报表，包括数据列。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# 此 [!UICONTROL Forecast Accuracy Report]

该报告按天显示指定项目组合的成本和收入模型的准确性。 默认情况下，它包括每个产品组合的每日预测和实际收入、成本和点击次数，以及预测的准确性。 它包括当前映射到项目组合的市场活动数据。

您可以查看前18个月的数据。

>[!NOTE]
>
>* 此报表提供与项目组合级别相同的数据 [!UICONTROL Model Accuracy Report] 但前提是您可以在多个项目组合中运行它，并且您可以更改归因规则。 您还可以使用自定义参数运行和计划报表，并可以使用它来创建电子表格馈送。
>
>* 最佳做法是查看 [!UICONTROL Forecast Accuracy Report] 至少在最近7天内，因为无论投资组合的支出策略如何，大多数投资组合都看到了固有的“一周中的某天”趋势。 优化能力会考虑此趋势并相应地分配支出。
>
>* 对于成本预测，过去7天中的10%的偏差被认为是可以接受的，因此预测支出的90%至110%之间的实际支出可以接受。 对于收入预测，过去7天中存在15%的偏差被认为是可接受的，因此预测支出的85%至115%之间的实际收入是可以接受的。 应该调查偏差较大的预测。
>
>* 当项目组合中的关键字与竞价转移约束关联时，项目组合因竞价转移导致的总支出超支或少支。 因此，预测的成本列偏离了增加或减少的支出的目标支出。


## 可用列

以下是可用于每个报表的列。 默认自动包含默认列。 您可以从以下位置添加可用的自定义列 [!UICONTROL Columns] 报告设置的部分。

| 列 | 默认？ | 描述 |
|----|----|----|
| [!UICONTROL Portfolio] | 默认 | 项目组合。 |
| [!UICONTROL Day of Week] | 默认 | 报告的一周中的日期： <i>[!UICONTROL Sunday]</i>， <i>[!UICONTROL Monday]</i>， <i>[!UICONTROL Tuesday]</i>， <i>[!UICONTROL Wednesday]</i>， <i>[!UICONTROL Thursday]</i>， <i>[!UICONTROL Friday]</i>，或 <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Start Date] | 默认 | 报告的第一天。 |
| [!UICONTROL End Date] | 默认 | 报告的最后一天。 |
| [!UICONTROL Predicted Revenue] | 默认 | 投资组合的预测收入。 |
| [!UICONTROL Revenue] | 默认 | 项目组合的实际收入。 |
| [!UICONTROL Revenue Accuracy] | 默认 | 收入预测的准确性，以百分比表示。 |
| [!UICONTROL Predicted Cost] | 默认 | 投资组合的预测成本。 |
| [!UICONTROL Cost] | 默认 | 投资组合的实际成本。 |
| [!UICONTROL Cost Accuracy] | 默认 | 成本预测的准确性，以百分比表示。 |
| [!UICONTROL Predicted Clicks] | 默认 | 预测的投资组合点击次数。 |
| [!UICONTROL Clicks] | 默认 | 项目组合的实际点击次数。 |
| [!UICONTROL Click Accuracy] | 默认 | 点击预测的准确度，以百分比表示。 |
| [!UICONTROL EF Portfolio Group ID] | 默认 | 项目组合所属的项目组合组的数值ID。 |
| [!UICONTROL Portfolio Group Name] | 默认 | 项目组合所属的项目组合组的名称。 |
| [!UICONTROL Portfolio ID] | 默认 | 数值项目组合ID。 |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [关于模型精度报告](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [此 [!UICONTROL Forecast Accuracy (Actuals) Report]](forecast-accuracy-actuals-report.md)
>* [生成模型准确性报告](model-accuracy-report-generate.md)
>* [模型准确性报表设置](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)

