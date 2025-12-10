---
title: 用于库存馈送的[!DNL Google Ads]购物广告模板设置
description: 参考 [!DNL Google Ads] 库存源的购物广告模板的设置。
exl-id: 36cbe719-f984-4456-8575-94b9d3e6094e
feature: Search Inventory Feeds
source-git-commit: c5739a7c3564f84c57500b54f17ca25591e09a43
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# 用于库存馈送的[!DNL Google Ads]购物广告模板设置

使用购物广告模板配置购物广告。

>[!NOTE]
>
>* 以下字符是为模板中的列名称和修饰符名称而保留的，因此禁止在所有属性字段中作为文本： `[ ] < > `

## \[所有选项卡上方\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[左侧面板\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

<!-- **[!UICONTROL Campaign Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-only.md}}

<!-- **[!UICONTROL Campaign Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-method.md}}

**[!UICONTROL Campaign Tracking Template]：** （对于客户端信息源文件的模板而言，它是可选的）营销活动级别的跟踪模板，它指定所有离登陆域重定向和跟踪参数，并将最终URL嵌入到参数中。 此值将覆盖帐户级别的设置，但更细粒度级别（使用关键字作为最细粒度级别）的跟踪模板将覆盖此值。

对于Adobe Advertising转化跟踪（在促销活动设置包括“[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]”时应用），请为Google广告购物促销活动使用[跟踪模板格式](/help/search-social-commerce/tracking/formats-click-tracking-google.md)。 如果整个帐户专门用于购物广告，则您可以在帐户级别定义跟踪模板。

对于第三方重定向和跟踪，请输入一个值。

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]：**&#x200B;其产品用于营销活动的商家帐户的客户ID。

**[!UICONTROL Sales Country]：**&#x200B;促销活动产品的销售国家/地区。 因为产品已关联
对于目标国家/地区，此设置确定在营销活动中广告的产品。

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Networks]：**&#x200B;要投放广告的网络。 已选择&#x200B;*[!UICONTROL Search]*。 要包括[!DNL Google Ads]搜索合作伙伴的列表竞价，请选中&#x200B;**[!UICONTROL Search partners]**&#x200B;旁边的复选框。

**[!UICONTROL Campaign Priority]：**&#x200B;多个营销活动广告
相同的产品： *[!UICONTROL Low]* （新营销活动的默认值）、*[!UICONTROL Medium]*&#x200B;或&#x200B;*[!UICONTROL High]*。 当同一产品包含在多个促销活动中时，广告网络会使用
首先确定哪个营销活动（及相关竞价）符合广告竞价条件的营销活动优先级。 如果所有促销活动具有相同的优先级，则具有最高竞价的促销活动符合条件。

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

**[!UICONTROL Has EU Political Ads]：**([!DNL Google Ads]和[!DNL Microsoft Advertising]营销活动仅适用针对欧盟(EU)受众的营销活动)根据欧盟第2024/90号条例在欧盟提供的广告要求，营销活动是否包含政治广告：*[!UICONTROL Yes]*&#x200B;或&#x200B;*[!UICONTROL No]*。

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]：**（可选）广告组级别的跟踪模板，它指定所有登入外域重定向和跟踪参数，并将最终URL嵌入到参数中。 此值将覆盖帐户级别和营销活动级别的设置，但更细粒度级别的跟踪模板将覆盖此值。

对于Adobe Advertising转化跟踪，您无需输入值。 营销活动级别的值就足够了。

对于第三方重定向和跟踪，请输入一个值。

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]：**&#x200B;默认的全包产品组“[!UICONTROL All products]”。 您无法删除此父产品组，但当馈送中缺少所有较低层时，将会自动删除该父产品组。

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]：** （不含子产品组的设备；可选）产品的跟踪模板
组，指定所有登入域重定向和跟踪参数，并将最终URL嵌入到[!DNL ValueTrack]参数中。 此模板将覆盖更高级别的模板。

对于Adobe Advertising转化跟踪，您无需输入值。 营销活动级别的值就足够了。

对于第三方重定向和跟踪，请输入一个值。

**[!UICONTROL Initial Bid]：**&#x200B;每个广告的初始出价。

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [关于使用库存信息源自动进行广告管理](../inventory-feeds-about.md)
>* [管理修饰符](../modifiers-manage.md)
>* [管理清单数据馈送文件](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [通过模板传播馈送数据](../feed-data-propagate.md)
>* [将来自库存馈送的促销活动数据发布到广告网络](../propagated-data-post.md)
