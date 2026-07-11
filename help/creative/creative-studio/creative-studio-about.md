---
title: 关于Advertising Creative中的Creative Studio
description: 了解如何使用Creative Studio在Adobe Advertising Creative中构建AI辅助广告内容。
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 24e27656edda50f29292cb75823ef6cacdb685fe
workflow-type: tm+mt
source-wordcount: 811
ht-degree: 0%

---

# 关于[!DNL Advertising Creative]中的[!UICONTROL Creative Studio]

*Beta功能*

[!UICONTROL Creative Studio]是一个AI辅助环境，您可以在其中在单个会话中跨多种格式构建、调整大小和优化显示广告。 您通过自然语言聊天界面与AI交互以生成和修改广告内容 — 内容字段无需手动设计工作。

## Workspace概述

[!UICONTROL Creative Studio]组织为三个选项卡：

**[!UICONTROL Creatives]** — 广告创建的起点。 显示从Creative Studio生成的现有创意，这些创意已整理到可折叠的创意库中。 在此处，您可以从模板生成标准展示广告，从目录数据构建动态展示创意，并管理现有创意（编辑、生成广告变体、预览、复制、下载、删除、QA和查看更改日志）。 请参阅“[在Creative Studio中管理标准广告](creative-studio-manage-standard-ads.md)”和“[在Creative Studio中管理动态广告](creative-studio-manage-dynamic-ads.md)”。

**[!UICONTROL Templates]** — 显示您的帐户可用的所有显示和视频广告模板，并按源（所有、系统模板、用户模板）、状态和广告格式进行筛选。 您可以预览、收藏、添加标签、下载和删除模板，或者直接从现有的显示广告模板启动广告生成会话。 请参阅“[在Creative Studio中管理模板](creative-studio-manage-templates.md)”。

**[!UICONTROL Assets]** — 存储模板中使用的图像、视频和音频文件，这些文件可用于在广告生成会话期间附加到AI聊天消息。 您可以搜索、筛选、上传、下载和删除资源。 请参阅[在Creative Studio中管理资源](creative-studio-manage-assets.md)。

## 主要功能

* **AI内容生成：**&#x200B;使用&#x200B;**[!UICONTROL Ad Variations Generator]**&#x200B;通过自然语言聊天界面生成广告概念和变化。 AI助手可以生成标题、副标题、CTA、正文和背景图像变化，并可以在同一会话中创建新的大小模板。 每个会话最多可以有10个概念处于活动状态。

* **显示和视频广告支持：**&#x200B;创建和管理显示广告模板和视频广告模板。 创建模板时，请选择&#x200B;**[!UICONTROL Display Ad Template]**&#x200B;或&#x200B;**[!UICONTROL Video Ad Template]**&#x200B;以匹配您的促销活动格式。

* **HTML5模板上传：**&#x200B;通过将现有HTML5广告模板上传为ZIP文件来导入它们。 **[!UICONTROL Import Templates]**&#x200B;对话框允许您在导入之前分配广告商和模板名称。

* **多大小支持：**&#x200B;只需一步即可将广告大小调整为IAB标准维度。 AI会自动调整每个格式的内容放置和大小，画布控件（放大/缩小、适合屏幕、重播动画）可帮助您查看每个大小。

* **与品牌一致的输出：**&#x200B;应用[品牌配置文件](/help/creative/brands/brand-manage.md)时，AI将使用您品牌的徽标、调色板、语音准则、图像标准和渠道准则来使生成的内容与品牌保持一致。

* **资源库访问：**&#x200B;通过从资源库中选择，在内容生成期间保持可视上下文可用，将图像和其他资源直接附加到AI聊天消息。

* **信息源集成：**&#x200B;对于动态广告营销活动，请连接产品或内容目录以大规模生成广告，然后使用AI代理筛选、预览和质量检查目录生成的广告组合。

* **模板组织：**&#x200B;将模板标记为收藏，应用标签，并按状态、格式或源进行筛选，以使模板库保持井井有条。

## 广告创建工作流

| 工作流 | 使用时间 |
| --- | --- |
| [从模板生成标准广告](creative-studio-manage-standard-ads.md) | 选择显示或视频模板并使用[!UICONTROL Ad Variations Generator]创建AI生成的内容变体。 当模板已存在并且您需要AI辅助内容生成时的最佳选择。 |
| [管理动态创意](creative-studio-manage-dynamic-ads.md) | 将产品或内容目录连接到模板，将目录字段映射到模板元素，然后使用AI代理预览和QA所有生成的广告组合。 最适合于以目录为导向的大规模营销活动。 |
| 构建新模板 | 从空白画布开始创建显示或视频模板。 当没有现有模板满足您的需求时最佳选择。 |
| 上传HTML5模板 | 导入一个或多个打包为ZIP文件的HTML5广告模板。 当您在[!DNL Advertising Creative]之外构建可用于生产的HTML5创意时，这是最佳选择。 |

## 标准广告与动态广告

[!UICONTROL Creative Studio]支持两个决定AI代理行为方式的广告内容模型：

**标准广告** — 您提供或生成所有广告内容。 AI代理可以在模板布局的限制内生成、修改或替换任何内容字段（标题、CTA、图像、颜色、复制色调）。 通过选择广告商和库（附带将广告附加到捆绑包的选项），将完成的标准广告保存到创意库。 标准广告最适合自定义消息传递活动。

**动态广告** — 内容由产品或内容目录驱动。 四步引导式工作流可指导您选择模板、将目录字段映射到模板元素以及配置广告集。 设置后，AI代理将转移到QA和预览角色：它可以按目录字段过滤广告、标记质量问题（字符限制、内容溢出、图像损坏、合规性）并分析跨目录的组合，但无法直接修改目录源内容。 要更改动态广告内容，请更新源目录。

>[!MORELIKETHIS]
>
>* [在Creative Studio中管理标准广告](creative-studio-manage-standard-ads.md)
>* [在Creative Studio中管理动态创意](creative-studio-manage-dynamic-ads.md)
>* [在Creative Studio中管理模板](creative-studio-manage-templates.md)
>* [在Creative Studio中管理资源](creative-studio-manage-assets.md)
>* [在Advertising Creative中管理品牌配置文件](/help/creative/brands/brand-manage.md)
