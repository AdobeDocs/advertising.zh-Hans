---
title: 自定义体验的跟踪URL
description: 了解如何使用决策树定位自定义体验中每个创意内容的跟踪URL。
feature: Creative Experiences
exl-id: ba3b15b4-116e-4caa-8ce1-4d2e488a6362
TQID: 'https://experienceleague.adobe.com/LjeF7eYU8V93W28VbV-D6NNWWwdKqywOP2BwzDwQAgo'
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
source-wordcount: '448'
ht-degree: 0%
---
# 通过决策树定位自定义体验中创意人员的跟踪URL

*仅定位具有现有创意的节点*

对于具有决策树定位的体验，您最多可以为用于体验的每个创意创建五个自定义展示跟踪URL和五个自定义点击跟踪URL。 当登陆页面覆盖可用时，您还可以指定一个自定义登陆页面URL。 您可以从任一决策树编辑器中自定义跟踪URL。

自定义URL仅用于根据体验创建的广告，不会保存在[!UICONTROL Creative Libraries]的基本创意设置中。

登陆页面覆盖适用于标准体验和使用默认创意的节点。 对于分配的动态包，登陆页面由馈送确定，并且不显示登陆页面选项卡。

## 使用AI驱动编辑器(Beta) {#ai-editor}

当您[创建](experience-create-targeting.md#ai-editor)或[编辑](experience-edit-targeting.md#ai-editor)体验时，请使用画布控件：

1. 在目标节点下的创意叶节点上，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Tracking URLs]**。

1. 选择&#x200B;**[!UICONTROL Click Tracking URLs]**、**[!UICONTROL Impression Tracking URLs]**&#x200B;或（可用时）**[!UICONTROL Landing URL]**&#x200B;选项卡。

   创意按捆绑分组。 体验的默认创意大小决定可用的创意大小。

1. 展开要编辑的创意内容，然后执行以下任一操作：

   * 要添加或编辑自定义URL，请在输入字段中输入URL。

   * 要添加另一个自定义跟踪URL，请单击&#x200B;**[!UICONTROL Add URL]**，然后在输入字段中输入该URL。

   * 要删除自定义URL，请单击&#x200B;**[!UICONTROL Delete URL]**。

   单击已编辑字段的外部，并在保存之前更正任何验证错误。

1. 在对话框中单击&#x200B;**[!UICONTROL Save]**&#x200B;以更新工作树。

1. 从树标头[保存体验](#save)。

## 使用手动编辑器 {#manual-editor}

[在执行以下步骤之前，请打开手动编辑器](experience-edit-targeting.md#experience-open)。

1. 在目标节点下的创意叶节点上，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Tracking URLs]**。

1. 选择&#x200B;**[!UICONTROL Click Tracking URLs]**、**[!UICONTROL Impression Tracking URLs]**&#x200B;或（可用时）**[!UICONTROL Landing URLs]**&#x200B;选项卡。

   选项卡列出所分配捆绑包中的创意。 体验的默认创意大小决定可用的创意大小。<!-- There's no distinct "Creative Sizes" setting. -->

1. 展开要编辑的创意内容，然后执行以下任一操作：

   * 要添加或编辑自定义URL，请在输入字段中输入URL。

   * 要添加另一个自定义跟踪URL，请单击&#x200B;**[!UICONTROL +]**，然后在输入字段中输入该URL。

   * 要删除自定义URL，请将光标悬停在创作行上，然后单击![删除](/help/creative/assets/delete.png "删除")。

1. 在对话框中单击&#x200B;**[!UICONTROL Save]**&#x200B;以更新工作树。

1. 从树标头[保存体验](#save)。

## 保存体验 {#save}

以下步骤适用于两个编辑器。 仅保存跟踪URL对话框不会保存或发布体验。

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [向体验中的最终节点分配和取消分配创意包](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [自定义没有决策树定位的体验的跟踪URL](experience-tracking-urls-no-targeting.md)
