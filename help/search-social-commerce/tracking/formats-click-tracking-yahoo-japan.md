---
title: ' [!DNL Yahoo! Japan Ads]的点击跟踪格式'
description: 了解 [!DNL Yahoo! Japan Ads] 帐户的点击跟踪格式。
exl-id: 79e45205-5c72-4612-9b60-36538e3c48c4
feature: Search Tracking
TQID: https://experienceleague.adobe.com/ZFNzA0bfxKhlNW6fvPWMwBc4naT7rOhvym-wSpxvYXg
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 0%

---

# [!DNL Yahoo! Japan Ads]上赞助广告的点击跟踪格式

以下基本跟踪模板格式适用于赞助广告：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

或者，当在[!DNL Yahoo! Japan Ads]中为帐户设置了自动标记选项时：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

示例：

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

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
>* [AMO ID格式](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
