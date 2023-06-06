---
title: 自定义警报模板设置
description: 了解自定义警报模板的设置。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# 自定义警报模板设置

| 选项卡 | 参数 | 描述 |
|--- |--- |--- |
| [!UICONTROL Date Range] | [!UICONTROL Date] | 评估警报条件的日期范围。 量度会在日期范围内进行汇总评估。 选项范围包括 *[!UICONTROL Yesterday]* 到 *[!UICONTROL Last 180 Days]*. |
| [!UICONTROL Filters] |  | 在上指定的时间触发警报的条件 [!UICONTROL Scheduling and Delivery] 选项卡。 可用列因实体类型（如营销策划或关键词）而异。 所有过滤器都使用布尔函数AND进行连接，这意味着必须满足所有指定的条件。<ul><li><p>要添加过滤器，请单击 ![向下箭头](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭头") 旁边 ![添加](/help/search-social-commerce/assets/add.png "添加") **[!UICONTROL ADD FILTER]**，然后执行以下操作：</p></li><ol><li><p>（可选）要按文本字符串筛选列名，请在 **[!UICONTROL ADD FILTER]** 输入字段。</p></li><li><p>从列菜单中选择一个列名。</p></li><li><p>在列上定义过滤器：</p></li><ul><li><p>（没有输入字段的筛选器）单击 ![向下箭头](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭头") ，然后选中要包含的每个值旁边的复选框。</p></li><li><p>（要跟踪其值在指定日期范围和上一时段之间增加或减少的量度列）对于运算符，选择 *增加* 或 *减少*，然后输入阈值。</p><p>例如，如果您选择了&quot;[!UICONTROL Cost]”列，并希望在任何营销活动的成本增加21%时收到警报，然后选择“[!UICONTROL increases by]”并在输入字段中输入21。 在 [!UICONTROL Date Comparison Format] 字段，表示您对百分比的更改（而不是货币单位的更改）感兴趣。</p><p>选择此选项时，将为每个常规数据列添加两个附加列。 例如，报表不只包括“点击数”的一列，而是包括“点击次数R1”（适用于范围1）“点击次数R2”（适用于范围2）以及“点击数差异”或“点击数差异(%)”的列，具体取决于指定的 [!UICONTROL Date Comparison Format] （见下文）。</p><p>**注释：**</p><ul><li><p>对于派生量度，不会填充差异列。<p></li><li><p>此功能不适用于属性名称、ID或标签分类列。</p></li><li><p>比较大日期范围的报表可能需要更长的时间才能生成。</p></li></ul></ul><li><p>（具有输入字段的所有其他筛选器）从第二个菜单中选择一个运算符，然后输入适用的值。</p><p>例如，如果您选择了“点击量”列，并且只想返回点击量超过100次的行，请选择“大于”并在输入字段中输入100。</p><p>根据数据类型，可用的运算符可能包括 <i>大于</i>， <i>小于</i>， <i>等于</i>， <i>包含</i>， <i>不包含</i>， <i>开头为</i>， <i>结束于</i>， <i>无值</i>， <i>具有值</i>， <i>早于</i>， <i>之后</i>，或 <i>无日期</i>.</p><p>**注意：** 文本值不区分大小写。 例如，如果按名称中包含“loan”的促销活动进行筛选，则结果可能包括“Consumer Loans”和“loan applications”。</p></li></ol><li><p>要删除筛选器，请单击 ![删除](/help/search-social-commerce/assets/delete.png "删除") 位于筛选器定义旁边。</p></li></ul> |
|  | [!UICONTROL Comparing] | （当警报跟踪在一个或多个量度列中增加或减少时可用；只读）比较数据的两个日期范围。 |
|  | [!UICONTROL Date Comparison Format] | （当警报跟踪在一个或多个指标列中增加或减少时可用）如何表示两个日期范围中的数据之间的差异：<ul><li><p><i>[!UICONTROL Variance]</i> （缺省） — 将差值显示为数值。</p></li><li><p><i>[!UICONTROL % Change]</i>  — 以百分比显示差异。</p></li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Name] | 警报名称。 它必须至少包含五个字符。 |
|  | [!UICONTROL Trigger this Alert] [时间] | 警报检查指定条件过滤器的频率，并在满足所有条件时发送电子邮件通知：<ul><li><p>[!UICONTROL Daily at <*NN*> [AMPM]]</p></li><li><p>[!UICONTROL Weekly on <*Day of Week*> at <*NN*> [AMPM]]</p></li><li><p>[!UICONTROL Every month on <*Day NN*> at <*NN*> [AMPM]]</p></li></ul>**注意：** 此值不会影响评估期。 |
|  | [!UICONTROL Email Recipients] | （仅警报模板的创建者可编辑；其他所有人仅可编辑）生成警报时用于发送通知的电子邮件地址。 默认情况下，会输入模板创建者的地址。<br><br>要添加地址，请输入地址，然后单击 **[!UICONTROL Add]**. 要指定多个地址，请使用逗号或空格分隔这些地址，或者单独添加它们。<br><br>当警报包含最多1000条记录时，会将警报的CSV版本附加到电子邮件中。 |

>[!MORELIKETHIS]
>
>* [关于自定义警报](alert-about.md)
>* [创建自定义警报模板](alert-template-create.md)
>* [编辑自定义警报模板](alert-template-edit.md)
>* [暂停自定义警报模板](alert-template-pause.md)
>* [激活自定义警报模板](alert-template-activate.md)
>* [删除自定义警报模板](alert-template-delete.md)
>* [查看自定义警报](alert-view.md)
>* [导出自定义警报的数据](alert-export-data.md)

