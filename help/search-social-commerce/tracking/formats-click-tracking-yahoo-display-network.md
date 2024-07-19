---
title: ' [!DNL Yahoo! Display Network]的点击跟踪格式'
description: 了解 [!DNL Yahoo! Display Network] 帐户的点击跟踪格式。
exl-id: ee6642b3-fb84-4604-91cc-da1213835be8
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '89'
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
>* 此格式表示为营销活动启用令牌传递（默认）。 如果禁用令牌传递，请在`<advertiser_ID>`之后将`cq?`替换为`c?`。
>
>* `<the landing page>`是一个变量，它表示最终用户被定向到的网站上的URL。

>[!MORELIKETHIS]
>
>* [关于Adobe Advertising转换跟踪服务的点击跟踪URL格式](formats-click-tracking-about.md)
>* [AMO ID格式](/help/integrations/analytics/ids.md#amo-id-formats)
