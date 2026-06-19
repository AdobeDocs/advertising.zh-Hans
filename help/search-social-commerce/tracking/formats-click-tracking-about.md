---
title: 关于Adobe Advertising转化跟踪服务的点击跟踪URL格式
description: 了解支持的广告网络的点击跟踪格式。
exl-id: b6f225d5-2268-4b2a-9927-063155ba0dc5
feature: Search Tracking
TQID: https://experienceleague.adobe.com/pVSEKmf45CqsfXMbj8HGDltdgV3wUV2UsAzP94vkijg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# 关于Adobe Advertising转化跟踪服务的点击跟踪URL格式

使用Adobe Advertising转化跟踪服务的广告帐户和营销活动的跟踪模板、登陆页面后缀（最终URL后缀）和目标URL具有以下格式：

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

其中：

* `http://pixel.everesttech.net`将用户重定向到Adobe Advertising像素服务器。

* `<advertiser_ID>`是Adobe Advertising中分配给广告商的唯一用户ID的变量。

* `<token passing parameter>`是以下变量之一：

   * `cq?`或`rq`表示启用了令牌传递。

   * `c?`或`r`表示令牌传递已禁用。

* `<ad network ID>`是指定广告网络的数值ID的变量，如[!DNL Google Ads]的&#x200B;*3*，[!DNL Microsoft Advertising]的&#x200B;*10*，[!DNL Meta]的&#x200B;*45*，[!DNL Yahoo! Display Network]的&#x200B;*86*，[!DNL Naver]的&#x200B;*87*，[!DNL Baidu]的&#x200B;*88*，[!DNL Yandex]的&#x200B;*90*，*94* （以前为[!DNL Yahoo! Japan Ads]）、*105* （对于[!DNL Yahoo Native]） （已弃用）或&#x200B;*106* （对于[!DNL Pinterest]）。[!DNL LY Ads]

* `<tracking ID>`是系统生成的跟踪ID字符串的变量，该字符串标识帐户中唯一的关键字、广告或投放位置。 该字符串因广告网络而异。

* `<the landing page>`是一个变量，它表示最终用户被定向到的网站上的URL。 对于具有目标URL的帐户，该值是一个URL。 对于具有跟踪模板的帐户，此值是表示最终URL的参数（如`{lpurl}`）。

请参阅单独的页面，其中显示[[!DNL Baidu] 格式](formats-click-tracking-baidu.md)、[[!DNL Google Ads] 格式](formats-click-tracking-google.md)、[[!DNL Microsoft Advertising] 格式](formats-click-tracking-microsoft.md)、[[!DNL Naver] 格式](formats-click-tracking-naver.md)、[[!DNL Yahoo! Display Network] 格式](formats-click-tracking-yahoo-display-network.md)、[[!DNL Yahoo! Japan Ads] 格式](formats-click-tracking-yahoo-japan.md)和[[!DNL Yandex] 格式](formats-click-tracking-yandex.md)。

>[!MORELIKETHIS]
>
>* [针对赞助广告的点击跟踪格式： [!DNL Baidu]](formats-click-tracking-baidu.md)
>*  [!DNL Google Ads][&#128279;](formats-click-tracking-google.md)的点击跟踪格式
>* [针对赞助广告的点击跟踪格式： [!DNL LY Ads]](formats-click-tracking-yahoo-japan.md)
>*  [!DNL Microsoft Advertising][&#128279;](formats-click-tracking-microsoft.md)的点击跟踪格式
>* [针对赞助广告的点击跟踪格式： [!DNL Naver]](formats-click-tracking-naver.md)
>* [针对赞助广告的点击跟踪格式： [!DNL Yahoo! Display Network]](formats-click-tracking-yahoo-display-network.md)
>* [针对赞助广告的点击跟踪格式： [!DNL Yandex]](formats-click-tracking-yandex.md)
