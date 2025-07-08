---
title: 从工具栏应用数据过滤器
description: 了解如何从工具栏筛选页面数据。
exl-id: fc1dca75-b0e5-48fd-90ee-f09c158e3e8b
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a89a6513dfe468b98513b2d47c086a3107e63d47
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# 从工具栏应用数据过滤器

<!-- Doesn't include instructions for legacy Portfolios view; not available in Reports views -->

您可以对视图应用任意数量的筛选器。<!-- True only for entity names, I think: All filters are joined using the AND operator. -->

## （新UI）在管理视图中应用工具栏中的数据筛选器

1. 在工具栏中，单击![筛选器](/help/search-social-commerce/assets/filter-new.png "筛选器")。

1. 在筛选器设置中，执行以下任一操作：

   * 要添加筛选器，请单击&#x200B;**[!UICONTROL ADD FILTER]**，然后执行以下操作：

      1. （可选）要按文本字符串筛选列名，请在&#x200B;**[!UICONTROL ADD FILTER]**&#x200B;输入字段中输入搜索字符串。

      1. 从列菜单中选择列名。

      1. 在列上定义过滤器：

         * （不带输入字段的筛选器）单击第二个菜单旁边的![向下箭头](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭头")，然后选中要包含的每个值旁边的复选框。

         * （带有输入字段的筛选器）从第二个菜单中选择运算符，然后输入适用的值。

           例如，如果已选择“[!UICONTROL Clicks]”列并且只想返回点击次数超过100次的行，请选择“*[!UICONTROL greater than]*”并在输入字段中输入`100`。

           根据数据类型，可用运算符可能包括&#x200B;*[!UICONTROL greater than]*、*[!UICONTROL less than]*、*[!UICONTROL equals]*、*[!UICONTROL contains]*、*[!UICONTROL doesn't contain]*、*[!UICONTROL starts with]*、*[!UICONTROL ends with]*、*[!UICONTROL no value]*、*[!UICONTROL has value]*、*[!UICONTROL before]*、*[!UICONTROL after]*&#x200B;或&#x200B;*[!UICONTROL no date]。*

           **注意：**&#x200B;文本值不区分大小写。 例如，如果按名称中包含“loan”的促销活动进行筛选，则结果将包含“Consumer Loans”和“loan application”。

   * 要编辑现有筛选器，请单击该筛选器，然后更改筛选器定义。

   * 要删除现有筛选器，请单击筛选器定义旁边的&#x200B;**[!UICONTROL -]**。

## （旧版UI）在营销活动管理视图中应用工具栏中的数据过滤器

1. 在工具栏中，单击![筛选器](/help/search-social-commerce/assets/filter.png "筛选器")。

1. 在筛选器设置中，执行以下任一操作：

   * 要添加筛选器，请单击![添加筛选器](/help/search-social-commerce/assets/add.png "添加筛选器") **[!UICONTROL ADD FILTER]**，然后执行以下操作：

      1. （可选）要按文本字符串筛选列名，请在&#x200B;**[!UICONTROL ADD FILTER]**&#x200B;输入字段中输入搜索字符串。

      1. 从列菜单中选择列名。

      1. 在列上定义过滤器：

         * （不带输入字段的筛选器）单击第二个菜单旁边的![向下箭头](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭头")，然后选中要包含的每个值旁边的复选框。

         * （带有输入字段的筛选器）从第二个菜单中选择运算符，然后输入适用的值。

           例如，如果已选择“[!UICONTROL Clicks]”列并且只想返回点击次数超过100次的行，请选择“*[!UICONTROL greater than]*”并在输入字段中输入`100`。

           根据数据类型，可用运算符可能包括&#x200B;*[!UICONTROL greater than]*、*[!UICONTROL less than]*、*[!UICONTROL equals]*、*[!UICONTROL contains]*、*[!UICONTROL doesn't contain]*、*[!UICONTROL starts with]*、*[!UICONTROL ends with]*、*[!UICONTROL no value]*、*[!UICONTROL has value]*、*[!UICONTROL before]*、*[!UICONTROL after]*&#x200B;或&#x200B;*[!UICONTROL no date]。*

           **注意：**&#x200B;文本值不区分大小写。 例如，如果按名称中包含“loan”的促销活动进行筛选，则结果将包含“Consumer Loans”和“loan application”。

         * （仅限[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、[!UICONTROL Product Groups]、[!UICONTROL Placements]和[!UICONTROL Auto Targets]视图；可选）将设置更改为“[!UICONTROL Include rows with performance data only]”。

           **警告：**&#x200B;如果取消选择该选项，并且视图包含许多没有性能数据的实体，则显示数据需要更长的时间。

   * 要编辑现有筛选器，请单击该筛选器，然后更改筛选器定义。

   * 要删除现有的筛选器，请单击筛选器定义旁边的![删除](/help/search-social-commerce/assets/delete.png "删除")。

1. 单击&#x200B;**[!UICONTROL Apply]**。

>[!MORELIKETHIS]
>
>* [从列标题菜单应用数据筛选器](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)
>* [编辑列筛选器](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-edit.md)
>* [删除列筛选器]&#x200B;(/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/
