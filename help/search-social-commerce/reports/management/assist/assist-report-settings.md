---
title: 协助报表设置
description: 了解辅助报表的必需和可选设置。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '2176'
ht-degree: 0%

---

# 协助报表设置

*具有搜索、社交和商务点击跟踪以及Adobe广告转化跟踪的广告商，Adobe Analytics(具有 [!DNL Analytics] 集成)，或使用令牌(`ef_id`)*

| 选项卡 | 参数 | 描述 |
|----|----|----|
| 不适用 | [!UICONTROL Name] | （可选）报表和模板的名称（如果将报表另存为模板）。 如果应用现有模板，则默认情况下会填充模板名称。 如果不应用模板或输入名称，则报表将命名为 `<client name>-<date and time>-<report type>` (如“acme - 2009年4月3日，11:25:19 AM PDT — 关键字”)。<br><br>您可以选择输入自定义名称，但不要使用文件扩展名。<br><br>如果要创建模板，请执行以下操作 [将报告发送到FTP目录](/help/search-social-commerce/reports/automation/ftp-reports.md)，那么您可以选择在文件名中的任意位置包含“CSV”（大写字母），以使用CSV格式而不是默认的TSV格式创建文件。 参见 [发送到FTP目录的报告的文件名要求](/help/search-social-commerce/reports/automation/ftp-reports.md). |
|  | [!UICONTROL Save as template] | （除非要根据计划运行报告，否则可选）将报告设置另存为模板，该模板可在 [!UICONTROL Reports] > [!UICONTROL Report Templates] 查看并可以重复使用来创建新报告。 要将报表另存为模板，请选中该复选框。<br><br>要根据计划运行报表，必须将设置另存为模板。<br><br><b>注意：</b> 您可以将当前参数集另存为新模板，即使它基于现有模板也是如此。 |
|  | [!UICONTROL Type] | 要生成的报表类型。 |
| [!UICONTROL Basic  Settings] | [!UICONTROL Template] | （可选）要应用的报表模板，该模板会根据模板预填充报表选项。 将为报表类型保存并且可供您使用的所有模板都将列出。<br><br>如果选择模板，您仍然可以更改报表选项，甚至可以将报表另存为新模板。 |
|  | [!UICONTROL Date Range] | 要生成数据的日期范围：<ul><li><i>[预设范围]：</i> 常用时间增量列表，范围从 <i>[!UICONTROL Today]</i> 到 <i>[!UICONTROL Last 180 Days]</i>. 默认为 <i>[!UICONTROL Last 7 Days]</i>，报告有可用数据的最近七天。 <b>注意：</b> <i>[!UICONTROL Last Month]</i>， <i>[!UICONTROL Last 3 Months]</i>、和 <i>[!UICONTROL Last 6 Months]</i> 显示前一个日历月份的数据。</li><li><i>[!UICONTROL Custom Date Range]：</i> 指定开始日期和结束日期。 以YYYY/MM/DD或M/D/YYYY格式输入日期，或单击 ![日历](/help/search-social-commerce/assets/calendar.png "日历") 在字段旁边，然后选择日期。</li></ul> |
|  | [!UICONTROL Filter By] | ([!UICONTROL Campaign Assist Report] 仅报告特定项目组合的数据还是特定广告网络的数据：<ul><li><i>[!UICONTROL Portfolio]</i> （默认）：用于在一个或多个项目组合中包含营销活动数据。</li><li><i>[!UICONTROL Search Engine]：</i> 要包含一个或多个广告网络中促销活动的数据（适用于报表类型），请执行以下操作： |
|  | \[主筛选器\] | ([!UICONTROL Campaign Assist Report] （仅限）要包含的数据组件。 如果不进行选择，则报表将包括转化路径中发生在任何适用的广告网络上的每种事件类型模式的数据行。 您可以选择过滤报告的数据，以便仅在指定组件和子组件中发生系列中的至少一个事件时才包含行。 根据您是按项目组合还是广告网络进行筛选，指定要包含的组件：<ul><li><i>[!UICONTROL Portfolio]：</i> 一个或多个项目组合或其子组件（营销活动或广告组）。 要选取元件及其所有子元件，请选中元件名称旁边的复选框。 要选择子组件，请选中子组件名称旁边的复选框，然后单击>>将其移动到 [!UICONTROL Selected Filters] 列。 例如，要获取Portfolio1及其所有促销活动和广告组的数据，请选中Portfolio1旁边的复选框。 要在Portfolio1的Campaign 1中至少发生一次事件时获取数据，请展开Portfolio1，然后仅选中Campaign 1旁边的复选框。</li><li><i>[!UICONTROL Search Engine]：</i> 一个或多个广告网络或其子组件（帐户、营销活动或广告组）。 要选择某个组件及其所有子组件，请选中组件名称旁边的复选框，然后单击>>将其移动到 [!UICONTROL Selected Filters] 列。 要选择子组件，请选中子组件名称旁边的复选框，然后单击>>将其移动到 [!UICONTROL Selected Filters] 列。 例如，在任一个事件中至少发生一次时获取数据 [!DNL Google Ads] 帐户、营销活动和广告组，选中旁边的复选框 [!DNL Google AdWords]. 在中仅获取Campaign 1的数据 [!DNL Google Ads] 帐户1，展开 [!DNL Google Ads] ，然后仅选中Campaign 1旁边的复选框。</li></ul><b>注释：</b><ul><li>要展开列表中的组件（如列出广告网络上的帐户），请单击 ![向右箭头图标](/help/search-social-commerce/assets/compressed-item.png "“向右箭头”图标") 位于组件旁边。</li><li>要查看任何项目的组件类型，请将光标悬停在该项目上。</li><li>默认情况下，仅列出a)活跃和优化的项目组合及其活跃组件，或b)活跃和启用的广告网络帐户、营销活动及其活跃组件。 要查看暂停的和删除的组件，请单击 ![向下箭头](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭头") 旁边 **[!UICONTROL Show]** 并选择 **[!UICONTROL All]**.</li><li>在按项目组合生成协助报告时，生成的数据适用于当前映射到指定项目组合的营销活动。 该报表不包括日期范围内项目组合中但不再存在的营销活动的数据。</li></ul> |
| [!UICONTROL Columns] | [!UICONTROL Use revenue and derived metrics from] | 在报表中填充以下一组默认视图（即使用最小公分母）共有的所有收入和自定义（派生）指标列：<ul><li><i>全部：</i> 要包含由所有选项卡的默认视图共享的列超集，请 [!UICONTROL Portfolios] 和 [!UICONTROL Campaigns] 视图（适用于广告商的产品配置）。</li><li><i>[!UICONTROL Portfolios]：</i> 要包含所有选项卡的默认视图共享的列，请 [!UICONTROL Portfolios] 视图。</li><li><i>[!UICONTROL Search]：</i> 要包含所有选项卡的默认视图共享的列，请 [!UICONTROL Campaigns] 视图。</li><li><i>[!UICONTROL Display]：</i> 已过时</li><li><i>[!UICONTROL Social]：</i> 已过时</li><ul><b>注释：</b><ul><li>没有可用的搜索流量量度（例如点击次数或展示次数），并且包含搜索流量量度的派生量度不可用。</li><li>您可以选择删除或重新排列任何可用的收入或派生的量度列。</li><li>尽管可以添加更多列，但已为报告预定义属性列。</li></ul> |
|  | [!UICONTROL Path Size] | 模式中项目（事件类型、关键字或投放位置、广告组或营销活动）的最小和最大数量。 默认路径大小为一(1)个或多个项目以及最多五(5)个项目。 您可以选择仅显示至少包含两(2)个或更多项目的路径。 项目类型和项目的最大数量因报告而异：<ul><li>[!UICONTROL Channel Assist Report]：逐项列出转化路径中在广告商发生的最多N个最早事件的数据 [单击回顾窗口](/help/search-social-commerce/glossary.md#c-d) 和 [展示回顾窗口](/help/search-social-commerce/glossary.md#i-j). 例如，如果您选择一(1)个或更多以及最多五(5)个事件的路径大小，则报表将包括最多包含五个事件的转化路径，每个跟踪的事件类型模式（例如“搜索点击”或“显示展示”）占一行。 您最多可以在路径中包含30个事件。</li><li>[!UICONTROL Keyword Assist Report]：逐项列出在广告商的搜索路径中发生的最多N个最早搜索关键词或投放位置的数据 [单击回顾窗口](/help/search-social-commerce/glossary.md#c-d) 和 [展示回顾窗口](/help/search-social-commerce/glossary.md#i-j). 例如，如果选择一(1)个或更多且最多五(5)个路径大小，则报表将包括最多包含五个关键字或版面的路径，并且每个跟踪的关键字字符串或版面模式都有一行。 您最多可以在路径中包含10个事件。</li><li>[!UICONTROL Campaign Assist Report]：在广告商的转化路径中详细列出最多N个发生的最早营销活动的数据 [单击回顾窗口](/help/search-social-commerce/glossary.md#c-d) 和 [展示回顾窗口](/help/search-social-commerce/glossary.md#i-j). 例如，如果您选择的路径大小为一(1)个或更多且最多五(5)，则报表将包括最多包含五个营销活动的路径，并且每个跟踪的营销活动模式都有一行。 您最多可以在路径中包含10个营销策划。</li></ul><b>注释：</b><ul><li>要查看协助报表的转化数据，必须添加相应的转化列。</li><li>当转化路径包括的事件类型、关键字或投放位置、广告组或营销活动多于您在报表中逐项统计时，则报表将包括额外的行，用于汇总因项目数量较多导致的转化数据（例如，对于由10个以上事件导致的转化，其中一行用于汇总转化数据）。</li><li>如果包含具有两个或多个项目的路径，则总路径数可能低于具有一个或多个项目的路径数总路径数。</li></ul> |
| [!UICONTROL Columns] | \[报表列\] | 报表中显示的数据列及其顺序：<ul><li>要添加列，请单击左列中的量度名称，然后单击 ![向右箭头](/help/search-social-commerce/assets/arrow-right-customize.png "向右箭头").</li><li>要删除列，请单击右列中的度量名称，然后单击 ![向左箭头](/help/search-social-commerce/assets/arrow-left-customize.png "向左箭头").</li><li>要将报表中的列向左移动，请单击右列中的量度名称，然后单击 ![向上箭头键](/help/search-social-commerce/assets/arrow-up-customize.png "向上箭头键").</li><li>要将报表中的列移动到右侧，请单击右列中的量度名称，然后单击 ![向下箭头](/help/search-social-commerce/assets/arrow-down-customize.png "向下箭头").</li></ul><p><b>注释：</b></p><ul><li>要查看辅助报表的转化数据，必须添加相应的转化列。</li><li>要仅列出特定类型的数据，请单击列表上方的任何图标：<ul><li>![属性](/help/search-social-commerce/assets/property-columns.png "属性") 用于广告网络帐户或项目组合组件的资产名称和ID，例如 [!UICONTROL Campaign Status]</li><li>![收入量度](/help/search-social-commerce/assets/revenue-metric-columns.png "收入量度") (对于为广告商跟踪的收入指标/交易属性，包括从Adobe Analytics同步的转化和网站参与指标)</li><li>![派生量度](/help/search-social-commerce/assets/derived-metric-columns.png "派生量度") 对于广告商创建的自定义派生量度</li></ul></li><li>包含许多事务属性的报表或包含许多事务属性的自定义派生量度的报表生成时间较长。</li><li>要添加、创建或编辑新量度，请参阅&quot;[创建自定义量度](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md)，&quot; &quot;[编辑自定义量度](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md)，”和“[删除自定义量度](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-delete.md).”</li><li>有关按报表类型列出的所有可用列的说明，请参阅&quot;[此[!UICONTROL Channel Assist Report]](/help/search-social-commerce/reports/management/assist/channel-assist-report.md)，&quot; &quot;[此 [!UICONTROL Campaign Assist Report]](/help/search-social-commerce/reports/management/assist/campaign-assist-report.md)，”和“[此 [!UICONTROL Keyword Assist Report]](/help/search-social-commerce/reports/management/assist/keyword-assist-report.md).”</li></ul> |
|  | [!UICONTROL Order Results/Limit Rows by] | 按报表中包含的最多两列对报表进行排序。 每种报表类型的默认值各不相同。 要自定义排序顺序，请选择一个报表列，然后选择 <i>[!UICONTROL Ascending]</i> （显示从A到Z或从1到100的结果）或 <i>[!UICONTROL Descending]</i> （显示从Z到A或从100到1的结果）。 指定至少一个要作为排序依据的列。 如果按两列排序，则报表首先按指定的第一列排序，然后按指定的第二列排序。 |
|  | [!UICONTROL Share with others] | 允许有权访问同一广告商数据的其他用户查看生成的报表，并且（如果您将报表另存为模板）使用该模板，但无法编辑或删除该模板。 默认情况下，不选中此选项。 <b>注意：</b> 无论此设置如何，您的报告和模板始终对级别较高的（管理员）Adobe的所有用户以及任何分配的管理员帐户团队成员可见。 |
|  | [!UICONTROL Indicate search engine after entity name] | ([!UICONTROL Campaign Assist Report] 仅限)将广告网络名称包含在促销活动名称后面的括号中。 示例： `<campaign name> [Google Adwords]` |
|  | [!UICONTROL Indicate account name after entity name] | ([!UICONTROL Campaign Assist  Report] 仅限)将广告网络帐户名称包含在促销活动名称后面的括号中。 示例： `<campaign name> [Google Adwords] [Account1]` |
|  | [!UICONTROL Indicate event  type after entity name] | ([!UICONTROL Campaign Assist Report] （仅限）在促销活动名称后的方括号中包含事件类型。 示例： `<campaign name> [click]` 或 `<campaign name> [Google Adwords] [Account1] [impression]` |
| [!UICONTROL Advanced Filters] | \[高级过滤器\] | ([!UICONTROL Campaign Assist Report] 仅当量度的值满足指定的条件时，才返回行；该量度无需作为列包含在报表中。 可用量度的列表因报表类型而异，但可能包括广告商的自定义派生量度，每个搜索引擎和项目组合组件的ID和属性名称(例如 [!UICONTROL Campaign ID] 和 [!UICONTROL Campaign Status])、广告商的收入量度（交易属性）以及广告网络中的点击相关量度。 可用的运算符包括 <i>[!UICONTROL contains]</i>， <i>[!UICONTROL starts with]</i>， <i>[!UICONTROL equals]</i>， <i>[!UICONTROL is greater than]</i>， <i>[!UICONTROL is greater than or equal to]</i>， <i>[!UICONTROL is less than]</i>， <i>[!UICONTROL is less than or equal to]</i>，或 <i>[!UICONTROL isn't equal to]</i>.<br><br>要应用一个或多个筛选器，请执行以下操作：<ul><li>选择量度和运算符，然后输入适用的值。 例如，要仅返回点击次数超过100次的关键字，请选择 [!UICONTROL Clicks]，选择 [!UICONTROL >]，然后在输入字段中输入100。</li><li>（要应用其他过滤器）对于每个其他过滤器，请单击 **[!UICONTROL +Add Filter]**，选择 **[!UICONTROL AND]** 或 **[!UICONTROL OR]**，选择量度和运算符，然后输入适用的值。</li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Report Schedule] | (可选；仅当&quot;[!UICONTROL Save as template]”选项处于选中状态)运行报表的时间： <i>[!UICONTROL Now]</i> （只运行一次报表；默认）， <i>[!UICONTROL Daily]</i>， <i>[!UICONTROL Weekly on] [星期]</i>，或 <i>[!UICONTROL Every Month] [日期]</i>. 对于除以下项之外的所有时间段 <i>[!UICONTROL Now]</i>，选择广告商时区中的小时，从上午9:00开始。 |
|  | [!UICONTROL Email Recipients] | <b>注意：</b>  此设置仅在电子邮件通知用于 [!UICONTROL Reports] 是 [启用范围 [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-edit.md).<br><br>Search、Social和Commerce注册用户的电子邮件地址，当报告完成或由于错误被取消时，将通知发送到这些用户。 默认情况下，会输入用户帐户的地址。 要指定多个地址，请用逗号、空格或新行分隔这些地址。 如果计划重复运行报告，则每次完成报告时都会发送通知。 |
|  | [!UICONTROL Email Notification] | <b>注意：</b>  此设置仅在电子邮件通知用于 [!UICONTROL Reports] 是 [启用范围 [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-edit.md).<br><br>(时间 [!UICONTROL Email Recipients] （已指定）向任何指定地址发送电子邮件通知时要包含的内容：<ul><li><i>[!UICONTROL Notification Only]</i> （默认）：仅发送报表完成或失败的通知，不带附件。 该通知包括所有报表格式的临时下载链接。</li><li><i>[!UICONTROL XLS Attachment]：</i> 在文件小于约10 MB时包括XLS格式的已完成报表的副本。 超过1 MB的文件将被压缩。</li><li><i>[!UICONTROL TSV Attachment]：</i> 在文件小于约10 MB时包括TSV格式的已完成报表的副本。 超过1 MB的文件将被压缩。</li><li><i>[!UICONTROL CSV Attachment]：</i> 在文件小于约10 MB时包括CSV格式已完成的报表的副本。 超过1 MB的文件将被压缩。 |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [此 [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [此 [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [此 [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [生成协助报告](assist-report-generate.md)
>* [关于报告](/help/search-social-commerce/reports/report-about.md)
