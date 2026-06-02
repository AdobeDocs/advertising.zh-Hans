---
title: （新UI）为潜在客户的 [!DNL Google Ads] 增强型转化创建转化操作
description: 了解如何为潜在客户的增强型转化创建 [!DNL Google Ads] 转化操作。
feature: Conversions
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
subfeature_v2:
  - id: d068b149-b9d1-421c-9033-a51495366ddc
source-git-commit: 0bfee2b52410b5cab8e9b3dfba35effc36fc40e1
workflow-type: tm+mt
source-wordcount: 510
ht-degree: 0%

---

# （新UI）为潜在客户的[!DNL Google Ads]增强型转化创建转化操作

*Beta功能*

仅&#x200B;*[!DNL Google Ads]个帐户*

您可以为单个[!DNL Google Ads]帐户要跟踪的潜在客户创建[!DNL Google Ads]增强型转化转化而不是为经理帐户级别跟踪的转化创建转化操作。

创建转化操作并实施转化跟踪标记后，您可以[上载组织捕获的离线转化数据](conversions-upload-offline-enhanced-conversions.md)并将其归因于转化操作。

不支持[!DNL Microsoft Advertising]帐户。

## 创建转化操作

1. 在主菜单中，单击&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversions]**。

1. 在数据表上方，单击&#x200B;**[!UICONTROL Set up Conversion]**。

1. 指定[转换操作设置](#conversion-action-settings-google)。

   1. 选择[!UICONTROL Setup Method] *[!UICONTROL Create Conversion]*。

   1. 选择帐户，然后选择转换类型： *[!UICONTROL Import conversion]*。

   1. 单击&#x200B;**[!UICONTROL Next]**。

   1. 指定转换操作选项。

   1. 单击&#x200B;**[!UICONTROL Review and Save]**&#x200B;以查看设置。

   1. 单击&#x200B;**[!UICONTROL Generate]**。

1. 阅读有关如何为潜在客户的增强转化创建跟踪标记的信息，然后单击&#x200B;**[!UICONTROL Next]**。

   您必须创建转化标记，并根据需要在要跟踪转化量度的网站上实施该标记。 您还需要为潜在客户启用增强的转化并同意客户数据条款和条件。 有关说明，请参阅[!DNL Google Ads]有关“[为潜在客户](https://support.google.com/google-ads/answer/11021502)配置增强型转化 [!DNL Google] 标记”的说明。

   如果要跟踪特定于事务的转化值，请[自定义您的事件片段](https://support.google.com/google-ads/answer/6095947)。

1. 单击&#x200B;**[!UICONTROL Close].**

## 转换操作设置 {#conversion-action-settings-google}

### 设置路径部分

**[!UICONTROL Setup Method]：**&#x200B;操作的类型： *[!UICONTROL Create Conversion]*

**[!UICONTROL Platform]：**&#x200B;广告网络： *[!UICONTROL Google]*。

### “转化详细信息”部分

**[!UICONTROL Select Account]：**&#x200B;适用的[!DNL Google Ads]帐户。

**[!UICONTROL Type of conversions]：**&#x200B;要跟踪的转换类型：选择&#x200B;*[!UICONTROL Import conversion]*。 所有其他类型均可用于为其他类型的转化创建转化跟踪标记（而非转化操作）。

### “转换设置”部分

**[!UICONTROL Conversion Name]：**&#x200B;转换操作的唯一名称。

**[!UICONTROL Goal Category]：**&#x200B;转化类别，如&#x200B;*合格潜在客户*&#x200B;或&#x200B;*注册*。

**[!UICONTROL Preferred Action optimization]：**&#x200B;目标是&#x200B;*[!UICONTROL Primary action used for bidding optimization]*&#x200B;还是&#x200B;*[!UICONTROL Secondary action not used for bidding optimization]*。

**[!UICONTROL Conversion Value]：**&#x200B;如何度量每次转换的[值](https://support.google.com/google-ads/answer/13064207)：

* *[!UICONTROL Use the same value for each conversion]，*，它要求您选择一种货币并输入每次转换的值。

* *[!UICONTROL Use different values for each conversion]，*，它要求您选择货币并为每次转换输入默认值。 在特定网页上实施标记时，可以使用特定于事务的值更改标记中的默认值。

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]：** [每次点击或交互要计数的转化数](https://support.google.com/google-ads/answer/3438531)： *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]*&#x200B;或&#x200B;*[!UICONTROL One (Recommended for leads, sign-ups and other conversions for which only the first interaction is valuable)]*。

**[!UICONTROL Click-Through Conversion Window]：**&#x200B;记录转化的广告交互后的最大天数。 对于搜索、展示和购物营销活动，此窗口可以为1到90天。 选择一个数字或选择&#x200B;**[!UICONTROL Custom]**&#x200B;并输入一个数字。

**[!UICONTROL View-Through Conversion Window]：**&#x200B;用户查看您的广告后记录浏览转化的最大天数。 对于搜索、展示和购物营销活动，此窗口可以为1到90天。 选择一个数字或选择&#x200B;**[!UICONTROL Custom]**&#x200B;并输入一个数字。

**[!UICONTROL Attribution Model]：** [确定每个广告交互获得多少点数的归因模型](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138)： *[!UICONTROL Data driven]*&#x200B;或&#x200B;*[!UICONTROL Last click]*。

>[!MORELIKETHIS]
>
>* [（新UI）上载增强型转换的离线转换数据](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [上载离线转化数据以进行增强型转化](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [为潜在客户实施 [!DNL Google Ads] 增强的转化](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
