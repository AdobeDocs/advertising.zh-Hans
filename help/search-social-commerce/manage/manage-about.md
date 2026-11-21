---
title: 关于管理营销活动和项目组合
description: 了解广告网络客户、营销活动、跟踪和产品组合优化如何协同工作，以及如何监控和提高性能。
feature: Search Campaign Management, Search Portfolios
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%
---
# 关于管理营销活动和项目组合

*Beta功能*

Search、Social和Commerce将活动管理、性能报告和产品组合优化整合到一个界面中。 根据广告网络和营销活动类型，您可以同步营销活动数据，创建和编辑营销活动组件，跟踪转化，以及优化竞价、预算或竞价策略目标。 有关每个广告网络的可用功能，请参阅[支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)。

[!UICONTROL Manage]菜单提供对您的帐户、营销活动、广告组、广告、关键字、产品组和项目组合的访问权限。 您的权限决定了哪些视图和操作可用。 有关完整的菜单组织，请参阅“[用户界面的组织方式](/help/search-social-commerce/getting-started/user-interface.md)”。

## 客户、营销活动和项目组合如何组合

* **广告网络帐户**&#x200B;将您的广告商数据连接到Search、Social和Commerce。 [帐户类型](/help/search-social-commerce/manage/accounts/ad-network-account-about.md)包括通过API连接同步的帐户、上载数据的帐户以及基于模板的仅跟踪帐户。 帐户类型确定您是否可以同步数据、管理营销活动或使用项目组合优化。

* **营销活动**&#x200B;包含用于投放广告的广告和其他组件。 对于支持的营销活动类型，您可以从[!UICONTROL Manage]视图[创建和管理营销活动](/help/search-social-commerce/manage/campaigns/campaign-manage.md)及其组件。 您还可以将[批量工作表](/help/search-social-commerce/set-up/bulksheets/about.md)用于支持的批量操作。

* **项目组合**&#x200B;将符合条件的营销活动分组，以针对共同的业务目标和预算或绩效目标对其进行优化。 一个营销活动只能属于一个项目组合，该项目组合中的所有营销活动必须使用相同的货币。 请参阅“[关于项目组合](/help/search-social-commerce/manage/portfolios/portfolio-about.md)”。

Portfolio分配是可选的。 您可以跟踪和报告营销活动，而无需将其分配给项目组合。 并非所有广告网络、营销活动类型或竞价策略都支持组合优化。

## 同步营销活动数据

对于通过API连接的帐户，Search、Social和Commerce会从广告网络检索支持的营销活动结构和效果数据。 您对Search、Social和Commerce中支持的促销活动组件所做的更改将发送到广告网络。

如有必要，您可以[请求手动同步](/help/search-social-commerce/manage/accounts/api-accounts/sync-api-accounts.md)。 如果帐户停止同步，请检查其[身份验证和访问状态](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#authentication-status)。

数据上传帐户和仅跟踪帐户不能与广告网络同步。 遵循[帐户类型](/help/search-social-commerce/manage/accounts/ad-network-account-about.md)的工作流以提供营销活动和性能数据。

## 设置跟踪和优化

[跟踪](/help/search-social-commerce/tracking/tracking-about.md)将促销活动与对您的业务重要的转化相关联。 根据您的实施，转化数据可能来自Adobe Advertising标记、Adobe Analytics集成、广告网络跟踪或数据馈送。 根据实施需要配置点击跟踪和转化跟踪，并在使用数据进行优化之前验证数据。

在[!UICONTROL Goals] > [!UICONTROL Conversions]中，您可以[查看为广告商跟踪的转化量度并控制其可见性](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md)。 在您的[目标](/help/search-social-commerce/goals/objectives/objective-about.md)中使用适当的量度。

要启用项目组合优化，请[创建项目组合](/help/search-social-commerce/manage/portfolios/portfolio-create.md)，分配目标且符合条件的营销活动，并配置其支出和优化设置。 有效的项目组合可收集和建模性能数据。 数据和设置就绪后，[将项目组合状态更改为已优化](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md)以开始优化。 执行的操作取决于项目组合类型和[营销活动竞价策略](/help/search-social-commerce/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy)。

有关详细的设置顺序，请参阅“[设置广告网络帐户和营销活动](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)”。

## 监测营销活动和项目组合绩效 {#monitor-performance}

客户团队、代理或广告商负责根据服务协议条款监控绩效并进行调整。 常规：

* 在[!UICONTROL Manage]视图中查看营销活动和帐户性能。 [自定义列、筛选器和日期范围](/help/search-social-commerce/common-tasks/data-views/data-views-about.md)以重点关注重要的量度和实体。

* 使用[!UICONTROL Dashboard] > [!UICONTROL Overview]可[监视组合趋势和性能变化](/help/search-social-commerce/dashboard/dashboard-overview.md)。

* 查看[自定义警报](/help/search-social-commerce/common-tasks/alerts-manage.md)以了解需要调查的情况。

* [生成营销活动、关键字、广告和组合绩效报告](/help/search-social-commerce/reports/management/report-manage.md)。 对于项目组合，[审查性能详细信息](/help/search-social-commerce/manage/portfolios/portfolio-details.md)，包括实际性能和模型准确性。

* 使用[模拟](/help/search-social-commerce/plan/simulations/simulation-about.md)（如果可用）来评估不同支出级别的预测效果。

* 调查报告的转化与源数据之间的差异。 请参阅相关链接中[!DNL Google Ads]和[!DNL Microsoft Advertising]转化数据的指南。

## 调整营销活动和项目组合

根据性能和业务目标的变化，您可能需要：

* 编辑营销活动设置、创建或暂停营销活动组件、优化关键词集或测试不同的广告。 可用操作取决于广告网络和促销活动类型。

* 使用相关管理视图和报告审查地理、受众和投放定位。

* 当应使用其他项目组合优化营销活动时，[更改营销活动分配](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio)。 将促销活动分配给另一个项目组合会将其从先前的项目组合中删除。

* [编辑产品配置文件允许的项目组合设置](/help/search-social-commerce/manage/portfolios/portfolio-edit.md)，包括目标、支出策略、约束或优化控制。

* 调查性能更改时查看[更改历史记录](/help/search-social-commerce/reports/history-logs.md)。

>[!MORELIKETHIS]
>
>* [设置广告网络帐户和营销活动](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)
>* [支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)
>* 搜索、社交和Commerce中的[[!DNL Google Ads] 转化数据](/help/search-social-commerce/tracking/google-conversion-data.md)
>* 搜索、社交和Commerce中的[[!DNL Microsoft Advertising] 转化数据](/help/search-social-commerce/tracking/microsoft-conversion-data.md)
