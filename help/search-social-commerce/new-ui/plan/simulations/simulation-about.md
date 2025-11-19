---
title: 关于模拟
description: 了解项目组合模拟。
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 2fbefee2-f8f7-4b3d-a039-e1ca0236c61a
source-git-commit: 73528e2aa905216584d1aa294f5581d2bca88432
workflow-type: tm+mt
source-wordcount: '1182'
ht-degree: 0%

---

# 关于模拟

*Beta功能*

模拟报表显示项目组合在不同支出（成本）水平和相应的每日预算或其他目标下预计的边际成本与目标值、成本、点击次数和目标值。 您可以选择[自定义视图](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)以查看其他流量量度、模拟设置以及仅查看特定模拟类型（[!UICONTROL Weekly]或[!UICONTROL Custom]）。

<!-- Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## 模拟类型

* 每周自动模拟

* 自定义、用户生成的模拟

### 每周自动模拟

每周使用当前项目组合设置自动运行模拟报表。 每周自动模拟仅适用于项目组合为[已优化或处于活动状态](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md)的期间。

#### 每周下载的模拟

每个下载的每周模拟都包含一个工作簿。 每个工作簿包括20个步骤级别中每个步骤级别的目标，以及基于相应目标的目标中包含的预计成本、点击次数、加权收入（目标值）和转化量度。 对于前20个数据行，未应用约束；对于其余数据行，已应用约束。

#### 屏幕上的每周模拟详细信息

屏幕模拟详细信息显示项目组合级别的可视化和表格式洞察。 对于按促销活动、广告组、竞价单位或设备划分的数据，请改为下载[模拟](simulation-download.md)。

##### 图形视图

图形视图显示20个支出级别中每个支出目标的预期目标值或其他指定指标([!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->)。 目标中点已识别，您可以选择更改目标中点以查看使用该值的预测数据。 将光标悬停在图形中的任何点上可查看该点的数据。

您可以查看应用了约束和不应用了约束、应用了约束和不应用约束的数据。 查看考虑约束的数据时，应用的约束在图形上方标识。

##### 表格视图

该表视图显示20个支出级别中每个级别的目标支出。 它还包括每个支出水平组合目标中的相应估计成本、边际成本到目标值、点击次数、目标值和转化量度。 目标中点已识别，您可以选择更改目标中点以查看使用该值的预测数据。

您可以查看应用了约束和不应用了约束、应用了约束和不应用约束的数据。 查看考虑约束的数据时，应用的约束在图形上方标识。

##### 模拟设置

在图形或表的下方，模拟设置显示为只读。

##### Portfolio设置

要查看适用项目组合的只读设置，请单击右上角的&#x200B;**[!UICONTROL Portfolio Settings]**。

### 自定义、用户生成的模拟

您可以使用当前项目组合设置或使用自定义项目组合设置（应用或不应用竞价单位级别约束）为单个[优化或活动](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md)项目组合创建自定义模拟报告，以查看这些设置在不实际更改它们的情况下生成的结果。 例如，您可以创建一个自定义模拟，以查看使用不同支出策略或学习预算的效果，而无需考虑对项目组合中竞价单位的有效限制。 您可以查看项目组合、促销活动、竞价单位和设备级别的预计性能。

#### 下载的自定义模拟

每个下载的自定义模拟都包含一个工作簿。 每个工作簿都包含每个指定实体层模拟（项目组合、促销活动、广告组、竞价单位）的一个工作表，前提是该层的数据可用。 指定设备级数据时，每个工作表都包含一个[!UICONTROL Device]列。 每个工作表都包含一行，其中包含每个适用实体的数据以及20个步骤中每个步骤的设备类型（例如，每个活动包含一行）（在为报表指定时）。 每一行中的数据包括基于相应目标的预测边际成本 — 收入比、成本、点击次数、加权收入（目标值）、设备类型和目标中包含的转化量度。 组合层工作表还包括步骤层的目标，实体层工作表包括广告网络、帐户、促销活动和（如果适用）广告组。   <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

#### 屏幕自定义模拟详细信息

屏幕模拟详细信息显示项目组合级别的可视化和表格式洞察。 对于按促销活动、广告组、竞价单位或设备划分的数据，请改为下载[模拟](simulation-download.md)。

#### 图形视图

图形视图显示指定数量的模拟支出级别（步骤）的支出目标的预期目标值或其他指定量度([!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->)。 确定目标中点。 将光标悬停在图形中的任何点上可查看该点的数据。

当考虑约束建立仿真时，在图形上方识别应用的约束。

##### 表格视图

该表视图显示每个指定数量的模拟支出层（步骤）的目标支出。 此外，它还会显示每个支出级别组合目标中的相应估计成本、边际成本到目标值、点击次数、目标值和转化量度。 确定目标中点。

当考虑约束建立仿真时，在图形上方识别应用的约束。

##### 模拟设置

在图形或表的下方，模拟设置显示为只读。

##### Portfolio设置

要查看适用项目组合的只读设置，请单击右上角的&#x200B;**[!UICONTROL Portfolio Settings]**。

## [!UICONTROL Simulations]视图

[!UICONTROL Simulations]视图列出每周模拟和自定义模拟。 管理员和其他一些用户类型<!-- Verify which -->可以查看其他用户创建的自定义模拟。 所有其他用户只能查看他们创建的自定义模拟。

数据表包括每个模拟的进度；为每行填充的[!UICONTROL Target Midpoint]列；以及成本/展示次数/点击次数/目标值预测、实际值和准确度的列。 您可以选择添加其他自定义列（包括提升量度，例如实际目标值除以成本）。

### 可用操作 {#simulations-actions}

* [自定义视图](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)以包含其他量度，包括预计展示次数；实际成本、点击次数、展示次数和目标值；成本与目标值；成本准确度、点击准确度和目标值准确度；以及预测目标值与实际目标值与成本与目标值之间的差值（增量）。 您还可以包含大多数模拟设置和模拟类型（[!UICONTROL Custom]或[!UICONTROL Weekly]）的列。

* [为单个项目组合生成或重新运行自定义模拟](simulation-create.md)。 您可以创建新模拟，也可以重新生成列表中的现有模拟。

* [在屏幕上查看每周或自定义模拟](simulation-view.md)。

* [将每周和自定义模拟](simulation-download.md)下载为ZIP文件中的[!DNL Microsoft Excel]工作簿。

* 使用[!UICONTROL Spend Planner]按钮，打开旧版支出推荐工具，该工具可帮助您识别项目组合间的最佳支出分配。

## 最佳实践

在以下情况下监控模拟报告：

* 在启动项目组合以使用相应的项目组合设置估计可预期的性能之前；至少使用两周的数据。 如果仿真结果显示性能低于您根据所包含营销活动的历史数据所预期的性能，请在启动项目组合之前调查并解决这些问题。

* 在对项目组合进行任何重大更改后，例如添加营销策划或更改目标。 如果您更改项目组合的建模开始日期、转化量度的权重或目标的单击值，则等到第二天17:00 PST之后再运行模拟，此时更新的成本和收入模型可用。

* 定期监控转化量度级别的性能趋势。

>[!MORELIKETHIS]
>
>* [运行或重新运行模拟](simulation-create.md)
>* [查看模拟详细信息](simulation-view.md)
>* [下载模拟](simulation-download.md)
