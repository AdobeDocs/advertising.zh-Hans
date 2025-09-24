---
title: 动态广告的工作流
description: 了解用于管理动态广告的工作流。
feature: Creative Dynamic Creatives
source-git-commit: 76e3ae8369fda1c4d95c06ecb085a8669dcf142b
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# 动态广告的工作流

1. 根据可用的资产[为您的动态广告创建广告模板](/help/creative/ad-templates/ad-template-manage.md)

1. 设置广告元素：

   * (对于单个静态HTML5广告)收集并[上传广告的图像资源](/help/creative/feeds/asset-manage.md)。

   * (对于动态HTML5广告)创建广告元素的目录：

      1. 创建一个采用Microsoft Excel电子表格(XLSX)格式的信息源文件，其中每个广告变量对应一行。 在每一行中包含图像名称或对Adobe Experience Manager的引用。 单独收集关联的图像资产。

      1. [上载信息源文件和图像资源](/help/creative/feeds/asset-manage.md)。

      1. [创建信息源模板](/help/creative/feeds/feed-template-manage.md)以将信息源文件（电子表格）中的字段映射到Advertising Creative后端中的字段。

      1. [从指定的信息源文件和指定的信息源模板创建目录](/help/creative/feeds/catalog-manage.md#feed-catalog-create)，然后[处理该目录](/help/creative/feeds/catalog-manage.md#feed-catalog-process)以查看可从它创建的广告变体。

         每个信息源文件只能用于一个目录。

         您可以在[ > ](/help/creative/feeds/job-status-track.md) > [!UICONTROL Creative]选项卡上[!UICONTROL Feeds]跟踪目录处理作业[!UICONTROL Job Status]的状态。

1. [为创意库创建动态创意内容](/help/creative/creative-libraries/creative-add-dynamic.md)。 对于动态HTML5广告，请使用指定的广告模板和指定的目录。

1. [创建动态广告包](/help/creative/creative-libraries/bundle-manage.md)，您可以一次将所有这些广告包附加到广告体验。

1. 创建具有目标[或](/help/creative/experiences/experience-create-targeting.md)的动态广告体验[而不具有目标](/help/creative/experiences/experience-create-no-targeting.md)，并[将创意包分配给体验](/help/creative/experiences/experience-assign-creative-bundles.md)。

1. [生成和实施广告体验标记](/help/creative/experiences/experience-tag-export.md)，以在DSP中将它们作为广告运行。

   要在Adobe Advertising DSP中将广告体验用作广告，请将广告体验标记上传到Advertising DSP营销活动。 要在其他DSP中将广告体验用作广告，请在该DSP中实施广告体验标记。
