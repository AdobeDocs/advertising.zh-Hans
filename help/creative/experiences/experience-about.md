---
title: 关于Advertising Creative中的体验
description: 了解如何配置个性化的广告体验并根据性能优化广告元素。
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# 关于Advertising Creative 2.0中的体验

*已关闭的测试版*

<!-- Revisit Description metadata -->

<!-- MORE -->

[!DNL Advertising Creative 2.0]为创意库<!-- can use a single library only -->中的广告提供两种不同的广告体验结构：

* **具有决策树定位的体验：** [!DNL Creative]允许您使用决策树模型在整个客户历程中配置个性化的广告体验。 您可以根据目标受众自定义所有广告元素 — 图像、标题、选件和登陆页面。

  例如，您可以为芝加哥和纽约市的特定Adobe Analytics受众区段中的人员指定相同的创意包，但是将芝加哥的同一区段中的人员发送给与纽约人不同的登陆页面。 此外，您还可以为区段中除芝加哥和纽约市之外的其他位置的用户指定不同的捆绑，并为不在此区段中的其他用户指定第三个捆绑。

  定位选项包括：来自Adobe Audience Manager、Adobe Analytics和Advertising Cloud DSP的第一方受众区段中的查看器；特定地理位置的查看器，包括国家/地区、州、美国境内的DMA、城市和邮政编码；从DSP、发布者或合作伙伴传递特定键值对（数据传递目标）的查看器；具有[!DNL Creative]重定位像素和指定属性值的查看器；以及具有特定设备类型、操作系统和浏览器的查看器。

  您可以为每个体验分配创意包，还可以选择自定义创意包的优化和计划，以及更改每个包中单个创意的默认登陆页面和跟踪URL<!-- and any flexible attributes -->。

* **没有决策树定位的体验：** [!DNL Creative]会优化广告体验的广告元素，而不会缩小受众范围。<!-- For first-party creatives, [!DNL Creative] serves the ads. -->您将为每个体验指定开始和结束日期以及一些默认设置，但大部分工作流并非直接在体验中。 您可以在[!UICONTROL Tag Manager]内为体验的每个广告大小创建广告标记，然后为其添加创意，配置创意优化和计划，以及自定义登陆页面和跟踪URL，而不是直接将创意添加到体验。

## 广告优化

<!-- MORE -->
[!DNL Creative]根据性能优化任何体验的广告元素。 对于定位到特定受众的体验，可以根据目标受众集的单个广告元素性能来优化广告。 对于没有特定受众目标的体验，广告元素会完全根据单个广告元素的性能进行优化。

## 实施和管理体验

创建实时体验（包含所有必需的广告元素）后，您可以[为整个体验](experience-tag-export.md)生成JavaScript或iframe标记，这些标记可以选择作为广告上传到Adobe Advertising DSP中的促销活动，或者在第三方DSP中作为广告实施。 [!DNL Creative]根据定位和广告轮换选项以及可用的广告库存为体验投放广告。

## 您的体验的性能数据

当您在[!UICONTROL Experiences]视图中启用[!UICONTROL Metrics]选项时，每个体验卡或行都会指示体验收到的展示次数和点击次数。

![量度选项](/help/creative/assets/metrics-option.png "量度选项")

<!-- insert screen shot of Metrics option?  If not, then add instructions elsewhere -->

<!-- I don't see this as of 1/9; why only in the table view?   You can also add conversion columns in the table view. -->

您可以从[!UICONTROL Creative] > [!UICONTROL Experiences]视图中查看任何体验的详细性能数据。 要在您的体验中监控性能，请创建[!UICONTROL Custom Creative Report]。

<!--
You can [view detailed performance data for any experience](experience-performance-details.md) from the Creative > Experiences view. To monitor performance across your experiences, [create custom reports](/help/dsp/reports/report-create.md).
-->

## 体验状态 {#experience-statuses}

<!-- verify that these are all still the same -->

体验的状态是自动设置的，但手动设置的&#x200B;*已删除，*&#x200B;除外。

*实时：*&#x200B;体验包括所有必需的元素，因此您可以生成体验标记，以在DSP中实施为广告。<!-- A live experience may be scheduled to start in the future -->

*草稿：*&#x200B;体验的所有分支均未分配创意，因此体验不完整，您无法生成体验标记。

*正在处理：*&#x200B;以前上线的体验已被编辑，但现在不完整。 无法为其生成体验标记。 **注意：**&#x200B;如果您已经为体验实施了体验标记，则仍将提供以前的实时版本。 如果您稍后完成该体验（使其重新上线），则将使用现有标记实施提供新版本。

*已删除：*&#x200B;该体验已从[!DNL Creative]中删除，并且不再显示在[!UICONTROL Experiences]视图中。

>[!NOTE]
>
>您可以在DSP中更改广告的状态，而不会影响[!DNL Creative]中的体验状态。

## [!UICONTROL Experiences]视图

[!UICONTROL Experiences]视图显示所有针对性和非针对性体验。 您可以查看已分配创意或创意包的体验名称、状态、开始和结束日期、数量和维度，以及体验是否包含动态广告。 当您在[!UICONTROL Experiences]视图中启用[!UICONTROL Metrics]选项时，每个体验卡或行都会指示体验收到的展示次数和点击次数。

您可以创建和管理体验，包括优化并将创意和创意捆绑包分配给体验。 您还可以创建和重命名广告体验标记，并导出JavaScript和iframe格式的标记，以供在DSP上实施。 使用Advertising DSP的广告商可以选择将标记作为广告直接上传到Advertising DSP促销活动。

<!--
### Available actions

* [Download data within the view](experience-download-view.md)

        + [Assign and unassign creative bundles to a final node](/help/creative/experiences/experience-assign-creative-bundles.md)
* Experiences with decision tree targeting: [Create](/help/creative/experiences/experience-create-targeting.md) and [edit](/help/creative/experiences/experience-edit-targeting.md) experiences, [assign and unassign creative bundles](/help/creative/experiences/experience-assign-creative-bundles.md), [customize creative optimization and scheduling](/help/creative/experiences/experience-optimization-scheduling-targeting.md), and [customize the tracking URLs for creatives](/help/creative/experiences/experience-tracking-urls-targeting.md)

* Experiences without decision tree targeting: [Create](experience-create-no-targeting.md) and [edit](/help/creative/experiences/experience-edit-no-targeting.md)

* [Clone](experience-clone.md) an experience

* [Preview](experience-preview.md) an experience

* [Share a demo URL](experience-share-demo-url.md) for an experience

* [Export ad tags for an experience](experience-tag-export.md)

* [Delete](experience-delete.md) an experience

-->

<!-- You can add or remove labels for your experiences.-->

<!-- Add links to workflows once they're done -->

>[!MORELIKETHIS]
>
>* [使用决策树定位创建体验](experience-create-targeting.md)
>* [在不定位的情况下创建体验](experience-create-no-targeting.md)
