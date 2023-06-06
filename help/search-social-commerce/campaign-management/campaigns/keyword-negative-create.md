---
title: 创建负关键字
description: 了解如何为搜索营销活动和广告组创建负面关键词。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# 创建负关键字

*[!DNL Baidu]， [!DNL Google Ads] 和 [!DNL Microsoft® Advertising]、和 [!DNL Yahoo! Japan Ads] 仅限帐户*

您可以为定位搜索或显示/本机网络的搜索广告组或营销活动创建负关键字。 负关键字不会触发广告。

>[!NOTE]
>您还可以在中创建和编辑负关键字 [广告组设置](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) 和 [campaign设置](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

>[!TIP]
>要一次创建多个负关键字，请使用 [营销活动批量处理工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Negatives]**.

1. 在数据表上方的工具栏中，单击 ![创建](/help/search-social-commerce/assets/add.png "创建")，然后单击 **[!UICONTROL Campaign]** 要创建营销活动级别的负关键字或 **[!UICONTROL Ad Group]** 创建广告组级别的负关键字。

1. 选择广告网络、帐户、营销活动，以及（如果相关）广告组，然后单击 **[!UICONTROL Continue]**.

1. 输入负关键字。 使用以下语法，不带减号(`-`)：

   * 负值广泛匹配： `keyword` (不支持 [!DNL Microsoft® Advertising])

   * 负片语匹配： `"keyword"`

   * 负精确匹配： `[keyword]`

   用逗号分隔多个值，或在单独行中输入它们。 在一个操作中，最多可以输入或粘贴2000个负关键字。 另请参阅以下要求和限制：

   * 最大字符长度： [!DNL Baidu]：30个单字节或15个双字节； [!DNL Microsoft® Advertising]：100个单字节或50个双字节； [!DNL Google Ads] 和 [!DNL Yahoo! Japan Ads]：80字节或40字节双字节。

   * [!DNL Baidu] 每个广告组的每个关键字仅允许一个匹配类型。 例如，广告组1不能同时包含两者 `"keyword"` 和 `[keyword]`.

   * [!DNL Google Ads]：每个关键字最多可包含10个单词，并且只能包含字母、数字和以下特殊字符：空格 `# $ & _ - " [ ] ' + . / :`

   * [!DNL Yandex]：每个关键字最多可以有7个单词，不包括停用词。 每个 [!DNL Yandex ad group] 最多可包含200个关键字。


1. 单击 **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [关于关键字](keyword-about.md)
>* [管理可竞价关键词](keyword-manage.md)
>* [更改关键字和负关键字的状态](keyword-status-edit.md)

