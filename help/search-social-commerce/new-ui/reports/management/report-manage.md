---
title: 管理计划报表
description: 了解如何管理计划报表。
feature: Search Reports, Search Basic Reports, Search Advanced Reports, Search Assist Reports, Search Model Accuracy Reports, Search Specialty Reports
source-git-commit: bfca434eacf52ec7236804c54b7740442aa12961
workflow-type: tm+mt
source-wordcount: '1571'
ht-degree: 0%

---

# 管理计划报表

性能报告允许您在任意精细的级别跟踪和管理项目组合、广告网络和广告网络帐户实体的性能。 通过大多数报表，可以全面了解每个营销渠道中的广告对整体转化率的贡献情况。

每次运行报表时，都会动态编译报表数据。 您可以选择从现有报表生成新报表。 可用的报告参数因报告类型而异。 对于大多数报表，您可以选择预览前50行，而不是生成整个报表。 生成报告时，您可以在报告完成时发送包含一个或多个电子邮件地址下载链接的通知，收件人可以在[!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md)中[管理通知。

所有完成的报表都位于[!UICONTROL Reports]视图的[!UICONTROL Latest Reports]部分，您可以在浏览器窗口中以表格式查看它们，或者以文件形式打开或下载它们。

## 可用的报表类别

[!UICONTROL Reports]视图中提供了以下报表类别。 您可能无权访问所有这些报表；可用的报表及其生成的数据取决于您的角色以及客户帐户的配置方式。

| 报告类别 | 描述 |
| ----| ---- |
| [!UICONTROL Basic Reports] | 适用于所有用户的[基本报表](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md)显示项目组合、广告网络帐户、特定广告网络帐户、促销活动、广告组、广告、关键字、产品组、标签分类和标签值、竞价单位约束以及网络约束的实际成本和点击数据。 它们基于适用广告网络计价的点击量，并且可以选择包括转化数据或您创建的任何其他量度。 |
| [!UICONTROL Advanced Reports] | [高级报告](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md)为您的广告配置提供了额外的insight，帮助您确定通过更改地理定位或网络设置可获益的位置。 它们还可以帮助您对照广告商的内部转化跟踪数据，验证促销活动以及产品组合管理视图和报告中的转化数据。 |
| [!UICONTROL Assist Reports] | [协助报表](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-about.md)分析广告商所有关键词和广告的转化路径。 它们使用通过Adobe Advertising转化跟踪服务捕获的数据，并且只能为该服务的广告商生成。 |
| [!UICONTROL Specialty Reports] | [专业报告](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-about.md)包含由广告网络收集的数据（而不是由Adobe Advertising跟踪收集的数据）。 |
| [!UICONTROL Model Accuracy Reports] | [模型准确性报表](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-about.md)指明用于优化项目组合竞价、促销活动预算和竞价策略目标的成本和收入模型的准确性。 |

## 报告自动化

计划通过以下任一方式或同时使用以下两种方式自动生成自定义报表：

* 使用[报告模板](/help/search-social-commerce/reports/automation/templates/template-about.md)每天或在一周或一个月中的特定日期自动生成报告。

  您可以选择设置使用模板的基本报表和高级报表的[FTP传送](/help/search-social-commerce/new-ui/reports/ftp-reports.md)。

* 使用[电子表格馈送](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md)，使用每日性能数据继续刷新您的自定义电子表格模板。

## [!UICONTROL Scheduled Reports]次查看

[!UICONTROL Reports] > [!UICONTROL Scheduled Reports]视图允许您创建和管理报告和报告模板：

* **[!UICONTROL Latest Reports]**&#x200B;选项卡列出了所有可供您使用的报告<!-- Doesn't seem to be true: that were requested in the last seven days -->，手动删除的报告除外，默认情况下最新报告位于顶部。 每个报表显示的信息包括运行计划（如果适用）、生成或将生成数据的开始和结束日期、创建报表的人员以及报表状态（*[!UICONTROL Finished]*、*[!UICONTROL In Progress]*&#x200B;或&#x200B;*[!UICONTROL Error]*）。

  通过每个报表旁边的链接，可打开报表或将报表另存为[!DNL Microsoft Excel]工作簿(XLS)、制表符分隔值(TSV)文件或逗号分隔值(CSV)文件。 某些报表类型还可以另存为[!UICONTROL Excel]工作簿，并为每个适用的营销活动使用单独的工作表。

  通过此选项卡，您还可以创建新报告（可以选择用作模板），根据现有报告的设置或使用报告模板创建新报告，通过删除报告来取消正在进行的报告，以及删除任何可用的已完成报告。

* **[!UICONTROL Templates]**&#x200B;选项卡列出了所有已保存的基本和高级报告模板，包括与它们关联的任何计划有关的信息。 默认情况下，最新模板位于顶部。

  在此选项卡中，您可以创建新模板，编辑您创建的任何模板（包括添加、更改或删除其计划），从模板生成报告，以及删除任何可供您使用的模板。

## 如何使用报表

| 用途 | 报表 |
| ---- | ---- |
| 性能监控 | <ul><li>[该[!UICONTROL Portfolio Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/portfolio-report.md)</li><li>[该[!UICONTROL Search Engine Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-report.md)</li><li>[该[!UICONTROL Search Engine Account Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[该[!UICONTROL Campaign Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/campaign-report.md)</li><li>[该[!UICONTROL Ad Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-group-report.md)</li><li>[该[!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/new-ui/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| 性能故障排除和趋势分析 | <ul><li>[该[!UICONTROL Keyword Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/keyword-report.md)</li><li>[该[!UICONTROL Ad Variation Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-variation-report.md)</li><li>[该[!UICONTROL Transaction Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)</li><li>[该[!UICONTROL RSA Asset Report]](/help/search-social-commerce/new-ui/reports/management/specialty/rsa-asset-report.md)</li><li>[该[!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/keyword-daily-impression-share-report.md)和[该[!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>使用“[!UICONTROL Compare with]”功能比较两个时间窗口的任何基本报告</li></ul> |
| 识别业务增长机会 | <ul><li>（仅具有Adobe Advertising转化跟踪的广告商） [该[!UICONTROL Geo Distribution Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/geo-distribution-report.md)</li><li>（仅具有Adobe Advertising转化跟踪的广告商） [该[!UICONTROL Domain Referral Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/domain-referral-report.md)</li><li>（具有[Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)的广告商）Adobe Analytics Analysis Workspace中的自定义报表</li></ul> |
| 分析 | <ul><li>（仅具有Adobe Advertising转化跟踪的广告商） [该[!UICONTROL Channel Assist Report]](/help/search-social-commerce/new-ui/reports/management/assist/channel-assist-report.md)</li><li>（具有[Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)的广告商）Adobe Analytics Analysis Workspace中的自定义报表</li></ul> |

## 生成报表

### 生成新报告

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**。

1. 单击&#x200B;**[!UICONTROL Create Report]**，单击左侧面板中的报表类别，然后选择报表类型。<!-- Add link to list of report categories and report types --> 单击&#x200B;**[!UICONTROL Proceed]**。

1. （可选）在[!UICONTROL Create Report]窗口中，更改[基本和高级报告](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md)、[辅助报告](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-settings.md)、[模型准确性报告](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-settings.md)和[专业报告](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-settings.md)的默认报告设置：

   1. （可选）为报表和模板（如果将报表另存为模板）输入自定义名称。

   1. （可选）要将报表设置另存为模板，请启用&#x200B;**[!UICONTROL Save as template]**&#x200B;设置。

   1. （可选）在同一报表类别中选择其他报表&#x200B;**[!UICONTROL Type]**。

   1. （可选）在&#x200B;**[!UICONTROL Basic Settings]**&#x200B;选项卡上，选择要使用的现有报表模板或更改报表的默认基本设置。

   1. （可选）单击&#x200B;**[!UICONTROL Columns]**&#x200B;选项卡，然后更改报表中的默认列，包括列顺序。

      默认情况下，报表中的所有货币数据均以美元的格式显示（如1,000.00）。 要以正确的货币格式显示值（但不包括CSV和TSV格式中的任何货币符号），请向报表中添加“[!UICONTROL Currency]”列。 如果报表包含使用不同货币的帐户的数据，则任何“[!UICONTROL Total]”货币值都是列中所有数字的总和，而不考虑货币。

   1. （某些报表类型，可选）单击&#x200B;**[!UICONTROL Filters & Attribution]**&#x200B;或&#x200B;**[!UICONTROL Filters]**&#x200B;选项卡，然后添加数据过滤器，（某些报表类型）将报表结果限制为仅包含特定标签分类，并更改默认归因规则和转化归因设置。

   1. （可选）单击&#x200B;**[!UICONTROL Scheduling]**&#x200B;选项卡，然后更改默认计划和提交选项。

1. 单击&#x200B;**[!UICONTROL Create]**。

如果未指定报表计划，则报表将立即运行；否则，报表将按照指定的计划运行。 报告名称已添加到[[!UICONTROL Latest Reports]视图](/help/search-social-commerce/reports/report-about.md)。 如果将报表另存为模板，则它也会添加到[[!UICONTROL Templates]视图](/help/search-social-commerce/reports/report-about.md)中。 报告完成时，文件可用于打开或保存；模板可立即使用。

如果您输入了通知的电子邮件地址，则当报告作业完成或失败时，每个收件人都会根据用户为报告配置的[通知设置](/help/search-social-commerce/notifications/notification-edit.md)收到通知。

### 从现有报表生成报表

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**，这将打开到&#x200B;**[!UICONTROL Latest Reports]**&#x200B;选项卡。

1. 执行以下任一操作：

   * 将光标悬停在报告行上，然后单击&#x200B;**...** > **[!UICONTROL Duplicate]**。

   * 选中报告旁边的复选框。 在批量操作工具栏中，单击[复制](/help/search-social-commerce/assets/duplicate.png "复制")。

1. 编辑报告设置（如有必要）。

1. 单击&#x200B;**[!UICONTROL Create]**。

### 从现有模板生成报告

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**。

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 执行以下任一操作：

   * 将光标悬停在模板行上，然后单击&#x200B;**...** > **[!UICONTROL Duplicate]**。

   * 选中现有模板旁边的复选框。 在批量操作工具栏中，单击[复制](/help/search-social-commerce/assets/duplicate.png) **[!UICONTROL Duplicate]**。

1. （可选）重命名模板，并在必要时编辑报表设置。

   单击&#x200B;**[!UICONTROL Next]**&#x200B;可在设置部分之间移动。

1. 启用&#x200B;**[!UICONTROL Save as Template]**&#x200B;设置。

1. 单击&#x200B;**[!UICONTROL Create]**。

## 预览或保存报告

您可以在Web浏览器中预览报表，或者打开报表数据或将报表数据另存为[!DNL Microsoft Excel]工作簿、制表符分隔值(TSV)文件、逗号分隔值(CSV)文件或（某些报表类型）选项卡式工作簿。[!DNL Microsoft Excel]

>[!NOTE]
>
>Adobe客户团队成员和某些管理员用户可以查看由广告商和代理机构用户创建的报告。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**，这将打开到&#x200B;**[!UICONTROL Latest Reports]**&#x200B;选项卡。

1. 执行以下任一操作：

   * （要在Web浏览器中查看报表）执行以下任一操作：

      * 将光标悬停在模板行上，然后单击&#x200B;**...** > **[!UICONTROL Preview]**。

      * 选中现有模板旁边的复选框。 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Preview]**。

   * （在文件中打开或保存报告数据）在报告名称旁边的[!UICONTROL Export]列中，单击格式的名称，然后按照浏览器的正常过程打开或保存文件：

      * **[!UICONTROL XLS]：**&#x200B;对于具有单个工作表（XLSX格式）的[!DNL Excel]工作簿。 此报表包括一个位于顶部且带有参数标签的工作表，在该组件的数据可用时每个组件均报告一行。 省略没有数据的行。

        基本报表包括每个数值列的合计。

      * **[!UICONTROL TSV]：**&#x200B;用于TSV文件。 该报表包括参数以及所报告的每个组件所对应的行。

      * **[!UICONTROL CSV]：**&#x200B;用于CSV文件。 该报表包括参数以及所报告的每个组件所对应的行。

## 删除报表

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**，这将打开到&#x200B;**[!UICONTROL Latest Reports]**&#x200B;选项卡。

1. 执行以下任一操作：

   * （要删除单个报表，请执行以下操作）：

      1. 将光标悬停在报告行上，然后单击&#x200B;**...** > **[!UICONTROL Run]**。

      1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。

   * （要删除一个或多个报表）：

      1. 选中要删除的每个报告旁边的复选框。

      1. 在批量操作工具栏中，单击[删除](/help/search-social-commerce/assets/delete-new.png "删除") **[!UICONTROL Delete]**。

      1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。

<!--

>[!MORELIKETHIS]
>
>* [About basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Basic and advanced report settings](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Report columns for basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-columns.md)

-->
