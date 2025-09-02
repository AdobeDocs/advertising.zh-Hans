---
title: Customer Journey Analytics中的Adobe Advertising量度和维度
description: 引用Customer Journey Analytics中可用的Adobe Advertising指标和维度。
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: 519d1ac2269e5ebaf8cc90a15b0eb421f8187229
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Customer Journey Analytics中的Adobe Advertising量度和维度

*仅集成Adobe Advertising-Customer Journey Analytics的广告商*

>[!NOTE]
>
>* Adobe Advertising每天将流量指标和维度传递给[!DNL Customer Journey Analytics]。
>* [!DNL Web SDK]实时捕获Adobe Advertising点进和显示点进，并将其传递给Customer Journey Analytics。

## Adobe Advertising流量量度

<!-- Verify column names -->

>[!NOTE]
>
>* 
>* “XDM字段名称”是Adobe Experience Platform中的字段名称。
>* “XDM字段显示名称”表示Customer Journey Analytics中的显示名称。

| Adobe Advertising字段名称 | XDM字段名称 | XDM字段显示名称 | Source |
|------------------------------|----------------|------------------------|--------|
| 日期 | 日期 | 全部 | |
| AMO ID | skwcid | ADOBE ADVERTISING ID | 全部 |
| AMO展示 | adobe_advertising_impressions | Adobe Advertising展示次数 | 全部 |
| AMO点击量 | adobe_advertising_clicks | Adobe Advertising单击次数 | 全部 |
| AMO成本 | adobe_advertising_cost | Adobe Advertising成本 | 全部 |
| 货币代码 | 货币 | 货币 | 全部 |
| AMO查看 | adobe_advertising_views | Adobe Advertising查看 | Ad Cloud DSP |
| AMO查看完成25% | adobe_advertising_views_25_pct | Adobe Advertising查看已完成25% | Ad Cloud DSP |
| AMO查看完成50% | adobe_advertising_views_50_pct | Adobe Advertising查看已完成50% | Ad Cloud DSP |
| AMO查看完成75% | adobe_advertising_views_75_pct | Adobe Advertising查看已完成75% | Ad Cloud DSP |
| AMO查看100%完成 | adobe_advertising_views_100_pct | Adobe Advertising查看100%完成 | Ad Cloud DSP |
| AMO查看分钟数 | adobe_advertising_minutes_viewed | Adobe Advertising查看分钟数 | Ad Cloud DSP |
| AMO可见展示次数 | adobe_advertising_viewable_impressions | Adobe Advertising可视展示次数 | Ad Cloud DSP |
| AMO不可查看的展示次数 | adobe_advertising_not_viewable_impressions | Adobe Advertising不可查看的展示次数 | Ad Cloud DSP |
| AMO可衡量的展示次数 | adobe_advertising_measurement_impressions | Adobe Advertising可衡量的展示次数 | Ad Cloud DSP |

<!--
| Adobe Advertising Landing Page Views | adobe_advertising_landing_page_views | Adobe Advertising Landing Page Views | Meta Only |
| Adobe Advertising App Events | adobe_advertising_app_events | Adobe Advertising App Events | Meta Only |
| Adobe Advertising Engagements | adobe_advertising_engagements | Adobe Advertising Engagements | Meta Only |
| Adobe Advertising Ad Platform Conversions | adobe_advertising_ad_platform_conversions | Adobe Advertising Ad Platform Conversions | Meta Only |
| Adobe Advertising App Installs | adobe_advertising_app_installs | Adobe Advertising App Installs | Meta Only |
| Adobe Advertising Ad Platform Conversion Value | adobe_advertising_ad_platform_conversion_value | Adobe Advertising Ad Platform Conversion Value | Meta Only |
| Adobe Advertising Ad Platform Leads | adobe_advertising_ad_platform_leads | Adobe Advertising Ad Platform Leads | Meta Only |
| Adobe Advertising Page Like | adobe_advertising_page_like | Adobe Advertising Page Like | Meta Only |
| Adobe Advertising Phone Calls | adobe_advertising_phone_calls | Adobe Advertising Phone Calls | Meta Only |
| Adobe Advertising Messages | adobe_advertising_messages | Adobe Advertising Messages | Meta Only |
-->

## Adobe Advertising维度

>[!NOTE]
>
>* “XDM字段”是Adobe Experience Platform中的字段名称。
>* “XDM字段显示名称”表示Customer Journey Analytics中的显示名称。

| Adobe Advertising字段名称 | XDM字段名称 | XDM字段显示名称 | Source |
|------------------------------|----------------|------------------------|--------|
| 键 | skwcid | ADOBE ADVERTISING ID |
| 广告平台 | adobe_advertising_ad_platform | Adobe Advertising广告平台 |
| 帐户 | adobe_advertising_account | Adobe Advertising帐户 |
| 营销活动 | adobe_advertising_campaign | Adobe Advertising Campaign |
| 广告组 | adobe_advertising_ad_group | Adobe Advertising广告组 |
| 关键词 | adobe_advertising_keyword | Adobe Advertising关键词 |
| 广告 | adobe_advertising_ad | Adobe Advertising广告 |
| 投放 | adobe_advertising_placement | Adobe Advertising投放位置 |
| 匹配类型 | adobe_advertising_match_type | Adobe Advertising匹配类型 |
| 广告标题 | adobe_advertising_ad_title | Adobe Advertising广告标题 |
| 广告描述 | adobe_advertising_ad_description | Adobe Advertising广告描述 |
| 广告目标URL | adobe_advertising_ad_destination_url | Adobe Advertising广告目标URL |
| 广告显示URL | adobe_advertising_ad_display_url | Adobe Advertising广告显示URL |
| 设备 | adobe_advertising_device | Adobe Advertising设备 |
| 关键字MatchType | adobe_advertising_keyword_matchtype | Adobe Advertising关键字MatchType |
| 网络 | adobe_advertising_network | Adobe Advertising网络 |
| 广告类型 | adobe_advertising_ad_type | Adobe Advertising广告类型 |
| 产品目标 | adobe_advertising_product_target | Adobe Advertising产品目标 |
| 登陆类型 | adobe_advertising_landing_type | Adobe Advertising登录类型 |
| 优化 | adobe_advertising_optimization | Adobe Advertising优化 |

>[!MORELIKETHIS]
>
>* [概述](overview.md)
>* [先决条件](prerequisites.md)
>* [使用的 [!DNL Customer Journey Analytics]](ids.md)Adobe Advertising ID
>* [设置数据收集、数据传输和报告](set-up.md)
