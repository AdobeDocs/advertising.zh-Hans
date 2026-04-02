---
title: Adobe Analytics转化跟踪
description: 了解如何在Adobe Advertising中对营销活动使用Adobe Analytics转化跟踪。
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
TQID: https://experienceleague.adobe.com/CM0S4RvR4RJ5Ylta5EJTdZh-VDDHYIfa7Qsd1Dm4D78
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 297
ht-degree: 0%

---

# Adobe Analytics转化跟踪

*仅集成Adobe Advertising-Adobe Analytics的广告商*

对于集成Adobe Advertising-Adobe Analytics的广告商，当您在您的[!DNL Analytics]竞价单位`ef_id`的点击跟踪URL中使用带有令牌（[参数）的重定向时，Advertising Cloud可以将您的广告点击次数和展示次数与](/help/search-social-commerce/glossary.md#a-b)跟踪的网站参与度和转化量度关联起来。 [!DNL Analytics]数据通过每日馈送文件自动发送到Advertising Cloud。

有关集成的详细信息，请参阅[概述 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/en/docs/advertising/integrations/analytics/overview){target="_blank"}。

>[!PREREQUISITES]
>
> 搜索、社交和Commerce广告商帐户、[!DNL Analytics]报表包和广告网络帐户中的时区必须匹配。 如果两者不匹配，则会在系统间发生数据差异。

## 实施概述

1. 在[!DNL Analytics]中，您的Search、Social和Commerce实施团队修改了每个报表包的以下配置设置：

   * `ef_id` [!DNL eVar]的过期时间已更改为与Adobe Advertising的广告商点击回顾时间范围相匹配。

   * Adobe Advertising用户ID。

   * 用于优化的标准和自定义事件。

1. 在Search、Social和Commerce中，您的实施团队将：

   1. 将现有的广告网络帐户层次结构同步到Search、Social和Commerce中。

   1. 添加带有传递给跟踪URL的“`ef_id`”令牌的重定向，并将它们发布到广告网络。

   此步骤会在重定向前附加到Adobe Advertising跟踪服务器（支持并行跟踪的浏览器中的[!DNL Google Ads]和[!DNL Microsoft Advertising]广告除外），并在广告单击时向URL添加动态填充的“ef_id”参数。 当并行跟踪应用时，最终用户将从广告直接发送到最终URL，并且跟踪模板URL（包含点击测量）将在后台加载。

集成完成后，Search、Social和Commerce会自动接收在[!DNL Analytics]中为配置的报表包跟踪的所有页面上的事件数据。

>[!MORELIKETHIS]
>
>* [转化跟踪选项](conversion-tracking-about.md)
