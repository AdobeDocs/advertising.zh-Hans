---
title: 本机显示广告设置
description: 请参阅本机显示广告可用广告设置的说明。
feature: DSP Ads
exl-id: 64ce1946-072d-4ca9-b3a8-348987580403
source-git-commit: 2f137b17deea4cd02ae19494a306ff37c7002423
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# 本机显示广告设置

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]：**（只读）您创建的广告类型，该类型与广告可以附加到的投放类型相对应。

**[!UICONTROL Ad Name]：**&#x200B;广告名称。 默认使用广告类型，但您可以更改名称。

>[!TIP]
>
> 在[!UICONTROL Ads]视图和报表中，使用将广告附加到投放位置时容易找到的名称。 例如，描述设备类型和某些关键属性（如Holiday Product Preview： 15sec Native）。

**[!UICONTROL Native Creative]：**&#x200B;一个1200x627的图像，用于最大化移动库存的交付。 单击&#x200B;**[!UICONTROL Browse]**&#x200B;并在您的设备或网络上找到该文件，然后单击&#x200B;**[!UICONTROL Upload]**。

**[!UICONTROL Title]：**&#x200B;吸引观众的引人注目的标题。

**[!UICONTROL Description]：**&#x200B;广告正文。 最大长度为100个字符。

**[!UICONTROL Landing Page]：**&#x200B;查看者在单击广告时登陆的URL。

**[!UICONTROL Final Landing Page]：**&#x200B;插入了包含必要的[Advertising DSP跟踪宏](/help/dsp/campaign-management/macros.md)的[!UICONTROL Landing Page] URL（如果适用）。

**[!UICONTROL Sponsored By (Advertiser Name)]：**&#x200B;广告的广告商。

**[!UICONTROL Call to Action]：**（可选）您希望查看者在看到此广告后执行的步骤。

**[!UICONTROL Advertiser Logo]：**（可选）要包含在广告中的1:1比例徽标，以提高品牌知名度。 单击&#x200B;**[!UICONTROL Browse]**&#x200B;并在您的设备或网络上找到该文件，然后单击&#x200B;**[!UICONTROL Upload]**。

### [!UICONTROL Pixel]

投放位置的所有现有事件跟踪像素都会自动附加。 您可以根据单个广告的跟踪需求，分离现有像素并根据需要创建新像素。 **提示：**&#x200B;要使用[!UICONTROL Ad Tools]视图在投放位置中一次编辑多个广告的第三方跟踪像素，请参阅“[将第三方跟踪像素附加到投放位置中的广告](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads)”。

以下设置适用于创建或编辑的每个像素。

**[!UICONTROL Integration Event]：**&#x200B;触发像素触发的事件。 对于此广告类型，唯一的选项是&#x200B;*[!UICONTROL Impression]*。

**[!UICONTROL Pixel Type]：**&#x200B;像素是&#x200B;*[!UICONTROL IMG URL]* （1x1像素图像文件）、*[!UICONTROL HTML]*&#x200B;还是&#x200B;*[!UICONTROL JavaScript URL]*。

**[!UICONTROL Pixel URL or Code]：**&#x200B;像素图像的URL，采用指定[!UICONTROL Pixel Type]的相应格式。

**[!UICONTROL Pixel Name]：**&#x200B;像素名称。 使用有助于您轻松识别像素的名称。

**[!UICONTROL Pixel Provider]：**&#x200B;像素提供程序： *[!UICONTROL None]*、*[!UICONTROL Comscore]*、*[!UICONTROL WhiteOps]*&#x200B;或&#x200B;*[!UICONTROL IAS]*。

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建单个Ad](ad-create.md)
>* [列出与广告关联的版面](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [广告规范](ad-specs.md)
>* [DSP宏](/help/dsp/campaign-management/macros.md)
