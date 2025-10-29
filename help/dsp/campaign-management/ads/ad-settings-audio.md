---
title: 音频广告设置
description: 请参阅音频广告可用广告设置的说明。
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# 音频广告设置

## [!UICONTROL Insert Ad Tag]

*仅限新广告*

**[!UICONTROL URL]**： VAST标记URL。

**[!UICONTROL Title]**： [!UICONTROL Ads]视图和报告中使用的文件名称。

>[!TIP]
>
> 要检查VAST标记的有效性，请将其粘贴到浏览器中并点击&#x200B;**[!UICONTROL Enter]**&#x200B;键。 如果标记有效，您将在顶部附近看到包含`<VAST>`的XML文件。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]：**（只读）您创建的广告类型，该类型与广告可以附加到的投放类型相对应。 默认为&#x200B;*[!UICONTROL Audio]*。

**[!UICONTROL Ad Name]：**&#x200B;广告名称。 默认使用资源标题，但您可以更改名称。

>[!TIP]
>
> 在[!UICONTROL Ads]视图和报表中，使用将广告附加到投放位置时容易找到的名称。 例如，描述设备类型和某些关键属性（如Holiday Product Preview： 30sec Audio）。

**[!UICONTROL Ad Duration]：**&#x200B;音频文件的长度。 根据所选的广告单位，它自动设置为[!UICONTROL 15]或[!UICONTROL 30]。

此字段不一定显示，具体取决于帐户权限。

**[!UICONTROL VAST Tag]：** （仅使用VAST标记的广告）第三方广告源的URL。 确保VAST标记仅包含音频媒体文件。

**[!UICONTROL Final VAST Tag]：** （仅使用VAST标记的广告）插入了第三方广告源的URL以及必要的[Advertising DSP跟踪宏](/help/dsp/campaign-management/macros.md)（如果适用）。

**[!UICONTROL Select Rate]：** （仅具有权限的用户）通过Adobe记帐的预协商费率，或者您协商并通过供应商记帐的费率之一。 要添加费率，请联系您的Adobe客户团队。

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建单个Ad](ad-create.md)
>* [列出与广告关联的版面](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [广告规范](ad-specs.md)
>* [DSP宏](/help/dsp/campaign-management/macros.md)
