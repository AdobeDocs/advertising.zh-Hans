---
title: 的点击跟踪格式 [!DNL Baidu]
description: 了解的点击跟踪格式 [!DNL Baidu] 帐户。
exl-id: a57ff0cf-0bcf-4d55-9a86-7551db8a08e7
feature: Search Tracking
source-git-commit: f80d05aa40fd4114e9585220fe747ca7d36a19bb
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# 上的赞助广告的点击跟踪格式 [!DNL Baidu]

以下基本目标URL格式适用于赞助广告：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_cmpid=<campaignID>&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=<the landing page>`

示例：

`http://pixel.everesttech.net/1234/cq?ev_sid=88&ev_cmpid=800577124&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` 是Adobe Advertising中广告商唯一ID的变量。
>
>* 此格式表示为营销活动启用令牌传递（默认）。 如果禁用令牌传递，则替换 `cq?` 之后 `<advertiser_ID>` 替换为 `c?`.
>
>* `<campaignID>` 是数值促销活动ID的变量。
>
>* `<the landing page>` 是一个变量，表示最终用户所定向到的网站上的URL。

>[!MORELIKETHIS]
>
>* [关于Adobe Advertising转化跟踪服务的点击跟踪URL格式](formats-click-tracking-about.md)
>* [AMO ID跟踪代码的格式](skwcid-tracking-parameter.md)
