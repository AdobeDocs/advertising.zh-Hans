---
title: 在体验中的节点之间添加目标节点
description: 了解如何在广告体验中的目标节点之间添加目标节点。
feature: Creative Experiences
exl-id: ac9211e5-c6ed-4185-bf9c-c2689f1b2775
TQID: 'https://experienceleague.adobe.com/lPQtymUs3okctV2t6ZEE2rMG-F-BA2tJZO1GuceTxtY'
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
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '1117'
ht-degree: 0%
---
# 在体验中的节点之间添加目标节点

*仅具有决策树定位的体验*

在现有级别之间插入目标节点时，新目标节点将保留所有现有的子目标和创意，并且新节点最初称为“全部”。 您可以选择保留新节点，而不添加更具体的目标。

要定义特定目标，请在同一级别添加其他同级目标节点，指定新目标，然后将创意仅分配给该目标。 添加同级目标节点将创建新的目标节点，并将之前分配给“全部”的所有子目标和创意移动到同一级别的新“其他所有内容”节点。 这样，新目标的添加不会影响现有的子分支，因为只有新的同级节点包含新的定向信息。

>[!NOTE]
>
>若要将目标节点添加到决策树的底层，请参阅“[将目标节点添加到体验中的最后一层](experience-target-node-add-final.md)”。

## 使用AI驱动编辑器(Beta) {#ai-editor}

