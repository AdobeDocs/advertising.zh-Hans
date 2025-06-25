---
title: 关于报告
description: 了解性能报表，包括可用的不同报表类型以及如何自动执行报表。
exl-id: 173d1bad-e3aa-4417-a9b1-4b5d06c304d2
feature: Search Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 0%

---

# 关于报告

性能报告允许您在任意精细的级别跟踪和管理项目组合、广告网络和广告网络帐户实体的性能。 通过大多数报表，可以全面了解每个营销渠道中的广告对整体转化率的贡献情况。

每次运行报表时，都会动态编译报表数据。 您可以选择从现有报表生成新报表。 可用的报告参数因报告类型而异。 对于大多数报表，您可以选择预览前50行，而不是生成整个报表。 生成报告时，您可以在报告完成时发送包含一个或多个电子邮件地址下载链接的通知，收件人可以在[!UICONTROL Notification Center][&#128279;](/help/search-social-commerce/notifications/notification-about.md)中管理通知。

所有完成的报表都位于[!UICONTROL Reports]视图的[!UICONTROL Latest Reports]部分，您可以在浏览器窗口中以表格式查看它们，或者以文件形式打开或下载它们。

## 可用的报表类别

[!UICONTROL Reports]视图中提供了以下报表类别。 您可能无权访问所有这些报表；可用的报表及其生成的数据取决于您的角色以及客户帐户的配置方式。

| 报告类别 | 描述 |
| ----| ---- |
| [!UICONTROL Basic Reports] | 适用于所有用户的[基本报表](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)显示项目组合、广告网络帐户、特定广告网络帐户、促销活动、广告组、广告、关键字、产品组、标签分类和标签值、竞价单位约束以及网络约束的实际成本和点击数据。 它们基于适用广告网络计价的点击量，并且可以选择包括转化数据或您创建的任何其他量度。 |
| [!UICONTROL Advanced Reports] | [高级报告](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)为您的广告配置提供了额外的insight，帮助您确定通过更改地理定位或网络设置可获益的位置。 它们还可以帮助您对照广告商的内部转化跟踪数据，验证促销活动以及产品组合管理视图和报告中的转化数据。 |
| [!UICONTROL Assist Reports] | [协助报表](/help/search-social-commerce/reports/management/assist/assist-report-about.md)分析广告商所有关键词和广告的转化路径。 它们使用通过Adobe Advertising转化跟踪服务捕获的数据，并且只能为该服务的广告商生成。 |
| [!UICONTROL Specialty Reports] | [专业报告](/help/search-social-commerce/reports/management/specialty/specialty-report-about.md)包含由广告网络收集的数据(而不是由Adobe Advertising跟踪收集的数据)。 |
| [!UICONTROL Model Accuracy Reports] | [模型准确性报表](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)指明用于优化项目组合竞价、促销活动预算和竞价策略目标的成本和收入模型的准确性。 |

## 报告自动化

计划通过以下任一方式或同时使用以下两种方式自动生成自定义报表：

* 使用[报告模板](/help/search-social-commerce/reports/automation/templates/template-about.md)每天或在一周或一个月中的特定日期自动生成报告。

  您可以选择设置使用模板的基本报表和高级报表的[FTP传送](/help/search-social-commerce/reports/automation/ftp-reports.md)。

* 使用[电子表格馈送](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md)，使用每日性能数据继续刷新您的自定义电子表格模板。

## 报告视图

位于[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Insights & Reports] > [!UICONTROL Reports]的[!UICONTROL Reports]视图允许您创建和管理报告、模板和电子表格馈送。 该视图包含两个选项卡：

* **[!UICONTROL Latest Reports]**&#x200B;选项卡列出了过去7天内请求的所有可用报告，手动删除的报告除外，默认情况下最新报告位于顶部。 每个报表显示的信息包括运行计划（如果适用）、生成或将生成数据的开始和结束日期以及报表状态（*[!UICONTROL Finished]*、*[!UICONTROL In Progress]*&#x200B;或&#x200B;*[!UICONTROL Error]*）。

  通过每个报表旁边的链接，您可以在Web浏览器中查看该报表，或者将其打开或另存为[!DNL Microsoft Excel]工作簿(XLS)或制表符分隔值(TSV)文件；某些报表类型还可以另存为[!UICONTROL Excel]工作簿，并为每个适用的营销活动使用单独的工作表。

  通过此选项卡，您还可以创建新报告（可以选择用作模板），根据现有报告的设置创建新报告，通过删除来取消您可用的正在进行的报告，以及删除您可用的任何已完成报告。 超过7天的报表将被自动删除。

* **[!UICONTROL Templates]**&#x200B;选项卡列出了所有已保存的基本和高级报告模板，包括与它们关联的任何计划有关的信息。 默认情况下，最新模板位于顶部。

  在此选项卡中，您可以创建新模板，编辑您创建的任何模板（包括添加、更改或删除其计划），从模板生成报告，以及删除任何可供您使用的模板。

## 如何使用报表

| 用途 | 报表 |
| ---- | ---- |
| 性能监控 | <ul><li>[该[!UICONTROL Portfolio Report]](/help/search-social-commerce/reports/management/basic-advanced/portfolio-report.md)</li><li>[该[!UICONTROL Search Engine Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-report.md)</li><li>[该[!UICONTROL Search Engine Account Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[该[!UICONTROL Campaign Report]](/help/search-social-commerce/reports/management/basic-advanced/campaign-report.md)</li><li>[该[!UICONTROL Ad Group Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-group-report.md)</li><li>[该[!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| 性能故障排除和趋势分析 | <ul><li>[该[!UICONTROL Keyword Report]](/help/search-social-commerce/reports/management/basic-advanced/keyword-report.md)</li><li>[该[!UICONTROL Ad Variation Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-variation-report.md)</li><li>[该[!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)</li><li>[该[!UICONTROL RSA Asset Report]](/help/search-social-commerce/reports/management/specialty/rsa-asset-report.md)</li><li>[该[!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/keyword-daily-impression-share-report.md)和[该[!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>使用“[!UICONTROL Compare with]”功能比较两个时间窗口的任何基本报告</li></ul> |
| 识别业务增长机会 | <ul><li>(仅具有Adobe Advertising转化跟踪的广告商) [该[!UICONTROL Geo Distribution Report]](/help/search-social-commerce/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(仅具有Adobe Advertising转化跟踪的广告商) [该[!UICONTROL Domain Referral Report]](/help/search-social-commerce/reports/management/basic-advanced/domain-referral-report.md)</li><li>(具有[Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)的广告商)Adobe Analytics Analysis Workspace中的自定义报表</li></ul> |
| 分析 | <ul><li>(仅具有Adobe Advertising转化跟踪的广告商) [该[!UICONTROL Channel Assist Report]](/help/search-social-commerce/reports/management/assist/channel-assist-report.md)</li><li>(具有[Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)的广告商)Adobe Analytics Analysis Workspace中的自定义报表</li></ul> |

>[!MORELIKETHIS]
>
>* [用于报表的数据](data-used-for-reports.md)
>* [报告的初始设置任务](initial-setup.md)
>* [生成基本或高级报告](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [生成模型准确性报告](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-generate.md)
>* [生成专业报告](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md)
>* [生成协助报告](/help/search-social-commerce/reports/management/assist/assist-report-generate.md)
