---
title: 实施广告网络帐户和营销活动概述
description: 了解设置、同步和管理广告网络帐户所涉及的任务。
exl-id: 36307e65-81f8-4794-8a75-a37623b294ed
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 0%

---

# 实施广告网络帐户和营销活动概述

Adobe可与每个广告商合作，建立其广告网络帐户和促销活动。 这包括配置Search、Social和Commerce以连接广告商帐户并与之同步，根据需要创建新的促销活动和促销活动组件，设置组件广告的跟踪，可以选择将促销活动添加到项目组合以允许Search、Social和Commerce优化广告竞价，以及验证初始成本、点击和收入数据。

激活促销活动并选择性地将其添加到产品组合后，Adobe客户管理团队、代理团队或广告商（取决于服务级别协议的条款）将需要监控每个促销活动，并根据需要更改相关组件和设置以实现广告商的目标。

本页包含有关所有帐户类型的信息，包括如何为已同步帐户设置营销活动结构。 有关为[!DNL Naver]设置仅跟踪帐户的其他说明，请参阅“[实现 [!DNL Naver] 仅跟踪帐户](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)”。

## 帐户和营销活动的初始设置任务

[!DNL Adobe]和/或您的机构将与您合作，执行以下操作：

1. （新广告商帐户）设置管理帐户：

   1. 设置广告商帐户。

   1. （如有必要）为广告商创建用户帐户，以查看和管理其促销活动数据并生成报表。

1. （某些广告网络）获得Search、Social和Commerce的授权，以使用广告网络的API和Search、Social和Commerce用户界面访问每个帐户。

1. 对于每个广告网络帐户：

   1. （如有必要）在广告网络上设置帐户。

   1. 通过[在Search、Social和Commerce中创建包含帐户访问凭据和跟踪选项的相应帐户记录](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account)并与帐户集成，并将帐户状态设置为“已启用”。

      然后，搜索、社交和Commerce与广告网络同步。 如果帐户已经包含促销活动数据，则约24小时内即可获得该数据。

   1. ([您可以在Search、Social和Commerce中创建/编辑](/help/search-social-commerce/introduction/supported-inventory.md)的广告类型)如果该帐户尚未包含促销活动数据，则可以使用以下适用于该广告类型的任意方法，从Search、Social和Commerce中创建促销活动结构和促销活动组件：

      * (Google Ads、Microsoft Advertising、Yahoo！ 仅限广告和Yandex帐户)设置[自动流程，以根据您创建的广告网络特定的广告模板以及您上传到FTP位置的库存数据文件的内容，创建针对库存中每个项目的动态广告和关键字](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)。

      * (百度、Google Ads、Microsoft Advertising、Yahoo！ 仅限日本广告和Yandex帐户)上传[批量工作表文件](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)，这些文件包含您希望帐户拥有的数据量，然后将它们发布到广告网络。

      * (百度、Google Ads、Microsoft Advertising、Yahoo！ 仅限日本广告和Yandex帐户)在界面中直接输入单个组件的数据。 对于大多数促销活动和广告类型，您可以在促销活动级别、广告组级别以及单个关键字、投放位置和广告级别创建数据。

      但是，某些营销活动和广告类型需要独特的工作流。 查看有关设置[[!DNL Microsoft Advertising] 购物营销活动](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)、[[!DNL Google Ads] 动态搜索广告](/help/search-social-commerce/campaign-management/special-campaign-types/google-dynamic-search-ads.md)、[[!DNL Google Ads] 效果最佳营销活动](/help/search-social-commerce/campaign-management/special-campaign-types/google-performance-max-campaigns.md)和[[!DNL Google Ads] 购物营销活动](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)的说明。

   1. （仅限[!DNL Naver]个仅跟踪帐户）上传包含数据的[批量工作表文件](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)，以复制Search、Social和Commerce中的现有促销活动、广告组和关键字，而无需将它们发布到[!DNL Naver]。

1. 为Adobe Advertising将跟踪转化的所有广告设置跟踪：

   1. (使用Adobe Advertising转化跟踪服务的广告商)如有必要，请[通过生成和上传搜索、社交和Commerce点击跟踪URL，为广告设置点击跟踪](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)，也可以选择为关键词、投放位置和广告扩展设置点击跟踪。

      对于[!DNL Google Ads]效果最佳的营销活动，请在[营销活动的跟踪设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)中设置所有跟踪。

1. 对于仅跟踪营销活动，您必须改用批量工作表生成目标URL，然后使用广告网络的本机编辑器将生成的目标URL添加到相关实体。

   1. 设置转化跟踪。 根据实施，这可能涉及将转化跟踪标记添加到广告商的网页，和/或为广告商单独收集的转化数据设置每日馈送拖放。

      如果您使用Adobe Advertising转化跟踪服务，则可以使用Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html)在Search、Social和Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md)内生成转化跟踪标记[或[。

   1. 验证跟踪的数据。

   有关设置跟踪的更多详细信息，请参阅“跟踪”一章。

1. (使用Adobe Analytics的广告商) [集成Adobe Advertising和Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)，以便他们能够交换数据。

1. (允许搜索、社交和Commerce优化竞价和/或营销活动预算；仅[支持的营销活动类型](/help/search-social-commerce/introduction/supported-inventory.md))[将营销活动分配给项目组合](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md)。

   如果项目组合尚未启动（优化竞价和/或预算），则让优化功能收集到足够的数据，以便构建成本和收入模型，这样您就可以在启动项目组合之前建立项目组合的基准表现。

   如果项目组合已启动，则启用项目组合的学习功能。 有关更多信息，请参阅“调整投资组合策略”。 在添加新营销活动后，您应该预计项目组合会不稳定，而优化功能会收集有关营销活动竞价单位的数据。 竞价会在一到三周内自动调整。

   有关项目组合的详细信息，请参阅《优化指南》，该指南可在Search、Social和Commerce中获取。<!-- verify convention for referencing Optimization Guide here -->

1. （如果将为广告商跟踪任何新转化）[使转化可用于报告、营销活动管理视图和项目组合目标](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)。

1. 对于每个促销活动，验证Search、Social和Commerce是否从广告网络接收点击次数和成本数据，并使用广告商自己的收入数据验证Search、Social和Commerce中显示的收入数据。

1. （可选）通过设置报表模板、电子表格馈送和FTP传送计划报表，自动执行报表。

   有关说明，请参阅“报表”一章。

>[!MORELIKETHIS]
>
>* [关于Search、Social和Commerce中的促销活动管理](campaign-management-about.md)
>* [监视和管理广告网络营销活动的效果](monitor-performance-campaigns.md)
>* [Search、Social和Commerce中的Google广告转化数据](google-conversion-data.md)
>* [支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)
