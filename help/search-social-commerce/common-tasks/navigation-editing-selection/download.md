---
title: 从营销活动管理视图下载数据
description: 了解如何从大多数营销活动管理视图下载数据。
exl-id: 0bbb02df-2ee0-4610-b60a-ca2b58daadbb
feature: Search Common Tasks
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# 从营销活动管理视图下载数据

您可以从以下位置下载数据： [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 视图，但 [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives]， [!UICONTROL Placements] - [!UICONTROL Placement Negatives]， [!UICONTROL Audiences]、和 [!UICONTROL Extensions] 视图。 您可以下载：

* 中的报告 [!DNL XLSM] (启用宏 [!DNL Microsoft® Excel] 电子表格)格式。 如果选择视图中的特定行，则报表将为每个选定行包含一行。 如果不选择任何行，则将为视图中的每一行创建一行。

* TXT格式的批量工作表文件，其中包括所有相关子实体。 如果您为多个广告网络上的实体选择行，则会为每个相关的广告网络创建一个文件。 如果不选择任何行，则会为视图中表示的每个广告网络创建一个文件。 为不同广告网络生成的批量工作表文件包含不同的数据列。

  如果您为多个营销活动生成数据，并且组合数据包含超过500,000行，则根据需要，营销活动会将数据进一步拆分为两个或多个名为的文件 `<bulksheet name>_1.txt`， `<bulksheet name>_2.txt`，等等。

  中的每个Bulksheet文件 [!UICONTROL Downloads] 面板也会列在 [!UICONTROL Bulksheets] 视图。 创建文件时，您会收到电子邮件通知，其中包含下载文件的链接；根据编译的数据量，通知可能需要几分钟或更长时间。 但是，如果文件生成失败，则“批量处理工作表”视图上会列出一个错误文件，并且您会收到一封电子邮件通知，其中包含指向错误文件的链接。 从任一位置删除批量工作表文件 [!UICONTROL Download] 面板或 [!UICONTROL Bulksheets] tab会将其从两个位置删除。

1. （可选）选择要包含在文件中的单个行。

   否则，将包含视图中的所有数据。

1. 在工具栏右侧，单击 ![报告下载](/help/search-social-commerce/assets/download.png "报告下载").

1. 单击 ![创建](/help/search-social-commerce/assets/add.png "创建") **[!UICONTROL Create]**，或者添加文件名，然后单击 **[!UICONTROL Report]** 或 **[!UICONTROL Bulksheet]**.

1. （可选）报告作业完成后，单击 ![报告下载](/help/search-social-commerce/assets/download.png "报告下载") 查看 [!UICONTROL Available Reports] 面板，然后下载或删除报表：

   * 要按照浏览器的正常过程打开或保存文件，请单击 ![下载电子表格](/help/search-social-commerce/assets/download-spreadsheet.png "下载电子表格").

     有关浏览器过程的详细信息，请参阅浏览器的联机帮助。

   * 要删除文件，请单击 ![删除](/help/search-social-commerce/assets/delete.png "删除").

>[!MORELIKETHIS]
>
>[从以下位置删除性能数据报表或批量工作表文件： [!UICONTROL Downloads] 菜单](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
