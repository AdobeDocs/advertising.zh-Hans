---
title: 与Adobe Experience Cloud解决方案和服务集成
description: 了解Search、Social和Commerce与Adobe Experience Cloud解决方案和服务的集成。
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
source-git-commit: 3f91cd92a364a8e9dd569bd590c59740ea1493d7
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# 与Adobe Experience Cloud解决方案和服务集成

Advertising Search、Social和Commerce已与以下[!DNL Adobe]产品集成。

* 来自Adobe Experience Platform的[标记](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html?lang=zh-Hans) — 您可以使用适用于Adobe Experience Platform的[Adobe Advertising Cloud扩展](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud)来[为您的广告登陆页面创建Adobe Advertising转化跟踪标记](/help/search-social-commerce/tools/conversion-tag-generate.md)以及第三方跟踪标记。 如果您的组织没有Experience Platform帐户，则仍可以直接在[用户界面中为Adobe Experience Platform数据收集](https://experience.adobe.com/#/data-collection/)安装该扩展，Adobe Experience Cloud客户可以免费使用该扩展。

  要安装所需的扩展，请联系您的组织管理员以访问UI中的数据收集功能，并让他们授予您`manage_properties`权限。

  **注意：**&#x200B;您还可以[直接在Search、Social和Commerce中创建转化跟踪标记](/help/search-social-commerce/tools/conversion-tag-generate.md)。

<!-- another link re tags, which is more direct within the tags docs but not very useful:  https://exchange.adobe.com/apps/ec/100155 -->

* Adobe Analytics — （选择加入功能）Adobe Advertising和[!DNL Analytics]通过以下方式集成：

   * Adobe Advertising和[!DNL Analytics]无缝共享数据。 [!DNL Analytics]可以每天将网站参与和转化数据发送到Search、Social和Commerce，从中可将这些数据用于广告优化和报表。 此外，Adobe Advertising还可以每天将广告流量数据（包括展示次数、点击次数和成本）从您的广告网络发送到[!DNL Analytics]，以便所有报表工具中都能提供这些数据。

     有关每个广告网络和广告类型[支持的详细信息，请参阅](/help/search-social-commerce/introduction/supported-inventory.md)支持的清单[!DNL Analytics]。 另请参阅“[&#x200B; [!DNL Analytics for Advertising]的](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=zh-Hans){target="_blank"}概述”，以了解有关数据交换的更多信息。

     要交换数据，必须首先配置Adobe Advertising和[!DNL Analytics]。 有关初始设置的更多信息，请与您的Adobe客户团队联系。

     >[!NOTE]
     >
     >默认情况下，[!DNL Analytics]指标在“搜索”、“社交”和“Commerce”屏幕中不可见。 在[实施团队将选定的标准或自定义事件配置为传递到Adobe Advertising后，您必须明确](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)使量度在营销活动管理视图、项目组合和报告中可用[!DNL Adobe]。 您可以选择更改显示的量度名称（无需在[!DNL Analytics]中更改它们）。 您可以使量度在UI中可见，并从[!UICONTROL Admin] > [!UICONTROL Conversions]重命名量度。

   * 具有[!DNL Analytics]但不具有Audience Manager的广告商可以从与Adobe Experience Cloud共享的[区段 [!DNL Google Ads] 创建](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)客户匹配受众[!DNL Analytics]。 广告商必须实施[Adobe Experience Platform Identity服务](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hans)并在其网站上部署标记，才能符合条件。 然后，您可以将[!DNL Google Ads]营销活动中的受众用作营销活动级别或广告组级别的[目标](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md)或[排除项](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)。

* Adobe Audience Manager区段 — （选择加入功能）您可以从将Search、Social和Commerce作为目标的Audience Manager区段[创建 [!DNL Google Ads] 客户匹配受众](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)。 这可能包括发布到Adobe Experience Cloud的[!DNL Analytics]区段和使用Adobe Experience Cloud受众库创建的区段。 然后，您可以将[!DNL Google Ads]营销活动中的受众用作营销活动级别或广告组级别的[目标](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md)或[排除项](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)。

  有关详细信息，请参阅[Adobe Advertising与Adobe Audience Manager的集成](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html?lang=zh-Hans)。

* Adobe Target — 您可以在Search、Social和Commerce与[!DNL Target]之间实施点进信号共享，在[!DNL Target]中为您的广告设置A/B测试活动，然后使用[!DNL Analytics] Analysis Workspace查看测试数据。

* Adobe Campaign — 您可以[使用 [!DNL Google Ads] 中的电子邮件列表创建和更新 [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md)客户匹配受众。

* Adobe Experience Cloud通知 — （通过Adobe Experience Cloud登录时）通过每页顶部的通知链接（[警报通知](/help/search-social-commerce/assets/notifications-panel.png "警报通知")），可以查看所有Adobe Experience Cloud系统更新、帖子、提及次数和共享资源。 有关访问Adobe的信息，请联系您的Adobe Experience Cloud客户团队。
