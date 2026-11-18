---
title: 关于自定义营销活动管理视图中的数据
description: 了解您可以在Campaign数据视图中自定义的数据类型。
exl-id: 89f36865-9275-494e-ac33-d41fa30faa2a
feature: Search Common Tasks, Search Custom Data Views
TQID: 'https://experienceleague.adobe.com/PnBql37yqK03DWH2OhLf8hnCBPOwFAVZxD65NNZu0VU'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: d6e2ef48-fac7-5a4a-96ff-9ac0264dc826
    internal-label: Search Custom Data Views
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 968023d95217d4d17b1441ae717f3e472b31f7c4
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 0%
---
# 关于自定义营销活动管理视图中的数据

在大多数Campaign数据视图中，您可以自定义数据表中显示的数据。 您可以通过以下方式自定义数据：

* [编辑特定实体视图（如[!UICONTROL Campaigns]）的整个默认视图](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md##view-edit)的设置，以包含特定列顺序、筛选器、日期范围、归因规则等，并暂时应用设置或保存它们。 您还可以[创建其他自定义视图](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#create-custom-view)、[克隆现有视图](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#view-clone)和[应用任何视图](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#apply-a-default-or-custom-view)。

* [使用工具栏中的[!UICONTROL Custom Columns]控件更改列及其排序顺序](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md)。 在新UI中，如果工具栏太窄而无法显示控件，请单击&#x200B;**[!UICONTROL Actions]>[!UICONTROL Custom Columns]**。 您还可以从视图中的任何列标题快速[仅更改列](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md)。

* （仅限旧版用户界面） [从左侧导航面板](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/filter-using-left-panel.md)，您可以：

  * 按广告网络浏览或搜索实体，并按实体的状态以及帐户、营销活动以及广告组或广告集的状态进行筛选。 单击面板中的任意实体或实体组可加载子实体的视图（例如，单击促销活动名称可查看其子广告组）。

  * 按项目组合或项目组合组浏览或搜索促销活动，并按实体的状态以及项目组合组、项目组合和促销活动的状态进行过滤。 单击面板中的任意项目组合组、项目组合或营销策划，可在当前实体视图中加载项目组合组、项目组合或营销策划的数据。

  * 访问、编辑和重置默认视图；以及访问、编辑和删除自定义视图。 单击任意视图名称可加载相应的视图。

* 对任何可用数据列应用筛选器以更改在当前选项卡上显示的数据。 您可以从列标题[&#128279;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)创建筛选器[，或从工具栏](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)上的按钮创建筛选器。 对于营销活动管理视图，在打开子实体时，会根据需要维护过滤器。 例如，如果您查看具有\> 100次点击的促销活动，然后在该促销活动中打开一个广告组，则只显示具有\> 100次点击的广告组。

* [更改尚未保存特定日期范围的所有默认视图和自定义视图中使用的日期范围](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/date-filter.md)。

* [根据特定列中的值重新排序数据](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-sort.md)。

* 控制是否在任意页面底部显示25行、50行、100行、（仅旧版用户界面）200行或（仅旧版用户界面）[!UICONTROL Continuous Scroll]。


## （新UI）数据表控件 {#data-table-tools-new-ui}

使用数据表上方的工具栏管理数据并更改其显示方式。 可用的工具取决于视图和您的权限。

如果工具栏太窄而无法显示工具，请在&#x200B;**[!UICONTROL Actions]**&#x200B;菜单中查找该工具。

如果可用，您可以：

* 来自[!UICONTROL Conversion based on]的Select *[!UICONTROL Click Date]*&#x200B;或&#x200B;*[!UICONTROL Transaction Date]*，用于控制如何报告转化数据。

* 比较两个时间段的性能并选择差异的显示方式。 请参阅“[按日期范围](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/date-filter.md#compare-periods-new-ui)过滤数据”。

* 使用工具栏或&#x200B;**[!UICONTROL Actions]**&#x200B;菜单中的&#x200B;**[!UICONTROL Compressed Mode]**&#x200B;打开或关闭紧凑表格间距。

  打开压缩模式时，工具栏按钮处于选中状态。 在[!UICONTROL Actions]中，开关表示当前状态。

* 使用工具栏或&#x200B;**[!UICONTROL Actions]**&#x200B;菜单中的&#x200B;**[!UICONTROL Charts]**&#x200B;显示或隐藏图表。

  在显示图表时，工具栏按钮处于选中状态。 在[!UICONTROL Actions]中，开关指示是否显示图表。 再次单击控件可隐藏图表。
