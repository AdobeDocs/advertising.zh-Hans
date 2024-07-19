---
title: 管理广告网络管理器帐户的凭据
description: 了解如何为 [!DNL Google Ads] 经理帐户提供凭据。
exl-id: 95866a2e-4695-4b1d-ac23-844d3b9a0a74
feature: Search Admin
source-git-commit: 4cf04fc7ea22e50b5f56cd278ad9a1aac724edf7
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%

---

# 管理广告网络管理器帐户的凭据

仅&#x200B;*[!DNL Google Ads]个帐户*

提供您的[!DNL Google Ads]经理帐户的凭据，您希望搜索、社交和Commerce将跨帐户转化上传到该帐户。 如果您想要a)将[!DNL Adobe]跟踪的跨帐户转化量度上传到[!DNL Google Ads]经理帐户，或者b)将包含跨帐户转化的项目组合目标上传到[!DNL Google Ads]以进行混合优化，请使用此功能。

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

您可以为新经理帐户记录添加凭据，或重新验证现有经理帐户。

为管理员帐户添加凭据后，帐户设置会将关联的管理员帐户ID显示为只读。 此外，[!UICONTROL Campaigns] > [!UICONTROL Accounts]视图中的可选“[!UICONTROL Manager Account for Cross-Account Conversions]”列会显示每个子帐户的经理帐户ID，并在经理帐户未通过身份验证时指示错误。 [!UICONTROL Notification Center]包含缺少经理帐户的凭据（[该[!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)）或经理帐户身份验证令牌过期时的通知（[该[!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)）。

## 为新的经理帐户添加凭据

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**。

1. 选择&#x200B;**[!UICONTROL Create new manager account]**。

1. 输入经理帐户的登录凭据。

   **[!UICONTROL Manager Account ID]**&#x200B;和&#x200B;**[!UICONTROL Login Email]**&#x200B;是必需的。 搜索、Social和Commerce会自动捕获和存储用于身份验证的帐户令牌。

   您可以选择在Search、Social和Commerce以及帐户&#x200B;**[!UICONTROL Password]**&#x200B;中包含用于标识的&#x200B;**[!UICONTROL MCC Account Name]**。 输入密码，以便帐户管理员根据需要刷新令牌。

1. 单击&#x200B;**[!UICONTROL Authenticate]**。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 重新验证现有经理帐户

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**。

1. 选择&#x200B;**[!UICONTROL Reauthenticate existing manager account]**。

1. 选择经理帐户。

1. 输入经理帐户的登录凭据。

   需要&#x200B;**[!UICONTROL Manager Account ID]**&#x200B;和&#x200B;**登录电子邮件**。 搜索、Social和Commerce会自动捕获和存储用于身份验证的帐户令牌。

   您可以选择在Search、Social和Commerce以及帐户&#x200B;**[!UICONTROL Password]**&#x200B;中包含用于标识的&#x200B;**[!UICONTROL MCC Account Name]**。 输入密码，以便帐户管理员根据需要刷新令牌。

1. 单击&#x200B;**[!UICONTROL Authenticate]**。

1. 单击&#x200B;**[!UICONTROL Save]**。

>[!MORELIKETHIS]
>
>* [启用将目标上传到广告网络](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [将转化量度上载到 [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [编辑您的通知设置](/help/search-social-commerce/notifications/notification-edit.md)
