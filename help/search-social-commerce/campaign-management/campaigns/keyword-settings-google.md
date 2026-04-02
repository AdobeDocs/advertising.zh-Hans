---
title: '[!DNL Google Ads]关键字设置'
description: 引用 [!DNL Google Ads] 关键字的设置。
exl-id: b2937d18-565a-43f0-ba33-d46d4c77ec07
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/XwutnbHVQrg8mfimzVjv-Px6OeUsOWzT7-347-ff2C0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 191
ht-degree: 0%

---

# [!DNL Google Ads]关键字设置

您可以为使用搜索和显示网络的营销活动创建关键字。

有关每个帐户[的关键字限制](https://support.google.com/google-ads/answer/6372658)，请参阅Google广告帮助。

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：**&#x200B;关键字（包括任何[!DNL Google Ads]关键字）与关键字和占位符的语法匹配。 [!DNL Google Ads]帐户需要具有以下属性的关键字：

* 每个关键字的最大长度为80个字符，不超过10个单词。
* 关键字只能包含字母、数字和以下特殊字符：空格`# $ & _ - " [] ' + . / :`

最多可以输入或粘贴2000个关键字。 用逗号分隔多个关键字，或在单独的行中输入它们。

>[!NOTE]
>
>* 您可以从[!UICONTROL Keywords] > [!UICONTROL Negatives]视图、广告组和促销活动设置中创建负关键字。
>* 更改[!DNL Google Ads]关键字或匹配类型会删除现有关键字并创建一个新关键字。

**[!UICONTROL Status]：**&#x200B;关键字的显示状态： *活动*&#x200B;或&#x200B;*已暂停*。 新关键字的默认值为&#x200B;*活动*。

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## 占位符

**[!UICONTROL Param1]：**&#x200B;如果基本URL或跟踪模板包含[动态替换字符串`{param1}`](https://support.google.com/google-ads/answer/6305348)，则用作替换值的字符串。

**[!UICONTROL Param2]：**&#x200B;如果基本URL或跟踪模板包含[动态替换字符串`{param2}`](https://support.google.com/google-ads/answer/6305348)，则用作替换值的字符串。

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
