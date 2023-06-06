---
title: 关于报告
description: 了解性能报表，包括可用的不同报表类型以及如何自动执行报表。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---

# 关于报告

性能报表允许您在任意精细的级别跟踪和管理项目组合、广告网络和广告网络帐户实体的性能。 通过大多数报表，可以全面了解每个营销渠道中的广告对整体转化率的贡献情况。

每次运行报表时，都会动态编译报表数据。 您可以选择从现有报表生成新报表。 可用的报告参数因报告类型而异。 对于大多数报表，您可以选择预览前50行，而不是生成整个报表。 在生成报告时，您可以在报告完成时发送包含一个或多个电子邮件地址下载链接的通知，收件人可以 [在中管理通知 [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

所有已完成的报表均可在 [!UICONTROL Latest Reports] 部分 [!UICONTROL Reports] 在浏览器窗口中以表格格式查看它们，或者打开它们或将其下载为文件。

## 可用的报表类别

以下报表类别可从 [!UICONTROL Reports] 视图。 您可能无权访问所有这些报表；可用的报表及其生成的数据取决于您的角色和客户帐户的配置方式。

| 报告类别 | 描述 |
| ----| ---- |
| [!UICONTROL Basic Reports] | [基本报告](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)，适用于所有用户)都会显示项目组合、广告网络帐户、特定广告网络帐户、促销活动、广告组、广告、关键字、产品组、标签分类和标签值、竞价单位约束以及网络约束的实际成本和点击数据。 它们基于适用广告网络计费的点击量，并且可以选择包括转化数据或您创建的任何其他量度。 |
| [!UICONTROL Advanced Reports] | [高级报告](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) 提供对广告配置的更多洞察，帮助您确定通过更改地理定位或网络设置可以获得哪些好处。 它们还可以帮助您根据广告商的内部转化跟踪数据验证营销活动和项目组合管理视图和报告中的转化数据。 |
| [!UICONTROL Assist Reports] | [协助报表](/help/search-social-commerce/reports/management/assist/assist-report-about.md) 提供对所有广告商关键词和广告的转化路径的洞察。 它们使用通过Adobe广告转化跟踪服务捕获的数据，并且只能为使用该服务的广告商生成。 |
| [!UICONTROL Specialty Reports] | [专业报告](/help/search-social-commerce/reports/management/specialty/specialty-report-about.md) 由广告网络收集的数据(而不是Adobe广告跟踪收集的数据)组成。 |
| [!UICONTROL Model Accuracy Reports] | [模型准确性报表](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) 指示用于优化竞价的成本和收入模型的准确性。 |

## 报告自动化

安排通过以下任一方式或同时采用以下两种方式自动生成自定义报告：

* 每天或在一周或一个月中的某一天自动生成报告，使用 [报告模板](/help/search-social-commerce/reports/automation/templates/template-about.md).

   您可以选择设置 [通过FTP提交基本和高级报告](/help/search-social-commerce/reports/automation/ftp-reports.md) 使用模板的。

* 使用每日性能数据刷新自定义电子表格模板，使用 [电子表格馈送](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md).

## 报告视图

此 [!UICONTROL Reports] 查看时间 [!UICONTROL Search] > [!UICONTROL Insights & Reports] > [!UICONTROL Reports] 允许您创建和管理报表、模板和电子表格源。 该视图包含两个选项卡：

* 此 **[!UICONTROL Latest Reports]** 选项卡列出了过去7天内请求的所有可供您使用的报告，但手动删除的报告除外，默认情况下，最新报告位于顶部。 每个报表显示的信息包括运行报表所依据的计划（如果适用）、生成或将生成数据的起始日期和终止日期以及报表状态(*[!UICONTROL Finished]*， *[!UICONTROL In Progress]*，或 *[!UICONTROL Error]*)。

   通过每个报告旁边的链接，您可以在Web浏览器中查看报告，或者将其打开或另存为 [!DNL Microsoft Excel] 工作簿(XLS)或制表符分隔值(TSV)文件；某些报表类型也可以另存为 [!UICONTROL Excel] 工作簿，每个适用的促销活动都有一个单独的工作表。

   通过此选项卡，您还可以创建新报告（可以选择用作模板），根据现有报告的设置创建新报告，通过删除进行中的报告来取消这些报告，并删除任何可供您使用的已完成报告。 超过7天的报表将被自动删除。

* 此 **[!UICONTROL Templates]** 选项卡列出了所有可供您使用的已保存的基本和高级报表模板，包括有关与其关联的任何计划的信息。 默认情况下，最新模板位于顶部。

   在此选项卡中，您可以创建新模板，编辑您创建的任何模板（包括添加、更改或删除其计划），从模板生成报告，以及删除任何可供您使用的模板。

## 如何使用报告

| 用途 | 报告 |
| ---- | ---- |
| 性能监控 | <ul><li>[此 [!UICONTROL Portfolio Report]](/help/search-social-commerce/reports/management/basic-advanced/portfolio-report.md)</li><li>[此 [!UICONTROL Search Engine Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-report.md)</li><li>[此 [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[此 [!UICONTROL Campaign Report]](/help/search-social-commerce/reports/management/basic-advanced/campaign-report.md)</li><li>[此 [!UICONTROL Ad Group Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-group-report.md)</li><li>[此 [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| 性能故障排除和趋势分析 | <ul><li>[此 [!UICONTROL Keyword Report]](/help/search-social-commerce/reports/management/basic-advanced/keyword-report.md)</li><li>[此 [!UICONTROL Ad Variation Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-variation-report.md)</li><li>[此 [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)</li><li>[此 [!UICONTROL RSA Asset Report]](/help/search-social-commerce/reports/management/specialty/rsa-asset-report.md)</li><li>[此 [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/keyword-daily-impression-share-report.md) 和 [此 [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>使用“”比较两个时间窗口的任何基本报表[!UICONTROL Compare with]”功能</li></ul> |
| 识别业务增长机会 | <ul><li>(仅具有Adobe广告转化跟踪的广告商) [此 [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(仅具有Adobe广告转化跟踪的广告商) [此 [!UICONTROL Domain Referral Report]](/help/search-social-commerce/reports/management/basic-advanced/domain-referral-report.md)</li><li>(广告商使用 [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html))Adobe Analytics Analysis Workspace中的自定义报表</li></ul> |
| 分析 | <ul><li>(仅具有Adobe广告转化跟踪的广告商) [此 [!UICONTROL Channel Assist Report]](/help/search-social-commerce/reports/management/assist/channel-assist-report.md)</li><li>(广告商使用 [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html))Adobe Analytics Analysis Workspace中的自定义报表</li></ul> |

>[!MORELIKETHIS]
>
>* [用于报表的数据](data-used-for-reports.md)
>* [报告的初始设置任务](initial-setup.md)
>* [生成基本或高级报告](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [生成模型准确性报告](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-generate.md)
>* [生成专业报告](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md)
>* [生成协助报告](/help/search-social-commerce/reports/management/assist/assist-report-generate.md)

