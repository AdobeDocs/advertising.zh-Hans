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

## 同步Audience Manager和其他[!DNL Adobe]区段以进行广告定位

[!DNL Search, Social, & Commerce]和DSP可以为广告商或代理的所有受众和其他[!DNL Adobe]Audience Manager拉入元数据、层次结构数据和唯一受众数据。 此唯一连接仅适用于使用Adobe Advertising的营销人员。 请参阅“导入Adobe Audience Manager区段以进行广告定位[&#128279;](/help/integrations/audience-manager/import-audiences.md)”。

### 使用Audience Manager和其他[!DNL Adobe]区段创建[!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*仅使用[!DNL Advertising Search, Social, & Commerce]的已选择加入广告商*

在[!DNL Search, Social, & Commerce]内，您可以使用现有Audience Manager区段（将[!UICONTROL Adobe Media Optimizer (HTTP)]和[!UICONTROL Adobe Media Optimizer Batch Destination]作为目标）从用户ID创建[!DNL Google Ads]个客户匹配受众。 （[!DNL Media Optimizer]是以前的[!DNL Search, Social, & Commerce]名称。） 这包括发布到Adobe Experience Cloud的Adobe Analytics区段和使用Adobe Experience Cloud [!DNL Audience Library]创建的区段。 有关详细信息，请参阅“从 [!DNL Adobe] 受众[&#128279;](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)创建 [!DNL Google Ads] 客户匹配受众”。

[用户ID中的客户匹配受众](https://support.google.com/google-ads/answer/9199250)类似于基于网站标记的受众，但会将非PII ID分配给唯一的受众成员，以便获得优于标准客户匹配和基于网站标记的受众的独特优势。

要创建必要的用户ID，您必须在您的网站上使用Adobe Advertising的JavaScript标记<!-- with a user ID parameter -->。 有关更多信息，请与您的Adobe客户团队联系。

![区段创建流程](/help/integrations/assets/ad_search_user_id_pic.png)

创建受众后，您可以在[!DNL Google Ads]个营销活动中将其用作[营销活动级别或广告组级别的目标或排除项](#audience-manager-targets)。

### 使用Audience Manager和其他[!DNL Adobe]区段来定位或排除广告 {#audience-manager-targets}

* （已选择使用[!DNL Search, Social, & Commerce]的广告商）您可以使用任何[!DNL Google Ads]受众，这些受众是[使用 [!DNL Adobe] 区段](#audience-manager-google-audiences)创建的，并在[!DNL Google Ads]营销活动中用作营销活动级别或广告组级别的目标或排除项。

* (使用DSP的广告商)您可以将现有[!DNL Adobe]区段用作广告投放的目标。 您可以选择将区段包含在可重用受众中，将其用作多个投放位置的定位或排除项。

* (具有Advertising Creative的广告商)您可以将现有[!DNL Adobe]区段用作广告体验中特定创意人员的目标。

>[!NOTE]
>
>有关如何在Audience Manager和Experience Cloud[!DNL Audience Library]界面中创建受众以及不同受众类型的常见用例的更多信息，请参阅“[受众创建选项](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=zh-Hans)”。

## 将DSP媒体曝光数据发送到Audience Manager

*仅使用DSP的广告商*

具有Adobe Audience Manager的DSP客户可以使用对Audience Manager的像素调用，从广告促销活动中捕获数据。 然后，您可以使用促销活动数据构建基于规则的特征，利用这些特征可定义新区段，以启用各种DSP用例，例如更高级的分段、频率管理、营销分析和报表见解。

有关详细信息，请参阅“将DSP媒体曝光数据发送到Adobe Audience Manager的概述”[&#128279;](/help/integrations/audience-manager/media-data-integration/overview.md)。

## 利用Audience Analytics更深入地了解网站活动

具有[[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=zh-Hans)的Adobe Advertising客户可以将Adobe Advertising跟踪数据和Audience Manager区段发送到[!DNL Analytics]，以丰富有关网站活动的见解。

有关详细信息，请参阅“[[!DNL Adobe Audience Analytics] Adobe Advertising客户](/help/integrations/audience-manager/audience-analytics.md)”。
