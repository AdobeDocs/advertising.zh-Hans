---
title: 关于见解
description: 了解可视化图表的性能见解。
feature: DSP Campaigns, DSP Packages, DSP Placements
exl-id: 0b7943c4-650c-4515-ae19-4417714ea7dd
TQID: https://experienceleague.adobe.com/gcIUBvGMJiIZZ2XwCmEsidqFvp39cQBBxQYzpeUl-E4
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
  - id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3d
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 1e4a456c3add52553936db29a72f42e7d45506c3
workflow-type: tm+mt
source-wordcount: 1371
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

## 见解类型

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

### [!UICONTROL Audience Analysis]选项卡

[!UICONTROL Audience Analysis]选项卡在投放位置级别实时分析受众区段定位的有效性。 它包括一段时间的区段大小趋势和funnel的每日竞价细分。 使用这些见解监控目标受众池的稳定性，并识别在受众匹配和展示投放之间卷的丢失位置。 数据仅适用于定向受众区段的投放位置。

默认情况下，将显示特定广告商和特定投放位置的数据。 您可以选择配置过滤器以显示其他广告商的数据或选择不同的投放位置。

这些见解包括：

* **[!UICONTROL Audience Segment Size Trends]：**&#x200B;趋势图显示投放位置的所有受众区段中的每日独特用户数。 使用此图表可监控目标受众是随时间增长、稳定还是收缩。 持续下降可能表示区段即将到期或缩小，并且可能需要刷新区段数据或扩大定位范围。

  要查看特定数据点的确切用户数和日期，请将光标悬停在该点上。

* **[!UICONTROL Audience Funnel Analysis]：**&#x200B;一个每日时间序列表，显示应用所有定位和资格筛选器后，目标受众如何从总可用池缩小为实际展示次数胜利。 将显示前一天的数据。 funnel包括以下量度，按从最广泛到最狭窄的顺序排列：

   * **[!UICONTROL Audience Segment Size]：**&#x200B;聚合受众中的独特用户总数。

   * **[!UICONTROL Cookies in Bid Stream]：**&#x200B;目标受众中在前24小时内在竞价流中处于活动状态的用户数。 此计数包括范围内的每个用户，无论是否对他们进行置入投标。 从[!UICONTROL Total Target Audience]减少到[!UICONTROL Reachable Audience]反映了报告期间竞价流中处于非活动状态的受众部分，这并非竞价绩效的反映。

   * **[!UICONTROL Eligible cookies]：**&#x200B;在应用地域、设备类型、操作系统和浏览器筛选器之后仍保留的可访问用户的子集。 如果此数字显着低于[!UICONTROL Reachable Audience]，请考虑审查您的地理或设备类型定位是否过于严格。

  **[!UICONTROL Cookies Bid On]：**&#x200B;投放位置已提交竞价的合格机会数。 此阶段的锐减可能表示预算或步调限制限制了竞价量。

   * **[!UICONTROL Impression Wins]：**&#x200B;投放位置赢得印象的机会数。 如果中标价格远低于投标价格，则您的投标价格可能低于目标库存的现行市场价格。

## 查看性能分析

1. 打开一组见解：

   * （要打开所有营销活动的分析）在主菜单中，单击&#x200B;**[!UICONTROL Insights BETA]**。

   * （要打开特定营销活动、包或投放位置的见解）在[!UICONTROL Campaigns]、[!UICONTROL Packages]或[!UICONTROL Placements]视图中的实体名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Insights]**。

   * （要打开特定投放位置的见解）在[!UICONTROL Campaigns]、[!UICONTROL Packages]或[!UICONTROL Placements]视图中的实体名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Analyze]** > **[!UICONTROL Insights]**。

1. （可选）查看

## 将过滤器应用到选项卡

1. 在选项卡顶部的工具栏中，单击![筛选器按钮](/help/dsp/assets/filter.png)。

1. 在左列中，选择一个维，然后在右列中选择一个或多个值（如果适用）。

   您一次只能选择一个广告商。

1. 单击&#x200B;**[!UICONTROL Apply]**。

1. （可选）要进一步缩小数据范围，请在工具栏中选择维度类型，然后选择特定维度（单个营销活动、资源包或投放位置）。

1. （仅限[!UICONTROL Audience Funnel Analysis]；可选）要更改每日和每周之间的时间增量，请选择&#x200B;**[!UICONTROL Day]**&#x200B;或&#x200B;**[!UICONTROL Week]**。

## 更改为insight报告的维度

* 从insight左上角的下拉菜单中，选择维度。

## 更改为insight报告的指标

*可用于某些分析*

对于转化量度，同时支持Adobe Advertising跟踪和Adobe Analytics跟踪的转化。

1. 在insight的右上角，单击![指标设置](/help/dsp/assets/metric-settings.png "指标设置")。

1. 选择量度，然后单击&#x200B;**[!UICONTROL Apply]**。

## 将选项卡的所有可视化导出到PDF文件

* 在选项卡右上角单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Export]**。

  该文件将保存到浏览器的默认“下载”文件夹中。

## 将特定的insight下载到XLSX文件

* 单击insight右上角的![下载](/help/creative/assets/download.png "下载")。

  该文件将保存到浏览器的默认“下载”文件夹中。

<!-- 
Add:
## Save a custom view for a tab
-->

>[!MORELIKETHIS]
>
>* [关于自定义报告](/help/dsp/reports/report-about.md)
>* [促销活动管理视图中的性能报告类型](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [可用的报表列](/help/dsp/reports/report-columns.md)
>* [管理您的营销活动数据视图](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
