---
title: 通用视频广告设置
description: 请参阅对通用视频广告可用广告设置的描述。
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# 通用视频广告设置

>[!NOTE]
>
>通用视频广告只能附加到通用视频投放位置。

## [!UICONTROL Insert Ad Tag]

*仅限新广告*

**[!UICONTROL URL]：** VAST标记URL。

**[!UICONTROL Title]：**&#x200B;文件标题，该文件在[!UICONTROL Ads]视图和报告中。

>[!TIP]
>
> 要检查VAST标记的有效性，请将其粘贴到浏览器中并点击&#x200B;**[!UICONTROL Enter]**&#x200B;键。 如果标记有效，您将在顶部附近看到包含`<VAST>`的XML文件。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]：**（只读）您创建的广告类型，该类型与广告可以附加到的投放类型相对应。

**[!UICONTROL Ad Name]：**&#x200B;广告名称。 默认使用资源标题，但您可以更改名称。

>[!TIP]
>
> 在[!UICONTROL Ads]视图和报表中，使用将广告附加到投放位置时容易找到的名称。 例如，描述设备类型和某些关键属性（如Holiday Product Preview： 30sec Universal Video）。

**[!UICONTROL Show Controls]：**&#x200B;在何处包括广告的视频控件： *[!UICONTROL Under]*、*[!UICONTROL Over]*、*[!UICONTROL Bottom]*&#x200B;或&#x200B;*[!UICONTROL None]*（默认）。

**[!UICONTROL Preserve Aspect Ratio]：**&#x200B;是保留视频的宽度和高度比例(*[!UICONTROL Yes]*)，还是拉伸视频以填充可用空间(*[!UICONTROL No]*)。

**[!UICONTROL VAST Tag]：** （仅使用VAST标记的广告；只读）您输入的作为广告源的第三方VAST标记。

**[!UICONTROL Final VAST Tag]：** （仅使用VAST标记的广告；只读）您输入的第三方VAST标记作为广告源并插入了必要的[Advertising DSP跟踪宏](/help/dsp/campaign-management/macros.md)（如果适用）。

**[!UICONTROL Wmode]：**&#x200B;窗口模式： *[!UICONTROL window]*、*[!UICONTROL transparent]*&#x200B;或&#x200B;*[!UICONTROL opaque]*。 如果此设置不适用，则将其留空。

**[!UICONTROL Video Format]：**&#x200B;潜在库存的广告播放器格式： *[!UICONTROL VPAID]*、*[!UICONTROL VPAID & VAST]*&#x200B;或&#x200B;*[!UICONTROL VAST]*。 始终为[!UICONTROL VPAID]测量可见性，但[!UICONTROL VPAID & VAST]包含不允许测量可见性的库存。 如果可见性指标对您的营销活动很重要，请考虑这种区别。

当您定位严格要求VAST格式的联网电视或库存时(通常来自Google Ad Manager、Appnexus、SpotX和Freewheel等供应源)，请使用[!UICONTROL VAST]，它不允许可见性测量。 此外，对于之前与标准前置广告(VAST)或手机+平板电脑标准前置广告(VAST)版面/广告兼容的库存，也使用此选项。

**[!UICONTROL Clock Number]**： （仅在英国使用；仅供具有权限的用户使用）用于确保广播正确广告的唯一标识符。 如果此设置不适用，则将其留空。

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* 有关通用视频的[常见问题解答](/help/dsp/campaign-management/faq-universal-video.md)
>* [关于广告管理](ad-about.md)
>* [创建单个Ad](ad-create.md)
>* [列出与广告关联的版面](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [广告规范](ad-specs.md)
>* [DSP宏](/help/dsp/campaign-management/macros.md)
