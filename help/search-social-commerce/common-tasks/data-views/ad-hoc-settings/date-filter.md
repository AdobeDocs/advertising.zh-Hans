---
title: 按日期范围筛选数据
description: 了解如何使用全局日期范围过滤器。
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# 按日期范围筛选数据

相同的全局日期范围过滤器适用于所有广告商中的大多数促销活动数据视图，但已保存特定日期范围的默认视图和自定义视图除外。 促销活动管理视图的系统默认日期范围是“昨天”。

日期范围设置会保存到特定于浏览器的Cookie，因此，在您每次使用同一浏览器应用程序登录时，所有广告商都会使用您对日期范围筛选器的任何更改，直到您更改筛选器或删除Cookie为止。 您使用的每个浏览器应用程序都会将日期范围过滤器设置存储在不同的Cookie中。

在为默认视图或自定义视图保存特定日期范围时，无论您使用何种浏览器应用程序，该范围都会在您应用视图时应用。

>[!NOTE]
>
>* 您可以查看前13个月的数据，但任何现有的自定义视图最多只能包含前180天的数据。
>* 要查看以前的数据，请转到[[!UICONTROL Reports]视图](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)并运行基本报表。
>* 您还可以保存[默认视图或自定义视图](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)的日期范围。

## 更改营销活动视图中的全局日期过滤器

1. 在“搜索\>促销活动\>促销活动”中任何数据表的上方，单击当前日期范围。

1. 在&#x200B;**[!UICONTROL Date Range]**&#x200B;字段中，指定范围：

   * 对于预设范围：从常用时间增量列表中选择，范围从&#x200B;*[!UICONTROL Today]*&#x200B;到&#x200B;*[!UICONTROL Last 180 Days]*。 默认值为&#x200B;*[!UICONTROL Yesterday]*。

   * 对于特定范围：选择&#x200B;**[!UICONTROL Custom Date Range]** ，然后指定开始日期和结束日期。

     以MM/DD/YYYY或MM-DD-YYYY格式输入日期，或单击每个字段旁边的![日历图标](/help/search-social-commerce/assets/calendar.png "日历图标")以打开日历并选择日期。

1. （可选）比较指定日期范围的数据与第二个日期范围的数据：

   1. 将&#x200B;**[!UICONTROL Comparison]**&#x200B;滑块移动到&#x200B;*[!UICONTROL On]*。

      选择此选项时，将为每个常规数据列添加两个额外的列。 例如，该表不只包括“[!UICONTROL Impressions]”的一列，而是包括“[!UICONTROL Impressions R1]”、“[!UICONTROL Impressions R2]”和“[!UICONTROL Impressions Diff]”的列。  如果导出数据，则相同的列将拼写为“[!UICONTROL Impressions Range 1]”、“[!UICONTROL Impressions Range 2]”和“[!UICONTROL Impressions Difference]”。

   1. 指定第二个日期范围。

   1. 在“\[_数据字段_\] Difference”列中选择如何表示两个所选日期范围中的数据之间的差异：

      * *[!UICONTROL Variance]* （默认）：将差异显示为数值。

      * *[!UICONTROL % Change]：*&#x200B;以百分比显示差异。

1. 单击&#x200B;**[!UICONTROL Apply]**。
