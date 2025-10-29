---
title: 移动广告设置
description: 请参阅有关移动广告可用广告设置的描述。
feature: DSP Ads
exl-id: 45e8da8c-d6a2-4c42-8932-4cf551f6f899
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# 移动广告设置

## [!UICONTROL Insert Ad Tag]

*仅限新的移动视频广告格式*

**[!UICONTROL URL]**&#x200B;或&#x200B;**[!UICONTROL Ad Tag]**：包含创意资源和跟踪像素的第三方VAST广告标记或广告标记

**[!UICONTROL Ad Title]**&#x200B;或&#x200B;**[!UICONTROL Title]**： [!UICONTROL Ads]视图和报告中使用的广告名称。

>[!TIP]
>
> 要检查VAST标记的有效性，请将其粘贴到浏览器中并点击&#x200B;**[!UICONTROL Enter]**&#x200B;键。 如果标记有效，您将在顶部附近看到包含`<VAST>`的XML文件。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]：移动显示广告

**[!UICONTROL Ad Type]：**（只读）您创建的广告类型，该类型与广告可以附加到的投放类型相对应。

**[!UICONTROL Ad Name]：**&#x200B;广告名称。 默认使用资源标题，但您可以更改名称。

>[!TIP]
>
> 在广告视图和报表中，使用将广告附加到投放位置时容易找到的名称。 例如，描述设备类型和一些关键属性（例如“假日产品预览：300x250游戏玩家”）。

**\[Ad Source\]**： （只读） *[!UICONTROL 3rd party]*。

**[!UICONTROL Display Code]：**&#x200B;第三方创意资产的URL。 任何[timestamp]和[[timestamp]]参数都被替换为实际值。

**[!UICONTROL Final Display Code]：**&#x200B;第三方创意资源的URL已插入必要的[Advertising DSP跟踪宏](/help/dsp/campaign-management/macros.md)（如果适用）。

### [!UICONTROL Basic]：视频广告

**[!UICONTROL Ad Type]：**（只读）您创建的广告类型，该类型与广告可以附加到的投放类型相对应。

**[!UICONTROL Ad Name]：**&#x200B;广告名称。 默认使用资源标题，但您可以更改名称。

>[!TIP]
>
> 在广告视图和报表中，使用将广告附加到投放位置时容易找到的名称。 例如，描述设备类型和某些关键属性（如Holiday Product Preview： 30sec Phone Preroll）。

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]：**&#x200B;整个广告单位的宽度。 此选项可能会锁定，具体取决于您选择的广告单位类型。

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]：**&#x200B;整个广告单元的高度。 此选项可能会锁定，具体取决于您选择的广告单位类型。

**[!UICONTROL Player X]：**&#x200B;广告单元的X坐标。 保留默认设置。

**[!UICONTROL Player Y]：**&#x200B;广告单元的Y坐标。 保留默认设置。

**[!UICONTROL Player Width]：**&#x200B;整个广告单位的宽度。 此选项可能会锁定，具体取决于您选择的广告单位类型。

这与&#x200B;**[!UICONTROL Width]**&#x200B;字段相同。

**[!UICONTROL Player Height]：**&#x200B;整个广告单元的高度。 此选项可能会锁定，具体取决于您选择的广告单位类型。

这与&#x200B;**[!UICONTROL Height]**&#x200B;字段相同。

**[!UICONTROL Show Controls]：**&#x200B;在何处包括广告的视频控件： *[!UICONTROL Under]*、*[!UICONTROL Over]*、*[!UICONTROL Bottom]*&#x200B;或&#x200B;*[!UICONTROL None]*（默认）。

**[!UICONTROL Preserve Aspect Ratio]：**&#x200B;是保留视频的宽度和高度比例(*[!UICONTROL Yes]*)，还是拉伸视频以填充可用空间(*[!UICONTROL No]*)。

**[!UICONTROL Close Button Delay]：** （某些广告类型）延迟关闭按钮出现的秒数。

**[!UICONTROL VAST Tag]：**（仅使用VAST标记的广告；只读）您作为创意资产输入的第三方VAST标记。

**[!UICONTROL Final VAST Tag]：** （仅使用VAST标记的广告；只读）作为创意资源输入的第三方VAST标记添加了必要的[Advertising DSP跟踪宏](/help/dsp/campaign-management/macros.md)（如果适用）。

**[!UICONTROL Wmode]：** （某些广告类型）窗口模式： *[!UICONTROL window]*、*[!UICONTROL transparent]*&#x200B;或&#x200B;*[!UICONTROL opaque]*。

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

### [!UICONTROL Sharing]

已弃用

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建单个Ad](ad-create.md)
>* [列出与广告关联的版面](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [广告规范](ad-specs.md)
>* [DSP宏](/help/dsp/campaign-management/macros.md)
