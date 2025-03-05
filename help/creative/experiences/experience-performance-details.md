---
title: 体验级性能报表
description: 了解如何查看体验级性能报表。
feature: Creative Experiences
exl-id: 5e7c4c9d-b992-460a-9765-4276027f9a61
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 0%

---

# 体验级性能报表

*已关闭的测试版*

您可以查看任何体验的详细性能数据。

## 体验级性能报表中的数据

报表视图包含以下数据：

* **概述**&#x200B;选项卡：整个体验的性能概述，包括：

   * **总体性能**&#x200B;部分：

   * **整体性能**：单个转化量度的总展示次数、点击次数、点进率(CTR)以及显示到达转化和点进转化。<!-- Just one, or can you select multiple? And I don't see this as of 2/8:  You can optionally combine two metrics at a time into a single chart. -->

     <!--
     ![Overall performance](/help/creative/assets/experience-report-overall-performance.png "Overall performance"){width="100" zoomable="yes"}
          -->

   * **默认比率**： （仅具有决策树定位的体验）由目标创意、无目标或面向“其他所有人”的通用创意，以及体验的默认创意产生的展示次数。

     <!--
     ![Default rate](/help/creative/assets/experience-report-default-rate.png "Default rate"){width="100" zoomable="yes"} 
     -->

   * **性能细分**&#x200B;部分：

      * **区域性能：*：按地理位置划分的各个量度。

        <!-- You can optionally do the following:
    
      * Click a metric name (such as [!UICONTROL Impressions]) to view that metric.

      * Select the region in the **[!UICONTROL Region]** menu.
      
      -->

        <!--   
      ![Regional performance](/help/creative/assets/experience-report-regional-performance.png "Regional performance"){width="100" zoomable="yes"}
      -->

      * **设备性能：**&#x200B;按设备类型、操作系统和浏览器列出的各个量度。 （可选）单击任何设备类别的值，以查看符合该条件的前<!-- NN -->个创意的列表。

        <!--    
      ![Device performance](/help/creative/assets/experience-report-device-performance.png "Device performance"){width="100" zoomable="yes"}
      -->

* **创意效果**&#x200B;选项卡*：按创意和捆绑包或广告标记列出的效果概述，包括：

   * **创意内容**&#x200B;子选项卡：体验中每个创意内容的展示次数、点击次数和CTR总数。<!-- No breakdown yet for the individual ad elements and/or the served ads. -->

     <!--

     * *Experiences with decision tree targeting:* The total number of impressions, clicks, and CTR for each creative. You can optionally do the following:
     
       * To break out the performance for each ad target, enable **[!UICONTROL Split targeting]**.

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report. [Find out about this:  ..., and total conversions for specified conversion metricsYour conversion metrics are combined into one Conversions column set unless you have made individual metric column sets available within Advertising Cloud Search.]

     * *Experiences without decision tree targeting:* The total number of impressions, clicks, and click-through rate (CTR) for each creative. You can optionally do the following:

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     -->

   * **包/标记**&#x200B;子选项卡：体验中的单个包（具有决策树定位的体验）或广告标记（没有决策树定位的体验）的展示次数、点击次数和CTR总数。

     <!--
   
     * *Experiences with decision tree targeting:* The total number of impressions, clicks, and CTR for each bundle. You can optionally do the following:
     
       * To break out the performance for each ad target, enable **[!UICONTROL Split targeting]**.

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions  and click-through conversions (using on the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     * *Experiences without decision tree targeting:* The total number of impressions, clicks, and click-through rate (CTR) for each ad tag. You can optionally do the following:

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     -->

## 查看某个体验的性能报表

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. （可选）[自定义视图](/help/creative/introduction/customize-data-views.md)以包含特定体验。

1. 选择体验：

   * 在卡片视图中，单击体验名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Reports]**。

   * 在表视图中，将光标悬停在行上并单击&#x200B;**[!UICONTROL Reports]**。

   将打开[!UICONTROL Overview]选项卡。

