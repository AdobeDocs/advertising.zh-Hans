---
title: 搜索、社交和商务的转化跟踪选项
description: 了解Search、Social和Commerce的转化跟踪选项。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 0%

---

# 搜索、社交和商务的转化跟踪选项

Adobe广告可以使用转化数据，并通过以下方式跟踪这些数据：

* **Adobe广告跟踪的转化：** 广告商在每个转化页面上插入一个Adobe广告转化跟踪标记。 标记将转化数据发送到跟踪服务器。 您可以使用旧版第三方像素或更新的第一方像素。 参见“[每种转化跟踪方法的比较](#conversion-tracking-comparison).”

* **Adobe Analytics转化：** 广告商对所有转化都使用Adobe Analytics跟踪。 此选项需要AdobeAdvertising-Adobe Analytics集成。 参见“[Adobe Analytics转化跟踪](conversion-tracking-analytics.md)”以了解更多信息。

* **[!DNL Google Analytics]转化：** 广告商使用 [!DNL Google Analytics] 标记以跟踪所有转化。 参见“[[!DNL Google Ads] 搜索、社交和商务中的转化数据](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)”以了解有关自动同步的转换的更多信息。

* **广告商跟踪的转化：** （仅限搜索、社交和商务客户端）广告商为Search、社交和商务提供包含在线和离线转化数据的任意组合的信息源文件。 参见“[使用EF ID馈送的转化跟踪](feed-efid.md)“ ”和“ ”[使用交易ID馈送进行转化跟踪](feed-transaction-id.md).”

## 每种转化跟踪方法的比较 {#conversion-tracking-comparison}

随着浏览器Cookie策略日益严格，了解您当前的跟踪功能并确定较长期的最佳选项非常重要。

| 跟踪方法 | 描述 | 限制 | 优点 | 推荐？ |
|----|----|----|----|----|
| Adobe Analytics | 广告商使用 [适用于广告的Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) 自动导入其 [!DNL Analytics] 标准和自定义事件，用于Adobe广告以实现报表和优化。 | <ul><li>[!DNL Safari] 仅允许查看七天的转化回顾时间，回顾时间范围内重复访问网站时将会重置该时间。</li><li> 在中预期类似的限制 [!DNL Chrome] 在2024年。</li></ul> | <ul><li>与无缝集成 [!DNL Analytics]</li> <li>请参阅中的付费搜索数据 [!DNL Analytics] Analysis Workspace</li><li>付费搜索以外的收益</li></ul> | 是 |
| 旧版Adobe广告像素 | 广告商将旧版Adobe广告图像或JavaScript像素添加到其转化页面。 当用户单击广告到达页面时，像素将触发。 此方法依赖于第三方Cookie。 | <ul><li>[!DNL Safari] 阻止使用此方法的所有转化跟踪。</li><li>在中预期类似的限制 [!DNL Chrome] 在2024年。</li></ul> | 像素已实施。 但是，您仍必须 [实施附加的ITP映射标记](itp-conversion-mapping-tag.md).<br><br>推荐：切换到第一方像素。 | 否 |
| Adobe广告第一方像素 | 广告商执行以下操作： <ul><li>实施适用于的JavaScript库 [Adobe Experience Cloud ID (ECID)服务](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) 在整个网站中搜索。</li><li>添加Adobe广告 [具有ITP映射的JavaScript标记](itp-conversion-mapping-tag.md) 通过搜索单击可转到任何可以作为登陆页面的页面（理想情况下，在所有页面上，因为登陆页面可能会随着时间的推移而更改）。 标记允许Adobe广告跟踪在登陆页面上将大量数字转换为科学记号的页面上发生的转化事件。</li><li>添加Adobe广告 [JavaScript转化跟踪标记v3](format-conversion-tag-jsv3.md) 到转化页面。</li></ul> | <ul><li>[!DNL Safari] 仅允许查看七天的转化回顾时间，回顾时间范围内重复访问网站时将会重置该时间。</li><li>在中预期类似的限制 [!DNL Chrome] 在2022年。</li></ul> | [!DNL Safari] 在七天回顾期间跟踪转化。 由于回溯在回溯时段内重复访问网站时重置，因此该限制不会影响所有 [!DNL Safari] 用户。 | 否 |
| EFID馈送 | 广告商的搜索帐户设置为使用Adobe广告唯一ID（令牌）生成目标URL/最终URL。 当用户单击广告时，Adobe广告会创建一个唯一ID (`EFID`)，并将其显示在最终URL的末尾。 广告商的客户端系统捕获EFID作为由点击产生的转化的唯一标识符，并将其发送到收入源中的Adobe广告，该收入源包括EFID、交易日期和转化属性。 然后，Adobe广告会使用EFID将转化与原始点击进行匹配。 | <ul><li>广告商必须能够捕获EFID，并每天向Adobe广告发送自动馈送。</li><li>转化跟踪时间最长为180天(每个Adobe广告)或根据广告商系统的限制。</li></ul> | <ul><li>此方法使用第一方转化数据，因此不受第三方Cookie限制的影响。</li><li>可以在一个馈送中发送在线和离线转化。</li><li>无需对网站进行代码更改或标记。</li></ul> | 是 |
| 交易ID馈送 [组合馈送] | 广告商添加Adobe广告像素，其中包含唯一交易ID的参数(`ev_transid=&lt;transid&gt;`)，则Adobe广告会捕获在像素触发时创建的唯一交易ID。 广告商的客户端系统还会捕获 [!UICONTROL Transaction ID] 和为Adobe广告发送具有匹配的离线转化的收入源 [!UICONTROL Transaction ID] 值 | <ul><li>如果广告商使用的是旧版像素，而 [!DNL Safari] 阻止触发，则不会捕获ID以用于离线数据。</li><li>馈送未自动化。</li></ul> | <ul><li>如果您实施第一方像素，则 [!UICONTROL Transaction ID] 在中捕获 [!DNL Safari].</li><li>提供对离线/批准的转化事件的跟踪。</li></ul> | 否 |
| Google转化 | 通过跟踪的转化 [!DNL Google Analytics] 标记是通过API连接自动导入到Adobe广告中的。 每个转化名称都有一个 `&quot;GGL_&quot;` 前缀。 | <ul><li>Google通常不跟踪离线数据。</li><li>Microsoft®广告转化不包括在内。</li></ul> | Google使用机器学习来外推&quot;[模型化转化](https://support.google.com/google-ads/answer/10081327).” | 否 |

<table style="table-layout:auto">

<!--
| Microsoft Advertising Conversions | Conversions tracked with Microsoft Advertising universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | Microsoft Advertising typically doesn't track offline data. Google conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [关于Adobe广告转化跟踪标记](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Analytics转化跟踪](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [使用EF ID馈送的转化跟踪](/help/search-social-commerce/tracking/feed-efid.md)
>* [使用交易ID馈送进行转化跟踪](/help/search-social-commerce/tracking/feed-transaction-id.md)

