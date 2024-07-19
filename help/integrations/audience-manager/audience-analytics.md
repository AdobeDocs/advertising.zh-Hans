---
title: 用于Adobe Advertising客户的'[!DNL Adobe] [!DNL Audience Analytics] '
description: 了解如何将 [!DNL Adobe] [!DNL Audience Analytics]用于广告用例
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Adobe Advertising客户的[!DNL Adobe] [!DNL Audience Analytics]

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)是Adobe Audience Manager与Adobe Analytics之间的集成，它允许Audience Manager客户将区段发送到[!DNL Analytics]，以丰富有关网站活动的见解。

Adobe Advertising客户可以通过使用[!DNL Audience Analytics]受益。 该集成允许您：

* 将Adobe Advertising风险数据直接发送到[!DNL Analytics]，以确定上层漏斗活动对下游网站活动的影响。

* 通过漏斗上层展示广告确定营销渠道和网站进入点。

* 对与[!DNL Analytics for Advertising]的集成进行分层，以纳入[Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html)中包含[!DNL Analytics for Advertising]数据的第三方人口统计区段，了解有关用户配置文件的更多见解。

  [!DNL Audience Marketplace]通过“激活”订阅模型提供对第三方数据馈送的访问权限，这些模型允许购买者将数据发送到目标。 如果数据在[!DNL Analytics]目标中使用，则不会收取激活费。

* (使用Advertising DSP的广告商)添加其他风险区段，以实现全面的旅程管理洞察。

  Advertising DSP可以通过实施Adobe Experience Platform或Audience Manager展示跟踪像素，将曝光数据作为可操作信号发送到Audience Manager。 将相同数据转发到[!DNL Analytics]可启用高级数据分析。 有关详细信息，请参阅“[Adobe Advertising Media数据与Adobe Audience Manager的集成概述](/help/integrations/audience-manager/media-data-integration/overview.md)”。

有关[!DNL Audience Analytics]的详细信息，包括其先决条件和工作流程，请参阅“[Audience Analytics概述](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)”。

## 如何将[!DNL Audience Analytics]数据用于Adobe Advertising数据的示例

以下是有关如何在[!DNL Analytics] [!DNL Analysis Workspace]中使用组合数据的示例。

### 查看上层漏斗活动对下游活动的影响

使用Audience Manager暴露区段查看漏斗上层网站活动对下游网站活动的影响。 在跟踪像素中包含Adobe Advertising或第三方宏ID，以跟踪对详细级别（从促销活动级别到用户所展示的网站级别）的影响。

主要优点：

* 按漏斗/广告类型跟踪曝光，并使用[!DNL Audience Analytics]来确定进入率以及与客户历程下一阶段的重叠。

* 确定上漏斗活动对下游网站活动的影响。

* 连接[!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event -->和[!DNL Audience Analytics]数据<!-- (which includes the user's last exposure event) -->以确定站点的整体历程。

以下是您可以在[!DNL Analysis Workspace]中创建的报告示例。

![查看上层漏斗活动对下游网站活动的影响](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### 使用[!DNL Audience Analytics]第三方区段数据进行用户配置文件分析

使用第三方Audience Manager区段更详细地分析用户如何与您的网站进行交互。 您可以根据第三方区段中的配置文件与媒体营销活动网站关键绩效指标的互动方式，使用信息确定要为其激活媒体的新第三方受众。

>[!TIP]
> 与[!DNL Analytics]收集的任何其他维度一样，在整个[!DNL Analytics]中使用Audience Manager`Audiences ID`和`Audiences Name`维度。

以下是您可以在[!DNL Analysis Workspace]中创建的报告示例。

![使用第三方区段丰富用户配置文件分析](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [与Adobe Audience Manager的Adobe Advertising集成](/help/integrations/audience-manager/overview.md)
