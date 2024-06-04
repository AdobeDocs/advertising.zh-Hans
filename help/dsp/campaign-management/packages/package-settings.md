---
title: 包设置
description: 请参阅有关可用包设置的说明。
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: 5d07300ab49b96daf392cb51f8936fa4c0cd20ce
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 0%

---

# 包设置

## [!UICONTROL Basic Details]

**[!UICONTROL Name]：** 包名称。 最大长度为60个字符。

**[!UICONTROL Description]：** （可选）包的描述。

**[!UICONTROL 3rd Party Billed Fees]：** （可选）作为不可计费成本跟踪的静态第三方费用：

>[!NOTE]
>
>可记帐费用反映在 [!UICONTROL Net CPM] 量度。
>
* **[!UICONTROL CPM]：** 每1000次展示的成本(CPM)。

* **[!UICONTROL CPM Description]：** CPM费用的描述。

您可以在以下位置覆盖包级别设置： [投放级别](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]：** （对于现有包为只读）在哪个级别上放置和限制包中的放置：

* **[!UICONTROL Package level pacing]：** 此步调策略的运行方式是步调和限制所有包含的投放位置，如下所示 *组*. 此策略可确保对给定包中的所有版面进行整体优化，根据性能和规模将支出分配到选定的关键绩效指标(KPI)。

* **[!UICONTROL Placement level pacing]：**  此步调策略的运行方式是步调和限制所有包含的投放位置 *单独*. 最佳做法是，仅将此策略用于执行有保证的私人市场交易。

**[!UICONTROL Flight Dates]：** 包的开始日期和结束日期。

要选择性地为包创建非匀速飞行，请选择 *[!UICONTROL *Activate Custom Flighting]**并在以下位置设置自定义航班： [!UICONTROL Flighting] 部分。 启用自定义灯光并保存包后，将无法禁用自定义灯光。

>[!NOTE]
>
>* 投放日期必须包含在营销活动投放日期中。 此外，分配给此包的所有投放位置的投放日期必须包含在这些日期中。
> * 激活自定义飞行时，无法编辑程序包开始日期。

**[!UICONTROL Budget]：** （仅具有包级别步调的包）总预算上限和预算间隔。

对于具有自定义飞行的包，预算间隔始终为 *[!UICONTROL All time]*. 对于没有自定义时间延迟的包，请指定预算间隔： *[!UICONTROL All time]，* *[!UICONTROL Daily]，* *[!UICONTROL Monthly]，* 或 *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]：** （仅限具有包级别步调和动态利润管理的包）包持续时间的总预算上限。

