---
title: 将广告附加到投放位置
description: 了解如何将广告附加到投放位置。
feature: DSP Ads
exl-id: bca590c9-e0d0-41e6-96b1-26ea5b2f842f
source-git-commit: 796af195bf935fa6ad9d83d9aa17931b9a640855
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# 将广告附加到投放位置

>[!NOTE]
>
>通用视频广告只能附加到通用视频投放位置。

## 从附加新广告 [!UICONTROL Ads] 视图

1. 在主菜单中，单击 **[!UICONTROL Campaigns]**.

1. 单击营销活动的名称。

1. 在子菜单中，单击 **[!UICONTROL Ads]**.

1. 在广告名称旁边，单击  **[!UICONTROL ...]** > **[!UICONTROL Add to Placements]**.

1. 在“置入广告”屏幕中，执行以下任一操作：

   * 要为广告创建新投放位置，请执行以下操作：

      1. 单击 **[!UICONTROL Create New Placement]**.

      1. 输入 [投放设置](/help/dsp/campaign-management/placements/placement-settings.md)，然后单击 **[!UICONTROL Create Placement]**.

   * 要将广告添加到一个或多个现有投放位置，请执行以下操作：

      1. 单击 **[!UICONTROL Select a Placement].**

      1. 执行以下任一操作：

         * 要一次添加一个广告，请执行以下操作：

            1. 在广告名称旁边，单击 **[!UICONTROL Select].**

            1. （可选）对于要附加的每个其他广告，单击 **[!UICONTROL Attach to Other Placement]**. 在广告名称旁边，单击 **[!UICONTROL Select].**

         * 要将广告一次附加到最多20个投放位置，请执行以下操作：

            1. 选中**批量选择”旁边的复选框。

            1. 选中每个要附加广告的投放位置旁边的复选框。

            1. 单击 **[!UICONTROL Attach]**.

      1. 在“完成和复查”选项卡上，选择下列选项之一：

         * 要返回广告视图，请单击 **[!UICONTROL I'm done for now]**.

         * 要将广告附加到其他投放位置，请单击 **[!UICONTROL Attach To Other Placement]**.

## 从附加新广告或现有广告 [!UICONTROL Placements] 视图

1. 在主菜单中，单击 **[!UICONTROL Campaigns]**.

1. 单击营销活动的名称。

1. 在子菜单中，单击 **[!UICONTROL Placements]**.

1. 在版面名称旁边，单击  **[!UICONTROL ...]** > **[!UICONTROL Attach Ads].**

1. 在 [!UICONTROL Add Ad to Placement] 屏幕，执行以下任一操作：

   * 要创建新广告：

      1. 单击 **[!UICONTROL Create a New Ad]**.

      1. 输入广告设置 [音频广告](ad-settings-audio.md)， [已连接电视](ad-settings-connected-tv.md)， [展示广告](ad-settings-display.md)， [移动广告](ad-settings-mobile.md)， [原生广告](ad-settings-native.md)，或 [前置广告](ad-settings-pre-roll.md).

      1. 单击 **[!UICONTROL Save & Submit for Review]**.

         此 [广告评论](ad-about.md) 对于新广告，需要24到48小时并包括敏感类别检查、单击URL功能和预览渲染。 此 [!UICONTROL Status] 列指示DSP是否已批准广告。 损坏的广告可能会有超过24-48小时的待处理状态，因此您有时间在错误被拒绝之前对其进行修复。

         >[!NOTE]
         >
         >只有当DSP和SSP都批准创意内容时，才会投放您的广告。 每个SSP都有自己的批准要求和流程。

   * 要选择现有广告，请执行以下操作：

      1. 单击 **[!UICONTROL Select an Ad].**

      1. 指定广告：

         * 要一次添加一个广告，请执行以下操作：

            1. 在广告名称旁边，单击 **[!UICONTROL Select].**

            1. （可选）对于要附加的每个其他广告，单击 **[!UICONTROL Add Another Ad]**. 在广告名称旁边，单击 **[!UICONTROL Select].**

         * 要一次最多添加20个广告，请执行以下操作：

            1. 选中旁边的复选框 **[!UICONTROL Bulk Select]**“

            1. 选中要添加的每个广告旁边的复选框。

            1. 单击 **[!UICONTROL Attach]**.

      1. （可选）要覆盖投放位置中特定广告的默认投放期限和广告轮换，请执行以下操作：

         1. 单击 **[!UICONTROL Custom Schedule Ads]**.

         1. 执行以下任一操作：

            * 要添加航班，请单击 **[!UICONTROL Add Flight]**，然后指定开始日期和结束日期。

            * 要将现有航班添加到广告，请单击 **[!UICONTROL +]** 在投放栏的广告行中。

            * 要从广告中删除现有航班，请单击 **[!UICONTROL x]** 在投放栏的广告行中。

            * （当多个广告具有相同投放时间时）要不均匀旋转广告，请单击 **[!UICONTROL Even Rotation]** 在飞行信息中，然后输入每个广告旋转的相对权重（百分比）。

              总重量必须等于100。

         1. 在右上角，单击 **[!UICONTROL Continue]**.

         1. 查看航班详细信息，然后单击 **[!UICONTROL Save & Finish]**.

      1. 单击 **[!UICONTROL I'm done for now]**.

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建单个广告](ad-create.md)
>* [创建多个第三方广告](ad-create-multiple.md)
>* [编辑广告](ad-edit.md)
>* [列出与广告关联的版面](ad-list-placements.md)
>* [编辑投放的广告计划](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [关于通用视频的常见问题解答](/help/dsp/campaign-management/faq-universal-video.md)
