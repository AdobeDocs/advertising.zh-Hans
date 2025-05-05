---
title: 搜索、社交和Commerce的转化跟踪选项
description: 了解Search、Social和Commerce的转化跟踪选项。
exl-id: 263da6a4-8d72-4882-8784-290a3be6f8fa
feature: Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---

# 搜索、社交和Commerce的转化跟踪选项

搜索、社交和Commerce可以使用转化数据，并通过以下方式进行跟踪：

* **Adobe Advertising跟踪转化：**&#x200B;广告商在每个转化页面上插入一个Adobe Advertising转化跟踪标签。 标记将转化数据发送到跟踪服务器。 您可以使用旧版第三方像素或更新的第一方像素。 请参阅“[每个转化跟踪方法的比较](#conversion-tracking-comparison)”。

* **Adobe Analytics转化：**&#x200B;广告商对所有转化都使用Adobe Analytics跟踪。 此选项需要Adobe Advertising-Adobe Analytics集成。 有关详细信息，请参阅&quot;[Adobe Analytics转化跟踪](conversion-tracking-analytics.md)&quot;。

* **[!DNL Google Analytics]转化：**&#x200B;广告商使用[!DNL Google Analytics]标记跟踪所有转化。 有关自动同步的转化的更多信息，请参阅[[!DNL Google Ads] 搜索、社交和Commerce中的转化数据](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)。

* **跟踪广告商的转化：** (仅限Search、Social和Commerce客户端)广告商为Search、Social和Commerce提供包含在线和离线转化数据的任意组合的信息源文件。 请参阅[使用EF ID馈送的转化跟踪](feed-efid.md)和[使用交易ID馈送的转化跟踪](feed-transaction-id.md)。

## 每种转化跟踪方法的比较 {#conversion-tracking-comparison}

随着浏览器Cookie策略日益严格，了解您当前的跟踪功能并确定较长期的最佳选项至关重要。

| 跟踪方法 | 描述 | 限制 | 优点 | 推荐？ |
|----|----|----|----|----|
| Adobe Analytics | 具有Advertising [Adobe Analytics ](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=zh-Hans)的广告商会自动将其[!DNL Analytics]个标准和自定义事件导入到Adobe Advertising中，以便生成报表和进行优化。 | <ul><li>[!DNL Safari]仅允许七天的转化回顾，在回顾期间重复访问网站时会重置该日期。</li><li> 预计2024年对[!DNL Chrome]有类似的限制。</li></ul> | <ul><li>与[!DNL Analytics]无缝集成</li> <li>查看[!DNL Analytics] Analysis Workspace中的付费搜索数据</li><li>付费搜索以外的权益</li></ul> | 是 |
| 旧版Adobe Advertising像素 | 广告商将旧版Adobe Advertising图像或JavaScript像素添加到其转化页面。 当用户单击广告后到达页面时，将触发该像素。 此方法依赖于第三方Cookie。 | <ul><li>[!DNL Safari]阻止使用此方法的所有转化跟踪。</li><li>预计2024年对[!DNL Chrome]有类似的限制。</li></ul> | 该像素已实施。 但是，您仍然必须[实施附加的ITP映射标记](itp-conversion-mapping-tag.md)。<br><br>推荐：切换到第一方像素。 | 否 |
| Adobe Advertising第一方像素 | 广告商执行以下操作： <ul><li>在整个网站上为[Adobe Experience Cloud ID (ECID)服务](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=zh-Hans)实施JavaScript库。</li><li>将具有ITP映射的Adobe Advertising[JavaScript标记](itp-conversion-mapping-tag.md)添加到任何可通过搜索单击而成为登陆页面的页面（理想情况下，在所有页面上，因为登陆页面可能会随着时间的推移而更改）。 标记允许Adobe Advertising跟踪在登陆页面上将大量数字转换为科学记号的页面上发生的转化事件。</li><li>将Adobe Advertising[JavaScript转化跟踪标记v3](format-conversion-tag-jsv3.md)添加到转化页面。</li></ul> | <ul><li>[!DNL Safari]仅允许七天的转化回顾，在回顾期间重复访问网站时会重置该日期。</li><li>预期2022年在[!DNL Chrome]中有类似的限制。</li></ul> | [!DNL Safari]在七天回顾期间跟踪转化。 由于在回顾时间范围内重复访问网站时会重置回顾，因此该限制不会影响所有[!DNL Safari]用户。 | 否 |
| EFID馈送 | 广告商的搜索帐户设置为生成具有Adobe Advertising唯一ID（令牌）的目标URL/最终URL。 当用户单击广告时，Adobe Advertising会创建一个唯一ID (`EFID`)，并将其显示在最终URL的末尾。 广告商的客户端系统捕获EFID作为由点击产生的转化的唯一标识符，并将其发送到包含EFID、交易日期和转化量度的收入馈送中的Adobe Advertising。 然后，Adobe Advertising使用EFID将转换与原始点击进行匹配。 | <ul><li>广告商必须能够每天捕获EFID并将自动馈送发送到Adobe Advertising。</li><li>转化跟踪时间最长为180天(每个Adobe Advertising)或根据广告商系统的限制。</li></ul> | <ul><li>此方法使用第一方转化数据，因此不受第三方Cookie限制的影响。</li><li>线上和线下转化可在一个馈送中发送。</li><li>无需对网站进行代码更改或标记。</li></ul> | 是 |
| 交易ID馈送[组合馈送] | 广告商将包含唯一交易ID (`ev_transid=&lt;transid&gt;`)参数的Adobe Advertising像素添加到其网页，Adobe Advertising将捕获在像素触发时创建的唯一交易ID。 广告商的客户端系统还捕获[!UICONTROL Transaction ID]并向Adobe Advertising发送收入源，用于具有匹配[!UICONTROL Transaction ID]值的离线转化 | <ul><li>如果广告商正在使用旧像素（阻止触发[!DNL Safari]个像素），则不会捕获ID以用于离线数据。</li><li>馈送未自动。</li></ul> | <ul><li>如果您实施了第一方像素，则在[!DNL Safari]中捕获[!UICONTROL Transaction ID]。</li><li>提供对离线/批准的转化事件的跟踪。</li></ul> | 否 |
| [!DNL Google]转化 | 通过API连接自动将使用[!DNL Google Analytics]标记跟踪的转化导入到Adobe Advertising。 每个转换名称都有一个`&quot;GGL_&quot;`前缀。 | <ul><li>[!DNL Google]通常不跟踪离线数据。</li><li>不包括[!DNL Microsoft Advertising]转化。</li></ul> | [!DNL Google]使用机器学习外推“[建模的转化](https://support.google.com/google-ads/answer/10081327)”。 | 否 |

<!--
| [!DNL Microsoft Advertising] Conversions | Conversions tracked with [!DNL Microsoft Advertising] universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | [!DNL Microsoft Advertising] typically doesn't track offline data. [!DNL Google] conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [关于Adobe Advertising转化跟踪标记](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Analytics转化跟踪](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [使用EF ID馈送的转化跟踪](/help/search-social-commerce/tracking/feed-efid.md)
>* [使用交易ID馈送进行转化跟踪](/help/search-social-commerce/tracking/feed-transaction-id.md)
