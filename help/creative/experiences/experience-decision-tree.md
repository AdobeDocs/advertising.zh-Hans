---
title: 决策树布局
description: 了解具有定位的体验的决策树布局。
feature: Creative Experiences
exl-id: 1d997422-8177-4a6b-b56a-e1c742b96ad2
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# [!DNL Creative]体验的决策树布局

为某个体验启用“[!UICONTROL Targeting]”选项时，您会使用决策树设置该体验。

最初，每个决策树都以根级别“全部”开头。 您可以添加一个或多个目标节点，然后将创意捆绑包分配给决策树每个分支中的最终节点。 默认情况下，决策树垂直显示，但您可以选择水平查看决策树。

![没有目标的垂直决策树示例](/help/creative/assets/experience-decision-tree-no-targets.png "没有目标的垂直决策树示例")

![没有目标的水平决策树示例](/help/creative/assets/experience-decision-tree-no-targets-horizontal.png "没有目标的水平决策树示例")

<!--
>[!NOTE]
>
>You can optionally assign creative bundles to the root level, without targets. However, the [XXXX workflow](experience-create-no-targeting.md) XXXXX is better XXX.<!-- Explain the diff and why to choose the other option. -->
>-->

## 术语

**树：**&#x200B;整个决策结构为带有分支的树。

**目标节点：**&#x200B;分支中的目标。

**叶节点：**&#x200B;分配给最终目标节点的一组创意。

## 决策树中的目标

每个决策树最多可以有五个级别的目标。 每个目标级别可以包括多个分支，每个分支具有具有相同目标类型（受众区段、地理位置类型、指定数据传递键的值、指定重定位像素的属性或设备类别）的一个或多个节点。 您可以在已为其指定默认图像创意或视频创意的每个广告大小中，将创意捆绑包分配给最低级别的目标节点。

![目标决策树示例](/help/creative/assets/experience-decision-tree.png "目标决策树示例")

将目标节点添加到最终级别时，可以指定新节点的目标。 系统会自动为与指定目标不匹配的所有用户创建一个额外的同级节点“其他所有内容”。 然后，您可以添加其他同级节点，这些节点具有不同的相同类型目标。

但是，当您在现有级别之间插入目标节点时，新级别的第一个节点最初会被分配给“全部”。 要标识特定目标，请在同一级别创建一个同级目标节点，您可以为其指定实际目标。 此操作创建目标节点，并将“所有”节点替换为“其他所有内容”节点（包括之前分配给所有内容的所有创意包）。 然后，您可以添加其他同级节点，这些节点具有不同的相同类型目标。

对于所有父节点，您可以选择复制所有子目标节点和创意捆绑包，并将其粘贴到同一级别的另一个节点中。 您可以将粘贴的节点添加到现有框架中，也可以使用它们替换现有框架。

## 决策树中的创意

将创意捆绑包分配给体验中的每个最终目标节点。

在具有创意包的每个节点中，您可以选择根据指定的权重或b)通过算法旋转包含的创意以优化点进率或自定义目标。 您还可以选择使用相同的选项按照指定的时序旋转创意。

您可以根据需要为各个创意人员自定义登陆页面URL、展示跟踪URL和点击跟踪URL。<!-- Not in the UI as of 1/31: For flexible HTML5 creatives, you can customize any of the flexible attributes. -->

>[!MORELIKETHIS]
>
>* [关于Advertising Creative 2.0](experience-about.md)中的体验
>* [创建具有定位功能的体验](/help/creative/experiences/experience-create-targeting.md)
>* [目标体验设置](/help/creative/experiences/experience-settings-targeting.md)
