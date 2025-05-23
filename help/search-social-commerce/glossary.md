---
title: 术语表
description: 请参阅关键术语的定义。
exl-id: 87ce61b5-8340-4a6b-bd98-89ef73b2a9d8
feature: Search Introduction
source-git-commit: 58fab7afdca3468bf2bcca0f3120b3863af6eae2
workflow-type: tm+mt
source-wordcount: '2303'
ht-degree: 0%

---

# 术语表 {#glossary}

## A-B {#a-b}

**广告组：**&#x200B;营销活动的一组广告及其相关关键字、投放位置和产品组。

**广告变量：**&#x200B;广告组或广告策略中的任何广告。

**[AMO ID](/help/integrations/analytics/ids.md#amo-id)：**&#x200B;允许Adobe Advertising与Adobe Analytics共享促销活动相关数据的跟踪代码。 它以`s_kwcid=`开头。

**竞价单位：**&#x200B;投标单位的搜索、社交和Commerce搜索词。

* 对于CPC营销活动，这是搜索或内容营销活动的关键字及其匹配类型，购物营销活动的单元级别产品组（最低级别细分），或动态搜索广告营销活动的动态搜索目标。 当同一关键词和匹配类型组合、同一产品组或同一动态搜索目标在单个营销活动中的多个广告组内出现时，所有实例都被视为相同的竞价单位，因此具有相同的竞价。

* 对于具有[!DNL Maximize Clicks]、[!DNL Maximize Conversion Value]、[!DNL Maximize Conversions]、[!DNL Target Cost Per Acquisition]或[!DNL Target Return on Ad Spend]支出策略的营销活动，每个营销活动都是一个竞价单位。

* 对于[!DNL Yahoo! Display Network]上的促销活动（不使用关键字），广告组中的所有广告都具有相同的竞价并被视为相同的竞价单位。

**竞价单位约束：**&#x200B;请参阅“约束”。

## C-D {#c-d}

**营销活动：**&#x200B;单个广告帐户中的一组广告组，它们共享预算、时间范围、定位和其他设置。 **注意：** [!DNL Baidu]没有促销活动的概念，但Search、Social和Commerce为在Search、Social和Commerce中同步的现有[!DNL Baidu]帐户中的每一组相关广告组创建伪促销活动。

**区分大小写的字段：**&#x200B;区分大小写的字段或查询处理大写字母（如C）的方式与处理小写字母（如c）的方式不同。 例如，将Car视为与car不同的值。

**点击：**&#x200B;单个用户点击在线广告或在线广告中点击。

**点击回顾窗口：**&#x200B;广告商级别的设置，它指定在事件序列中发生付费点击后经过的天数，在该事件序列中，点击可归因于转化。

**点击时间：**&#x200B;具有唯一IP地址的最终用户首次点击广告网络中的广告的时间。

**点进率：** (CTR)点击次数除以广告的展示次数。 与搜索查询最相关的广告具有最高的点进率。

**点击跟踪URL：**&#x200B;跟踪模板或包含嵌入代码的目标URL，用于跟踪对关键字、广告变体或投放位置的点击。

**约束：** （具有组合的广告商；仅适用于标准组合中的竞价单位）用于对特定关键词或广告进行竞价的规则。 它覆盖了项目组合级别的任何限制以及推荐的竞价策略。

**转化：**&#x200B;最终用户点击广告后操作的完成，通常捕获为量度。 例如，登记和购买，它们可以表示数量或金额。 转化可以包含一个或多个交易事件，但“转化”和“交易”这两个术语通常可互换使用。

**转化跟踪：**&#x200B;转化跟踪使用Cookie来跟踪a)广告商在广告网络上的广告点击次数，以及b)广告商网站上的结果交易。

**成本准确性：** （具有组合项的广告商）组合的实际支出除以预测支出。 [模型准确度报表](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)指示用于优化的成本模型的准确度，[[!UICONTROL Model Accuracy]分析](/help/search-social-commerce/advertising-insights/insight-about.md)包含更多详细信息，以及提高模型准确性的建议。

**成本模型：**（具有产品组合的广告商）搜索、社交和Commerce技术，它使用历史数据和数学预测技术来预测成本量、赢得每个职位或位置所需的出价以及每个出价单位的CPC（搜索）或CPM（显示）。

**成本模型覆盖率：**（具有产品组合的广告商）在过去七天内至少获得一次展示的CPC或eCPC促销活动中竞价单位的数量和/或百分比，以便优化功能可以构建成本模型。 并非所有竞价单位都有成本模型；具有成本模型的竞价单位计入成本模型覆盖范围。

**成本模型半衰期：**（具有投资组合的广告商）当前日期之前的天数，在此天数内，成本数据被视为较新，因此与成本模型更相关。

**每1000次展示的成本：** (CPM)每1000次展示的广告成本。 使用CPM定价模型的广告商通过展示次数而不是点击次数来付费。

**每次购置成本：** (CPA)广告成本除以转化次数。 也称为每次交易成本(CPT)或每次订单成本(CPO)。

**每次点击成本：** (CPC) 1)广告成本除以广告点击总数。 例如，如果您为一个广告展示花费了100 USD，并且该广告生成了10次点击，则每次点击成本为100 USD/10=10 USD/每次点击。 2)一种定价模型，在此模型中，每次广告点击都会向广告商收费。

