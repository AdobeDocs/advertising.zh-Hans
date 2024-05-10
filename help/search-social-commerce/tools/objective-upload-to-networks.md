---
title: 允许将目标上传到广告网络
description: 了解如何将混合项目组合的目标上传到 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# 允许将目标上传到广告网络

*广告商使用 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 仅限帐户*

*仅为混合优化启用的广告商*

Search、Social和Commerce可以将广告商帐户组合的目标上传到 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 以便将其用于混合优化。 您上传的目标可用作帐户级别和营销活动级别自定义转化目标的转化操作。

启用此选项会自动触发上传项目组合中的目标，其中包含具有智能竞价策略的营销活动。 搜索、社交和Commerce会在广告网络上为每个适用的目标创建一个转化。 转化表示目标中的所有加权转化量度。 每个转换都有以下名称之一：

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  位置 `<network_ID>` 是Search、Social和Commerce用于广告网络的数值ID， `<objective_id>` 是数值目标ID，并且 `<network_account_ID>` 是广告网络帐户或经理帐户的数值ID。

* （将来将弃用的旧格式） `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  位置 `<portfolio_id>` 是数值项目组合ID和 `<se_acctid/conversion_manager_se_acctid>` 是广告网络帐户或经理帐户的数值ID。

  在弃用旧格式之前，您的Adobe客户团队将与您合作，迁移广告网络中的现有转化操作名称。 在迁移期间，新旧格式的上传将并行运行。 建模和优化不会受到影响，因为新的转化操作最初以“次要”（未优化）状态出现，并带有90天的回填数据。

上传至 [!DNL Google Ads] 在广告商所在时区的每天06:00发生。 上传至 [!DNL Microsoft® Advertising] 在广告商所在时区的每天09:00发生。

>[!IMPORTANT]
>
>由Google Ads和Microsoft Advertising通用事件跟踪(UET)标记跟踪的转化不会重新上传到广告网络。 如果您将它们包含在目标中，请将其添加到广告网络编辑器中的促销活动目标。

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. 选中旁边的复选框 **[!UICONTROL Enable Objective Upload]**.

1. (广告商使用 [!DNL Google Ads] 在欧洲经济区(EEA)或英国(UK)开展业务的帐户；可选)如果您已向EEA和英国用户收集同意以上传其数据用于广告，请选中 **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. 单击 **[!UICONTROL Save]**.

1. （如果在经理帐户级别跟踪您的转化） [为您的经理帐户添加凭据](/help/search-social-commerce/admin/manager-accounts.md) 在 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

每日上传完成后，您可以验证转化操作是否显示在广告网络中。

>[!MORELIKETHIS]
>
>* [关于管理广告商的转化量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [将转化量度上传到 [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
