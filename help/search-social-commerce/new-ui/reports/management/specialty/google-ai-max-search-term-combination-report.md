---
title: '[!UICONTROL Google AI Max Search Term Combination Report]'
description: 了解[!UICONTROL Google AI Max Search Term Combination Report]。
feature: Search Reports, Search Specialty Reports
source-git-commit: a595c7d6245fa5d65e704e88230f2eab0a336e72
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%
---
# [!UICONTROL Google AI Max Search Term Combination Report]

*仅适用于[!DNL Google Ads]个启用了最大AI营销活动的帐户*

[!UICONTROL Google AI Max Search Term Combination Report]显示特定搜索查询如何映射到由AI生成的标题和动态登陆页面，以及如何映射到指定帐户中启用了[!DNL Google Ads AI Max]的营销活动中广告的转化操作。 报告包含两个工作表：

* [!UICONTROL AI Max Search Term]表：基于搜索网络中的搜索的特定广告组合和登陆页面的性能。 该工作表包括展示次数、点击次数、成本数据以及在报告设置中指定的任何可选的[!DNL Google Ads]跟踪的转化量度。 默认情况下，对于在指定数据范围内至少获得一次展示的每个搜索词、标题和登陆页面组合，数据包括一行。 默认情况下，这些行先按促销活动升序，然后按您选择的另一列升序。

  使用此工作表可以分析每个查询生成的广告元素的目的和性能，以便构建可靠的负面关键词列表。

* <!-- [!UICONTROL Search Term x Conversion Action] sheet? -->[!UICONTROL AI Max Search Term #1]表：按每个搜索词和匹配类型的转换操作跟踪了[!DNL Google Ads]的转换数据。 每一行包括转换操作、转换次数、转换值，以及在报表设置中指定的任何其他可选的[!DNL Google Ads]跟踪的转换量度。 默认情况下，指定数据范围内每个搜索词和转换操作组合都包含一行。 这些行的顺序与第一页上的行的顺序相同。

  <!-- Should it be this?  The sheet includes the number of conversions and the conversion value, all conversions and the all conversions value, and cross-device conversions. -->

  使用此工作表可以了解每个搜索词如何促进按转化操作划分的转化。

<!-- We're pulling data directly from GGL and not storing it, so no limitations on our end WRT date range. -->

## 默认列

有关所有默认列和自定义列的说明，请参阅[专业报告的报告列](specialty-report-columns.md)。

<!-- VERIFY -- probably more will be included by default -->

* [!UICONTROL Event Date]
* [!UICONTROL Account Name]
* [!UICONTROL Network Campaign ID]
* [!UICONTROL Campaign Name]
* [!UICONTROL Ad Group Name]
* [!UICONTROL Search Term]
* [!UICONTROL Headline 1]
* [!UICONTROL Headline 2]
* [!UICONTROL Landing Page]
* [!UICONTROL Impressions]
* [!UICONTROL Clicks]
* [!UICONTROL Cost]
* [!UICONTROL Conversion Action] （自动包含在[!UICONTROL AI Max Search Term #1]工作表中，即使您不明确包含它）
* [!UICONTROL Conversions] （自动包含在[!UICONTROL AI Max Search Term #1]工作表中，即使您不明确包含它）
* [!UICONTROL Conversions Value] （自动包含在[!UICONTROL AI Max Search Term #1]工作表中，即使您不明确包含它）

>[!MORELIKETHIS]
>
>* [关于专业报告](specialty-report-about.md)
>* [管理计划报告](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
>* [专业报告设置](specialty-report-settings.md)
>* [专业报告的报告列](specialty-report-columns.md)
