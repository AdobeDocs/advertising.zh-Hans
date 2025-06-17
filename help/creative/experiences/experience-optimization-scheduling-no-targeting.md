---
title: 自定义体验的创意优化和计划
description: 了解如何
feature: Creative Experiences
exl-id: 9398df69-6a48-4b72-8c5c-a79341bf3b8a
source-git-commit: 006b0c61c28f5fac111ccdcc007e1752e05da63f
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 0%

---

# 无需决策树定位即可自定义体验的创意优化和计划

*仅具有现有创意的体验*
*已关闭的测试版*

默认情况下，广告体验标记的创意轮换将通过算法来确定以优化整体点进率，并且创意优化设置将应用于所有分配的创意。 您可以自定义创意轮换，以根据相对权重手动运行创意，或针对指定的Advertising DSP自定义目标进行算法优化。 您还可以安排特定创意在指定的连续时段中运行，并为每个计划应用自定义创意轮换设置。

## 在不进行调度的情况下配置创意优化

禁用创意计划后，创意优化设置将应用于所有分配的创意内容。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. 执行以下操作之一：

   * 在卡片视图中，单击体验名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Tag Manager]**。

   * 在表格视图中，将光标悬停在行上，单击&#x200B;**[!UICONTROL More]**，然后单击&#x200B;**[!UICONTROL Tag Manager]**

1. 将光标悬停在适用的广告标记的行上，然后单击![广告计划](/help/creative/assets/edit-gray.png "编辑跟踪URL") **[!UICONTROL Ad Schedule]**。 <!-- For targeted experiences, this is "Edit Schedules" -->&lt;！ — 从2/2开始，Tag Manager只有一个列表视图，但没有卡片视图。>

1. 禁用&#x200B;**[!UICONTROL Schedule]**。

1. 选择创意旋转类型：

   * *[!UICONTROL Weighted]：*&#x200B;根据相对权重手动旋转创意。 输入每个创意内容的权重，以百分比表示。 所有选定创意内容的权重之和必须为100。

   * *[!UICONTROL Algorithmic]：*&#x200B;根据指定的优化目标以算法方式旋转创意。

      * 对于&#x200B;**[!UICONTROL Optimization Goal]**，选择&#x200B;*[!UICONTROL Click Through Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果选择&#x200B;*[!UICONTROL Custom Objective]*，则请选择现有的[Advertising DSP自定义目标](/help/dsp/optimization/custom-goal.md)。<!-- Verify -->

1. 单击&#x200B;**[!UICONTROL Save]**。

## 使用创意计划配置创意优化

您可以选择安排用于广告体验标记的特定创意在体验开始日期和结束日期之间的指定连续时段中运行，并为每个计划应用自定义创意轮换设置。 例如，您可以安排Creative 1在前两周运行以优化点进率，安排Creative 2在随后两周运行，以优化指定的自定义目标。

使用计划时，必须根据体验持续时间计划创意。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. 执行以下操作之一：

   * 在卡片视图中，单击体验名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Tag Manager]**。

   * 在表格视图中，将光标悬停在行上，单击&#x200B;**[!UICONTROL More]**，然后单击&#x200B;**[!UICONTROL Tag Manager]**

1. 将光标悬停在适用的广告标记的行上，然后单击![广告计划](/help/creative/assets/edit-gray.png "编辑跟踪URL") **[!UICONTROL Ad Schedule]**。 <!-- For targeted experiences, this is "Edit Schedules" -->&lt;！ — 从2/2开始，Tag Manager只有一个列表视图，但没有卡片视图。>

1. 启用&#x200B;**[!UICONTROL Schedule]**。

1. 对于第一个计划：

   1. 在左列中，选中每个要添加到第一个时间表的创意内容旁边的复选框。

   1. 指定计划的开始日期和结束日期。

   1. 选择创意旋转类型：

      * *[!UICONTROL Weighted]：*&#x200B;根据相对权重手动旋转创意。 输入每个创意内容的权重，以百分比表示。 所有选定创意内容的权重之和必须为100。

      * *[!UICONTROL Algorithmic]：*&#x200B;根据指定的优化目标以算法方式旋转创意。

         * 对于&#x200B;**[!UICONTROL Optimization Goal]**，选择&#x200B;*[!UICONTROL Click Through Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果选择&#x200B;*[!UICONTROL Custom Objective]*，则请选择现有的[Advertising DSP自定义目标](/help/dsp/optimization/custom-goal.md)。<!-- Verify -->

1. 对于每个附加计划：

   1. 单击&#x200B;**[!UICONTROL + Add Schedule]**。

   1. 在左列中，选中每个要添加到第一个时间表的创意内容旁边的复选框。

   1. 指定计划的开始日期和结束日期。

   1. 选择创意旋转类型：

      * *[!UICONTROL Weighted]：*&#x200B;根据相对权重手动旋转创意。 输入每个创意内容的权重，以百分比表示。 所有选定创意内容的权重之和必须为100。

      * *[!UICONTROL Algorithmic]：*&#x200B;根据指定的优化目标以算法方式旋转创意。

         * 对于&#x200B;**[!UICONTROL Optimization Goal]**，选择&#x200B;*[!UICONTROL Click Through Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果选择&#x200B;*[!UICONTROL Custom Objective]*，则请选择现有的[Advertising DSP自定义目标](/help/dsp/optimization/custom-goal.md)。<!-- Verify -->

1. 单击&#x200B;**[!UICONTROL Save]**。

>[!MORELIKETHIS]
>
>* [为适用的创意大小手动创建广告标签](/help/creative/experiences/experience-tag-create-manually.md)
>* [将创意内容分配给无定位体验的广告标记](experience-tag-assign-creatives.md)
>* [自定义没有决策树定位的体验的跟踪URL](experience-tracking-urls-no-targeting.md)
