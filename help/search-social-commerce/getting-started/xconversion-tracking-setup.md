---
title: 为网页设置转化跟踪
description: 了解如何启用Adobe广告以跟踪由广告展示次数和点击量产生的转化。
source-git-commit: cd8367fbae2234cfdb937c5da8f21f94a615e92a
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# 为网页设置转化跟踪

<!-- I don't think this is necessary here -- we already have a bullet point in the implementation overview -- so removing from TOC. -->

在生成转化数据报表之前，Adobe广告需要每个关键词和广告的展示次数、点击次数、成本和转化（交易）数据。 Adobe广告还使用此数据构建所需的数据预测模型，以优化促销活动预算以及关键词和广告的竞价。

要启用Adobe广告以跟踪由广告展示次数和点击量产生的转化，您需要执行以下操作：

* 在Search、Social和Commerce管理的每个广告促销活动的每个关键词、广告、投放位置、站点链接和产品组的跟踪模板或目标URL中包含唯一的点击跟踪代码（可能还包括用于将最终用户重定向到跟踪服务器的附加代码）。 这允许Adobe广告跟踪每个广告展示（仅适用于展示广告和社交广告）以及每次点击广告。

* 通过以下方式之一跟踪转化数据：

   * **Adobe广告跟踪的转化：** 广告商在每个转化页面上插入一个Adobe广告转化跟踪标记。

   * **Adobe Analytics转化：** 广告商对所有转化都使用Adobe Analytics跟踪。

   * **[!DNL Google Analytics]转化：** 广告商使用 [!DNL Google Analytics] 标记以跟踪所有转化。

   * **广告商跟踪的转化：** 广告商提供包含在线和离线转化数据的任意组合的每日馈送文件。

有关实施跟踪的详细信息，请参阅有关“跟踪”的帮助章节。

>[!MORELIKETHIS]
>
>* [生成Adobe广告转化标记](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [使用跟踪URL工具生成搜索、社交和商务点击跟踪URL](/help/search-social-commerce/tools/click-tracking-url-generate.md)
>* [解码搜索、社交和商务点击跟踪URL](/help/search-social-commerce/tools/click-tracking-url-decode.md)