1. （可选）在右上角的工具栏中，指定所有性能报表中报告的日期范围、转化归因规则和转化：

   * （可选）要更改性能数据的日期范围，请在日期菜单中选择一个选项：

      * 要指定预设时段，请选择报表： (*[!UICONTROL Last Month-to-date]，* *[!UICONTROL Last 7 days]，* *[!UICONTROL Last 30 days]，* *[!UICONTROL Last 7 days]，* *[!UICONTROL Last 30 days]，* *[!UICONTROL Today]，*&#x200B;或&#x200B;*[!UICONTROL Yesterday]*。

      * 要指定自定义日期范围，请指定开始日期和结束日期<!-- in the format MM/DD/YYYY or M/D/YYYY,-->或单击字段旁边的![日历图标](/help/search-social-commerce/assets/calendar.png)并选择日期。

   * （可选）要更改用于在一系列导致转化的事件中归因转化数据的规则，请单击![设置](/help/creative/assets/settings.png)并更改&#x200B;**[!UICONTROL Attribution Rule]**。

   * （可选）要更改报告的转化，请单击![设置](/help/creative/assets/settings.png)，然后在&#x200B;**[!UICONTROL Conversions]**&#x200B;菜单中选择转化名称。&lt;！ — 只有一个，还是多个？ 验证这些内容的显示方式 — 我需要看到已设置多个转化的广告商 — >

     可用的转化列包括Advertising Search、Social和Commerce中可用的转化，无论您是Search、Social还是Commerce客户。 当广告商具有[an [!DNL Adobe Analytics for Advertising] 集成](/help/integrations/analytics/overview.md)时，这可能包括从Adobe Analytics同步的转化和网站参与量度。 <!--Analytics calculated metrics and advanced calculated metrics aren't available.-->有关在报表中包括收集的转化率的详细信息，请参阅《搜索、社交和Commerce指南》主题“[关于管理广告商的转化量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)”。

1. （在[!UICONTROL Overview]选项卡上）：

   * （可选）在[!UICONTROL Overall Regional Performance]部分中，将光标悬停在图表中的某个点上可查看该点的数据。

   * （可选）在[!UICONTROL Regional Performance]部分中，执行以下任一操作：

      * 单击某个量度名称（如[!UICONTROL Impressions]）以查看该量度。

      * 在[!UICONTROL Region]菜单中选择区域。

      * 将光标悬停在国家/地区或州上可查看该区域的数据。

   * （可选）在[!UICONTROL Device Performance]部分中，执行以下任一操作：

      * 将光标悬停在任何设备类别的值上可查看该标准的数据。

      * 单击任何设备类别的值可查看使用该条件的前<!-- NN-->个创意的列表。

1. （可选）要按创意、包或广告标记查看数据，请单击&#x200B;**[!UICONTROL Creative Performance]**&#x200B;选项卡。

   * 在[!UICONTROL Creatives]子选项卡上，您可以执行以下任一操作：

      * （可选）若要在图表视图和网格视图之间切换，请分别单击![图表](/help/creative/assets/chart-view-button.png "图表")和![网格](/help/creative/assets/table-view-button.png "网格")。

      * （可选）在图表视图中，将光标悬停在图表中的某个点上可查看该点的数据。

      * （仅具有决策树定位的体验；可选）要划分每个应用的广告目标的性能，请启用&#x200B;**[!UICONTROL Split targeting]**。

1. 要按捆绑（具有决策树定位的体验）或广告标记（没有决策树定位的体验）查看数据，请单击&#x200B;**[!UICONTROL Bundles]**&#x200B;子选项卡。 您可以执行以下任一操作：

   * （可选）若要在图表视图和网格视图之间切换，请分别单击![图表](/help/creative/assets/chart-view-button.png "图表")和![网格](/help/creative/assets/table-view-button.png "网格")。

   * （可选）在图表视图中，将光标悬停在图表中的某个点上可查看该点的数据。

   * （仅具有决策树定位的体验；可选）要划分每个应用的广告目标的性能，请启用&#x200B;**[!UICONTROL Split targeting]**。

1. （可选）要以电子表格(XLSX)格式下载[!DNL Microsoft Excel]文件中的数据，请单击工具栏中的![下载](/help/creative/assets/download.png "下载")。

   将按照浏览器的正常过程下载文件。

>[!MORELIKETHIS]
>
>* [自定义创意报告](/help/creative/report-custom-creative.md)
