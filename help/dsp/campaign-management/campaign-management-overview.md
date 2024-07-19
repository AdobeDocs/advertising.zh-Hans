---
title: Advertising DSP中的Campaign Management概述
description: 了解营销活动管理层次结构和组件。
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# Advertising DSP中的Campaign Management概述

DSP促销活动具有以下层次结构：

* 营销活动
   * 包
      * 投放位置
         * 广告
<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
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
>* [关于Campaign Management](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [关于包管理](/help/dsp/campaign-management/packages/package-about.md)
>* [关于版面管理](/help/dsp/campaign-management/placements/placement-about.md)
>* [关于广告管理](/help/dsp/campaign-management/ads/ad-about.md)
>* [营销活动启动项核对清单](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [设置效果营销活动的最佳实践](/help/dsp/optimization/campaign-best-practices-performance.md)
>* Campaign Management视图中的[性能报告类型](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [管理您的Campaign数据视图](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [视频： DSP帐户结构和用户界面](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
