---
title: Adobe Advertising与Adobe Audience Manager的集成
description: 了解Adobe Advertising与Adobe Audience Manager交换数据的各种方式。
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
TQID: https://experienceleague.adobe.com/4O4O-DmHhClvSiOSxM9blAEvVslzYzRobEyU6RGeMEQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
  - id: f2860a4b-f905-4545-bead-1bbc92564592
subfeature_v2:
  - id: d1e2786d-1070-4f97-93d7-f5b95de25b2b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 517
ht-degree: 0%

---

# Adobe Advertising与Adobe Audience Manager的集成

您可以通过以下方式将Adobe Advertising与Audience Manager集成。

## 同步Audience Manager和其他[!DNL Adobe]区段以进行广告定位

[!DNL Search, Social, & Commerce]和DSP可以为广告商或代理的所有受众和其他[!DNL Adobe]受众拉入元数据、层次结构数据和唯一受众数据。 此唯一连接仅适用于使用Adobe Advertising的营销人员。 请参阅“[导入Adobe Audience Manager区段以进行广告定位](/help/integrations/audience-manager/import-audiences.md)”。

### 使用Audience Manager和其他[!DNL Adobe]区段创建[!DNL Google Ads]受众 {#audience-manager-google-audiences}

*仅使用[!DNL Advertising Search, Social, & Commerce]的已选择加入广告商*

在[!DNL Search, Social, & Commerce]内，您可以使用现有Audience Manager区段（将[!UICONTROL Adobe Media Optimizer (HTTP)]和[!UICONTROL Adobe Media Optimizer Batch Destination]作为目标）从用户ID创建[!DNL Google Ads]客户匹配受众。 （[!DNL Media Optimizer]是以前的[!DNL Search, Social, & Commerce]名称。） 这包括发布到Adobe CX Enterprise的Adobe Analytics区段和使用Adobe CX Enterprise [!DNL Audience Library]创建的区段。 有关详细信息，请参阅“从 [!DNL Adobe] 受众[&#128279;](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)创建 [!DNL Google Ads] 客户匹配受众”。

[用户ID中的客户匹配受众](https://support.google.com/google-ads/answer/9199250)类似于基于网站标记的受众，但会将非PII ID分配给唯一的受众成员，以便获得优于标准客户匹配和基于网站标记的受众的独特优势。

要创建必要的用户ID，您必须在您的网站上使用Adobe Advertising JavaScript标记<!-- with a user ID parameter -->。 有关更多信息，请与您的Adobe客户团队联系。

![区段创建流程](/help/integrations/assets/ad_search_user_id_pic.png)

创建受众后，您可以在[!DNL Google Ads]个营销活动中将其用作[营销活动级别或广告组级别的目标或排除项](#audience-manager-targets)。

### 使用Audience Manager和其他[!DNL Adobe]区段来定位或排除广告 {#audience-manager-targets}

* （已选择使用[!DNL Search, Social, & Commerce]的广告商）您可以使用任何[!DNL Google Ads]受众，这些受众是[使用 [!DNL Adobe] 区段](#audience-manager-google-audiences)创建的，并在[!DNL Google Ads]营销活动中用作营销活动级别或广告组级别的目标或排除项。

* （使用DSP的广告商）您可以将现有[!DNL Adobe]区段用作广告投放的目标。 You can optionally include the segments in reusable audiences, which you can use as targets or exclusions for multiple placements.

* (Advertisers with Advertising Creative) You can use your existing [!DNL Adobe] segments as targets for specific creatives in your ad experiences.

>[!NOTE]
>
>For more information about how to create audiences in the Audience Manager and Adobe CX Enterprise [!DNL Audience Library] interfaces, and common use cases for different audience types, see &quot;[Audience creation options](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## Send DSP media exposure data to Audience Manager

*Advertisers with DSP only*

DSP customers with Adobe Audience Manager can capture data from ad campaigns using pixel calls to Audience Manager. You can then use the campaign data to build rule-based traits, which you can use to define new segments to enable various DSP use cases, such as more advanced segmentation, frequency management, marketing analytics, and reporting insights.

See &quot;[Overview of sending DSP media exposure data to Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; for more information.

## Get richer insights into site activity with Audience Analytics

Adobe Advertising customers with [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) can send both Adobe Advertising-tracked data and Audience Manager segments to [!DNL Analytics] for enriched insights about site activity.

For more information, see &quot;[[!DNL Adobe Audience Analytics] for Adobe Advertising customers](/help/integrations/audience-manager/audience-analytics.md).&quot;
