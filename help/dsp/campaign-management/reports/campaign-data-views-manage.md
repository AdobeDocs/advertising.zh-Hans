---
title: 管理Campaign数据视图
description: 了解如何自定义营销活动、包、投放位置和广告的数据视图。
feature: DSP Campaign Data Views
source-git-commit: 14da2c26a6a6c3820f691cd752c22c982278314d
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---


# 管理Campaign数据视图

## 管理数据可视化图表

您可以为跨营销活动或单个营销活动的所有数据可视化更改量度和图表模式。 对单个营销活动的更改会应用于该营销活动的所有数据可视化图表，包括 [!UICONTROL Packages]， [!UICONTROL Placements]、和 [!UICONTROL Ads] 选项卡。

### 更改数据可视化的量度

1. 在数据可视化图表的右上角，单击 ![设置](/help/dsp/assets/settings-chart.png).
1. 选择量度。
您不能选择同一量度两次。
1. 单击 **[!UICONTROL Apply]**.

### 更改数据可视化的显示模式

* 在数据可视化图表的右上角，单击 [!UICONTROL Overlay] 切换(![重叠切换](/help/dsp/assets/overlay.png))，以便在叠加模式（所有图表叠加在一起）和网格图模式（三个单独的图表）之间更改。

## 管理数据表

在所有营销活动管理视图中([!UICONTROL Campaigns]， [!UICONTROL Packages]， [!UICONTROL Placements]、和 [!UICONTROL Ads])，您可以自定义显示在数据表中的数据。

### 更改列视图

* 在视图选择器中，单击 ![向下箭头](/help/dsp/assets/chevron-down.png)，然后单击所需列视图的名称。

### 创建自定义列视图

1. 在视图选择器中，单击 ![向下箭头](/help/dsp/assets/chevron-down.png)，然后单击 **[!UICONTROL Create View]**.

1. 指定要包含在视图中的量度：

   1. 在可用量度列表中，选中要包含的每个量度旁边的复选框。

   1. 根据需要编辑列顺序，方法是单击右侧面板中的列名称并将它们拖到所需位置。

   某些列具有固定位置，无法移动或删除。

1. 应用或保存设置：

   * 要暂时应用设置而不将其保存到视图，请单击 **[!UICONTROL Apply].**

   * 要将设置保存到新的自定义列视图，请单击 **[!UICONTROL Save As]**. 在 [!UICONTROL Save View] 窗口中，输入新视图的名称，然后单击 **[!UICONTROL Save]**.

### 编辑自定义列视图

>[!NOTE]
>
>您不能编辑标准（预定义的）列视图。

1. 在视图选择器中，单击 ![向下箭头](/help/dsp/assets/chevron-down.png)，然后单击现有的列视图名称。

1. 在视图选择器中，单击 ![向下箭头](/help/dsp/assets/chevron-down.png)，然后单击 **[!UICONTROL Edit View]**.

1. 编辑要包含在视图中的量度：

   1. 在可用量度列表中，选中每个要包含的量度旁边的复选框，然后清除每个要排除的量度旁边的复选框。

   1. 根据需要编辑列顺序，方法是单击右侧面板中的列名称并将它们拖到所需位置。

   某些列具有固定位置，无法移动或删除。

1. 应用或保存设置：

   * 要暂时应用设置而不将其保存到视图，请单击 **[!UICONTROL Apply].**

   * 要将设置保存到新的自定义列视图，请单击 **[!UICONTROL Save As]**. 在 [!UICONTROL Save View] 窗口中，输入新视图的名称，然后单击 **[!UICONTROL Save]**.

### 过滤营销活动数据

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

### 排序数据列

您可以按升序（A到Z，或1到10）或降序（Z到A，或10到1）对任意数据列进行排序。

* 单击列标题可在升序和降序之间切换。

<!-- add more links-->

>[!MORELIKETHIS]
>
>* [关于平台内报告](campaign-reports-about.md)
>* [管理数据可视化图表](/help/dsp/campaign-management/reports/campaign-data-visualization-manage.md)
>* [更改列视图](column-view-change.md)
>* [创建自定义列视图](column-view-create.md)
>* [编辑自定义列视图](/help/dsp/campaign-management/reports/column-view-edit.md)
>* [过滤营销活动数据](campaign-data-filter.md)
>* [排序数据列](campaign-data-sort.md)
>* [查看投放位置的网站、广告和频率详细信息](placement-details-view.md)
>* [查看职位安排预测报表](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [查看放置诊断报告](placement-diagnostics.md)
>* [从Campaign Management视图中导出数据](campaign-export-data.md)
>* [视频：DSP帐户结构和用户界面](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
