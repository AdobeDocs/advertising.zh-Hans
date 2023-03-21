---
title: Adobe与Adobe Analytics的广告集成
description: 了解Adobe广告如何与Adobe Analytics交换数据，以及如何在搜索、社交和商务中使用数据。
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: def6a3a8d1de1f9f80dee6ecd1a18667afc79fd3
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Adobe与Adobe Analytics的广告集成

您可以通过以下方式将Adobe广告与Analytics集成。

## 之间交换数据 [!A分析] 和Adobe广告

### 拉取 [!A分析] 数据到Adobe广告

使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] 和DSP拉入：

* **[!DNL Analytics]区段：**  在中创建的所有广告商或代理区段的元数据、层次结构数据和唯一受众数据 [!DNL Analytics] 和发布到Experience Cloud。

* **[!DNL Analytics]网站参与量度**

* **[!DNL Analytics]标准、自定义和保留量度**

### 将Adobe广告数据发送到 [!A分析]

* **来自Adobe广告的流量量度**

* **Dimension自Adobe广告**

>[!NOTE]
>
>对于 [!DNL Search, Social, & Commerce]，则大多数广告网络和营销活动类型都支持此功能。 请参阅 [!DNL Search, Social, & Commerce] 指南以了解更多信息。<!-- add link when that's published in ExL -->

### 使用 [!DNL Analytics] 要创建的区段 [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*已选择加入的广告商，具有 [!DNL Advertising Search, Social, & Commerce] 仅*

<!-- Verify all -->

在 [!DNL Search, Social, & Commerce]，您可以创建 [!DNL Google Ads] Google客户使用您现有的 [!DNL Analytics] 区段。 这包括发布到Adobe Experience Cloud的Adobe Analytics区段以及使用Adobe Experience Cloud创建的区段 [!DNL Audience Library]. 有关更多信息，请参阅 [!DNL Search, Social, & Commerce].

[客户匹配来自用户ID的受众](https://support.google.com/google-ads/answer/9199250) 与基于网站标签的受众类似，但会将非PII ID分配给独特受众成员，以获得比标准客户匹配和基于网站标签的受众更显着的优势。

要创建必要的用户ID，您必须使用Adobe广告JavaScript标记 <!-- with a user ID parameter -->在您的网站上。 有关更多信息，请联系您的Adobe客户团队。

![区段创建过程](/help/integrations/assets/ad_search_user_id_pic.png)

创建受众后，即可在 [!DNL Google Ads] 营销活动 [营销活动级别或广告组级别的目标或排除项](#audience-manager-targets).

### 使用 [!DNL Analytics] 要定位或排除广告的区段 {#analytics-targets}

* (已选择加入的广告商， [!DNL Search, Social, & Commerce])您可以使用 [!DNL Google Ads] 受众 [使用 [!DNL Analytics] 区段](#audience-manager-google-audiences) 作为营销活动级别或广告组级别的目标或排除项 [!DNL Google Ads] 营销活动。

* (使用DSP的广告商)您可以使用现有 [!DNL Analytics] 区段作为广告投放的目标。 您可以选择将区段包含在可重复使用的受众中，以将其用作多个版面的目标或排除项。

* （具有广告创意的广告商）您可以使用现有 [!DNL Analytics] 区段作为广告体验中特定创意的目标。
