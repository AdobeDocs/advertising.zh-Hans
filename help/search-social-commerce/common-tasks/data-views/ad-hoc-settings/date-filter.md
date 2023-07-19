---
title: 按日期范围筛选数据
description: 了解如何使用全局日期范围过滤器。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# 按日期范围筛选数据

除了已保存特定日期范围的默认视图和自定义视图外，相同全局日期范围过滤器应用于所有广告商中的大多数促销活动数据视图。 促销活动管理视图的系统默认日期范围是“昨天”。

日期范围设置将保存到特定于浏览器的Cookie，因此，在您每次使用同一浏览器应用程序登录时，会对所有广告商使用对日期范围筛选器的任何更改，直到您更改筛选器或删除Cookie为止。 您使用的每个浏览器应用程序都会将日期范围过滤器设置存储在其他Cookie中。

在为默认视图或自定义视图保存特定日期范围时，无论您使用何种浏览器应用程序，该范围都会在您应用视图时应用。

>[!NOTE]
>
>* 您可以查看前13个月的数据，但任何现有的自定义视图最多只能包含前180天的数据。
>* 要查看以前的数据，请转到 [[!UICONTROL Reports] 视图](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) 并运行基本报表。
>* 您还可以保存日期范围 [默认视图或自定义视图](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).


## 在营销活动视图中更改全局日期过滤器

1. 在“搜索”\>“促销活动”\>“促销活动”的任何数据表上方，单击当前日期范围。

1. 在 **[!UICONTROL Date Range]** 字段，指定范围：

   * 对于预设范围：从常用时间增量列表中选择，范围从 *[!UICONTROL Today]* 到 *[!UICONTROL Last 180 Days]*. 默认为 *[!UICONTROL Yesterday]*.

   * 对于特定范围：选择 **[!UICONTROL Custom Date Range]** ，然后指定开始日期和结束日期。

      以MM/DD/YYYY或MM-DD-YYYY格式输入日期，或单击 ![日历图标](/help/search-social-commerce/assets/calendar.png "日历图标") ，打开日历并选择日期。

1. （可选）比较指定日期范围的数据与第二个日期范围的数据：

   1. 移动 **[!UICONTROL Comparison]** 滑块到 *[!UICONTROL On]*.

      选择此选项时，将为每个常规数据列添加两个附加列。 例如，不要只包含“”的一列[!UICONTROL Impressions]，”该表包含“”的列[!UICONTROL Impressions R1]，&quot; &quot;[!UICONTROL Impressions R2]，”和“[!UICONTROL Impressions Diff].”  如果导出数据，则相同的列将拼写为&quot;[!UICONTROL Impressions Range 1]，&quot; &quot;[!UICONTROL Impressions Range 2]，”和“[!UICONTROL Impressions Difference].”

   1. 指定第二个日期范围。

   1. 在“\[”中选择如何表示两个所选日期范围中的数据之间的差异&#x200B;_数据字段_“\] Difference”列：

      * *[!UICONTROL Variance]* （默认）：将差异显示为数值。

      * *[!UICONTROL % Change]：*  以百分比显示差异。

1. 单击 **[!UICONTROL Apply]**.