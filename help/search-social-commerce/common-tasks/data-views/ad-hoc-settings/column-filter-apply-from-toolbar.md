---
title: 从工具栏应用数据过滤器
description: 了解如何从工具栏筛选页面数据。
exl-id: 922cc148-e6dc-428b-a7f3-1da3780df326
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# 从工具栏应用数据过滤器

您可以根据自己的需要为视图应用任意数量的过滤器。 所有过滤器都使用AND运算符进行连接。

1. 在工具栏中，单击 ![筛选](/help/search-social-commerce/assets/filter.png "筛选").

1. 在筛选器设置中，执行以下任一操作：

   * 要添加过滤器，请单击 ![添加筛选器](/help/search-social-commerce/assets/add.png "添加筛选器") **[!UICONTROL ADD FILTER]**，然后执行以下操作：

      1. （可选）要按文本字符串筛选列名，请在 **[!UICONTROL ADD FILTER]** 输入字段。

      1. 从列菜单中选择列名。

      1. 在列上定义过滤器：

         * （没有输入字段的筛选器）单击 ![向下箭头](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭头") ，然后选中要包含的每个值旁边的复选框。

         * （带有输入字段的筛选器）从第二个菜单中选择运算符，然后输入适用的值。

           例如，如果您选择了&quot;[!UICONTROL Clicks]”列并希望仅返回点击超过100次的行，然后选择 *[!UICONTROL greater than]*”并输入 `100` 在输入字段中。

           根据数据类型，可用的运算符可能包括 *[!UICONTROL greater than]*， *[!UICONTROL less than]*， *[!UICONTROL equals]*， *[!UICONTROL contains]*， *[!UICONTROL doesn't contain]*， *[!UICONTROL starts with]*， *[!UICONTROL ends with]*， *[!UICONTROL no value]*， *[!UICONTROL has value]*， *[!UICONTROL before]*， *[!UICONTROL after]*，或 *[!UICONTROL no date].*

           **注意：** 文本值不区分大小写。 例如，如果按名称中包含“loan”的促销活动进行筛选，则结果将包含“Consumer Loans”和“loan application”。

         * ([!UICONTROL Ad Groups]， [!UICONTROL Keywords]， [!UICONTROL Product Groups]， [!UICONTROL Placements]、和 [!UICONTROL Auto Targets] 仅限视图；可选)将设置更改为&quot;[!UICONTROL Include rows with performance data only]“

           **警告：** 如果取消选择选项，并且视图包含许多没有性能数据的实体，则显示数据需要更长的时间。

   * 要编辑现有筛选器，请单击该筛选器，更改筛选器定义，然后单击 ![更新筛选器](/help/search-social-commerce/assets/select.png "更新筛选器").

   * 要删除现有筛选器，请单击 **[!UICONTROL X]** 位于筛选器定义旁边。

1. 单击 **[!UICONTROL Apply]**.
