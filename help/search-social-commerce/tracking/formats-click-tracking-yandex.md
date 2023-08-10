---
title: 的点击跟踪格式 [!DNL Yandex]
description: 了解的点击跟踪格式 [!DNL Yandex] 帐户。
exl-id: cf1d6c4b-9bcd-4b82-919f-c14dbaff9a76
feature: Search Tracking
source-git-commit: f80d05aa40fd4114e9585220fe747ca7d36a19bb
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# 上的赞助广告的点击跟踪格式 [!DNL Yandex]

以下基本目标URL格式适用于赞助广告：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

示例：

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` 是Adobe Advertising中广告商唯一ID的变量。
>
>* 此格式表示为营销活动启用令牌传递（默认）。 如果禁用令牌传递，则替换 `cq?` 之后 `<advertiser_ID>` 替换为 `c?`.
>
>* `<the landing page>` 是一个变量，表示最终用户所定向到的网站上的URL。
>
>* `source_type`  是匹配类型。
>
>* `source` 是广告显示在搜索网站还是基于内容的网站上。
>
>* `position` 是广告在块中的位置编号。 对于非搜索流量，值为“0”。
>
>* `position_type` 是广告在其中显示的块 [!DNL Yandex]. 可能的值：“premium”（顶部块）、“other”（右侧块）或“none”（非搜索流量）。

>[!MORELIKETHIS]
>
>* [关于Adobe Advertising转化跟踪服务的点击跟踪URL格式](formats-click-tracking-about.md)
>* [AMO ID跟踪代码的格式](skwcid-tracking-parameter.md)
