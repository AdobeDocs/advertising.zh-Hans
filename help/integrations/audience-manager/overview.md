---
title: Adobe广告与Adobe Audience Manager的集成
description: 了解Adobe广告与Adobe Audience Manager交换数据的各种方式。
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: f6308ac9af8019987f4a2e501cba6b019cb032b6
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Adobe广告与Adobe Audience Manager的集成

您可以通过以下方式将Adobe广告与Audience Manager集成。

## 同步Audience Manager和其他 [!DNL Adobe] 用于广告定位的区段

[!DNL Search] 并且DSP可以拉入元数据、层次结构数据和唯一受众数据，以了解广告商或代理机构的所有其他Audience Manager [!DNL Adobe] 受众。 此唯一连接仅适用于使用Adobe广告的营销人员。 参见“[导入Adobe Audience Manager区段以进行广告定位](/help/integrations/audience-manager/import-audiences.md).”

### 使用Audience Manager和其他 [!DNL Adobe] 要创建的区段 [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*已选择加入的广告商 [!DNL Advertising Search] 仅限*

范围 [!DNL Search]，您可以创建 [!DNL Google Ads] Google客户使用具有以下特征的现有Audience Manager区段，从用户ID匹配受众 [!UICONTROL Adobe Media Optimizer (HTTP)] 和 [!UICONTROL Adobe Media Optimizer Batch Destination] 作为目标。 ([!DNL Media Optimizer] 是以前的名称 [!DNL Search].) 这包括发布到Adobe Experience Cloud的Adobe Analytics区段和使用Adobe Experience Cloud创建的区段 [!DNL Audience Library]. 有关更多信息，请参阅的产品内帮助。 [!DNL Search].

[客户通过用户ID匹配受众](https://support.google.com/google-ads/answer/9199250) 类似于基于网站标记的受众，但会将非PII ID分配给唯一的受众成员，以便获得优于标准客户匹配和基于网站标记的受众的明显优势。

要创建必要的用户ID，您必须使用Adobe广告JavaScript标记 <!-- with a user ID parameter -->在你的网站上。 有关更多信息，请与您的Adobe客户团队联系。

![区段创建过程](/help/integrations/assets/ad_search_user_id_pic.png)

创建受众后，您便可以在以下位置使用它们 [!DNL Google Ads] 营销活动作为 [营销活动级别或广告组级别的目标或排除项](#audience-manager-targets).

### 使用Audience Manager和其他 [!DNL Adobe] 要定位或排除广告的区段 {#audience-manager-targets}

* (选择加入的广告商，具有 [!DNL Search])您可以使用任意 [!DNL Google Ads] 受众属于 [创建方式 [!DNL Adobe] 区段](#audience-manager-google-audiences) 作为活动级别或广告组级别的目标或排除项，在 [!DNL Google Ads] 营销活动。

* (使用DSP的广告商)您可以使用现有的 [!DNL Adobe] 区段作为广告投放的目标。 您可以选择将区段包含在可重用受众中，将其用作多个投放位置的定位或排除项。

* （使用Advertising Creative的广告商）您可以使用现有的 [!DNL Adobe] 区段作为广告体验中特定创意人员的目标。

>[!NOTE]
>
>有关如何在Audience Manager和Experience Cloud中创建受众的更多信息 [!DNL Audience Library] 界面以及不同受众类型的常见用例，请参阅&quot;[受众创建选项](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).”

## 将DSP Media Exposure数据发送到Audience Manager

*仅使用DSP的广告商*

具有Adobe Audience Manager的DSP客户可以使用像素调用从广告促销活动中捕获Audience Manager数据。 然后，您可以使用促销活动数据构建基于规则的特征，这些特征可用于定义新区段，以启用各种DSP用例，例如更高级的分段、频率管理、营销分析和报表分析。

参见“[将DSP媒体曝光数据发送到Adobe Audience Manager概述](/help/integrations/audience-manager/media-data-integration/overview.md)”以了解更多信息。

## 通过Audience Analytics更深入地了解网站活动

通过以下方式Adobe广告客户 [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) 可将跟踪广告的Adobe数据和Audience Manager区段发送到 [!DNL Analytics] 以深入了解网站活动。

有关更多信息，请参阅“[[!DNL Adobe Audience Analytics] 面向Adobe广告客户](/help/integrations/audience-manager/audience-analytics.md).”
