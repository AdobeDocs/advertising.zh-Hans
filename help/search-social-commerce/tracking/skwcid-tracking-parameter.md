---
title: AMO ID (s_kwcid)跟踪参数
description: 了解用于与Adobe Analytics共享Adobe Advertising数据的跟踪参数。
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: 47cb00bc456601ef943c37de14a2047220f756f1
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# AMO ID (s_kwcid)跟踪参数

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs."  But I'll need to update with when/where to add the code for DSP clients. -->

Adobe AdvertisingAdobe Analytics使用AMO ID附加参数(也称为 `s_kwcid` 参数，它由广告渠道和广告网络特定的元素组成。

<!-- add everything below to IDs page -->

参数可通过以下方式之一添加到您的跟踪URL中：

* （推荐）已实施服务器端插入功能。

  对象 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 帐户具有 [!UICONTROL Auto Upload] 为帐户或营销活动启用的设置，当最终用户单击广告时，像素服务器会自动将AMO ID参数附加到您的登陆页面后缀 <!-- click a search ad or views a display ad --> Adobe Advertising像素。

  对于其他广告网络，或 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 帐户具有 [!UICONTROL Auto Upload] 禁用设置，可手动将AMO ID参数添加到帐户级别的附加参数，以便将其附加到基本URL。

* <!-- (Search, Social, & Commerce only) -->未实施服务器端插入功能，您需要手动将AMO ID参数添加到([!DNL Google Ads] 和 [!DNL Microsoft Advertising])登陆页面后缀或（其他广告网络）帐户级别的附加参数。

要实施服务器端插入功能，或确定最适合您企业的选项，请与您的Adobe客户团队联系。

## Advertising DSP广告的AMO ID格式

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

其中：

* `AC` 指示显示渠道。

* `{TM_AD_ID}` 是字母数字广告键。

* `{TM_PLACEMENT_ID}` 是字母数字放置键。

## 搜索、社交和商务广告的AMO ID格式

这些参数因广告网络而异，但以下参数是所有参数共有的：

* `AL` 指示搜索渠道。 <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` 是分配给广告商的唯一用户ID。

* `{sid}` 将由广告商广告网络帐户的数值ID替换： *3* 对象 [!DNL Google Ads]， *10* 对象 [!DNL Microsoft Advertising]， *45* 对象 [!DNL Meta]， *86* 对象 [!DNL Yahoo! Display Network]， *87* 对象 [!DNL Naver]， *88* 对象 [!DNL Baidu]， *90* 对象 [!DNL Yandex]， *94* 对象 [!DNL Yahoo! Japan Ads]， *105* 对象 [!DNL Yahoo Native] （已弃用），或 *106* 对象 [!DNL Pinterest] （已弃用）。

### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

### [!DNL Google Ads]

其中包括使用的购物营销活动 [!DNL Google Merchant Center].

* 使用最新AMO ID格式（支持营销活动和广告组级别报表以实现最佳效果营销活动以及草稿和实验营销活动）的帐户：

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* 所有其他帐户：

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

>[!NOTE]
>
>* 对于动态搜索广告， {keyword} 使用自动定位填充。
>* 在为生成跟踪时 [!DNL Google] 购物广告、产品ID参数、 `{adwords_producttargetid}`，，插入在keyword参数之前。 产品ID参数未出现在 [!DNL Google Ads] 帐户级别和促销活动级别的跟踪参数。
>* 要使用最新的AMO ID跟踪代码，请参阅[更新的AMO ID跟踪代码 [!DNL Google Ads] 帐户](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)“ <!-- Update terminology there too. -->

<!--

### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

### [!DNL Microsoft Advertising]

* 搜索促销活动：

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* 购物营销活动(使用 [!DNL Microsoft Merchant Center])：

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* 受众网络营销活动：

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [管理广告网络帐户](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [百度营销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Google Ads促销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Microsoft Advertising campaign设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [雅虎！ 日本广告促销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Yandex营销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
