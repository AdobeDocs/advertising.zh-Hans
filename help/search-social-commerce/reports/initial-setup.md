---
title: 报告的初始设置任务
description: 了解如何在报表中提供量度以及如何自动执行报表。
exl-id: 0f55aae9-6898-4967-a377-190a13dff6fd
feature: Search Reports
source-git-commit: 82023f8c0fc72cc7993c238116fff3c0b4180221
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# 报告的初始设置任务

新用户应执行以下初始设置任务：

* 制定Adobe Advertising正在跟踪的广告商转化量度 [可用于报告和其他视图](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-available.md)和（可选） [重命名任何转化量度](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) 列标题中显示的内容以提高可读性。

  事务属性不适用于报表，除非您特别规定它们可用。

  如果您稍后开始跟踪新的转化量度，则需要重复此任务。

* （可选）自动生成报表：

   * 如果要定期生成特定时间增量的报表数据，例如 [!UICONTROL Campaign Report] 对于上周或最近30天，您可以设置 [报告模板](/help/search-social-commerce/reports/automation/templates/template-about.md) 并安排它们每天运行或在一周或一月中的特定日期运行。 每次计划运行报告时，都会生成一个新报告。 报表完成后，您可以选择根据电子邮件通知特定Search、Social和Commerce用户的电子邮件地址。 [在中配置的通知设置 [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * 如果您要在自定义格式的电子表格中查看最新的每日报表数据，无论是否具有数据透视表以及您需要执行进一步计算的任何其他列，则可以设置每日 [电子表格馈送](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md). 电子表格馈送每天使用最新的性能数据刷新，并继续保留以前日期的数据。 要配置电子表格馈送，您必须先在中创建自定义电子表格模板 [!DNL Microsoft Excel]. 您可以选择在信息源文件可用时根据电子邮件通知特定Search、Social和Commerce用户的电子邮件地址。 [在中配置的通知设置 [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * 如果您希望在FTP位置接收基本和高级报表，则可以设置 [通过FTP访问基本报表和高级报表](/help/search-social-commerce/reports/automation/ftp-reports.md) 通过请求FTP帐户并使用特定命名惯例设置报表模板。

>[!MORELIKETHIS]
>
>* [关于报告](report-about.md)
>* [用于报表的数据](data-used-for-reports.md)
