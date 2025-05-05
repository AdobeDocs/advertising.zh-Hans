---
title: 报告的初始设置任务
description: 了解如何在报表中提供量度以及如何自动执行报表。
exl-id: c2e76c63-ddb8-4762-8628-30cf3f54b8fd
feature: Search Reports
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 报告的初始设置任务

新用户应执行以下初始设置任务：

* 使Adobe Advertising正在跟踪的广告商[的转化指标可用于报告和其他视图](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md)，并可以选择地[重命名列标题中显示的任何转化指标](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md)以便可读。

  事务属性不适用于报表，除非您特别规定它们可用。

  如果您稍后开始跟踪新的转化量度，则必须重复此任务。

* （可选）自动生成报表：

   * 如果您要定期生成特定时间增量的报表数据，如上周或最近30天的[!UICONTROL Campaign Report]，则可以设置[报表模板](/help/search-social-commerce/reports/automation/templates/template-about.md)并安排它们每天或在一周或一个月的特定日期运行。 每次计划运行报告时，都会生成一个新报告。 您可以选择在报表完成时根据[!UICONTROL Notification Center][&#128279;](/help/search-social-commerce/notifications/notification-about.md)中配置的通知设置，通知特定Search、Social和Commerce用户的电子邮件地址。

   * 如果您要在自定义格式的电子表格中查看最新的每日报表数据，无论是否具有透视表以及您需要执行进一步计算的任何其他列，则可以设置每日[电子表格馈送](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md)。 电子表格馈送每天使用最新的性能数据刷新，并继续保留以前日期的数据。 要配置电子表格馈送，您必须首先在[!DNL Microsoft Excel]中创建自定义电子表格模板。 您可以选择根据[!UICONTROL Notification Center][&#128279;](/help/search-social-commerce/notifications/notification-about.md)中配置的通知设置，在信息源文件可用时通知特定Search、Social和Commerce用户的电子邮件地址。

   * 如果您希望在FTP位置接收基本和高级报表，则可以通过请求FTP帐户并使用特定命名惯例设置报表模板来设置[对基本和高级报表的FTP访问](/help/search-social-commerce/reports/automation/ftp-reports.md)。

>[!MORELIKETHIS]
>
>* [关于报告](report-about.md)
>* [用于报表的数据](data-used-for-reports.md)
