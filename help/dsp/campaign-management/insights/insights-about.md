---
title: 关于见解
description: 了解可视化图表的性能见解。
feature: DSP Campaigns, DSP Packages, DSP Placements
exl-id: 0b7943c4-650c-4515-ae19-4417714ea7dd
source-git-commit: a098e99f26a4e7d472d4a391d2cd465fc8d4255b
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 0%

---

# 关于见解

*Beta功能*

通过可视化图表获得高级别的性能洞察，可为您提供高效优化活动以及发现提升性能的新机会所需的信息。 您可以查看指定广告商的跨促销活动的数据或向下钻取到更低级别。

使用性能分析可以：

* 跟踪战略规划和明智决策的长期趋势。

* 找出取得更好成果的机会。

* 通过缩短从获取原始数据到获得可操作见解之间的时间来提高效率。

您可以将选项卡的所有可视化导出到PDF文件，或下载特定insight的数据，而无需使用Microsoft Excel电子表格(XLSX)格式进行可视化。

您还可以[更改日期范围、配置视图并保存自定义视图](/help/dsp/campaign-management/reports/campaign-data-views-manage.md){target="_blank"}，就像您为促销活动管理视图所做的那样。

## 分析类型

### [!UICONTROL Home]选项卡

[!UICONTROL Home]选项卡在所有广告商的营销活动中提供关键标准、性能和可见性量度。 默认情况下，将显示特定广告商和自定义目标的跨版面数据。 您可以选择配置过滤器以显示不同广告商、不同自定义目标或特定投放位置的数据。 <!-- I don't see campaigns or packages anymore:  You can optionally configure filters to show data for a different advertiser or data for only specific campaigns, packages, custom goals, and placements. -->分析包括：

* **[!UICONTROL Trends]：**&#x200B;三个客户指定的指标（默认情况下，[!UICONTROL Net Spend]、[!UICONTROL Impressions]和[!UICONTROL Net CPM]）的趋势图。

* **[!UICONTROL Delivery Breakdown]：**&#x200B;按三个客户指定的维度（例如按促销活动、发布者和媒体类型）对特定量度的数据进行细分。 对于每个维度细分，您可以选择不同的量度。

### [!UICONTROL Household Reach]选项卡

[!UICONTROL Household Reach]选项卡跨广告商的所有营销活动提供家庭覆盖率量度。 默认情况下，会显示跨营销活动数据。 您可以选择配置过滤器以显示不同广告商、特定促销活动、跨包或投放位置或特定包或投放位置的数据。 这些见解包括：

* **[!UICONTROL Trends]：**&#x200B;按天或按周显示三个客户指定的指标（默认为[!UICONTROL Net Spend]、[!UICONTROL Unique Reach]和[!UICONTROL Net CPM]）的趋势图。

* **[!UICONTROL Incremental Household Reach]：**&#x200B;一个圆环图，显示[!UICONTROL Media Type]、[!UICONTROL Device Type]或[!UICONTROL Inventory Type]的增量家庭访问量。 *增量家庭覆盖范围*&#x200B;定义为仅通过单个媒体、设备或库存类型实现的家庭。

* **[!UICONTROL Reach Breakdown]：**&#x200B;递增的独特家庭覆盖与重叠家庭覆盖的比较，[!UICONTROL Media Type]、[!UICONTROL Device Type]或[!UICONTROL Inventory Type]。

  *增量家庭覆盖范围*&#x200B;定义为仅通过单个媒体、设备或库存类型实现的家庭。 *重叠的家庭覆盖范围*&#x200B;定义为通过多种媒体、设备或库存类型访问的家庭。

* **[!UICONTROL Top Performers]：**&#x200B;按[!UICONTROL Unique Reach]、[!UICONTROL Net Spend]和[!UICONTROL Cost per Reach]排列的表现最佳的促销活动、投放、包、发布者、站点/应用程序、媒体类型、库存类型或设备类型。

