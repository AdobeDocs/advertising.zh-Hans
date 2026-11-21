---
title: （新UI）Advertising分析
description: 了解如何配置和查看advertising insight功能板的模型准确性、性能、模拟、预算限制和转化。
feature: Search Advertising Insights
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bc8b5578-58f6-5342-a640-fce94e5ff4a7
    internal-label: Search Advertising Insights
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: f2335fa20fd8685b13b5bcebe63c21c7e3600551
workflow-type: tm+mt
source-wordcount: '1217'
ht-degree: 0%
---
# （新UI）Advertising分析

Advertising分析可提供可视化、可操作的数据，帮助您评估项目组合性能、识别优化问题并比较转化数据。 每个insight都会按需生成，并显示为屏幕仪表板。

**[!UICONTROL Reports]>[!UICONTROL Insights]**&#x200B;视图在&#x200B;**[!UICONTROL Dashboards]**&#x200B;下显示可用的分析。 页面标题为&#x200B;**[!UICONTROL Advertising Insights]**。

>[!NOTE]
>
>本页介绍了测试版新用户界面中的insight功能板。 可用性取决于您的访问权限以及对所选广告商可用的分析。 [旧版Advertising Insights](/help/search-social-commerce/legacy-ui/advertising-insights/insight-about.md)包含一组用于生成文件的其他分析和过程。

## 见解类型 {#insight-types}

| insight | 描述 |
| --- | --- |
| [!UICONTROL Model Accuracy] | 确定Search、Social和Commerce预测产品组合成本和收入的有效性。 您可以在项目组合、广告网络和营销策划级别审查模型的准确性。 |
| [!UICONTROL Performance Insights] | 比较项目组合在优化状态更改、目标更改或指定日期前后的绩效。 仪表板包括性能摘要、影响优化的更改的审核、活动比较、趋势和目标值分析。 |
| [!UICONTROL Portfolio Simulation Analysis] | 将现有自定义模拟与实际性能进行比较。 您可以审查项目组合和活动数据，分析模拟准确性，以及探索不同目标支出级别的估计性能。 |
| [!UICONTROL Campaign Budget Cap Analysis] | 指示投资组合的支出是否受营销活动预算上限限制。 仪表板包括上限支出、受影响的营销活动、预计损失的展示次数、每日和每周日期趋势，以及项目组合设置的建议。 |
| [!UICONTROL Modeled Conversions] | 将Adobe转化值与广告网络报告的值（包括模型化的数据）进行比较。 您可以分析帐户、项目组合或营销活动，并将Adobe测量值和Adobe测量值和模型化值与发布者报告的值进行比较。 |
| [!UICONTROL Delayed Revenue Analysis] | 测量转化滞后时间（在广告点击或浏览到后续转化之间经过的时间），并显示其对目标值、投资回报率(ROI)和模型准确性的影响。 该分析仅适用于具有基于点击或浏览式收入归因的项目组合。 |

## 生成insight {#insight-generate}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Insights]**。

1. 单击要生成的insight。

1. 在&#x200B;**[!UICONTROL Configure]**&#x200B;面板中，指定[insight设置](#insight-settings)。

1. 单击&#x200B;**[!UICONTROL Generate Insight]**。

   配置面板关闭，仪表板显示分析。

