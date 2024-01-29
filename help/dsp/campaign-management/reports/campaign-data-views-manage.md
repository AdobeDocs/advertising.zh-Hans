---
title: 管理Campaign数据视图
description: 了解如何自定义营销活动、包、投放位置和广告的数据视图。
feature: DSP Campaign Data Views
source-git-commit: 1ac58da2d538cc682161ebc944a0412ad4a8af17
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 0%

---

# 管理Campaign数据视图

您可以自定义在营销活动管理视图中显示的数据([!UICONTROL Campaigns]， [!UICONTROL Packages]， [!UICONTROL Placements]、和 [!UICONTROL Ads])。

## 管理数据可视化图表 {#data-visualizations-manage}

您可以为跨营销活动或单个营销活动的所有数据可视化更改量度和图表模式。 对单个营销活动的更改会应用于该营销活动的所有数据可视化图表，包括 [!UICONTROL Packages]， [!UICONTROL Placements]、和 [!UICONTROL Ads] 视图。

### 更改数据可视化的量度

1. 在数据可视化图表的右上角，单击 ![设置](/help/dsp/assets/settings-chart.png).

1. 选择量度。

   您不能选择同一量度两次。

1. 单击 **[!UICONTROL Apply]**.

### 更改数据可视化的显示模式

* 在数据可视化图表的右上角，单击 [!UICONTROL Overlay] 切换(![重叠切换](/help/dsp/assets/overlay.png))，以便在叠加模式（所有图表叠加在一起）和网格图模式（三个单独的图表）之间更改。

## 管理数据表 {#data-tables-manage}

在所有营销活动管理视图中([!UICONTROL Campaigns]， [!UICONTROL Packages]， [!UICONTROL Placements]、和 [!UICONTROL Ads])，您可以自定义显示在数据表中的数据。

### 管理列视图 {#column-views-manage}

每个营销活动管理级别([!UICONTROL Campaigns]， [!UICONTROL Packages]， [!UICONTROL Placements]、和 [!UICONTROL Ads])包括内置的 [!UICONTROL Pacing] 和 [!UICONTROL Performance] 包含该实体的相关量度的视图。 默认情况下， [!UICONTROL Pacing] 此时会显示视图，以便您一眼即可识别性能不佳的促销活动和促销活动组件。 您可以选择创建和编辑自定义列集。

![列视图选择器](/help/dsp/assets/column-view-selector.png)

DSP将最近的视图保存为默认视图，以便您每次返回到页面时，始终能够查看与您相关的度量。

#### 更改列视图 {#column-view-change}

* 在视图选择器中，单击 ![向下箭头](/help/dsp/assets/chevron-down.png)，然后单击所需列视图的名称。

#### 创建自定义列视图 {#column-view-create}

1. 在视图选择器中，单击 ![向下箭头](/help/dsp/assets/chevron-down.png)，然后单击 **[!UICONTROL Create View]**.

1. 指定要包含在视图中的量度：

   1. 在可用量度列表中，选中要包含的每个量度旁边的复选框。

      所有量度均按类别以字母顺序排列： [!UICONTROL Settings]， [!UICONTROL Spend]， [!UICONTROL Pacing]， [!UICONTROL Reporting] (DSP跟踪的标准指标)， [!UICONTROL Viewability]、和 [!UICONTROL Conversions]. 带有“(”的量度[!UICONTROL Lifetime])”从营销活动开始返回值，与在页面上选择的日期范围无关。

   1. 根据需要编辑列顺序，方法是单击右侧面板中的列名称并将它们拖到所需位置。

   某些列具有固定位置，无法移动或删除。

1. 应用或保存设置：

   * 要暂时应用设置而不将其保存到视图，请单击 **[!UICONTROL Apply].**

   * 要将设置保存到新的自定义列视图，请单击 **[!UICONTROL Save As]**. 在 [!UICONTROL Save View] 窗口中，输入新视图的名称，然后单击 **[!UICONTROL Save]**.

#### 编辑列视图 {#column-view-edit}

>[!NOTE]
>
>您无法将更改保存到标准（预定义）列视图，但可以临时应用更改或将更改保存到新的自定义视图。

1. 在视图选择器中，单击 ![向下箭头](/help/dsp/assets/chevron-down.png)，然后单击现有的列视图名称。

1. 在视图选择器中，单击 ![向下箭头](/help/dsp/assets/chevron-down.png)，然后单击 **[!UICONTROL Edit View]**.

