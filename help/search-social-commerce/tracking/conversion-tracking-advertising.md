---
title: 关于Adobe Advertising转化跟踪标签
description: 了解如何使用Adobe Advertising转化跟踪标签。
exl-id: 07403d60-6db2-47e7-977b-4b59c8797c3d
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# 关于Adobe Advertising转化跟踪标签

Adobe Advertising使用Adobe Advertising转化跟踪标记(在发生转化事件时，这些标记会插入到打开的网页（例如“成功”页面）中)跟踪因广告点击量导致的转化。 标记包括嵌入信息，用于将交易数据以及用户的Adobe AdvertisingCookie发送到跟踪服务器，从该服务器，交易被贷记到适当的广告点击或展示（根据广告商的转化归因设置）。

>[!NOTE]
>
>如果用户没有有效的Cookie，则Adobe Advertising不会报告转化。

对于要跟踪的每组转化量度，您必须创建一个单独的转化标记。 向广告商或代理机构提供要在其上插入每个标签的网页列表。 您可以生成以下任一类型的转化标记。 请参阅&quot;[生成Adobe Advertising转换标记](/help/search-social-commerce/tools/conversion-tag-generate.md)”以获取说明。

* （推荐）JavaScript标记（版本3或版本2），这些标记在网页中不可见。

* HTML图像标签以在网页上显示1像素x 1像素的透明图像（像素），最终用户看不到这些图像。 仅当公司制定了禁止使用JavaScript标记的政策时，才使用图像标记。

有关标记类型之间差异的更多信息，请参阅&quot;[关于Advertising Cloud转化跟踪标记的常见问题解答](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)“

>[!NOTE]
>
>* 此功能不会将图像标记或JavaScript标记添加到广告商的网页。 必须按照广告商更新网页的正常过程添加标记。
>* 确保考虑实施标记将需要多长时间。 根据公司的策略，实施可能需要几周甚至几个月。

## Adobe Advertising转化跟踪标签的功能

转化跟踪像素允许Adobe Advertising执行以下操作：

* 跟踪和报告搜索促销活动关键词级别的转化数据。

* 跨所有营销渠道（付费搜索和显示）在广告（创意）级别跟踪和报告转化数据，这有助于创意测试。

* 在所有营销渠道的交易级别跟踪和报告转化数据。

* 显示转化在不同营销渠道中的分配方式，以便您查看哪个最有效。

* 报告并优化不同的归因级别（例如，将转化归因到最后一个相关事件或平均加权所有事件）。

* 提供对点击协助（搜索关键词或构成转化漏斗的投放位置）和渠道协助（构成转化漏斗的用户事件，可能跨多个营销渠道）的可见性。

* 提供对网站流量和转换的地理分布和反向链接域的可见性，以使您可优化地理位置和网站定位。

* 分析每周或每天的趋势，这可用于提高转化率。

>[!MORELIKETHIS]
>
>* [转化跟踪选项](conversion-tracking-about.md)
>* [生成Adobe Advertising转换标记](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [JavaScript转换跟踪标记版本3的格式](format-conversion-tag-jsv3.md)
>* [JavaScript转换跟踪标记版本2的格式](format-conversion-tag-jsv2.md)
>* [图像转换跟踪标记的格式](format-conversion-tag-image.md)
>* [有关转化和页面查看跟踪标记的常见问题解答](faqs-conversion-page-view-tracking-tags.md)
>* [Adobe AdvertisingJavaScript转换映射标记](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
