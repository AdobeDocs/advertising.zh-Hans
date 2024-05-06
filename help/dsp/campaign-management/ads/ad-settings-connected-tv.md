---
title: 已连接电视广告设置
description: 请参阅已连接电视广告可用广告设置的说明。
feature: DSP Ads
exl-id: d8e47f7e-7480-400f-8ffa-ecf41ce2ebfb
source-git-commit: 2f137b17deea4cd02ae19494a306ff37c7002423
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# 已连接电视广告设置

## [!UICONTROL Insert Ad Tag]

*仅限新广告*

**[!UICONTROL URL]**：VAST标记URL。

**[!UICONTROL Title]**：文件的名称，将在广告视图和报表中使用。

>[!TIP]
>
> 要检查VAST标记的有效性，请将其粘贴到浏览器中并点击 **[!UICONTROL Enter]** 键。 如果标记有效，您将看到一个包含的XML文件 `<VAST>` 接近顶端。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]：** （只读）您创建的广告类型，该类型与广告可以附加到的版面类型相对应。

**[!UICONTROL Ad Name]：** 广告名称。 默认使用资源标题，但您可以更改名称。

>[!TIP]
>
> 在中，使用将广告附加到投放位置时容易找到的名称 [!UICONTROL Ads] 视图，并在报表中查看。 例如，描述设备类型和某些关键属性（如“Holiday Product Preview： 30sec CTV”）。

**[!UICONTROL Width | Ad Unit Width]：** 整个广告单位的宽度。 此选项可能会锁定，具体取决于您选择的广告单位类型。

**[!UICONTROL Height | Ad Unit Height]：** 整个广告单元的高度。 此选项可能会锁定，具体取决于您选择的广告单位类型。

**[!UICONTROL Player X]：** 广告单位的X坐标。 保留默认设置。

**[!UICONTROL Player Y]：** 广告单元的Y坐标。 保留默认设置。

**[!UICONTROL Player Width]：** 整个广告单位的宽度。 此选项可能会锁定，具体取决于您选择的广告单位类型。

这与 **[!UICONTROL Width]** 字段。

**[!UICONTROL Player Height]：** 整个广告单元的高度。 此选项可能会锁定，具体取决于您选择的广告单位类型。

这与 **[!UICONTROL Height]** 字段。

**[!UICONTROL Show Controls]：** 要包含广告的视频控件的位置： *[!UICONTROL Under]*， *[!UICONTROL Over]*， *[!UICONTROL Bottom]*，或 *[!UICONTROL None]* （默认）。

**[!UICONTROL Preserve Aspect Ratio]：** 是否保持视频的宽度和高度比例(*[!UICONTROL Yes]*)或拉伸视频以填充可用空间(*[!UICONTROL No]*)。

**[!UICONTROL VAST Tag]：** （仅使用VAST标记的广告；只读）您输入的作为广告源的第三方VAST标记。

**[!UICONTROL Final VAST Tag]：** （仅使用VAST标记的广告；只读）您输入的作为广告源的第三方VAST标记，具有必要 [Advertising DSP跟踪宏](/help/dsp/campaign-management/macros.md) 已插入（如果适用）。

**[!UICONTROL Clock Number]**：（仅在英国使用；仅向有权限的用户提供）用于确保正确广告广播的唯一标识符。 如果此设置不适用，则将其留空。

### [!UICONTROL Pixel]

投放位置的所有现有事件跟踪像素都会自动附加。 您可以根据单个广告的跟踪需求，分离现有像素并根据需要创建新像素。 **提示：** 要使用一次性编辑投放位置中多个广告的第三方跟踪像素，请执行以下操作 [!UICONTROL Ad Tools] 视图，请参阅“[将第三方跟踪像素附加到投放位置中的广告](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads)“

以下设置适用于创建或编辑的每个像素。

**[!UICONTROL Integration Event]：** 触发像素触发的事件。 对于此广告类型，使用在 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]：** 像素是否为 *[!UICONTROL IMG URL]* （1x1像素图像文件）， *[!UICONTROL HTML]*，或 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]：** 像素图像的URL，采用指定像素类型的相应格式。

**[!UICONTROL Pixel Name]：** 像素名称。 使用有助于您轻松识别像素的名称。

**[!UICONTROL Pixel Provider]：** 像素提供程序： *[!UICONTROL None]*， *[!UICONTROL Comscore]*， *[!UICONTROL WhiteOps]*，或 *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建单个广告](ad-create.md)
>* [列出与广告关联的版面](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [广告规范](ad-specs.md)
>* [DSP宏](/help/dsp/campaign-management/macros.md)
