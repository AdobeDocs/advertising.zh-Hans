---
title: 将子节点复制到同一级别的其他目标节点
description: 了解如何将父目标节点的所有子节点复制到同一级别的其他目标节点
feature: Creative Experiences
exl-id: b3705689-57b6-41ce-9e00-2358bd195c93
TQID: 'https://experienceleague.adobe.com/KLKVrggOQ8V99Cd-2PcFEdwImKvLYkskSD-DPDvpwu0'
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
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%
---
# 将子节点复制到同一级别的其他目标节点

*仅具有决策树定位的体验*

您可以将父目标节点的所有子节点（包括所有子目标和分配给它们的创意捆绑包）复制到同一级别的其他目标节点。 您可以通过a)将复制的节点添加到现有框架或b)完全替换现有框架来复制节点。<!-- Give the main use case or an example to explain. -->

此功能不会影响为父节点指定的目标 — 它只影响子节点。

## 使用AI驱动编辑器(Beta) {#ai-editor}

当您[创建](experience-create-targeting.md#ai-editor)或[编辑](experience-edit-targeting.md#ai-editor)体验时，请使用画布控件：

1. 在要复制其子节点的父节点上单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Copy Children]**。

1. 在同一级别的目标节点上，单击&#x200B;**[!UICONTROL ...]**，然后选择下列选项之一：

   * 若要在不删除现有子项的情况下添加复制的子目标和创意，请单击&#x200B;**[!UICONTROL Add]**。

   * 要将现有的子目标和创意替换为复制的子项，请单击&#x200B;**[!UICONTROL Replace]**。

   如果树结构不支持某个操作，则会禁用该操作。 在继续之前查看任何警告。

1. 查看目标分支，然后[保存体验](#save)。

## 使用手动编辑器 {#manual-editor}

[在执行以下步骤之前，请打开手动编辑器](experience-edit-targeting.md#experience-open)。

1. 单击要复制其子节点的父节点，单击![添加](/help/creative/assets/add.png "添加")，然后a\)选择&#x200B;**[!UICONTROL Copy Children ctrl+c]**&#x200B;或b\)在键盘上输入&#x200B;**[!UICONTROL Ctrl+C]** ([!DNL Microsoft Windows])或&#x200B;**[!UICONTROL Command-C]** ([!DNL Apple Macintosh])。

1. 执行以下任一操作：

   * 要替换节点的所有子节点和创意，请单击要向其粘贴复制信息的节点，单击&#x200B;**[!UICONTROL ...]**，然后a\)选择&#x200B;**[!UICONTROL Replace ctrl+shift+v]**&#x200B;或b\)在键盘上输入&#x200B;**[!UICONTROL Ctrl+Shift+V]** ([!DNL Microsoft Windows])或&#x200B;**[!UICONTROL Command-Shift-V]** ([!DNL Apple Macintosh])。

   * （具有多个子目标的节点，没有“所有”节点，仅没有创意）要将所有子节点和创意添加到节点而不删除现有节点，请单击要向其粘贴复制信息的节点，单击&#x200B;**[!UICONTROL ...]**，然后a\)选择&#x200B;**[!UICONTROL Add ctrl+v]**&#x200B;或b\)在键盘上输入&#x200B;**[!UICONTROL Ctrl+V]** ([!DNL Microsoft Windows])或&#x200B;**[!UICONTROL Command-V]** ([!DNL Apple Macintosh])。

## 保存体验 {#save}

以下步骤适用于两个编辑器。

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [将目标节点添加到最终级别](experience-target-node-add-final.md)
>* [在节点之间插入目标节点](experience-target-node-add-inner.md)
>* [在节点之间添加同级目标节点](experience-target-node-add-sibling.md)
>* [将创意内容分配给最终节点](experience-assign-creative-bundles.md)
>* [删除目标节点或创意叶节点](/help/creative/experiences/experience-target-node-delete.md)
>* [使用决策树定位创建体验](experience-create-targeting.md)
>* [使用决策树定位编辑体验](experience-edit-targeting.md)
>* [目标体验设置](experience-settings-targeting.md)
