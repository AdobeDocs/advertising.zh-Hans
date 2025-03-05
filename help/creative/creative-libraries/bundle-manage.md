---
title: 管理创意包
description: 了解xxxx。
feature: Creative Bundles
exl-id: a9ed4e8f-db93-46d5-9231-2b3bb0aa072a
source-git-commit: 97e0f562153983202a2f3641e17dd682ff3d00ea
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 0%

---

# 管理创意包

*已关闭的测试版*

<!--
**I'll probably split this up into multiple pages since the creative-related topics are separate**
-->

捆绑包是您可以将多个创意内容作为一个单元添加到体验中的组合。 创建捆绑包容器后，可以将创意附加到该捆绑包。 标准包只能包含标准广告，而动态包只能包含动态广告。 您可以覆盖捆绑包中所有创意的登陆页面、展示跟踪标记和点击跟踪标记，这些捆绑包是从体验决策树中分配给体验的，不会影响基本创意内容。

[!DNL Creative]按照为捆绑包所分配到的每个体验指定的方式，在捆绑包中的创意之间旋转。 您可以选择允许[!DNL Creative]使用算法广告轮换(由Adobe Sensei提供支持)根据性能优化任何体验的广告元素。

要优化广告体验中各个包的广告元素，每个包只能包含每个\[创意大小+语言\]组合中的一个。 例如，如果一个捆绑包中包含一个默认语言为“法语”的250x250创意内容，那么您将无法添加另一个默认语言为“法语”的250x250创意内容。 如果您有具有相同语言的多个相同大小的创意，请单独将它们添加到体验中。

附加到捆绑的创意仍以单个创意的形式提供。 您可以将单个创意内容添加到多个捆绑包。 如果编辑附加到捆绑包的创意内容的任何设置，则这些更改将传播到捆绑包中。 但是，始终将体验用于为体验中的创意配置的任何自定义登陆页面、展示跟踪标记和点击跟踪标记。

<!-- multiselect only to duplicate and delete -->

## 为创意库创建捆绑包

您可以将创意内容附加到多个捆绑包中。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 单击库名称。

1. 单击&#x200B;**[!UICONTROL Bundles]**&#x200B;选项卡。

1. 单击右上角的&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Bundles]** > **[!UICONTROL Bundle]**。

1. 输入唯一的&#x200B;**[!UICONTROL Bundle Name]**&#x200B;和&#x200B;**[!UICONTROL Bundle Type]：** *标准*（对于标准创意）或&#x200B;*动态*（对于动态创意）。

1. 单击&#x200B;**[!UICONTROL Create]**。

## 在捆绑销售中列出创意内容

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. （可选） [自定义视图](/help/creative/introduction/customize-data-views.md)以包含特定库。

1. 单击库名称。

1. 单击&#x200B;**[!UICONTROL Bundles]**&#x200B;选项卡。

1. 单击束卡或行可查看束中的所有创意。

## 复制包

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. （可选） [自定义视图](/help/creative/introduction/customize-data-views.md)以包含特定库。

1. 单击库名称。

1. 单击&#x200B;**[!UICONTROL Bundles]**&#x200B;选项卡。

1. 选择要复制的包：

   * 要复制单个捆绑包，请执行以下操作：

      * 在卡片视图中，单击包名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Duplicate]**。

      * 在表视图中，将光标悬停在行上并单击&#x200B;**[!UICONTROL Duplicate]**。

   * 要复制一个或多个包，请选中要复制的每个包的复选框。 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Duplicate].**

     要选择所有行，请选中左上角的全局复选框。

   新包名为`<original name> (copy) # 1`（或序列中的下一个编号）。 例如，如果您为“测试包”创建两个副本，则这些副本将分别命名为“测试包（副本） # 1”和“测试包（副本） # 2”。

## 编辑包名称

对捆绑包名称所做的更改会传播到所有关联的体验中。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 单击库名称。

1. 单击&#x200B;**[!UICONTROL Bundles]**&#x200B;选项卡。

1. 选择包：

   * 在卡片视图中，单击库名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Edit]**。

   * 在表视图中，将光标悬停在行上并单击&#x200B;**[!UICONTROL Edit]**。

1. 编辑&#x200B;**[!UICONTROL Bundle Name]**。

   [!UICONTROL Bundle Name]必须是唯一的。

1. 单击&#x200B;**[!UICONTROL Update]**.<!-- inconsistent with "Edit" for creative libraries and creatives -->

## 将创意内容附加到捆绑包

您可以将[现有的标准创意](/help/creative/creative-libraries/creative-libraries-about.md)附加到标准捆绑包并将现有的动态创意<!-- [existing dynamic creatives](creative-dynamic-manage.md) -->附加到动态捆绑包。 将创意内容附加到捆绑包后，创意内容便可在捆绑包所分配到的所有体验中可用。 每个包只能包含每个\[创意大小+语言\]组合中的一个。

