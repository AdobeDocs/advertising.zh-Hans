---
title: 按日期范围筛选数据
description: 了解如何使用全局日期范围过滤器。
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
TQID: 'https://experienceleague.adobe.com/1zB1NSise7wN1B68fUTq6ef824eiJx3zEglI0iUzwKQ'
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
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 968023d95217d4d17b1441ae717f3e472b31f7c4
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%
---
# 按日期范围筛选数据

使用日期范围筛选器指定要显示性能数据的时段。 在支持日期比较的视图中，您还可以比较两个时段的性能。

## （新UI）更改日期范围 {#date-filter-new-ui}

1. 在页眉中，单击带有日历图标的日期范围控件。

1. 指定日期范围：

   * 要使用预设范围，请从第一个日历上方的菜单中选择一个选项，如&#x200B;**[!UICONTROL Yesterday]**&#x200B;或&#x200B;**[!UICONTROL Last 7 Days]**。

   * 要使用自定义范围，请选择&#x200B;**[!UICONTROL Custom Date Range]**&#x200B;并在日历中选择开始日期和结束日期。 使用日历箭头在月份之间导航。

1. 单击&#x200B;**[!UICONTROL Apply]**。

## （新UI）比较两个期间的数据 {#compare-periods-new-ui}

*只支持日期比较的视图*

1. 在页眉中，单击带有日历图标的日期范围控件。

1. 打开&#x200B;**[!UICONTROL Compare Periods]**。

   两个日历面板并排显示。 第一个时段具有青色标记，而比较时段具有紫色标记。

1. 在第一个面板中，指定日期范围：

   * 要使用预设范围，请从第一个日历上方的菜单中选择一个选项，如&#x200B;**[!UICONTROL Yesterday]**&#x200B;或&#x200B;**[!UICONTROL Last 7 Days]**。

   * 要使用自定义范围，请选择&#x200B;**[!UICONTROL Custom Date Range]**&#x200B;并在日历中选择开始日期和结束日期。 使用日历箭头在月份之间导航。

1. 在第二个面板中，选择比较预设或单击日历中的开始日期。

   比较时段与第一个时段的天数相同。 查看两个日历上完整的日期范围。

1. 从&#x200B;**[!UICONTROL Comparison Format]**&#x200B;中，选择如何显示差异：

   * **[!UICONTROL As percentage]：**&#x200B;以百分比显示差异。

   * **[!UICONTROL As variance]：**&#x200B;将差异显示为数字值。

1. 单击&#x200B;**[!UICONTROL Apply]**。

   日期范围控件显示完整的日期范围及其期间标签和颜色标记。 每个可比较量度都分组为两个时段列和一个&#x200B;**[!UICONTROL Change]**&#x200B;列。 不可比较的字段仍保持为单列。 列标题中的期间标记标识对应的日期范围。

要停止比较期间，请打开日期范围控件，关闭&#x200B;**[!UICONTROL Compare Periods]**，然后单击&#x200B;**[!UICONTROL Apply]**。 关闭比较会根据比较数据清除过滤器。

### 从列菜单更改比较格式

1. 启用日期比较后，打开&#x200B;**[!UICONTROL Change]**&#x200B;列的列标题菜单或可比较量度的期间列的任一菜单。

1. Select **[!UICONTROL As percentage]**&#x200B;或&#x200B;**[!UICONTROL As variance]**。

   该选择适用于数据表中的所有比较量度，而不仅仅是选定列。 日期范围控件与所选内容同步，并且格式在当前广告商的适用页面（包括已保存日期范围的视图）之间共享。

   成功刷新数据表后，将显示一条确认消息。 如果数据表无法以所选格式刷新，则会显示错误消息；请尝试再次选择格式。

排序和筛选选项在支持的列菜单中仍然可用。

## （旧版UI）日期范围设置

相同的全局日期范围过滤器适用于所有广告商的大多数数据视图，但已保存特定日期范围的默认视图和自定义视图除外。 促销活动管理视图的系统默认日期范围是“昨天”。

日期范围设置会保存到特定于浏览器的Cookie，因此，在您每次使用同一浏览器应用程序登录时，所有广告商都会使用您对日期范围筛选器的任何更改，直到您更改筛选器或删除Cookie为止。 您使用的每个浏览器应用程序都会将日期范围过滤器设置存储在不同的Cookie中。

在为默认视图或自定义视图保存特定日期范围时，无论您使用何种浏览器应用程序，该范围都会在您应用视图时应用。

>[!NOTE]
>
>* 您可以查看前13个月的数据，但任何现有的自定义视图最多只能包含前180天的数据。
>* 要查看以前的数据，请转到[[!UICONTROL Reports]视图](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)并运行基本报表。
>* 您还可以保存[默认视图或自定义视图](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)的日期范围。

## （旧版UI）更改营销活动视图中的全局日期过滤器

1. 在“搜索\>促销活动\>促销活动”中任何数据表的上方，单击当前日期范围。

1. 在&#x200B;**[!UICONTROL Date Range]**&#x200B;字段中，指定范围：

   * 对于预设范围：从常用时间增量列表中选择，范围从&#x200B;*[!UICONTROL Today]*&#x200B;到&#x200B;*[!UICONTROL Last 180 Days]*。 默认值为&#x200B;*[!UICONTROL Yesterday]*。

   * 对于特定范围：选择&#x200B;**[!UICONTROL Custom Date Range]** ，然后指定开始日期和结束日期。

     以MM/DD/YYYY或MM-DD-YYYY格式输入日期，或单击每个字段旁边的![日历图标](/help/search-social-commerce/assets/calendar.png "日历图标")以打开日历并选择日期。

1. （可选）比较指定日期范围的数据与第二个日期范围的数据：

   1. 将&#x200B;**[!UICONTROL Comparison]**&#x200B;滑块移动到“开”位置。

      选择此选项时，将为每个常规数据列添加两个额外的列。 例如，该表不只包括“[!UICONTROL Impressions]”的一列，而是包括“[!UICONTROL Impressions R1]”、“[!UICONTROL Impressions R2]”和“[!UICONTROL Impressions Diff]”的列。  如果导出数据，则相同的列将拼写为“[!UICONTROL Impressions Range 1]”、“[!UICONTROL Impressions Range 2]”和“[!UICONTROL Impressions Difference]”。

   1. 指定第二个日期范围。

   1. 在“\[_数据字段_\] Difference”列中选择如何表示两个所选日期范围中的数据之间的差异：

      * *[!UICONTROL Variance]* （默认）：将差异显示为数值。

      * *[!UICONTROL % Change]：*&#x200B;以百分比显示差异。

1. 单击&#x200B;**[!UICONTROL Apply]**。
