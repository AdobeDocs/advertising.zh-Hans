---
title: 使用决策树定位创建体验
description: 了解如何使用决策树创建定向广告体验。
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
source-git-commit: a631ac2db1f4807a3a55b41d79acfe64c04496c3
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# 使用决策树定位创建体验

*已关闭的测试版*

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. 单击&#x200B;**[!UICONTROL Create New Experience]**。

1. 输入[常规体验设置](experience-settings-targeting.md)。

1. 单击&#x200B;**[!UICONTROL Create]**。

1. 在诊断树中，执行以下操作：

   1. （可选）更改决策树的视图设置。

      您的设置会一直保存到您注销为止。

      * 通过移动滑块来放大或缩小。

      * 通过分别单击![作为垂直树查看](/help/creative/assets/tree-vertical.png "作为垂直树查看")或![以水平树状结构查看](/help/creative/assets/tree-horizontal.png "以水平树状结构查看")在查看垂直列表和水平列表之间进行切换。

   1. （可选）通过以下任何方式设置广告目标和相应的创意内容：

      * 目标：

        *[将目标节点添加到体验中的最终级别](experience-target-node-add-final.md)。

         * [在节点之间插入目标节点](experience-target-node-add-inner.md)。

         * [在节点](experience-target-node-add-sibling.md)之间添加同级目标节点。

         * [将子节点和创意复制到同一级别](experience-target-node-copy.md)的另一个节点。

      * Creative包：

         * [将创意内容分配和取消分配给最终节点](experience-assign-creative-bundles.md)。

           如果不向每个最终节点至少分配一个捆绑，则在保存体验时，可以选择为每个未分配的节点使用默认创意。 要发布体验，您必须分配捆绑包或为每个最终节点使用默认创意。

         * [自定义分配的包中创意的跟踪URL](experience-tracking-urls-targeting.md)。

         * [为分配的捆绑自定义创意优化和计划](experience-optimization-scheduling-targeting.md)。

1. （可选）在决策树和常规设置之间切换：

   * 要从决策树中打开常规设置，请单击右上角的&#x200B;**[!UICONTROL Experience Form]**。

   * 要从常规设置中打开决策树，请单击右上角的&#x200B;**[!UICONTROL Decision Tree]**。

1. 单击&#x200B;**[!UICONTROL Save]**，然后执行以下操作。

   * （如果最底层的每个节点至少包含一个创意捆绑包）单击&#x200B;**[!UICONTROL OK]**。

   * （如果最底层的每个节点均不包含至少一个创意包）执行以下操作之一：

      * 要在没有所有必需创意捆绑包的情况下保存体验，请单击&#x200B;**[!UICONTROL Save as Draft]**。

        您无法为[草稿](experience-about.md#experience-statuses)体验创建广告标记。

      * 要将默认创意分配给每个尚未分配创意捆绑包的目标，请单击&#x200B;**[!UICONTROL Assign Default Creatives]**。 在查看已分配默认创意的更新树后，单击&#x200B;**[!UICONTROL Save]**&#x200B;和&#x200B;**[!UICONTROL OK]**。

      * 要继续编辑决策树，请单击&#x200B;**[!UICONTROL Continue Edit]**。

当体验上线时，[!DNL Creative]会自动为每个适用的创意大小创建广告标记。

>[!MORELIKETHIS]
>
>* [目标体验设置](experience-settings-targeting.md)
>* [将目标节点添加到最终级别](experience-target-node-add-final.md)
>* [在节点之间插入目标节点](experience-target-node-add-inner.md)
>* [在节点之间添加同级目标节点](experience-target-node-add-sibling.md)
>* [将子节点和创意复制到同一级别的其他节点](experience-target-node-copy.md)
>* [将创意内容分配给最终节点](experience-assign-creative-bundles.md)
>* [自定义分配的包中创意内容的跟踪URL](experience-tracking-urls-targeting.md)
>* [自定义创意优化和计划](experience-optimization-scheduling-targeting.md)
>* [导出和实施实时体验的广告体验标记](/help/creative/experiences/experience-tag-export.md)
>* [使用决策树定位编辑体验](experience-edit-targeting.md)
