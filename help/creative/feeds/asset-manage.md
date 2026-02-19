---
title: 管理资源文件
description: 了解如何上传和管理广告商的资源文件。
feature: Creative Dynamic Creatives
exl-id: 2fe2d778-8456-490a-bf44-234dbc08649f
source-git-commit: ad7d2b02103b5a45dadcd51b60621c31e9db0d29
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---

# 管理资源文件

* 动态HTML5广告需要采用Microsoft Excel电子表格(XLSX)格式的信息源文件，以及在电子表格中引用的实际图像资源。

* 静态HTML5广告只需每个广告使用一个图像资源。

* 视频广告需要采用Microsoft Excel电子表格(XLSX)格式的信息源文件，以及在电子表格中引用的实际视频资源。

>[!NOTE]
>
> 每个信息源文件只能用于一个目录。

## 文件要求

* Dynamic HTML5广告：

   * CSV、TSV或Microsoft Excel电子表格(XLSX)格式的信息源文件，每个广告变体具有一个标题行和一个数据行。 在每一行中使用格式`images/image_name`（如`images/300x250_acme_logo.png`）包括图像名称。

     广告商特定的字段名称必须映射到动态广告馈送文件的[可用字段](/help/creative/appendix-available-feed-fields.md)。

   * GIF、JPEG、JPG或PNG格式中关联的图像资源。<!-- Is this true: The maximum file size is two (2) MB. -->查看[支持的创意大小](/help/creative/creative-libraries/creative-sizes.md)。

  您可以上传单个XLSX文件、单个图像文件或包含XLSX和图像文件任意组合的单个ZIP文件。<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* 静态HTML5广告：

   * GIF、JPG、JPEG或PNG格式中每个广告一个图像资源。

     您可以在ZIP文件中上传单个图像或多个图像。<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* 动态视频广告：

   * CSV、TSV或Microsoft Excel电子表格(XLSX)格式的信息源文件，每个广告变体具有一个标题行和一个数据行。 在每一行中使用格式`videos/image_name`（如`videos/300x250_acme_logo.png`）包含一个视频名称。 ZIP文件最大为512 MB，最大为500行。

     广告商特定的字段名称必须映射到动态广告馈送文件的[可用字段](/help/creative/appendix-available-feed-fields.md)。

     对于包含动态视频的所有帐户，最佳实践是[使用资源文件以及](catalog-manage.md)通用信息源模板[的副本[!UICONTROL Adobe Creative Template]](feed-template-manage.md)创建目录，您可以在其中将资源文件中的每个字段映射到Advertising Creative后端上的字段。

   * 以MP4、MOV或WEBM格式表示的关联视频资产。 支持的广告模板包括开始卡、结束卡、顶部叠加、底部叠加或L形。 每个视频的持续时间必须介于1至90秒之间。 查看[支持的创意大小](/help/creative/creative-libraries/creative-sizes.md)。

  您可以上传单个XLSX文件、单个图像文件或包含XLSX和视频文件任意组合的单个ZIP文件。<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

## 上传资源文件

>[!NOTE]
>
>在[将动态创意添加到创意库](/help/creative/creative-libraries/creative-add-dynamic.md)时，您还可以直接上传目录，而不是上传资源文件。 您在此处创建的任何目录均可在[!UICONTROL Catalogs]视图中供将来使用。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**。

1. 单击&#x200B;**[!UICONTROL Assets]**&#x200B;选项卡。

1. 单击右上角的&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Asset]**。

1. 配置资源文件：

   1. 选择可以访问资源文件的广告商。

   1. 通过以下任一方式指定资源文件：

      * 将文件拖放到设备或网络上的框中。

      * 单击&#x200B;**[!UICONTROL Select a file]**&#x200B;在您的设备或网络上查找该文件。

   1. 单击&#x200B;**[!UICONTROL Upload]**。

所有ZIP文件都会自动解压缩。 上传电子表格文件时，该文件将列在[!UICONTROL Feeds]子选项卡上。 上传图像文件时，该图像文件列在[!UICONTROL Images]子选项卡上。

## 下载资源文件

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**。

1. 单击&#x200B;**[!UICONTROL Assets]**&#x200B;选项卡。

1. 将光标悬停在资源行上并单击&#x200B;**[!UICONTROL Download]**。

   将按照浏览器的正常过程下载文件。

## 删除资源文件

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**。

1. 单击&#x200B;**[!UICONTROL Assets]**&#x200B;选项卡。

1. 将光标悬停在资源行上并单击&#x200B;**[!UICONTROL Delete]**。

>[!MORELIKETHIS]
>
>* [动态广告馈送文件的可用字段](/help/creative/appendix-available-feed-fields.md)
>* [动态广告的工作流](/help/creative/introduction/workflow-dynamic-ads.md)
>* [管理馈送模板](/help/creative/feeds/feed-template-manage.md)
>* [管理目录](/help/creative/feeds/catalog-manage.md)
>* [管理动态广告模板](/help/creative/ad-templates/ad-template-manage.md)
>* [将动态创意添加到创意库](/help/creative/creative-libraries/creative-add-dynamic.md)
