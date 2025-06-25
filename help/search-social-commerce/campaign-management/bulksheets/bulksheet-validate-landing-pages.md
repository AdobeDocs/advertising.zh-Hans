---
title: 验证批量处理工作表文件中的登陆页面
description: 了解如何在单帐户批量处理工作表文件中验证目标URL。
exl-id: 191cb1bc-54a9-4c6c-a29c-f3cbae08e0d8
feature: Search Bulksheets
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# 验证批量处理工作表文件中的登陆页面

*仅具有目标URL的帐户*

您可以在单个帐户批量工作表文件中验证所有目标URL中的登陆页面。 您可以指定指示无效页面的任何短语和URL，并可以选择将登陆页面重定向报告为错误。 搜索、Social和Commerce会检查您指定的条件和缺少的登陆页面（这会导致HTTP 404或“未找到”错误）。

当发现错误时，Search、Social和Commerce会创建一个批量处理工作表错误文件，该文件包含原始批量处理工作表中的所有行，以及包含无效登陆页的所有行的错误消息。 错误记录在[!UICONTROL EF Errors]列中。 文件名约定是`<bulksheet name>__lpv_errors.<extension used for the bulksheet>`。

您可以稍后下载文件，更正错误并上传更正后的文件，然后将更正后的文件发布到广告网络帐户。

>[!NOTE]
>
>* 此功能不会验证基本URL/最终URL列中的值。
>* 您可以在验证批量工作表文件时发布这些文件，即使发现错误也是如此。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**。

1. 选中每个要验证的文件旁边的复选框。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Validate URLs]**。

1. 在对话框中，在字段中输入信息，然后单击&#x200B;**[!UICONTROL Apply]**：

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]：**&#x200B;登陆页面正文中的文本，指示该页面无效。 要指定多个值，请在单独的行中输入它们。

   **[!UICONTROL Enter invalid landing pages(one per line):]**&#x200B;作为登陆页面无效的页面的URL。 要指定多个值，请在单独的行中输入它们。

   **[!UICONTROL User Agent:]**&#x200B;如何将登陆页验证代理标识到登陆页所在的Web服务器。 默认值为默认值，它会将代理的视图归因于匿名[!DNL Mozilla Firefox]用户。 如果Web服务器阻止来自匿名[!DNL Mozilla Firefox]用户的请求，请输入其他代理的名称。 例如，对于[!DNL Googlebot]，输入`Googlebot/2.1;+http://www.google.com/bot.html`。

   **[!UICONTROL Report redirects as errors]：**&#x200B;当登陆页面重定向到其他页面时（例如，如果登陆页面缺失且站点显示替换页面），登陆页面错误文件中的[!UICONTROL ER Errors]列将指示登陆页面被重定向到的URL。

任务开始时，会在[!UICONTROL Bulksheets view]中添加一个新行。 创建文件后，将发送一封包含指向文件的链接的电子邮件通知。 根据编译的数据量，电子邮件通知可能需要几分钟或更长时间。 您可以下载文件以进行编辑，然后重新上传以供发布，也可以按原样发布文件。 但是，如果文件生成失败，则[!UICONTROL Bulksheet Management]页面上会列出一个错误文件，并且会发送电子邮件通知，其中包含指向错误文件的链接。

>[!NOTE]
>
>* 验证大型文件需要较长时间。
>* 多个营销活动的批量处理工作表文件最多可以包含500,000个数据行。 如果您为多个营销活动生成数据，并且组合数据包含超过500,000行，则数据将按营销活动拆分为两个或多个名为`<bulksheet name>_1.tsv`、`<bulksheet name>_2.tsv`等的文件。

>[!MORELIKETHIS]
>
>* [关于使用批量处理工作表管理营销活动数据](bulksheet-about.md)
>* [删除上载的批量工作表和错误文件](bulksheet-delete.md)
>* [发布批量工作表或已更正的错误文件](bulksheet-post.md)
>* [停止正在进行的批量处理工作表作业](bulksheet-stop-job.md)
>* [上载批量工作表或已更正的错误文件](bulksheet-upload.md)
>* [导出生成或上载的批量工作表文件](bulksheet-export.md)
