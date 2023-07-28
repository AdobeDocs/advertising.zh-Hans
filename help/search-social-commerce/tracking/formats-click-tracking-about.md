---
title: 关于Adobe Advertising转化跟踪服务的点击跟踪URL格式
description: 了解支持的广告网络的点击跟踪格式。
exl-id: 12148caf-fde6-4ac2-b8b4-222409895dd7
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# 关于Adobe Advertising转化跟踪服务的点击跟踪URL格式

使用Adobe Advertising转换跟踪服务的广告帐户和营销活动的跟踪模板、登陆页后缀（最终URL后缀）和目标URL具有以下格式：

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

其中：

* `http://pixel.everesttech.net` 将用户重定向到Adobe Advertising像素服务器。

* `<advertiser_ID>` 是分配给Adobe Advertising内广告商的唯一用户ID的变量。

* `<token passing parameter>` 是适用于以下任一情况的变量：

   * `cq?` 或 `rq` 表示启用了令牌传递。

   * `c?` 或 `r` 表示令牌传递已禁用。

* `<ad network ID>` 是指定广告网络的数字ID的变量，例如 *3* 对象 [!DNL Google Ads]， *10* 对象 [!DNL Microsoft Advertising]， *45* 对象 [!DNL Meta]， *86* 对象 [!DNL Yahoo! Display Network]， *87* 对象 [!DNL Naver]， *88* 对象 [!DNL Baidu]， *90* 对象 [!DNL Yandex]， *94* 对象 [!DNL Yahoo! Japan Ads]， *105* 对象 [!DNL Yahoo Native] （已弃用），或 *106* 对象 [!DNL Pinterest] （已弃用）。

* `<tracking ID>` 是系统生成的跟踪ID字符串的变量，用于标识帐户中唯一的关键字、广告或投放位置。 该字符串因广告网络而异。

* `<the landing page>` 是一个变量，表示最终用户所定向到的网站上的URL。 对于具有目标URL的帐户，该值是一个URL。 对于具有跟踪模板的帐户，该值是一个参数(例如 `{lpurl}`)表示最终URL。

请参阅单独的页面，以指示 [[!DNL Baidu] 格式](formats-click-tracking-baidu.md)， [[!DNL Google Ads] 格式](formats-click-tracking-google.md)， [[!DNL Microsoft Advertising] 格式](formats-click-tracking-microsoft.md)， [[!DNL Naver] 格式](formats-click-tracking-naver.md)， [[!DNL Yahoo! Display Network] 格式](formats-click-tracking-yahoo-display-network.md)， [[!DNL Yahoo! Japan Ads] 格式](formats-click-tracking-yahoo-japan.md)、和 [[!DNL Yandex] 格式](formats-click-tracking-yandex.md).

>[!MORELIKETHIS]
>
>* [上的赞助广告的点击跟踪格式 [!DNL Baidu]](formats-click-tracking-baidu.md)
>* [的点击跟踪格式 [!DNL Google Ads]](formats-click-tracking-google.md)
>* [的点击跟踪格式 [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)
>* [上的赞助广告的点击跟踪格式 [!DNL Naver]](formats-click-tracking-naver.md)
>* [上的赞助广告的点击跟踪格式 [!DNL Yahoo! Japan Ads]](formats-click-tracking-yahoo-japan.md)
>* [上的赞助广告的点击跟踪格式 [!DNL Yahoo! Display Network]](formats-click-tracking-yahoo-display-network.md)
>* [上的赞助广告的点击跟踪格式 [!DNL Yandex]](formats-click-tracking-yandex.md)
