---
title: 为 [!DNL Google Ads]创建转化标记
description: 了解如何创建 [!DNL Google Ads] 转化标记。
feature: Conversions
exl-id: 214611f0-bd38-499e-a7de-3a5878995fb5
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# 为[!DNL Google Ads]创建转化标记

您可以为要跟踪单个[!DNL Google Ads]帐户，而不是在经理帐户级别跟踪的新转化创建转化标记。

要为现有转化生成转化标记，请使用广告网络的编辑器。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**。

1. 在数据表上方的工具栏中，单击![创建](/help/search-social-commerce/assets/add.png "创建")。

1. 指定[转换标记设置](#conversion-tag-settings-google)。

   1. 选择帐户，然后选择转换类型。

   1. 单击&#x200B;**[!UICONTROL Next]**。

   1. 指定转换选项。

   1. 单击&#x200B;**[!UICONTROL Generate]**。

1. 复制转化标记，并在要跟踪转化量度的网站上实施该标记。

   请参阅“[”的[!DNL Google Ads]帮助中的“安装[!DNL Google]标记”。 设置您的Google标记](https://support.google.com/google-ads/answer/12215519)。”

1. 单击&#x200B;**[!UICONTROL Done].**

将标记添加到您的网站并开始触发后，[!DNL Google Ads]会在网站上记录转化。 搜索、社交和Commerce每天都会同步转化。 有关同步数据的更多信息，请参阅Search、Social和Commerce中的[[!DNL Google Ads] 转化数据](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)。

## 转换标记设置 {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]：**&#x200B;适用的Google Ads帐户。

**[!UICONTROL Type of Conversion]：**&#x200B;要跟踪的转换类型： *[!UICONTROL Click on a webpage element]*、*[!UICONTROL Calls to a phone number on your website]*&#x200B;或&#x200B;*[!UICONTROL Clicks to your number on your mobile website]*。

**[!UICONTROL Conversion Name]：**&#x200B;转化量度的唯一名称。

**\[转化类别\]：**&#x200B;转化类别。 可用的类别因转化类型而异。 对于&#x200B;*[!UICONTROL Calls to a phone number on your website]*&#x200B;和&#x200B;*[!UICONTROL Clicks to your number on your mobile website]*，默认情况下选中“[!UICONTROL Phone Call Lead]”。

**\[操作类型\]：**&#x200B;目标是&#x200B;*[!UICONTROL Primary action used for bidding optimization]*&#x200B;还是&#x200B;*[!UICONTROL Secondary action not used for bidding optimization]*。

**[!UICONTROL Value]：**&#x200B;如何度量每次转换的[值](https://support.google.com/google-ads/answer/3419241)：

* *[!UICONTROL Use the same value for each conversion]，*，它要求您选择一种货币并输入每次转换的值。

* *[!UICONTROL Use a different value for each conversion]，*，它要求您选择货币并为每次转换输入默认值。 在特定网页上实施标记时，可以使用特定于事务的值更改标记中的默认值。

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]：** [每次点击或交互要计数的转化数](https://support.google.com/google-ads/answer/3438531)： *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]*&#x200B;或&#x200B;*[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*。

**[!UICONTROL Click Through Conversion Window]：**&#x200B;记录转化的广告交互后的最大天数。 对于搜索、展示和购物营销活动，此窗口可以为1到90天。 选择一个数字或选择&#x200B;**[!UICONTROL Custom]**&#x200B;并输入一个数字。

**[!UICONTROL View Through Conversion Window]：**&#x200B;用户查看您的广告后记录浏览转化的最大天数。 对于搜索、展示和购物营销活动，此窗口可以为1到90天。 选择一个数字或选择&#x200B;**[!UICONTROL Custom]**&#x200B;并输入一个数字。

**[!UICONTROL Attribution Model]：** [每个广告交互获得的点数是](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138)： *[!UICONTROL Data driven]*、*[!UICONTROL Last click]*、*[!UICONTROL First click]*、*[!UICONTROL Linear]*、*[!UICONTROL Time decay]*&#x200B;或&#x200B;*[!UICONTROL Position based]*。

>[!MORELIKETHIS]
>
>* 搜索、社交和Commerce中的[[!DNL Google Ads] 转化数据](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
