---
title: “[!DNL Baidu]关键字设置”
description: 引用 [!DNL Baidu] 关键字的设置。
exl-id: 3b3a578b-06f1-486f-9ade-9104e0a1dd5f
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# [!DNL Baidu]关键字设置

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：**&#x200B;关键字。 每个关键字的最大长度为30个单字节字符或15个双字节字符

最多可以输入或粘贴2000个关键字。 用逗号分隔多个关键字，或在单独的行中输入它们。 使用以下语法：

* 广泛匹配的`keyword`
* `"keyword"`匹配短语
* `[keyword]`进行完全匹配

>[!NOTE]
>
>* [!DNL Baidu]仅允许每个广告组的每个关键字有一个匹配类型。 例如，广告组1不能同时包括`"keyword"`和`[keyword]`。
>* 您可以从[!UICONTROL Keywords] > [!UICONTROL Negatives]视图、广告组和促销活动设置中创建负关键字。
>* 更改[!DNL Baidu]关键字会删除现有关键字，并使用新的关键字ID创建新关键字。 但是，更改匹配类型不会删除现有关键字。

**[!UICONTROL Status]：**&#x200B;关键字的显示状态： *活动*&#x200B;或&#x200B;*已暂停*。 新关键字的默认值为&#x200B;*活动*。

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## URL选项

**[!UICONTROL Base URL]：** （仅具有关键词级别跟踪的营销活动；可选）用户单击您的广告时获得的登陆页面URL。 其中可能包括
第三方重定向和跟踪代码。 如果输入值，则会覆盖广告的基本URL。

保存记录后，基本URL将包含为促销活动或帐户配置的任何附加参数。

如果您使用Adobe Advertising转化跟踪服务，并且促销活动设置包括使用[!UICONTROL EF Redirect]和在关键词级别添加跟踪，则Search、Social和Commerce会自动添加其自身的点击跟踪代码。

>[!MORELIKETHIS]
>
>* [管理关键字](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
