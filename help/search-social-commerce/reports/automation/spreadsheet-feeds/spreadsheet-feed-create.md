---
title: 创建电子表格报表源
description: 了解如何设置电子表格馈送。
exl-id: a6a9ce46-51b4-4b06-b004-89fce06d1da6
feature: Search Reports
TQID: https://experienceleague.adobe.com/LM5QfP4QSOBQ4YFLgdARTKb4xNkyXSJxzG79dGdo-HA
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 185
ht-degree: 0%

---

# 创建电子表格报表源

*仅用于基本报告和模型准确性报告*

使用从常规报表模板创建的特殊格式的[!DNL Excel]电子表格模板设置电子表格馈送。

1. [创建 [!DNL Excel] 模板以使用报表数据填充](spreadsheet-feed-create-excel-template.md)。

2. 创建电子表格信息源：

   1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Spreadsheet Feeds]**。

   1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Create]**。

   1. 在&#x200B;**[!UICONTROL Add Spreadsheet Feed]**&#x200B;对话框中，指定[电子表格馈送设置](spreadsheet-feed-settings.md)。

   1. 单击&#x200B;**[!UICONTROL Submit]**。

   1. （可选）信息源的[!UICONTROL Update Status]为&#x200B;*[!UICONTROL Finished]*&#x200B;后，单击信息源旁边的&#x200B;**[!UICONTROL XLSX]**，然后按照浏览器的正常过程打开或保存文件。

      >[!NOTE]
      >
      >如果稍后删除与信息源关联的报表模板，则也会删除信息源。

      电子表格馈送在每天配置的[!UICONTROL Schedule Time]自动刷新。 如果报表模板包含任何电子邮件收件人的地址，则这些地址会在电子表格刷新后接收通知。

>[!MORELIKETHIS]
>
>* [关于电子表格报表馈送](spreadsheet-feed-about.md)
>* [为电子表格报表馈送创建 [!DNL Excel] 模板](spreadsheet-feed-create-excel-template.md)
>* [编辑电子表格报表源设置](spreadsheet-feed-edit.md)
>* [电子表格报表源设置](spreadsheet-feed-settings.md)
>* [查看或保存电子表格报表源文件](spreadsheet-feed-view-or-save.md)
>* [手动刷新电子表格报表馈送](spreadsheet-feed-refresh.md)
>* [删除电子表格报表馈送](spreadsheet-feed-delete.md)
