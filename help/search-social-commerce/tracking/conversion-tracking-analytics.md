---
title: Adobe Analytics转化跟踪
description: 了解如何在Adobe Advertising中对营销活动使用Adobe Analytics转化跟踪。
exl-id: 0ed1d059-829a-4090-950d-41cbcc27b3ac
feature: Search Tracking
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Adobe Analytics转化跟踪

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

对于集成了Adobe Advertising-Adobe Analytics的广告商，Advertising Cloud可以将您的广告点击量和展示次数与由跟踪的网站参与度和转化量度联系起来 [!DNL Analytics] 当您使用带有令牌的重定向时(`ef_id` 参数)的点击跟踪URL [竞价单位](/help/search-social-commerce/glossary.md#a-b). 此 [!DNL Analytics] 数据会通过每日馈送文件自动发送到Advertising Cloud。

请参阅&quot;[概述 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/integrations/analytics/overview.html){target="_blank"}”以了解有关集成的更多信息。

>[!PREREQUISITES]
>
> 搜索、社交和商务广告商帐户中的时区， [!DNL Analytics] 报表包，并且广告网络帐户必须匹配。 如果两者不匹配，则将存在系统间的数据差异。

## 实施概述

1. 在 [!DNL Analytics]，Search、Social和Commerce实施团队会为每个报表包修改以下配置设置：

   * 的到期 `ef_id` [!DNL eVar] 更改为匹配广告商的Adobe Advertising点击回顾窗口。

   * Adobe Advertising的用户ID。

   * 用于优化的标准和自定义事件。

1. 在Search、Social和Commerce中，您的实施团队：

   1. 将现有广告网络帐户层次结构同步到Search、Social和Commerce。

   1. 使用“”添加重定向`ef_id`”令牌传递到跟踪URL并将它们发布到广告网络。

   此步骤会在重定向前附加到Adobe Advertising跟踪服务器(除 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 浏览器中支持并行跟踪的广告)，并在广告单击时向URL添加动态填充的“ef_id”参数。 当并行跟踪应用时，最终用户将从广告直接发送到最终URL，并且跟踪模板URL（包含点击测量）将在后台加载。

集成完成后，Search、Social和Commerce会自动接收中跟踪的所有页面上的事件数据 [!DNL Analytics] （对于已配置的报表包）。

>[!MORELIKETHIS]
>
>* [转化跟踪选项](conversion-tracking-about.md)
