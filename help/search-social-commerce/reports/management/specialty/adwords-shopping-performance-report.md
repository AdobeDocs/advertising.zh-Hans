---
title: '[!UICONTROL AdWords Shopping Performance Report]'
description: 了解[!UICONTROL AdWords Shopping Performance Report]。
exl-id: 891c8940-bf92-455c-a6f3-92e2a0122b4a
feature: Search Reports, Search Specialty Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# [!UICONTROL AdWords Shopping Performance Report]

仅&#x200B;*[!DNL Google Ads]个帐户*

[!UICONTROL AdWords Shopping Performance Report]包括成本、点击次数和印象数据；由[!DNL Google Ads Conversion Optimizer]跟踪的转化点击次数和转化数据；以及（可选）由[!DNL Adobe]跟踪的转化数据和在购物营销活动中一个或多个广告组的产品ID级别聚合的派生量度数据。 默认情况下，指定日期范围内每个时间单位的每个产品ID和每个广告组的产品类别都包含一行。 默认情况下，这些行按帐户名称、促销活动名称和广告组名称以升序排列。

您可以查看前两个月的数据。 2018年9月21日之前的数据可能以两行显示：一行包含成本和点击数据，另一行包含由Adobe跟踪的转化数据。 后续数据显示在一行中。

>[!NOTE]
>
>* 如果产品包含[!UICONTROL Product Category]列，并且产品出现在多个类别中，则该产品会出现在多个行中，并且转化计数会在每个适用的行中重复。 由于转化数据总计不准确，因此请仅按类别对数据进行排序，以便大致了解转化如何按类别呈趋势。
>* 此报告的数据提取时间为前一天的23:00（晚上11:00）。 例如，6月18日23:00时，它会提取6月17日的数据。 如果您在6月19日09:00运行报表（在提取6月18日的数据之前），则报表包含截至6月17日23:00的数据。

## 默认列

有关所有默认列和自定义列的说明，请参阅[专业报告的报告列](specialty-report-columns.md)。

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
>* [关于专业报告](specialty-report-about.md)
>* [生成专业报告](specialty-report-generate.md)
>* [专业报告设置](specialty-report-settings.md)
