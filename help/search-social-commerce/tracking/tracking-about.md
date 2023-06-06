---
title: 关于搜索、社交和商务的跟踪
description: 了解搜索、社交和商务的跟踪选项。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# 关于搜索、社交和商务的跟踪

要跟踪广告效果，搜索、社交和商务需要广告的展示次数、点击次数、成本和转化（交易）数据。 Search、Social和Commerce使用此数据构建优化广告组合所需的数据预测模型。

## 成本、点击次数和展示数据

搜索、Social和Commerce直接从检索展示次数、点击次数和成本数据 [支持的广告网络](/help/search-social-commerce/introduction/supported-inventory.md) 每天。 此外，Search、Social和Commerce还可以在跟踪模板和目标URL中添加唯一的点击跟踪代码（包括重定向到跟踪服务器），以跟踪显示/内容展示次数、点击次数和成本，并在以后将事件与转化相关联。

如果要跟踪搜索、社交和商务不同步数据的广告网络上的促销活动，则必须通过发送包含展示、点击和成本数据的每日信息源文件来提供这些促销活动的数据。

### 点击跟踪标记

您的Search、Social和Commerce实施团队通过在同步的广告促销活动中更新广告、关键字、投放位置、产品组和站点链接扩展的跟踪模板和目标URL来设置点击跟踪，以包含唯一的跟踪ID字符串和Adobe广告重定向。 它们还会将跟踪添加到您的登陆页面后缀（最终URL后缀） [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 帐户和营销活动。

利用跟踪参数，Adobe广告可以跟踪单个关键词级别（搜索促销活动）或广告变体级别（具有内容或网站定位的搜索促销活动、展示促销活动以及社交促销活动）的点击量。 每当用户查看显示/内容广告或单击您的某个广告时，广告网络就会使用与关键词或广告关联的点击跟踪标记，将事件发送到Adobe广告像素服务器。 对于点击：

* 对于支持并行跟踪的浏览器上的Google Ads和Microsoft Advertising广告，广告网络会先将点击发送到您的网站，然后发送到AdobeAdvertising像素服务器，然后这些服务器会在用户的计算机上放置一个Cookie（如果尚未存在）。

* 在所有其他情况下，广告网络会将点击直接发送到Adobe广告像素服务器。 像素服务器会在用户的计算机上放置一个Cookie（如果尚不存在），然后将用户重定向到您网站上的相关URL。 最终用户的整体体验与没有重定向时的体验相同。

Cookie是在 [!DNL Adobe] 域(`everesttech.net`)作为第一方Cookie。 在重定向后，用户位于广告商的域中，然后Cookie会被视为第三方Cookie。 有关AdobeAdvertising Cookie的更多信息，请参阅“[Adobe广告Cookie](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-advertising-cloud.html).”

## 转化数据

当客户点击广告或查看显示或社交广告时，Search、Social和Commerce需要将每个生成的转化映射回原始点击或显示/社交展示。

广告商在提供所有点击和显示/社交印象的转化数据方面发挥作用。 转化数据可以包含有关网站上发生的任何类型事件的信息，这些信息可用于竞价优化。 您可以通过在广告商的转化页面（例如，客户完成交易后显示的“成功”页面）中实施转化跟踪代码，或者发送包含由其他方法捕获的转化数据的每日馈送文件，来提供转化数据。

### 转化跟踪标记

您可以使用 [来自不同供应商的转化标记](/help/search-social-commerce/tracking/conversion-tracking-about.md).

当您使用Adobe广告转化标记并且用户完成一个成功的交易并登陆“成功”页面时，Adobe广告像素服务器会检查用户计算机上是否存在在单击重定向时设置的Cookie。 当它找到Cookie时，使用ef_transid参数传递有关交易事件的信息，该交易被识别为转化，并计入前一个广告点击或显示展示。

如果用户点击了您的多个广告，则Adobe广告会将交易计入最终广告点击或（对于显示或视频促销活动）最终广告展示次数中，除非您另有指定。 您的 [单击回顾窗口](/help/search-social-commerce/glossary.md#c-d) 和 [展示回顾窗口](/help/search-social-commerce/glossary.md#i-j) 确定付费点击或显示/视频展示（分别）发生后事件可归因于转化的天数。

Adobe广告实施团队与广告商合作，确定广告商需要实施的转化标记的格式，确定应在其中插入每个转化标记的网页，然后提供要实施的转化标记。
