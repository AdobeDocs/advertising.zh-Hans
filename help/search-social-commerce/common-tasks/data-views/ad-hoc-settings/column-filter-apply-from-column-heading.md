---
title: 从列标题菜单应用数据过滤器
description: 了解如何从列标题菜单中筛选页面数据。
exl-id: 508f254a-d859-4155-9bbd-84e0442f01d5
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a438e0c24f9ff83941710f890c55c94b74d4d0f3
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# 从列标题菜单应用数据过滤器

<!-- The same in new UI and legacy CM views -->

<!-- Doesn't include instructions for legacy Portfolios or Reports views -->

您可以对列应用所需数量的过滤器，一次应用一个。<!-- True only for entity names, I think: All filters are joined using the AND operator. -->要使用所有可用量度一次添加多个筛选器，请参阅[应用工具栏中的数据筛选器](column-filter-apply-from-toolbar.md)。

1. 单击列标题右侧的![向下箭头](/help/search-social-commerce/assets/arrow-down-dropdown.png "向下箭头")，然后单击&#x200B;**[!UICONTROL Add Filter]**。

1. 在列上定义过滤器：

   * （不带输入字段的筛选器）选中要包含的每个值旁边的复选框，然后单击![更新筛选器](/help/search-social-commerce/assets/select.png "添加")。

   * （带有输入字段的筛选器）从第二个菜单中选择运算符，输入适用的值，然后单击![更新筛选器](/help/search-social-commerce/assets/select.png "添加")。

     例如，如果您选择了“[!UICONTROL Clicks]”列并且希望仅返回点击超过100次的行，请选择“*[!UICONTROL greater than]*”并在输入字段中输入`100`根据数据类型，可用运算符可能包括&#x200B;*[!UICONTROL greater than]*、*[!UICONTROL less than]*、*[!UICONTROL equals]*、*[!UICONTROL contains]*、*[!UICONTROL doesn't contain]*、*[!UICONTROL starts with]*、*[!UICONTROL ends with]*、*[!UICONTROL no value]*、*[!UICONTROL has value]*、*[!UICONTROL before]*、*[!UICONTROL after]*&#x200B;或&#x200B;*[!UICONTROL no date]。*

     >[!NOTE]
     >
     >* 文本值不区分大小写。 例如，如果按名称中包含“loan”的促销活动进行筛选，则结果将包含“Consumer Loans”和“loan application”。
     >* 每列只能应用一个简单数字过滤器（如[!UICONTROL Impressions] \> 100）。

>[!MORELIKETHIS]
>
>* [从工具栏应用数据筛选器](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)
>* [编辑列筛选器](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-edit.md)
>* [删除列筛选器]&#x200B;(/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/
