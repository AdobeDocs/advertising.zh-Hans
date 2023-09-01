---
title: 关于Campaign数据视图
description: 了解如何自定义营销活动、包、投放位置和广告的数据视图。
feature: DSP Campaign Data Views
exl-id: 125f8f49-2fa3-4838-82dc-4760d2ea9c7e
source-git-commit: 16081f3ec55eb6d2d42927e440fba17cd0f4265c
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# 关于Campaign数据视图

在所有营销活动管理视图中([!UICONTROL Campaigns]， [!UICONTROL Packages]， [!UICONTROL Placements]、和 [!UICONTROL Ads])，您可以自定义显示在数据表中的数据。 您可以通过以下方式自定义数据：

* 通过从视图选择器中选择视图、编辑现有视图中的列以暂时应用更改或创建自定义列视图来指定数据列及其顺序。

  每个营销活动管理级别([!UICONTROL Campaigns]， [!UICONTROL Packages]， [!UICONTROL Placements]、和 [!UICONTROL Ads])包括内置的 [!UICONTROL Pacing] 和 [!UICONTROL Performance] 包含该实体的相关量度的视图。 默认情况下， [!UICONTROL Pacing] 此时会显示视图，以便您一眼即可识别性能不佳的促销活动和促销活动组件。 您可以选择 [更改列视图](column-view-change.md) 查看性能数据(使用 [!UICONTROL Performance] 视图)或任何保存的列集。 您可以选择 [编辑列](column-view-edit.md) 在 [!UICONTROL Pacing] 或 [!UICONTROL Performance] 查看以临时应用更改。

  您还可以保存 [自定义列集](column-view-create.md) 任何顺序的任意列。

  ![列视图选择器](/help/dsp/assets/column-view-selector.png)

  在列视图编辑器中，所有量度按类别按字母顺序排列： [!UICONTROL Settings]， [!UICONTROL Spend]， [!UICONTROL Pacing]， [!UICONTROL Reporting] (DSP跟踪的标准指标)， [!UICONTROL Viewability]、和 [!UICONTROL Conversions]. 带有“(”的量度[!UICONTROL Lifetime])”从营销活动开始返回值，与在页面上选择的日期范围无关。

  ![列视图编辑器](/help/dsp/assets/column-view-editor.png)

  DSP将最近的视图另存为默认视图，以便您每次返回到页面时，都可以查看与您相关的度量。

* 应用 [过滤器](campaign-data-filter.md) 更改当前选项卡上显示的数据。 可用的筛选器因实体类型而异，但可能包括实体名称、状态和其他属性列。

* 更改在所有标准和自定义视图中使用的日期范围。

* [按任意列中的值对数据排序](campaign-data-sort.md).

* 控制在任何页面的右下角显示25行、50行还是100行。

>[!MORELIKETHIS]
>
>* [关于平台内报告](campaign-reports-about.md)
>* [更改列视图](column-view-change.md)
>* [创建自定义列视图](column-view-create.md)
>* [编辑自定义列视图](column-view-edit.md)
>* [管理数据可视化图表](campaign-data-visualization-manage.md)
>* [查看投放位置的网站、广告和频率详细信息](placement-details-view.md)
>* [查看职位安排预测报表](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [查看放置诊断报告](placement-diagnostics.md)
>* [从Campaign Management视图中导出数据](campaign-export-data.md)
>* [视频：DSP帐户结构和用户界面](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
