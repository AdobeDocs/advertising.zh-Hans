---
title: 通过FTP访问报表
description: 了解如何在只读FTP位置接收报表。
exl-id: eca9f033-5b1b-4afa-926b-b4c31e2dede3
feature: Search Reports
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# 通过FTP访问报表

您可以选择在只读FTP位置接收报表，从中检索文件以进行其他自动化流程（例如，使用其他程序解析数据）。 除以下各项外的所有基本报表： [!UICONTROL Search Engine Account Report] 并且所有高级报表都可以作为压缩的TSV文件（默认）或扩展名为.ZIP的CSV文件传送到FTP位置。 包含任何TSV或CSV文件标头，并且无法隐藏。

使用FTP访问报表需要访问指定的FTP帐户，并且您必须使用特定的命名惯例和计划来设置报表模板。

## 设置FTP帐户以访问报表

* 请联系您的Adobe帐户团队，以设置FTP帐户以进行报表访问。

  团队为您提供用户名和密码。

## 为FTP传递设置报表模板

要在指定的FTP目录中生成报告，请创建 [报告模板](templates/template-create.md) 使用下列命名约定和时间表。

>[!NOTE]
>
>所有高级报告和所有基本报告，但 [!UICONTROL Search Engine Account Report] 可传送到FTP位置。

1. 在报表模板中，将以下信息包含到模板名称中的任何位置：

   * `FTP` （使用大写字母）。

   * （可选）使用以下区分大小写的语法（包括括号），选择三个系统日期中的任一日期：

      * `[TODAY]`  — 包括运行报告的日期、小时和分钟。 由于其中包含确切时间，因此同一模板可以每天运行多次，而不会覆盖以前的报表。

      * `[SDATE]`  — 包括报告日期范围的开始日期。

      * `[EDATE]`  — 包括报告日期范围的结束日期。

   * （可选） `[CSV]` （大写字母并括在括号中）以CSV格式而不是默认的TSV格式创建文件。

   示例： `[TODAY]-Portfolio-FTP-[SDATE]-[EDATE]-[CSV]` 将创建类似202305051656-Portfolio-FTP-20230428-20110504.csv的文件。

1. 安排报表在特定时间运行。

   报表在完成后的一小时内会被发送到FTP帐户。

>[!NOTE]
>
>* 要通过电子邮件发送已完成的报告，只需在生成报告或模板时输入所有电子邮件收件人的地址即可。
>* 报表会根据其指定的计划运行，并在完成后一小时内传送到FTP帐户。

## 访问FTP存储库中的报表

要访问报表，请使用FTP帐户的登录名连接到以下FTP主机之一(`amo<userID>rpt`，例如amo1234rpt)和密码或专用连接密钥（如果已设置）：

* 国际客户： `ftp3.adobe.net`
* 美国客户： `ftp5.adobe.net`

>[!NOTE]
>
>报告存储库为只读，每15天清除一次。


>[!MORELIKETHIS]
>
>* [创建报表模板](/help/search-social-commerce/reports/automation/templates/template-create.md)
