---
title: 移动广告设置
description: 请参阅有关移动广告可用广告设置的描述。
feature: DSP Ads
exl-id: 45e8da8c-d6a2-4c42-8932-4cf551f6f899
source-git-commit: f521cf26d9d3945bdf1abe4577bb37d732432c87
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# 移动广告设置

## [!UICONTROL Insert Ad Tag]

*仅限新的移动视频广告格式*

**[!UICONTROL URL]** 或 **[!UICONTROL Ad Tag]**：包含创意资源和跟踪像素的第三方VAST广告标记或广告标记

**[!UICONTROL Ad Title]** 或 **[!UICONTROL Title]**：在中使用的广告的名称 [!UICONTROL Ads] 查看和报告。

>[!TIP]
>
> 要检查VAST标记的有效性，请将其粘贴到浏览器中并点击 **[!UICONTROL Enter]** 键。 如果标记有效，您将看到一个包含的XML文件 `<VAST>` 接近顶端。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]：移动设备显示广告

**[!UICONTROL Ad Type]：** （只读）您创建的广告类型，该类型与广告可以附加到的版面类型相对应。

**[!UICONTROL Ad Name]：** 广告名称。 默认使用资源标题，但您可以更改名称。

>[!TIP]
>
> 在广告视图和报表中，使用将广告附加到投放位置时容易找到的名称。 例如，描述设备类型和一些关键属性（例如“假日产品预览：300x250游戏玩家”）。

**\[广告源\]**：（只读） *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]：** 第三方创意资产的URL。 任何 [时间戳] 和[[时间戳]]参数将被替换为实际值。

**[!UICONTROL Final Display Code]：** 第三方创意资源的URL，带有必要的 [Advertising DSP跟踪宏](/help/dsp/campaign-management/macros.md) 已插入（如果适用）。

### [!UICONTROL Basic]：视频广告

**[!UICONTROL Ad Type]：** （只读）您创建的广告类型，该类型与广告可以附加到的版面类型相对应。

**[!UICONTROL Ad Name]：** 广告名称。 默认使用资源标题，但您可以更改名称。

>[!TIP]
>
> 在广告视图和报表中，使用将广告附加到投放位置时容易找到的名称。 例如，描述设备类型和某些关键属性（如Holiday Product Preview： 30sec Phone Preroll）。

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]：** 整个广告单位的宽度。 此选项可能会锁定，具体取决于您选择的广告单位类型。

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]：** 整个广告单元的高度。 此选项可能会锁定，具体取决于您选择的广告单位类型。

**[!UICONTROL Player X]：** 广告单位的X坐标。 保留默认设置。

**[!UICONTROL Player Y]：** 广告单元的Y坐标。 保留默认设置。

**[!UICONTROL Player Width]：** 整个广告单位的宽度。 此选项可能会锁定，具体取决于您选择的广告单位类型。

这与 **[!UICONTROL Width]** 字段。

**[!UICONTROL Player Height]：** 整个广告单元的高度。 此选项可能会锁定，具体取决于您选择的广告单位类型。

这与 **[!UICONTROL Height]** 字段。

**[!UICONTROL Show Controls]：** 要包含广告的视频控件的位置： *[!UICONTROL Under]*， *[!UICONTROL Over]*， *[!UICONTROL Bottom]*，或 *[!UICONTROL None]* （默认）。

**[!UICONTROL Preserve Aspect Ratio]：** 是否保持视频的宽度和高度比例(*[!UICONTROL Yes]*)或拉伸视频以填充可用空间(*[!UICONTROL No]*)。

**[!UICONTROL Close Button Delay]：** （某些广告类型）延迟关闭按钮显示的秒数。

**[!UICONTROL VAST Tag]：** （仅使用VAST标记的广告；只读）您作为创意资产输入的第三方VAST标记。

**[!UICONTROL Final VAST Tag]：** （仅使用VAST标记的广告；只读）您作为创意资产输入的第三方VAST标记（如有必要） [Advertising DSP跟踪宏](/help/dsp/campaign-management/macros.md) 已插入（如果适用）。

**[!UICONTROL Wmode]：** （部分广告类型）窗口模式： *[!UICONTROL window]*， *[!UICONTROL transparent]*，或 *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

投放位置的所有现有事件跟踪像素都会自动附加。 您可以根据单个广告的跟踪需求，分离现有像素并根据需要创建新像素。

以下设置适用于创建或编辑的每个像素。

**[!UICONTROL Integration Event]：** 触发像素触发的事件。 对于此广告类型，使用在 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]：** 像素是否为 *[!UICONTROL IMG URL]* （1x1像素图像文件）， *[!UICONTROL HTML]*，或 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]：** 像素图像的URL，采用指定的相应格式 [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]：** 像素名称。 使用有助于您轻松识别像素的名称。

**[!UICONTROL Pixel Provider]：** 像素提供程序： *[!UICONTROL None]*， *[!UICONTROL Comscore]*， *[!UICONTROL WhiteOps]*，或 *[!UICONTROL IAS]*.

### [!UICONTROL Sharing]

已弃用

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建单个广告](ad-create.md)
>* [列出与广告关联的版面](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [广告规范](ad-specs.md)
>* [DSP宏](/help/dsp/campaign-management/macros.md)