1. 编辑要包含在视图中的量度：

   1. 在可用量度列表中，选中每个要包含的量度旁边的复选框，然后清除每个要排除的量度旁边的复选框。

      所有量度均按类别以字母顺序排列： [!UICONTROL Settings]， [!UICONTROL Spend]， [!UICONTROL Pacing]， [!UICONTROL Reporting] (DSP跟踪的标准指标)， [!UICONTROL Viewability]、和 [!UICONTROL Conversions]. 带有“(”的量度[!UICONTROL Lifetime])”从营销活动开始返回值，与在页面上选择的日期范围无关。

   1. 根据需要编辑列顺序，方法是单击右侧面板中的列名称并将它们拖到所需位置。

   某些列具有固定位置，无法移动或删除。

1. 应用或保存设置：

   * （仅限自定义视图）要保存设置，请单击 **[!UICONTROL Save]**.

   * 要暂时应用设置而不将其保存到视图，请单击 **[!UICONTROL Apply].**

   * 要将设置保存到新的自定义列视图，请单击 **[!UICONTROL Save As]**. 在 [!UICONTROL Save View] 窗口中，输入新视图的名称，然后单击 **[!UICONTROL Save]**.

### 过滤营销活动数据 {#filter-data-tables}

筛选器会更改在当前选项卡上显示的数据。 可用的筛选器因实体类型而异，但可能包括实体名称、状态和其他属性列。

1. 在主工具栏中，单击 ![“筛选器”按钮](/help/dsp/assets/filter.png).
1. 对于每个要应用的过滤器，单击左列中的过滤器名称，然后指定过滤器值。
1. 单击 **[!UICONTROL Apply]**.

#### 可用筛选器

以下筛选器适用于您的 [!UICONTROL Campaigns]， [!UICONTROL Packages]、和 [!UICONTROL Placements] 视图：

* [!UICONTROL Campaigns] 查看筛选器：
   * [!UICONTROL Campaign status]
   * [!UICONTROL Advertiser]
* [!UICONTROL Packages] 查看筛选器：
   * [!UICONTROL Custom flights] （无论它们是否存在）
   * [!UICONTROL Custom goal] （如果适用）
   * [!UICONTROL End end date]
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package status]
   * [!UICONTROL Start date]
* [!UICONTROL Placements] 查看筛选器：
   * [!UICONTROL Custom ad scheduling]
   * [!UICONTROL Custom goal] （如果适用）
   * [!UICONTROL End date]
   * [!UICONTROL Max bid] ([!UICONTROL less than]， [!UICONTROL greater than]，或 [!UICONTROL equal to] 指定值)
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Pacing on] ([!UICONTROL impressions] 或 [!UICONTROL spend])
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package]
   * [!UICONTROL Placement status]
   * [!UICONTROL Placement type]
   * [!UICONTROL Placement sub-type]
   * [!UICONTROL Start date]
   * [!UICONTROL Creation date]
* [!UICONTROL Ads] 查看筛选器：
   * [!UICONTROL Adobe ad approval status]
   * [!UICONTROL Ad ID]
   * [!UICONTROL Ad name]
   * [!UICONTROL Ad type]
   * [!UICONTROL Creation date]


### 更改日期范围

使用任何数据表上方的日期范围选择器，更改在所有标准和自定义视图中使用的日期范围。

![日期范围选择器](/help/dsp/assets/date-range-selector.png "日期范围选择器")

* 对于预设范围：从常用时间增量列表中选择。 默认为 [!UICONTROL Last 30 days]*.

* 对于特定范围，请执行下列任一操作：

   * 单击 ![日历](/help/dsp/assets/calendar.png "日历")，然后单击日历中的开始日期和结束日期。

   * 在日期范围内单击，然后输入起始日期和终止日期或在日历中选择它们。

     您可以输入数值（从M-D-YY到MM-DD-YYYY）和/或月份名称或缩写（如Jan或January）。

### 排序数据列

您可以按升序（A到Z，或1到10）或降序（Z到A，或10到1）对任意数据列进行排序。

* 单击列标题可在升序和降序之间切换。


### 指定数据行数

任意页面右下角的 **[!UICONTROL Items per page]** ，选择 *[!UICONTROL 25]*， *[!UICONTROL 50]*，或 *[!UICONTROL 100]*.

>[!MORELIKETHIS]
>
>* [Campaign Management视图中的性能报表类型](campaign-reports-about.md)
>* [查看投放位置的网站、广告和频率详细信息](placement-details-view.md)
>* [查看职位安排预测报表](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [查看放置诊断报告](placement-diagnostics.md)
>* [从Campaign Management视图中导出数据](campaign-export-data.md)
>* [视频：DSP帐户结构和用户界面](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
