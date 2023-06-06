---
title: 允许将目标上传到广告网络
description: 了解如何将混合项目组合的目标上传到 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising].
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# 允许将目标上传到广告网络

*广告商使用 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 仅限帐户*

*仅为混合优化启用的广告商*

如果您的广告商帐户配置为使用混合优化，则Adobe广告可以选择将帐户项目组合的目标上传到 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 作为转化，以便将其用于混合优化。

启用此选项会自动触发上传包含具有智能竞价策略营销活动的项目组合。 搜索、社交和商务会在广告网络上为每个适用的组合和目标组合创建一个转化。 每个转换都有名称 `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`，其中 `<portfolio_id>` 是数值项目组合ID和 `<se_acctid/conversion_manager_se_acctid>` 是广告网络帐户或经理帐户的数值ID。 转换表示目标中的所有加权交易属性。

上传至 [!DNL Google Ads] 每天06:00（广告商所在时区）。 上传至 [!DNL Microsoft® Advertising] 每天09:00（广告商所在时区）。

<!-- Note to self: Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren't re-uploaded to the ad networks. -->

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. 选中旁边的复选框 **[!UICONTROL Enable Objective Upload]**.

   仅当将广告商帐户配置为使用混合优化时，此选项才可用。 要启用混合优化，请联系您的Adobe客户团队。

1. 单击 **[!UICONTROL Save]**.

1. （如果在经理帐户级别跟踪您的转化） [为您的经理帐户添加凭据](/help/search-social-commerce/admin/manager-accounts.md) 在 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [关于管理广告商的交易属性](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md)
>* [将转化量度上传到 [!DNL Google Ads]](conversion-metrics-upload-to-google.md)

