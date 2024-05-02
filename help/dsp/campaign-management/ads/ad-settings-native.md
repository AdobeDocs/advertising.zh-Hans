---
title: 本机显示广告设置
description: 请参阅本机显示广告可用广告设置的说明。
feature: DSP Ads
exl-id: 64ce1946-072d-4ca9-b3a8-348987580403
source-git-commit: f521cf26d9d3945bdf1abe4577bb37d732432c87
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# 本机显示广告设置

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]：** （只读）您创建的广告类型，该类型与广告可以附加到的版面类型相对应。

**[!UICONTROL Ad Name]：** 广告名称。 默认使用广告类型，但您可以更改名称。

>[!TIP]
>
> 在中，使用将广告附加到投放位置时容易找到的名称 [!UICONTROL Ads] 视图，并在报表中查看。 例如，描述设备类型和某些关键属性（如Holiday Product Preview： 15sec Native）。

**[!UICONTROL Native Creative]：** 1200x627图像，可最大程度地提高移动库存的交付能力。 单击 **[!UICONTROL Browse]** 并在设备或网络上找到文件，然后单击 **[!UICONTROL Upload]**.

**[!UICONTROL Title]：** 吸引观众的抢眼标题。

**[!UICONTROL Description]：** 广告正文。 最大长度为100个字符。

**[!UICONTROL Landing Page]：** 查看器单击广告时登陆的URL。

**[!UICONTROL Final Landing Page]：** 此 [!UICONTROL Landing Page] 具有必要的URL [Advertising DSP跟踪宏](/help/dsp/campaign-management/macros.md) 已插入（如果适用）。

**[!UICONTROL Sponsored By (Advertiser Name)]：** 广告商。

**[!UICONTROL Call to Action]：** （可选）您希望查看者在看到此广告后执行的步骤。

**[!UICONTROL Advertiser Logo]：** （可选）要与广告配合使用的1:1比例徽标，以提高品牌知名度。 单击 **[!UICONTROL Browse]** 并在设备或网络上找到文件，然后单击 **[!UICONTROL Upload]**.

### [!UICONTROL Pixel]

投放位置的所有现有事件跟踪像素都会自动附加。 您可以根据单个广告的跟踪需求，分离现有像素并根据需要创建新像素。

以下设置适用于创建或编辑的每个像素。

**[!UICONTROL Integration Event]：** 触发像素触发的事件。 对于此广告类型，唯一的选项是 *[!UICONTROL Impression]*.

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
