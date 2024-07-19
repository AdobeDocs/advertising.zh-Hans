---
title: 编辑列筛选条件
description: 了解如何编辑列过滤器。
exl-id: 68f816ea-cde2-4df0-b46c-f47fa20a2727
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# 编辑列筛选条件

## 编辑过滤器集

1. 单击工具栏中的![筛选器](/help/search-social-commerce/assets/filter.png "筛选器")。

1. 在筛选器设置中，执行以下任一操作：

   * 要添加筛选器，请单击![添加筛选器](/help/search-social-commerce/assets/add.png "添加筛选器") **[!UICONTROL ADD FILTER]**，然后执行以下操作：

      1. （可选）要按文本字符串筛选列名，请在&#x200B;**[!UICONTROL ADD FILTER]**&#x200B;输入字段中输入搜索字符串。

      1. 从列菜单中选择列名。

      1. 在列上定义过滤器：

         * （不带输入字段的筛选器）单击第二个菜单旁边的![向下箭头](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭头")，选中要包含的每个值旁边的复选框，然后单击![更新筛选器](/help/search-social-commerce/assets/select.png "更新筛选器")。

         * （包含输入字段的筛选器）从第二个菜单中选择运算符，输入适用的值，然后单击![更新筛选器](/help/search-social-commerce/assets/select.png "更新筛选器")。

           例如，如果已选择“[!UICONTROL Clicks]”列并且只想返回点击次数超过100次的行，请选择“*[!UICONTROL greater than]*”并在输入字段中输入`100`。

           根据数据类型，可用运算符可能包括&#x200B;*[!UICONTROL greater than]*、*[!UICONTROL less than]*、*[!UICONTROL equals]*、*[!UICONTROL contains]*、*[!UICONTROL doesn't contain]*、*[!UICONTROL starts with]*、*[!UICONTROL ends with]*、*[!UICONTROL no value]*&#x200B;或&#x200B;*[!UICONTROL has value]*、*[!UICONTROL before]*、*[!UICONTROL after]*&#x200B;或&#x200B;*[!UICONTROL no date]。*

           **注意：**&#x200B;文本值不区分大小写。 例如，如果您搜索名称中包含“loan”的促销活动，则结果将包含“Consumer Loans”和“loan applications”。

   * 要编辑现有筛选器，请单击该筛选器，更改筛选器定义，然后单击![更新筛选器](/help/search-social-commerce/assets/select.png "更新筛选器")。

   * 要删除现有筛选器，请单击筛选器定义旁边的&#x200B;**[!UICONTROL X]**。

1. （[!UICONTROL Keywords]仅查看；可选）选择或取消选择“[!UICONTROL Include rows with no performance data]”的设置。

   >[!WARNING]
   >
   >选择此选项将增加页面加载时间。

1. 单击&#x200B;**[!UICONTROL Apply]**。

## 编辑单个筛选器

1. （如有必要）在数据表上方的筛选器集中，单击![更多](/help/search-social-commerce/assets/more-filters.png "更多")以展开筛选器集。

1. 在数据表上方，单击过滤器定义。

1. 编辑要应用的过滤器：

   1. （可选）从列菜单中编辑列名。

   1. （可选）在列上重新定义过滤器：

      * （不带输入字段的筛选器）单击第二个菜单旁边的![向下箭头](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭头")，选中要包含的每个值旁边的复选框，然后单击![更新筛选器](/help/search-social-commerce/assets/select.png "更新筛选器")。

      * （包含输入字段的筛选器）从第二个菜单中选择运算符，输入适用的值，然后单击![更新筛选器](/help/search-social-commerce/assets/select.png "更新筛选器")。

        例如，如果已选择“[!UICONTROL Clicks]”列并且只想返回点击次数超过100次的行，请选择“*[!UICONTROL greater than]*”并在输入字段中输入`100`

        根据数据类型，可用的运算符可能包括&#x200B;*[!UICONTROL greater than]*、*小于*、*[!UICONTROL equals]*、*[!UICONTROL contains]*、*不包含*&#x200B;或&#x200B;*开头为。*

        **注意：**&#x200B;文本值不区分大小写。 例如，如果您搜索名称中包含“loan”的促销活动，则结果将包含“Consumer Loans”和“loan applications”。
