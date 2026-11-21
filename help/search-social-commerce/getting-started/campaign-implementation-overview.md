---
title: 设置广告网络帐户和营销活动
description: 按照广告网络连接、营销活动、跟踪、转化量度和可选项目组合优化的设置工作流操作。
feature: Search Getting Started, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 54967645-9f46-5896-8af7-b943b426aadf
    internal-label: Search Getting Started
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%
---
# 设置广告网络帐户和营销活动

*Beta功能*

[!DNL Adobe]和您的代理机构与您合作，共同连接您的广告网络帐户、准备营销活动、配置跟踪和验证性能数据。 如果您希望Search、Social和Commerce优化符合条件的促销活动，则该工作流还包括项目组合设置。

此核对清单为更广泛的[实施工作流](implemention-overview.md)提供帐户和营销活动详细信息。 您可以执行的任务取决于您的权限以及每个广告网络和促销活动类型[&#128279;](/help/search-social-commerce/introduction/supported-inventory.md)支持的功能。

## 设置工作流

1. **确认访问和帐户要求。**

   与管理员合作，确认对相应广告商的访问权限和任务所需的权限。 请参阅[搜索、社交和Commerce的用户管理](/help/search-social-commerce/user-administration.md)。

   如有必要，请在广告网络的网站上创建实际的广告网络帐户。 在Search、Social和Commerce中创建帐户记录时，不会在广告网络上创建帐户。

1. **连接或注册每个ad网络帐户。**

   在[!UICONTROL Manage] > [!UICONTROL Accounts]中，为[帐户类型](/help/search-social-commerce/manage/accounts/ad-network-account-about.md)使用工作流：

   * **API连接：** [创建帐户详细信息](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#create-account)、完成特定于网络的身份验证、配置跟踪选项并启用帐户。 验证其[身份验证和访问状态](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#authentication-status)；成功的身份验证不一定意味着已授予所有所需的权限。

   * **数据上传：** [创建帐户详细信息并上传营销活动和绩效数据](/help/search-social-commerce/manage/accounts/data-upload-accounts/data-upload-account-manage.md)。 这些帐户不会与广告网络同步，也不会支持组合优化。

   * **[!DNL Naver]仅跟踪：**&#x200B;遵循[仅跟踪帐户工作流](/help/search-social-commerce/manage/accounts/template-account-manage.md)。 使用批量工作表生成跟踪URL并在广告网络的编辑器中应用它们；该帐户不会同步或支持组合优化。

1. **查看或创建营销活动结构。**

   对于连接API的帐户，查看同步的营销活动及其组件。 [必要时请求手动同步](/help/search-social-commerce/manage/accounts/api-accounts/sync-api-accounts.md)。

   对于支持的营销活动类型，请使用[!UICONTROL Manage] > [!UICONTROL Campaigns]来[创建或编辑营销活动](/help/search-social-commerce/manage/campaigns/campaign-manage.md)。 创建所需的[广告组](/help/search-social-commerce/manage/ad-groups/ad-group-manage.md)、[广告](/help/search-social-commerce/manage/ads/ad-manage.md)和其他支持的组件。 您还可以将[批量工作表](/help/search-social-commerce/set-up/bulksheets/about.md)用于支持的批量操作。

   在激活营销活动之前，完成任何所需的网络特定设置。 在广告网络自己的界面中管理不支持的组件。

1. **在启动之前配置并验证跟踪。**

   Select与您的实现匹配的[转化跟踪方法](/help/search-social-commerce/tracking/conversion-tracking-about.md)。 必要时，[生成并应用点击跟踪URL](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)和[生成转化跟踪标记](/help/search-social-commerce/goals/conversions/conversion-tag-generate.md)。

   配置任何所需的[集成](/help/integrations/home.md)或[转化源](/help/search-social-commerce/tracking/tracking-about.md)，并验证转化是否可以按预期归因。 对于仅跟踪的促销活动，在广告网络的编辑器中应用生成的跟踪URL。

1. **查看转化量度。**

   在[!UICONTROL Goals] > [!UICONTROL Conversions]中，[查看跟踪的量度并使所需的量度对管理视图、报告和目标可见](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#conversion-metrics-change-available)。 需要区分量度时更改显示名称。

1. **（可选）准备项目组合优化。**

   确认营销活动及其竞价策略[符合组合优化](/help/search-social-commerce/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy)的条件。

   [创建或选择使用相应转化指标的目标](/help/search-social-commerce/goals/objectives/objective-about.md)。 在[!UICONTROL Manage] > [!UICONTROL Portfolios]中，[创建项目组合](/help/search-social-commerce/manage/portfolios/portfolio-create.md)或[编辑具有所需目标、支出策略和优化设置的现有项目组合](/help/search-social-commerce/manage/portfolios/portfolio-edit.md)。

   [将营销活动分配给项目组合](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio)。 每个营销活动只能属于一个项目组合，并且项目组合中的所有营销活动必须使用相同的货币。

1. **验证营销活动数据并建立性能基线。**

   确认成本、点击和转化数据可用于每个营销活动。 将转化数据与相应的源进行比较，包括在适用的情况下[!DNL Google Ads]和[!DNL Microsoft Advertising]。 在比较报表时，请使用一致的日期范围和归因设置。

   对于新的项目组合，[激活它](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md)以收集和建模数据。 在启用优化之前验证数据和项目组合设置。

1. **（可选）启动项组合优化。**

   项目组合准备就绪后，[将其状态更改为已优化](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md)，查看先决条件和确认消息。 然后，搜索、Social和Commerce会根据其设置和支持的活动竞价策略优化组合。

1. **配置正在进行的监视和报告。**

   [自定义您的数据视图](/help/search-social-commerce/common-tasks/data-views/data-views-about.md)、[设置自定义警报](/help/search-social-commerce/common-tasks/alerts-manage.md)和[生成计划报表](/help/search-social-commerce/reports/management/report-manage.md)。 需要时，使用[报告模板](/help/search-social-commerce/reports/report-templates-manage.md)和[电子表格馈送](/help/search-social-commerce/reports/spreadsheet-feeds-manage.md)自动报告。

   启动后继续[监控和调整营销活动和项目组合](/help/search-social-commerce/manage/manage-about.md#monitor-performance)。

>[!MORELIKETHIS]
>
>* [实施Search、Social和Commerce概述](implemention-overview.md)
>* [关于管理营销活动和项目组合](/help/search-social-commerce/manage/manage-about.md)
>* 搜索、社交和Commerce中的[[!DNL Google Ads] 转化数据](/help/search-social-commerce/tracking/google-conversion-data.md)
>* 搜索、社交和Commerce中的[[!DNL Microsoft Advertising] 转化数据](/help/search-social-commerce/tracking/microsoft-conversion-data.md)
