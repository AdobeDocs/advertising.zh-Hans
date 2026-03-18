---
title: Adobe Advertising与Adobe Analytics的集成
description: 了解Adobe Advertising如何与Adobe Analytics交换数据，以及如何在Search、Social和Commerce中使用数据。
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 94a5b5591aef0aa5ae5d3459d547f52d939d559c
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Adobe Advertising与Adobe Analytics的集成

您可以通过以下方式将Adobe Advertising与Analytics集成。

## 在[!DNL Analytics]和Adobe Advertising之间交换数据

### 将[!DNL Analytics]数据提取到Adobe Advertising

通过[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)、[!DNL Search, Social, & Commerce]和DSP拉入：

* **[!DNL Analytics]区段：**&#x200B;在[!DNL Analytics]中创建并发布到Experience Cloud的所有广告商或代理区段的元数据、层次结构数据和独特受众数据。

* **[!DNL Analytics]网站参与量度**

* **[!DNL Analytics]个标准、自定义和保留的量度**

### 将Adobe Advertising数据发送到[!DNL Analytics]

* 来自Adobe Advertising的&#x200B;**流量指标**

* 来自Adobe Advertising的&#x200B;**维度**

>[!NOTE]
>
>对于[!DNL Search, Social, & Commerce]，大多数广告网络和营销活动类型都支持此功能。 有关详细信息，请参阅[!DNL Search, Social, & Commerce]指南中的“支持的清单”。<!-- add link when that's published in ExL -->

### 使用[!DNL Analytics]区段创建[!DNL Google Ads]受众 {#audience-manager-google-audiences}

*仅使用[!DNL Advertising Search, Social, & Commerce]的已选择加入广告商*

<!-- Verify all -->

在[!DNL Search, Social, & Commerce]内，您可以使用现有的[!DNL Google Ads]区段从用户ID创建[!DNL Analytics]个Google客户匹配受众。 这包括发布到Adobe Experience Cloud的Adobe Analytics区段和使用Adobe Experience Cloud [!DNL Audience Library]创建的区段。 有关详细信息，请参阅“从[受众 [!DNL Google Ads] 创建 [!DNL Adobe] 客户匹配受众”。](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)

[用户ID中的客户匹配受众](https://support.google.com/google-ads/answer/9199250)类似于基于网站标记的受众，但会将非PII ID分配给唯一的受众成员，以便获得优于标准客户匹配和基于网站标记的受众的独特优势。

要创建必要的用户ID，您必须在您的网站上使用Adobe Advertising JavaScript标记<!-- with a user ID parameter -->。 有关更多信息，请与您的Adobe客户团队联系。

![区段创建流程](/help/integrations/assets/ad_search_user_id_pic.png)

创建受众后，您可以在[!DNL Google Ads]个营销活动中将其用作[营销活动级别或广告组级别的目标或排除项](#audience-manager-targets)。

### 使用[!DNL Analytics]区段来定位或排除广告 {#analytics-targets}

* （已选择使用[!DNL Search, Social, & Commerce]的广告商）您可以使用任何[!DNL Google Ads]受众，这些受众是[使用 [!DNL Analytics] 区段](#audience-manager-google-audiences)创建的，并在[!DNL Google Ads]营销活动中用作营销活动级别或广告组级别的目标或排除项。

* （使用DSP的广告商）您可以将现有[!DNL Analytics]区段用作广告投放的目标。 您可以选择将区段包含在可重用受众中，将其用作多个投放位置的定位或排除项。

* （使用Advertising Creative的广告商）您可以将现有[!DNL Analytics]区段用作广告体验中特定创意人员的目标。
