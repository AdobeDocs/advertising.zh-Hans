---
title: 关于Adobe Advertising Creative
description: 了解 [!DNL Creative]。
feature: Creative Introduction
exl-id: 2cc12119-5924-4fcd-a54b-30f7887ae6a7
source-git-commit: de2a2a097802cc4a7b5ac63bee2eb326895e70f1
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# 关于Adobe Advertising Creative 2.0

<!-- verify all and rewrite to include new stuff -->

作为Adobe Advertising的一部分，Advertising Creative是一个自助服务平台，用于自动化实时、个性化的广告体验并可以选择在创意元素级别优化广告。<!-- Verify -->您可以在包括Adobe Advertising DSP在内的任何DSP中将广告体验作为广告实施。

## 可重用创意的自定义创意库

通过Creative Libraries，您可以管理将在广告体验中使用的创意。 您可以创建多个库，每个库都具有单独的创意和创意组（称为&#x200B;*包*，您将附加到体验中）。

### [!DNL Adobe]资源集成

[!DNL Creative]直接与Adobe Experience Manager集成，允许您轻松上传设计团队为标准图像广告创建和批准的[!DNL Adobe]图像资源。

## 基于规则的体验和非目标体验

* **基于规则的定位体验：**&#x200B;使用基于规则的决策树模型构建故事 — 展开根据您对受众的了解实时自定义的编排广告字符串。 例如，故事可以根据客户行为、地理位置、人口统计、重新定位、客户历程中的位置等发生更改。

* **非定向体验：**&#x200B;在不缩小受众范围的情况下计划和优化广告元素。

### [!DNL Adobe]数据集成

您可以将来自Adobe Audience Manager和Adobe Analytics的第一方受众区段，以及您在Advertising DSP中创建的自定义受众区段，和使用[!DNL Creative]创建的重新定位像素，用作广告体验中特定创意人员的目标。<!-- Advertiser should be able to target all segments that are available in DSP for targeting -->

### 体验作为广告的实施

创建体验后，您可以为该体验生成JavaScript或iframe标记，并在Advertising DSP营销活动或任何其他DSP中将该标记作为第三方广告实施。

### 广告元素优化

您可以选择允许[!DNL Creative]使用由[!DNL Adobe AI]提供支持的经过优化、加权的广告轮换，根据性能（无论您是否定义特定受众目标）优化任何体验的广告元素。

<!--
[!DNL Creative] serves first-party ads and triggers third-party ads for the experience based on the specified targeting (when applicable), scheduling, ad rotation, and optimization goal options 
-->

## 正在重新定位像素

您可以创建重定位像素，以用作广告体验中创意内容的目标。 这些目标只向具有指定属性的用户显示广告，这些用户以前访问过特定网页。

## 展示、点击和转化跟踪

[!DNL Creative]自动跟踪从体验提供的广告的所有展示次数和点击次数。 您还可以选择将第三方展示跟踪和点击跟踪URL添加到Creative Libraries中的创意内容，以及体验中的自定义跟踪URL。

[!DNL Creative]还跟踪根据您的广告体验创建的已提供广告的转化。<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optional?  -->

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
