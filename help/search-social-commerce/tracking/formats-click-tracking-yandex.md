---
title: ' [!DNL Yandex]的点击跟踪格式'
description: 了解 [!DNL Yandex] 帐户的点击跟踪格式。
exl-id: bcbd369b-b98d-491c-a921-58bf79e01744
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# [!DNL Yandex]上赞助广告的点击跟踪格式

以下基本目标URL格式适用于赞助广告：

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

示例：

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>`是Adobe Advertising中广告商唯一ID的变量。
>
>* 此格式表示为营销活动启用令牌传递（默认）。 如果禁用令牌传递，请在`<advertiser_ID>`之后将`cq?`替换为`c?`。
>
>* `<the landing page>`是一个变量，它表示最终用户被定向到的网站上的URL。
>
>* `source_type`是匹配类型。
>
>* `source`是广告显示在搜索网站还是基于内容的网站上。
>
>* `position`是广告在块中的位置编号。 对于非搜索流量，值为“0”。
>
>* `position_type`是在[!DNL Yandex]中显示广告的块。 可能的值：“premium”（顶部块）、“other”（右侧块）或“none”（非搜索流量）。

>[!MORELIKETHIS]
>
>* [关于Adobe Advertising转换跟踪服务的点击跟踪URL格式](formats-click-tracking-about.md)
>* [AMO ID格式](/help/integrations/analytics/ids.md#amo-id-formats)
