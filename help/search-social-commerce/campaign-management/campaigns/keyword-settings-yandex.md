---
title: ”[!DNL Yandex] 关键词设置”
description: 引用设置 [!DNL Yandex] 关键字。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# [!DNL Yandex] 关键词设置

Yandex关键字用于搜索和显示（内容）网络。

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：** 关键词短语，包括任何 [Yandex匹配类型语法](https://yandex.com/support/direct/keywords/symbols-and-operators.html) （关键字）。 每个关键字最多可以有7个单词，不包括停用词。

最多可以输入或粘贴2000个关键字。 用逗号分隔多个关键字，或在单独的行中输入它们。

>[!NOTE]
>
>* 更改 [!DNL Yandex] keyword或match type删除现有关键字并创建新关键字。
>* 每个Yandex广告组最多可包含200个关键词。


**[!UICONTROL Status]：** 关键字的显示状态： *活动* 或 *已暂停*. 新关键字的默认值为 *活动*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## 占位符

**[!UICONTROL Param1]** **[!UICONTROL Param2]：** 的值 `{param1}` 和 `{param2}` 替换变量，当使用关键字显示广告时，这些变量将替换广告和站点链接的基本URL中{param1}和{param2}的任何实例。 最大长度为255字节。

特殊字符会自动使用UTF-8进行编码。 例如，如果相关广告的基本URL为“http://www.example.com/{param1}”，且{param1}的关键字级别值为“shoes/flats.html”，则该广告会引向http://www.example.com/shoes%2Fflats.html。

>[!MORELIKETHIS]
>
>* [管理关键字](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)