1. 查看[insight结果](#insight-results)。

要更改设置，请单击&#x200B;**[!UICONTROL Configure]**，更改值，然后再次单击&#x200B;**[!UICONTROL Generate Insight]**。 要返回到insight列表，请在痕迹导航中单击&#x200B;**[!UICONTROL Analysis List]**。

## insight设置 {#insight-settings}

### 模型精度 {#model-accuracy-settings}

* **[!UICONTROL Portfolios]：** Select one项目组合。

* **[!UICONTROL Choose Revenue Type]：** Select **[!UICONTROL Actual Revenue]** （默认）或&#x200B;**[!UICONTROL Delayed Revenue]**。

* **[!UICONTROL Date Range]：** Select要分析的日期。 查看[日期范围设置](#date-range-settings)。

### 性能分析 {#performance-insights-settings}

* **[!UICONTROL Portfolios]：** Select one项目组合。

* **[!UICONTROL Revenue Type]：** Select **[!UICONTROL Actual Revenue]** （默认）或&#x200B;**[!UICONTROL Delayed Revenue]**。

* **活动日期：** Select要比较绩效的日期类型：

  * **[!UICONTROL Optimization Status Change (last 90 days)]** （默认）： Select具有项目组合的可用优化状态更改日期。

  * **[!UICONTROL Objective Change Date (last 90 days)]：** Select为项目组合提供了一个可用的目标更改日期。

  * **[!UICONTROL Specific Date]：**&#x200B;使用日期选取器指定日期。

  在配置比较时段之前，Select事件日期。 如果所选项目组合没有可用的事件日期，则可以使用&#x200B;**[!UICONTROL Specific Date]**。

* **[!UICONTROL Pre Days]：**&#x200B;指定事件日期之前的时段：

  * Select **[!UICONTROL 7]** （默认）、**[!UICONTROL 14]**&#x200B;或&#x200B;**[!UICONTROL 30]**。

  * Select **[!UICONTROL Pre Start Date]**&#x200B;并指定&#x200B;**[!UICONTROL Custom Pre Date]**。

  * Select **[!UICONTROL Custom Pre Days]**&#x200B;并输入正天数。

* **[!UICONTROL Post Days]：**&#x200B;指定事件日期之后的时间段：

  * Select **[!UICONTROL 7]** （默认）、**[!UICONTROL 14]**&#x200B;或&#x200B;**[!UICONTROL 30]**。

  * Select **[!UICONTROL Post End Date]**&#x200B;并指定&#x200B;**[!UICONTROL Custom Post Date]**。

  * Select **[!UICONTROL Custom Post Days]**&#x200B;并输入正天数。

  两个比较期间均不包括事件日期本身。

* **[!UICONTROL Date Exclusion]：**（可选）从分析中排除日期：

  1. 单击&#x200B;**[!UICONTROL Select Dates]**。

  1. Select要排除的日期：

     * 单击单个日期以将其选中或取消选中。

     * 在单击选择范围时按住&#x200B;**[!UICONTROL Shift]**。

     * 要删除所有排除项，请单击&#x200B;**[!UICONTROL Clear All]**。

  1. 完成后，单击&#x200B;**[!UICONTROL Done]**。

### Portfolio仿真分析 {#simulation-settings}

* **[!UICONTROL Portfolios]：** Select一个包含现有自定义模拟的项目组合。

* **[!UICONTROL Simulation Date]：** Select要分析的模拟日期。 如果该日期有多个可用的模拟，则还应选择按名称显示的模拟。

  如果没有可用的自定义模拟，则在使用此insight之前[生成自定义模拟](/help/search-social-commerce/manage/portfolios/portfolio-create-simulation.md)。

* **[!UICONTROL Actual Days]：** Select **[!UICONTROL 7]** （默认）、**[!UICONTROL 14]**&#x200B;或&#x200B;**[!UICONTROL 30]**&#x200B;天的实际性能数据。 要指定其他数字，请选择&#x200B;**[!UICONTROL Enter Actual Days]**&#x200B;并输入1-90之间的值。

* **[!UICONTROL Type]：** Select **[!UICONTROL Transaction Date]** （默认）或转化归因的&#x200B;**[!UICONTROL Click Date]**。

### 营销活动预算上限分析 {#budget-cap-settings}

* **[!UICONTROL Portfolio]：** Select one项目组合。

* **[!UICONTROL Date Range]：** Select要分析的日期。 查看[日期范围设置](#date-range-settings)。

### 模型化转化 {#modeled-conversions-settings}

* **[!UICONTROL Analysis Level]：** Select **[!UICONTROL Account]**、**[!UICONTROL Portfolio]** （默认）或&#x200B;**[!UICONTROL Campaign]**。

* **[!UICONTROL Accounts]**、**[!UICONTROL Portfolios]**&#x200B;或&#x200B;**[!UICONTROL Campaigns]：** Select分析级别的适用实体。 可选取多个图元。

* **[!UICONTROL Date Range]：** Select要分析的日期。 查看[日期范围设置](#date-range-settings)。

* **[!UICONTROL Adobe Conversion]：** Select要比较的Adobe转换属性。

* **[!UICONTROL Publisher Conversion]：** Select要比较的发布者转换属性。

  可用的转换属性取决于分析级别、选定的图元和日期范围。 进行比较需要两个转换属性。

### 延迟收入分析 {#delayed-revenue-settings}

* **[!UICONTROL Portfolios]：** Select一个具有基于点击或浏览收入归因的项目组合。

* **[!UICONTROL Date Range]：** Select要分析的日期。 查看[日期范围设置](#date-range-settings)。

### 日期范围设置 {#date-range-settings}

对于具有&#x200B;**[!UICONTROL Date Range]**&#x200B;设置的分析，请选择&#x200B;**[!UICONTROL Last 7 days]**（默认值）、**[!UICONTROL Last 14 days]**&#x200B;或&#x200B;**[!UICONTROL Last 30 days]**。

要指定其他句点，请选择&#x200B;**[!UICONTROL Custom Date]**&#x200B;并输入&#x200B;**[!UICONTROL Start Date]**&#x200B;和&#x200B;**[!UICONTROL End Date]**。 您可以选择从当前日期到最近90天内的日期。

## 查看insight结果 {#insight-results}

### 模型精度 {#model-accuracy-results}

查看项目组合详细信息并使用以下选项卡：

* **[!UICONTROL Portfolio]：**&#x200B;审核项目组合级别的模型准确性和预算比较。

* **[!UICONTROL Ad Network]：**&#x200B;按广告网络审查模型准确性和预算比较。

* **[!UICONTROL Campaigns]：**&#x200B;审查营销活动级别的模型准确性和目标与实际绩效。

* **[!UICONTROL Playground Beta]：**&#x200B;比较多个营销活动的模型准确性。

对于促销活动准确度图表，请选择&#x200B;**[!UICONTROL Comparison Options]**&#x200B;和&#x200B;**[!UICONTROL Campaign]**。 在&#x200B;**[!UICONTROL Playground Beta]**&#x200B;中，您可以选择多个营销策划。 单击&#x200B;**[!UICONTROL Table View]**&#x200B;可在图表及其基础数据之间切换。

### 性能分析 {#performance-insights-results}

仪表板显示&#x200B;**[!UICONTROL Pre Period]**&#x200B;和&#x200B;**[!UICONTROL Post Period]**、两个时段的汇总绩效指标以及项目组合详细信息。

**[!UICONTROL Audit Trail]**&#x200B;汇总了影响优化的因素的变化，包括组合预算、支出策略、最低活动支出和支出限制倍数。 当更改具有详细信息时，单击&#x200B;**[!UICONTROL View Details]**&#x200B;以检查更改。

使用&#x200B;**[!UICONTROL Comparative Overview]**、**[!UICONTROL Campaigns Comparison]**、**[!UICONTROL Trends & Patterns]**、**[!UICONTROL Deep Analysis]**&#x200B;和&#x200B;**[!UICONTROL Objective Value And Analysis]**&#x200B;选项卡浏览该比较。

### Portfolio仿真分析 {#simulation-results}

复查模拟详细信息并使用以下选项卡：

* **[!UICONTROL Portfolio]：**&#x200B;查看项目组合级别的模拟数据。 在此选项卡中：

  * **[!UICONTROL Simulation Data]**&#x200B;显示模拟量度和目标支出性能。

  * **[!UICONTROL Simulation Vs Actual]**&#x200B;比较模拟性能和实际性能。

  * **[!UICONTROL Try New Target]**&#x200B;允许您在&#x200B;**[!UICONTROL Explore Target Spend]**&#x200B;中输入目标支出以查看预计点击次数、成本和收入。 这是对预计绩效的分析；它不会改变投资组合的支出目标。

* **[!UICONTROL Campaigns]：**&#x200B;查看营销活动级别的模拟比较。

* **[!UICONTROL Accuracy Analysis]：**&#x200B;查看模拟准确性。

### 营销活动预算上限分析 {#budget-cap-results}

查看项目组合详细信息和摘要量度：

* **[!UICONTROL Total Capped Spend]：**&#x200B;达到营销活动预算时的天数支出百分比。

* **[!UICONTROL Capped Campaigns]：**&#x200B;至少达到其预算一次的营销活动数。

* 由于预算限制，**[!UICONTROL Est. Lost Impressions]：**&#x200B;预计展示次数已错过。

* **[!UICONTROL Peak Capping Day]：**&#x200B;一周中支出上限最多的时间。

**[!UICONTROL Spend on Capped Campaigns by Day]**&#x200B;和&#x200B;**[!UICONTROL Capped Spend by Weekday]**&#x200B;图表显示上限趋势。 查看&#x200B;**[!UICONTROL Capped Campaign Performance]**&#x200B;以了解促销活动详细信息，查看&#x200B;**[!UICONTROL Portfolio Settings Recommendations]**&#x200B;以了解建议的设置更改。

### 模型化转化 {#modeled-conversions-results}

查看选定实体和日期范围的以下表：

* **[!UICONTROL Adobe Measured vs Publisher Conversions]：**&#x200B;将Adobe直接测量的转化值与发布者报告的值（包括测量数据和模型化数据）进行比较。

* **[!UICONTROL Adobe Modeled vs Publisher Conversions]：**&#x200B;将Adobe测量和模型化的转化值与发布者报告的值进行比较。

两个表都包含实体名称和ID、Adobe值、发布者报告的值、绝对差异和百分比差异。

如果没有可用数据，请确认您选择了转换属性，并且选定实体和日期范围存在相应数据。

### 延迟收入分析 {#delayed-revenue-results}

**[!UICONTROL Key Insights Summary]**&#x200B;显示预期的加权收入（现在称为“[目标值](/help/search-social-commerce/glossary.md#o-p)”）、ROI和模型准确性信息。

**[!UICONTROL Conversion Lag Breakdown by Revenue Property]**&#x200B;部分显示每个收入属性在第0天以及第3、7、14和28天实现的转化的百分比。

在&#x200B;**[!UICONTROL Performance Over Time]**&#x200B;中，选择&#x200B;**[!UICONTROL Objective Value]**、**[!UICONTROL ROI]**&#x200B;或&#x200B;**[!UICONTROL Model Accuracy]**&#x200B;比较点击日期、交易日期和预期性能。 单击&#x200B;**[!UICONTROL Table View]**&#x200B;可在图表及其基础数据之间切换。

在&#x200B;**[!UICONTROL Metrics Definitions]**&#x200B;中，单击&#x200B;**[!UICONTROL Show]**&#x200B;以获取分析中使用的日期和量度的说明，或单击&#x200B;**[!UICONTROL Hide]**&#x200B;以折叠这些日期和量度。

如果分析不适用，请选择具有基于点击或浏览式收入归因的项目组合。 如果没有可用数据，请验证所选项目组合和日期范围是否存在数据。
