---
title: 使用交易ID馈送进行转化跟踪
description: 了解如何将交易ID馈送用于转化跟踪数据。
exl-id: 58f231a6-970b-46b4-824b-67b3d3f83051
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# 使用交易ID馈送进行转化跟踪

当广告商同时具有在线和离线交易时，Adobe Advertising可以通过Adobe Advertising转化跟踪像素跟踪在线交易，广告商可以使用交易ID跟踪离线交易，并通过馈送进行投放：

* 对于在线交易，Adobe Advertising会跟踪您的广告点击量以及网站上产生的交易。

* 广告商必须跟踪离线转化并将事务级信息源文件发送到Adobe Advertising。

## 实施概述

*代理客户经理， [!DNL Adobe] 仅帐户管理员和管理员用户角色*

1. 使用帐户或营销活动跟踪选项»[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]»为帐户或营销活动中的每个关键字（用于关键字级别的跟踪）或广告（用于广告级别的跟踪）自动生成目标URL或最终URL。

1. 为在线转化设置Adobe Advertising转化跟踪。 此过程与使用基于Adobe Advertising像素的转化跟踪的广告商相同。 生成包含唯一交易ID参数(`ev_transid=<transid>`)。

1. 对于每个交易的离线部分，广告商生成在交易的在线部分中使用的相同交易ID以包含在馈送文件中。

1. 广告商上传一个文件，其中 [必需的转化数据](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) 到指定的服务器位置。

1. 技术服务会解析上传文件中的转化数据，然后将该数据上传到Adobe Advertising。 然后，Adobe Advertising根据各个关键字、广告和投放位置跟踪数据，并为每个关键字、广告和投放位置创建收入预测。

1. 技术服务根据馈送数据验证处理过的数据并检查任何 [孤立事务](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [转换信息源文件的文件要求](feed-file-requirements.md)
>* [使用交易ID的数据馈送的数据要求](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
