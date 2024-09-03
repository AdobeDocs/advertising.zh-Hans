---
title: 为潜在客户的 [!DNL Google Ads] 增强型转化创建转化操作
description: 了解如何为潜在客户的增强型转化创建 [!DNL Google Ads] 转化操作。
feature: Conversions
source-git-commit: 5eb6ed5b42e74f424fc8499f6df0dbe3f2430ab2
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# 为潜在客户的[!DNL Google Ads]增强型转化创建转化操作

仅&#x200B;*[!DNL Google Ads]个帐户*

您可以为单个[!DNL Google Ads]帐户要跟踪的潜在客户创建[!DNL Google Ads]增强型转化转化而不是为经理帐户级别跟踪的转化创建转化操作。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**，打开&#x200B;**[!UICONTROL Summary]**&#x200B;选项卡。

1. 在数据表上方的工具栏中，单击![创建](/help/search-social-commerce/assets/add.png "创建")。

1. 指定[转换操作设置](#conversion-action-settings-google)。

   1. 选择帐户，然后选择转换类型： *[!UICONTROL Import conversion]*。

   1. 单击&#x200B;**[!UICONTROL Next]**。

   1. 指定转换操作选项。

   1. 单击&#x200B;**[!UICONTROL Generate]**。

1. 阅读有关如何为潜在客户的增强转化创建跟踪标记的信息，然后单击&#x200B;**[!UICONTROL Next]**。

   创建转化标记，并根据需要在要跟踪转化量度的网站上实施该标记。 有关说明，请参阅以下内容：

   * 要使用[!DNL Google]标记，请参阅“[为具有 [!DNL Google] 标记](https://support.google.com/google-ads/answer/11347292)的潜在客户设置增强转化”中“配置[!DNL Google]标记设置”的[!DNL Google Ads]说明。

   * 要使用[!DNL Google Tag Manager]，请参阅“[为具有 [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11021502?#configure)的潜在客户设置增强转化”中的[!DNL Google Ads]说明，以便“配置[!DNL Google]标记设置”和“验证您的设置并发布容器”。

1. 单击&#x200B;**[!UICONTROL Done].**

在创建转化操作并实施转化跟踪标记后，您可以上传组织捕获的离线转化数据，并将其归因于转化操作。 请参阅“[上传离线转化数据以获得增强型转化](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)”。

## 转换操作设置 {#conversion-action-settings-google}

**[!UICONTROL Select an Account]：**&#x200B;适用的Google Ads帐户。

**[!UICONTROL Type of Conversion]：**&#x200B;要跟踪的转换类型：选择&#x200B;*[!UICONTROL Import conversion]*。 所有其他类型均可用于为其他类型的转化创建转化跟踪标记（而非转化操作）。

**[!UICONTROL Conversion Name]：**&#x200B;转换操作的唯一名称。

**\[转化类别\]：**&#x200B;转化类别，如&#x200B;*合格的潜在客户*&#x200B;或&#x200B;*注册*。

**\[操作类型\]：**&#x200B;目标是&#x200B;*[!UICONTROL Primary action used for bidding optimization]*&#x200B;还是&#x200B;*[!UICONTROL Secondary action not used for bidding optimization]*。

**[!UICONTROL Value]：**&#x200B;如何度量每次转换的[值](https://support.google.com/google-ads/answer/13064207)：

* *[!UICONTROL Use the same value for each conversion]，*，它要求您选择一种货币并输入每次转换的值。

* *[!UICONTROL Use a different value for each conversion]，*，它要求您选择货币并为每次转换输入默认值。 在特定网页上实施标记时，可以使用特定于事务的值更改标记中的默认值。

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]：** [每次点击或交互要计数的转化数](https://support.google.com/google-ads/answer/3438531)： *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]*&#x200B;或&#x200B;*[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*。

**[!UICONTROL Click Through Conversion Window]：**&#x200B;记录转化的广告交互后的最大天数。 对于搜索、展示和购物营销活动，此窗口可以为1到90天。 选择一个数字或选择&#x200B;**[!UICONTROL Custom]**&#x200B;并输入一个数字。

**[!UICONTROL View Through Conversion Window]：**&#x200B;用户查看您的广告后记录浏览转化的最大天数。 对于搜索、展示和购物营销活动，此窗口可以为1到90天。 选择一个数字或选择&#x200B;**[!UICONTROL Custom]**&#x200B;并输入一个数字。

**[!UICONTROL Attribution Model]：** [每个广告交互获得的点数是](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138)： *[!UICONTROL Data driven]*&#x200B;或&#x200B;*[!UICONTROL Last click]*。

>[!MORELIKETHIS]
>
>* [上载离线转化数据以进行增强型转化](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [为潜在客户实施 [!DNL Google Ads] 增强的转化](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
