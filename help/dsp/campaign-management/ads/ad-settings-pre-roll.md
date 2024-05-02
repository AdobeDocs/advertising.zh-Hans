---
title: 前置广告设置
description: 请参阅前置广告可用广告设置的描述。
feature: DSP Ads
exl-id: d0ba4346-13ae-405c-92b6-a0c32dd09d0a
source-git-commit: f521cf26d9d3945bdf1abe4577bb37d732432c87
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# 前置广告设置

## [!UICONTROL Insert Ad Tag]

*仅限新广告*

**[!UICONTROL URL]：** VAST标记URL。

**[!UICONTROL Title]：** 文件的标题，位于 [!UICONTROL Ads] 查看和报告。

>[!TIP]
>
> 要检查VAST标记的有效性，请将其粘贴到浏览器中并点击 **[!UICONTROL Enter]** 键。 如果标记有效，您将看到一个包含的XML文件 `<VAST>` 接近顶端。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]：** （只读）您创建的广告类型，该类型与广告可以附加到的版面类型相对应。

**[!UICONTROL Ad Name]：** 广告名称。 默认使用资源标题，但您可以更改名称。

>[!TIP]
>
> 在中，使用将广告附加到投放位置时容易找到的名称 [!UICONTROL Ads] 视图，并在报表中查看。 例如，描述设备类型和某些关键属性（如Holiday Product Preview： 30sec Preroll ）。

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]：** （仅限标准和可跳过的前置广告）整个广告单位的宽度。 此选项可能会锁定，具体取决于您选择的广告单位类型。

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]：** （仅限标准和可跳过的前置广告）整个广告单元的高度。 此选项可能会锁定，具体取决于您选择的广告单位类型。

**[!UICONTROL Player X]：** 广告单位的X坐标。 保留默认设置。

**[!UICONTROL Player Y]：** 广告单元的Y坐标。 保留默认设置。

**[!UICONTROL Player Width]：** 整个广告单位的宽度。 此选项可能会锁定，具体取决于您选择的广告单位类型。

此字段与 **[!UICONTROL Width]** 字段。

**[!UICONTROL Player Height]：** 整个广告单元的高度。 此选项可能会锁定，具体取决于您选择的广告单位类型。

这与 **[!UICONTROL Height]** 字段。

**[!UICONTROL Show Controls]：** 要包含广告的视频控件的位置： *[!UICONTROL Under]*， *[!UICONTROL Over]*， *[!UICONTROL Bottom]*，或 *[!UICONTROL None]* （默认）。

**[!UICONTROL Preserve Aspect Ratio]：** 是否保持视频的宽度和高度比例(*[!UICONTROL Yes]*)或拉伸视频以填充可用空间(*[!UICONTROL No]*)。

**[!UICONTROL VAST Tag]：** （仅使用VAST标记的广告；只读）您输入的作为广告源的第三方VAST标记。

**[!UICONTROL Final VAST Tag]：** （仅使用VAST标记的广告；只读）您输入的作为广告源的第三方VAST标记，具有必要 [Advertising DSP跟踪宏](/help/dsp/campaign-management/macros.md) 已插入（如果适用）。

**[!UICONTROL Wmode]：** （仅限交互式前置式广告）窗口模式： *[!UICONTROL window]*， *[!UICONTROL transparent]*，或 *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]：** （仅限交互式前置式广告）潜在库存的广告播放器格式： *[!UICONTROL VPAID]* 或 *[!UICONTROL VPAID & VAST]*. 可视性始终按VPAID进行测量，但VPAID和VAST包括不允许进行可视性测量的库存。 如果可见性指标对您的营销活动很重要，请考虑这种区别。

**[!UICONTROL Clock Number]**：（仅限交互式前置广告；仅在英国使用；仅供拥有权限的用户使用）用于确保正确广告广播的唯一标识符。 如果此设置不适用，则将其留空。

### [!UICONTROL Pixel]

投放位置的所有现有事件跟踪像素都会自动附加。 您可以根据单个广告的跟踪需求，分离现有像素并根据需要创建新像素。

以下设置适用于创建或编辑的每个像素。

**[!UICONTROL Integration Event]：** 触发像素触发的事件。 对于此广告类型，使用在 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]：** 像素是否为 *[!UICONTROL IMG URL]* （1x1像素图像文件）， *[!UICONTROL HTML]*，或 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]：** 像素图像的URL，采用指定的相应格式 [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]：** 像素名称。 使用有助于您轻松识别像素的名称。

**[!UICONTROL Pixel Provider]：** 像素提供程序： *[!UICONTROL None]*， *[!UICONTROL Comscore]*， *[!UICONTROL WhiteOps]*，或 *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建单个广告](ad-create.md)
>* [列出与广告关联的版面](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [广告规范](ad-specs.md)
>* [DSP宏](/help/dsp/campaign-management/macros.md)
