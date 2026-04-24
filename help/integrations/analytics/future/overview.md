---
title: Adobe Advertising integrations with Adobe Analytics
description: Learn about how Adobe Advertising can exchange data with Adobe Analytics and how you can use the data within Search, Social, & Commerce.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Adobe Advertising integrations with Adobe Analytics

You can integrate Adobe Advertising with Analytics in the following ways.

## Exchange data between [!DNL Analytics] and Adobe Advertising

### Pull [!DNL Analytics] data into Adobe Advertising

With [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] and DSP pull in:

* **[!DNL Analytics]segments:**  Metadata, hierarchy data, and unique audience data for all of an advertiser&#39;s or agency&#39;s segments created in [!DNL Analytics] and published to Adobe CX Enterprise.

* **[!DNL Analytics]site engagement metrics**

* **[!DNL Analytics]standard, custom, and reserved metrics**

### Send Adobe Advertising data to [!DNL Analytics]

* **Traffic metrics from Adobe Advertising**

* **Dimensions from Adobe Advertising**

>[!NOTE]
>
>For [!DNL Search, Social, & Commerce], this feature is supported for most ad networks and campaign types. See &quot;Supported Inventory&quot; in the [!DNL Search, Social, & Commerce] Guide for more information.<!-- add link when that's published in ExL -->

### Use [!DNL Analytics] segments to create [!DNL Google Ads] audiences {#audience-manager-google-audiences}

*仅使用[!DNL Advertising Search, Social, & Commerce]的已选择加入广告商*

<!-- Verify all -->

Within [!DNL Search, Social, & Commerce], you can create [!DNL Google Ads] Google customer match audiences from user IDs using your existing [!DNL Analytics] segments. 这包括发布到Adobe CX Enterprise的Adobe Analytics区段和使用Adobe CX Enterprise [!DNL Audience Library]创建的区段。 有关详细信息，请参阅“从 [!DNL Adobe] 受众](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)创建 [!DNL Google Ads] 客户匹配受众”。[

[用户ID中的客户匹配受众](https://support.google.com/google-ads/answer/9199250)类似于基于网站标记的受众，但会将非PII ID分配给唯一的受众成员，以便获得优于标准客户匹配和基于网站标记的受众的独特优势。

要创建必要的用户ID，您必须在您的网站上使用Adobe Advertising JavaScript标记<!-- with a user ID parameter -->。 有关更多信息，请与您的Adobe客户团队联系。

![区段创建流程](/help/integrations/assets/ad_search_user_id_pic.png)

创建受众后，您可以在[!DNL Google Ads]个营销活动中将其用作[营销活动级别或广告组级别的目标或排除项](#audience-manager-targets)。

### Use [!DNL Analytics] segments to target or exclude ads {#analytics-targets}

* （已选择使用[!DNL Search, Social, & Commerce]的广告商）您可以使用任何[!DNL Google Ads]受众，这些受众是[使用 [!DNL Analytics] 区段](#audience-manager-google-audiences)创建的，并在[!DNL Google Ads]营销活动中用作营销活动级别或广告组级别的目标或排除项。

* （使用DSP的广告商）您可以将现有[!DNL Analytics]区段用作广告投放的目标。 You can optionally include the segments in reusable audiences, which you can use as targets or exclusions for multiple placements.

* (Advertisers with Advertising Creative) You can use your existing [!DNL Analytics] segments as targets for specific creatives in your ad experiences.
