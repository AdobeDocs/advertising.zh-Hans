---
title: 使用决策树定位编辑体验
description: 了解如何使用人工智能驱动或手动决策树编辑器编辑定向广告体验。
feature: Creative Experiences
exl-id: 8c5e8f9b-c405-41b2-98a9-da7c5debd3e1
TQID: 'https://experienceleague.adobe.com/0mcPjfiET-DKrm2qaa1Odygv1GIgv4cR7lBRNmrYGBk'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%
---
# 使用决策树定位编辑体验

默认情况下，会为具有定位的体验打开AI驱动编辑器(Beta)。 您可以使用AI代理、直接编辑画布或打开现有的手动编辑器。

## 打开体验 {#experience-open}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. （可选）[自定义视图](/help/creative/introduction/customize-data-views.md)以包含特定体验。

1. 执行以下操作之一：

   * 要打开AI驱动的编辑器，请执行以下操作：

     * 在卡片视图中，单击体验名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Edit]**。

     * 在表格视图中，将光标悬停在行上，单击&#x200B;**[!UICONTROL More]**，然后单击&#x200B;**[!UICONTROL Edit]**。

   * 要打开手动编辑器，请执行以下操作：

     * 在卡片视图中，单击体验名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Create Decision Tree Manually (Legacy)]**。

     * 在表格视图中，将光标悬停在行上，单击&#x200B;**[!UICONTROL More]**，然后单击&#x200B;**[!UICONTROL Create Decision Tree Manually (Legacy)]**。

     * 在AI驱动的编辑器中，

## 使用AI驱动编辑器编辑(Beta) {#ai-editor}

1. [打开体验](#experience-open)。

1. 描述您希望在对话中进行的定位更改。 通过受其目标或节点ID（在画布上显示）标识受影响的分支。

1. 查看更新的树，并描述任何进一步的更改。 等待助理完成处理，然后再与画布交互。

1. （可选）直接在画布中进行更改：

   * [添加最终级别目标](experience-target-node-add-final.md#ai-editor)、[插入目标级别](experience-target-node-add-inner.md#ai-editor)或[添加同级目标](experience-target-node-add-sibling.md#ai-editor)。

   * 通过单击目标旁边的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit]**，更改值，然后单击&#x200B;**[!UICONTROL Edit Node]**&#x200B;来编辑目标的条件。

   * [复制子节点和创意](experience-target-node-copy.md#ai-editor)或[删除节点](experience-target-node-delete.md#ai-editor)。

   * [分配或取消分配创意包](experience-assign-creative-bundles.md#ai-editor)。

   * [自定义创意优化和计划](experience-optimization-scheduling-targeting.md)或[跟踪URL](experience-tracking-urls-targeting.md#ai-editor)。

1. [保存体验](#save)。

## 使用手动编辑器编辑 {#manual-editor}

1. [打开体验](#experience-open)。

1. （状态为`[processing](experience-about.md#experience-statuses)`的体验）如果系统提示存在未发布的现有草稿，请执行下列操作之一：

   * 单击&#x200B;**[!UICONTROL Continue editing draft]**&#x200B;以查看并继续编辑草稿。

   * 单击&#x200B;**[!UICONTROL Discard and start again]**&#x200B;可放弃草稿并从实时版本开始。

   * 单击&#x200B;**[!UICONTROL Cancel this edit]**&#x200B;停止编辑。

1. （可选）调整缩放滑块，或单击![以垂直树查看](/help/creative/assets/tree-vertical.png "以垂直树查看")或![以水平树状结构查看](/help/creative/assets/tree-horizontal.png "以水平树状结构查看")以更改方向。

   视图设置会一直保存到您注销为止。

1. 根据需要更改目标和创意：

   * [添加最终级别目标](experience-target-node-add-final.md#manual-editor)、[在节点之间插入目标](experience-target-node-add-inner.md#manual-editor)或[添加同级目标](experience-target-node-add-sibling.md#manual-editor)。

   * [复制子节点和创意](experience-target-node-copy.md#manual-editor)或[删除节点](experience-target-node-delete.md#manual-editor)。

   * [分配或取消分配创意包](experience-assign-creative-bundles.md#manual-editor)。

   * [自定义创意优化和计划](experience-optimization-scheduling-targeting.md)或[跟踪URL](experience-tracking-urls-targeting.md#manual-editor)。

1. [保存体验](#save)。

## 切换编辑器或编辑体验设置 {#switch-editors}

>[!IMPORTANT]
>
>在退出AI驱动编辑器之前，请保存要保留的任何树更改。 切换到手动编辑器或体验表单不会传输未保存的更改。

* **AI驱动编辑器到手动编辑器：**&#x200B;单击&#x200B;**[!UICONTROL Manual Decision Tree]**。 在确认对话框中，单击&#x200B;**[!UICONTROL Yes]**&#x200B;以放弃未保存的更改并打开手动编辑器，或单击&#x200B;**[!UICONTROL No]**&#x200B;以保留。

* **AI驱动编辑器到常规设置：**&#x200B;单击&#x200B;**[!UICONTROL Experience Form]**，然后单击&#x200B;**[!UICONTROL Yes]**&#x200B;放弃未保存的树更改并打开表单。 编辑[常规体验设置](experience-settings-targeting.md)，然后单击&#x200B;**[!UICONTROL Save]**。

* **手动编辑常规设置：**&#x200B;保存要保留的任何树更改，然后单击&#x200B;**[!UICONTROL Experience Form]**。 编辑[常规体验设置](experience-settings-targeting.md)，然后单击&#x200B;**[!UICONTROL Save]**。

* **AI驱动编辑器的常规设置：**&#x200B;单击&#x200B;**[!UICONTROL Decision Tree]**。 保存对目标体验常规设置的更改也会打开AI驱动的编辑器。

* **手动编辑器到AI驱动编辑器：**&#x200B;保存树更改，返回[!UICONTROL Experiences]视图，并选择&#x200B;**[!UICONTROL Edit]**&#x200B;体验。

要退出AI驱动编辑器而不打开其他编辑器，请单击&#x200B;**[!UICONTROL Cancel]**。 单击&#x200B;**[!UICONTROL Yes]**&#x200B;可放弃未保存的树更改，单击&#x200B;**[!UICONTROL No]**&#x200B;可继续编辑。

## 保存体验 {#save}

以下步骤适用于两个编辑器。

{{$include /help/_includes/experience-save.md}}

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
>* [使用决策树定位创建体验](experience-create-targeting.md)
>* [查看体验的更改日志](/help/creative/experiences/experience-view-change-log.md)
