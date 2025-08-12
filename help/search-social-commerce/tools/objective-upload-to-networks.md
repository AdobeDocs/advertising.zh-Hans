---
title: 允许将目标上传到广告网络
description: 了解如何将混合项目组合的目标上传到 [!DNL Google Ads] 和 [!DNL Microsoft Advertising]。
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 3d3031946bb614f2c58b83170473b1394e4a017c
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# 允许将目标上传到广告网络

*仅具有[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户的广告商*

*仅启用混合优化的广告商*

Search、Social和Commerce可以将广告商帐户组合的目标上传到[!DNL Google Ads]和[!DNL Microsoft Advertising]，以便您可以将它们用于混合优化。 您上传的目标可用作帐户级别和营销活动级别自定义转化目标的转化操作。

启用此选项会自动触发上传项目组合中的目标，其中包含具有智能竞价策略的营销活动。 搜索、社交和Commerce会在广告网络上为每个适用的目标创建一个转化。 转化表示EF ID（点击ID）级别的目标中的所有加权转化量度。 对于[!DNL Google Ads]点击，EF ID是[!DNL Google Ads] `gclid`；对于[!DNL Microsoft Advertising]点击，EF ID是[!DNL Microsoft Advertising] `msclkid`。 由于此点击ID，转化数据可以映射到特定的关键字并单击时间。

每个上传的转化都具有以下名称：

`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

其中，`<network_ID>`是Search、Social和Commerce用于广告网络的数值ID，`<objective_id>`是数值目标ID，`<network_account_ID>`是广告网络帐户或经理帐户的数值ID。

上传到[!DNL Google Ads]和[!DNL Microsoft Advertising]的过程会在一天中持续进行，有时甚至会一小时一次。 对于具有大型帐户或自定义配置的广告商，每天至少进行三次上传。

>[!IMPORTANT]
>
>由Google广告和Microsoft Advertising通用事件跟踪(UET)标记跟踪的转化不会重新上传到广告网络。 如果您将它们包含在目标中，则必须将它们添加到广告网络编辑器中的促销活动目标。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**。

1. 选中&#x200B;**[!UICONTROL Enable Objective Upload]**&#x200B;旁边的复选框。

1. (在欧洲经济区(EEA)或英国(UK)开展业务且拥有[!DNL Google Ads]帐户的广告商；可选)如果您已向EEA和英国用户收集同意以将其数据上传用于广告，请选中&#x200B;**[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**&#x200B;旁边的复选框

1. 单击&#x200B;**[!UICONTROL Save]**。

1. （如果在经理帐户级别跟踪您的转化）[在](/help/search-social-commerce/admin/manager-accounts.md) > **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin]为您的经理帐户添加凭据[!UICONTROL Manager Accounts]**。

1. 验证每个名为`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`的目标是否会在两天内在广告网络上显示。

   在[!DNL Google Ads]编辑器中，查找您的[转化操作](https://support.google.com/google-ads/answer/11461796)。 在[!DNL Microsoft Advertising]编辑器中，查找您的[转化目标](https://help.ads.microsoft.com/#apex/ads/en/56709)。

   如有必要，请更新日期范围以包含上传日期。

## 如何计算加权目标

传递给广告网络的加权目标是收集的所有量度值的总和，但[!DNL Google Ads]或[!DNL Microsoft Advertising]通用事件跟踪(UET)标记跟踪的转化除外。 该值使用为广告商的Search、Social和Commerce帐户设置的归因方法计算。

例如，假设目标的目标量度是权重为25的购物车添加次数，您的辅助量度包括权重为1的GGL_Lead和Revenue以及权重为0.5的“下载”。

![加权目标示例](/help/search-social-commerce/assets/objective-example.png "加权目标示例")

假设关键字导致项目组合执行以下操作：

* 10个购物车加货
* 收入$500
* 50次下载
* 5 GGL_Lead

GGL_Lead不包含在计算/上传中，因为它是一个Google广告跟踪指标。 因此，加权目标值计算为((10 x 25) + (500 x 1) + (50 x 0.5)) = 775。

>[!TIP]
>
>您可以在广告网络的报表中查看Adobe Advertising加权收入的数据。 作为最佳实践，将加权收入与[!DNL Google Ads]“所有收入”进行比较。 (由conv. 时间)”量度或[!DNL Microsoft Advertising]量度“全部” 收入”，分段到O_ACS_OBJ*量度。<!--clarify -->

## 排除缺少的目标

如果某个项目组合的目标（名为`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`）未出现在广告网络上，请检查以下项：

* ([!DNL Google Ads])检查是否应将转化上传到帐户或经理级别。 如果应在经理级别上传它们：

   * 检查[!DNL Google Ads]经理帐户的凭据是否在&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**&#x200B;中提供。 如有必要，[添加经理帐户](/help/search-social-commerce/admin/manager-accounts.md)的凭据。

   * 检查广告网络帐户是否已包含相同的量度名称。 如果超过100次，则重命名该量度，以便创建正确的管理员级别属性。

* 检查项目组合的“混合”选项是否已选中，以及目标是否具有有效的收入。

>[!MORELIKETHIS]
>
>* [关于管理广告商的转化量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [将搜索、社交和Commerce跟踪的转化量度上传到 [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
