---
title: 创建和实施自定义区段
description: 了解如何创建和实施自定义区段以跟踪向广告公开的用户或访问您网页的用户。
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: 67b59f4f066d25f323620b83b5a0cb49beb3ee04
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# 创建和实施自定义区段

您可以通过创建和实施自定义DSP区段来收集您自己的第一方受众数据。 您可以使用区段跟踪a)从桌面和移动设备向广告展示的用户以及b)访问特定网页的用户。 之后，您可以使用其他广告重新定位区段中的用户，或阻止区段中的用户接收其他广告。

>[!NOTE]
>
>要根据加州消费者隐私法案(CCPA)在网站上跟踪消费者选择退出销售请求的用户ID，请创建 [CCPA选择退出销售区段](ccpa-opt-out-segment-create.md).

1. 创建区段：

   1. 在主菜单中，单击 **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. 在数据表的上方，单击 **[!UICONTROL Create]**.

   1. 输入唯一值 **[!UICONTROL Segment Name]**.

   1. 对于 **[!UICONTROL Segment Type]**，选择 *[!UICONTROL Custom]*.

   1. 输入 **[!UICONTROL Segment Window]**，即用户的Cookie在区段中保留的天数。

      默认窗口为45天。 输入一个介于1 (1)到365之间的值。

   1. 单击 **[!UICONTROL Save]**.

1. 根据需要复制并实施标记以跟踪区段：

   1. 返回到 **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. 将光标悬停在区段行上并单击 **[!UICONTROL Get Pixel]**.

      * 要跟踪网页的桌面和移动设备访客，请执行以下操作：

         1. 复制标记为“ ”的页面查看跟踪标记[!UICONTROL Desktop or mobile websites]“

         1. 将标记提供给广告商或网站联系人以进行部署。

            广告商的IT部门或其他组可能需要计划标记部署或通知标记部署。

      * 要在桌面或移动设备上跟踪向广告单元公开的用户，请执行以下操作：

         1. 复制标记为的展示跟踪标记&quot;[!UICONTROL Desktop or mobile ads]“

1. 将标记添加到 [!UICONTROL Pixel] 选项卡，或者转到 [!UICONTROL Event Pixels] 的部分 [[!UICONTROL Tracking] 每个相关投放位置的设置](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

实施跟踪标记后，您可以在受众目标或排除项中将该区段用于任何投放位置。

>[!TIP]
>
>在跟踪用户时跟踪区段大小。

>[!MORELIKETHIS]
>
>* [关于受众管理](audience-about.md)
>* [编辑区段信息](segment-edit.md)
>* [删除区段](segment-delete.md)
>* [查看区段的跟踪像素](segment-view-pixels.md)
>* [共享或停止共享区段](segment-share.md)
>* [创建和实施 [!UICONTROL CCPA Opt-Out-of-Sale] 区段](ccpa-opt-out-segment-create.md)
>* [创建可重复使用的受众](reusable-audience-create.md)
>* [可用的第三方数据提供商](third-party-data-providers.md)
>* [投放设置](/help/dsp/campaign-management/placements/placement-settings.md)