* **[!UICONTROL Performance Analysis]：**&#x200B;包、发布者或站点/应用程序的[!UICONTROL Cost per Reach]和[!UICONTROL Net Spend]。 使用此insight可查看哪些包、发布者或站点/应用程序表明潜在的显着增量访问。

  每个气泡的大小表示递增到达分数，气泡越大，表示平均递增到达分数越高。 要查看任何气泡的完整实体名称和关键量度，请将光标悬停在气泡上。

  影响级别包括：

   * **高影响：**&#x200B;考虑增加预算。
   * **中等影响**
   * **有限影响：**&#x200B;需要注意

### [!UICONTROL Household Conversion]选项卡

[!UICONTROL Household Conversion]选项卡提供所有广告商促销活动<!-- active only? -->的家庭转化量度。 默认情况下，将显示特定广告商和特定转化量度的跨营销活动数据。 您可以选择配置过滤器，以显示不同广告商或转化量度、特定促销活动、跨包或投放位置，或特定包或投放位置的数据。 这些见解包括：

* **[!UICONTROL Trends]：**&#x200B;按天或按周显示三个客户指定的指标（默认为[!UICONTROL Net Spend]、[!UICONTROL Conversions]和[!UICONTROL Net CPM]）的趋势图。

* **[!UICONTROL Conversion Participation Overview]：**&#x200B;一个条形图，其中显示了哪些媒体类型、库存类型和设备类型导致了大多数家庭转化。

  在回顾期间（30天）内投放的展示次数被视为有效参与转化。

* **[!UICONTROL Top Performers]：**&#x200B;包含促销活动、包、版面、发布者、站点/应用程序、媒体类型和库存类型的表，这些表可提升三个客户指定的量度（默认情况下，[!UICONTROL Net Spend]、[!UICONTROL CPA]和[!UICONTROL Conversions]）的性能。 首先列出最佳执行者。

* **[!UICONTROL Performance Analysis]：**&#x200B;包、发布者或站点/应用程序的[!UICONTROL CPA]和[!UICONTROL Net Spend]。 使用此insight可查看哪些包、发布者或站点/应用程序表明潜在的显着增量访问。

  每个气泡的大小表示递增到达分数，气泡越大，表示平均递增到达分数越高。 要查看任何气泡的完整实体名称和关键量度，请将光标悬停在气泡上。

  影响级别包括：

   * **高影响：**&#x200B;考虑增加预算。
   * **中等影响**
   * **有限影响：**&#x200B;需要注意

## 打开性能分析

* （要打开所有营销活动的分析）在主菜单中，单击&#x200B;**[!UICONTROL Insights BETA]**。

* （要打开特定营销活动、包或投放位置的见解）在[!UICONTROL Campaigns]、[!UICONTROL Packages]或[!UICONTROL Placements]视图中的实体名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Insights]**。

## 将过滤器应用到选项卡

1. 在选项卡顶部的工具栏中，单击![筛选器按钮](/help/dsp/assets/filter.png)。

1. 在左列中，选择一个维，然后在右列中选择一个或多个值（如果适用）。

   您一次只能选择一个广告商。

1. 单击&#x200B;**[!UICONTROL Apply]**。

1. （可选）要进一步缩小数据范围，请在工具栏中选择实体类型，然后选择特定实体值（单个营销活动、资源包或投放位置）。

## 更改为Insight报告的Dimension

* 从insight左上角的下拉菜单中，选择维度。

## 更改为Insight报告的指标

对于转化量度，同时支持Adobe Advertising跟踪和Adobe Analytics跟踪的转化。

1. 在insight的右上角，单击![指标设置](/help/dsp/assets/metric-settings.png "指标设置")。

1. 选择量度，然后单击&#x200B;**[!UICONTROL Apply]**。

## 将选项卡的所有可视化导出到PDF文件

* 在该选项卡上方，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Export]**。

  该文件将保存到浏览器的默认“下载”文件夹中。

## 将特定的Insight下载到XLSX文件

* 单击insight右上角的![下载](/help/creative/assets/download.png "下载")。

  该文件将保存到浏览器的默认“下载”文件夹中。

>[!MORELIKETHIS]
>
>* [关于自定义报告](/help/dsp/reports/report-about.md)
>* 营销活动管理视图中的[性能报表类型](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [可用报告列](/help/dsp/reports/report-columns.md)
>* [管理您的Campaign数据视图](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
