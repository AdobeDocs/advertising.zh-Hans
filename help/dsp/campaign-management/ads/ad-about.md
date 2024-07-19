---
title: 关于Advertising DSP中的广告管理
description: 了解广告管理。
feature: DSP Ads
exl-id: 41dbe28e-a476-4601-a3d8-a9111eae3f6b
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---

# 关于Advertising DSP中的广告管理

<!-- add "The Ads View (Dashboard?)" section -->

DSP支持通过适用于各种广告类型的第三方广告投放标签(例如Google、Flashtalking或Sizmek)进行广告投放，并支持针对原生显示广告直接上传资源。 您可以单独上传第三方标记，也可以批量上传。 批量上传使用合作伙伴标记表或批量标记模板。

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

设置广告后，将每个广告附加到投放位置，其中包含用于控制营销活动交付方式的定位参数（例如地域、受众、设备和库存定位）。 您可以将单个广告附加到一个或多个投放位置。

## 可用广告类型 {#ad-types}

以下所有广告类型在DSP中均可用。 有关每种广告类型的完整规范，请参阅[广告规范](ad-specs.md)。

* **音频广告（仅限第三方）**：音频广告在数字发布者网站上的内容之间播放，并且可以作为音频文件单独运行或与随附横幅一起运行。 音频最适合用于提升品牌知名度以及与移动受众互动。 音频的关键绩效指标包括[!UICONTROL Completion Rate]和[!UICONTROL Cost per Completion]。

* **显示广告（仅限第三方）**：显示广告是在Web浏览器或应用程序中显示的动画或静态图像。 单击广告单元会将用户转至品牌网站或微型网站。 “显示”最适合用来推动高效的CPM、增强消息关联、添加其他品牌或产品接触点以及促使用户降低购买漏斗水平。 显示的关键绩效指标包括[!UICONTROL Clicks]、[!UICONTROL Cost per Click]、[!UICONTROL Conversions]和[!UICONTROL Cost per Conversion]。 DSP支持各种不同的显示横幅广告大小。

* **移动设备广告（仅限第三方）**：移动设备广告可以是前置视频(VAST、MRAID)或标准显示格式。 移动设备前置视频可以自动播放或单击播放，最适合跨屏幕触及观看者。 移动标准显示是在移动Web浏览器或应用程序中显示的静态图像，最适合用于补充数字视频购买、促进消息关联以及添加其他品牌或产品接触点。 移动广告还可以用作全屏收购或移动插播式广告，这些是全屏、高影响力的移动广告，最适合用于提高移动受众的品牌知名度并促进转化。

* **本机显示广告（仅限第一方）**：标准显示格式支持本机广告。 原生广告包括标题和/或标题、描述、徽标和图像。 组合并呈现广告元素以匹配发布者的页面样式，以便广告与发布者的有机内容融合并促进更高的参与度。 “原生”最适合用于品牌知名度，以及通过便于查看的广告提高受众查看次数和参与率。 关键绩效指标包括[!UICONTROL Clicks]、[!UICONTROL Cost Per Click]、[!UICONTROL Conversions]和[!UICONTROL Cost Per Conversion]。

* **前置广告（仅限第三方）**：前置广告（VAST和VPAID）显示在高级视频内容之前，并提供引人入胜的沉浸式观众体验。 前置式视频可以是交互式的，包含富媒体功能，并包括叠加、变换图像和行动号召。 前置视频广告的关键性能指标包括[!UICONTROL Video Completion Rate]和[!UICONTROL Viewability Rate]。

* **连接的电视广告（仅限第三方）**：在优质电视视频内容之前和期间显示连接的电视广告。 所有连接的电视设备清单都运行在电视设备上，这意味着视频在倾斜的全屏环境中自动播放，观看者无法跳过。 Connected TV是与电视广告最接近的数字视频格式。 已连接电视的关键性能指标包括[!UICONTROL Completion Rate]。

* **通用视频广告（仅限第三方）**：通用视频广告允许您通过单个视频投放位置，从桌面、移动设备和连接的电视环境中为VPAID和VAST库存定位视频库存。 它们组合了连接电视、前置广告和移动设备前置广告的所有功能，并在视频内容之前和期间显示。 通用视频的关键性能指标包括[!UICONTROL Completion Rate]和[!UICONTROL Viewability Rate]。

  通用视频广告只能附加到通用视频投放位置。

  有关通用视频广告的更多信息，请参阅[关于通用视频的常见问题解答](/help/dsp/campaign-management/faq-universal-video.md)。

## DSP广告审批

创建广告时，DSP会检查敏感类别，单击URL功能，然后预览渲染。

最初，广告的[!UICONTROL Status]列显示一个红点。 审查过程通常需要24-48小时。 但是，损坏的广告可能会有超过48小时的待处理状态，因此您可以在广告被拒绝之前有时间修复错误。 被拒绝的广告包括拒绝的原因。

当DSP批准广告时，广告的状态列会显示一个绿点。

[!UICONTROL Status]列中的![审批指示器](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>只有DSP和SSP都批准创意内容后，才能提供您的广告。 每个SSP都有自己的批准要求和流程。

>[!MORELIKETHIS]
>
>* [创建单个Ad](ad-create.md)
>* [创建多个第三方广告](ad-create-multiple.md)
>* [广告规范](ad-specs.md)
