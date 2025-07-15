---
title: 关于模拟
description: 了解项目组合模拟。
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# 关于模拟

*Beta功能*

模拟报表显示项目组合在不同支出（成本）水平和相应的每日预算或其他目标下预计的边际成本与目标值、成本、点击次数和目标值。 您可以选择自定义视图<!-- add link -->，以查看其他流量量度、模拟设置以及仅特定模拟类型（[!UICONTROL Weekly]或[!UICONTROL Custom]）。

<!-- Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## 模拟类型

* **每周自动模拟：**&#x200B;使用当前项目组合设置每周自动运行模拟报告。 每周自动模拟仅适用于项目组合为[已优化或处于活动状态](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md)的期间。

  每个下载的每周模拟都包含一个工作簿。 每个工作簿包括20个步骤级别中每个步骤级别的目标，以及基于相应目标的目标中包含的预计成本、点击次数、加权收入（目标值）和转化量度。 对于前20个数据行，未应用约束；对于其余数据行，已应用约束。

* **自定义、用户生成的模拟：**&#x200B;您可以使用当前项目组合设置或使用自定义项目组合设置为单个[优化或活动的](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md)项目组合创建自定义模拟报告，以查看这些设置在不实际更改它们的情况下生成的结果。 例如，您可以创建一个自定义模拟，以查看使用其他支出策略或学习预算<!-- Not available yet:  , or without considering active constraints on bid units in the portfolio-->的效果。 您可以查看项目组合、促销活动、竞价单位和设备级别的预计性能。 自定义模拟会从项目组合中继承限制支出设置。

  >[!NOTE]
  >
  > 新的自定义模拟表单使用与旧表单相同的设置，不同之处在于它从项目组合设置继承竞价单位约束信息。 您不能像在旧的自定义模拟设置页面中那样忽略竞价单位约束。

  每个下载的自定义模拟都包含一个工作簿。 每个工作簿都包含每个指定实体层模拟（项目组合、促销活动、广告组、竞价单位）的一个工作表，前提是该层的数据可用。 指定设备级数据时，每个工作表都包含一个[!UICONTROL Device]列。 每个工作表都包含一行，其中包含每个适用实体的数据以及20个步骤中每个步骤的设备类型（例如，每个活动包含一行）（在为报表指定时）。 每一行中的数据包括基于相应目标的预测边际成本 — 收入比、成本、点击次数、加权收入（目标值）、设备类型和目标中包含的转化量度。 组合层工作表还包括步骤层的目标，实体层工作表包括广告网络、帐户、促销活动和（如果适用）广告组。   <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

## [!UICONTROL Simulations]视图

[!UICONTROL Simulations]视图列出每周模拟和自定义模拟。 管理员和其他一些用户类型<!-- Verify which -->可以查看其他用户创建的自定义模拟。 所有其他用户只能查看他们创建的自定义模拟。

数据表包括每个模拟的进度；为每行填充的[!UICONTROL Target Midpoint]列；以及成本/展示次数/点击次数/目标值预测、实际值和准确度的列。 您可以选择添加其他自定义列（包括提升量度，例如实际目标值除以成本）。

### 可用操作 {#simulations-actions}

* [自定义视图](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)以包含其他量度，包括预计展示次数；实际成本、点击次数、展示次数和目标值；成本与目标值；成本准确度、点击准确度和目标值准确度；以及预测目标值与实际目标值与成本与目标值之间的差值（增量）。 您还可以包含大多数模拟设置和模拟类型（[!UICONTROL Custom]或[!UICONTROL Weekly]）的列。

* [为单个项目组合生成或重新运行自定义模拟](simulation-create.md)。 您可以创建新模拟，也可以重新生成列表中的现有模拟。

* [将每周和自定义模拟](simulation-download.md)下载为ZIP文件中的[!DNL Microsoft Excel]工作簿。

* 使用[!UICONTROL Spend Planner]按钮，打开旧版支出推荐工具，该工具可帮助您识别项目组合间的最佳支出分配。

## 最佳实践

在以下情况下监控模拟报告：

* 在启动项目组合以使用相应的项目组合设置估计可预期的性能之前；至少使用两周的数据。 如果仿真结果显示性能低于您根据所包含营销活动的历史数据所预期的性能，请在启动项目组合之前调查并解决这些问题。

* 在对项目组合进行任何重大更改后，例如添加营销策划或更改目标。 如果您更改了项目组合的建模开始日期、转化指标的权重或目标的单击值，则等到第二天17:00 PST之后再运行模拟，此时更新的成本和收入模型可用。

* 定期监控转化量度级别的性能趋势。

>[!MORELIKETHIS]
>
>* [运行或重新运行模拟](simulation-create.md)
>* [下载模拟](simulation-download.md)
