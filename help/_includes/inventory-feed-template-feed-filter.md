---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---
# 文本广告模板 — 信息源筛选器

**\[信息源筛选器\]：** 要传播的信息源文件中的哪些行：

* *[!UICONTROL Propagate all rows found in feed:]* （默认）为所有行传播数据。

* *[!UICONTROL Propagate rows that meet certain conditions:]* 只传播满足最多10个指定条件的行的数据。 指定要应用的过滤器：

   1. 选择要用于所有过滤器的布尔运算：  **[!UICONTROL AND]** 或 **[!UICONTROL OR]**.

   1. 从第一个菜单中选择列名，从第二个菜单中选择运算符，然后输入适用的值或将输入字段留空以传播无条件的行的数据。

   列列表包含信息源中所有可用的列。

   可用的运算符包括 *[!UICONTROL contains]*， *[!UICONTROL does not contain]*， *[!UICONTROL =]*， *[!UICONTROL <>]* （不等于）， *[!UICONTROL in]*， *[!UICONTROL not in]*， *[!UICONTROL less than]*、和 *[!UICONTROL greater than]*. 当您选择运算符“[!UICONTROL in]，”您可以输入以逗号分隔的值列表；如果记录与任何指定的值匹配，则会传播这些行的数据。 对于所有其他运算符，只输入一个值。 值不区分大小写。

   例如，如果您选择了“product_type”列，并且只想为包含“shoes”的产品名称返回行，请选择“**[!UICONTROL contains]**”并输入 `shoes` 在输入字段中。

   1. （要应用最多九个其他过滤器）对于每个其他过滤器，请单击 **[!UICONTROL Add Condition]**，然后按照步骤2指定附加过滤器。
