---
title: 将创意捆绑包分配和取消分配给体验中的最终节点
description: 了解如何在广告体验中为每个目标分配创意元素。
feature: Creative Experiences
exl-id: 5449a760-6ade-41c0-9cab-bd92026b150b
source-git-commit: 2cf156702b44fe01d217f0f3ca4893a5af64e95f
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# 将创意捆绑包分配和取消分配给体验中的最终节点

*仅使用决策树定位的体验*

您可以将创意捆绑包分配给体验决策树中最低级别的目标节点。 对于尚未配置目标的体验，最底层的级别在“全部”下。

对于标准广告体验，您只能分配标准创意捆绑包。 对于动态广告体验，您只能分配动态创意捆绑包。

>[!NOTE]
>
>如果未向每个最终节点至少分配一个创意捆绑包，则可以选择在[保存体验](experience-create-targeting.md)时为每个未分配的节点使用默认创意。 要发布体验，必须分配捆绑包或使用每个最终节点的默认创意元素。

<!-- 1. [ways to get to the decision tree] -->

1. 执行以下操作之一：

   * （没有创意的最终节点）在该节点下，单击&#x200B;**[!UICONTROL Assign Bundles]**。

   * （包含现有创意的节点）将光标悬停在目标节点下方的创意捆绑包框上，然后单击“**[!UICONTROL ...]**”>“**[!UICONTROL Edit Bundles]**”。

1. 选中要分配给目标节点的每个捆绑旁边的复选框，并取消选中要取消分配的每个捆绑旁边的复选框。

   仅列出体验的相关捆绑类型的捆绑包（标准捆绑包或动态捆绑包）。

1. 单击&#x200B;**[!UICONTROL Save]**。

1. （可选） [为分配的捆绑包自定义创意优化和计划](experience-optimization-scheduling-targeting.md)。

1. （可选）[自定义所分配捆绑包中创意作品的跟踪URL](experience-tracking-urls-targeting.md)。

<!--
1. (Optional) To save the experience, click **[!UICONTROL Save]**, and then do the following.
...

These formatted steps are inserted automatically from text in the following file in the _includes folder, which reused in multiple places.
-->

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [将目标节点添加到最终级别](experience-target-node-add-final.md)
>* [在节点之间插入目标节点](experience-target-node-add-inner.md)
>* [在节点之间添加同级目标节点](experience-target-node-add-sibling.md)
>* [将子节点和创意内容复制到同一级别的其他节点](experience-target-node-copy.md)
>* [使用决策树定位创建体验](experience-create-targeting.md)
>* [编辑决策树定位体验](experience-edit-targeting.md)
>* [目标体验设置](experience-settings-targeting.md)
>* [导出和实施广告体验标记以获得实时体验](experience-tag-export.md)
>* [查看体验的更改日志](/help/creative/experiences/experience-view-change-log.md)