**[!UICONTROL Optimization Goal]：** （仅限具有包级别步调的包）包的优化目标。 请参见以下位置对每个优化目标的说明： [优化目标及其使用方式](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goal for Model Learning]：** (带有&quot;[!UICONTROL Highest Return on Ad Spend]”和“[!UICONTROL Lowest Cost per Acquisition]”仅限优化目标)A [自定义目标](/help/dsp/optimization/custom-goal.md) 包括用于计算CPA或ROAS指标的收入或转化事件。 自定义目标可以选择除了用于包优化的CPA或ROAS量度之外，还包括要使用的其他加权上漏斗事件（例如页面访问次数和购物车添加）。 有关自定义目标的最佳实践和使用它们的营销活动的更多信息，请参阅 [构建自定义目标的最佳实践](/help/dsp/optimization/custom-goal.md#custom-goal-best-practices) 和 [设置效果活动的最佳实践](/help/dsp/optimization/campaign-best-practices-performance.md).

**[!UICONTROL Consider Only Click Conversions for Model Learning]：** (可选；带有&quot;[!UICONTROL Highest Return on Ad Spend]”和“[!UICONTROL Lowest Cost per Acquisition]&quot;仅限优化目标)告知优化模型仅从基于点击的转化中学习。 否则，优化模型会学习基于点击和基于展示的转化。

**[!UICONTROL Conversion Metric]：** (可选；带有&quot;[!UICONTROL Highest Return on Ad Spend]”和“[!UICONTROL Lowest Cost per Acquisition]“仅限优化目标)最终转化事件（例如注册）或收入事件/销售金额（例如购买和购买值），用于计算广告支出回报率或每次购买成本。 从映射到所选自定义目标的所有主要事件（“目标量度”）的列表中进行选择。 如果列表为空，则编辑自定义目标以包含至少一个基础事件作为目标量度。

**[!UICONTROL Package Goal Type]：** （仅限具有自定义优化目标的包）包的用途。 此设置可帮助确定如何优化包：

* *[!UICONTROL Prospecting]：* 潜在客户包侧重于获取新客户。

* *[!UICONTROL Retargeting]：* 重新定位资源包侧重于重新公开以前的访客或客户。

* *[!UICONTROL Other]：* 所有其他目的。

**[!UICONTROL Linked Package for Optimization Learnings Carryover]：** （仅限具有自定义优化目标的包）另一个包，其历史数据用作优化包的输入。

**[!UICONTROL Target]：** （仅限具有包级别步调的包）用于跟踪性能的目标目标。

>[!NOTE]
>
>此字段只是一个基准，不用于决策。

**[!UICONTROL Frequency Cap]：** （仅限具有包级别步调的包）唯一设备、通用ID或人员(取决于指定的 [!UICONTROL Cross Device Level] 促销活动和投放位置的 [!UICONTROL Targeting] 设置)可以从包中提供广告。 选项包括 *[!UICONTROL Unlimited]* 或每天、每周或每月的特定金额。

>[!NOTE]
>
>* 您可以在营销活动、包和投放级别设置频率上限。 DSP遵循营销活动层次结构中最严格的频率限制。
>* 最佳做法是在软件包级别为发现客户和重新定位设置频率上限。
> * 频率上限越高，支出和展示次数越多，但覆盖范围越窄。 频率上限越低，支出和展示次数就越少，但覆盖率却越高。

**[!UICONTROL Pace on]：** （仅限具有包级别步调的包）步调基于什么步调：

* *[!UICONTROL Budget]：* （默认）此选项会在分配的资源包预算内尽可能多地提供展示次数。

* *[!UICONTROL Impressions]：* 此选项会一直提供展示次数，直到在指定间隔内达到指定数量为止。 选择此选项时，请指定展示次数和间隔： *所有时间，* *[!UICONTROL Daily]，* *[!UICONTROL Monthly]，* 或 *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]：** （仅限具有包级别步调的包）如何在整个航班中安排广告投放的步调：

* *[!UICONTROL Even]：* 每次飞行均采用相同的投放步长，目标是在飞行前半段投放的50%。

* *[!UICONTROL Slightly Ahead]：* （默认）加快投放，使其在飞行时间的半程完成55-65%。

* *[!UICONTROL Frontload]：* 加速投放，使其在飞行中途完成65-75%。

* *[!UICONTROL Aggressive Frontload]：* 加速投放，使其在飞行中途完成75-85%。

**[!UICONTROL Intraday pacing]：** （仅限具有包级别步调的包）如何在投放过程中的每天进行广告投放步调：

* *[!UICONTROL Even]：* （默认）根据库存可用性调整交付。 通常，在拍卖量较高的白天，每小时会投放更多广告，而在早上和晚上投放的广告会更少。

* *[!UICONTROL ASAP]：* 将投放速度提升到两倍 *平衡*.

  >[!CAUTION]
  >
  >此选项可能会对性能产生负面影响。 仅在您完全优先考虑投放并花费超过性能优化的时间时才使用它。

## [!UICONTROL Flighting]

(具有包级别步调和带&quot;[!UICONTROL Activate Custom Flighting]”已启用)整个中的自定义投放期限 [!UICONTROL Flight Dates] 指定于 [!UICONTROL Goals & Budget] 部分。

对于每个航班，输入开始日期、结束日期和目标展示次数。 要添加其他航班，请单击 **[!UICONTROL Add Flight]**.

>[!MORELIKETHIS]
>
>* [关于包管理](package-about.md)
>* [创建资源包](package-create.md)
>* [编辑包](package-edit.md)
>* [将投放位置附加到包](package-attach-placement.md)
>* [查看包的更改日志](package-change-log.md)
>* [关于Campaign Management的常见问题解答](/help/dsp/campaign-management/faq-campaign-management.md)
