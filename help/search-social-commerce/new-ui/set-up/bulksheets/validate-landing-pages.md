---
title: （新UI）验证批量处理工作表文件中的登陆页面
description: 了解如何在新的Search、Social和Commerce UI中验证单帐户批量工作表文件中的目标URL。
feature: Search Bulksheets
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e58024d1-d6da-420c-80af-6be211808316id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: f22a0f3f1884066faca71c6e8bb760253366b30e
workflow-type: tm+mt
source-wordcount: 585
ht-degree: 0%

---

# （新UI）验证批量处理工作表文件中的登陆页面

*仅具有目标URL的帐户*

您可以在单个帐户批量工作表文件中验证所有目标URL中的登陆页面。 您可以指定指示无效页面的任何短语和URL，并可以选择将登陆页面重定向报告为错误。 搜索、Social和Commerce会检查您指定的条件和缺少的登陆页面（这会导致HTTP 404或“未找到”错误）。

当发现错误时，Search、Social和Commerce会创建一个批量工作表错误文件，该文件包含原始批量工作表中的所有行，以及包含无效登陆页的所有行的错误消息。 错误记录在[!UICONTROL EF Errors]列中。 文件名约定是`<bulksheet name>__lpv_errors.<extension used for the bulksheet>`。

您可以稍后下载文件，更正错误并上传更正后的文件，然后将更正后的文件发布到广告网络帐户。

>[!NOTE]
>
>* 此功能不会验证基本URL/最终URL列中的值。
>* 您可以在验证批量工作表文件时发布这些文件，即使发现错误也是如此。

>[!IMPORTANT]
>
>已暂停对登陆页面验证中的非ASCII字符的支持。 如果您的登陆页面URL包含非ASCII字符，请与技术支持联系以获得帮助。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**。

1. 选中每个要验证的文件旁边的复选框。

   >[!NOTE]
   >
   >您只能验证当前未正在进行的单帐户EF批量工作表。 如果选择多帐户批量工作表或当前正在处理的批量工作表，则将排除这些文件。

1. 在操作栏中，单击&#x200B;**[!UICONTROL Validate URLs]**。

1. 在对话框中，在字段中输入信息，然后单击&#x200B;**[!UICONTROL Apply]**：

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page (one per line):]**&#x200B;登陆页面正文中的文本，指示页面无效。 要指定多个值，请在单独的行中输入它们。

   **[!UICONTROL Enter invalid landing pages (one per line):]**&#x200B;作为登陆页面无效的页面的URL。 要指定多个值，请在单独的行中输入它们。

   **[!UICONTROL User Agent:]**&#x200B;如何将登陆页验证代理标识到登陆页所在的Web服务器。 默认值为`default`，它将代理的视图归因于匿名[!DNL Mozilla Firefox]用户。 如果Web服务器阻止来自匿名[!DNL Mozilla Firefox]用户的请求，请输入其他代理的名称。 例如，对于[!DNL Googlebot]，输入`Googlebot/2.1;+http://www.google.com/bot.html`。

   **[!UICONTROL Report redirects as errors]：**&#x200B;当登陆页面重定向到其他页面时（例如，如果登陆页面缺失且站点显示替换页面），登陆页面错误文件中的[!UICONTROL EF Errors]列将指示登陆页面被重定向到的URL。

任务开始时，将在[!UICONTROL Bulksheets]视图中添加一个新行。 如果在[!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md)中启用了批量处理工作表的电子邮件通知[，则在创建文件时会发送一封电子邮件通知，其中包含指向文件的链接。 根据编译的数据量，电子邮件通知可能需要几分钟或更长时间。 您可以下载文件以进行编辑，然后重新上传以供发布，也可以按原样发布文件。

>[!NOTE]
>
>* 验证大型文件需要较长时间。
>* 多个营销活动的批量处理工作表文件最多可以包含500,000个数据行。 如果您为多个营销活动生成数据，并且组合的数据包含超过500,000行，则数据将按营销活动拆分为两个或多个名为`<bulksheet name>_1.tsv`、`<bulksheet name>_2.tsv`等的文件。

>[!MORELIKETHIS]
>
>* [（新UI）关于使用批量处理工作表管理营销活动数据](about.md)
>* [（新UI）上载批量工作表或已更正的错误文件](upload.md)
>* [（新UI）发布批量工作表或已更正的错误文件](post.md)
>* [（新UI）删除上传的批量工作表和错误文件](delete.md)
>* [（新UI）停止正在进行的批量处理工作表作业](stop-job.md)
