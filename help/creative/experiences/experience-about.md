---
title: 关于Advertising Creative中的体验
description: 了解如何配置个性化的广告体验并根据性能优化广告元素。
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: 4b780760e5a7a0c3d370054fce8b1c15fbc6802d
workflow-type: tm+mt
source-wordcount: '1103'
ht-degree: 0%

---

# 关于Advertising Creative 2.0中的体验

*已关闭的测试版*

每个广告体验可以包含一个广告类型（标准显示、标准视频或动态显示）。 [!DNL Advertising Creative 2.0]在单个创意库中为广告提供两种不同的广告体验结构。

* **具有决策树定位的体验：** [!DNL Creative]允许您使用决策树模型在整个客户历程中配置个性化的广告体验。 您可以根据目标受众自定义所有广告元素 — 图像、标题、选件和登陆页面。

  例如，您可以为芝加哥和纽约市的特定Adobe Analytics受众区段中的人员指定相同的创意包，但是将芝加哥的人员发送至与纽约人不同的登陆页面。 此外，您还可以为区段中除芝加哥和纽约市之外的其他位置的用户指定不同的捆绑，并为不在此区段中的其他用户指定第三个捆绑。

  定位选项包括：

   * Adobe Audience Manager、Adobe Analytics和Advertising DSP中的第一方受众区段；Advertising DSP中的自定义区段；Advertising DSP提供的第三方区段

   * 特定地理位置，包括国家/地区、州、美国境内的DMA、城市和邮政编码

   * 从DSP、发布者或合作伙伴(例如SKU=01234567890123或Cart=empty)传递特定键值对（数据传递目标）的查看器

   * [!DNL Creative]重定位像素和指定的属性值

   * 特定设备类型、操作系统和浏览器

  在决策树中创建目标受众分支后，您可以通过为分支分配创意捆绑包来将目标受众与潜在创意配对。 对于每个体验，您可以自定义创意捆绑包的优化和计划，并更改每个捆绑包中单个创意的默认登陆页面和跟踪URL<!-- later: and any flexible attributes -->。

* **没有决策树定位的体验：** [!DNL Creative]会优化广告体验的广告元素，而不会缩小受众范围。 对于每个体验，您可以指定开始和结束日期以及一些默认设置，但大多数工作流并不直接在体验中。 请使用[!UICONTROL Tag Manager]为体验的每个广告大小创建广告标记，然后为其添加创意，配置创意优化和计划，以及自定义登陆页面和跟踪URL<!-- later: and any flexible attributes -->，而不是将创意直接添加到体验。

>[!NOTE]
>
> 由于这两种类型的体验具有不同的工作流，因此您无法将非定位体验更改为目标体验，也无法将目标体验更改为非目标体验。

## 广告投放和优化

<!-- MORE -->
<!-- When multiple ad variants qualify for an impression -->

[!DNL Creative]提供第一方广告并根据指定的定位（适用时）、计划、广告轮换和优化目标选项以及可用的广告库存触发体验的第三方广告。

* **计划：**（可选）计划特定创意在指定的连续时间段内运行。

* **广告轮换：**&#x200B;根据相对权重手动旋转创意，或根据指定的优化目标通过算法旋转创意。

* **优化目标：**&#x200B;为最佳点进率或现有[Advertising DSP自定义目标](/help/dsp/optimization/custom-goal.md)优化广告元素

  [!DNL Creative]通过为体验中表现最佳的资产提供展示份额来优化广告体验。 对于定位到特定受众的体验，可以根据目标受众集的单个广告元素性能来优化广告。 对于没有特定受众目标的体验，广告元素仅基于单个广告元素的性能进行优化。

例如，您可以安排Creative 1在前两周运行以优化点进率，安排Creative 2在随后两周运行，以优化指定的自定义目标。

## 实施和管理体验

创建实时体验（包含所有必需的广告元素）后，您可以[为整个体验](experience-tag-export.md)生成JavaScript或iframe标记。 您可以将Experience Tag作为广告上传到Adobe Advertising DSP中的促销活动，或作为广告在第三方DSP中实施。

>[!NOTE]
>
>分层定位行为可能因DSP而异。 Advertising DSP对投放位置级别定位应用广告级别定位。

## 您的体验的性能数据

可以使用以下性能数据：

* 当您在[!UICONTROL Metrics] > [!UICONTROL Creative]视图中启用[!UICONTROL Experiences]选项时，每个体验卡或行都会指示体验收到的展示次数和点击次数。

  ![量度选项](/help/creative/assets/metrics-option.png "量度选项")

* 您可以从[视图](experience-performance-details.md)查看任何体验[!UICONTROL Experiences]的详细性能数据。

* 要监控所有体验的表现，请创建[自定义Creative报表](/help/creative/report-custom-creative.md)。

## 体验状态 {#experience-statuses}

体验的状态是自动设置的，但手动设置的&#x200B;*已删除，*&#x200B;除外。

| 状态 | 描述 |
| ------ | ----------- |
| [!UICONTROL Live] | 该体验包含所有必需的元素，因此您可以生成体验标记，以在DSP中实施为广告。 可能计划在未来开始实时体验。 |
| [!UICONTROL Draft] | 由于体验的所有分支均未分配创意，因此体验不完整，您无法生成体验标记。 |
| [!UICONTROL Processing] | 以前的上线体验经过编辑，但现在不完整。 无法为其生成体验标记。 **注意：**&#x200B;如果您已经为体验实施了体验标记，则仍可以提供以前的实时版本。 如果您稍后完成该体验（使其重新上线），则可以使用现有标记实施提供新版本。 |
| [!UICONTROL Deleted] | 该体验已从[!DNL Creative]中删除，在[!UICONTROL Experiences]视图中不再可见。 |

>[!NOTE]
>
>您可以在DSP中更改广告的状态，而不会影响[!DNL Creative]中的体验状态。

## [!UICONTROL Experiences]视图

[!UICONTROL Experiences]视图显示所有针对性和非针对性体验。 您可以查看已分配创意或创意包的体验名称、状态、开始和结束日期、数量和维度，以及体验是否包含动态广告。 当您在[!UICONTROL Metrics]视图中启用[!UICONTROL Experiences]选项时，每个体验卡或行都会指示体验收到的展示次数和点击次数。 在卡片模式下，您可以使用&lt;和>按钮滚动浏览具有多个创意的体验中的创意。

您可以创建和管理体验、创建和重命名广告体验标记，以及导出JavaScript和iframe格式的标记，以在DSP中实施。 使用Advertising DSP的广告商可以选择将广告标记直接上传到Advertising DSP促销活动。

### 可用操作

以下是可用的关键操作。 有关完整列表，请参阅“创意人员”>“体验”章节的目录。

* [在视图中下载数据](experience-download-view.md)

* [创建](/help/creative/experiences/experience-create-targeting.md)和[编辑](/help/creative/experiences/experience-edit-targeting.md)使用定位的体验

* [创建](/help/creative/experiences/experience-create-no-targeting.md)、[编辑](/help/creative/experiences/experience-edit-no-targeting.md)和[手动为体验创建广告标记](/help/creative/experiences/experience-tag-create-manually.md)，而无需定位

* [克隆](experience-clone.md)体验

* [预览](experience-preview.md)体验

* [共享体验URL](experience-share-demo-url.md)

* [导出体验的广告标记](experience-tag-export.md)，包括选择性地将广告标记直接上传到Advertising DSP营销活动

* [删除](experience-delete.md)体验

>[!MORELIKETHIS]
>
>* [使用决策树定位创建体验](experience-create-targeting.md)
>* [在不定位的情况下创建体验](experience-create-no-targeting.md)
