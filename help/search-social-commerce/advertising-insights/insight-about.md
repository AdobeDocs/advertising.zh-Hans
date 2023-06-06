---
title: 关于 [!UICONTROL Advertising Insights]
description: 了解不同类型的应用程序 [!UICONTROL Advertising Insights] 可用。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1310'
ht-degree: 0%

---

# 关于 [!UICONTROL Advertising Insights]

[!UICONTROL Advertising Insights] 提供关于包含有效营销活动的优化和活动项目组合的可视化可操作数据。

每个洞察都会按需生成，并且输出是可以下载的文件或屏幕报告。 您可以删除生成的分析文件实例。

## 类型 [!UICONTROL Advertising Insights]

| Insight | 描述 |
| --- | --- |
| [!UICONTROL AMO-AA Tracking Discrepancy] | (仅限具有AdobeAdvertising-Adobe Analytics集成的广告商)标识跟踪问题，其特征是天数具有超出正常方差的点击实例数比率，或具有20%或更高的方差。 该报告包括：<ul><li>A [!DNL Microsoft® PowerPoint] 包含数据差异摘要的文件；显示存在最常见跟踪问题的促销活动按促销活动显示的差异的表格和趋势图；故障排除建议；以及对报告方法的解释。</li><li>A [!DNL Microsoft® Excel] 文件包含项目组合中每个活动的概要数据以及每个活动过去一个月的每日数据。</li></ul> |
| [!UICONTROL Attribution Analysis] | ([!DNL PowerPoint] 呈现格式)指示不同的归因模型何时可以改进单个投资组合的收入模型和优化。 |
| [!UICONTROL Campaign Caps] | ([!DNL PowerPoint] 表示格式)指示单个组合在过去30天的支出是否受促销活动预算上限限制，并建议调整组合设置以实现最佳投资回报。 |
| [!UICONTROL Day of Week] | ([!DNL PowerPoint] presentation format)指示单个投资组合在过去30天内按星期几(DOW)列出的表现，并推荐使用DOW支出目标来提高您的投资回报。<br><br>**注意：** 支出不足的Portfolio或过去两天中无法支出进行定位的访客，无法用于洞察。 |
| [!UICONTROL Delayed Revenue] | 测量项目组合的转化滞后时间（在广告点击与后续转化之间经过的时间），并显示以下各项中的任何差异： [加权收入](/help/search-social-commerce/glossary.md#w-x)、ROI和模型准确性由于滞后而影响。 利用此分析，可检测点击日期归因绩效指标中的近期更改，并按点击日期与交易日期查看报表的影响。<br><br>此洞察包括 [!DNL Excel] 包含加权收入、未加权收入、收入准确性和滞后因子的单个工作表的工作簿。 它还包括一个 [!DNL Powerpoint] 包含各种图表的文件。 |
| [!UICONTROL Event Path] | 通过分析事件路径和多点接触转化，识别不同的渠道和营销活动如何推动转化。 您可以上传XLSX和ZIP（压缩XLSX）格式的文件，并且a)提取事件或b)分析分类的事件。 |
| [!UICONTROL Google Account Audit] | (对于 [!DNL Google Ads] 帐户；对预售最有用)提供帐户性能的概述，并突出显示不足之处，以显示管理帐户的效率。 审核包括有关竞价、匹配类型、预算上限、每周工作时间、移动性能等的信息。 要生成分析，您必须上传1) [!DNL Google Ads] 从以下位置查看客户的促销活动、关键字和更改历史记录报告： [!DNL Google Ads] Web用户界面和b)帐户的大批量工作表文件，该文件来自 [!DNL Google Ads Editor] 应用程序。 所有文件必须是CSV、TSV、TXT或ZIP（压缩的CSV、TSV或TXT）格式。<br><br>此洞察可用于帮助潜在客户了解Search、Social和Commerce如何提高性能并解决分析中强调的缺陷。 Adobe客户团队还可以在正式为客户上线之前使用该洞察信息评估客户。 |
| [!UICONTROL Impression Share Lost] | ([!DNL PowerPoint] presentation format)指示投资组合的预算何时限制了的展示份额 [!DNL Google Ads] 营销活动，并建议对预算和营销活动进行更改”[!UICONTROL Multiple]”设置。 |
| [!UICONTROL Location Target Performance] | (对于 [!DNL Google Ads] 营销活动； [!DNL Excel] 电子表格格式)竞价调整、点击次数、成本和 [加权收入](/help/search-social-commerce/glossary.md#w-x) 对于单个项目组合中的每个位置目标。 数据适用于过去90天内的任何日期范围，您可以查看每日结果或每个营销活动的摘要。 |
| [!UICONTROL Match Type] | 成本与成本的屏幕图表 [加权收入](/help/search-social-commerce/glossary.md#w-x) 最近90天内，在单个组合中跨匹配类型进行匹配。 |
| [!UICONTROL Mobile Optimization] | ([!DNL PowerPoint] 呈现格式)显示单个项目组合在过去30天内按设备类型的性能，评估特定于移动设备的优化功能的当前设置，并建议对设置进行调整。 |
| [!UICONTROL Model Accuracy] | 标识搜索、社交和商务预测单个活动或优化产品组合的支出和收入的效果，并标识模型不准确的来源。 该报告包括：<ul><li>A [!DNL PowerPoint] 包含过去7天预测和实际成本、点击次数、每次点击成本(CPC)、收入、每次点击收入(RPC)和投资回报率(ROI)的摘要的文件；上个月超支和支出过少竞价单位数据的汇总；显示上个月成本模型准确性、收入模型准确性和预测成本、点击次数、CPC、收入、RPC和ROI与实际值的趋势图；按点击级别划分的模型准确性；支出最多或支出过多的竞价单位；以及提高模型准确性的建议。</li><li>An [!DNL Excel] 按日期显示每个关键字的模型精确度和模型精确度的文件。</li></ul>此洞察比项目组合级别的模型准确性报告提供更多的详细信息，该报告可从 [!UICONTROL Portfolios] 视图。 |
| [!UICONTROL Normalized Sim (Combined)] | 返回多个项目组合中指定数量的目标支出级别（步骤）的最佳支出分配。 此洞察使用规范化的 [加权收入](/help/search-social-commerce/glossary.md#w-x) 基于指定时间期间的每周模拟。 您可以生成a)每个选定项目组合的单个模拟，或b)具有相同目标和币种的多个项目组合的单个模拟。 仿真以电子表格形式呈现。<br><br>对于单项、多项目组合模拟，该电子表格包括两个工作表：1)一个趋势图，显示每个目标支出级别（步骤）的规范化加权收入；2)一个表，显示每个适用支出级别（步骤）的一行。 对于个别项目组合模拟，该电子表格包括1)列出所有适用项目组合和时间期的汇总表，以及2)每个项目组合的两个表：a)显示每个目标支出级别（步骤）的规范化加权收入的趋势图，以及b)显示每个适用支出级别（步骤）一行的表格。 |
| [!UICONTROL Portfolio Launch] | ([!DNL PowerPoint] presentation format)标识项目组合是否已准备好启动（已更改为“已优化”状态）。 该报表包括预测绩效与实际绩效的比较；推荐的产品组合开始日期和应排除在成本和收入预测之外的日期列表；成本、收入、按成本划分的收入和随时间变化的关键字转化；有关过去两周支出上限的任何营销活动的信息；以及对launch或not launch的建议。 |
| [!UICONTROL Quality Score] | 显示具有展示次数的关键字的质量分数趋势 [!DNL Google Ads] 或 [!DNL Microsoft® Advertising] 过去90天内。 它包括a) a [!DNL PowerPoint] 文件和b) [!DNL Excel] 文件包含支出最多的100个关键字和质量分数较低的前100个关键字（如果适用）。<br><br>**注释：**<ul><li>当项目组合具有超过20,000个竞价单位时，只包括在过去30天（而不是90天）内多次点击的关键字。</li><li>包含许多关键字的数据的分析需要更长的时间才能生成。</li></ul> |
| [!UICONTROL Query Cross Matching] | ([!DNL Google Ads] accounts)标识搜索查询的实例 [!DNL Google Ads] 匹配多个关键字，并提供有关流量所定向目标的建议。 使用这些建议来改进关键词性能，从而改进模型的准确性。<br><br>此分析包括交叉匹配查询、匹配的关键字和性能数据的电子表格；帮助您可视化交叉匹配查询与关键字之间关系的网络图；底层搜索查询报表；有关如何解释数据的信息。 |
| [!UICONTROL Settings Audit] | 指示您的项目组合是否按最佳实践进行配置。 它包括：<ul><li>A [!DNL PowerPoint] 该文件显示是否根据最佳实践配置了所有项目组合及其组件营销活动的关键设置、是否将任何营销活动分配给项目组合，以及偏离最佳实践的后果。</li><li>An [!DNL Excel] 文件，其中每个关键项目组合设置和关键促销活动设置都有一个单独的选项卡。 数据包括您的每个项目组合的项目组合设置，以及不符合最佳实践的每个营销活动的营销活动设置。</li></ul> |
| [!UICONTROL Time-of-day Analysis] | (适用于具有以下特征的项目组合： [!DNL Google Ads] 仅限搜索、显示或购物营销活动)建议 [!DNL Google Ads] 基于单个组合每小时性能的每日不同时间的促销活动级别竞价修饰符（广告计划竞价修饰符）。<br><br>此洞察包括 [!DNL Excel] 带有单独工作表的工作簿 [!UICONTROL Detailed Performance] （按活动显示的时间间隔的绩效）和 [!UICONTROL Recommended TBAs] （每个促销活动的推荐广告时间表）。 您可以导出 [!UICONTROL Recommended TBAs] 将工作表直接添加到 [!DNL Google Ads] 编辑者。 此洞察还包括 [!UICONTROL Powerpoint] 包含支持数据和解释的文件。 |

>[!MORELIKETHIS]
>
>* [生成 [!DNL Advertising Insight]](insight-generate.md)
>* [查看或保存 [!DNL Advertising Insight]](insight-view-save.md)
>* [删除 [!DNL Advertising Insight]](insight-delete.md)

