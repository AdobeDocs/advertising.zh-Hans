---
title: '[!DNL Yandex]关键字设置'
description: 引用 [!DNL Yandex] 关键字的设置。
exl-id: 973be0df-9b3c-4f33-b48b-ef1db4ab35da
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/-PRiQ9myH0XNYF8pc2OVBuLOK-8BpxzqruOP2hzPW0I
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 181
ht-degree: 0%

---

# [!DNL Yandex]关键字设置

Yandex关键字同时用于搜索和显示（内容）网络。

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：**&#x200B;关键字短语，包括关键字的任何[Yandex匹配类型语法](https://yandex.com/support/direct/keywords/symbols-and-operators.html)。 除停用词外，每个关键字最多可以有7个词。

最多可以输入或粘贴2000个关键字。 用逗号分隔多个关键字，或在单独的行中输入它们。

>[!NOTE]
>
>* 更改[!DNL Yandex]关键字或匹配类型会删除现有关键字并创建一个新关键字。
>* 每个Yandex广告组最多可包含200个关键字。

**[!UICONTROL Status]：**&#x200B;关键字的显示状态： *活动*&#x200B;或&#x200B;*已暂停*。 新关键字的默认值为&#x200B;*活动*。

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## 占位符

**[!UICONTROL Param1]** **[!UICONTROL Param2]：**&#x200B;当使用该关键字显示广告时，`{param1}`和`{param2}`替换变量的值将替代广告和站点链接的基本URL中{param1}和{param2}的任何实例。 最大长度为255字节。

特殊字符会自动使用UTF-8进行编码。 例如，如果相关广告的基本URL为“http://www.example.com/{param1}”，而关键字级别值{param1}为“shoes/flats.html”，则该广告将指向http://www.example.com/shoes%2Fflats.html。

>[!MORELIKETHIS]
>
>* [管理关键字](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
