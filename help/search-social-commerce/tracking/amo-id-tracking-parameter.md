---
title: AMO ID (s_kwcid)跟踪参数
description: 了解用于与Adobe Analytics共享Adobe Advertising数据的跟踪参数。
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: a150a55fd8d97db83cc269c787a1c67d557b7e3a
workflow-type: tm+mt
source-wordcount: '250'
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

有关DSP和Search、Social和Commerce的AMO ID格式，请参阅“[使用的Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id)“

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [使用的Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* [管理广告网络帐户](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [百度营销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Google Ads促销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Microsoft Advertising campaign设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [雅虎！ 日本广告促销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Yandex营销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
