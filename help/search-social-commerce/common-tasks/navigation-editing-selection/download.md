---
title: 从营销活动管理视图下载数据
description: 了解如何从大多数营销活动管理视图下载数据。
exl-id: f549f03c-ed0b-4d7d-8d7e-91192c17e77e
feature: Search Common Tasks
source-git-commit: 399974645b5083e735ff7aa94eba0a1115b4ddeb
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# 从营销活动管理视图下载数据

*旧版用户界面*

您可以从[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]视图下载数据，但[!UICONTROL Keywords] - [!UICONTROL Keyword Negatives]、[!UICONTROL Placements] - [!UICONTROL Placement Negatives]、[!UICONTROL Audiences]和[!UICONTROL Extensions]视图除外。 您可以下载：

* [!DNL XLSM] （启用宏的[!DNL Microsoft Excel]电子表格）格式的报告。 如果选择视图中的特定行，则报表将为每个选定行包含一行。 如果不选择任何行，则将为视图中的每一行创建一行。

* TXT格式的批量工作表文件，其中包括所有相关子实体。 如果您为多个广告网络上的实体选择行，则会为每个相关的广告网络创建一个文件。 如果不选择任何行，则会为视图中表示的每个广告网络创建一个文件。 为不同广告网络生成的批量工作表文件包含不同的数据列。

  如果您为多个营销活动生成数据，且组合数据包含超过500,000行，则根据需要，营销活动会进一步将数据拆分为两个或多个名为`<bulksheet name>_1.txt`、`<bulksheet name>_2.txt`等的文件。

  [!UICONTROL Downloads]面板中的每个批量处理工作表文件也在[!UICONTROL Bulksheets]视图中列出。 创建文件时，您会收到电子邮件通知，其中包含下载文件的链接；根据编译的数据量，通知可能需要几分钟或更长时间。 但是，如果文件生成失败，则“批量处理工作表”视图上会列出一个错误文件，并且您会收到一封电子邮件通知，其中包含指向错误文件的链接。 从[!UICONTROL Download]面板或[!UICONTROL Bulksheets]选项卡中删除批量处理工作表文件会同时将其从这两个位置删除。

1. （可选）选择要包含在文件中的单个行。

   否则，将包含视图中的所有数据。

1. 单击工具栏右侧的![报告下载](/help/search-social-commerce/assets/download.png "报告下载")。

1. 单击![创建](/help/search-social-commerce/assets/add.png "创建") **[!UICONTROL Create]**，可以选择添加文件名，然后单击&#x200B;**[!UICONTROL Report]**&#x200B;或&#x200B;**[!UICONTROL Bulksheet]**。

1. （可选）报告作业完成后，单击![报告下载](/help/search-social-commerce/assets/download.png "报告下载")以查看[!UICONTROL Available Reports]面板，然后下载或删除报告：

   * 若要按照浏览器的正常程序打开或保存文件，请单击![下载电子表格](/help/search-social-commerce/assets/download-spreadsheet.png "下载电子表格")。

     有关浏览器过程的详细信息，请参阅浏览器的联机帮助。

   * 要删除该文件，请单击![删除](/help/search-social-commerce/assets/delete.png "删除")。

>[!MORELIKETHIS]
>
>[从[!UICONTROL Downloads]菜单删除性能数据报告或批量处理工作表文件](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
