---
title: '[!DNL Microsoft Advertising]关键字设置'
description: 引用[!DNL Microsoft Advertising]关键字的设置。
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
source-wordcount: '281'
ht-degree: 0%
---
# [!DNL Microsoft Advertising]关键字设置

您可以为使用搜索和显示网络的营销活动创建关键字。

## [!UICONTROL Basic Settings]

*仅新关键字*

**[!UICONTROL Network]：**&#x200B;广告网络。

**[!UICONTROL Account]：**&#x200B;广告网络帐户。

**[!UICONTROL Campaign]：**&#x200B;营销活动。

**[!UICONTROL Ad Group]：**&#x200B;广告组。

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]：**&#x200B;关键字，包括任何[!DNL Microsoft Advertising]匹配语法和占位符。 每个关键字的最大长度为100个字符。

最多可以输入或粘贴2000个关键字。 用逗号分隔多个关键字，或在单独的行中输入它们。

>[!NOTE]
>
>* 您可以从[!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives]选项卡，在广告组和营销活动设置中创建负关键字。
>* 更改[!DNL Microsoft Advertising]关键字会删除现有关键字，并使用新的关键字ID创建新关键字。 但是，更改匹配类型不会删除现有关键字。

**[!UICONTROL Status]：**&#x200B;关键字的显示状态： *[!UICONTROL Active]*&#x200B;或&#x200B;*[!UICONTROL Paused]*。 新关键字的默认值为&#x200B;*[!UICONTROL Active]*。

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

**[!UICONTROL Param1]：**&#x200B;要用作替换值的字符串（如果关键字的基本URL或广告的标题、描述或基本URL包含[动态替换字符串`{Param1}`）。 &#x200B;](https://help.bingads.microsoft.com/#apex/3/en/53079/0)最大长度为70个字符，但请注意，在其中使用它的广告元素的最大长度（例如，标题1和标题2组合可能最多为76个字符）。

**[!UICONTROL Param2]：**&#x200B;要用作替换值的字符串（如果关键字的基本URL或广告的标题、描述或基本URL包含[动态替换字符串`{Param2}`）。 &#x200B;](https://help.bingads.microsoft.com/#apex/3/en/53079/0)最大长度为70个字符，但请注意，在其中使用它的广告元素的最大长度（例如，标题1和标题2组合可能最多为76个字符）。

## [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

此字段可以选择包括`{Param1}`和`{Param2}`动态替换变量。

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [管理关键字](keyword-manage.md)
