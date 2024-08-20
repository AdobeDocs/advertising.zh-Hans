---
title: 包设置
description: 请参阅有关可用包设置的说明。
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: f7332ae243daed3fcc45b69a8d71fff74d7caaeb
workflow-type: tm+mt
source-wordcount: '1060'
ht-degree: 0%

---

# 包设置

## [!UICONTROL Basic Details]

**[!UICONTROL Name]：**&#x200B;包名称。 最大长度为60个字符。

**[!UICONTROL Description]：**（可选）包的描述。

**[!UICONTROL 3rd Party Billed Fees]：**（可选）要作为不可记帐成本跟踪的静态第三方费用：

* **[!UICONTROL CPM]：**&#x200B;每1000次展示的成本(CPM)。

* **[!UICONTROL Description]：** CPM费用的说明。

>[!NOTE]
>
>可记帐费用反映在[!UICONTROL Net CPM]指标中。

您可以在[放置级别](/help/dsp/campaign-management/placements/placement-settings.md)覆盖包级别设置。

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]：** （现有包的只读模式）在哪个级别占位和限制包中的投放位置：

* **[!UICONTROL Package level pacing]：**&#x200B;此步调策略的操作方式是作为&#x200B;*组*&#x200B;对所有包含的投放位置进行步调和设置上限。 此策略可确保对给定包中的所有版面进行整体优化，根据性能和规模将支出分配到选定的关键绩效指标(KPI)。

* **[!UICONTROL Placement level pacing]：**&#x200B;此步调策略的操作方式是通过对所有包含的投放位置&#x200B;*单独进行步调和设置上限*。 最佳做法是，仅将此策略用于执行有保证的私人市场交易。

**[!UICONTROL Flight Dates]：**&#x200B;包的总开始日期和结束日期。 投放日期必须包含在营销活动投放日期中。

>[!NOTE]
>
>* 分配到此包的所有投放位置的投放日期必须包含在这些日期中。
> * 激活自定义飞行时，无法编辑程序包开始日期。

**[!UICONTROL Activate Custom Flighting]：**&#x200B;允许您在下面[!UICONTROL Flighting]部分中为包创建非偶数步调航班。 启用自定义灯光并保存包后，您既无法禁用自定义灯光，也无法编辑包的开始日期。

**[!UICONTROL Budget]：** （仅具有包级别步调的包）总预算上限和预算间隔。

对于具有自定义空闲的包，预算间隔始终为&#x200B;*[!UICONTROL All time]*。 对于没有自定义浮点的包，请指定预算间隔： *[!UICONTROL All time]、* *[!UICONTROL Daily]、* *[!UICONTROL Monthly]、*&#x200B;或&#x200B;*[!UICONTROL Weekly]*。

**[!UICONTROL Gross Budget]：** （仅具有包级别步调和动态利润管理的包）包持续时间的总预算上限。

**[!UICONTROL Optimization Goal]：** （仅具有包级别步调的包）包的优化目标。 在[优化目标上查看每个优化目标的说明及使用方法](/help/dsp/optimization/optimization-goals.md)。

**[!UICONTROL Custom Goal for Model Learning]：** （仅具有“[!UICONTROL Highest Return on Ad Spend]”和“[!UICONTROL Lowest Cost per Acquisition]”优化目标的包）包含用于计算CPA或ROAS量度的收入或转化事件的[自定义目标](/help/dsp/optimization/custom-goal.md)。 自定义目标可以选择除了用于包优化的CPA或ROAS量度之外，还包括要使用的其他加权上漏斗事件（例如页面访问次数和购物车添加）。 有关自定义目标的更多信息，包括为自定义目标创建的最佳实践和使用这些目标的营销活动，请参阅&quot;[自定义目标](/help/dsp/optimization/custom-goal.md)&quot;和&quot;[设置效果营销活动的最佳实践](/help/dsp/optimization/campaign-best-practices-performance.md)&quot;<!-- At some point, all of the objectives will be prefixed with "ADSP_," but probably that won't show up in the Custom Goal list in the DSP UI. -->

**[!UICONTROL Consider Only Click Conversions for Model Learning]：** （可选；仅优化目标为“[!UICONTROL Highest Return on Ad Spend]”和“[!UICONTROL Lowest Cost per Acquisition]”的包）告知优化模型仅从基于点击的转化中学习。 否则，优化模型会学习基于点击和基于展示的转化。

**[!UICONTROL Conversion Metric]：**（可选；仅具有“[!UICONTROL Highest Return on Ad Spend]”和“[!UICONTROL Lowest Cost per Acquisition]”优化目标的包）最终转化事件（如注册）或收入事件/销售金额（如购买和购买值），用于计算广告支出回报或每次收购成本。 从映射到所选自定义目标的所有主要事件（“目标量度”）的列表中进行选择。 如果列表为空，则编辑自定义目标以包含至少一个基础事件作为目标量度。

**[!UICONTROL Package Goal Type]：** （仅具有自定义优化目标的包）包的用途。 此设置可帮助确定如何优化包：

