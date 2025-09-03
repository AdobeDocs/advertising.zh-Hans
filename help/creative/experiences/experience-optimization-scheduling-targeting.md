---
title: 自定义体验的创意优化和计划
description: 了解如何
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
source-git-commit: a271589a2cb51ec50c37a52254fd8d1b535f279a
workflow-type: tm+mt
source-wordcount: '1073'
ht-degree: 0%

---

# 通过决策树定位为体验自定义创意优化和计划

*仅定位具有现有创意的节点*

默认情况下，通过算法确定体验的创意轮换以优化整体点进率，创意优化设置适用于所有分配的包。 您可以自定义创意轮换以手动运行每个捆绑中的创意，从而通过算法优化来达到指定的Advertising DSP自定义目标；根据指定的捆绑序列，在每个捆绑序列中指定展示次数；或根据相对权重。 您还可以安排特定创意捆绑包在指定的连续时间段内运行，并为每个计划应用自定义创意轮换设置。

>[!NOTE]
>
>这些功能不适用于使用默认创意而非指定创意的节点。

## 在不进行调度的情况下配置创意优化

禁用创意计划后，创意优化设置将应用于所有分配的创意内容。

1. 将光标悬停在目标节点下方的创意叶节点上，然后单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Creative Optimization]**。

1. 禁用&#x200B;**[!UICONTROL Schedule]**。

1. 选择创意旋转类型：

   * *[!UICONTROL Weighted]：*&#x200B;根据相对权重手动旋转每个包中的创意。 输入每个束的重量（百分比）。 所有捆绑的重量之和必须为100。

   * *[!UICONTROL Algorithmic]：*&#x200B;根据指定的优化目标以算法方式旋转每个包中的创意。

      * 对于&#x200B;**[!UICONTROL Optimization Goal]**，选择&#x200B;*[!UICONTROL Click Through Rate]*、（标准视频广告体验） *[!UICONTROL Completion Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果选择&#x200B;*[!UICONTROL Custom Objective]*，则请选择现有的[Advertising DSP自定义目标](/help/dsp/optimization/custom-goal.md)。

   * *[!UICONTROL Sequencing]：*&#x200B;按指定的顺序（包1先提供，包2先提供，依此类推）旋转关联的创意包，每个包序列具有指定的展示总数。 提供的广告大小由可用库存决定。 可将序列中的最后一个束配置为a\)无限显示（缺省值）或b\)循环返回到第一个束。 例如，您可以在包1中显示三(3)次印象的任何创意，在包2中显示一(1)次印象的任何创意，然后在包3中显示两(2)次印象的任何创意，然后再次开始循环。 或者，一旦显示束3中的创意，您就可以继续无限期地显示束3中的创意，而不是创建循环。 在启用排序时：

      1. 将分配的捆绑包拖放到所需顺序中。

     默认情况下，分配的捆绑包将按照其添加到体验中的顺序进行排列。

      1. 输入每个序列的展示次数。

      1. 对于最后一个序列，将是否更改为a\)无限期地显示序列中的最后一个捆绑(*[!UICONTROL Infinite]* （默认值）或b\)在显示最后一个捆绑后，回圈到第一个捆绑(*[!UICONTROL Keep in Loop]*)。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 使用创意计划配置创意优化

您可以选择安排特定创意捆绑包在体验开始日期和结束日期之间的指定连续时间段内运行，并为每个计划应用自定义创意轮换设置。 例如，您可以计划捆绑1在前两周运行以优化点进率，并计划捆绑2在后两周运行以优化指定的自定义目标。

使用计划编制时，必须在体验的持续时间中计划捆绑包。

1. 将光标悬停在目标节点下方的创意叶节点上，然后单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Creative Optimization]**。

1. 启用&#x200B;**[!UICONTROL Schedule]**。

1. 对于第一个计划：

   1. 在左列中，选中要添加到第一个计划中的每个创意捆绑包旁边的复选框。

   1. 指定计划的开始日期和结束日期。

   1. 选择创意旋转类型：

      * *[!UICONTROL Weighted]：*&#x200B;根据相对权重手动旋转每个包中的创意。 输入每个束的重量（百分比）。 所有选定包的权重之和必须为100。

      * *[!UICONTROL Algorithmic]：*&#x200B;根据指定的优化目标以算法方式旋转每个包中的创意。

         * 对于&#x200B;**[!UICONTROL Optimization Goal]**，选择&#x200B;*[!UICONTROL Click Through Rate]*、（标准视频广告体验） *[!UICONTROL Completion Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果选择&#x200B;*[!UICONTROL Custom Objective]*，则请选择现有的[Advertising DSP自定义目标](/help/dsp/optimization/custom-goal.md)。

      * *[!UICONTROL Sequencing]：*&#x200B;按指定的顺序（包1先提供，包2先提供，依此类推）旋转关联的创意包，每个包序列具有指定的展示总数。 提供的广告大小由可用库存决定。 可将序列中的最后一个束配置为a\)无限显示（缺省值）或b\)循环返回到第一个束。 例如，您可以在包1中显示三(3)次印象的任何创意，在包2中显示一(1)次印象的任何创意，然后在包3中显示两(2)次印象的任何创意，然后再次开始循环。 或者，一旦显示束3中的创意，您就可以继续无限期地显示束3中的创意，而不是创建循环。 在启用排序时：

         1. 将分配的捆绑包拖放到所需顺序中。

            默认情况下，分配的捆绑包将按照其添加到体验中的顺序进行排列。

         1. 输入每个序列的展示次数。

         1. 对于最后一个序列，将是否更改为a\)无限期地显示序列中的最后一个捆绑(*[!UICONTROL Infinite]* （默认值）或b\)在显示最后一个捆绑后，回圈到第一个捆绑(*[!UICONTROL Keep in Loop]*)。

1. 对于每个附加计划：

   1. 单击&#x200B;**[!UICONTROL + Add Schedule]**。

   1. 在左列中，选中要添加到第一个计划中的每个创意捆绑包旁边的复选框。

   1. 指定计划的开始日期和结束日期。

   1. 选择创意旋转类型：

      * *[!UICONTROL Weighted]：*&#x200B;根据相对权重手动旋转每个包中的创意。 输入每个束的重量（百分比）。 所有选定包的权重之和必须为100。

      * *[!UICONTROL Algorithmic]：*&#x200B;根据指定的优化目标以算法方式旋转每个包中的创意。

         * 对于&#x200B;**[!UICONTROL Optimization Goal]**，选择&#x200B;*[!UICONTROL Click Through Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。  如果选择&#x200B;*[!UICONTROL Custom Objective]*，则请选择现有的[Advertising DSP自定义目标](/help/dsp/optimization/custom-goal.md)。

      * *[!UICONTROL Sequencing]：*&#x200B;按指定的顺序旋转关联的创意包，每个包序列具有指定的展示总数。 在启用排序时：

         1. 将分配的捆绑包拖放到所需顺序中。

            默认情况下，分配的捆绑包将按照其添加到体验中的顺序进行排列。

         1. 输入每个序列的展示次数。

         1. 对于最后一个序列，将是否更改为a\)无限期地显示序列中的最后一个捆绑(*[!UICONTROL Infinite]* （默认值）或b\)在显示最后一个捆绑后，回圈到第一个捆绑(*[!UICONTROL Keep in Loop]*)。

1. 单击&#x200B;**[!UICONTROL Save]**。

>[!MORELIKETHIS]
>
>* [向体验中的最终节点分配和取消分配创意包](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [自定义创意内容的跟踪URL](/help/creative/experiences/experience-tracking-urls-targeting.md)
