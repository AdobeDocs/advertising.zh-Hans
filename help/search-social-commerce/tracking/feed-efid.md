---
title: 使用EF ID馈送的转化跟踪
description: 了解如何将EF ID馈送用于转化跟踪数据。
source-git-commit: 46e918418bf2e5c412efa8825dda22bc1953e439
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# 使用EF ID馈送的转化跟踪

在此方法中，Advertising Cloud收集 `ef_id` 值。 `ef_id` 值，并在数据馈送中发送。

## 实施概述

*代理客户经理， [!DNL Adobe] 仅帐户管理员和管理员用户角色*

1. 使用帐户或营销活动跟踪选项»[!UICONTROL EF Redirect]，”的重定向类型“[!UICONTROL Token]，”和“[!UICONTROL Auto Upload]»为帐户或营销活动中的每个关键字（用于关键字级别的跟踪）或广告（用于广告级别的跟踪）自动生成带有Adobe广告令牌(ef_id)的目标URL或最终URL。

   >[!NOTE]
   >* 此方法不需要广告商使用Adobe Advertising转化跟踪标签。
   >* 如果从切换现有帐户或营销活动的重定向类型 [!UICONTROL Standard] 到 [!UICONTROL Token]，反之亦然，则必须重新生成所有适用的跟踪URL。

   当最终用户单击广告时，会填充ef_id并将其附加到登陆页面URL，然后被重定向到Adobe Advertising服务器。 然后，在广告或关键字的目标URL或最终URL中，将ef_id传递到广告商。 以下是在重定向期间传递到广告商的目标URL示例：

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. 广告商从重定向中提取ef_id，并将其与相关的转化数据一起存储以包含在馈送文件中。 请勿更改ef_id或更改其大小写。

1. （可选，但推荐）广告商可以为要包含在馈送文件中的每个交易创建唯一的交易ID。

1. 广告商上传一个文件，其中包含 [所需的转化数据](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) 到指定的服务器位置。

1. 技术服务会解析上传文件中的转化数据，然后将该数据上传到Adobe广告中。 然后，Adobe广告会根据各个关键词、广告和投放位置跟踪数据，并为每个关键词和广告创建收入预测。

1. 技术服务根据馈送数据验证处理过的数据并检查任何 [孤立事务](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [转换信息源文件的文件要求](feed-file-requirements.md)
>* [使用EF ID的数据馈送的数据要求](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)


