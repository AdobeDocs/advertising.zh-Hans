---
title: DSP如何优化您的活动
description: 了解DSP如何优化营销活动中的包。
feature: DSP Optimization
exl-id: 92d411cf-4307-4449-97b4-da3817f2a0b4
source-git-commit: de2a2a097802cc4a7b5ac63bee2eb326895e70f1
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 0%

---

# Advertising DSP如何优化您的活动

此页概述由[!DNL Adobe AI]提供支持的DSP优化引擎如何优化营销活动中的包。 有关如何手动优化促销活动的提示和技巧，请与Adobe客户团队联系。<!-- add link to trading playbook if we add it to help -->

包优化目标在两个级别运行：

* 对于每个包：DSP会根据投放位置对选定KPI的表现，将预算分配给包中的每个投放位置。

* 对于程序包中的每个投放/拍卖： DSP计算每个投放的每个拍卖的实时经济KPI值，然后使用此值确定竞价。

  >[!NOTE]
  >
  >经济价值可能会根据配售的支出水平得到大幅加权。 如果配售落后于其支出目标，那么它就可以购买质量较低的拍卖。 如果职位安排能够轻松达到支出目标，那么焦点就会转向更高质量的拍卖。

## 包优化

DSP可以从两个基本方面优化您的投放，其中有20个变体可供使用，以便与您的特定性能目标保持一致。 您可以选择：

* 区分性能速率的优先级

* 优先考虑兼顾成本效益与性能率

请参阅[优化目标以及如何使用它们](optimization-goals.md)以确定哪个优化目标可以帮助您实现KPI。

### 排定性能速率优先级的程序包

对于优先考虑性能率的优化目标，DSP会预测每次拍卖的性能，并始终按最高出价竞价。 适用的优化目标示例包括[!UICONTROL Highest Viewability Rate]、[!UICONTROL Highest Clickthrough Rate]等。

此优化模式在以下情况下可正常工作：

* 您已经知道有效/可接受的CPM级别（例如，历史基准）。

* 如果您在缩放时遇到问题，那么您愿意手动调整每个投放位置的[!UICONTROL Max Bid]。

* 你将规模置于效率之上。

#### 步调逻辑 {#pacing-logic-performance}

* 如果支出保持节奏，竞价就会变得更加有选择性，这样一来，你只会竞拍那些预计会获得高绩效率的拍卖。

* 如果支出落后于节奏，竞价就会变得不那么有选择性，这样你就能在预计表现会较低的拍卖会上竞价，以赶上节拍目标。

#### 结算价格/竞价底纹 {#clearing-price-performance}

在执行步调逻辑后，DSP通过清算价格预测模型运行提议的竞价。 如果预测指示出价可以以最小的获胜率下降而降低，则根据预测降低出价。

### 优先考虑成本效益与性能比率平衡的软件包

对于某些优化目标，DSP会预测每个拍卖的表现并自动调整竞价，而不会超过投放位置的[!UICONTROL Max Bid]。 适用的优化目标示例包括[!UICONTROL Lowest CPM]、[!UICONTROL Lowest CPA]、[!UICONTROL Lowest Cost per View]、[!UICONTROL Lowest Cost per Click]等。

#### 步调逻辑 {#pacing-logic-balanced}

* 如果支出保持节奏，DSP就会对价格更加敏感，降低出价，从而用步调计划来抵消中标率。

* 如果还平衡了某个性能指标（除[!UICONTROL Lowest CPM]之外的所有目标），则预测的KPI将混合到竞价金额中。 因此，你竞拍的价位更高，而按“每笔成本”计算，这些拍卖的表现预计会更好。

* 如果支出落后于步伐，则DSP将降低价格敏感性，并调高出价（最高达[!UICONTROL Max Bid]）以抵消步调计划带来的中标率。

#### 结算价格/竞价底纹 {#clearing-price-balanced}

在执行步调逻辑后，DSP通过清算价格预测模型运行提议的竞价。 如果预测指示出价可以以最小的获胜率下降而降低，则根据预测降低出价。

## 置入优化

置入预竞价过滤器是确保强大性能的最严格方法。 DSP可跨不同的广告类型战略性使用预竞价过滤器，以实现每个包中不同投放位置的性能目标。 您可以同时将预竞价过滤器与包级别优化结合使用，也可以单独使用。

>[!NOTE]
>
>可用的预竞价过滤器因广告类型而异。 例如，对于标准显示放置，可按点进率和可视性进行过滤，而不按完成率过滤。

请参阅[位置级别预竞价筛选器及使用方法](optimization-pre-bid-filters.md)以确定哪个预竞价筛选器可以帮助您实现KPI。

>[!MORELIKETHIS]
>
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
>* [位置设置](/help/dsp/campaign-management/placements/placement-settings.md)
>* [优化目标及其使用方式](optimization-goals.md)
>* [投放位置级别预竞价筛选器及其使用方式](optimization-pre-bid-filters.md)
>* [性能疑难解答](/help/dsp/optimization/troubleshooting-performance.md)
