---
title: （新UI）报表的初始设置任务
description: 了解如何在报表中提供量度以及如何自动执行报表。
feature: Search Reports
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e246c273-d720-4ece-b29b-7aaba7d50169
source-git-commit: 18f4c5afafd63a6ae9421bf80b4e5b5fd424ed86
workflow-type: tm+mt
source-wordcount: 357
ht-degree: 0%

---

# （新UI）报表的初始设置任务

新用户应执行以下初始设置任务：

* 使Adobe Advertising跟踪的广告商转化量度可用于报表和其他视图，还可以选择重命名列标题中显示的任何转化量度以提高可读性。 请参阅&quot;[管理和查看广告商转化量度](/help/search-social-commerce/new-ui/goals/conversions/conversion-metrics-manage.md)的性能数据。&quot;

  事务属性不适用于报表，除非您特别规定它们可用。

  如果您稍后开始跟踪新的转化量度，则必须重复此任务。

* （可选）自动生成报表：

   * 如果您要定期生成特定时间增量的报表数据，如上周或最近30天的[!UICONTROL Campaign Report]，则可以设置[报表模板](report-templates-manage.md)并安排它们每天或在一周或一个月的特定日期运行。 每次计划运行报告时，都会生成一个新报告。 您可以选择在报表完成时根据[!UICONTROL Notification Center]&rbrack;[Manage custom alerts]&#x200B;(/help/search-social-commerce/new-ui/notifications-manage.md)中配置的&lbrack;通知设置通知特定Search、Social和Commerce用户的电子邮件地址。

   * 如果您要在自定义格式的电子表格中查看最新的每日报表数据，无论是否具有透视表以及您需要执行进一步计算的任何其他列，则可以设置每日[电子表格馈送](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md)。 电子表格馈送每天使用最新的性能数据刷新，并继续保留以前日期的数据。 要配置电子表格馈送，您必须首先在[!DNL Microsoft Excel]中创建自定义电子表格模板。 您可以选择根据[!UICONTROL Notification Center][&#128279;](/help/search-social-commerce/new-ui/notifications-manage.md)中配置的通知设置，在信息源文件可用时通知特定Search、Social和Commerce用户的电子邮件地址。

   * 如果您希望在FTP位置接收基本和高级报表，则可以通过请求FTP帐户并使用特定命名惯例设置报表模板来设置[对基本和高级报表的FTP访问](/help/search-social-commerce/new-ui/reports/ftp-reports.md)。

>[!MORELIKETHIS]
>
>* [关于报告](report-about.md)
>* [用于报表的数据](data-used-for-reports.md)
