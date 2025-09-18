---
title: 显示广告设置
description: 请参阅显示广告可用广告设置的描述。
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 0%

---

# 显示广告设置

以下设置适用于标准显示广告。

## [!UICONTROL Ad Options]

### 基本

**[!UICONTROL Ad Type]：**（只读）您创建的广告类型，该类型与广告可以附加到的投放类型相对应。 默认为&#x200B;*[!UICONTROL Display]*。

**[!UICONTROL Ad Name]：**&#x200B;广告名称。 默认使用资源标题，但您可以更改名称。

>[!TIP]
>
> 在[!UICONTROL Ads]视图和报表中，使用将广告附加到投放位置时容易找到的名称。 例如，描述设备类型和一些关键属性（例如“假日产品预览：300x250游戏玩家”）。

**\[Ad Source\]**： （只读） *[!UICONTROL 3rd party]*。

**[!UICONTROL This is an expandable Banner]：** （仅限第三方广告）指示广告是可展开的横幅广告。 相关的扩展设置决定了要购买的库存，因此请确保它们反映了广告行为。

**[!UICONTROL Expansion Method]：** （仅限第三方可展开的横幅广告）横幅是展开于&#x200B;*[!UICONTROL Click]*&#x200B;还是&#x200B;*[!UICONTROL Rollover]*。

**[!UICONTROL Expansion Directions]：** （仅限第三方可展开的横幅广告）广告展开的方向： *[!UICONTROL Up]*、*[!UICONTROL Down]*、*[!UICONTROL Left]*&#x200B;或&#x200B;*[!UICONTROL Right]*。

**[!UICONTROL Certified Vendors]：** （仅限第三方可展开的横幅广告）广告可用的认证供应商： *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers])、*[!UICONTROL Flashtalking]*、*[!UICONTROL Sizmek]*&#x200B;或&#x200B;*[!UICONTROL Jivox]*。

**[!UICONTROL Display Code]：**（仅限第三方广告）第三方创意资源的URL。 任何[timestamp]和[[timestamp]]参数都被替换为实际值。

**[!UICONTROL Final Display Code]：**（仅限第三方广告）第三方创意资源的URL，已插入必要的[Advertising DSP跟踪宏](/help/dsp/campaign-management/macros.md)（如果适用）。

**[!UICONTROL Ad Size]：**&#x200B;广告的宽度和高度。 它必须是[支持的标准显示广告大小](ad-specs.md)。 您可以在上传广告之前手动输入广告大小或输入[!UICONTROL Display Code]。 如果不输入广告大小，则上传的广告或广告标记的维度会自动输入为只读。

>[!IMPORTANT]
>
> 在宽度和高度字段中声明的广告大小与传入的竞价请求匹配。 如果广告的维度与声明的广告大小不匹配，您可能会遇到投放问题。

### [!UICONTROL Pixel]

投放位置的所有现有事件跟踪像素都会自动附加。 您可以根据单个广告的跟踪需求，分离现有像素并根据需要创建新像素。 **提示：**&#x200B;要使用[!UICONTROL Ad Tools]视图在投放位置中一次编辑多个广告的第三方跟踪像素，请参阅“[将第三方跟踪像素附加到投放位置中的广告](/help/dsp/campaign-management/ads/ad-pixel-attach-detach.md#attach-pixels-ads)”。

以下设置适用于创建或编辑的每个像素。

**[!UICONTROL Integration Event]：**&#x200B;触发像素触发的事件。 对于此广告类型，使用在&#x200B;*[!UICONTROL Impression]*&#x200B;或&#x200B;*[!UICONTROL Click-through]*&#x200B;上触发的像素。

**[!UICONTROL Pixel Type]：**&#x200B;像素是&#x200B;*[!UICONTROL IMG URL]* （1x1像素图像文件）、*[!UICONTROL HTML]*&#x200B;还是&#x200B;*[!UICONTROL JavaScript URL]*。

**[!UICONTROL Pixel URL or Code]：**&#x200B;像素图像的URL，采用指定[!UICONTROL Pixel Type]的相应格式。

**[!UICONTROL Pixel Name]：**&#x200B;像素名称。 使用有助于您轻松识别像素的名称。

**[!UICONTROL Pixel Provider]：**&#x200B;像素提供程序： *[!UICONTROL None]*、*[!UICONTROL Comscore]*、*[!UICONTROL WhiteOps]*&#x200B;或&#x200B;*[!UICONTROL IAS]*。

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建单个Ad](ad-create.md)
>* [列出与广告关联的版面](ad-list-placements.md)
>* [广告规范](ad-specs.md)
>* [DSP宏](/help/dsp/campaign-management/macros.md)
