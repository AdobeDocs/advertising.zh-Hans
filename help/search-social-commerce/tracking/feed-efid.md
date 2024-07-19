---
title: 使用EF ID馈送的转化跟踪
description: 了解如何将EF ID馈送用于转化跟踪数据。
exl-id: fd065313-3d27-4bb9-a934-e815e02cf405
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# 使用EF ID馈送的转化跟踪

在此方法中，Advertising Cloud会在用户每次点击和广告并到达登陆页面时收集一个`ef_id`值，广告商将该`ef_id`值与转化数据一起存储并在数据馈送中发送。

## 实施概述

*仅代理帐户管理员、[!DNL Adobe]帐户管理员和管理员用户角色*

1. 使用帐户或营销活动跟踪选项“[!UICONTROL EF Redirect]”、重定向类型“[!UICONTROL Token]”和“[!UICONTROL Auto Upload]”，为帐户或营销活动中的每个关键字（用于关键字级别的跟踪）或广告（用于广告级别的跟踪）自动生成包含Adobe Advertising令牌(ef_id)的目标URL或最终URL。

   >[!NOTE]
   >* 此方法不需要广告商使用Adobe Advertising转化跟踪标签。
   >* 如果您将现有帐户或营销活动的重定向类型从[!UICONTROL Standard]切换为[!UICONTROL Token]，或反之，则必须重新生成所有适用的跟踪URL。

   最终用户单击广告时，会填充ef_id并将其附加到登陆页面URL，然后会重定向到Adobe Advertising服务器。 随后，ef_id会传递到广告或关键字的目标URL或最终URL中的广告商。 以下是在重定向期间传递到广告商的目标URL示例：

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. 广告商从重定向中提取ef_id，并将其与相关的转化数据一起存储以包含在馈送文件中。 请勿更改ef_id或更改其大小写。

1. （可选，但是推荐）广告商可以为要包含在馈送文件中的每个交易创建唯一的交易ID。

1. 广告商将包含[所需转化数据](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)的文件上载到指定的服务器位置。

1. 技术服务会解析上传文件中的转化数据，然后将该数据上传到Adobe Advertising。 然后，Adobe Advertising根据各个关键字、广告和投放位置跟踪数据，并为每个关键字、广告和投放位置创建收入预测。

1. 技术服务将根据馈送数据验证已处理的数据并检查任何[孤立事务](/help/search-social-commerce/glossary.md#o-p)。

>[!MORELIKETHIS]
>
>* [转换信息源文件的文件要求](feed-file-requirements.md)
>* [使用EF ID的数据馈送的数据要求](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
