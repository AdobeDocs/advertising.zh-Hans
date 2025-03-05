---
title: 关于Adobe Advertising Creative
description: 了解 [!DNL Creative]。
feature: Creative Introduction
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# 关于Adobe Advertising Creative 2.0

*已关闭的测试版*

<!-- verify all and rewrite to include new stuff -->

作为Adobe Advertising的一部分，Advertising Creative是一个自助服务平台，用于自动化实时、个性化的广告体验并可以选择在创意元素级别优化广告。

## 可重用创意的自定义创意库

通过Creative Libraries，您可以管理将在广告体验中使用的创意。 您可以创建多个库，每个库具有单个创意和创意组（称为&#x200B;*包*）。 您将向广告体验添加创意包。

## 基于规则的体验

通过[!DNL Creative]，您可以使用基于规则的决策树模型构建故事 — 展开根据您了解的受众情况实时自定义的编排广告字符串，并跟踪您的客户，即使他们迁移到不同的网站<!-- verify if that's true without Adobe CDP -->。 例如，故事可以根据客户行为、地理位置、人口统计、重新定位、客户历程中的位置等发生更改。

### 体验作为广告的实施

创建体验后，您可以为该体验生成JavaScript或iframe标记，并在Advertising DSP或任何其他DSP中将该标记作为第三方广告实施。<!-- Add any more info about integration with DSP? -->

<!-- Maybe add a subsection "Audience targeting options" with info about types of creative-level REtargeting and placement-level targeting within your DSP.  Need to clarify if any placement-level targeting might contradict/override creative-level targeting, or if they're completely different.

Advertiser should be able to target all segments which are available in DSP for targeting
-->

### 广告元素优化

您可以选择允许[!DNL Creative]使用由Adobe Sensei提供支持的经过优化、加权的广告轮换，根据效果（无论您是否定义特定受众目标）优化任何体验的广告元素。

## 正在重新定位像素

您可以创建重定位像素，以用作广告体验中创意内容的目标。 这些目标只向具有指定属性的用户显示广告，这些用户以前访问过特定网页。

## 展示、点击和转化跟踪

[!DNL Creative]自动跟踪从体验提供的广告的所有展示次数和点击次数。 您还可以选择将第三方展示跟踪和点击跟踪URL添加到Creative Libraries中的创意内容，以及体验中的自定义跟踪URL。

[!DNL Creative]还跟踪根据您的广告体验创建的已提供广告的转化。<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optoinal?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## 绩效报表

您可以在创意>体验中查看详细的体验级性能报表。

您还可以在“报表”>“自定义报表”中创建自定义Creative报表，以监控体验中的体验级别性能。 如果您在DSP促销活动中将[!DNL Creative]体验用作广告，则这些广告的效果数据可在其他自定义报表中获取，就像其他DSP广告的数据一样。<!-- Verify that [!DNL Creative] users have access to ALL other reports, and if I can completely duplicate the report help for both help sets. -->

您可以选择将自定义报告传送到指定的[报告目标](/help/dsp/reports/report-destinations/report-destination-about.md)。

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [关于您的创意库](/help/creative/creative-libraries/creative-libraries-about.md)
>* [关于Advertising Creative中的体验](/help/creative/experiences/experience-about.md)
