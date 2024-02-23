---
title: Adobe Advertising与Adobe Audience Manager的集成
description: 了解Adobe Advertising与Adobe Audience Manager交换数据的各种方式。
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: d0260fc3b10f1944b82cdc4c1e3b8137a695e05e
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Adobe Advertising与Adobe Audience Manager的集成

您可以通过以下方式将Adobe Advertising与Audience Manager集成。

## 同步Audience Manager及其他 [!DNL Adobe] 用于广告定位的区段

[!DNL Search, Social, & Commerce] 并且DSP可以拉入元数据、层次结构数据和唯一受众数据，以便用于广告商或代理机构的所有其他Audience Manager [!DNL Adobe] 受众。 此唯一连接仅适用于使用Adobe Advertising的营销人员。 请参阅&quot;[导入Adobe Audience Manager区段以进行广告定位](/help/integrations/audience-manager/import-audiences.md)“

### 使用Audience Manager和其他 [!DNL Adobe] 要创建的区段 [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*已选择加入的广告商 [!DNL Advertising Search, Social, & Commerce] 仅限*

范围 [!DNL Search, Social, & Commerce]，您可以创建 [!DNL Google Ads] Audience Manager客户匹配来自用户ID的受众，使用您具有 [!UICONTROL Adobe Media Optimizer (HTTP)] 和 [!UICONTROL Adobe Media Optimizer Batch Destination] 作为目标。 ([!DNL Media Optimizer] 是以前的名称 [!DNL Search, Social, & Commerce].) 这包括发布到Adobe Experience Cloud的Adobe Analytics区段和使用Adobe Experience Cloud创建的区段 [!DNL Audience Library]. 有关更多信息，请参阅&quot;[创建 [!DNL Google Ads] 客户匹配受众来自 [!DNL Adobe] 受众](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)“

[通过用户ID匹配客户受众](https://support.google.com/google-ads/answer/9199250) 类似于基于网站标记的受众，但会将非PII ID分配给独特受众成员，以实现与标准客户匹配和基于网站标记的受众相比明显的优势。

要创建必要的用户ID，您必须使用Adobe Advertising的JavaScript标记 <!-- with a user ID parameter -->在您网站上。 有关更多信息，请与您的Adobe客户团队联系。

![区段创建过程](/help/integrations/assets/ad_search_user_id_pic.png)

创建受众后，您便可以在以下位置使用它们 [!DNL Google Ads] 营销活动作为 [营销活动级别或广告组级别的目标或排除项](#audience-manager-targets).

### 使用Audience Manager和其他 [!DNL Adobe] 要定位或排除广告的区段 {#audience-manager-targets}

* (选择加入的广告商，具有 [!DNL Search, Social, & Commerce])您可以使用任何 [!DNL Google Ads] 受众属于 [创建方式 [!DNL Adobe] 区段](#audience-manager-google-audiences) 作为营销活动级别或广告组级别的目标或排除项，在 [!DNL Google Ads] 营销活动。

* (使用DSP的广告商)您可以使用现有的 [!DNL Adobe] 区段作为广告投放的目标。 您可以选择将区段包含在可重用受众中，将其用作多个投放位置的定位或排除项。

* (具有Advertising Creative的广告商)您可以使用现有的 [!DNL Adobe] 区段用作广告体验中特定创意人员的目标。

>[!NOTE]
>
>有关如何在Audience Manager和Experience Cloud中创建受众的更多信息 [!DNL Audience Library] 界面以及不同受众类型的常见用例，请参阅&quot;[受众创建选项](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html)“

## 将DSP媒体曝光数据发送到Audience Manager

*仅使用DSP的广告商*

具有Adobe Audience Manager的DSP客户可以使用对Audience Manager的像素调用，从广告促销活动中捕获数据。 然后，您可以使用促销活动数据构建基于规则的特征，利用这些特征可定义新区段，以启用各种DSP用例，例如更高级的分段、频率管理、营销分析和报表见解。

请参阅&quot;[将DSP媒体曝光数据发送到Adobe Audience Manager概述](/help/integrations/audience-manager/media-data-integration/overview.md)”以了解更多信息。

## 利用Audience Analytics更深入地了解网站活动

通过以下方式Adobe Advertising客户 [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) 可同时将Adobe Advertising跟踪数据和Audience Manager区段发送到 [!DNL Analytics] 以获取有关网站活动的丰富见解。

有关更多信息，请参阅&quot;[[!DNL Adobe Audience Analytics] 面向Adobe Advertising客户](/help/integrations/audience-manager/audience-analytics.md)“
