---
title: （新UI）查看查看项目组合绩效详细信息
description: 了解如何查看项目组合绩效详细信息，包括项目组合级别和每个分配营销活动的实际和预测指标。
feature: Search Portfolios, Search Optimization
hide: true
exl-id: b5178856-1b0e-45cf-a351-6f31c0b0ec76
source-git-commit: fee9c6e4649c348cad7561f81a9d45d92eb672ec
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# （新UI）查看项目组合绩效详细信息

*Beta功能*

<!-- Verify all, including why (if) the first report is for active and optimized portfolios(?), and why the other reports are for active portfolios, not optimized ones -->

项目组合详细信息视图包含有关项目组合的以下信息：

* 最多三个性能指标的实际值和预测值。 这些报表包括项目组合的总量度值和按日期的量度细分。<!-- Not for active portfolios only?  -->

* 活动项目组合的模型准确度数据，它显示模型与预测的偏差程度。 此报表显示每日或滚动七天的总体成本准确度、点击准确度以及目标值准确度。

  您可以按单击日期（默认值）或事务处理日期查看数据。   您还可以以趋势图（默认）或表的形式查看数据。

* 目标支出与有效项目组合的实际支出。 您也可以选择包括项目组合的市场活动预算合计。

* 广告网络对活动项目组合的成本、点击次数或[目标值](/help/search-social-commerce/glossary.md#o-p)预测的准确性。<!-- Verify -->

* 项目组合设置。

  您可以选择打开项目组合设置进行编辑。

## 打开项目组合的性能详细信息

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Portfolios]**。

1. 单击项目组合名称。

1. （可选）从&#x200B;**[!UICONTROL Granularity]**&#x200B;菜单中，更改&#x200B;*[!UICONTROL Daily]、* *[!UICONTROL Weekly]、*&#x200B;或&#x200B;*[!UICONTROL Monthly]之间的数据粒度。*

1. （可选）要更改项目组合详细信息的日期范围，请单击右上角的日期范围，指定日期范围，然后单击&#x200B;**[!UICONTROL Apply]**。

## 自定义[!UICONTROL Portfolio Overview]选项卡

* （可选）要自定义[!UICONTROL Portfolio Performance]报表，请执行以下任一操作：

   * 要更改用于总指标和详细指标的性能指标，请单击&#x200B;**[!UICONTROL Metrics]**&#x200B;并选择最多三个指标。

     默认量度为&#x200B;*[!UICONTROL Cost]*、*[!UICONTROL Clicks]*&#x200B;和&#x200B;*[!UICONTROL Objective Value]*.<!-- What else is available: the advertiser's revenue metrics? Anything else from the ad networks? -->

   * 对于详细量度：

      * 将开关移动到&#x200B;**[!UICONTROL Display predictions]**&#x200B;旁以显示或隐藏预测的量度值。

      * 在图表视图（![图表视图](/help/search-social-commerce/assets/chart-view.png "图表视图")）和表视图(![表格视图](/help/search-social-commerce/assets/table-view.png "表格视图"))之间切换。

      * （在图表视图中）要查看图表上任何点的数据，请将光标悬停在该点上。

* （可选）要自定义[!UICONTROL Model accuracy]趋势图，请执行以下任一操作：

   * 在图表视图（![图表视图](/help/search-social-commerce/assets/chart-view.png "图表视图")）和表视图(![表格视图](/help/search-social-commerce/assets/table-view.png "表格视图"))之间切换。

   * 按&#x200B;*[!UICONTROL Click Date]*&#x200B;和&#x200B;*[!UICONTROL Transaction Date]*&#x200B;切换查看数据。

   * 在查看有关&#x200B;*[!UICONTROL Daily Accuracy]*&#x200B;和&#x200B;*[!UICONTROL 7 Day Rolling Accuracy]*&#x200B;的数据之间切换。

     [!UICONTROL 7 Day Rolling Accuracy]是前七天预测的平均准确性，以百分比表示。 例如，2025年5月8日的值是2025年5月1日至5月7日的平均准确率。

   * （在图表视图中）要查看图表上任何点的数据，请将光标悬停在该点上。

* （可选）要自定义[!UICONTROL Target vs actual spend]趋势图，请执行以下任一操作：

   * 将开关移动到&#x200B;**[!UICONTROL Display budget]**&#x200B;旁边，可显示或隐藏每个日期的总营销活动预算。

   * 要查看图表上任何点的数据，请将光标悬停在该点上。

* （可选）要自定义[!UICONTROL Network Accuracy]趋势图，请执行以下任一操作：

   * 将报告的量度更改为&#x200B;*[!UICONTROL Cost]*、*[!UICONTROL Clicks]*&#x200B;或&#x200B;*[!UICONTROL Objective Value]*。

   * 要查看图表上任何点的数据，请将光标悬停在该点上。

1. 单击&#x200B;**[!UICONTROL Download report]**。

## 列出项目组合中的营销活动

* 单击&#x200B;**[!UICONTROL Campaigns]**&#x200B;选项卡。

## 列出项目组合中的广告组

* 要查看项目组合内某个促销活动中的所有广告组，请单击&#x200B;**[!UICONTROL Campaigns]**&#x200B;选项卡，然后单击促销活动名称。

## 列出项目组合中的关键词

* 要查看项目组合中的所有关键字，请单击&#x200B;**[!UICONTROL Keywords]**&#x200B;选项卡。

* 要查看项目组合内广告组中的所有关键字，请单击&#x200B;**[!UICONTROL Ad Groups]**&#x200B;选项卡，然后单击广告组名称。

## 查看和编辑项目组合设置

* 要查看或隐藏项目组合设置，请单击&#x200B;**[!UICONTROL Portfolio Settings]**。

   * 要编辑可见的项目组合设置，请单击设置部分旁边的![编辑](/help/search-social-commerce/assets/edit.png "编辑")，然后单击[编辑项目组合设置](portfolio-edit.md)。

有关项目组合设置的更多信息，请参阅可在搜索、社交和Commerce中找到的“优化指南” 。

## 下载项目组合性能报表和项目组合组件列表

1. 单击工具栏中的&#x200B;**[!UICONTROL Download report]**。

1. 选中要包含的每个性能报表和项目组合组件类型旁边的复选框。

   对于某些性能报表，您可以选择将数据下载为购物车还是表格。

>[!MORELIKETHIS]
>
>* [（新UI）关于项目组合](portfolio-about.md)
>* [（新UI）编辑项目组合](portfolio-edit.md)
>* [（新UI）下载[!UICONTROL Portfolios]视图中的数据](portfolio-view-report.md)
