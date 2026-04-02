---
title: ' [!DNL Yahoo! Display Network]的点击跟踪格式'
description: 了解 [!DNL Yahoo! Display Network] 帐户的点击跟踪格式。
exl-id: ee6642b3-fb84-4604-91cc-da1213835be8
feature: Search Tracking
TQID: https://experienceleague.adobe.com/sQo6hr3UHQwN9GgazCKv2ba-m4ZXf2ZrhdemCpbVYvU
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 90
ht-degree: 0%

---

# [!DNL Yahoo! Display Network]上赞助广告的点击跟踪格式

以下基本目标URL格式适用于赞助广告：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=86&ev_cl={ef_uniqueid}&url=<the landing page>`

示例：

`http://pixel.everesttech.net/1234/cq?ev_sid=86&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>`是Adobe Advertising中广告商唯一ID的变量。
>
>* 此格式表示为营销活动启用令牌传递（默认）。 如果禁用令牌传递，请在`cq?`之后将`<advertiser_ID>`替换为`c?`。
>
>* `<the landing page>`是一个变量，它表示最终用户被定向到的网站上的URL。

>[!MORELIKETHIS]
>
>* [关于Adobe Advertising转化跟踪服务的点击跟踪URL格式](formats-click-tracking-about.md)
>* [AMO ID格式](https://experienceleague.adobe.com/zh-hans/docs/analytics/components/dimensions/amo-id#dimension-items)
