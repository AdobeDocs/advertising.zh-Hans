---
title: '[!DNL Microsoft Advertising]响应式广告设置'
description: 引用 [!DNL Microsoft Advertising] 响应式广告的设置。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 730b474b83ae4df47c18f93adfec62b1dc9b8a16
workflow-type: tm+mt
source-wordcount: 243
ht-degree: 0%

---

# [!DNL Microsoft Advertising]个响应式（受众）广告设置

响应式广告格式可用于[!DNL Microsoft Audience Network]上基于图像、基于视频和已连接的电视视频的受众广告。 广告网络使用最有效的广告元素组合来动态组合响应式广告。

## [!UICONTROL Basic Settings]

*仅限新广告*

**[!UICONTROL Network]：**&#x200B;广告网络。

**[!UICONTROL Account]：**&#x200B;广告网络帐户。

**[!UICONTROL Campaign]：**&#x200B;营销活动。

**[!UICONTROL Ad Group]：**&#x200B;广告组。

## [!UICONTROL Audience CTV Video Ad Details]

<!-- I can't find a video ad -- this same header is used for image ads. Need to verify the video ad settings and when you'll get them -->

### 视频广告

**[!UICONTROL Videos]：**&#x200B;一个视频广告的URL。

**[!UICONTROL Status]：**&#x200B;广告状态： *[!UICONTROL Active]*&#x200B;或&#x200B;*[!UICONTROL Paused]*。

### 图像广告)

>[!NOTE]
>
>广告网络会自动为受众营销活动创建广告，并使用商店的产品信息和广告组级别的用户定位链接到商家中心商店。 您无需手动创建广告。

**[!UICONTROL Images]：**&#x200B;广告的最多15个JPEG或PNG图像。 包括至少一个具有1.91:1纵横比的图像。 查看[受众广告图像](https://help.ads.microsoft.com/#apex/ads/en/56912/0)所允许的宽高比和尺寸。

对于受众广告，[!DNL Microsoft Advertising]会针对所有可能的纵横比自动裁剪此图像。

<!-- Instructions -->

{{$include /help/_includes/images-ms-multimedia-responsive-ad.md}}

**[!UICONTROL Business Name]：**&#x200B;业务名称，最多25个字符。 它可以用在仅限调用的广告格式中。

**[!UICONTROL Short Headlines]：**&#x200B;至少3个（最多15个）简短标题，其中至少一个单词，每个单词最多为30个字符。

**[!UICONTROL Long Headlines]：**&#x200B;至少3个、最多5个长标题，每个标题最多90个字符。

**[!UICONTROL Ad Text]：**&#x200B;至少有两个（最多四个）描述，每个描述中至少有一个单词，最多有90个字符。

**[!UICONTROL Status]：**&#x200B;广告状态： *[!UICONTROL Active]*&#x200B;或&#x200B;*[!UICONTROL Paused]*。

## [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [管理广告](/help/search-social-commerce/new-ui/manage/ads/ad-manage.md)
