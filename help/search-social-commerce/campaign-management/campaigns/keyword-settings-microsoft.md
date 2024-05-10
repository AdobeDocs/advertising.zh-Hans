---
title: ’[!DNL Microsoft Advertising] 关键字设置
description: 引用设置 [!DNL Microsoft Advertising] 关键字。
exl-id: 82eee01f-db4b-4d1a-ae24-1ef65f8c6953
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] 关键词设置

您可以为使用搜索和显示网络的营销活动创建关键字。

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：** 关键字，包括任何 [!DNL Microsoft Advertising] 匹配语法和占位符。 每个关键字的最大长度为100个字符。

最多可以输入或粘贴2000个关键字。 用逗号分隔多个关键字，或在单独的行中输入它们。

>[!NOTE]
>
>* 您可以从以下位置创建负关键字 [!UICONTROL Keywords] > [!UICONTROL Negatives] 在广告组和营销活动设置中查看和。
>* 更改 [!DNL Microsoft Advertising] 关键字删除现有关键字，并使用新关键字ID创建新关键字。 但是，更改匹配类型不会删除现有关键字。

**[!UICONTROL Status]：** 关键字的显示状态： *活动* 或 *已暂停*. 新关键字的默认值为 *活动*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## 占位符

**[!UICONTROL Param2]：** 如果关键字的基本URL或广告的标题、描述或基本URL包含，则用作替换值的字符串 [该 `{Param2}` 动态替换字符串](https://help.bingads.microsoft.com/#apex/3/en/53079/0). 最大长度为70个字符，但请注意，在其中使用它的广告元素的最大长度（例如，标题1和标题2组合可能最多为76个字符）。

**[!UICONTROL Param3]：** 如果关键字的基本URL或广告的标题、描述或基本URL包含，则用作替换值的字符串 [该 `{Param3}` 动态替换字符串](https://help.bingads.microsoft.com/#apex/3/en/53079/0). 最大长度为70个字符，但请注意，在其中使用它的广告元素的最大长度（例如，标题1和标题2组合可能最多为76个字符）。

## URL选项

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

此字段可以选择包括 `{Param2}` 和 `{Param3}` 动态替换变量。

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [管理关键字](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
