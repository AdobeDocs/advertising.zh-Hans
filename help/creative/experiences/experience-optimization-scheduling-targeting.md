---
title: 自定义体验的创意优化和计划
description: 了解如何
feature: Creative Experiences
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---

# 通过决策树定位为体验自定义创意优化和计划

*仅定位具有现有创意的节点*
*已关闭的测试版*

默认情况下，通过算法确定体验的创意轮换以优化整体点进率，创意优化设置适用于所有分配的包。 您可以自定义创意轮换，以根据相对权重手动运行每个包中的创意，或针对指定的Advertising DSP自定义目标进行算法优化。 <!-- verify -->您还可以安排特定创意包在指定的连续时间段运行，并为每个计划应用自定义创意轮换设置。

>[!NOTE]
>
>这些功能不适用于使用默认图像创意而非指定创意的节点。

## 在不进行调度的情况下配置创意优化

禁用创意计划后，创意优化设置将应用于所有分配的创意内容。

1. 将光标悬停在目标节点下方的创意叶节点上，然后单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]**。

1. 禁用&#x200B;**[!UICONTROL Schedule]**。

1. 选择创意旋转类型：

   * ** *加权*** — 根据相对权重手动旋转每个包中的创意。 输入每个束的重量（百分比）。 所有捆绑的重量之和必须为100。

   * ** *算法*** — 根据指定的优化目标以算法方式旋转每个包中的创意。

   * 对于&#x200B;**[!UICONTROL Optimization Goal]**，选择&#x200B;*[!UICONTROL Click Through Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果选择&#x200B;*[!UICONTROL Custom Objective]*，则请选择现有的[Advertising DSP自定义目标](/help/dsp/optimization/custom-goal.md)。<!-- Verify -->

1. 单击&#x200B;**[!UICONTROL Save]**。

## 使用创意计划配置创意优化

您可以选择安排特定创意捆绑包在体验开始日期和结束日期之间的指定连续时间段内运行，并为每个计划应用自定义创意轮换设置。 例如，您可以计划捆绑1在前两周运行以优化点进率，并计划捆绑2在后两周运行以优化指定的自定义目标。

使用计划编制时，必须在体验的持续时间中计划捆绑包。

1. 将光标悬停在目标节点下方的创意叶节点上，然后单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]**。

1. 启用&#x200B;**[!UICONTROL Schedule]**。

1. 对于第一个计划：

   1. 在左列中，选中要添加到第一个计划中的每个创意捆绑包旁边的复选框。

   1. 指定计划的开始日期和结束日期。

   1. 选择创意旋转类型：

      * ** *加权*** — 根据相对权重手动旋转每个包中的创意。 输入每个束的重量（百分比）。 所有选定包的权重之和必须为100。

      * ** *算法*** — 根据指定的优化目标以算法方式旋转每个包中的创意。

      * 对于&#x200B;**[!UICONTROL Optimization Goal]**，选择&#x200B;*[!UICONTROL Click Through Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果选择&#x200B;*[!UICONTROL Custom Objective]*，则请选择现有的[Advertising DSP自定义目标](/help/dsp/optimization/custom-goal.md)。<!-- Verify -->

1. 对于每个附加计划：

   1. 单击&#x200B;**[!UICONTROL + Add Schedule]**。

   1. 在左列中，选中要添加到第一个计划中的每个创意捆绑包旁边的复选框。

   1. 指定计划的开始日期和结束日期。

   1. 选择创意旋转类型：

      * ** *加权*** — 根据相对权重手动旋转每个包中的创意。 输入每个束的重量（百分比）。 所有选定包的权重之和必须为100。

      * ** *算法*** — 根据指定的优化目标以算法方式旋转每个包中的创意。

      * 对于&#x200B;**[!UICONTROL Optimization Goal]**，选择&#x200B;*[!UICONTROL Click Through Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果选择&#x200B;*[!UICONTROL Custom Objective]*，则请选择现有的[Advertising DSP自定义目标](/help/dsp/optimization/custom-goal.md)。<!-- Verify -->

1. 单击&#x200B;**[!UICONTROL Save]**。

>[!MORELIKETHIS]
>
>* [向体验中的最终节点分配和取消分配创意包](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [自定义创意内容的跟踪URL](/help/creative/experiences/experience-tracking-urls-targeting.md)
