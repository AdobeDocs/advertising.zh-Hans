---
title: AMO ID (s_kwcid)跟踪参数
description: 了解用于与Adobe Analytics共享Adobe Advertising数据的跟踪参数。
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: 3c91d0a764397fd72192f5a522ac936176047bc2
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# AMO ID (s_kwcid)跟踪参数

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs" once I've finalized content for DSP clients.  -->

Adobe AdvertisingAdobe Analytics使用AMO ID附加参数(也称为 `s_kwcid` 参数，它由广告渠道和广告网络特定的元素组成。

参数可通过以下方式之一添加到您的跟踪URL中：

* （推荐）已实施服务器端插入功能。

   * DSP客户：当最终用户查看带有Adobe Advertising像素的显示广告时，像素服务器会自动将s_kwcid参数附加到登陆页面后缀。

   * 搜索、社交和商务客户：

      * 对象 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 帐户具有 [!UICONTROL Auto Upload] 为帐户或营销活动启用的设置，当最终用户单击带有Adobe Advertising像素的广告时，像素服务器会自动将s_kwcid参数附加到您的登陆页后缀。

      * 对于其他广告网络，或 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 帐户具有 [!UICONTROL Auto Upload] 禁用设置，手动将参数添加到帐户级别的附加参数，以便将其附加到基本URL。

* 未实现服务器端插入功能：

   * DSP客户：

      * 对象 [!DNL Flashtalking] 添加标记，手动为每个&#39;&#39;插入其他宏[附加 [!DNL Analytics for Advertising] 宏到 [!DNL Flashtalking] 广告标记](/help/integrations/analytics/macros-flashtalking.md)“

      * 对象 [!DNL Google Campaign Manager 360] 添加标记，手动为每个&#39;&#39;插入其他宏[附加 [!DNL Analytics for Advertising] 宏到 [!DNL Google Campaign Manager 360] 广告标记](/help/integrations/analytics/macros-google-campaign-manager.md)“

  <!--  * For all other ads, XXXX. -->

   * 搜索、社交和商务客户：

      * 对于([!DNL Google Ads] 和 [!DNL Microsoft® Advertising])广告，请手动将AMO ID参数添加到登陆页面后缀。

      * 对于所有其他广告网络上的广告，请手动将AMO ID参数添加到帐户级别的附加参数，以便将其附加到基本URL。

要实施服务器端插入功能，或确定最适合您企业的选项，请与您的Adobe客户团队联系。

有关DSP和Search、Social和Commerce的AMO ID格式，请参阅“[使用的Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id)“

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [使用的Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* （搜索、社交和商务） [管理广告网络帐户](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* （搜索、社交和商务） [百度营销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* （搜索、社交和商务） [Google Ads促销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* （搜索、社交和商务） [Microsoft® Advertising campaign设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* （搜索、社交和商务） [雅虎！ 日本广告促销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* （搜索、社交和商务） [Yandex营销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