**每订单成本：** (CPO)广告成本除以订单数。 也称为每次收购成本(CPA)或每次交易成本(CPT)。

**每笔交易成本：** (CPT)广告成本除以交易数。 也称为每次收购成本(CPA)。

**CPA：**&#x200B;请参阅“每次购置成本”。

**CPC：**&#x200B;请参阅“每次点击成本”。

**CPM：**&#x200B;请参阅“每1000次展示的成本”。

**CPO：**&#x200B;请参阅“每订单成本”。

**CPT：**&#x200B;请参阅“每笔交易的成本”。

**CSV：**&#x200B;包含逗号分隔值(CSV)的文件格式。

**CTR：**&#x200B;请参阅“点进率”。

## E-F {#e-f}

**eCPM：**&#x200B;有效的CPM，或在指定日期范围内每1000次展示所支付的平均成本。 可以为CPM或CPC营销活动计算eCPM值。

## G-H {#g-h}

**半衰期：**&#x200B;将数量减少到其初始值的一半所需的时间。 对于每个项目组合，您可以指定半衰期以指示数据与成本模型和收入模型相关的时间。
请参阅“成本模型半衰期”和“收入模型半衰期”。

## I-J {#i-j}

**展示：**&#x200B;网页、移动应用或其他投放媒体上的单次广告显示。 用户不必查看或单击广告，即可将其计为展示。

**展示回顾窗口：**（仅限显示和社交营销活动）广告商级别的设置，它指定在广告展示出现后，展示可以归因于转化的天数。

**展示次数覆盖权重：**&#x200B;转化值中用于归因于展示次数的指定百分比，该展示次数在客户端的展示次数回顾时间范围内（当转化前同时有付费点击次数和展示次数时）。 当转化之前只有展示时，广告商的展示权重而不是展示覆盖权重应用于展示。

## K-L {#k-l}

**关键字：**&#x200B;与广告关联的单词或短语。

**关键字约束：**&#x200B;请参阅“约束”。

**标签分类：**&#x200B;一种将帐户组件分组为有意义的集的方法。 标签分类可以包含多个标签值，这些值表示属性。 例如，“地域”标签分类可能包括不同地理区域的值。

**标签值：**&#x200B;标签分类的元素。 它可以作为标记分配给广告促销活动和促销活动实体，因此您可以按标签筛选性能数据和报表，或者对与标签关联的竞价单位配置可选限制。

**登陆页面URL：**&#x200B;最终用户单击广告时打开的广告商网页的URL。

## M-N {#m-n}

**边际成本：**&#x200B;当数量按单位变化时，总成本的变化。

**边际成本 — 目标值：**&#x200B;将目标值增加一(1)所需的成本变化。 其值与旧版列“边际成本与收入”的值相同。

**匹配类型：**&#x200B;指定搜索词与广告匹配方式的选项。 选项因广告网络而异。

**最低出价：** 1)每次展示或每1000次展示要支付的最低金额。 2)对于搜索关键词，根据给定关键词的质量分数，要求的最低竞价。 为了让关键字显示广告，最低出价通常是每次点击可支付的最低金额。

**模型准确性：** （拥有产品组合的广告商）用于优化产品组合出价、促销活动预算和出价策略目标的成本模型和收入模型的准确性百分比。 请参阅“成本模型”、“成本准确性”、“收入模型”和“收入准确性”。

## O-P {#o-p}

**目标：**（具有产品组合的广告商）客户为满足特定产品组合或展示营销活动的业务目标（如实现最大利润或达到特定销售目标）而设置的目标。 目标包含要为组合跟踪和优化的转化量度，以及这些量度的相对权重。 所计算的投资组合的总加权转化称为“目标值”。

**目标值：** （具有产品组合的广告商）根据产品组合当前目标计算的总加权转化率，包括：

* 所有转化，同时要考虑a)分配给项目组合目标中每次转化的权重，以及在适用时b)显示显示显示到达次数的显示到达权重。

* 所有点击，优化功能将单次转化考虑在内，并根据目标的点击值进行加权。

其值与旧版列“加权收入”的值相同。

**优化功能：**（具有组合项的广告商）搜索、社交和Commerce关键词竞价技术，可根据组合的业务目标确定组合的最佳竞价和预算管理策略。

**孤立事务：**&#x200B;无法与特定关键字或广告关联的事务事件。

