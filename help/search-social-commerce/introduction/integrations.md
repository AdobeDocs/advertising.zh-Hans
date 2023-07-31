---
title: 与Adobe Experience Cloud解决方案和服务集成
description: 了解Search、Social和Commerce与Adobe Experience Cloud解决方案和服务的集成。
exl-id: e8b521f5-f426-4c50-9df4-361a047c9ff0
feature: Search Introduction
source-git-commit: b730716565dfae9cb32556eaede1c3f29f316ac7
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# 与Adobe Experience Cloud解决方案和服务集成

Advertising Search、Social和Commerce已与以下集成 [!DNL Adobe] 产品。

* [Adobe Experience Platform中的标记](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html)  — 您可以使用 [Adobe Advertising Cloud扩展](https://exchange.adobe.com/apps/ec/100155) ，以便Adobe Experience Platform为您的广告登陆页面创建Adobe Advertising转化跟踪标记以及第三方跟踪标记。 (您还可以 [直接在Search、Social和Commerce中创建转化跟踪标记](/help/search-social-commerce/tools/conversion-tag-generate.md).) 有关要包含在标记中的信息，请联系您的Adobe客户团队或实施团队。

* Adobe Analytics — （选择加入功能）Adobe Advertising和 [!DNL Analytics] 通过以下方式进行集成：

   * Adobe Advertising和 [!DNL Analytics] 无缝共享数据。 [!DNL Analytics] 可每天将网站参与和转化数据发送到搜索、社交和商务，从中可将这些数据用于广告优化和报表。 此外，Adobe Advertising可以每天将广告流量数据（包括展示次数、点击量和成本）从您的广告网络发送到 [!DNL Analytics]，其中的数据在所有报表工具中均可用。

     请参阅&quot;[支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)”以了解有关 [!DNL Analytics] 支持每种广告网络和广告类型。 另请参阅&quot;[概述 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}”以了解有关数据交换的更多信息。

     要交换数据，请Adobe Advertising和 [!DNL Analytics] 必须初始配置。 有关初始设置的更多信息，请与您的Adobe客户团队联系。

     >[!NOTE]
     >
     >默认情况下， [!DNL Analytics] 量度在“搜索”、“社交”和“商务”屏幕中不可见。 您必须明确 [使指标可在营销活动管理视图、组合和报告中使用](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md) 之后 [!DNL Adobe] 实施团队已配置选定标准或自定义事件以传递到Adobe Advertising。 您可以选择更改显示的指标名称（无需在中更改这些名称） [!DNL Analytics])。 您可以使量度在UI中可见，然后从重命名量度 [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

   * 广告商使用 [!DNL Analytics] 但Audience Manager不能 [创建 [!DNL Google Ads] 客户匹配受众](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) 从 [!DNL Analytics] 与Adobe Experience Cloud共享的区段。 广告商必须实施 [Adobe Experience Platform Identity服务](https://experienceleague.adobe.com/docs/id-service/using/home.html) 并在其网站上部署标记。 然后，您可以在中使用受众 [!DNL Google Ads] 营销活动（营销活动级别或广告组级别） [目标](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) 或 [排除项](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

* Adobe Audience Manager区段 — （选择加入功能）您可以 [创建 [!DNL Google Ads] 客户匹配受众](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) Audience Manager区段，将“搜索”、“社交”和“商务”作为目标。 这可能包括 [!DNL Analytics] 发布到Adobe Experience Cloud的区段和使用Adobe Experience Cloud受众库创建的区段。 然后，您可以在中使用受众 [!DNL Google Ads] 营销活动（营销活动级别或广告组级别） [目标](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) 或 [排除项](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

  请参阅&quot;[Adobe Advertising与Adobe Audience Manager的集成](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)”以了解更多信息。

* Adobe Target — 您可以在搜索、社交和商务之间实施点进信号共享 [!DNL Target]，在中设置A/B测试活动 [!DNL Target] ，然后使用 [!DNL Analytics] Analysis Workspace以查看测试数据。

* Adobe Campaign — 您可以 [创建和更新 [!DNL Google Ads] 使用中的电子邮件列表进行客户匹配受众 [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Adobe Experience Cloud Notifications —(当您通过Adobe Experience Cloud登录时)从“通知”链接([警报通知](/help/search-social-commerce/assets/notifications-panel.png "警报通知"))，您可以查看所有Adobe Experience Cloud系统更新、帖子、提及次数和共享资源。 有关访问Adobe Experience Cloud的信息，请联系您的Adobe客户团队。
