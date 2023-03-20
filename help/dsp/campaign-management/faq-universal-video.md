---
title: 关于通用视频的常见问题解答
description: 了解有关通用视频广告的更多信息。
feature: DSP Placements, DSP Ads
source-git-commit: fe5340cbf495eb9498d89c18080307464d4067d9
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# 有关通用视频的常见问题解答

## 如何创建通用视频投放和广告？

通用视频投放只能包含通用视频广告，通用视频广告只能附加到通用视频投放。

创建它们的方式与创建其他类型的版面和视频的方式类似：

1. 在所需的营销活动中， [创建通用视频版面](/help/dsp/campaign-management/placements/placement-create.md)，选择 [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   您需要至少指定一个环境（桌面、移动设备、连接的电视）来定位。

1. 在与通用视频投放相同的营销活动中， [创建单个通用视频广告](/help/dsp/campaign-management/ads/ad-create.md) 或 [创建多个通用视频广告](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   如果创建多个广告，请确保指定“[!UICONTROL Universal Video]”作为 [!UICONTROL Ad Type]:

   * 对于 [!DNL Google] 或 [!DNL Flashtalking] 广告：在“[!UICONTROL Review ad types]“ ”步骤，单击 **[!UICONTROL Ad Type]** 字段和选择 **[!UICONTROL Universal Video]**.

   * 对于其他类型的广告标记：在您上传的电子表格文件中，将每个广告的“广告类型”字段指定为 **[!UICONTROL Universal Video]**.

1. [打开广告设置](/help/dsp/campaign-management/ads/ad-edit.md) 对于每个新广告，选择适用的视频格式：

   * **[!UICONTROL VPAID]:** 可视性始终由测量。
   * **[!UICONTROL VPAID & VAST (Default)]:** 包括不允许可视性测量的库存。
   * **[!UICONTROL VAST]**  — 适合连接的电视清单。

   请参阅“[通用视频广告设置](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)“ ”以了解详细信息。

1. [附加新的通用视频广告](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) 到通用视频位置。

## 为什么在选择连接的电视环境进行通用视频放置时，某些优化目标和包不可用？

通用视频版面中的连接电视环境不支持与标准连接电视版面不兼容的目标，例如“每次点击最低成本”。 同样，具有不兼容优化目标的包也无法进行选择。

## 何时应 **[!UICONTROL VAST]** 视频格式是否用于通用视频广告？

使用 **[!UICONTROL VAST]** 在以下任一情况下：

* 该位置将针对连接的电视内容库。
* 该位置将针对Google广告管理器、Appnexus、SpotX或Freewheel中的视频库存。 这些SSP不支持VPAID和VAST视频格式。

## 是否可以将多个通用视频广告附加到同一通用视频位置？

是的。
