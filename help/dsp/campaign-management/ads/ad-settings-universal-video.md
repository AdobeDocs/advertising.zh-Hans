---
title: 通用视频广告设置
description: 请参阅对通用视频广告可用广告设置的描述。
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: d4af504a84d8fb356b2aca6d324e20fc0fb8fbbe
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# 通用视频广告设置

>[!NOTE]
>
>通用视频广告只能附加到通用视频投放位置。

## [!UICONTROL Insert Ad Tag]

*仅限新广告*

**[!UICONTROL URL]：** VAST标记URL。

**[!UICONTROL Title]：** 文件的标题，位于 [!UICONTROL Ads] 查看和报告。

>[!TIP]
>
> 要检查VAST标记的有效性，请将其粘贴到浏览器中并点击 **[!UICONTROL Enter]** 键。 如果标记有效，您将看到一个包含的XML文件 `<VAST>` 靠近顶端。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]：** （只读）您创建的广告类型，该类型与广告可以附加到的版面类型相对应。

**[!UICONTROL Ad Name]：** 广告名称。 默认情况下使用资源标题，但您可以更改名称。

>[!TIP]
>
> 在中，使用将广告附加到投放位置时容易找到的名称 [!UICONTROL Ads] 视图，以及在报表中。 例如，描述设备类型和某些关键属性（例如，Holiday Product Preview： 30sec Universal Video）。

**[!UICONTROL Show Controls]：** 要包含广告的视频控件的位置： *[!UICONTROL Under]*， *[!UICONTROL Over]*， *[!UICONTROL Bottom]*，或 *[!UICONTROL None]* （默认）。

**[!UICONTROL Preserve Aspect Ratio]：** 是否保持视频的宽度和高度比例(*[!UICONTROL Yes]*)或拉伸视频以填充可用空间(*[!UICONTROL No]*)。

**[!UICONTROL VAST Tag]：** （仅使用VAST标记的广告；只读）您输入的作为广告源的第三方VAST标记。

**[!UICONTROL Final VAST Tag]：** （仅使用VAST标记的广告；只读）您输入的作为广告源的第三方VAST标记，具有必需的 [Advertising DSP跟踪宏](/help/dsp/campaign-management/macros.md) 已插入（如果适用）。

**[!UICONTROL Wmode]：** 窗口模式： *[!UICONTROL window]*， *[!UICONTROL transparent]*，或 *[!UICONTROL opaque]*. 如果此设置不适用，则将其留空。

**[!UICONTROL Video Format]：** 潜在库存的广告播放器格式： *[!UICONTROL VPAID]*， *[!UICONTROL VPAID & VAST]*，或 *[!UICONTROL VAST]*. 可视性始终测量为 [!UICONTROL VPAID]，但 [!UICONTROL VPAID & VAST] 包括不允许可见性测量的库存。 如果可见性指标对您的营销活动很重要，请考虑此区别。

使用 [!UICONTROL VAST]，这不允许可视性测量，当您定位严格要求VAST格式的已连接电视或库存时(通常来自Google Ad Manager、Appnexus、SpotX和Freewheel等供应源)。 此外，此选项还可用于以前与标准前置广告(VAST)或手机+平板电脑标准前置广告(VAST)版面/广告兼容的库存。

**[!UICONTROL Clock Number]**：（仅在英国使用；仅向有权限的用户提供）用于确保正确广告广播的唯一标识符。 如果此设置不适用，则将其留空。

### [!UICONTROL Pixel]

投放位置的所有现有事件跟踪像素都会自动附加。 您可以根据单个广告的跟踪需求，分离现有像素并根据需要创建新像素。

以下设置适用于您创建或编辑的每个像素。

**[!UICONTROL Integration Event]：** 触发像素触发的事件。 对于此广告类型，请使用在广告上触发的像素。 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]：** 像素是否为 *[!UICONTROL IMG URL]* （1x1像素图像文件）， *[!UICONTROL HTML]*，或 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]：** 像素图像的URL，采用指定的相应格式 [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]：** 像素名称。 使用有助于您轻松识别像素的名称。

**[!UICONTROL Pixel Provider]：** 像素提供程序： *[!UICONTROL None]*， *[!UICONTROL Nielsen]*，或 *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [关于通用视频的常见问题解答](/help/dsp/campaign-management/faq-universal-video.md)
>* [关于广告管理](ad-about.md)
>* [创建单个广告](ad-create.md)
>* [列出与广告关联的投放位置](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [广告规范](ad-specs.md)
>* [DSP宏](/help/dsp/campaign-management/macros.md)

