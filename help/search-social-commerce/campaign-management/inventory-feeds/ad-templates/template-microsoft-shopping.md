---
title: ’[!DNL Microsoft Ads] 库存源的购物广告模板设置
description: 引用设置 [!DNL Microsoft Ads] 库存源的购物广告模板。
exl-id: a0dd6542-0516-406a-b8c5-2e102ec7ab3d
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# [!DNL Microsoft Ads] 库存源的购物广告模板设置

使用购物广告模板配置购物广告。

>[!NOTE]
>
>* 以下字符是模板中用于指定列名和修改量名称的保留字符，因此禁止在所有属性字段中作为文本：  `[ ] < > `


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

**[!UICONTROL Campaign Tracking Template]：** （对于客户端信息源文件的模板而言，它是可选项）营销活动级别的跟踪模板，它指定所有离登陆域重定向和跟踪参数，并将最终URL嵌入到参数中。 此值将覆盖帐户级别的设置，但更细粒度级别（使用关键字作为最细粒度级别）的跟踪模板将覆盖此值。

* 用于Adobe Advertising转化跟踪，当促销活动设置包括&#39;&#39;时应用[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]，请执行下列操作之一：

   * （推荐）使用 [Microsoft购物营销活动的跟踪模板格式](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md). 如果整个帐户专门用于购物广告，则您可以在帐户级别定义跟踪模板。

   * 如果您改为使用“”在信息源中包含每个产品的值[!DNL bingads_redirect]”列(使用 [正确格式](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md))，然后输入参数 `{lpurl}`. 您可以选择将第三方重定向和跟踪添加到 `{lpurl}` 参数。

* 对于第三方重定向和跟踪，请输入一个值。

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]：** 其产品用于营销活动的商家帐户的客户ID。

**[!UICONTROL Sales Country]：** 促销活动产品销售的国家/地区。 由于产品与目标国家/地区相关联，因此此设置确定在营销活动中广告的产品。

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

**[!UICONTROL Campaign Priority]：** 当多个营销活动广告相同产品时，营销活动的使用优先级： *[!UICONTROL Low]* （新营销活动的默认值）， *[!UICONTROL Medium]*，或 *[!UICONTROL High]*. 如果同一产品包含在多个促销活动中，广告网络会首先使用促销活动优先级来确定哪个促销活动（及相关竞价）符合广告竞价的条件。 如果所有促销活动具有相同的优先级，则具有最高竞价的促销活动符合条件。

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]：** （可选）广告组级别的跟踪模板，用于指定所有离登陆域重定向和跟踪参数，并将最终URL嵌入到参数中。 此值将覆盖帐户级别和营销活动级别的设置，但更细粒度级别的跟踪模板将覆盖此值。

对于Adobe Advertising转化跟踪，无需输入值。 营销活动级别的值就足够了。

对于第三方重定向和跟踪，请输入一个值。

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]：** 默认、包含所有内容的产品组“[!UICONTROL All products]“ 您无法删除此父产品组，但当馈送中缺少所有较低层时，将会自动删除该父产品组。

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]：** （没有子产品组的设备；可选）产品组的跟踪模板，它指定所有离岸域重定向和跟踪参数，并将最终URL嵌入到 [!DNL ValueTrack] 参数。 此模板将覆盖更高级别的模板。

对于Adobe Advertising转化跟踪，无需输入值。 营销活动级别的值就足够了。

对于第三方重定向和跟踪，请输入一个值。

**[!UICONTROL Initial Bid]：** 每个广告的初始出价。

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [关于使用库存信息源自动化广告管理](../inventory-feeds-about.md)
>* [管理修饰符](../modifiers-manage.md)
>* [管理清单数据馈送文件](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [通过模板传播馈送数据](../feed-data-propagate.md)
>* [将活动数据从库存馈送发布到广告网络](../propagated-data-post.md)
