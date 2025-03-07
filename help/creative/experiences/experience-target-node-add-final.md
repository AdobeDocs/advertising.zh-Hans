---
title: 将目标节点添加到体验中的最终级别
description: 了解如何将目标节点添加到广告体验的最终目标级别。
feature: Creative Experiences
exl-id: 3ff657d5-bad1-47f4-a3ec-9ea678fd3c9d
source-git-commit: 5d8b511708008c77e817ccdb00ae02c158dfe63e
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# 将目标节点添加到体验中的最终级别

*仅具有决策树定位的体验*
*已关闭的测试版*

当您将目标节点添加到体验的最底层时 — 无论是根“所有”节点、特定于目标的节点还是“其他所有内容”节点 — 您都可以直接定义目标，而无需创建同级节点。 添加底层节点会在同一级别创建目标节点和其他“其他所有内容”节点。

>[!NOTE]
>
>要在决策树的现有级别之间插入目标节点，请参阅“[在体验中的节点之间插入目标节点](experience-target-node-add-inner.md)”。

<!-- 1. [ways to get to the decision tree] -->

1. 在要插入目标的节点下，单击![添加](/help/creative/assets/add.png "添加")，然后选择&#x200B;**[!UICONTROL Insert New Target]**。

1. 指定目标：

   * 对于Adobe受众目标，请选择&#x200B;**[!UICONTROL Adobe Audience]**，然后执行以下操作：

      1. 单击&#x200B;**[!UICONTROL Click to Browse]**&#x200B;以打开您的[!UICONTROL Audience Targeting]选项，打开&#x200B;**[!UICONTROL Adobe Segments]**&#x200B;选项卡，指定广告商的一个或多个[!DNL Adobe]受众目标，然后单击&#x200B;**[!UICONTROL Create]**。

      1. （可选）要在指定多个受众时创建多个目标节点，请选择&#x200B;**[!UICONTROL Split targets to create nodes]**。

         此功能为每个指定的受众创建一个单独的目标节点（具有单独的创意包）。 如果不拆分目标，则用户必须属于所有指定的受众。

      1. 单击&#x200B;**[!UICONTROL Apply]**。

   * 对于地理目标，请选择单个地理类别（如[!UICONTROL Geo: Country]），然后执行以下操作：

      1. 单击&#x200B;**[!UICONTROL Click to Browse]**&#x200B;以打开您的[!UICONTROL Geo Targeting]选项，指定一个或多个地理目标，然后单击&#x200B;**[!UICONTROL Save]**。

         邮政编码目标具有批量编辑选项。 要粘贴多个邮政编码，请单击&#x200B;**[!UICONTROL Paste postal codes]**&#x200B;选项卡，选择国家/地区，粘贴或输入以逗号分隔的邮政编码或输入单独的行，然后单击&#x200B;**[!UICONTROL Include All]**。 要删除包含的邮政编码目标，请将光标悬停在目标上，然后单击![删除](/help/creative/assets/delete.png "删除") **[!UICONTROL Remove]**。

      1. （可选）要在指定多个地理目标时创建多个目标节点，请选择&#x200B;**[!UICONTROL Split targets to create nodes]**。

         此功能为每个指定的地理目标创建一个单独的目标节点（具有单独的创意包）。 如果不拆分目标，则用户必须属于所有指定位置。

      1. 单击&#x200B;**[!UICONTROL Apply]**。

   * 对于数据传递目标，请选择&#x200B;**[!UICONTROL Data Pass]**，输入单个数据传递值，然后单击&#x200B;**[!UICONTROL Apply]**。

   已在[体验设置](experience-settings-targeting.md)的[!UICONTROL Advanced]部分的&#x200B;**[!UICONTROL Data Pass]**&#x200B;字段中设置了键值对的键。

   * 对于重定位像素目标，请选择&#x200B;**[!UICONTROL RT Pixel]**，选择要使用的单个重定位像素以及显示创意所需的任何像素属性的值，然后单击&#x200B;**[!UICONTROL Apply]**。

     在[重定位像素设置](/help/creative/pixels/retargeting-pixel-manage.md)中配置了重定位像素的属性。

   * 对于设备目标，请执行以下操作：

      1. 选择单个目标类别（**[!UICONTROL Device: Type]**、**[!UICONTROL Device: OS]**&#x200B;或&#x200B;**[!UICONTROL Device: Browser]**），然后选择目标。

      1. （可选）要在指定多个地理目标时创建多个目标节点，请选择&#x200B;**[!UICONTROL Split targets to create nodes]**。

         此功能为每个指定的地理目标创建一个单独的目标节点（具有单独的创意包）。 如果不拆分目标，则用户必须属于所有指定位置。

      1. 单击&#x200B;**[!UICONTROL Apply]**。

1. 执行以下任一操作：

   * （可选） [将创意内容](experience-assign-creative-bundles.md)分配给新目标节点和“其他所有内容”节点。

   * （可选）要保存体验，请执行以下操作：

      1. 单击&#x200B;**[!UICONTROL Save]**，然后单击&#x200B;**[!UICONTROL OK]**。

      1. （如果最底层的每个节点至少不包含一个创意内容）：执行以下操作之一：

         * 要在没有所有必需创意捆绑包的情况下保存体验，请单击&#x200B;**[!UICONTROL Save as Draft]**。

           无法为草稿体验创建广告标记。

         * 要将默认创意分配给每个尚未分配创意捆绑包的目标，请单击&#x200B;**[!UICONTROL Assign Default Creatives]**。 在查看已分配默认创意的更新树后，单击&#x200B;**[!UICONTROL Save]**&#x200B;和&#x200B;**[!UICONTROL OK]**。

         * 要继续编辑决策树，请单击&#x200B;**[!UICONTROL Continue Edit]**。

>[!MORELIKETHIS]
>
>* [在节点之间插入目标节点](experience-target-node-add-inner.md)
>* [在节点之间添加同级目标节点](experience-target-node-add-sibling.md)
>* [将子节点和创意复制到同一级别的其他节点](experience-target-node-copy.md)
>* [将创意内容分配给最终节点](experience-assign-creative-bundles.md)
>* [删除目标节点或创意叶节点](/help/creative/experiences/experience-target-node-delete.md)
>* [使用决策树定位创建体验](experience-create-targeting.md)
>* [使用决策树定位编辑体验](experience-edit-targeting.md)
>* [目标体验设置](experience-settings-targeting.md)
