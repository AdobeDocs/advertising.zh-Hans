---
title: 管理广告网络管理器帐户的凭据
description: 了解如何为提供凭据 [!DNL Google Ads] 经理帐户。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---

# 管理广告网络管理器帐户的凭据

*Beta功能*

*[!DNL Google Ads]仅限帐户*

提供您的凭据 [!DNL Google Ads] 您希望搜索、社交和商务将跨帐户转换上传到的经理帐户。 如果您想要)上传，请使用此功能 [!DNL Adobe]-tracked、跨帐户转化指标 [!DNL Google Ads] 经理帐户或b)上传包含跨帐户转换的项目组合目标 [!DNL Google Ads] 进行混合优化。

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

您可以为新经理帐户记录添加凭据，或重新验证现有经理帐户。

添加经理帐户的凭据后，帐户设置会将关联的经理帐户ID显示为只读。 此外，可选»[!UICONTROL Manager Account for Cross-Account Conversions]中的“ ”列 [!UICONTROL Campaigns] > [!UICONTROL Accounts] 视图显示每个子帐户的Manager帐户ID，并指示Manager帐户未经身份验证时的错误。 [!UICONTROL Notification Center] 包括经理帐户的凭据缺失时的通知([此 [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md))或manager帐户身份验证令牌过期时间([此 [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md))。

## 为新的经理帐户添加凭据

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. 选择 **[!UICONTROL Create new manager account]**.

1. 输入经理帐户的登录凭据。

   此 **[!UICONTROL Manager Account ID]** 和 **[!UICONTROL Login Email]** 是必需的。 搜索、Social和Commerce会自动捕获和存储用于身份验证的帐户令牌。

   您可以选择包括 **[!UICONTROL MCC Account Name]** 用于在Search、Social、Commerce和帐户中标识 **[!UICONTROL Password]**. 输入密码，以便帐户管理员根据需要刷新令牌。

1. 单击 **[!UICONTROL Authenticate]**.

1. 单击 **[!UICONTROL Save]**.

## 重新验证现有经理帐户

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. 选择 **[!UICONTROL Reauthenticate existing manager account]**.

1. 选择经理帐户。

1. 输入经理帐户的登录凭据。

   此 **[!UICONTROL Manager Account ID]** 和 **登录电子邮件** 是必需的。 搜索、Social和Commerce会自动捕获和存储用于身份验证的帐户令牌。

   您可以选择包括 **[!UICONTROL MCC Account Name]** 用于在Search、Social、Commerce和帐户中标识 **[!UICONTROL Password]**. 输入密码，以便帐户管理员根据需要刷新令牌。

1. 单击 **[!UICONTROL Authenticate]**.

1. 单击 **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [允许将目标上传到广告网络](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [将转化量度上传到 [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [编辑您的通知设置](/help/search-social-commerce/notifications/notification-edit.md)

