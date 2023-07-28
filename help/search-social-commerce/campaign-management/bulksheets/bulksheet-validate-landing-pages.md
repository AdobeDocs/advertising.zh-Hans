---
title: 验证批量处理工作表文件中的登陆页面
description: 了解如何在单帐户批量处理工作表文件中验证目标URL。
exl-id: cf703687-1151-46f6-9540-12a83d41dfc8
feature: Search Bulksheets
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# 验证批量处理工作表文件中的登陆页面

*仅具有目标URL的帐户*

您可以在单个帐户批量工作表文件中验证所有目标URL中的登陆页面。 您可以指定指示无效页面的任何短语和URL，并可以选择将登陆页面重定向报告为错误。 搜索、Social和Commerce会检查您指定的条件和缺少的登陆页面（这会导致HTTP 404或“未找到”错误）。

当发现错误时，Search、Social和Commerce会创建一个批量处理工作表错误文件，该文件包含原始批量处理工作表中的所有行，以及具有无效登陆页面的所有行的错误消息。 错误记录在 [!UICONTROL EF Errors] 列。 文件名的约定是 `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

您可以稍后下载文件，更正错误并上传更正后的文件，然后将更正后的文件发布到广告网络帐户。

>[!NOTE]
>
>* 此功能不会验证基本URL/最终URL列中的值。
>* 您可以在验证批量工作表文件时发布这些文件，即使发现错误也是如此。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. 选中每个要验证的文件旁边的复选框。

1. 在数据表上方的工具栏中，单击 **[!UICONTROL Validate URLs]**.

1. 在对话框中，在字段中输入信息，然后单击 **[!UICONTROL Apply]**：

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]：** 登陆页面正文中的文本，指示页面无效。 要指定多个值，请在单独的行中输入它们。

   **[!UICONTROL Enter invalid landing pages(one per line):]** 作为登陆页面无效的页面的URL。 要指定多个值，请在单独的行中输入它们。

   **[!UICONTROL User Agent:]** 如何将登陆页验证代理标识到登陆页所在的Web服务器。 缺省值为缺省值，该缺省值将代理的视图归因于匿名 [!DNL Mozilla Firefox] 用户。 如果Web服务器阻止来自匿名用户的请求 [!DNL Mozilla Firefox] 用户，然后输入其他代理的名称。 例如，对于 [!DNL Googlebot]，输入 `Googlebot/2.1;+http://www.google.com/bot.html`.

   **[!UICONTROL Report redirects as errors]：** 当登陆页面重定向到另一个页面时（例如，如果登陆页面缺失且站点显示替代页面），则 [!UICONTROL ER Errors] 登陆页面错误文件中的列指示登陆页面被重定向到的URL。

任务开始时，新行将添加到 [!UICONTROL Bulksheets view]. 创建文件时，将发送一封包含指向文件的链接的电子邮件通知。 根据编译的数据量，电子邮件通知可能需要几分钟或更长时间。 您可以下载文件以进行编辑，然后重新上传以供发布，也可以按原样发布文件。 但是，如果文件生成失败，则会在 [!UICONTROL Bulksheet Management] 页面，并发送包含错误文件链接的电子邮件通知。

>[!NOTE]
>
>* 验证大型文件需要较长时间。
>* 多个营销活动的批量处理工作表文件最多可以包含500,000个数据行。 如果您为多个营销活动生成数据，并且组合数据包含超过500,000行，则数据将按营销活动拆分为两个或多个文件，名为 `<bulksheet name>_1.tsv`， `<bulksheet name>_2.tsv`，等等。

>[!MORELIKETHIS]
>
>* [关于使用批量处理工作表管理营销活动数据](bulksheet-about.md)
>* [删除上传的批量工作表和错误文件](bulksheet-delete.md)
>* [发布批量工作表或已更正的错误文件](bulksheet-post.md)
>* [停止正在进行的批量处理工作表作业](bulksheet-stop-job.md)
>* [上传批量工作表或已更正的错误文件](bulksheet-upload.md)
>* [导出生成或上传的批量处理工作表文件](bulksheet-export.md)
