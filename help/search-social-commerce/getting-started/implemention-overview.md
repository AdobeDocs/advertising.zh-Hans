---
title: 实施Search、Social和Commerce概述
description: 了解用于启动和维护项目组合的常规工作流。
exl-id: c99dc029-81e4-4416-89b1-7cf8d66658b2
feature: Search Getting Started
TQID: 'https://experienceleague.adobe.com/AFMTue1YGuFjAJF04HTHEimfd2JC8ZxSkYCRDu8wDFY'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 54967645-9f46-5896-8af7-b943b426aadf
    internal-label: Search Getting Started
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 0%
---
# 实施Search、Social和Commerce概述

[!DNL Adobe]或其关联代理与每个广告商合作，以启动其在线广告组合并跟踪任何其他广告营销活动。 首次启动后，其他持续性任务将确保广告商的目标继续得到实现。

以下是实施和使用“搜索”、“社交”和“Commerce”的常规工作流程。

## 初始启动

[!DNL Adobe]和/或您的代理机构与您合作执行以下操作：

1. 评估您的高级业务目标并设计实现这些目标的策略：

   1. 确定您的业务模式和营销目标。

   1. 确定您的转化跟踪要求

   1. 分析现有的在线广告帐户结构。

   1. 确定项目组合优化和报告的量度。

1. （管理员或帐户管理员用户）设置管理帐户：

   1. 设置广告商帐户。 如果代理管理广告商的数据，则广告商的帐户必须与代理帐户关联。

   1. （如有必要）为广告商创建用户帐户，以查看和管理其促销活动数据并生成报表。

   与您的管理员合作，使用Adobe Admin Console和相应的产品配置文件配置访问权限。 请参阅[搜索、社交和Commerce的用户管理](/help/search-social-commerce/user-administration.md)。

