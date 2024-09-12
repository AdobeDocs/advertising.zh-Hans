---
title: 关于Adobe Advertising转化和页面查看跟踪标记的常见问题解答
description: 请参阅Adobe Advertising转化与页面查看跟踪标记的比较。
exl-id: 2e5ef792-e0f5-4409-bd37-87d9fab1265f
feature: Search Tracking
source-git-commit: e9d55ba2f4b3ce8b1ac19c06fe8759a2f862c480
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# 关于Adobe Advertising转化和页面查看跟踪标记的常见问题解答

以下内容适用于Adobe Advertising转化跟踪标记和页面查看跟踪标记。

| | 带有ECID的JS标记 | JS版本3标记 | JS版本2标记 | 图像标记 |
| ---- | ---- | ---- | ---- | ---- |
| 可以在与其他JS版本相同的网页上使用 | — | — | — | 不适用 |
| 允许在同一网页上使用具有相同广告商用户ID的多个标记 | 是 | 是 | 是 | — |
| 允许在同一网页上使用具有不同广告商用户ID的多个标记 | 是 | 是 | — | — |
| 供Adobe Experience Platform的Adobe Advertising扩展使用，并与使用Experience Platform生成的其他标记兼容 | 是 | 是 | — | — |
| 允许将源自[!DNL Apple Safari]和[!DNL Mozilla Firefox]的所有转化与Adobe AdvertisingJavaScript转化映射标记一起使用时进行跟踪 | 是 | 是 | 是 | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* 所有新的实施都使用JavaScript版本3。
>* 带ECID的JavaScript标记使用[Adobe Experience Cloud ID (ECID)服务](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html)以及旧版ef_id和gsurferid来度量转化。 此最新标记创建[第一方Experience Clouds_ecid Cookie](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html)，并提供与其他Experience Cloud产品更紧密的集成。
>* 仅当已在广告商的网页上实施标记时，才使用JavaScript版本2标记。
>* 最佳实践是使用JavaScript标记，而不是图像标记，除非网站有禁止使用这些标记的策略。
>* 广告商需要使用JavaScript标签，它们需要定位在Adobe Experience Cloud中创建、在Adobe Audience Manager中创建或从Audience Manager或Adobe Analytics发布到Adobe Experience Cloud的受众。

>[!MORELIKETHIS]
>
>* [关于Adobe Advertising转化跟踪标记](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [生成Adobe Advertising转换标记](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [JavaScript转换跟踪标记版本3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [JavaScript转换跟踪标记版本2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)的格式
>* [图像转换跟踪标记的格式](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!-- add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
