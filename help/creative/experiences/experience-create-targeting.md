---
title: 使用决策树定位创建体验
description: 了解如何使用人工智能驱动或手动决策树编辑器创建有针对性的广告体验。
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
TQID: 'https://experienceleague.adobe.com/nxegtoNEqfAk7LUyb-3qD6YJYaGfx3M3QdrLx-q5y14'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
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
source-wordcount: '715'
ht-degree: 0%
---
# 使用决策树定位创建体验

使用决策树创建目标广告体验。 每个体验使用一个创意库中的广告。

默认情况下，将打开AI驱动编辑器(Beta)。 您可以通过AI代理配置树或直接编辑其画布。 您也可以切换到现有的手动编辑器。

>[!NOTE]
>
>* 创建目标体验后，无法将其更改为使用其他工作流程的非目标体验。
>* 确保您的广告体验包含与将在其中实施该功能的营销活动兼容的定位。 分层定位行为可能因DSP而异。 当您将广告体验标记上载到Advertising DSP并将其附加到投放位置时，广告级别定位将应用于（而不是）投放位置级别定位。 例如，如果投放位置以澳大利亚的用户为目标，而广告以日本的用户为目标，则广告将以“其他各项”分支为目标。

## 创建体验

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. 单击&#x200B;**[!UICONTROL Create New Experience]**。

1. 输入[常规体验设置](experience-settings-targeting.md)，并启用&#x200B;**[!UICONTROL Targeting]**。

1. 单击&#x200B;**[!UICONTROL Create]**。

   此时将打开AI驱动的决策树编辑器以提供新体验。

1. 使用以下任一过程配置树。

## 使用人工智能驱动编辑器(Beta)配置树 {#ai-editor}

1. 在对话中，描述所需的定位结构，包括每个分支的条件以及如何处理不匹配指定目标的查看者。

1. 查看画布中的树。 要请求更改，请在对话中描述这些更改。 等待助理完成处理，然后再与画布交互。

1. （可选）直接在画布中优化树：

   * [添加最终级别目标](experience-target-node-add-final.md#ai-editor)、[插入目标级别](experience-target-node-add-inner.md#ai-editor)或[添加同级目标](experience-target-node-add-sibling.md#ai-editor)。

   * [复制子节点和创意](experience-target-node-copy.md#ai-editor)或[删除节点](experience-target-node-delete.md#ai-editor)。

1. [为最终节点分配创意包](experience-assign-creative-bundles.md#ai-editor)，并可选[自定义创意优化和计划](experience-optimization-scheduling-targeting.md)和[跟踪URL](experience-tracking-urls-targeting.md#ai-editor)。

   要发布体验，必须将捆绑包分配给每个最终节点或使用体验的默认创意。 保存时，可以为未分配的节点分配默认值。

1. （可选）编辑常规体验设置：

   1. 要保存要保留的任何树更改，请单击&#x200B;**[!UICONTROL Save]**。

   1. 单击&#x200B;**[!UICONTROL Experience Form]**，然后单击&#x200B;**[!UICONTROL Yes]**&#x200B;以放弃未保存的树更改并打开表单。

   1. 编辑[常规体验设置](experience-settings-targeting.md)，然后单击&#x200B;**[!UICONTROL Save]**。

      AI驱动的编辑器将打开。

1. [保存体验](#save)。

## 使用手动编辑器配置树 {#manual-editor}

1. 在AI驱动编辑器中，单击&#x200B;**[!UICONTROL Manual Decision Tree]**，然后单击&#x200B;**[!UICONTROL Yes]**&#x200B;以退出AI驱动编辑器。

   在切换之前保存要保留的任何AI编辑器更改。 确认交换机将丢弃未保存的树更改。

1. （可选）更改视图设置：

   * 通过移动滑块来放大或缩小。

   * 通过单击![作为垂直树查看](/help/creative/assets/tree-vertical.png "作为垂直树查看")或![以水平树状结构查看](/help/creative/assets/tree-horizontal.png "以水平树状结构查看")在垂直视图和水平视图之间切换。

   视图设置会一直保存到您注销为止。

1. 配置广告目标和相应的创意内容：

   * [添加最终级别目标](experience-target-node-add-final.md#manual-editor)、[在节点之间插入目标](experience-target-node-add-inner.md#manual-editor)或[添加同级目标](experience-target-node-add-sibling.md#manual-editor)。

   * [复制子节点和创意](experience-target-node-copy.md#manual-editor)或[删除节点](experience-target-node-delete.md#manual-editor)。

   * [分配创意包](experience-assign-creative-bundles.md#manual-editor)，并可选[自定义创意优化和计划](experience-optimization-scheduling-targeting.md)和[跟踪URL](experience-tracking-urls-targeting.md#manual-editor)。

1. （可选）要编辑常规体验设置，请单击&#x200B;**[!UICONTROL Experience Form]**&#x200B;并编辑[常规体验设置](experience-settings-targeting.md)。

1. [保存体验](#save)。

## 保存体验 {#save}

以下步骤适用于两个编辑器。

{{$include /help/_includes/experience-save.md}}

## 用于保存体验的广告标记和视频转码

当体验处于实时状态时，[!DNL Creative]会为每个适用的创意大小或视频持续时间自动创建一个广告标记。 然后，您可以[导出广告标记并在DSP](/help/creative/experiences/experience-tag-export.md)中实施它。

对于视频广告体验，视频创意会在Adobe Advertising DSP中自动转码为VAST 2.0标记，以便您进行预览。 您可以选择将其他DSP的转码[应用于任何视频广告体验标签。](experience-tag-video-transcoding.md)

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
>* [查看体验的更改日志](/help/creative/experiences/experience-view-change-log.md)
