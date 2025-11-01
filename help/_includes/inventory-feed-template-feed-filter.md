---
source-git-commit: 73c9cc7134360e073fc466dda3733cfc9bac8786
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---
# 文本广告模板 — 信息源筛选器

**\[信息源筛选器\]：**&#x200B;信息源文件中要传播的行：

* *[!UICONTROL Propagate all rows found in feed:]*（默认）以传播所有行的数据。

* *[!UICONTROL Propagate rows that meet certain conditions:]*&#x200B;只传播满足最多10个指定条件的行的数据。 指定要应用的过滤器：

   1. 选择要用于所有筛选器的布尔运算： **[!UICONTROL AND]**&#x200B;或&#x200B;**[!UICONTROL OR]**。

   1. 从第一个菜单中选择列名，从第二个菜单中选择运算符，然后输入适用的值或将输入字段留空以传播无条件的行的数据。

  列列表包含信息源中所有可用的列。

  可用的运算符包括&#x200B;*[!UICONTROL contains]*、*[!UICONTROL does not contain]*、*[!UICONTROL =]*、*[!UICONTROL <>]*（不等于）、*[!UICONTROL in]*、*[!UICONTROL not in]*、*[!UICONTROL less than]*&#x200B;和&#x200B;*[!UICONTROL greater than]*。 选择运算符“[!UICONTROL in]”时，您可以输入以逗号分隔的值列表；如果记录与任何指定的值匹配，则会传播这些行的数据。 对于所有其他运算符，仅输入一个值。 值不区分大小写。

  例如，如果您选择了“product_type”列，并且希望仅返回包含“shoes”的产品名称的行，则选择“**[!UICONTROL contains]**”并在输入字段中输入`shoes`。

   1. （要应用最多九个其他筛选器）对于每个其他筛选器，请单击&#x200B;**[!UICONTROL Add Condition]**，然后按照步骤2指定其他筛选器。
