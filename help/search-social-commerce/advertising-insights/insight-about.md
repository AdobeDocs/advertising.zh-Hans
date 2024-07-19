---
title: 关于[!UICONTROL Advertising Insights]
description: 了解可用的不同类型的[!UICONTROL Advertising Insights]。
exl-id: e6eec71e-04ab-4180-95f2-da31a26e5c1a
feature: Search Advertising Insights
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1354'
ht-degree: 0%

---

# 关于[!UICONTROL Advertising Insights]

[!UICONTROL Advertising Insights]显示有关包含有效营销活动的优化和活动项目组合的可视、可操作数据。

每个分析都是按需生成的，输出是可以下载的文件或屏幕报告。 您可以删除生成的分析文件实例。

## [!UICONTROL Advertising Insights]的类型

| Insight | 描述 |
| --- | --- |
| [!UICONTROL AMO-AA Tracking Discrepancy] | (仅限集成了Adobe Advertising-Adobe Analytics的广告商)标识跟踪问题，其特征是点击实例数比率超出正常方差的天数或20%或以上的方差。 该报告包括：<ul><li>包含数据差异摘要的[!DNL Microsoft PowerPoint]文件；显示具有最常见跟踪问题的营销活动的各营销活动差异的表格和趋势图；故障排除建议；以及对报告方法的解释。</li><li>[!DNL Microsoft Excel]文件，其中包含产品组合中每个营销活动的概要数据以及每个营销活动过去一个月内的每日数据。</li></ul> |
| [!UICONTROL Attribution Analysis] | （[!DNL PowerPoint]呈现格式）指示不同的归因模型何时可以改进单个投资组合的收入模型和优化。 |
| [!UICONTROL Campaign Caps] | （[!DNL PowerPoint]演示格式）指示单个组合在过去30天的支出是否受促销活动预算上限限制，并建议调整组合设置以实现最佳投资回报。 |
| [!UICONTROL Day of Week] | （[!DNL PowerPoint]演示格式）指示单个投资组合在过去30天内按星期几(DOW)列出的表现，并建议采用DOW支出目标以提高您的投资回报。<br><br>**注意：**&#x200B;支出不足或过去两天无法支出的Portfolio不可用于分析。 |
| [!UICONTROL Delayed Revenue] | 测量产品组合的转化滞后时间（在广告点击与后续转化之间经过的时间），并显示由于该滞后导致的加权收入（现在称为“[目标值](/help/search-social-commerce/glossary.md#o-p)”）、ROI和模型准确性方面的任何差异。 通过此分析，您可以检测点击日期归因绩效指标中的最新更改，并按点击日期与交易日期查看报表的影响。<br><br>此分析包含一个[!DNL Excel]工作簿，其中包含加权收入（现在称为“目标值”）、收入准确性和滞后因素等各个工作表。 它还包含带有各种图表的[!DNL Powerpoint]文件。 |
| [!UICONTROL Event Path] | 通过分析事件路径和多点触控转化，识别不同的渠道和营销活动如何推动转化。 您可以上传XLSX和ZIP（压缩XLSX）格式的文件，以及a)提取事件或b)分析分类的事件。 |
| [!UICONTROL Google Account Audit] | （对于[!DNL Google Ads]帐户；对预销售最有用）提供帐户性能的概述，并突出显示不足之处以显示其管理效率。 审核包括有关竞价、匹配类型、预算上限、每周工作时间、移动性能等的信息。 要生成洞察，您必须从[!DNL Google Ads] Web用户界面上传1) [!DNL Google Ads]帐户促销活动、关键字和更改历史记录报告，以及b)从[!DNL Google Ads Editor]应用程序上传帐户批量处理工作表文件。 所有文件都必须采用CSV、TSV、TXT或ZIP（压缩的CSV、TSV或TXT）格式。<br><br>此洞察信息可用于帮助潜在客户了解Search、Social和Commerce如何提高性能并解决分析所强调的缺陷。 Adobe客户团队还可以在正式为客户上线之前使用该见解评估客户。 |
| [!UICONTROL Impression Share Lost] | （[!DNL PowerPoint]演示格式）指示项目组合的预算何时限制了[!DNL Google Ads]营销活动的展示份额，并相应地建议更改预算和营销活动“[!UICONTROL Multiple]”设置。 |
| [!UICONTROL Location Target Performance] | （对于[!DNL Google Ads]个促销活动；[!DNL Excel]电子表格格式）单个项目组合中每个位置目标的竞价调整、点击次数、成本和加权收入（现在称为“[目标值](/help/search-social-commerce/glossary.md#o-p)”）。 数据适用于过去90天内的任何日期范围，您可以查看每日结果或每个营销活动的摘要。 |
| [!UICONTROL Match Type] | 最近90天内单个组合中匹配类型的成本和加权收入（现在称为“[目标值](/help/search-social-commerce/glossary.md#o-p)”）的屏幕图表。 |
| [!UICONTROL Mobile Optimization] | （[!DNL PowerPoint]演示格式）按设备类型显示单个项目组合在过去30天的性能，评估特定于移动设备的优化功能的当前设置，并建议调整设置。 |
| [!UICONTROL Model Accuracy] | 确定Search、Social和Commerce预测单个活动或优化产品组合的支出和收入的情况，并确定模型不准确的来源。 该报告包括：<ul><li>一个[!DNL PowerPoint]文件，其中包含过去7天的预测成本和实际成本、点击次数、每次点击成本(CPC)、收入、每次点击收入(RPC)和投资回报率(ROI)的摘要；上个月超支和支出不足竞价单位的汇总数据；显示成本模型准确性、收入模型准确性以及上个月预测成本、点击次数、CPC、收入、RPC和ROI与实际值的趋势图；按点击级别划分的模型准确性；支出不足或支出最多的竞价单位；以及提高模型准确性的建议。</li><li>[!DNL Excel]文件，其中包含每个关键字的模型精确度和按天计算的模型精确度。</li></ul>此分析提供的详细信息多于项目组合级别模型准确性报告（可从[!UICONTROL Portfolios]视图中获得）。 |
| [!UICONTROL Normalized Sim (Combined)] | 返回多个项目组合中指定数量的目标支出级别（步骤）的最佳支出分配。 此分析基于指定时间段内的每周模拟，使用规范化的加权收入（现在称为“[目标值](/help/search-social-commerce/glossary.md#o-p)”）。 您可以生成a)每个选定项目组合的单个模拟，或b)具有相同目标和币种的多个项目组合之间的单个模拟。 仿真以电子表格形式呈现。<br><br>对于单个、多产品组合模拟，电子表格包含两个工作表：1)趋势图，显示每个目标支出级别（步骤）的标准化加权收入（现在称为“[目标值](/help/search-social-commerce/glossary.md#o-p)”）；2)表，显示每个适用支出级别（步骤）的一行。 对于个别项目组合模拟，该电子表格包括1)列出所有适用项目组合和时间期的摘要工作表，以及2)每个项目组合的两个工作表： a)显示每个目标支出级别（步骤）的标准化加权收入（现在称为“[目标值](/help/search-social-commerce/glossary.md#o-p)”）的趋势图，以及b)显示每个适用支出级别（步骤）一行的表格。 |
| [!UICONTROL Portfolio Launch] | （[!DNL PowerPoint]演示格式）标识项目组合是否已准备好启动（已更改为“已优化”状态）。 该报表包括预测绩效与实际绩效的比较；推荐的项目组合开始日期以及应排除在成本和收入预测之外的日期列表；成本、收入、每成本收入和随时间变化的转化关键词；有关过去两周支出受限的任何营销活动的信息；以及对launch或不启动的建议。 |
| [!UICONTROL Quality Score] | 显示过去90天内展示次数为[!DNL Google Ads]或[!DNL Microsoft Advertising]的关键字的质量分数趋势。 它包括a) [!DNL PowerPoint]文件和b) [!DNL Excel]文件，这些文件包含支出最高的100个关键字和（如果适用）质量分数较低的前100个关键字。<br><br>**注释：**<ul><li>当项目组合具有超过20,000个竞价单位时，只包括在过去30天（而不是90天）内多次点击的关键字。</li><li>包含许多关键字的数据的见解生成时间较长。</li></ul> |
| [!UICONTROL Query Cross Matching] | （[!DNL Google Ads]帐户）识别[!DNL Google Ads]与多个关键字匹配的搜索查询实例，并提供有关流量所定向目标的建议。 使用这些建议来提高关键词性能，从而改善模型准确性。<br><br>此分析包括交叉匹配查询、匹配的关键字和性能数据的电子表格；帮助您可视化交叉匹配查询和关键字之间关系的网络图；基础搜索查询报表；有关如何解释数据的信息。 |
| [!UICONTROL Settings Audit] | 指示您的项目组合是否按最佳实践进行配置。 它包括：<ul><li>一个[!DNL PowerPoint]文件，其中显示是否根据最佳实践配置了所有项目组合及其组件营销活动的关键设置、是否将任何营销活动分配给项目组合，以及偏离最佳实践的后果。</li><li>[!DNL Excel]文件，每个关键产品组合设置和关键促销活动设置具有单独的选项卡。 数据包括每个项目组合的项目组合设置，以及不符合最佳实践的每个营销活动的营销活动设置。</li></ul> |
| [!UICONTROL Time-of-day Analysis] | （仅适用于具有[!DNL Google Ads]搜索、展示或购物营销活动的项目组合）根据单个项目组合的小时表现，在一天中的不同时间建议[!DNL Google Ads]个营销活动级别的竞价修饰符（广告计划竞价修饰符）。<br><br>此分析包含一个[!DNL Excel]工作簿，其中包含[!UICONTROL Detailed Performance] （按营销活动显示的时间间隔列出的性能）和[!UICONTROL Recommended TBAs] （每个营销活动的推荐广告计划）的单个工作表。 您可以将[!UICONTROL Recommended TBAs]工作表直接导出到[!DNL Google Ads]编辑器。 分析还包括一个包含支持数据和解释的[!UICONTROL Powerpoint]文件。 |

>[!MORELIKETHIS]
>
>* [生成 [!DNL Advertising Insight]](insight-generate.md)
>* [查看或保存 [!DNL Advertising Insight]](insight-view-save.md)
>* [删除 [!DNL Advertising Insight]](insight-delete.md)
