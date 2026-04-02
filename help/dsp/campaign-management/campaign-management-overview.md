---
title: Advertising DSP中的促销活动管理概述
description: 了解营销活动管理层次结构和组件。
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
TQID: https://experienceleague.adobe.com/w7j86H42OR371vewJM--ep2YUn70XJpMWJQNT92r2CY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
  - id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3d
  - id: d9510790-d834-436d-8423-8d69cd50464a
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 335
ht-degree: 0%

---

# Advertising DSP中的促销活动管理概述

DSP营销活动具有以下层级：

* 营销活动
   * 包
      * 投放位置
         * 广告
<!--
 Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package includes placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[营销活动](/help/dsp/campaign-management/campaigns/campaign-about.md)是外部测试版设置的总体框架。 每个营销活动都配置了广告商、开始和结束日期、整体预算、跨设备定位选项和默认频率上限，以及可视性、欺诈、品牌安全和受众验证的报告选项。 所有营销活动级别的设置都会自动应用于营销活动中的每个包和投放位置。

## [!UICONTROL Packages]

每个营销活动可以包含一个或多个[包](/help/dsp/campaign-management/packages/package-about.md)，每个包都包含一组版面。

使用资源包将投放位置分组，以使其达到设定的预算、性能目标和自定义步调策略。 DSP通过将预算转移到包中性能最佳的投放位置来优化包。 您可以按版面格式、库存类型、数据提供商、角色或其他可区分的特征来组织资源包。

包是可选的，但建议使用。

## [!UICONTROL Placements]

[投放位置](/help/dsp/campaign-management/placements/placement-about.md)存储了相同广告类型的一个或多个广告的定位参数。 您可以为单个营销活动或营销策划包创建投放位置，然后为其分配广告。

## [!UICONTROL Ads]

[广告](/help/dsp/campaign-management/ads/ad-about.md)包含创意资源和跟踪URL。 您可以使用合作伙伴标记表或批量标记模板，单独或批量上传第三方广告投放标记。 您还可以手动创建本机显示广告以供DSP提供。

设置广告后，必须将每个广告附加到投放位置才能开始投放广告。 您可以将单个广告附加到一个或多个投放位置。

根据投放位置定位参数，活跃促销活动中所有活跃的已批准广告都可以运行。

>[!MORELIKETHIS]
>
>* [关于Advertising DSP中的营销活动管理](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [关于Advertising DSP中的包管理](/help/dsp/campaign-management/packages/package-about.md)
>* [关于Advertising DSP中的版面管理](/help/dsp/campaign-management/placements/placement-about.md)
>* [关于Advertising DSP中的广告管理](/help/dsp/campaign-management/ads/ad-about.md)
>* [营销活动启动项核对清单](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [设置效果营销活动的最佳实践](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [促销活动管理视图中的性能报告类型](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [管理您的营销活动数据视图](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [视频： DSP帐户结构和用户界面](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
