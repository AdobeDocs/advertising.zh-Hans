---
title: ”[!DNL Google Ads] 关键词设置”
description: 引用设置 [!DNL Google Ads] 关键字。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# [!DNL Google Ads] 关键词设置

您可以为使用搜索和显示网络的营销活动创建关键词。

请参阅Google Ads帮助，了解 [每个帐户的关键字限制](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：** 关键字，包括任何 [!DNL Google Ads] 匹配关键字和占位符的语法。 [!DNL Google Ads] 帐户需要具有以下属性的关键字：

* 每个关键字的最大长度为80个字符，不超过10个单词。
* 关键字只能包含字母、数字和以下特殊字符：空格 `# $ & _ - " [] ' + . / :`

最多可以输入或粘贴2000个关键字。 用逗号分隔多个关键字，或在单独的行中输入它们。

>[!NOTE]
>
>* 您可以从以下位置创建负关键字 [!UICONTROL Keywords] > [!UICONTROL Negatives] 在广告组和营销活动设置中查看和。
>* 更改 [!DNL Google Ads] keyword或match type删除现有关键字并创建新关键字。


**[!UICONTROL Status]：** 关键字的显示状态： *活动* 或 *已暂停*. 新关键字的默认值为 *活动*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## 占位符

**[!UICONTROL Param1]：** 如果基本URL或跟踪模板包含 [此 `{param1}`](https://support.google.com/google-ads/answer/6305348) 动态替换字符串。

**[!UICONTROL Param2]：** 如果基本URL或跟踪模板包含 [此 `{param2}`](https://support.google.com/google-ads/answer/6305348) 动态替换字符串。

## URL选项

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[note for Base URL field]:** -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [管理关键字](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)

