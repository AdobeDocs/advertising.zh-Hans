---
title: '[!DNL Yandex]关键字设置'
description: 引用[!DNL Yandex]关键字的设置。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%
---
# [!DNL Yandex]关键字设置

[!DNL Yandex]关键字同时用于搜索和显示（内容）网络。

## [!UICONTROL Basic Settings]

*仅新关键字*

**[!UICONTROL Network]：**&#x200B;广告网络。

**[!UICONTROL Account]：**&#x200B;广告网络帐户。

**[!UICONTROL Campaign]：**&#x200B;营销活动。

**[!UICONTROL Ad Group]：**&#x200B;广告组。

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：**&#x200B;关键字短语，包括关键字的任何[[!DNL Yandex] 匹配类型语法](https://yandex.com/support/direct/keywords/symbols-and-operators.html)。 除停用词外，每个关键字最多可以有7个词。

最多可以输入或粘贴2000个关键字。 用逗号分隔多个关键字，或在单独的行中输入它们。

>[!NOTE]
>
>* 更改[!DNL Yandex]关键字或匹配类型会删除现有关键字并创建一个新关键字。
>* 每个[!DNL Yandex]广告组最多可包含200个关键字。

**[!UICONTROL Status]：**&#x200B;关键字的显示状态： *[!UICONTROL Active]*&#x200B;或&#x200B;*[!UICONTROL Paused]*。 新关键字的默认值为&#x200B;*[!UICONTROL Active]*。

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

>[!NOTE]
>
>特殊字符会自动使用UTF-8进行编码。 例如，如果相关广告的基本URL为`http://www.example.com/{param1}`，而关键字级别值`{param1}`为`shoes/flats.html`，则广告将指向`http://www.example.com/shoes%2Fflats.html`。

**[!UICONTROL Param1]：**&#x200B;当使用关键字显示广告时，如果基本URL包含广告和站点链接的`{param1}`动态替换字符串，则用作替换值的字符串。 最大长度为255字节。

**[!UICONTROL Param2]：**&#x200B;当使用关键字显示广告时，如果基本URL包含广告和站点链接的`{param2}`动态替换字符串，则用作替换值的字符串。 最大长度为255字节。

>[!MORELIKETHIS]
>
>* [管理关键字](keyword-manage.md)
