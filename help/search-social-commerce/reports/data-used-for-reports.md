---
title: 用于报表的数据
description: 了解数据视图和自定义报告中可用的不同类型数据。
exl-id: ba808b21-4421-4de5-9293-a20ec67cc81c
feature: Search Reports
source-git-commit: 840c7f6295b73a784725c301a78ae89c827fd45e
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# 用于报表的数据

搜索、社交和Commerce包括基于点击和转化数据的全套性能报表。 您可以从[!UICONTROL Portfolios]和[!UICONTROL Campaigns]视图中，以及通过生成各种基本和高级报告来查看组合或广告帐户的各种组件的基本性能数据。

使用Adobe Advertising转化跟踪服务的广告商还可以识别反向链接网站的地理位置或域名的点击次数、每个渠道中的广告以及导致转化的各种事件对整体转化率的贡献情况，以及营销渠道单个[转化量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)的转化分布情况。 可用的报告因用户帐户类型而异。 Adobe帐户团队有权访问所有报表。

大多数报告都可以自定义为仅显示要查看的信息。 以下标准量度在大多数报表中可用，并在广告级别计算：

* **标准性能指标：**

   * **[!UICONTROL Impressions]：**&#x200B;广告投放的总次数。

   * **[!UICONTROL Clicks]：**&#x200B;广告中链接被点击的总次数。

   * **[!UICONTROL Cost]：**&#x200B;广告的总成本。 每次点击付费(PPC)广告的成本始终是点击次数乘以每次点击成本。

   * **[!UICONTROL Cost per Click]：**&#x200B;广告一次点击的平均成本，即广告成本除以广告点击总数。 例如，如果您为一个广告展示花费了100 USD，并且该广告生成了10次点击，则每次点击成本为100 USD/10=10 USD/每次点击。

   * **[!UICONTROL Average Position]：** （适用时）已投放广告的平均位置，用展示次数加权。

   * **[!UICONTROL Estimated Clicks]：** (仅包含在具有Adobe Advertising转化跟踪服务的广告商的高级报告中)反向链接网站的某个城市或域名的预计点击总数。 这可能包括广告商没有广告帐户的广告网络的数据。

* **转化量度：**&#x200B;每个广告商的转化量度的转化总数，或针对某个转化量度跟踪的交易数据。 这可能包括转化和网站参与量度，但不包括从Adobe Analytics同步的计算量度和高级计算量度。

  这可能还包括为广告商帐户同步的[[!DNL Google Ads]跟踪的转化](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)和[[!DNL Google Analytics]跟踪的转化](/help/search-social-commerce/admin/data-sources/data-source-about.md)。

* **自定义量度：**&#x200B;您自己的量度，这些量度是通过基于现有量度（如每订单成本）创建公式派生的。

## 数据可用性

在生成报表时，您可以选择如何将转化数据归因到一系列导致转化的事件中。 例如，您可以选择将整个转化归因于最后一个事件，或者选择对最后一个事件的权重高于其他事件。 默认情况下，转化归属于最后一个事件。

根据您为报表指定的归因规则，每种报表类型的数据在以下日期可用。

| 报表组 | 报表 | 数据可用的日期 |
|---|---|---|
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | 自二零二一年五月十五日起。<br><br><b>异常：</b>显着性指标数据自2022年9月8日起可用。 |
| | 所有其他[!UICONTROL Basic Reports] | 之前的36个月。<br><br><b>异常：</b>显着性指标数据自2022年9月8日起可用。 |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | 之前的45天。 |
| | [!UICONTROL Domain Referral Report]，[!UICONTROL Geo Distribution Report] | 前两(2)个月加上本月。 |
| [!UICONTROL Assist Reports] | 全部 | 前18个月。 |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | 上一年。 |
| | [!UICONTROL RSA Assets Report] | 由二零二二年八月十日起 |
| | [!UICONTROL MSA Ad Extension by Ad Report]，[!UICONTROL MSA Ad Extension by Keyword Report]，[!UICONTROL MSA Ad Extension Detail Report]，[!UICONTROL MSA Network Impression Share Report]，[!UICONTROL MSA Network Performance Report] | 最近180天。 |
| | 所有其他[!UICONTROL Specialty Reports] | 前两(2)个月。 |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | 前18个月。 |
| [!UICONTROL Change History Report] | — | 之前的31天。 |

>[!MORELIKETHIS]
>
>* [关于报告](report-about.md)
>* [报告的初始设置任务](initial-setup.md)
