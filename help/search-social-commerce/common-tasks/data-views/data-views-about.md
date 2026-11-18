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
source-git-commit: 2f170883b2876ea4a7b39e814df598d337f7ca07
workflow-type: tm+mt
source-wordcount: '425'
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

<!--

## (New UI) Data table tools {#grid-controls-new-ui}

In applicable management views, the toolbar includes the following controls:

* On the left, the [!UICONTROL Filter] control appears before grid search. Where supported, the [!UICONTROL Conversion based on] selector follows search and lets you select [!UICONTROL Click Date] or [!UICONTROL Transaction Date].

* On the right, operational actions, such as [!UICONTROL Reports], appear alongside view and display controls. The available controls depend on the view and your permissions.

* When the available width is reduced, controls move into the [!UICONTROL Actions] menu. This can happen when you narrow the window or open the AI Assistant panel. If a control isn't visible in the toolbar, look for it in [!UICONTROL Actions]. In wider layouts, controls remain inline.

* Within [!UICONTROL Actions], a horizontal divider separates operational actions from view and display controls, such as the current view, [!UICONTROL Custom Columns], [!UICONTROL Compressed Mode], and [!UICONTROL Charts], where available.

* The primary create button remains outside [!UICONTROL Actions].

The [!UICONTROL Refresh] icon is beside the page title in applicable views. The date range control is in the page header. For instructions on comparing two date ranges and changing the comparison format, see "[Filter data by date range](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/date-filter.md#compare-periods-new-ui)."

### Change the grid density

* Where available, click **[!UICONTROL Compressed Mode]** in the toolbar or **[!UICONTROL Actions]** menu to turn compact grid spacing on or off.

  The toolbar button is selected when compressed mode is on. In [!UICONTROL Actions], a switch indicates the current state.

### Show or hide charts

* Where available, click **[!UICONTROL Charts]** in the toolbar or **[!UICONTROL Actions]** menu.

  The toolbar button is selected when charts are shown. In [!UICONTROL Actions], a switch indicates whether charts are shown. Click the control again to hide the charts.

-->
