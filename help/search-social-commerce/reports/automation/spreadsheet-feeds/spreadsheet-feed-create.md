---
title: 创建电子表格报表源
description: 了解如何设置电子表格馈送。
exl-id: ed793de5-0df1-4fc3-be59-29adec4959f7
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# 创建电子表格报表源

*仅用于基本报表和模型准确性报表*

使用特殊格式设置电子表格馈送 [!DNL Excel] 从常规报表模板创建的电子表格模板。

1. [创建 [!DNL Excel] 要填充报表数据的模板](spreadsheet-feed-create-excel-template.md).

2. 创建电子表格信息源：

   1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Spreadsheet Feeds]**.

   1. 在数据表上方的工具栏中，单击 **[!UICONTROL Create]**.

   1. 在 **[!UICONTROL Add Spreadsheet Feed]** 对话框，请指定 [电子表格馈送设置](spreadsheet-feed-settings.md).

   1. 单击 **[!UICONTROL Submit]**.

   1. （可选）在每次加载馈送时 [!UICONTROL Update Status] 是 *[!UICONTROL Finished]*，单击 **[!UICONTROL XLSX]** ，然后按照浏览器的正常步骤打开或保存该文件。

      >[!NOTE]
      >
      >如果稍后删除与信息源关联的报表模板，则也会删除信息源。

      电子表格馈送在每天配置的时自动刷新 [!UICONTROL Schedule Time]. 如果报表模板包含任何电子邮件收件人的地址，则这些地址会在电子表格刷新后接收通知。

>[!MORELIKETHIS]
>
>* [关于电子表格报表源](spreadsheet-feed-about.md)
>* [创建 [!DNL Excel] 电子表格报表馈送模板](spreadsheet-feed-create-excel-template.md)
>* [编辑电子表格报表馈送设置](spreadsheet-feed-edit.md)
>* [电子表格报表馈送设置](spreadsheet-feed-settings.md)
>* [查看或保存电子表格报表源文件](spreadsheet-feed-view-or-save.md)
>* [手动刷新电子表格报表馈送](spreadsheet-feed-refresh.md)
>* [删除电子表格报表源](spreadsheet-feed-delete.md)