1. 与每个广告网络帐户同步或创建活动：

   * 对于连接API的帐户，[在[!UICONTROL Manage] > [!UICONTROL Accounts]中创建帐户详细信息](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#create-account)，完成特定于网络的身份验证，配置跟踪选项，并启用帐户。

   * 对于没有API支持的帐户，请按照适用的[数据上传](/help/search-social-commerce/manage/accounts/data-upload-accounts/data-upload-account-manage.md)或[仅跟踪帐户](/help/search-social-commerce/manage/accounts/template-account-manage.md)工作流操作。 这些帐户不会与广告网络同步，也不会支持组合优化。

   * 如果帐户中尚未包含促销活动数据，请在Search、Social和Commerce中或广告网络内添加促销活动、广告组、关键字、广告和投放位置。

     有关详细的设置核对清单，请参阅“[设置广告网络帐户和营销活动](campaign-implementation-overview.md)”。 对于支持的营销活动类型，请使用[!UICONTROL Manage] > [!UICONTROL Campaigns]来[创建和管理营销活动](/help/search-social-commerce/manage/campaigns/campaign-manage.md)。

1. 为希望Adobe Advertising跟踪转化的所有广告设置跟踪：

   1. （如有必要） [通过生成和上传点击跟踪URL，为广告、（可选）关键字、[!DNL Google Ads]投放位置和[!DNL Google Ads]扩展设置点击跟踪](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)。

      使用基于Adobe Advertising像素的转化跟踪服务的广告商的点击跟踪URL包括到[!DNL Adobe]服务器的重定向。

   1. [设置转化跟踪](/help/search-social-commerce/tracking/conversion-tracking-about.md)。 根据实施，这可能涉及将转化跟踪标记添加到相应的网页，和/或为您使用自己的方法收集的转化数据设置每日馈送拖放。 您可以从[!UICONTROL Goals] > [!UICONTROL Conversions] [生成Adobe Advertising转化跟踪标记](/help/search-social-commerce/goals/conversions/conversion-tag-generate.md)。

      有关详细信息，请参阅“[关于搜索、社交和Commerce的跟踪](/help/search-social-commerce/tracking/tracking-about.md)”。

1. 设置与其他产品的集成：

   1. （使用Adobe Analytics和/或Adobe Audience Manager的广告商）设置各种帐户之间的集成，以便Adobe Advertising可以与这些帐户交换数据。

      请参阅“[与CX Enterprise](/help/integrations/home.md)的集成”指南。

   1. （具有[!DNL Google Analytics]的广告商）同步[!DNL Google Analytics]帐户、属性和视图组合的转化量度，以进行优化和报告。

      此配置使用旧版用户界面。 请参阅“[关于同步 [!DNL Google Analytics] 转化量度](/help/search-social-commerce/legacy-ui/admin/data-sources/data-source-about.md)”，并在需要时[切换到旧版接口](ui-switch.md)。

1. （可选）设置和启动项目组合：

   1. 在[!UICONTROL Goals] > [!UICONTROL Conversions]中，[查看转化量度并使所需量度可见](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#conversion-metrics-change-available)。 在[!UICONTROL Goals] > [!UICONTROL Objectives]中，[创建或选择目标](/help/search-social-commerce/goals/objectives/objective-about.md)以进行优化。

   1. 在[!UICONTROL Manage] > [!UICONTROL Portfolios]中，[&#128279;](/help/search-social-commerce/manage/portfolios/portfolio-create.md)通过适当的[合格营销活动](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio)创建配置为满足您的目标和业务目标的项目组合。 [激活项目组合](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md)以收集和建模数据。 然后，实施团队会收集并验证至少14天的点击和收入数据，并验证项目组合设置。

      >[!NOTE]
      >
      >搜索、Social和Commerce仍会跟踪和报告未分配到项目组合的活动数据，但不会为他们提供优化。

   1. 在有足够的数据可用于创建基线后，团队可以[将项目组合状态更改为已优化](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) — 允许Search、Social和Commerce根据项目组合类型和营销活动竞价策略优化项目组合的竞价、预算和/或竞价策略目标。

   有关优化支持和项目组合状态，请参阅&quot;[关于项目组合](/help/search-social-commerce/manage/portfolios/portfolio-about.md)&quot;。

1. 监控您的项目组合性能：

   1. 使用[!UICONTROL Dashboard] > [!UICONTROL Overview]到[查看项目组合趋势](/help/search-social-commerce/dashboard/dashboard-overview.md)和[查看项目组合性能详细信息](/help/search-social-commerce/manage/portfolios/portfolio-details.md)来调查结果和模型准确性。

   1. [设置自定义警报](/help/search-social-commerce/common-tasks/alerts-manage.md)和[生成自定义报告](/help/search-social-commerce/reports/management/report-manage.md)以进行性能监控。 需要时，使用[报告模板](/help/search-social-commerce/reports/report-templates-manage.md)和[电子表格馈送](/help/search-social-commerce/reports/spreadsheet-feeds-manage.md)自动报告。

   有关详细信息，请参阅“[监视营销活动和项目组合效果](/help/search-social-commerce/manage/manage-about.md#monitor-performance)”。

1. （可选）配置[性能数据视图](/help/search-social-commerce/common-tasks/data-views/data-views-about.md)以显示要查看的数据。

## 正在进行的任务

首次启动后，需要执行以下持续任务。 根据您的参与条款，[!DNL Adobe]、附属机构或广告商将执行以下任务：

* 通过查看警报、每个项目组合及其组件促销活动的性能数据、可自定义的报表和（某些角色）模拟，继续监控和分析每个项目组合的性能。

* 根据组合的实际和预测绩效以及增长机会，根据需要调整用于管理组合集的各种策略和设置：

  * 调整项目组合预算、目标和其他设置。

  * 调整帐户/营销活动结构以适应营销策略的变化。

  * 添加/暂停/删除营销活动组件。 这可能包括基于搜索词分析扩展关键词集，以及测试广告文案和登陆页面。

  * 根据高级性能报告更新地理和站点定位策略。

  * （可选）将竞价限制添加到单个搜索关键词或广告组、营销活动或项目组合中的所有关键词。

  * 添加新项目组合。

有关监视营销活动和项目组合以及调整其设置的说明，请参阅“[关于管理营销活动和项目组合](/help/search-social-commerce/manage/manage-about.md)”和“[编辑项目组合详细信息](/help/search-social-commerce/manage/portfolios/portfolio-edit.md)”。
