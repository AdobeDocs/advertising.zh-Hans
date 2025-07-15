---
title: （新UI）关于目标
description: 了解实现业务目标的目标。
feature: Search Objectives, Search Optimization
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# （新UI）关于目标

*Beta功能*

目标是指广告商为实现其业务目标而设定的目标，例如实现利润最大化或达到特定的销售目标。 Advertising Search、Social和Commerce以及Advertising DSP都使用目标：

* 每个“搜索”、“社交”和“Commerce”项目组合都必须有一个目标，以便优化功能可以为该项目组合创建点击和收入模型。

* 在DSP中，目标显示为与Search、Social和Commerce帐户关联的DSP帐户的自定义目标。 每个使用优化目标“最高广告支出回报率(ROAS)”或“最低每次收购成本(CPA)”的包都必须包含一个自定义目标，以帮助实现整体优化目标。

目标包含要跟踪和优化的转化量度以及这些量度的相对权重。 例如，假设一个在线杂志有两个在线订阅级别和一个印刷订阅级别，并且其目标“利润最大化”有三个指标：价值20美元的“基本在线订阅”、价值40美元的“优质在线订阅”和价值30美元的“印刷订阅”。 如果杂志想要根据订阅的一次性货币值赋予权重，则这些量度的相对权重将分别为1、2和1.5。

对于目标中的每个量度，您可以：

* 为来自移动设备的转化配置单独的权重。

* 将量度标记为[!UICONTROL Goal]量度或[!UICONTROL Assist]量度。

* 将权重推荐应用于量度。

>[!NOTE]
>* (搜索、社交和Commerce)当您[创建项目组合](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create.md)或稍后[修改项目组合设置](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-edit.md)时，可以将目标与项目组合关联。
>* (具有链接到Search、Social和Commerce帐户的DSP帐户的广告商)在Advertising DSP中，您可以选择目标作为具有包级别步调的包的[自定义优化目标](/help/dsp/campaign-management/packages/package-settings.md)。
>* 您可以对多个Search、Social和Commerce项目组合和/或多个DSP项目组合使用同一目标。
>* [!UICONTROL Objectives]视图中每个目标的指标不包括DSP中的数据。

## 可用量度

您可以在目标中包含以下任意内容：

* Adobe Advertising使用[Adobe Advertising转化跟踪像素](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)跟踪的指标。

* [来自转化馈送文件的广告商跟踪量度](/help/search-social-commerce/tracking/conversion-tracking-about.md)。<!-- Search only, or might DSP-only clients also have these? -->

* （具有[!DNL Adobe Analytics for Advertising]的广告商） [转化和网站参与度量度已从Adobe Analytics](/help/integrations/analytics/overview.md)同步。

  在Search、Social和Commerce中，以下[网站参与量度](/help/integrations/analytics/analytics-data-in-advertising.md)会自动计入项目组合竞价算法： `timespent_secs_1stvisit`、`timespent_secs_total`、`pageviews_1stvisit`、`pageviews_total`和`bounces`。

* [!DNL Google]个量度：<!-- Search only, or might DSP-only clients also have these? -->

   * 已从同步的[[!DNL Google Ads]帐户中跟踪](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)次转化[!DNL Google Ads]。

   * （具有[[!DNL Google Analytics] 集成](/help/search-social-commerce/admin/data-sources/data-source-about.md)的广告商）页面查看次数、会话数、跳出率（计算公式为跳出次数/会话数）和会话持续时间。

     在Search、Social和Commerce中，这些指标会自动计入项目组合竞价算法。

## 用于将目标上传到广告网络的选项

您可以选择将[帐户组合的目标作为转化 [!DNL Google Ads] 和/或 [!DNL Microsoft Advertising] 上传](/help/search-social-commerce/tools/objective-upload-to-networks.md)，以便将其用于营销活动或广告组级别优化。 启用该选项后，Search、Social和Commerce每天都会将EF ID（点击ID）级别的加权收入数据传递到广告网络。 它忽略任何广告网络跟踪量度。

>[!MORELIKETHIS]
>
>* [创建目标](objective-create.md)
>* [编辑目标](objective-edit.md)
>* [删除目标](objective-delete.md)
>* [将权重推荐应用于目标](objective-apply-weight-recommendations.md)
>* [目标设置](objective-settings.md)
