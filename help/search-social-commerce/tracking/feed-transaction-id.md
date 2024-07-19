---
title: 使用交易ID馈送进行转化跟踪
description: 了解如何将交易ID馈送用于转化跟踪数据。
exl-id: 3341ac20-d435-4387-99da-7b874e53c2e7
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# 使用交易ID馈送进行转化跟踪

当广告商同时具有在线和离线交易时，Adobe Advertising可以通过Adobe Advertising转化跟踪像素跟踪在线交易，广告商可以使用交易ID跟踪离线交易，并通过馈送进行投放：

* 对于在线交易，Adobe Advertising会跟踪您的广告点击量以及网站上产生的交易。

* 广告商必须跟踪离线转化并将事务级信息源文件发送到Adobe Advertising。

## 实施概述

*仅代理帐户管理员、[!DNL Adobe]帐户管理员和管理员用户角色*

1. 使用帐户或营销活动跟踪选项“[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]”为帐户或营销活动中的每个关键字（用于关键字级别的跟踪）或广告（用于广告级别的跟踪）自动生成目标URL或最终URL。

1. 为在线转化设置Adobe Advertising转化跟踪。 此过程与使用基于Adobe Advertising像素的转化跟踪的广告商相同。 生成包含唯一交易ID (`ev_transid=<transid>`)参数的转化标记很重要。

1. 对于每个交易的离线部分，广告商生成在交易的在线部分中使用的相同交易ID以包含在馈送文件中。

1. 广告商将包含[所需转化数据](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)的文件上载到指定的服务器位置。

1. 技术服务会解析上传文件中的转化数据，然后将该数据上传到Adobe Advertising。 然后，Adobe Advertising根据各个关键字、广告和投放位置跟踪数据，并为每个关键字、广告和投放位置创建收入预测。

1. 技术服务将根据馈送数据验证已处理的数据并检查任何[孤立事务](/help/search-social-commerce/glossary.md#o-p)。

>[!MORELIKETHIS]
>
>* [转换信息源文件的文件要求](feed-file-requirements.md)
>* [使用交易ID的数据馈送的数据要求](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
