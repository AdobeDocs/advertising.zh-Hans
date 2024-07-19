---
title: 音频广告设置
description: 请参阅音频广告可用广告设置的说明。
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '406'
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

**[!UICONTROL Select Rate]：** （仅具有权限的用户）通过Adobe计费的预协商费率，或者您通过供应商协商并计费的费率之一。 要添加费率，请与您的Adobe客户团队联系。

### [!UICONTROL Pixel]

投放位置的所有现有事件跟踪像素都会自动附加。 您可以根据单个广告的跟踪需求，分离现有像素并根据需要创建新像素。 **提示：**&#x200B;要使用[!UICONTROL Ad Tools]视图在投放位置中一次编辑多个广告的第三方跟踪像素，请参阅“[将第三方跟踪像素附加到投放位置中的广告](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads)”。

以下设置适用于创建或编辑的每个像素。

**[!UICONTROL Integration Event]：**&#x200B;触发像素触发的事件。 对于此广告类型，使用在&#x200B;*[!UICONTROL Impression]*&#x200B;或&#x200B;*[!UICONTROL Click-through]*&#x200B;上触发的像素。

**[!UICONTROL Pixel Type]：**&#x200B;像素是&#x200B;*[!UICONTROL IMG URL]* （1x1像素图像文件）、*[!UICONTROL HTML]*&#x200B;还是&#x200B;*[!UICONTROL JavaScript URL]*。

**[!UICONTROL Pixel URL or Code]：**&#x200B;像素图像的URL，采用指定像素类型的相应格式。

**[!UICONTROL Pixel Name]：**&#x200B;像素名称。 使用有助于您轻松识别像素的名称。

**[!UICONTROL Pixel Provider]：**&#x200B;像素提供程序：*[!UICONTROL None]*、*[!UICONTROL Comscore]*、*[!UICONTROL WhiteOps]*&#x200B;或&#x200B;*[!UICONTROL IAS]*。

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建单个Ad](ad-create.md)
>* [列出与广告关联的版面](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [广告规范](ad-specs.md)
>* [DSP宏](/help/dsp/campaign-management/macros.md)
