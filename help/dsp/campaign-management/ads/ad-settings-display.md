---
title: 显示广告设置
description: 请参阅显示广告可用广告设置的描述。
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: 2f137b17deea4cd02ae19494a306ff37c7002423
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# 显示广告设置

以下设置适用于标准显示广告。

## [!UICONTROL Ad Options]

### 基本

**[!UICONTROL Ad Type]：** （只读）您创建的广告类型，该类型与广告可以附加到的版面类型相对应。 默认为 *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]：** 广告名称。 默认使用资源标题，但您可以更改名称。

>[!TIP]
>
> 在中，使用将广告附加到投放位置时容易找到的名称 [!UICONTROL Ads] 视图，并在报表中查看。 例如，描述设备类型和一些关键属性（例如“假日产品预览：300x250游戏玩家”）。

**\[广告源\]**：（只读） *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]：** （仅限第三方广告）指示广告是可展开的横幅广告。 相关的扩展设置决定了要购买的库存，因此请确保它们反映了广告行为。

**[!UICONTROL Expansion Method]：** （仅限第三方可展开的横幅广告）横幅是否展开 *[!UICONTROL Click]* 或 *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]：** （仅限第三方可展开的横幅广告）广告展开的方向： *[!UICONTROL Up]*， *[!UICONTROL Down]*， *[!UICONTROL Left]*，或 *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]：** （仅限第三方可展开的横幅广告）提供广告的认证供应商： *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers])， *[!UICONTROL Flashtalking]*， *[!UICONTROL Sizmek]*，或 *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]：** （仅限第三方广告）第三方创意资产的URL。 任何 [时间戳] 和[[时间戳]]参数将被替换为实际值。

**[!UICONTROL Final Display Code]：** （仅限第三方广告）第三方创意资产的URL，带有必要的 [Advertising DSP跟踪宏](/help/dsp/campaign-management/macros.md) 已插入（如果适用）。

**[!UICONTROL Ad Size]：** 广告的宽度和高度。 它必须是 [支持的标准显示广告大小](ad-specs.md). 在上传广告之前，您可以手动输入广告大小，也可以输入 [!UICONTROL Display Code]. 如果不输入广告大小，则上传的广告或广告标记的维度会自动输入为只读。 请注意，如果尺寸不在标准显示范围内，则不会将显示广告另存为大小 — 例如，301x250而不是300x250广告大小。

>[!IMPORTANT]
>
> 在宽度和高度字段中声明的广告大小将与传入的竞价请求匹配。 如果广告的维度与声明的广告大小不匹配，您可能会遇到投放问题。

### [!UICONTROL Pixel]

投放位置的所有现有事件跟踪像素都会自动附加。 您可以根据单个广告的跟踪需求，分离现有像素并根据需要创建新像素。 **提示：** 要使用一次性编辑投放位置中多个广告的第三方跟踪像素，请执行以下操作 [!UICONTROL Ad Tools] 视图，请参阅“[将第三方跟踪像素附加到投放位置中的广告](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads)“

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
>* [列出与广告关联的版面](ad-list-placements.md)
>* [广告规范](ad-specs.md)
>* [DSP宏](/help/dsp/campaign-management/macros.md)
