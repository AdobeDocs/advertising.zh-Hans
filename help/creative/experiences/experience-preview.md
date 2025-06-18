---
title: 预览体验
description: 了解如何在广告体验中预览创意内容。
feature: Creative Experiences
exl-id: 2ac8f580-7d3d-4de6-ba14-5d72b30188d7
source-git-commit: ae226015d1a8a3da4ea2a0db0db31858e750b9a7
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# 预览体验

*已关闭的测试版*

您可以预览具有特定广告大小的创意，目标查看者将看到该广告大小的体验，包括所有超链接。 对于具有决策树定位的体验，您可以预览单个创意内容、特定分支的创意内容（目标类型）或体验中的所有创意内容。 对于没有决策树定位的体验，您可以预览单个创意内容。<!-- verify -->

* 预览体验或特定分支的所有创意时，将显示所有适用的创意。

* 当您预览单个创意且多个创意符合条件时，您每次刷新预览时看到的创意将基于体验的广告轮换设置：

   * 对于算法广告轮换，根据优化目标选择创意。

   * 对于加权广告轮换，每次都根据指定的权重(例如，显示Creative A的概率为80%，显示Creative B的概率为20%)来选择创意。

   * 对于计划的广告轮换，将显示计划中的第一个创意内容。 您可以继续刷新预览以继续完成序列。<!-- Refresh isn't there as of 2/3 -->

## 使用决策树定位预览体验中的创意

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. （可选）[自定义视图](/help/creative/introduction/customize-data-views.md)以包含特定体验。

1. 执行以下操作之一：

   * 在卡片视图中，单击体验名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Preview]**。

   * 在表格视图中，将光标悬停在行上，单击&#x200B;**[!UICONTROL More]**，然后单击&#x200B;**[!UICONTROL Preview]**。

1. 选择要预览的创意：

   * 要预览单个创意，请执行以下操作：

      1. 单击&#x200B;**[!UICONTROL Creative]**。

      1. 选择广告大小。

      1. 在[!UICONTROL Decision Tree Targeting]部分中，选择创意目标。

   * 要预览特定分支的创意，请执行以下操作：

      1. 单击&#x200B;**[!UICONTROL Particular branch]**。

      1. 选择广告大小。

     <!-- I don't see this as of 2/3:
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

      1. 选择创意目标。

   * 要预览体验中的所有创意内容，请单击&#x200B;**[!UICONTROL Entire Tree]**。

     <!-- I don't see this as of 2/3:
     1. Click **[!UICONTROL Entire Tree]**.
     1. Select the ad size.
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

1. （可选）要包含创意的名称、创意类型和大小、登陆页面URL或单击URL以及每个创意下面的灵活属性，请选择&#x200B;**[!UICONTROL Display Creative Metadata]**。

1. 单击&#x200B;**[!UICONTROL Preview]**。

1. （仅按创意内容预览；可选）在工具栏中，单击&#x200B;**[!UICONTROL Refresh]**&#x200B;以根据广告轮转设置预览任何可能显示的其他创意内容。<!-- I don't see this as of 2/3 -->

1. （可选）要复制体验的演示URL以与未登录[!DNL Creative]的其他人共享，请执行以下操作：

   1. 单击预览右上角的![共享](/help/creative/assets/share.png "共享")。

   1. 在[!UICONTROL Share Demo URL]对话框中，单击&#x200B;**[!UICONTROL Copy]**&#x200B;以将URL复制到剪贴板，以便与其他人共享。

## 在没有决策树定位的情况下预览体验中的创意

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. （可选）[自定义视图](/help/creative/introduction/customize-data-views.md)以包含特定体验。

1. 执行以下操作之一：

   * 在卡片视图中，单击体验名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Preview]**。

   * 在表格视图中，将光标悬停在行上，单击&#x200B;**[!UICONTROL More]**，然后单击&#x200B;**[!UICONTROL Preview]**。

1. （可选）通过选择特定的创意大小来限制创意内容列表。

   默认情况下，将列出所有大小的创意。

1. 单击广告标记的名称，可展开行并预览创意。

1. （可选）要转至创意的登陆页面，请单击该创意内容。

   <!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. （可选）要复制体验的演示URL以与未登录[!DNL Creative]的其他人共享，请执行以下操作：

   1. 单击预览右上角的![共享](/help/creative/assets/share.png "共享")。

   1. 在[!UICONTROL Share Demo URL]对话框中，单击&#x200B;**[!UICONTROL Copy]**&#x200B;以将URL复制到剪贴板，以便与其他人共享。

>[!MORELIKETHIS]
>
>* [使用决策树定位创建体验](experience-create-targeting.md)
>* [创建没有决策树定位的体验](/help/creative/experiences/experience-create-no-targeting.md)