<!--
>[!NOTE]
>
>You can also [attach creatives to bundles from the Standard Ads and Dynamic Ads views](creative-attach-detach-bundles.md).
-->

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. （可选） [自定义视图](/help/creative/introduction/customize-data-views.md)以包含特定库。

1. 单击库名称。

1. 单击&#x200B;**[!UICONTROL Bundles]**&#x200B;选项卡。

1. 选择包：

   * 在卡片视图中，单击包名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Attach Creatives]**。

   * 在表视图中，将光标悬停在行上并单击&#x200B;**[!UICONTROL Attach Creatives]**。

   符合该捆绑包类型的每个创意内容都列在右框架中。 已附加到该捆绑包的创意已列出，但不可选择。

1. 在右框中，选中要附加到捆绑包的每个创意内容旁边的复选框，然后单击&#x200B;**[!UICONTROL Attach Creative to Bundle]**。

## 将创意内容从捆绑包中分离 {#bundle-detach-creatives}

将创意内容从捆绑包分离会删除两者之间的关联，以便该创意内容不再用于针对捆绑包的体验。

从捆绑包中分离创意时不会从创意库中的“创意”选项卡中删除该创意。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. （可选） [自定义视图](/help/creative/introduction/customize-data-views.md)以包含特定库。

1. 单击库名称。

1. 单击&#x200B;**[!UICONTROL Bundles]**&#x200B;选项卡。

1. 单击束卡或行可查看束中的所有创意。

1. 选择要从捆绑中分离的创意：

   * 要分离单个创意，请执行以下操作：

      * 在卡片视图中，单击创意名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Detach]**。

      * 在表视图中，将光标悬停在行上并单击&#x200B;**[!UICONTROL Detach]**。

   * 要分离一个或多个创意，请选中要分离的每个创意所对应的复选框。 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Detach]**。

     要选择所有行，请选中左上角的全局复选框。

## 预览捆绑包中的创意

您可以在查看者看到创意时预览它，包括超链接。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. （可选） [自定义视图](/help/creative/introduction/customize-data-views.md)以包含特定库。

1. 单击库名称。

1. 单击&#x200B;**[!UICONTROL Bundles]**&#x200B;选项卡。

1. 单击束卡或行可查看束中的所有创意。

1. 选择创意内容：

   * 在卡片视图中，单击创意名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Preview]**。

   * 在表视图中，将光标悬停在行上并单击&#x200B;**[!UICONTROL Preview]**。

1. （可选）要调整屏幕中图像的大小，请在&#x200B;**[!UICONTROL Zoom]**&#x200B;列表中选择一个选项，其范围为图像大小的10%到100%。

<!-- Not there as of 1/22/24:  1. (Flexible HTML5 creatives; optional) To show all frames for the creative, select **Show frames**. -->

1. （可选）要下载创意，请单击![下载](/help/creative/assets/download.png "下载")。

   将按照浏览器的正常过程下载文件。


<!-- Not there as of 1/22/25:

## Edit the landing page and tracking tags for the creatives in a standard creative bundle

*Standard creative bundles only*

[Verify and edit all this, including the command names and where they're available. This is supposed to be a single and bulk action from within the right frame when you've open bundle details for a single bundle -- not from the Bundles table view.]

This procedure customizes the landing page, impression-tracking tags, and click-tracking tags for the creatives only within the context of the bundle. It doesn't change the settings for the base creative in [!UICONTROL Creative Libraries].

The custom URL and tags are applied to a creative when the bundle is assigned to an experience and the creative is served for the experience.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Click the bundle name.

1. In the right pane, XXXXXXXXXXXX.

1. 

1. Edit any of the following settings: **[!UICONTROL Landing Page]**, **[!UICONTROL Click Tags]**, **[!UICONTROL Impression Tags]**.[Verify, and is can you do this for only one creative or is multiselect available?]

1.

 -->

## 删除包

您可以删除未分配给[实时](/help/creative/experiences/experience-about.md#experience-statuses-experience-statuses)体验的包。 如果将捆绑包分配给实时体验，则在继续之前[从决策树](/help/creative/experiences/experience-target-node-delete.md)中删除该捆绑包以供该体验使用。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. （可选） [自定义视图](/help/creative/introduction/customize-data-views.md)以包含特定库。

1. 单击库名称。

1. 单击&#x200B;**[!UICONTROL Bundles]**&#x200B;选项卡。

1. 选择要删除的包：

   * 要删除单个捆绑包，请执行以下操作：

      * 在卡片视图中，单击包名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Delete]**。

      * 在表视图中，将光标悬停在行上并单击&#x200B;**[!UICONTROL Delete]**。

   * 要删除一个或多个包，请选中要删除的每个包的复选框。 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Delete].**

     要选择所有行，请选中左上角的全局复选框。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Delete].**

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [向体验中的最终节点分配和取消分配创意包](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [将标准创意添加到创意库](/help/creative/creative-libraries/creative-add-standard.md)
>* [管理创意库](/help/creative/creative-libraries/creative-library-manage.md)
>* [关于您的创意库](/help/creative/creative-libraries/creative-libraries-about.md)
