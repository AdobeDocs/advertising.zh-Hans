---
title: 管理信息源模板
description: 了解如何管理信息源模板。
feature: Creative Dynamic Creatives
source-git-commit: 0d7a7ab23173a061961c4b5c66ace5b69a746e86
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# 管理信息源模板

<!-- I have a "Retail" feed template that was created by rkarthik@adobe. Ask product if this is available to all clients or just internal.  -->

<!-- We have a finite set of supported fields on the backend. I need to include that info in an appendix. -->

馈送模板将馈送文件/目录中的字段映射到Advertising Creative后端上的字段。 动态HTML5广告(而非静态HTML5广告)需要信息源模板来创建动态广告。

您可以对多个广告模板使用一个信息源模板。

## 创建信息源模板

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**。

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 单击右上角的&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Template]**。

1. 指定[信息源模板设置](#feed-template-settings)。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 编辑馈送模板

**注意：**&#x200B;您只能编辑您创建的馈送模板。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**。

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 将光标悬停在模板行上并单击&#x200B;**[!UICONTROL Duplicate]**。

1. 根据需要编辑[信息源模板设置](#feed-template-settings)。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 查看馈送模板

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**。

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 将光标悬停在模板行上并单击&#x200B;**[!UICONTROL View]**。

## 复制馈送模板

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**。

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 将光标悬停在模板行上并单击&#x200B;**[!UICONTROL Duplicate]**。

1. 在[!UICONTROL Duplicate Template]屏幕中，输入唯一的&#x200B;**[!UICONTROL Template Name]**。 如果要复制其他人创建的模板，请选择&#x200B;**[!UICONTROL Advertiser]**。 根据需要编辑其他[信息源模板设置](#feed-template-settings)。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 下载信息源模板

下载的信息源模板采用压缩的Microsoft Excel电子表格(XLSX)格式。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Feeds]**。

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 将光标悬停在模板行上并单击&#x200B;**[!UICONTROL Download]**。

   将按照浏览器的正常过程下载文件。

## 信息源模板设置 {#feed-template-settings}

### [!UICONTROL General]设置

**[!UICONTROL Template Name]：**&#x200B;指定广告商的唯一模板名称。

**[!UICONTROL Advertiser]：**&#x200B;可以使用模板的广告商。

**[!UICONTROL Description]：** （可选）对使用信息源模板的任何人都有用的信息。

### [!UICONTROL Field Mapping]设置

将信息源文件中的每个字段映射到Advertising Creative后端上的字段。 有关后端字段及其必需属性的列表，请参阅[动态广告馈送文件的可用字段](/help/creative/appendix-available-feed-fields.md)。<!-- Check w/product: What is displayed where in the UI/reports and published ads? -->

必须至少将一个信息源文件字段标记为“[!UICONTROL Is Unique]”。 要添加字段映射，请单击&#x200B;**[!UICONTROL +]**。 要删除最后一个字段映射，请单击&#x200B;**[!UICONTROL +]**。

**[!UICONTROL Field Name]：**&#x200B;信息源文件中的字段。

**[!UICONTROL Description]：** （可选）对使用信息源模板的任何人都有用的信息。

**[!UICONTROL Is Unique]：**&#x200B;指示该字段是唯一ID（键）。 每个馈送模板必须至少有一个字段是唯一的。 要选择此选项，请单击按钮将其向右移动。<!-- **Note: The unique identifier is different from the feed "trigger" in experience settings. -->

**[!UICONTROL Backend Field]：** Advertising Creative后端[上映射到馈送文件中指定](/help/creative/appendix-available-feed-fields.md)的[!UICONTROL Field Name]字段。

>[!MORELIKETHIS]
>
>* [动态广告的工作流](/help/creative/introduction/workflow-dynamic-ads.md)
>* [管理资源文件](/help/creative/feeds/asset-manage.md)
>* [管理目录](/help/creative/feeds/catalog-manage.md)
>* [跟踪目录处理作业的状态](/help/creative/feeds/job-status-track.md)
>* [管理动态广告模板](/help/creative/ad-templates/ad-template-manage.md)
>* [将动态创意添加到创意库](/help/creative/creative-libraries/creative-add-dynamic.md)
