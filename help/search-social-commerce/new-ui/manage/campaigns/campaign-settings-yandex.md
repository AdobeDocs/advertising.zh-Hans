---
title: '[!DNL Yandex]营销活动设置'
description: 引用 [!DNL Yandex] 营销活动的设置。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: d45eb490f9dbb7da89bd1270582e5548b70cbd31
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 0%

---

# [!DNL Yandex]营销活动设置

## \[页面顶部]

**[!UICONTROL Campaign Name]：**&#x200B;帐户中唯一的促销活动名称。

**[!UICONTROL Status]：**&#x200B;促销活动的显示状态： *活动*&#x200B;或&#x200B;*已暂停*。 新广告营销活动的默认值为&#x200B;*活动*。

## [!UICONTROL Basic Settings]选项卡

*仅新营销活动*

**[!UICONTROL Network]：**&#x200B;广告网络。

**[!UICONTROL Account]：**&#x200B;广告网络帐户。

**[!UICONTROL Campaign Type]：**&#x200B;广告的放置位置：

* *[!UICONTROL Search Network Only]：*&#x200B;在搜索网络上显示文本广告。 您必须为每个广告组指定关键字。

* *[!UICONTROL Search and Display Network]：*&#x200B;在搜索网络和[!DNL Yandex Advertising Network]上显示文本广告。 对于搜索广告，您必须为每个广告组指定搜索关键词。 对于显示广告，您必须为要在其中为每个广告组进行广告的网站指定关键字。

* *[!UICONTROL Display Network Only]：*&#x200B;在[!DNL Yandex Advertising Network]上显示文本广告。 对于每个广告组，您必须为要在其上进行广告的网站指定关键字。

## [!UICONTROL Campaign Details]选项卡

<!-- **[!UICONTROL Start date]:** -->

{{$include /help/_includes/start-date.md}}

## [!UICONTROL Budget Options]选项卡

**[!UICONTROL Budget]：**&#x200B;预算，这是您希望每日（平均）或在营销活动存留期花费的金额，具体取决于帐户的预算类型。 最低预算为6 300日元、10欧元或10美元。

**注释：**

* 新营销活动的竞价管理策略为“最高可用位置”。

* 根据搜索条件，如果您将此促销活动分配给配置为允许自动调整促销活动预算限制的项目组合，则您实际上可能在任何给定日、月或生命周期中花费的金额多于或少于指定的预算。

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

## [!UICONTROL Additional Campaign Information]选项卡

### [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]：** （仅适用于[!UICONTROL EF Redirect]；只读）应跟踪点击次数和收入的级别。 只有&#x200B;*[!UICONTROL Creative]*&#x200B;可用于[!DNL Yandex] — 仅在广告（创意）级别跟踪数据。

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
