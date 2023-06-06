---
title: 从列标题菜单应用数据筛选器
description: 了解如何从列标题菜单中筛选页面数据。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# 从列标题菜单应用数据过滤器

您可以对列应用所需数量的过滤器，一次应用一个。 所有过滤器都使用AND运算符连接。 要使用所有可用量度一次添加多个过滤器，请参阅&quot;[从工具栏应用数据过滤器](column-filter-apply-from-toolbar.md).”

1. 在列标题的右侧，单击 ![向下箭头](/help/search-social-commerce/assets/arrow-down-dropdown.png "向下箭头")，然后单击 **[!UICONTROL Add Filter]**.

1. 在列上定义过滤器：

   * （不带输入字段的筛选器）选中要包含的每个值旁边的复选框，然后单击 ![更新筛选器](/help/search-social-commerce/assets/select.png "更新筛选器").

   * （带有输入字段的筛选器）从第二个菜单中选择一个运算符，输入适用的值，然后单击 ![更新筛选器](/help/search-social-commerce/assets/select.png "更新筛选器").

      例如，如果您选择了&quot;[!UICONTROL Clicks]“ ”列并希望仅返回点击超过100次的行，然后选择 *[!UICONTROL greater than]*”并输入 `100` 在输入字段中根据数据类型，可用的运算符可能包括 *[!UICONTROL greater than]*， *[!UICONTROL less than]*， *[!UICONTROL equals]*， *[!UICONTROL contains]*， *[!UICONTROL doesn't contain]*， *[!UICONTROL starts with]*， *[!UICONTROL ends with]*， *[!UICONTROL no value]*， *[!UICONTROL has value]*， *[!UICONTROL before]*， *[!UICONTROL after]*，或 *[!UICONTROL no date].*

      >[!NOTE]
      >
      >* 文本值不区分大小写。 例如，如果按名称中包含“loan”的促销活动进行筛选，则结果会包括“Consumer Loans”和“loan applications”。
      >* 您只能应用一个简单数字过滤器(例如 [!UICONTROL Impressions] \> 100)。