* *[!UICONTROL Prospecting]：*&#x200B;潜在客户包侧重于获取新客户。

* *[!UICONTROL Retargeting]：*&#x200B;重定位包侧重于重新公开以前的访客或客户。

* *[!UICONTROL Other]：*&#x200B;所有其他目的。

**[!UICONTROL Linked Package for Optimization Learnings Carryover]：** （仅具有自定义优化目标的包）其历史数据用作优化包的输入的另一个包。

**[!UICONTROL Target]：** （仅具有包级别步调的包）用于跟踪性能的目标目标。

>[!NOTE]
>
>此字段只是一个基准，不用于决策。

**[!UICONTROL Frequency Cap]：** （仅具有包级别步调的包）从包中可为独特设备、通用ID或人员（取决于为营销活动指定的[!UICONTROL Cross Device Level]和投放位置的[!UICONTROL Targeting]设置）提供广告的次数。 选项包括&#x200B;*[!UICONTROL Unlimited]*&#x200B;或每天、每周或每月的特定金额。

>[!NOTE]
>
>* 您可以在营销活动、包和投放级别设置频率上限。 DSP遵循营销活动层次结构中最严格的频率限制。
>* 最佳做法是在软件包级别为发现客户和重新定位设置频率上限。
> * 频率上限越高，支出和展示次数越多，但覆盖范围越窄。 频率上限越低，支出和展示次数就越少，但覆盖率却越高。

**[!UICONTROL Pace on]：** （仅具有包级别步调的包）步调所基于的内容：

* *[!UICONTROL Budget]：*（默认）此选项在分配的包预算内尽可能多地提供展示次数。

* *[!UICONTROL Impressions]：*&#x200B;此选项会一直提供展示次数，直到在指定时间间隔内达到指定的数量为止。 选择此选项时，请指定展示次数和间隔： *所有时间、* *[!UICONTROL Daily]、* *[!UICONTROL Monthly]、*&#x200B;或&#x200B;*[!UICONTROL Weekly]*。

**[!UICONTROL Flight pacing]：** （仅具有包级别步调的包）如何在整个飞行中安排广告投放的步调：

* *[!UICONTROL Even]：*&#x200B;在每个航班上均匀安排投放，目标是在航班的前半段投放的50%。

* *[!UICONTROL Slightly Ahead]：* （默认）加快投放，使其在飞行持续时间的半程完成55-65%。

* *[!UICONTROL Frontload]：*&#x200B;加速投放，使其在飞行中途完成65-75%。

* *[!UICONTROL Aggressive Frontload]：*&#x200B;加速投放，使其在飞行中途完成75-85%。

**[!UICONTROL Intraday pacing]：** （仅具有包级步调的包）如何在飞行中的每一天安排广告投放的步调：

* *[!UICONTROL Even]：*（默认）根据库存可用性来缩放投放。 通常，在拍卖量较高的白天，每小时会投放更多广告，而在早上和晚上投放的广告会更少。

* *[!UICONTROL ASAP]：*&#x200B;将投放速度加快到&#x200B;*Even*&#x200B;的两倍。

  >[!CAUTION]
  >
  >此选项可能会对性能产生负面影响。 仅在您完全优先考虑投放并花费超过性能优化的时间时才使用它。

## [!UICONTROL Flighting]

（具有包级别步调的包）包的投放期，包括包的总体[!UICONTROL Flight Dates]中的任何自定义投放期。 只有在[!UICONTROL Goals & Budget]部分中启用了[!UICONTROL Activate Custom Flighting]选项时，才能配置自定义航班。

**[!UICONTROL Automatically rollover remaining flight budget to next flight]：** （仅在启用[!UICONTROL Activate Custom Flighting]选项时可用）自动将上一个航班的任何剩余预算添加到下一个航班的现有预算。

在[!UICONTROL Packages]视图和[!DNL Package Name] > [!UICONTROL Flights]视图中，显示当前外部测试版目标的[!UICONTROL Interval Goal]字段包含任何滚动更新预算。

**[!DNL Flight N]：** （仅在启用[!UICONTROL Activate Custom Flighting]选项时可用）对于每个航班，指定开始日期、结束日期和目标支出目标。 要添加其他航班，请单击&#x200B;**[!UICONTROL Add Flight]**。

对于未启用“[!UICONTROL Automatically rollover remaining flight budget to next flight]”选项的现有包，您可以选择重新打开设置以在&#x200B;**[!UICONTROL Rollover]**&#x200B;列中为所有航班输入一个值，从而向下一个航班添加潜在的未用预算。

>[!MORELIKETHIS]
>
>* [关于包管理](package-about.md)
>* [创建包](package-create.md)
>* [编辑包](package-edit.md)
>* [将投放位置附加到包](package-attach-placement.md)
>* [查看包的更改日志](package-change-log.md)
>* 有关Campaign Management的[常见问题解答](/help/dsp/campaign-management/faq-campaign-management.md)
