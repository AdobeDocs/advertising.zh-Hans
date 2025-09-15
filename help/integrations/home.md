---
title: 新增功能
description: 了解Adobe Advertising与Adobe Experience Cloud中的其他产品和服务之间的集成更新。
cloud: Experience Cloud
product: advertising cloud
index: true
exl-id: e5874077-d2a8-43bb-ad4e-55547442c8a4
source-git-commit: 5025b135385c2e1fc7a026aa4cb6489765f0d34c
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# 新增功能

以下功能是新增的或最近更改的。

| 日期 | 功能 | 描述 | 了解更多信息 |
| ---- | ------- | ----------- | -------------------- |
| 2025年9月8日 | 与Customer Journey Analytics集成 | (Beta功能)具有Customer Journey Analytics但不具有[!DNL Analytics for Advertising]的广告商现在可以使用[Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hans)在Adobe Advertising和Customer Journey Analytics之间本机交换数据。 | 请参阅“[Adobe Advertising与Customer Journey Analytics的集成概述](/help/integrations/customer-journey-analytics/overview.md)”。 |
| 2025年3月26日 | [!DNL Adobe Analytics for Advertising] | (具有Search、Social和Commerce的广告商； [!DNL Microsoft Advertising]帐户；以及[!DNL Adobe Analytics for Advertising])对于具有[!UICONTROL Auto Upload]跟踪选项的帐户，所有营销活动类型的登陆页面后缀中的AMO ID参数格式已更新为最新格式。 以前，大多数客户的效果最佳营销活动都迁移到新格式。<br><br>对于没有[!UICONTROL Auto Upload]跟踪选项的帐户，这些帐户尚未迁移到新格式，但是，您必须手动更新每个登陆页面后缀以包含新的AMO ID格式。<br><br>当前格式：`s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}` | 请参阅[概述 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)和[AMO ID格式](/help/integrations/analytics/ids.md#amo-id-formats)。 |
| 2024年11月13日 | [!DNL Analytics for Advertising] | (具有[!DNL Analytics for Advertising]和Adobe Customer Journey Analytics的广告商)如果您使用保留变量来捕获AMO ID和EF ID，那么您可以通过尽快将为AMO ID和EF ID保留的变量复制到标准[!DNL eVars]中，为Adobe Advertising和Adobe Customer Journey Analytics之间的未来集成做准备。 这样一来，在您完成任务后，即可立即收集AMO ID和EF ID的历史数据，并且历史数据可供将来使用。 如果您使用保留的变量并且需要完成此任务，您的Adobe客户团队将告知您。 | 请参阅“[收集在Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md)中使用的AMO ID和EF ID的历史数据。” |
| 2024年10月29日发布 | [!DNL Adobe Analytics for Advertising] | （具有[!DNL Adobe Analytics for Advertising]和[!DNL Microsoft Advertising]个效果最佳促销活动的广告商）现在，当您在效果最佳促销活动的跟踪URL中实施新的AMO ID ([!DNL s_kwcid])参数时，Adobe Analytics中提供了效果最佳促销活动的资源组级别数据，这些参数不包括广告和关键字。 对大多数具有最高效果营销活动的帐户的跟踪已迁移到新格式。 对于没有[!UICONTROL Auto Upload]跟踪选项且营销活动效果最佳的帐户，这些帐户尚未迁移到新格式，但是，您必须手动更新每个登陆页面后缀以包含新的AMO ID格式。<br><br>Search、Social和Commerce中也提供了您的效果最佳营销活动的Adobe Analytics数据。 | 查看新的[AMO ID格式](/help/integrations/analytics/ids.md#amo-id-formats)和[何时以及如何将该参数添加到您的跟踪URL](/help/integrations/analytics/ids.md#amo-id-implement)。 |
| 2023年12月16日 | 帮助 | 新文档介绍了如何在[!DNL Target]中为来自搜索、社交和Commerce中广告的点进流量设置A/B测试，以及有关如何在[!DNL Analytics]中测量和可视化测试的提示。 | 请参阅“[在Adobe Target中为Search、Social和Commerce广告配置A/B测试](/help/integrations/target/ab-tests-search.md)”。 |
| 2023年8月8日 | [!DNL Analytics for Advertising] | 某些[!DNL Analytics]成功事件量度（包括标准、自定义和保留的转化量度以及流量量度）在DSP以及Search、Social和Commerce中自动可用。 现在，您还可以通过将[!DNL Analytics]和[!DNL eVars]级别的数据导入自定义成功事件，根据现有[!DNL props] [!DNL eVar]和[!DNL prop]配置自己的成功量度。 | 请参阅“[从Adobe Analytics创建转化量度 [!DNL eVars] 和 [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)”。 |
| 2023年7月13日 | 报表 | (具有[!DNL Analytics for Advertising]的DSP用户)连接电视(CTV)投放位置的显示到达转化现在包含在Adobe Analytics中提供的转化数据中。 | 请参阅[的 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md#integration-examples)概述中的“如何使用集成的示例”部分。 |
| 2022年11月1日 | 帮助 | 新文档介绍了如何在Advertising DSP和Adobe Target之间实施点进和显示信号共享，在[!DNL Target]中为您的DSP广告设置A/B测试活动，以及如何设置Adobe Analytics Analysis Workspace以查看测试数据。 | 请参阅“[在Adobe Target中为Advertising DSP广告配置A/B测试](/help/integrations/target/ab-tests-dsp.md)”。 |
| 2022年8月17日 | 帮助 | 新章节将介绍Adobe Advertising与Adobe Audience Manager集成的所有方式。 | 请参阅有关“与Adobe Audience Manager的集成”的一章，包括“Adobe Advertising与Adobe Audience Manager[的集成”的概述。](/help/integrations/audience-manager/overview.md) |
| 2021年4月27日 | [!DNL Analytics for Advertising] | 了解为什么以及如何将[!DNL Analytics for Advertising]宏添加到[!DNL Google Campaign Manager 360]广告标记以将点击数据发送到Adobe Analytics。 | 请参阅“[将 [!DNL Analytics for Advertising] 宏附加到 [!DNL Google Campaign Manager 360] 添加标记](/help/integrations/analytics/macros-google-campaign-manager.md)”。 |
| 2021年4月19日 | [!DNL Analytics for Advertising] | 了解为什么以及如何将宏附加到您的[!DNL Flashtalking]广告标记以将点击数据发送到Adobe Analytics。 | 请参阅“[将 [!DNL Analytics for Advertising] 宏附加到 [!DNL Flashtalking] 添加标记](/help/integrations/analytics/macros-flashtalking.md)”。 |
| 2021年10月27日 | [!DNL Analytics for Advertising] | 如果您的组织需要从使用旧版Adobe Analytics `visitorAPI.js`库转为使用[Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hans)库(`alloy.js`)来收集数据，则您必须进行一些更改来支持ID拼接。 | 请参阅“[在Adobe Experience Platform [!DNL Last Event Service] 中使用 [!DNL Web SDK]](/help/integrations/analytics/web-sdk.md)JavaScript库。” |
| 2021年5月26日 | 帮助 | 章节“[!DNL Analytics for Advertising]”现在包含有关“在[!DNL Analytics Marketing Channels]中工作”的子章节。 | 请参阅：“[营销渠道基础知识](/help/integrations/analytics/marketing-channels/mc-overview.md)”、“[使用Adobe Advertising ID创建 [!DNL Analytics Marketing Channels] 处理规则](/help/integrations/analytics/marketing-channels/mc-ids.md)”、“[结合使用 [!DNL Analytics Marketing Channels] Adobe Advertising数据](/help/integrations/analytics/marketing-channels/mc-ac-data.md)”和“[为什么渠道数据在Adobe Advertising和 [!DNL Analytics Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)之间可能不同。” |
| 2021年5月26日 | 帮助 | 添加了指向所有关于[!DNL Analytics for Advertising]的视频教程的链接。 | 请参阅： &quot;[有关Adobe Advertising集成的视频教程](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/overview.html?lang=zh-Hans)。&quot; |

{style="table-layout:auto"}

<!-- At some point, just make this an overview page instead?

Adobe Advertising is integrated with the following Adobe Experience Cloud products:

* [Adobe Analytics](/help/integrations/analytics/overview.md)

* Adobe Audience Manager

* Adobe Campaign (Adobe Advertising Search only)

 -->
