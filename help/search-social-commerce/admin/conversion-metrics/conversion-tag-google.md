---
title: 为创建转化标记 [!DNL Google Ads]
description: 了解如何创建 [!DNL Google Ads] 转化标记。
feature: Conversions
source-git-commit: af32aea1c50edb6b22b0b15c920cb8c2dcdc37e9
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# 为创建转化标记 [!DNL Google Ads]

您可以为要为个人跟踪的新转化创建转化标记 [!DNL Google Ads] 帐户，不在经理帐户级别进行跟踪。

要为现有转化生成转化标记，请使用广告网络的编辑器。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

1. 在数据表上方的工具栏中，单击 ![创建](/help/search-social-commerce/assets/add.png "创建").

1. 指定 [转化标记设置](#conversion-tag-settings-google).

   1. 选择帐户，然后选择转换类型。

   1. 单击 **[!UICONTROL Next]**.

   1. 指定转换选项。

   1. 单击 **[!UICONTROL Generate]**.

1. 复制转化标记，并在要跟踪转化量度的网站上实施该标记。

   请参阅“安装 [!DNL Google] 标记” [!DNL Google Ads] “帮助”[2. 设置您的Google标记](https://support.google.com/google-ads/answer/12215519)“

1. 单击 **[!UICONTROL Done].**

将标记添加到您的网站并开始触发后， [!DNL Google Ads] 会记录网站上的转化。 搜索、社交和商务会每天同步转化。 有关已同步数据的更多信息，请参阅&quot;[[!DNL Google Ads] 搜索、社交和商务中的转化数据](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

## 转换标记设置 {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]：** 适用的Google Ads帐户。

**[!UICONTROL Type of Conversion]：** 要跟踪的转换类型： *[!UICONTROL Click on a webpage element]*， *[!UICONTROL Calls to a phone number on your website]*，或 *[!UICONTROL Clicks to your number on your mobile website]*.

**[!UICONTROL Conversion Name]：** 转化量度的唯一名称。

**\[目标类别\]：** 转化目标。 可用的目标因转化类型而异。 对象 *[!UICONTROL Calls to a phone number on your website]* 和 *[!UICONTROL Clicks to your number on your mobile website]*， &quot;[!UICONTROL Phone Call Lead]默认情况下会选中“”。

**\[操作类型\]：** 目标是否为 *[!UICONTROL Primary action used for bidding optimization]* 或 *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]：** 如何测量 [每次转换的值](https://support.google.com/google-ads/answer/3419241)：

* *[!UICONTROL Use the same value for each conversion]，* 这要求您选择一种货币并输入每次折换的值。

* *[!UICONTROL Use a different value for each conversion]，* 这要求您选择一种货币并为每种兑换输入默认值。 在特定网页上实施标记时，可以使用特定于事务的值更改标记中的默认值。

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]：** [每次点击或交互要计数的转化数](https://support.google.com/google-ads/answer/3438531)： *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* 或 *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]：** 广告交互后记录转化的最大天数。 对于搜索、展示和购物营销活动，此窗口可以为1到90天。 选择一个数字或选择 **[!UICONTROL Custom]** 并输入一个数字。

**[!UICONTROL View Through Conversion Window]：** 用户查看您的广告后记录显示到达转化的最大天数。 对于搜索、展示和购物营销活动，此窗口可以为1到90天。 选择一个数字或选择 **[!UICONTROL Custom]** 并输入一个数字。

**[!UICONTROL Attribution Model]：** [每个广告互动获得的点数](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138)： *[!UICONTROL Data driven]*， *[!UICONTROL Last click]*， *[!UICONTROL First click]*， *[!UICONTROL Linear]*， *[!UICONTROL Time decay]*，或 *[!UICONTROL Position based]*.

>[!MORELIKETHIS]
>
>* [[!DNL Google Ads] 搜索、社交和商务中的转化数据](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
