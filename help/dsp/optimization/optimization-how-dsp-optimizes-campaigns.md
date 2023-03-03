---
title: DSP如何优化活动
description: 了解DSP如何优化营销活动中的包。
feature: DSP Optimization
exl-id: 92d411cf-4307-4449-97b4-da3817f2a0b4
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Advertising DSP如何优化营销活动

此页概述了DSP优化引擎的工作原理，该引擎由 [!DNL Adobe Sensei]，可优化营销活动中的包。 有关如何手动优化营销活动的提示和技巧，请与您的Adobe客户团队联系。 <!-- add link to trading playbook if we add it to help -->

包优化目标在两个级别运行：

* 对于每个包：DSP根据投放位置对选定KPI的表现，为包中的每个投放位置分配预算。

* 对于包中的每个投放/拍卖：DSP计算每个投放的每个拍卖的实时经济KPI值，然后使用此值确定竞价。

   >[!NOTE]
   >
   >经济价值可能会根据配售的支出情况得到大幅加权。 如果配售落后于其支出目标，那么它将获准购买质量较低的拍卖。 如果投放位置很容易达到其支出目标，那么它将专注于更高质量的拍卖。

## 包优化

DSP可以通过两种基本方式来优化投放，其中有20种变体可用于与特定的性能目标保持一致。 您可以选择：

* 优先考虑性能率

* 优先考虑成本效益与性能比率之间的平衡

参见 [优化目标及其使用方式](optimization-goals.md) 以确定哪个优化目标将帮助您实现KPI。

### 排定性能速率优先级的包

对于优先考虑性能率的优化目标，DSP会预测每次拍卖的性能，并始终以最高出价竞价。 适用的优化目标示例包括 [!UICONTROL Highest Viewability Rate]， [!UICONTROL Highest Clickthrough Rate]，等等。

此优化模式在以下情况下工作正常：

* 您已经知道有效/可接受的CPM级别（例如，历史基准）。

* 您愿意手动调整 [!UICONTROL Max Bid] 如果您在缩放时遇到困难，则针对每个投放位置。

* 你将规模置于效率之上。

#### 步调逻辑 {#pacing-logic-performance}

* 如果支出按部就班，竞价将变得更加有选择性，这样你只会竞拍那些预计会有高绩效率的拍卖。

* 如果支出落后于节奏，竞价就会变得不那么有选择性，这样你就能在预计表现会较低的拍卖会上竞价，以便赶上节拍目标。

#### 结算价格/竞价底纹 {#clearing-price-performance}

在执行步调逻辑后，DSP通过清算价格预测模型运行提议的竞价。 如果预测指示出出价可以以最小的获胜率下降而降低，则根据预测来降低出价。

### 将成本效益与性能比率进行平衡排定优先级的软件包

对于某些优化目标，DSP会预测每个拍卖的表现并自动调整竞价，而不会超过投放位置 [!UICONTROL Max Bid]. 适用的优化目标示例包括 [!UICONTROL Lowest CPM]， [!UICONTROL Lowest CPA]， [!UICONTROL Lowest Cost per View]， [!UICONTROL Lowest Cost per Click]，等等。

#### 步调逻辑 {#pacing-logic-balanced}

* 如果支出保持节奏，那么DSP就会对价格更加敏感，通过降低出价来换取中标率与节奏。

* 如果绩效指标也在平衡(所有目标，但 [!UICONTROL Lowest CPM])，则预测的KPI将混合到竞价金额中。 因此，你竞拍的价位更高，而根据“每笔成本”计算，这些拍卖的表现预计会更好。

* 如果支出跟不上节奏，那么DSP对价格的敏感度就会降低，而出价会提高，直至达到 [!UICONTROL Max Bid]，以通过步调计划来权衡获胜率。

#### 结算价格/竞价底纹 {#clearing-price-balanced}

在执行步调逻辑后，DSP通过清算价格预测模型运行提议的竞价。 如果预测指示出出价可以以最小的获胜率下降而降低，则根据预测来降低出价。

## 置入优化

置入预竞价过滤器是确保强大性能的最严格方法。 DSP可策略性地跨不同的广告类型使用预竞价过滤器，以实现每个包中各个投放位置的性能目标。 您可以与包级别优化同时使用预竞价过滤器，也可以单独使用。

>[!NOTE]
>
>可用的预竞价过滤器因广告类型而异。 例如，对于标准显示放置，您可以按点进率和可视性进行筛选，但不能按完成率进行筛选。

参见 [置入级别预竞价筛选器及其使用方式](optimization-pre-bid-filters.md) 以确定哪个预竞价过滤器将帮助您实现KPI。

>[!MORELIKETHIS]
>
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
>* [置入设置](/help/dsp/campaign-management/placements/placement-settings.md)
>* [优化目标及其使用方式](optimization-goals.md)
>* [置入级别预竞价筛选器及其使用方式](optimization-pre-bid-filters.md)
>* [性能疑难解答](/help/dsp/optimization/troubleshooting-performance.md)

