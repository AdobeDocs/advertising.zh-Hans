---
title: 允许将目标上传到广告网络
description: 了解如何将混合项目组合的目标上传到 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 7b857f2f75f05685d0776c710a442088a72f590c
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# 允许将目标上传到广告网络

*广告商使用 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 仅限帐户*

*仅为混合优化启用的广告商*

如果您的广告商帐户配置为使用混合优化，则Adobe Advertising可以选择性地将帐户组合的目标上传到 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 作为转化，以便将其用于混合优化。

启用此选项会自动触发对包含具有智能竞价策略营销活动的项目组合的上传。 搜索、社交和Commerce会在广告网络上为每个适用的组合和目标组合创建转化。 每个转换都有名称 `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`，其中 `<portfolio_id>` 是数值项目组合ID和 `<se_acctid/conversion_manager_se_acctid>` 是广告网络帐户或经理帐户的数值ID。 转化表示目标中的所有加权转化量度。

上传至 [!DNL Google Ads] 在广告商所在时区的每天06:00发生。 上传至 [!DNL Microsoft® Advertising] 在广告商所在时区的每天09:00发生。

<!-- Note to self: Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren't re-uploaded to the ad networks. -->

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. 选中旁边的复选框 **[!UICONTROL Enable Objective Upload]**.

1. (广告商使用 [!DNL Google Ads] 在欧洲经济区(EEA)或英国(UK)开展业务的帐户；可选)如果您已向EEA和英国用户收集同意以上传其数据用于广告，请选中 **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. 单击 **[!UICONTROL Save]**.

1. （如果在经理帐户级别跟踪您的转化） [为您的经理帐户添加凭据](/help/search-social-commerce/admin/manager-accounts.md) 在 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [关于管理广告商的转化量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [将转化量度上传到 [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