当您[创建](experience-create-targeting.md#ai-editor)或[编辑](experience-edit-targeting.md#ai-editor)体验时，可以请求AI代理插入目标级别。 确定插入位置以及要保留的现有分支和创意，并查看结果。 直接在画布中插入级别：

1. 在要插入级别的边界处，单击&#x200B;**[!UICONTROL Add targeting level]**。

   在水平视图中，此控件是一个具有相同标签的图标。

1. 在&#x200B;**[!UICONTROL New targeting level]**&#x200B;中选择目标类别，然后单击&#x200B;**[!UICONTROL Add targeting level]**。

   * 对于受众目标，请选择&#x200B;**[!UICONTROL Audience]**。

   * 对于地理目标，请选择单个地理类别（如&#x200B;**[!UICONTROL Geo: Country]**）。

   * 对于数据传递目标，请选择&#x200B;**[!UICONTROL Data Pass]**。

   * 要重新定位像素目标，请选择&#x200B;**[!UICONTROL RT Pixel]**。

   * 对于设备目标，请选择单个目标类别（**[!UICONTROL Device: Type]**、**[!UICONTROL Device: OS]**&#x200B;或&#x200B;**[!UICONTROL Device: Browser]**）。

   插入级别不会提示输入目标值。 新级别最初使用“全部”并保留现有的子目标和创意。

1. （可选）要在新级别定义特定目标，请[添加同级目标节点](experience-target-node-add-sibling.md#ai-editor)。 否则，请保留新的“全部”节点，而不添加特定目标。

1. （可选）要重命名用户定义的目标节点，请单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Name]**，输入&#x200B;**[!UICONTROL Node Name]**，然后单击&#x200B;**[!UICONTROL Save]**。

   无法重命名“全部”或“其他各项”节点。

1. 查看保留的分支，并[将创意包](experience-assign-creative-bundles.md#ai-editor)分配给任何新的最终节点。

1. [保存体验](#save)。

## 使用手动编辑器 {#manual-editor}

[在执行以下步骤之前，请打开手动编辑器](experience-edit-targeting.md#experience-open)。

1. 在要插入目标的节点下，单击![添加](/help/creative/assets/add.png "添加")，然后选择&#x200B;**[!UICONTROL Insert New Target]**。

1. 执行以下操作之一：

   * 如果同级节点尚不存在，请执行以下操作：

     1. 选择目标类型，然后单击&#x200B;**[!UICONTROL Apply]**：

        * 对于受众目标，请选择&#x200B;**[!UICONTROL Audience]**。

        * 对于地理目标，请选择单个地理类别（如&#x200B;**[!UICONTROL Geo: Country]**）。

        * 对于数据传递目标，请选择&#x200B;**[!UICONTROL Data Pass]**。

        * 要重新定位像素目标，请选择&#x200B;**[!UICONTROL RT Pixel]**。

        * 对于设备目标，请选择单个目标类别（**[!UICONTROL Device: Type]**、**[!UICONTROL Device: OS]**&#x200B;或&#x200B;**[!UICONTROL Device: Browser]**）。

   * 如果同级节点已存在，请执行以下操作：

     * 对于受众目标：

       1. 单击&#x200B;**[!UICONTROL Click to Browse]**&#x200B;以打开&#x200B;**[!UICONTROL Audience Targeting]**&#x200B;选项。

       1. 配置受众区段和组：

          * 要添加第一个区段，请在左侧面板中查找该区段，然后选中区段名称旁边的复选框。

          * 要将区段添加到现有区段组，请执行以下操作：

            1. 单击右侧面板中的区段组。

            1. （可选）根据需要将组逻辑更改为&#x200B;**[!UICONTROL Include Any]**、**[!UICONTROL Include All]**&#x200B;或&#x200B;**[!UICONTROL Exclude All]**。

               **[!UICONTROL Include Any]**&#x200B;与至少一个选定区段中的用户匹配；**[!UICONTROL Include All]**&#x200B;需要所有选定区段中的成员资格。

               **[!UICONTROL Exclude All]**&#x200B;不可用于第一个区段组。 对于仅包含排除项的受众，使用&#x200B;**[!UICONTROL Include Any]**&#x200B;构建该受众，然后在将该受众添加到DSP中的版面时将其排除。

            1. 在左侧面板中找到新区段，然后选中区段名称旁边的复选框。 对每个其他区段重复执行上述步骤。

               区段组会自动更新为新区段。

          * 要添加新区段组，请执行以下操作：

            1. 单击右侧面板中的&#x200B;**[!UICONTROL + New Group]**。

            1. （可选）根据需要将上一个组与新组之间的逻辑更改为&#x200B;**[!UICONTROL And]**&#x200B;或&#x200B;**[!UICONTROL Or]**。

               **[!UICONTROL And]**&#x200B;要求用户满足两个组的条件；**[!UICONTROL Or]**&#x200B;要求用户满足至少一个组的条件。

            1. 在左侧面板中找到新组的区段，并选中区段名称旁边的复选框。

            1. （可选）根据需要将组逻辑更改为&#x200B;**[!UICONTROL Include Any]**、**[!UICONTROL Include All]**&#x200B;或&#x200B;**[!UICONTROL Exclude All]**。

       1. 单击&#x200B;**[!UICONTROL Create]**。

       1. 单击&#x200B;**[!UICONTROL Apply]**。

     * 对于地理目标，请执行以下操作：

       1. 单击&#x200B;**[!UICONTROL Click to Browse]**&#x200B;以打开您的[!UICONTROL Geo Targeting]选项，指定一个或多个地理目标，然后单击&#x200B;**[!UICONTROL Save]**。

          邮政编码目标具有批量编辑选项。 要粘贴多个邮政编码，请单击&#x200B;**[!UICONTROL Paste postal codes]**&#x200B;选项卡，选择国家/地区，粘贴或输入以逗号分隔的邮政编码或输入单独的行，然后单击&#x200B;**[!UICONTROL Include All]**。 要删除包含的邮政编码目标，请将光标悬停在目标上，然后单击![删除](/help/creative/assets/delete.png "删除") **[!UICONTROL Remove]**。

       1. （可选）要在指定多个地理目标时创建多个目标节点，请选择&#x200B;**[!UICONTROL Split targets to create nodes]**。

          此功能为每个指定的地理目标创建一个单独的目标节点（具有单独的创意包）。 如果不拆分目标，则用户必须属于所有指定的位置（[!DNL Boolean] `AND`语句）。

       1. 单击&#x200B;**[!UICONTROL Apply]**。

     * 对于数据传递目标，可以选择自定义数据传递密钥，输入单个数据传递值，然后单击&#x200B;**[!UICONTROL Apply]**。

       默认数据传递密钥在[常规体验设置](experience-settings-targeting.md)的&#x200B;**[!UICONTROL Advanced]**&#x200B;部分的&#x200B;**[!UICONTROL Data Pass]**&#x200B;字段中配置。 如果需要，可自定义目标的键。

     * 对于重定位像素目标，请选择要使用的单个重定位像素以及显示创意所需的任何像素属性的值，然后单击&#x200B;**[!UICONTROL Apply]**。

       可用的属性在[重定位像素设置](/help/creative/pixels/retargeting-pixel-manage.md)中配置。

     * 对于设备目标，请执行以下操作：

       1. 选择目标。

       1. （可选）要在指定多个地理目标时创建多个目标节点，请选择&#x200B;**[!UICONTROL Split targets to create nodes]**。

          此功能为每个指定的地理目标创建一个单独的目标节点（具有单独的创意包）。 如果不拆分目标，则用户必须属于所有指定的位置（[!DNL Boolean] `AND`语句）。

       1. （可选）要在指定多个地理目标时创建多个目标节点，请选择&#x200B;**[!UICONTROL Split targets to create nodes]**。

       1. 单击&#x200B;**[!UICONTROL Apply]**。

1. （可选）为用户定义的分支指定自定义分支名称。

   默认情况下，用户定义的分支使用应用的目标进行标记。

   您无法为“全部”或“其他所有人”分支创建自定义分支名称。

   1. 将光标悬停在目标节点上并单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Name]**。

   1. 输入&#x200B;**[!UICONTROL Node Name]**，然后单击&#x200B;**[!UICONTROL Save]**。

1. （可选） [将创意包](experience-assign-creative-bundles.md#manual-editor)分配给新目标节点和“其他所有内容”节点。

1. （可选） [添加指定目标类型的同级目标节点](experience-target-node-add-sibling.md#manual-editor)。

## 保存体验 {#save}

以下步骤适用于两个编辑器。

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [将目标节点添加到最终级别](experience-target-node-add-final.md)
>* [在节点之间添加同级目标节点](experience-target-node-add-sibling.md)
>* [将子节点和创意复制到同一级别的其他节点](experience-target-node-copy.md)
>* [将创意内容分配给最终节点](experience-assign-creative-bundles.md)
>* [删除目标节点或创意叶节点](/help/creative/experiences/experience-target-node-delete.md)
>* [使用决策树定位创建体验](experience-create-targeting.md)
>* [使用决策树定位编辑体验](experience-edit-targeting.md)
>* [目标体验设置](experience-settings-targeting.md)
