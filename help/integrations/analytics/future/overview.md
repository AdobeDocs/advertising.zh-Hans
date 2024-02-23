---
title: Adobe Advertising与Adobe Analytics的集成
description: 了解Adobe Advertising如何与Adobe Analytics交换数据，以及如何使用Search、Social和Commerce中的数据。
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 78f69587771d9e72eb137f1e0866d782ed5c4d01
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Adobe Advertising与Adobe Analytics的集成

您可以通过以下方式将Adobe Advertising与Analytics集成。

## 在之间交换数据 [!DNL Analytics] 和Adobe Advertising

### 提取 [!DNL Analytics] 将数据导入Adobe Advertising

替换为 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)，[!DNL Search, Social, & Commerce] 和DSP拉入：

* **[!DNL Analytics]区段：**  在中创建的所有广告商或代理区段的元数据、层次结构数据和唯一受众数据 [!DNL Analytics] 并发布到Experience Cloud。

* **[!DNL Analytics]网站参与量度**

* **[!DNL Analytics]标准、自定义和保留量度**

### 将Adobe Advertising数据发送到 [!DNL Analytics]

* **来自Adobe Advertising的流量量度**

* **来自Adobe Advertising的Dimension**

>[!NOTE]
>
>对象 [!DNL Search, Social, & Commerce]中，大多数广告网络和营销活动类型支持此功能。 请参阅 [!DNL Search, Social, & Commerce] 指南，以了解更多信息。<!-- add link when that's published in ExL -->

### 使用 [!DNL Analytics] 要创建的区段 [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*已选择加入的广告商 [!DNL Advertising Search, Social, & Commerce] 仅限*

<!-- Verify all -->

范围 [!DNL Search, Social, & Commerce]，您可以创建 [!DNL Google Ads] Google客户使用您现有的根据用户ID匹配受众 [!DNL Analytics] 区段。 这包括发布到Adobe Experience Cloud的Adobe Analytics区段和使用Adobe Experience Cloud创建的区段 [!DNL Audience Library]. 有关更多信息，请参阅&quot;[创建 [!DNL Google Ads] 客户匹配受众来自 [!DNL Adobe] 受众](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)“

[通过用户ID匹配客户受众](https://support.google.com/google-ads/answer/9199250) 类似于基于网站标记的受众，但会将非PII ID分配给独特受众成员，以实现与标准客户匹配和基于网站标记的受众相比明显的优势。

要创建必要的用户ID，您必须使用Adobe Advertising的JavaScript标记 <!-- with a user ID parameter -->在您网站上。 有关更多信息，请与您的Adobe客户团队联系。

![区段创建过程](/help/integrations/assets/ad_search_user_id_pic.png)

创建受众后，您便可以在以下位置使用它们 [!DNL Google Ads] 营销活动作为 [营销活动级别或广告组级别的目标或排除项](#audience-manager-targets).

### 使用 [!DNL Analytics] 要定位或排除广告的区段 {#analytics-targets}

* (选择加入的广告商，具有 [!DNL Search, Social, & Commerce])您可以使用任何 [!DNL Google Ads] 受众属于 [创建方式 [!DNL Analytics] 区段](#audience-manager-google-audiences) 作为营销活动级别或广告组级别的目标或排除项，在 [!DNL Google Ads] 营销活动。

* (使用DSP的广告商)您可以使用现有的 [!DNL Analytics] 区段作为广告投放的目标。 您可以选择将区段包含在可重用受众中，将其用作多个投放位置的定位或排除项。

* (具有Advertising Creative的广告商)您可以使用现有的 [!DNL Analytics] 区段用作广告体验中特定创意人员的目标。
