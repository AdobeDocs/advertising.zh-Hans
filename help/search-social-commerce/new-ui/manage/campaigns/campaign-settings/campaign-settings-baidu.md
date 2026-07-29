---
title: '[!DNL Baidu]营销活动设置'
description: 引用 [!DNL Baidu] 营销活动的设置。
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 3a5c2507f3acb08419e143ba906cf55df2496d0f
workflow-type: tm+mt
source-wordcount: 309
ht-degree: 0%

---

# [!DNL Baidu]营销活动设置

## \[页面顶部]

**[!UICONTROL Campaign Name]：**&#x200B;帐户中唯一的促销活动名称。

**[!UICONTROL Status]：**&#x200B;促销活动的显示状态： *活动*&#x200B;或&#x200B;*已暂停*。 新广告营销活动的默认值为&#x200B;*活动*。

## [!UICONTROL Basic Settings]选项卡

*仅新营销活动*

**[!UICONTROL Network]：**&#x200B;广告网络。

**[!UICONTROL Account]：**&#x200B;广告网络帐户。

**[!UICONTROL Campaign Type]：**&#x200B;广告的放置位置以及促销活动可能包含的广告类型。 唯一的选项是&#x200B;*仅搜索网络*。

## [!UICONTROL Campaign Details]选项卡

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Contains EU Political Ads]：**(适用于针对欧盟(EU)受众的营销活动)根据欧盟第2024/90号条例在欧盟提供的广告要求，营销活动是否包含政治广告： *[!UICONTROL Yes]*&#x200B;或&#x200B;*[!UICONTROL No]*。

## [!UICONTROL Budget Options]选项卡

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

<!--VERIFY OPTIMIZATION BEHAVIOR -->**[!UICONTROL Bid strategy]：**&#x200B;营销活动的竞价策略：

* *[!UICONTROL Maximize Conversions]：*&#x200B;广告网络（而不是Search、Social和Commerce）会优化竞价以最大限度地提高转化率。 （可选）输入&#x200B;**[!UICONTROL Target CPA]**（每次购置成本）。 **注意：**&#x200B;请将此选项用于具有营销活动级别优化的项目组合中的营销活动。 在包含营销活动级优化的组合中， Search、Social和Commerce可优化Target CPA。

* *[!UICONTROL Maximize Conversion Value]：*&#x200B;广告网络（而不是Search、Social和Commerce）会优化竞价以最大限度地提高转化值。 （可选）输入&#x200B;**[!UICONTROL Target Return on Ad Spend]** (ROAS)作为百分比。 **注意：**&#x200B;请将此选项用于具有营销活动级别优化的项目组合中的营销活动。 在包含营销活动级优化的组合中， Search、Social和Commerce可优化Target ROAS。

## [!UICONTROL Campaign Targeting]选项卡

**[!UICONTROL Languages]：**&#x200B;广告的语言，它应该与您的广告可以显示的网站的语言匹配。 广告网络从各种信号确定用户的语言，包括用户的查询、发布者的国家和用户的语言设置。

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

## [!UICONTROL Additional Campaign Information]选项卡

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-baidu.md}}

### [!UICONTROL Campaign Tracking]选项卡

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]：** （仅适用于[!UICONTROL EF Redirect]）通过添加重定向（相关时）并将参数附加到相关URL来跟踪点击次数和收入的级别：

* *[!UICONTROL Keyword]：*&#x200B;只跟踪关键字级别的数据。

* *[!UICONTROL Creative]：*&#x200B;仅跟踪广告（创意）级别的数据。

* *[!UICONTROL Creative and Keyword]：*&#x200B;在广告（创意）和关键词级别跟踪数据。

**[!UICONTROL Enable conversion reporting in Adobe Analytics]：**&#x200B;向帐户或促销活动中的广告添加URL参数，以进行转化跟踪。

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

<!--

Not there as of 7/22 -- what's going on here? If we're removing it, then I need to update many references throughout the whole doc:

[               **[!UICONTROL Auto Upload]:**      ]

{{$include /help/_includes/auto-upload.md}}

-->

>[!MORELIKETHIS]
>
>* [管理营销活动](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