**像素：**&#x200B;为跟踪目的而嵌入到网页上的透明、逐像素图像。 Adobe Advertising转化跟踪标记包括HTML图像像素或JavaScript ，用于跟踪点击及其产生的交易。

**投放位置：**&#x200B;显示网络上可显示广告的位置。 它可以是整个网站、网站的子集或特定页面上的广告位置。

**项目组合：**&#x200B;一组针对单个业务目标和绩效目标优化的广告营销活动及其关联的竞价单位。

**POS：**&#x200B;支出百分比

**PPC：**&#x200B;请参阅“每次点击付费”。

**属性：**&#x200B;请参阅“转化量度”。

**属性时间：**&#x200B;发生单个转化事件的时间。 当事件包含相关的后续事件时（例如，客户首先注册免费试用，然后订阅付费服务），每个事件都有自己的属性时间。

## Q-R {#q-r}

**质量分数：**&#x200B;广告网络分配给您其中一个关键字的分数，用于确定其竞价和广告位置。 它是根据关键字与其相关广告的相关性、与用户的搜索查询、关键字的点进率等因素计算的。

**重定向URL：**&#x200B;在广告商的登陆页面之前或相反，将用户发送到另一服务器的目标URL的一部分。

**投资回报率：** (ROI)收入减去成本。

**收入准确性：** （具有项目组合的广告商）项目组合的实际收入除以预测收入。 [模型准确性报表](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)指示用于优化的收入模型的准确性，[[!UICONTROL Model Accuracy]分析](/help/search-social-commerce/advertising-insights/insight-about.md)包含更多详细信息，以及提高模型准确性的建议。

**收入模型：**（具有产品组合的广告商）搜索、社交和Commerce技术，它根据点击数据（搜索和社交）或展示数据（显示）以及广告商的转化数据，预测每个竞价单位的转化率和预计回报。

**收入模型覆盖率：** （具有投资组合的广告商）具有收入模型的投资组合中竞价单位的数量和/或百分比。 竞价单位可以具有收入模型，即使它们没有收到收入但收到了展示次数。

**收入模型半衰期：**（具有项目组合的广告商）当前日期之前的天数，收入数据会被视为较新，因此与收入模型更相关。

**ROI：**&#x200B;请参阅“投资回报率”。

## S-T {#s-t}

**模拟：** （具有项目组合的广告商）Portfolio建模，使用历史数据估计项目组合可预期的不同支出级别和相应每日预算的点击和转化次数。

**支出策略：** （具有投资组合的广告商）为优化投资组合的关键字/广告竞价而选择的策略。

**`s_kwcid`：**&#x200B;请参阅“AMO ID”。

**跟踪模板：** （仅具有最终URL的帐户）跟踪模板或跟踪URL，它指定所有登出域重定向和跟踪参数，并将最终/高级URL嵌入到参数中。 对于Adobe Advertising转化跟踪（在Campaign设置包括&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot;时应用），Search、Social和Commerce会在您保存记录时自动为其自己的重定向和跟踪代码添加前缀。

**跟踪URL：**&#x200B;添加了跟踪模板或目标URL以及额外的参数，用于跟踪有关广告点击的信息。 它可以包括一个重定向URL，用于在将用户重定向到广告商的登陆页面之前，先将用户发送到跟踪服务器。

**事务：**&#x200B;在线或离线发生的任何可跟踪事件。 可以将多个交易事件作为同一交易或转换的一部分一起跟踪；例如，在线信息请求加上结果的电话订单可被视为购买的组成部分。 “交易”和“转化”这两个术语经常互换使用。 事务由事务ID表示，并具有一个或多个与其关联的属性。

**交易ID：**&#x200B;广告商指定的标识交易的ID。 当一个事务包含多个事件时，它们都具有相同的事务ID。

**事务属性：**&#x200B;请参阅“转化”。

**事务时间：**&#x200B;点击或展示转换为事务的时间。 当交易由多个交易事件组成时（例如，当客户首次注册免费试用并稍后订阅付费服务时），交易时间来自链中的第一个事件（注册免费试用）。

**TSV：**&#x200B;包含制表符分隔值(CSV)的文件格式。

## U-V {#u-v}

**显示到达：** （显示广告和社交广告）用户未点击广告即导致转化的广告展示（或展示次数字符串）。

**显示到达权重：**（仅限显示和社交营销活动）广告商级别的设置，它指定要归因于显示到达转化的权重，以百分比表示，该权重要相对于归因于基于点击的转化的权重。

## W-X {#w-x}

**加权目标：**&#x200B;请参阅“目标”。

**加权收入：**&#x200B;请参阅“目标值”。

**XLS**&#x200B;或&#x200B;**XLSX**： [!DNL Microsoft Office Excel]工作簿的二进制文件格式。

## Y-Z {#y-z}
