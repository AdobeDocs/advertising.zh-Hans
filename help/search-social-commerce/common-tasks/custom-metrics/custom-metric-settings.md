---
title: 自定义量度设置
description: 引用自定义量度的设置，这些量度是通过标准量度计算的。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 0%

---

# 自定义量度设置

自定义量度设置在界面的不同部分略有不同。

## 营销活动管理视图中的自定义量度设置

| 参数/节 | 描述 |
|----|----|
| 自定义量度名称 | 度量的名称，显示为列名。 <b>提示：</b> 请使用有意义的量度名称，但请考虑使用较长的名称会使列更宽。 |
| 插入量度 | 用于计算新量度的数学公式(例如 [成本]/[注册]：<ul><li>要从流量和收入量度列表中插入量度，请将光标放在要插入量度的位置，然后从列表中选择该量度，或手动输入该量度并将其括在括号中(例如， `[CPC]`)。</li><li>要插入运算符，请将光标放在要插入运算符的位置，然后单击按钮或手动输入符号。 可用的数学运算符： `+ - * / ( ) ()`</li></ul><b>注意：</b> 计算复杂的自定义量度需要更长的时间，并且包含这些量度的报表和视图（尤其是当它们包含用于点进和浏览转换的单独列时）的生成时间更长。 |
| 格式 | 如何显示此指标的数据： *[!UICONTROL Currency]* （货币价值）， *[!UICONTROL Number to 2 Decimal Points]*， *[!UICONTROL Number to 3 Decimal Points]*， *[!UICONTROL Number w/out Decimal Points]*，或 *[!UICONTROL Percentage]* （具有两个小数点的百分比）。<br><br><b>注意：</b> 如果您使用格式创建派生量度 [!UICONTROL Number w/out Decimal Points] （将数据显示为整数），并将其包含在使用加权转化归因规则([!UICONTROL Weight First Event More]， [!UICONTROL Weight Last Event More]，或 [!UICONTROL Even Distribution])，则输出将以整数而不是小数形式显示。 因此，即使总计是正确的，单个数据字段也可能不正确。 例如，如果一个顺序平均分配到三个事件中，则一个顺序（而不是0.33顺序）将归因于三个事件的每个。 要防止出现此问题，请使用量度格式 [!UICONTROL Number to 2 Decimal Points]. |

## 报表、报表模板和 [!UICONTROL Portfolios] 查看次数

| 参数/节 | 描述 |
|----|----|
| 自定义量度名称 | 度量的名称，显示为列名。 <b>提示：</b> 请使用有意义的量度名称，但请考虑使用较长的名称会使列更宽。 |
| 格式 | 如何显示此指标的数据： *[!UICONTROL Currency]* （货币价值）， *[!UICONTROL Number to 2 Decimal Points]*， *[!UICONTROL Number to 3 Decimal Points]*， *[!UICONTROL Number w/out Decimal Points]*，或 *[!UICONTROL Percentage]* （具有两个小数点的百分比）。<br><br><b>注意：</b> 如果您使用格式创建派生量度 [!UICONTROL Number w/out Decimal Points] （将数据显示为整数），并将其包含在使用加权转化归因规则([!UICONTROL Weight First Event More]， [!UICONTROL Weight Last Event More]，或 [!UICONTROL Even Distribution])，则输出将以整数而不是小数形式显示。 因此，即使总计是正确的，单个数据字段也可能不正确。 例如，如果一个顺序平均分配到三个事件中，则一个顺序（而不是0.33顺序）将归因于三个事件的每个。 要防止出现此问题，请使用量度格式 [!UICONTROL Number to 2 Decimal Points]. |
| 插入量度 | 可从中创建公式的现有量度列表。<br><br>要在公式输入字段中插入指标，请将光标放在要插入指标的位置，然后从列表中选择指标或手动输入指标并将其括在括号中(例如， `[CPC]`)。 |
| 插入运算符 | 可用的数学运算符： `+ - x / ( )`<br><br>要在公式输入字段中插入运算符，请将光标放在要插入运算符的位置，然后单击按钮或手动输入符号。 |
| [量度的公式输入字段] | 用于根据一个或多个现有属性或标准量度(例如 `[Cost]/[Registrations]`. 它可以包含量度和运算符的任意组合。<br><br><b>注意：</b> 计算复杂的自定义量度需要更长的时间，并且包含这些量度的报表和视图（尤其是当它们包含用于点进和浏览转换的单独列时）的生成时间更长。 |

>[!MORELIKETHIS]
>
>* [关于自定义量度](custom-metric-about.md)
>* [创建自定义量度](custom-metric-create.md)
>* [编辑自定义量度](custom-metric-edit.md)
>* [删除自定义量度](custom-metric-delete.md)

