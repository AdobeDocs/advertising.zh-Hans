---
title: 与Adobe Experience Cloud解决方案和服务集成
description: 了解Search、Social和Commerce与Adobe Experience Cloud解决方案和服务的集成。
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# 与Adobe Experience Cloud解决方案和服务集成

Advertising Search、Social和Commerce已与以下[!DNL Adobe]产品集成。

* 来自Adobe Experience Platform的[标记](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html?lang=zh-Hans) — 您可以使用Adobe Experience Platform的[Adobe Advertising Cloud扩展](https://exchange.adobe.com/apps/ec/100155)为您的广告登陆页面创建Adobe Advertising转化跟踪标记以及第三方跟踪标记。 (您也可以直接[在Search、Social和Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md)中创建转化跟踪标记。) 有关要包含在标记中的信息，请联系您的Adobe客户团队或实施团队。

* Adobe Analytics — （选择加入功能）Adobe Advertising和[!DNL Analytics]通过以下方式进行集成：

   * Adobe Advertising和[!DNL Analytics]无缝共享数据。 [!DNL Analytics]可以每天将网站参与和转化数据发送到Search、Social和Commerce，从中可将这些数据用于广告优化和报表。 此外，Adobe Advertising可以每天将广告流量数据（包括展示次数、点击量和成本）从您的广告网络发送到[!DNL Analytics]，该数据可在所有报表工具中获取。

     有关每个广告网络和广告类型[!DNL Analytics]支持的详细信息，请参阅[支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)。 另请参阅“[概述 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=zh-Hans){target="_blank"}”以了解有关数据交换的更多信息。

     要交换数据，必须首先配置Adobe Advertising和[!DNL Analytics]。 有关初始设置的更多信息，请与您的Adobe客户团队联系。

     >[!NOTE]
     >
     >默认情况下，[!DNL Analytics]指标在“搜索”、“社交”和“Commerce”屏幕中不可见。 在[!DNL Adobe]实施团队将选定的标准或自定义事件配置为传递到Adobe Advertising后，您必须明确[使指标在营销活动管理视图、项目组合和报告中可用](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)。 您可以选择更改显示的量度名称（无需在[!DNL Analytics]中更改它们）。 您可以使量度在UI中可见，并从[!UICONTROL Admin] > [!UICONTROL Conversions]重命名量度。

   * 具有[!DNL Analytics]但不具有Audience Manager的广告商可以从与Adobe Experience Cloud共享的[!DNL Analytics]区段[创建 [!DNL Google Ads] 客户匹配受众](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)。 广告商必须实施[Adobe Experience Platform Identity服务](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hans)并在其网站上部署标记，才能符合条件。 然后，您可以将[!DNL Google Ads]营销活动中的受众用作营销活动级别或广告组级别的[目标](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md)或[排除项](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)。

* Adobe Audience Manager区段 — （选择加入功能）您可以从将Search、Social和Commerce作为目标的Audience Manager区段[创建 [!DNL Google Ads] 客户匹配受众](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)。 这可能包括发布到Adobe Experience Cloud的[!DNL Analytics]区段和使用Adobe Experience Cloud受众库创建的区段。 然后，您可以将[!DNL Google Ads]营销活动中的受众用作营销活动级别或广告组级别的[目标](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md)或[排除项](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)。

  有关详细信息，请参阅[Adobe Advertising与Adobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html?lang=zh-Hans)的集成。

* Adobe Target — 您可以在Search、Social和Commerce与[!DNL Target]之间实施点进信号共享，在[!DNL Target]中为您的广告设置A/B测试活动，然后使用[!DNL Analytics] Analysis Workspace查看测试数据。

* Adobe Campaign — 您可以[使用 [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md)中的电子邮件列表创建和更新 [!DNL Google Ads] 客户匹配受众。

* Adobe Experience Cloud通知 — (通过Adobe Experience Cloud登录时)通过每页顶部的通知链接（[警报通知](/help/search-social-commerce/assets/notifications-panel.png "警报通知")），可以查看所有Adobe Experience Cloud系统更新、帖子、提及次数和共享资源。 有关访问Adobe Experience Cloud的信息，请联系您的Adobe客户团队。
