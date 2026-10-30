---
title: 自定义体验的创意优化和计划
description: 了解如何针对目标体验配置优化和广告计划。
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
TQID: 'https://experienceleague.adobe.com/gDBTQn7F0ZNeiEylTDA9HNgDockR6FHE3MSvr0bJaDM'
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
source-wordcount: '1244'
ht-degree: 0%
---
# 通过决策树定位为体验自定义创意优化和计划

*仅定位具有现有创意的节点*

默认情况下，体验会优化所有已分配捆绑的总体点进率的创意轮换。 您可以自定义轮换设置或计划特定捆绑包在连续时间段内运行，并为每个计划设置单独的轮换设置。

>[!NOTE]
>
>这些功能不适用于使用默认创意而非指定创意的节点。

您可以直接在AI驱动编辑器(Beta)的画布中或手动编辑器中配置这些设置。 在任一编辑器中，保存包对话框都会更新工作树；您还必须从树标头[保存体验](#save)。

## 旋转设置 {#rotation-settings}

* **[!UICONTROL Weighted]：**&#x200B;根据相对权重在关联的创意包中显示广告变体。

* **[!UICONTROL Algorithmic]：**&#x200B;根据指定的优化目标（如点进率或Advertising DSP自定义目标），更频繁地显示最有效的广告变体。

* **[!UICONTROL Sequence]（AI驱动编辑器）或[!UICONTROL Sequencing] （手动编辑器）：**&#x200B;按指定顺序显示关联的创意包，序列中的每个包具有指定数量的展示次数。 默认情况下，捆绑包会按照其添加到体验中的顺序进行排列。 提供的广告大小由可用库存决定。 最终捆绑可以无限期地提供（默认），或者序列可以循环返回到第一个捆绑。

  例如，序列可以为三个展示提供组合1中的广告变体，为一次展示提供组合2，为两次展示提供组合3，然后重复此操作。 如果没有循环，包3将无限期地继续运行。

## 在不进行调度的情况下配置创意优化

禁用创意计划后，创意优化设置将应用于所有分配的创意内容。

### 使用AI驱动编辑器(Beta) {#without-scheduling-ai}

1. 当您[创建](experience-create-targeting.md#ai-editor)或[编辑](experience-edit-targeting.md#ai-editor)体验时，在创意叶节点上单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**。

   对于没有捆绑包的最后一个节点，单击&#x200B;**[!UICONTROL Assign Bundles]**&#x200B;并先[分配捆绑包](experience-assign-creative-bundles.md#ai-editor)。

1. 打开&#x200B;**[!UICONTROL Creative optimisation]**&#x200B;选项卡。

1. 禁用&#x200B;**[!UICONTROL Schedule]**。

1. 选择创意旋转类型并配置其设置：

   * **[!UICONTROL Weighted]：**&#x200B;输入每个包行的相对权重。 总重量必须为100。 若要平均分配权重，请单击&#x200B;**[!UICONTROL Apply equal weight]**。

   * **[!UICONTROL Algorithmic]：**&#x200B;选择一个&#x200B;**[!UICONTROL Optimization goals]**&#x200B;选项。 如果选择自定义目标，请在&#x200B;**[!UICONTROL Custom objective]**&#x200B;中选择现有[Advertising DSP自定义目标](/help/dsp/optimization/custom-goal.md)。

   * **[!UICONTROL Sequence]：**&#x200B;将捆绑包拖入所需的顺序，然后输入每个序列的展示次数。 启用&#x200B;**[!UICONTROL Keep in loop]**&#x200B;以重复该序列，或保持禁用状态以将最后一个包的展示次数设置为&#x200B;**[!UICONTROL Infinite]**。

1. 单击对话框中的&#x200B;**[!UICONTROL Save]**。

1. [保存体验](#save)。

### 使用手动编辑器 {#without-scheduling-manual}

[在执行以下步骤之前，请打开手动编辑器](experience-edit-targeting.md#experience-open)。

1. 当您[创建](experience-create-targeting.md)或[编辑](experience-edit-targeting.md)体验时，请打开创意优化设置：

   1. 将光标悬停在目标节点下方的创意叶节点上，然后执行以下操作：

      * 对于现有包，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**。

      * 对于新包，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]**&#x200B;并[分配包](experience-assign-creative-bundles.md)。

   1. 单击&#x200B;**[!UICONTROL Creative Optimization]**&#x200B;选项卡。

1. 禁用&#x200B;**[!UICONTROL Schedule]**。

1. 为关联捆绑包中的广告变体选择创意轮换类型：

   * *[!UICONTROL Weighted]：*&#x200B;以百分比形式输入每个包的权重。 若要对所有关联捆绑应用等权重，请单击（![应用等权重](/help/creative/assets/apply-equal-weight.png "应用等权重")）。 所有选定包的权重之和必须为100。

   * *[!UICONTROL Algorithmic]：*&#x200B;对于&#x200B;**[!UICONTROL Optimization Goal]**，请选择&#x200B;*[!UICONTROL Click Through Rate]*、（标准视频广告体验） *[!UICONTROL Completion Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。 如果选择&#x200B;*[!UICONTROL Custom Objective]*，则请选择现有的[Advertising DSP自定义目标](/help/dsp/optimization/custom-goal.md)。

   * *[!UICONTROL Sequencing]:*

     1. 将分配的捆绑包拖放到所需顺序中。

     1. 输入每个序列的展示次数。

     1. 对于最后一个序列，将是否更改为a\)无限期地显示序列中的最后一个捆绑(*[!UICONTROL Infinite]* （默认值）或b\)在显示最后一个捆绑后，回圈到第一个捆绑(*[!UICONTROL Keep in Loop]*)。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 使用创意计划配置创意优化

您可以选择安排特定创意捆绑包在体验开始日期和结束日期之间的指定连续时间段内运行，并为每个计划应用自定义创意轮换设置。 例如，您可以计划捆绑1在前两周运行以优化点进率，并计划捆绑2在后两周运行以优化指定的自定义目标。

使用计划编制时，必须在体验的持续时间中计划捆绑包。

### 使用AI驱动编辑器(Beta) {#with-scheduling-ai}

1. 当您[创建](experience-create-targeting.md#ai-editor)或[编辑](experience-edit-targeting.md#ai-editor)体验时，在创意叶节点上单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**。

   对于没有捆绑包的最后一个节点，单击&#x200B;**[!UICONTROL Assign Bundles]**&#x200B;并先[分配捆绑包](experience-assign-creative-bundles.md#ai-editor)。

1. 打开&#x200B;**[!UICONTROL Creative optimisation]**&#x200B;选项卡，并启用&#x200B;**[!UICONTROL Schedule]**。

1. 为计划选择&#x200B;**[!UICONTROL Timezone]**。

1. 对于第一个计划：

   1. 选中要包含在左列中的每个束旁边的复选框。

   1. 指定开始和结束日期及时间。

   1. 选择创意旋转类型并配置其设置：

      * **[!UICONTROL Weighted]：**&#x200B;输入计划中每个包行的相对权重。 总重量必须为100。 若要平均分配权重，请单击&#x200B;**[!UICONTROL Apply equal weight]**。

      * **[!UICONTROL Algorithmic]：**&#x200B;选择一个&#x200B;**[!UICONTROL Optimization goals]**&#x200B;选项。 如果选择自定义目标，请在&#x200B;**[!UICONTROL Custom objective]**&#x200B;中选择现有[Advertising DSP自定义目标](/help/dsp/optimization/custom-goal.md)。

      * **[!UICONTROL Sequence]：**&#x200B;将捆绑包拖入所需的顺序，然后输入每个序列的展示次数。 启用&#x200B;**[!UICONTROL Keep in loop]**&#x200B;以重复该序列，或保持禁用状态以将最后一个包的展示次数设置为&#x200B;**[!UICONTROL Infinite]**。

1. 对于每个其他计划，请单击&#x200B;**[!UICONTROL + Add Schedule]**，选择其计划卡片，并配置其包、日期和时间以及轮换设置。

   捆绑复选框适用于选定的计划，而非所有计划。 确保这些计划包含分配的捆绑包的整个体验持续时间。

1. 单击对话框中的&#x200B;**[!UICONTROL Save]**。

1. [保存体验](#save)。

### 使用手动编辑器 {#with-scheduling-manual}

[在执行以下步骤之前，请打开手动编辑器](experience-edit-targeting.md#experience-open)。

1. 当您[创建](experience-create-targeting.md)或[编辑](experience-edit-targeting.md)体验时，请打开创意优化设置：

   1. 将光标悬停在目标节点下方的创意叶节点上，然后执行以下操作：

      * 对于现有包，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**。

      * 对于新包，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]**&#x200B;并[分配包](experience-assign-creative-bundles.md)。

   1. 单击&#x200B;**[!UICONTROL Creative Optimization]**&#x200B;选项卡。

1. 启用&#x200B;**[!UICONTROL Schedule]**。

1. 对于第一个计划：

   1. 在左列中，选中要添加到第一个计划中的每个创意捆绑包旁边的复选框。

   1. 指定计划的开始日期和开始时间以及结束日期和结束时间。

   1. 选择创意旋转类型：

      * *[!UICONTROL Weighted]：*&#x200B;以百分比形式输入每个包的权重。 要对计划中的所有捆绑应用相等权重，请单击（![应用相等权重](/help/creative/assets/apply-equal-weight.png "应用相等权重")）。 所有选定包的权重之和必须为100。

      * *[!UICONTROL Algorithmic]：*&#x200B;对于&#x200B;**[!UICONTROL Optimization Goal]**，请选择&#x200B;*[!UICONTROL Click Through Rate]*、（标准视频广告体验） *[!UICONTROL Completion Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。 如果选择&#x200B;*[!UICONTROL Custom Objective]*，则请选择现有的[Advertising DSP自定义目标](/help/dsp/optimization/custom-goal.md)。

      * *[!UICONTROL Sequencing]:*

        1. 将分配的捆绑包拖放到所需顺序中。

        1. 输入每个序列的展示次数。

        1. 对于最后一个序列，将是否更改为a\)无限期地显示序列中的最后一个捆绑(*[!UICONTROL Infinite]* （默认值）或b\)在显示最后一个捆绑后，回圈到第一个捆绑(*[!UICONTROL Keep in Loop]*)。

1. 对于每个附加计划：

   1. 单击&#x200B;**[!UICONTROL + Add Schedule]**。

   1. 在左列中，选中要添加到第一个计划中的每个创意捆绑包旁边的复选框。

   1. 指定计划的开始日期和结束日期。

   1. 选择创意旋转类型：

      * *[!UICONTROL Weighted]：*&#x200B;以百分比形式输入每个包的权重。 所有选定包的权重之和必须为100。

      * *[!UICONTROL Algorithmic]：*&#x200B;对于&#x200B;**[!UICONTROL Optimization Goal]**，请选择&#x200B;*[!UICONTROL Click Through Rate]*&#x200B;或&#x200B;*[!UICONTROL Custom Objective]*。 如果选择&#x200B;*[!UICONTROL Custom Objective]*，则请选择现有的[Advertising DSP自定义目标](/help/dsp/optimization/custom-goal.md)。

      * *[!UICONTROL Sequencing]:*

        1. 将分配的捆绑包拖放到所需顺序中。

        1. 输入每个序列的展示次数。

        1. 对于最后一个序列，将是否更改为a\)无限期地显示序列中的最后一个捆绑(*[!UICONTROL Infinite]* （默认值）或b\)在显示最后一个捆绑后，回圈到第一个捆绑(*[!UICONTROL Keep in Loop]*)。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 保存体验 {#save}

以下步骤适用于两个编辑器。

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [向体验中的最终节点分配和取消分配创意包](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [自定义创意内容的跟踪URL](/help/creative/experiences/experience-tracking-urls-targeting.md)
>* [查看体验的更改日志](/help/creative/experiences/experience-view-change-log.md)
