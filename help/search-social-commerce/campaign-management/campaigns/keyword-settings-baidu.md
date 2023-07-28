---
title: ’[!DNL Baidu] 关键字设置
description: 引用设置 [!DNL Baidu] 关键字。
exl-id: 70ecb5da-1056-4d87-82ba-ac03e0c81761
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# [!DNL Baidu] 关键词设置

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：** 关键字。 每个关键字的最大长度为30个单字节字符或15个双字节字符

最多可以输入或粘贴2000个关键字。 用逗号分隔多个关键字，或在单独的行中输入它们。 使用以下语法：

* `keyword` 进行广泛比赛
* `"keyword"` 用于短语匹配
* `[keyword]` 进行精确匹配

>[!NOTE]
>
>* [!DNL Baidu] 每个广告组仅允许每个关键字有一种匹配类型。 例如，广告组1不能同时包含两者 `"keyword"` 和 `[keyword]`.
>* 您可以从以下位置创建负关键字 [!UICONTROL Keywords] > [!UICONTROL Negatives] 在广告组和营销活动设置中查看和。
>* 更改 [!DNL Baidu] 关键字删除现有关键字，并使用新关键字ID创建新关键字。 但是，更改匹配类型不会删除现有关键字。

**[!UICONTROL Status]：** 关键字的显示状态： *活动* 或 *已暂停*. 新关键字的默认值为 *活动*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## URL选项

**[!UICONTROL Base URL]：** （仅限具有关键词级别跟踪的促销活动；可选）用户在单击您的广告时将被带入的登陆页面URL。 它可以包含第三方重定向和跟踪代码。 如果输入值，则会覆盖广告的基本URL。

保存记录后，基本URL将包含为促销活动或帐户配置的任何附加参数。

如果您使用Adobe Advertising转化跟踪服务，并且促销活动设置包括使用 [!UICONTROL EF Redirect] 并在关键词级别添加跟踪，则Search、Social和Commerce会自动添加其自身的点击跟踪代码。

>[!MORELIKETHIS]
>
>* [管理关键字](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
