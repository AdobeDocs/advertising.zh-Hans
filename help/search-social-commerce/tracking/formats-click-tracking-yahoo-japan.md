---
title: 的点击跟踪格式 [!DNL Yahoo! Japan Ads]
description: 了解的点击跟踪格式 [!DNL Yahoo! Japan Ads] 帐户。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# 上的赞助广告的点击跟踪格式 [!DNL Yahoo! Japan Ads]

以下基本跟踪模板格式适用于赞助广告：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

或者，当为中的帐户设置了自动标记选项时 [!DNL Yahoo! Japan Ads]：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

示例：

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

>[!NOTE]
>
>* `<advertiser_ID>` 是Adobe广告中广告商唯一ID的变量。
>
>* 此格式表示已为营销活动启用令牌传递（默认）。 如果禁用令牌传递，请替换 `cq?` 之后 `<advertiser_ID>` 替换为 `c?`.
>
>* `<the landing page>` 是一个变量，表示最终用户被定向到的网站上的URL。


>[!MORELIKETHIS]
>
>* [关于Adobe广告转化跟踪服务的点击跟踪URL格式](formats-click-tracking-about.md)
>* [s\_kwcid跟踪代码的格式](skwcid-tracking-parameter.md)
