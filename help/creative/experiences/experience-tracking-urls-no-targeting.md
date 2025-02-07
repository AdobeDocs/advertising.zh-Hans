---
title: 自定义体验的跟踪URL，而无需定位
description: 了解如何在不使用决策树定位的情况下自定义体验中每个创意内容的跟踪URL。
feature: Creative Experiences
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 0%

---

# 自定义体验的跟踪URL，而无需决策树定位

*已关闭的测试版*

对于没有决策树定位的体验，您最多可以从[!UICONTROL Tag Manager]中为广告体验标记使用的每个创意创建五个自定义展示跟踪URL、五个自定义点击跟踪URL和一个自定义登陆页面URL。

自定义URL仅用于从广告体验标记创建的广告，不会保存在[!UICONTROL Creative Libraries]的基本创意设置中。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. 执行以下操作之一：

   * 在卡片视图中，单击体验名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Tag Manager]**。

   * 在表格视图中，将光标悬停在行上，单击&#x200B;**[!UICONTROL More]**，然后单击&#x200B;**[!UICONTROL Tag Manager]**

1. （如果广告大小的标记不存在）为适用的创意大小创建标记。

   您可以为体验使用的每个创意大小创建一个或多个标记。

   1. 单击右上角的&#x200B;**[!UICONTROL Create Tag]**。

   1. 输入唯一的&#x200B;**[!UICONTROL Tag name]**&#x200B;并选择&#x200B;**[!UICONTROL Tag size]**。

      可用大小由体验的默认图像创意的大小决定。

   1. 单击&#x200B;**[!UICONTROL Create]**。

1. 将光标悬停在适用的广告标记的行上，然后单击![编辑跟踪URL](/help/creative/assets/edit-gray.png "编辑跟踪URL") **[!UICONTROL Tracking URLs]**。 <!-- For targeted experiences, this is "EDIT Tracking URLs" -->&lt;！ — 从2/2开始，Tag Manager只有一个列表视图，但没有卡片视图。>

   [!UICONTROL Click Tracking URLs]、[!UICONTROL Impression Tracking URLs]和[!UICONTROL Landing URLs]选项卡在分配的捆绑包中列出了适用大小的所有创意的名称。 适用的大小由体验的默认图像创意的大小决定。<!-- There's no distinct "Creative Sizes" setting. -->

1. 在&#x200B;**[!UICONTROL Click Tracking URLs]**、**[!UICONTROL Impression Tracking URLs]**&#x200B;和&#x200B;**[!UICONTROL Landing URLs]**&#x200B;选项卡上，根据需要对每个创意执行以下操作：

   1. 展开创意内容所在的行。

   1. 执行以下任一操作：

      * 要添加或编辑自定义URL，请在输入字段中输入URL。

      * 要添加其他自定义URL，请单击&#x200B;**[!UICONTROL +]**&#x200B;并在输入字段中输入该URL。

      * 要删除自定义URL，请将光标悬停在创意行上，然后单击![删除](/help/creative/assets/delete.png "删除")。

      您最多可以包含5个自定义展示跟踪URL、5个自定义点击跟踪URL和1个自定义登陆页面URL。

1. 单击&#x200B;**[!UICONTROL Save]**。

>[!MORELIKETHIS]
>
>* [将创意内容分配给无定位体验的广告标记](experience-tag-assign-creatives.md)
>* [自定义具有决策树定位的体验的跟踪URL](experience-tracking-urls-targeting.md)
