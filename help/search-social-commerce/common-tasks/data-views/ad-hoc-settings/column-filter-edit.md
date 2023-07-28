---
title: 编辑列筛选条件
description: 了解如何编辑列过滤器。
exl-id: 6e42e006-089b-44b9-b9b1-66835b680413
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# 编辑列筛选条件

## 编辑过滤器集

1. 单击 ![筛选](/help/search-social-commerce/assets/filter.png "筛选") 工具栏中。

1. 在筛选器设置中，执行以下任一操作：

   * 要添加过滤器，请单击 ![添加筛选器](/help/search-social-commerce/assets/add.png "添加筛选器") **[!UICONTROL ADD FILTER]** ，然后执行以下操作：

      1. （可选）要按文本字符串筛选列名，请在 **[!UICONTROL ADD FILTER]** 输入字段。

      1. 从列菜单中选择列名。

      1. 在列上定义过滤器：

         * （没有输入字段的筛选器）单击 ![向下箭头](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭头") 在第二个菜单旁边，选中要包含的每个值旁边的复选框，然后单击 ![更新筛选器](/help/search-social-commerce/assets/select.png "更新筛选器").

         * （带有输入字段的筛选器）从第二个菜单中选择一个运算符，输入适用的值，然后单击 ![更新筛选器](/help/search-social-commerce/assets/select.png "更新筛选器").

           例如，如果您选择了&quot;[!UICONTROL Clicks]”列并希望仅返回点击超过100次的行，然后选择 *[!UICONTROL greater than]*”并输入 `100` 在输入字段中。

           根据数据类型，可用的运算符可能包括 *[!UICONTROL greater than]*， *[!UICONTROL less than]*， *[!UICONTROL equals]*， *[!UICONTROL contains]*， *[!UICONTROL doesn't contain]*， *[!UICONTROL starts with]*， *[!UICONTROL ends with]*， *[!UICONTROL no value]*，或 *[!UICONTROL has value]*， *[!UICONTROL before]*， *[!UICONTROL after]*，或 *[!UICONTROL no date].*

           **注意：** 文本值不区分大小写。 例如，如果您搜索名称中包含“loan”的促销活动，则结果将包含“Consumer Loans”和“loan applications”。

   * 要编辑现有筛选器，请单击该筛选器，更改筛选器定义，然后单击 ![更新筛选器](/help/search-social-commerce/assets/select.png "更新筛选器").

   * 要删除现有筛选器，请单击 **[!UICONTROL X]** 位于筛选器定义旁边。

1. ([!UICONTROL Keywords] 仅查看；可选)选择或取消选择设置为&quot;[!UICONTROL Include rows with no performance data]“

   >[!WARNING]
   >
   >选择此选项将增加页面加载时间。

1. 单击 **[!UICONTROL Apply]**.

## 编辑单个筛选器

1. （如有必要）在数据表上方的过滤器集中，单击 ![更多](/help/search-social-commerce/assets/more-filters.png "更多") 以展开过滤器集。

1. 在数据表上方，单击过滤器定义。

1. 编辑要应用的过滤器：

   1. （可选）从列菜单中编辑列名。

   1. （可选）在列上重新定义过滤器：

      * （没有输入字段的筛选器）单击 ![向下箭头](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭头") 在第二个菜单旁边，选中要包含的每个值旁边的复选框，然后单击 ![更新筛选器](/help/search-social-commerce/assets/select.png "更新筛选器").

      * （带有输入字段的筛选器）从第二个菜单中选择一个运算符，输入适用的值，然后单击 ![更新筛选器](/help/search-social-commerce/assets/select.png "更新筛选器").

        例如，如果您选择了&quot;[!UICONTROL Clicks]”列并希望仅返回点击超过100次的行，然后选择 *[!UICONTROL greater than]*”并输入 `100` 在输入字段中

        根据数据类型，可用的运算符可能包括 *[!UICONTROL greater than]*， *小于*， *[!UICONTROL equals]*， *[!UICONTROL contains]*， *不包含*，或 *开头是。*

        **注意：** 文本值不区分大小写。 例如，如果您搜索名称中包含“loan”的促销活动，则结果将包含“Consumer Loans”和“loan applications”。
