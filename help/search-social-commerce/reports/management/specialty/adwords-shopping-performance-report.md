---
title: '[!UICONTROL AdWords Shopping Performance Report]'
description: 了解 [!UICONTROL AdWords Shopping Performance Report].
exl-id: 5884efb5-d34f-47fd-82ad-93a5f4064110
feature: Search Reports, Search Specialty Reports
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# [!UICONTROL AdWords Shopping Performance Report]

*[!DNL Google Ads]仅限帐户*

此 [!UICONTROL AdWords Shopping Performance Report] 包括成本、点击量和展示量数据；由跟踪的已转换点击量和转化数据 [!DNL Google Ads Conversion Optimizer]；和（可选）由跟踪的转化数据 [!DNL Adobe] 和在产品ID级别为购物营销活动中的一个或多个广告组聚合的派生量度数据。 默认情况下，指定日期范围内每个时间单位的每个产品ID和每个广告组的产品类别都包含一行。 默认情况下，这些行按帐户名称、促销活动名称和广告组名称以升序排列。

您可以查看前两个月的数据。 2018年9月21日之前的数据可能以两行显示：一行包含成本和点击数据，另一行包含由Adobe跟踪的转化数据。 后续数据显示在一行中。

>[!NOTE]
>
>* 如果产品包含 [!UICONTROL Product Category] 列，并且产品以多个类别出现，然后该产品会出现在多个行中，并且转化计数会在每个适用的行中重复。 由于转化数据总计不准确，因此请仅按类别对数据进行排序，以便大致了解转化如何按类别呈趋势。
>* 此报告的数据提取时间为前一天的23:00（晚上11:00）。 例如，6月18日23:00时，它会提取6月17日的数据。 如果您在6月19日09:00运行报表（在提取6月18日的数据之前），则报表包含截至6月17日23:00的数据。

## 默认列

有关所有默认列和自定义列的说明，请参见&#39;&#39;[专业报告的报告列](specialty-report-columns.md)“

* [!UICONTROL Account Name]
* [!UICONTROL Campaign Name]
* [!UICONTROL Ad Group Name]
* [!UICONTROL Product ID]
* [!UICONTROL Category (1st level - 5th level)]
* [!UICONTROL Product Type (1st level - 5th level)]
* [!UICONTROL Start Date]
* [!UICONTROL End Date]
* [!UICONTROL Impressions]
* [!UICONTROL Clicks]
* [!UICONTROL Cost]
* [!UICONTROL Google Converted Clicks]
* [!UICONTROL Google Conversions]
* [!UICONTROL CTR]
* [!UICONTROL CPC]

>[!MORELIKETHIS]
>
* [关于专业报告](specialty-report-about.md)
* [生成专业报告](specialty-report-generate.md)
* [专业报告设置](specialty-report-settings.md)
