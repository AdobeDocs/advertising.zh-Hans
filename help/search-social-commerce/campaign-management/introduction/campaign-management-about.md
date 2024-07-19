---
title: 关于Search、Social和Commerce中的促销活动管理
description: 了解Search、Social和Commerce中的促销活动管理功能。
exl-id: 19e36e73-fcb6-4ff3-980b-fc05042725fd
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# 关于Search、Social和Commerce中的促销活动管理

通过“搜索”、“社交”和“Commerce”，您可以在一个位置跟踪和/或管理搜索、显示/内容、社交、购物、受众和效果最佳的营销活动。 根据广告网络和促销活动类型，可用功能可能包括与广告网络的同步、创建和编辑功能、跟踪和转化归因、报告以及竞价和预算优化。 有关每个广告网络可用功能的详细信息，请参阅[支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)。

当您在[!UICONTROL Campaigns]视图中添加和编辑促销活动数据时，Search、Social和Commerce会立即将数据更改推送到广告网络。 搜索、Social和Commerce还每天从同步的广告网络帐户中提取一次营销活动结构数据并单击数据（或者在检测到新营销活动时更频繁），并根据请求按需提取这些数据。

## 设置对您的广告网络帐户的访问权限

为了跟踪广告商广告网络帐户中的广告效果（并可能为广告投标），Adobe帐户团队[在Search、Social和Commerce中创建相应的帐户记录](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)。 帐户记录包括跟踪选项。

对于通过广告网络的API同步的帐户，帐户记录还包括帐户访问凭据。 启用帐户后，即会通过广告网络从中提取帐户数据。 然后，您可以查看现有帐户数据，以及创建和编辑营销活动结构和广告数据。

## 点击跟踪可将点击次数与转化次数绑定

如果您使用Adobe Advertising转化跟踪服务，则必须在登陆页面后缀、跟踪模板以及广告、关键词和版面、站点链接和产品列表的最终/目标URL中包含Search、Social和Commerce点击跟踪代码。 对于其促销活动设置包括“[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]”的[支持的广告网络和促销活动类型](/help/search-social-commerce/introduction/supported-inventory.md)，Search、Social和Commerce会在您保存记录时自动附加其自身的重定向和跟踪代码，因此您无需手动添加。 否则，您必须手动将代码添加到跟踪模板或最终URL中。

有关跟踪的更多信息，请参阅关于“跟踪”的一章。

## 自动竞价和预算管理

对于[支持的广告网络和营销活动类型](/help/search-social-commerce/introduction/supported-inventory.md)，您可以将营销活动分组到项目组合中，每个项目组合都具有特定的业务目标和特定的预算或绩效目标。 在标准产品组合中， Search 、 Social和Commerce可优化CPC关键词竞价和促销活动预算。 混合项目组合将来自搜索、社交和Commerce的优化技术与您的广告网络相结合。

有关可用项目组合选项以及如何设置项目组合的详细信息，请参阅有关“Portfolio”的“优化指南”一章，该章可从Search、Social和Commerce中获取。<!-- verify convention for referencing Optimization Guide here -->

## 营销活动管理视图

利用营销活动管理视图，可监控和管理搜索帐户。 可以使用以下视图：

* **[!UICONTROL Campaigns]** — [!UICONTROL Campaigns]视图显示来自每个连接的广告网络帐户的数据。 您可以查看所有广告网络帐户以及单个帐户、促销活动、广告组、关键字、广告、购物产品组、投放位置、自动目标（动态搜索目标）、受众和广告扩展库及其相关帐户实体的成本、点击、展示和收入数据。 对于支持的广告网络上的[支持的促销活动类型](/help/search-social-commerce/introduction/supported-inventory.md)，您可以直接在界面中创建和编辑单个促销活动和促销活动组件的数据。 您可以选择将大多数子视图中的数据导出到电子表格文件。

  >[!NOTE]
  >
  >广告级别的数据不适用于[!DNL Google Ads]动态搜索广告(DSA)、最佳效果、智能购物和[!DNL YouTube]营销活动。

* **[!UICONTROL Products]** — [!UICONTROL Products]视图显示已同步的每个[[!DNL Google] 或 [!DNL Microsoft] 商家中心帐户的数据](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)。 默认的[!UICONTROL Accounts]子视图列出了所有同步的帐户；某些用户类型可以从此视图添加新帐户。 [!UICONTROL Products]子视图列出了帐户中的每个产品。

* **[!UICONTROL Advanced (ACM)]** — 从[!DNL Advanced] ([!DNL AMC]，对于高级Campaign Management)视图中，您可以设置自动流程，以根据您创建的广告网络特定的广告模板以及您上传到FTP位置的[!DNL Google Merchant Center]帐户或清单数据文件的内容，创建针对清单中每个项目的[动态广告和关键字](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)。 子视图显示有关广告商的每个馈送模板的详细信息，以及馈送中包含的每个营销活动、广告组、关键词和广告（通过馈送模板传播但未发布到广告网络）。

* **[!UICONTROL Bulksheets]** — 使用[!UICONTROL Bulksheets]视图为[支持的广告网络](/help/search-social-commerce/introduction/supported-inventory.md)上的帐户创建包含所需数量的数据的[批量工作表文件](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)，然后将它们发布到广告网络。

* **[!UICONTROL Audiences]** — [在[!UICONTROL Audiences]视图](/help/search-social-commerce/campaign-management/campaigns/audience-about.md)中，列出了从各种类型的用户列表生成的所有[!DNL Google Ads]和[!DNL Microsoft Advertising]受众。 您可以从现有Adobe Experience Cloud受众和客户电子邮件列表中创建[!DNL Google Ads]受众。 您还可以查看和管理[!DNL Google Ads]和[!DNL Microsoft Advertising]广告的受众目标和排除项。

* **[!UICONTROL Label Classifications]** — 使用此视图创建和删除[标签分类](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md)，这可以帮助您将标签分组为有意义的集。

>[!MORELIKETHIS]
>
>* [实施广告网络帐户和营销活动概述](campaign-implemention-overview.md)
>* [监视和管理广告网络营销活动的效果](monitor-performance-campaigns.md)
>* [Search、Social和Commerce中的Google广告转化数据](google-conversion-data.md)
