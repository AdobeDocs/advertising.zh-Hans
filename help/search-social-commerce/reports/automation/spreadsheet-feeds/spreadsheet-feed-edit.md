---
title: 编辑电子表格报表馈送设置
description: 了解如何编辑电子表格馈送的设置。
exl-id: 8ca36006-4038-404b-aaf9-66dc3e9ddcf6
feature: Search Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---

# 编辑电子表格报表馈送设置

*仅用于基本报告和模型准确性报告*

您可以更改用于电子表格馈送的报表模板、[!DNL Microsoft Excel]模板和其他参数。

>[!NOTE]
>
> 如果您编辑报表模板中的列，或者使用新的或更新后的报表模板，则必须相应地更新[!DNL Excel]模板并重新上传。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Spreadsheet Feeds]**。

1. （可选）要更新用于电子表格馈送的报表模板或[!DNL Excel]模板：

   * （可选）若要为信息源使用其他或更新的报表模板，请[为报表模板](spreadsheet-feed-create-excel-template.md)创建新的 [!DNL Excel] 模板。

     在下一步中，您将需要上载报表模板和新的[!DNL Excel]文件。

   * （可选）要简单地向[!DNL Excel]模板添加自定义列，请在报表模板中列的右侧插入列，然后将该文件另存为.XLSX格式的[!DNL Excel]电子表格。 您需要在下一步中上传新的[!DNL Excel]文件。

1. 更改电子表格馈送设置：

   * 在主菜单中，单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**。

   * 在电子表格馈送名称旁边，单击![查看/编辑设置按钮](/help/search-social-commerce/assets/settings.png "查看/编辑设置按钮")。

   * 在[!UICONTROL Edit Spreadsheet Feed]对话框中，更改[电子表格馈送设置](spreadsheet-feed-settings.md)。

   * 单击&#x200B;**[!UICONTROL Submit]**。

   * （可选）信息源的[!UICONTROL Update Status]为&#x200B;*[!UICONTROL Finished]*&#x200B;后，单击信息源旁边的&#x200B;**[!UICONTROL XLSX]**，然后按照浏览器的正常过程打开或保存文件。

     >[!NOTE]
     >
     > 如果稍后删除与信息源关联的报表模板，则也会删除信息源。

     电子表格馈送在广告商所在时区的每天08:00自动刷新。 如果报表模板包含任何电子邮件收件人的地址，则这些地址会在电子表格刷新后接收通知。

>[!MORELIKETHIS]
>
>* [关于电子表格报表馈送](spreadsheet-feed-about.md)
>* [创建电子表格报表源](spreadsheet-feed-create.md)
>* [为电子表格报表馈送创建 [!DNL Excel] 模板](spreadsheet-feed-create-excel-template.md)
>* [编辑电子表格报表源设置](spreadsheet-feed-edit.md)
>* [电子表格报表源设置](spreadsheet-feed-settings.md)
>* [查看或保存电子表格报表源文件](spreadsheet-feed-view-or-save.md)
>* [手动刷新电子表格报表馈送](spreadsheet-feed-refresh.md)
