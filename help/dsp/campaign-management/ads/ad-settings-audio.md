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

**[!UICONTROL URL]**：VAST标记URL。

**[!UICONTROL Title]**：文件的名称，用于 [!UICONTROL Ads] 查看和报告。

>[!TIP]
>
> 要检查VAST标记的有效性，请将其粘贴到浏览器中并点击 **[!UICONTROL Enter]** 键。 如果标记有效，您将看到一个包含的XML文件 `<VAST>` 接近顶端。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]：** （只读）您创建的广告类型，该类型与广告可以附加到的版面类型相对应。 默认为 *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]：** 广告名称。 默认使用资源标题，但您可以更改名称。

>[!TIP]
>
> 在中，使用将广告附加到投放位置时容易找到的名称 [!UICONTROL Ads] 视图，并在报表中查看。 例如，描述设备类型和某些关键属性（如Holiday Product Preview： 30sec Audio）。

**[!UICONTROL Ad Duration]：** 音频文件的长度。 它会自动设置为 [!UICONTROL 15] 或 [!UICONTROL 30]，具体取决于所选的广告单位。

此字段不一定显示，具体取决于帐户权限。

**[!UICONTROL VAST Tag]：** （仅使用VAST标记的广告）第三方广告源的URL。 确保VAST标记仅包含音频媒体文件。

**[!UICONTROL Final VAST Tag]：** （仅使用VAST标记的广告）第三方广告源的URL，具有必要的 [Advertising DSP跟踪宏](/help/dsp/campaign-management/macros.md) 已插入（如果适用）。

**[!UICONTROL Select Rate]：** （仅限具有权限的用户）通过Adobe计费的预协商费率，或者您已经协商并通过供应商计费的费率之一。 要添加费率，请与您的Adobe客户团队联系。

### [!UICONTROL Pixel]

投放位置的所有现有事件跟踪像素都会自动附加。 您可以根据单个广告的跟踪需求，分离现有像素并根据需要创建新像素。 **提示：** 要使用一次性编辑投放位置中多个广告的第三方跟踪像素，请执行以下操作 [!UICONTROL Ad Tools] 视图，请参阅“[将第三方跟踪像素附加到投放位置中的广告](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads)“

以下设置适用于创建或编辑的每个像素。

**[!UICONTROL Integration Event]：** 触发像素触发的事件。 对于此广告类型，使用在 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]：** 像素是否为 *[!UICONTROL IMG URL]* （1x1像素图像文件）， *[!UICONTROL HTML]*，或 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]：** 像素图像的URL，采用指定像素类型的相应格式。

**[!UICONTROL Pixel Name]：** 像素名称。 使用有助于您轻松识别像素的名称。

**[!UICONTROL Pixel Provider]：** 像素提供程序：*[!UICONTROL None]*， *[!UICONTROL Comscore]*， *[!UICONTROL WhiteOps]*，或 *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建单个广告](ad-create.md)
>* [列出与广告关联的版面](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [广告规范](ad-specs.md)
>* [DSP宏](/help/dsp/campaign-management/macros.md)
