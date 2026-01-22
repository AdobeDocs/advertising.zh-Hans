---
title: 关于Adobe Advertising Creative
description: 了解详情 [!DNL Creative]。
feature: Creative Introduction
exl-id: 2cc12119-5924-4fcd-a54b-30f7887ae6a7
source-git-commit: 1394b988828f5400b858f1a40b1b6382431a62b0
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# 关于Adobe Advertising Creative 2.0

<!-- verify all and rewrite to include new stuff -->

作为 Adobe 广告的一部分，Advertising Creative 是一个自助平台，用于自动化实时、个性化的广告体验，并可选择性地在创意层面优化广告内容。<!-- Verify --> 你可以在任何DSP中实现广告体验，包括Adobe Advertising DSP。

## 可重用创意的自定义创意库

通过Creative Libraries，您可以管理将在广告体验中使用的创意。 您可以创建多个库，每个库都具有单独的创意和创意组（称为&#x200B;*包*，您将附加到体验中）。

### [!DNL Adobe]资源集成

[!DNL Creative]与以下[!DNL Adobe]产品直接集成，允许您将资源导入到创意库：

* **Adobe Experience Manager：**&#x200B;上传您的设计团队为标准图像广告创建和批准的[!DNL Adobe]图像资源。

* **Adobe GenStudio for Performance Marketing：**&#x200B;从您的显示广告体验中导入所有广告变体作为HTML5创意。

## 基于规则的体验和非目标体验

* **针对性的规则驱动体验：** 利用基于规则的决策树模型构建故事——展开一系列编排好的广告，实时根据你对受众的了解进行定制。 例如，故事可以根据客户行为、地理位置、人口统计、重新定位、客户历程中的位置等发生更改。

* **非定向体验：** 在不缩小受众的情况下，安排和优化广告元素。

### [!DNL Adobe] 数据集成

使用来自Adobe Audience Manager和Adobe Analytics的第一方受众区段，以及您在Advertising DSP中创建的自定义受众区段，并使用[!DNL Creative]重新定位您创建的像素，作为广告体验中特定创意人员的目标。<!-- Advertiser should be able to target all segments that are available in DSP for targeting -->

### 体验作为广告的实施

创建体验后，您可以为该体验生成JavaScript或iframe标记，并在Advertising DSP营销活动或任何其他DSP中将该标记作为第三方广告实施。

### 广告元素优化

您可以选择允许[!DNL Creative]使用由[!DNL Adobe AI]提供支持的经过优化、加权的广告轮换，根据性能（无论您是否定义特定受众目标）优化任何体验的广告元素。

<!--
[!DNL Creative] serves first-party ads and triggers third-party ads for the experience based on the specified targeting (when applicable), scheduling, ad rotation, and optimization goal options 
-->

## 正在重新定位像素

您可以创建重定位像素，以用作广告体验中创意内容的目标。 这些目标只向具有指定属性的用户显示广告，这些用户以前访问过特定网页。

## 曝光、点击和转化追踪

[!DNL Creative] 自动跟踪体验中投放的所有广告的曝光和点击。 你还可以选择在创意库中的创意中添加第三方的印象追踪和点击追踪URL，以及在体验中自定义追踪URL。

[!DNL Creative] 还能追踪由您的广告体验创建的广告转化率。<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optional?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## 绩效报表

您可以在创意>体验中查看详细的体验级性能报表。

您还可以在“报表”>“自定义报表”中创建自定义Creative报表，以监控体验中的体验级别性能。 如果您在DSP促销活动中将[!DNL Creative]体验用作广告，则这些广告的效果数据可在其他自定义报表中获取，就像其他DSP广告的数据一样。<!-- Verify that [!DNL Creative] users have access to ALL other reports. -->

您可以选择将自定义报告传送到指定的[报告目标](/help/dsp/reports/report-destinations/report-destination-about.md)。

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [关于您的创意库](/help/creative/creative-libraries/creative-libraries-about.md)
>* [关于Advertising Creative中的体验](/help/creative/experiences/experience-about.md)
