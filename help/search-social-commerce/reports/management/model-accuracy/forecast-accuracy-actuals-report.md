---
title: '[!UICONTROL Forecast Accuracy (Actuals) Report]'
description: 了解[!UICONTROL Forecast Accuracy (Actuals) Report]，包括数据列。
exl-id: 659e11c7-5fed-4d91-a73f-7c435d36634f
feature: Search Reports, Search Model Accuracy Reports
TQID: https://experienceleague.adobe.com/wQyO42Dt5McqK23z-adEP-BAxxTrBk9RJi0I-4noP0I
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 318
ht-degree: 0%

---

# [!UICONTROL Forecast Accuracy (Actuals) Report]

此报表可按天显示每个项目组合的实际展示次数、点击次数、成本和收入来自广告网络的数据。

## 可用列

以下是自动包含在每个报表中的列。 无法添加其他列。

| 列 | 默认？ | 描述 |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | 默认 | 项目组合所属的项目组合组的名称。 |
| [!UICONTROL Portfolio ID] | 默认 | 数值项目组合ID。 |
| [!UICONTROL EF Portfolio Group ID] | 默认 | 项目组合所属的项目组合组的数值ID。 |
| [!UICONTROL Portfolio] | 默认 | 项目组合。 |
| [!UICONTROL Portfolio Status] | 默认 | 项目组合状态：<ul><li><i>[!UICONTROL Optimize]：</i>优化功能正在收集相关营销活动的点击和收入数据，对用于优化的数据进行建模，并优化竞价、营销活动预算和营销活动竞价策略目标（具体取决于优化类型和竞价策略）。</li><li><i>[!UICONTROL Active]：</i>优化功能正在收集相关营销活动的点击和收入数据并正在建模数据，但并未优化竞价或营销活动预算。</li><li><i>[!UICONTROL Inactive]：</i>优化功能正在收集相关营销活动的点击数据以便进行报告，但它既不建模数据，也不优化竞价或营销活动预算。 |
| [!UICONTROL Day of Week] | 默认 | 报告的星期几： <i>[!UICONTROL Sunday]</i>、<i>[!UICONTROL Monday]</i>、<i>[!UICONTROL Tuesday]</i>、<i>[!UICONTROL Wednesday]</i>、<i>[!UICONTROL Thursday]</i>、<i>[!UICONTROL Friday]</i>或<i>[!UICONTROL Saturday]</i>。 |
| [!UICONTROL Event Date] | 默认 | 报告的日期。 |
| [!UICONTROL Device] | 默认 | (Google Ads， [!DNL LY Ads]， Microsoft Advertising， Yahoo！ 显示网络和Yahoo Native促销活动)显示广告的设备类型： <i>[!UICONTROL Computers]</i>、<i>[!UICONTROL Mobile]</i>、<i>[!UICONTROL Tablets]</i>、<i>[!UICONTROL Other]</i>或<i>[!UICONTROL N/A]</i>（无值）。 其他广告网络的行的值为<i>[!UICONTROL N/A]</i>。<br><br>在搜索营销活动中，如果关键字、广告和/或广告扩展的跟踪模板或目标URL包含按设备跟踪数据的参数(<code>&amp;ev_dvc={device}&amp;ev_dvm={devicemodel})</code>)，则转化数据也会包含在每种设备类型的行中。 否则，如果转化数据无法归因于某个设备类型，则会将其聚合到单独的行中，且该行的“[!UICONTROL Device]”值为<i>[!UICONTROL N/A]</i>。 |
| [!UICONTROL Revenue] | 默认 | 总收入。 |
| [!UICONTROL Impressions] | 默认 | 总展示次数。 |
| [!UICONTROL Clicks] | 默认 | 总点击次数。 |
| [!UICONTROL Cost] | 默认 | 总成本。 |

>[!MORELIKETHIS]
>
>* [关于模型准确性报告](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [该[!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [生成模型准确性报告](model-accuracy-report-generate.md)
>* [模型准确性报表设置](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
