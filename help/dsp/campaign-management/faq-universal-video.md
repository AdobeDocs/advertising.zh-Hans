---
title: 关于通用视频的常见问题解答
description: 了解有关通用视频广告的更多信息。
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
source-git-commit: 8d65069b7da5d3c33cc7713c6c80af27eb6bf227
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# 关于通用视频的常见问题解答

[通用视频广告](/help/dsp/campaign-management/ads/ad-about.md#ad-types)允许您使用单个视频投放位置从桌面、移动设备和连接的电视环境中针对VPAID和VAST内容库定位视频内容库。

## 如何创建通用视频投放位置和广告？

通用视频投放位置只能包含通用视频广告，并且通用视频广告只能附加到通用视频投放位置。

创建通用视频投放位置和广告的方式与创建其他类型的投放位置和视频的方式类似：

1. 在所需的营销活动中，[创建一个通用视频投放位置](/help/dsp/campaign-management/placements/placement-create.md)，选择[!UICONTROL Placement Type] **[!UICONTROL Universal Video]**。

   您必须至少指定一个要定位的环境（桌面、移动设备、已连接电视）。

1. 在与通用视频广告相同的促销活动中，[创建单个通用视频广告](/help/dsp/campaign-management/ads/ad-create.md)或[创建多个通用视频广告](/help/dsp/campaign-management/ads/ad-create-multiple.md)。

   如果您创建多个广告，请确保将“[!UICONTROL Universal Video]”指定为[!UICONTROL Ad Type]：

   * 对于[!DNL Google]或[!DNL Flashtalking]广告：在上传文件后的“[!UICONTROL Review ad types]”步骤中，单击&#x200B;**[!UICONTROL Ad Type]**&#x200B;字段并选择&#x200B;**[!UICONTROL Universal Video]**。

   * 对于其他类型的广告标记：在上传的电子表格文件中，将每个广告的广告类型字段指定为&#x200B;**[!UICONTROL Universal Video]**。

1. [打开每个新广告的广告设置](/help/dsp/campaign-management/ads/ad-edit.md)，然后选择适用的视频格式：

   * 始终测量&#x200B;**[!UICONTROL VPAID]：**&#x200B;可见性。
   * **[!UICONTROL VPAID & VAST (Default)]：**&#x200B;包含不允许可见性测量的库存。
   * **[!UICONTROL VAST]** — 适用于已连接的电视清单。

   有关详细信息，请参阅[通用视频广告设置](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)。

1. [将新的通用视频广告](/help/dsp/campaign-management/ads/ad-attach-to-placement.md)附加到通用视频投放位置。

## 为什么在为通用视频放置选择连接的电视环境时，某些优化目标和包不可用？

与标准连接电视投放位置不兼容的目标（例如“每次点击成本最低”）在通用视频投放位置中的连接电视环境不受支持。 同样，具有不兼容优化目标的包也无法进行选择。

## 何时应将&#x200B;**[!UICONTROL VAST]**&#x200B;视频格式用于通用视频广告？

在以下任一情况下使用&#x200B;**[!UICONTROL VAST]**：

* 放置目标为连接的电视机盘点。
* 投放位置面向Google Ad Manager、Appnexus、SpotX或Freewheel中的视频库存。 这些SSP不支持VPAID和VAST视频格式。

## 是否可以将多个通用视频广告附加到同一个通用视频投放位置？

是的。
