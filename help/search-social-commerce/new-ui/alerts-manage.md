---
title: （新UI）管理自定义警报
description: 了解如何创建、配置、暂停、激活、删除、查看和导出自定义警报和警报模板。
feature: Search Alerts
source-git-commit: 0fddeb8f01bd7c310544973ae2aff78339eb2144
workflow-type: tm+mt
source-wordcount: '1065'
ht-degree: 0%

---

# （新UI）管理自定义警报

创建警报模板，以识别在指定时间段内，任何项目组合、营销活动或广告组何时满足特定条件（例如绩效指标），然后生成警报。 警报适用于单个广告商。 警报包括相关默认视图中的所有列。 例如，营销活动级别的警报包含默认[!UICONTROL Campaigns]视图中的所有列。

您可以从[!UICONTROL Custom Alerts]面板的[!UICONTROL Alert Templates]选项卡或任何页面顶部创建警报模板。

为警报模板触发警报实例时：

* 指定的收件人将收到电子邮件通知。 当警报包含最多1000条记录时，电子邮件通知包含一个包含警报数据的[CSV](/help/search-social-commerce/glossary.md#c-d)文件，其中包括触发警报的所有实体的数据。

* 警报列在[!UICONTROL Custom Alert Templates]面板的[!UICONTROL Triggered Alerts]选项卡中。<!-- Not available as of 5/22 for alerts triggered the day before:  A downloadable report is available for ten days after the alert is triggered. -->

<!-- This doesn't seem to be true as of 5/22 -- check on this behavior:    * The alert is listed in the [!UICONTROL Notifications] center in the applicable entity view, which is available from the right toolbar. Notifications remain in the [!UICONTROL Notifications] center unless you delete them or mark them as read. -->

## [!UICONTROL Custom Alerts]视图

要打开[!UICONTROL Custom Alerts]面板，请单击右上角的![自定义警报](/help/search-social-commerce/assets/custom-alert.png "自定义警报")。

[!UICONTROL Custom Alerts]面板包括[!UICONTROL Alert Templates]视图，该视图列出了为帐户创建的所有警报模板，您可以从中创建、编辑、暂停、重新激活和删除警报模板。 [!UICONTROL Triggered Alerts]视图列出了生成的警报实例。

## 可用操作

* [查看触发的警报](#alert-view)

* [查看自定义警报模板](#alert-template-view)

* [创建自定义警报模板](#alert-template-create)

* [编辑自定义警报模板](#alert-template-edit)

* [暂停自定义警报模板](#alert-template-pause)

* [激活自定义警报模板](#alert-template-activate)

* [删除自定义警报模板](#alert-template-delete)

<!-- Not available as of 5/22:  * [Export data for triggered alerts](#alert-export-data) -->

## 查看触发的警报 {#alert-view}

1. 单击任意页面右上角的![自定义警报](/help/search-social-commerce/assets/custom-alert.png "自定义警报")。

1. 单击&#x200B;**[!UICONTROL Triggered Alerts]**&#x200B;选项卡。

1. （可选）筛选列表以包含特定实体类型的警报，或在模板名称中搜索文本字符串。 搜索查询不区分大小写。

## 查看自定义警报模板 {#alert-template-view}

1. 在任意页面的右上角，单击![自定义警报](/help/search-social-commerce/assets/custom-alert.png "自定义警报")，此时将打开到[!UICONTROL Alert Templates]选项卡。

1. （可选）筛选列表以包含特定实体类型的警报，或在模板名称中搜索文本字符串。 搜索查询不区分大小写。

1. （可选）要查看警报模板的所有条件，请单击条件数（如![示例自定义警报条件按钮](/help/search-social-commerce/assets/custom-alert-criteria.png "示例自定义警报条件按钮")）。

## 创建自定义警报模板 {#alert-template-create}

新警报模板的状态为“[!UICONTROL Active]”。

1. 执行以下任一操作：

   * 单击任意页面右上角的![自定义警报](/help/search-social-commerce/assets/custom-alert.png "自定义警报") > **[!UICONTROL Create Custom Alert]**。

   在任意页面的右上角，单击![自定义警报](/help/search-social-commerce/assets/custom-alert.png "自定义警报") > **[!UICONTROL View Custom Alerts]**，这将打开到[!UICONTROL Alert Templates]选项卡。 单击&#x200B;**[!UICONTROL Create Alert]**。

1. 在&#x200B;**[!UICONTROL Entity]**、**[!UICONTROL Date Range]**、**[!UICONTROL Filters]**&#x200B;和&#x200B;**[!UICONTROL Scheduling and Delivery]**&#x200B;选项卡上指定[警报设置](#alert-template-settings)。

   您可以通过单击选项卡名称（如“筛选器”）或单击右下角的&#x200B;**[!UICONTROL Next]**&#x200B;在选项卡之间移动。

1. 在[!UICONTROL Summary]选项卡上，单击&#x200B;**[!UICONTROL Create Alert]**。

## 编辑自定义警报模板 {#alert-template-edit}

1. 单击右上角的![自定义警报](/help/search-social-commerce/assets/custom-alert.png "自定义警报") > **[!UICONTROL View Custom Alerts]**，此时将打开到[!UICONTROL Alert Templates]选项卡。

1. （可选）筛选列表以包含特定实体类型的警报，或在模板名称中搜索文本字符串。 搜索查询不区分大小写。

1. 单击模板名称旁边的![编辑](/help/search-social-commerce/assets/edit-new.png "编辑")。

1. 在[!UICONTROL Edit Custom Alert]窗口中，编辑&#x200B;**[!UICONTROL Date Range]**、**[!UICONTROL Filters]**&#x200B;和&#x200B;**[!UICONTROL Scheduling and Delivery]**&#x200B;选项卡上的[警报设置](#alert-template-settings)。

   您可以通过单击选项卡名称（如“筛选器”）或单击右下角的&#x200B;**[!UICONTROL Next]**&#x200B;在选项卡之间移动。

1. 在[!UICONTROL Summary]选项卡上，单击&#x200B;**[!UICONTROL Update Alert]**。

## 暂停自定义警报模板 {#alert-template-pause}

1. 单击右上角的![自定义警报](/help/search-social-commerce/assets/custom-alert.png "自定义警报") > **[!UICONTROL View Custom Alerts]**，此时将打开到[!UICONTROL Alert Templates]选项卡。

1. （可选）筛选列表以包含特定实体类型的警报，或在模板名称中搜索文本字符串。 搜索查询不区分大小写。

1. 在模板行中，选择&#x200B;*[!UICONTROL Paused]*。

## 激活自定义警报模板 {#alert-template-activate}

1. 单击右上角的![自定义警报](/help/search-social-commerce/assets/custom-alert.png "自定义警报") > **[!UICONTROL View Custom Alerts]**，此时将打开到[!UICONTROL Alert Templates]选项卡。

1. （可选）筛选列表以包含特定实体类型的警报，或在模板名称中搜索文本字符串。 搜索查询不区分大小写。

1. 在模板行中，选择&#x200B;*[!UICONTROL Active]*。

## 删除自定义警报模板 {#alert-template-delete}

您只能删除您创建的警报模板。

1. 单击右上角的![自定义警报](/help/search-social-commerce/assets/custom-alert.png "自定义警报") > **[!UICONTROL View Custom Alerts]**，此时将打开到[!UICONTROL Alert Templates]选项卡。

1. （可选）筛选列表以包含特定实体类型的警报，或在模板名称中搜索文本字符串。 搜索查询不区分大小写。

1. 在模板行中，单击![删除](/help/search-social-commerce/assets/delete-new.png "删除")。

1. 在确认消息框中，单击&#x200B;**[!UICONTROL Delete]**。

## 自定义警报模板设置 {#alert-template-settings}

| 选项卡 | 参数 | 描述 |
|--- |--- |--- |
|  | [!UICONTROL Name] | 警报名称。 必须至少包含五个字符。 |
| [!UICONTROL Date Range] | [!UICONTROL Select Entity] | 要计算的实体类型： <i>[!UICONTROL Portfolio]</i>、<i>[!UICONTROL Campaign]</i>或<i>[!UICONTROL Ad Group]</i>。 |
| [!UICONTROL Date Range] | [!UICONTROL Period] | 评估警报条件的日期范围。 将在日期范围内对指标进行汇总评估。 选项范围从&#x200B;*[!UICONTROL Yesterday]*&#x200B;到&#x200B;*[!UICONTROL Last 180 Days]*。 |
| [!UICONTROL Filters] | \[定义的筛选器\] | 在[!UICONTROL Scheduling and Delivery]选项卡上指定的时间触发警报的条件。 可用列因图元类型而异。 所有过滤器都使用布尔函数AND进行连接，这意味着必须满足所有指定的条件。<ul><li><p>要添加过滤器，请执行以下操作：<p><ol><li><p>（可选）要按文本字符串筛选列名，请在[!UICONTROL ADD FILTER]输入字段中输入搜索字符串。</p></li><li><p>在列列表中，选择一个列名。</p></li><li><p>在列上定义过滤器：</p></li><ul><li><p>（不带输入字段的筛选器）单击第二个菜单旁边的![向下箭头](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭头")，然后选中要包含的每个值旁边的复选框。</p></li><li><p>（具有输入字段的所有其他筛选器）从第二个菜单中选择运算符，然后输入适用的值。</p><p>例如，如果您选择了“点击量”列并且只想返回点击量超过100次的行，请选择“大于”并在输入字段中输入100。</p><p>根据数据类型，可用运算符可能包括<i>大于</i>、<i>小于</i>、<i>等于</i>、<i>包含</i>、<i>不包含</i>、<i>开头为</i>、<i>结尾为</i>、<i>无值</i>、<i>具有值</i>、<i>在</i>之前、<i>在</i>之后，或<i>无日期</i>。</p><p>**注意：**&#x200B;文本值不区分大小写。 例如，如果按名称中包含“loan”的促销活动进行过滤，则结果可能包括“Consumer Loans”和“loan application”。</p></li></ol><li><p>要删除筛选器，请单击筛选器定义旁边的![删除](/help/search-social-commerce/assets/delete.png "删除")。</p></li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Trigger this Alert] \[when\] | 警报检查指定条件过滤器的频率，并在满足所有条件时发送电子邮件通知：<ul><li><p>[!UICONTROL Daily at <*NN*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Weekly on <*每周时间*> &lt;*NN*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Every month on <*第NN*>天&lt;*NN*> `[AM\|PM]`]</p></li></ul>**注意：**&#x200B;此值不会影响评估期。 |
|  | [!UICONTROL Email Recipients] | （仅警报模板的创建者可编辑；其他每个人仅可编辑）触发警报时要向其发送通知的已注册Search、Social和Commerce用户。 默认情况下，会选择用户帐户的名称。 （可选）添加或删除有权访问广告商数据的用户。<br><br>当警报包含最多1000条记录时，会将CSV版本的警报附加到电子邮件中。 |

<!--

Not available as of 5/22:

## Export data for triggered alerts {#alert-export-data}

You can export data for a triggered alert or data for the most recently triggered alert for an alert template as a [!DNL Microsoft Excel] workbook ([XLS](/help/search-social-commerce/glossary.md#w-x) file), a tab-separated values ([TSV](/help/search-social-commerce/glossary.md#s-t)) file, or a comma-separated values ([CSV](/help/search-social-commerce/glossary.md#c-d)) file. Downloadable reports are available for ten days after the alert is triggered and are then automatically deleted.

1. Do either of the following:

   * (To export data for the most recently triggered alert for an alert template) In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert") > **[!UICONTROL View Custom Alerts]**, which opens to the [!UICONTROL Alert Templates] tab.

   * (To export data for a specific triggered alert) In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert"). Click **[!UICONTROL Triggered Alerts]**.

1. In the [!UICONTROL Export] column next to the template or report name, click the name of a format, and then open or save the file according to your browser's normal procedure:

   * **[!UICONTROL XLS]:** For an [!DNL Excel] workbook with a single worksheet (XLS). The report includes one worksheet, labeled at the top with the parameters, with one row for each included component when data for the component is available. Rows with no data are omitted. Basic reports include a total for each numeric column.

   * **[!UICONTROL TSV]:** For a TSV file. The report includes the parameters and one row for each included component.

   * **[!UICONTROL CSV]:** For a CSV file. The report includes the parameters and one row for each included component.

-->
