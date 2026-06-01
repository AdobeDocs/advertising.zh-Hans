---
title: （新UI）管理Google广告管理器帐户的凭据
description: 了解如何在新的UI中为Google Ads管理器帐户设置和管理凭据。
feature: Search Admin
source-git-commit: bf1ca7f6133c19bb68dbe0395416dca8ef647464
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# （新UI）管理[!DNL Google Ads]经理帐户的凭据

*Beta功能*

仅&#x200B;*[!DNL Google Ads]个帐户*

为希望Search、Social和Commerce将跨帐户转化上传到的[!DNL Google Ads]经理帐户提供凭据。 如果您想要a)将[!DNL Adobe]跟踪的跨帐户转化量度上传到[!DNL Google Ads]经理帐户，或者b)将包含跨帐户转化的项目组合目标上传到[!DNL Google Ads]以进行混合优化，请使用此功能。

您可以为新经理帐户记录添加凭据，或重新验证现有经理帐户。

为管理员帐户添加凭据后，帐户设置会将关联的管理员帐户ID显示为只读。 [!UICONTROL Notification Center]包括经理帐户的凭据缺失([!UICONTROL Manager Account Missing Error])或经理帐户身份验证令牌过期([!UICONTROL Manager Account Auth Error])时的[通知](/help/search-social-commerce/new-ui/notifications-manage.md)。

## 为新经理帐户添加凭据 {#create-manager-account}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**。

1. 单击&#x200B;**[!UICONTROL +]**。

1. 选择广告网络，然后单击&#x200B;**[!UICONTROL Next]**。

1. 指定[管理员帐户设置](#manager-account-settings)。

1. 单击&#x200B;**[!UICONTROL Authenticate]**&#x200B;并使用经理帐户凭据登录。

   搜索、Social和Commerce会自动捕获和存储身份验证令牌。

1. 在“搜索”、“社交”和“Commerce”中，单击&#x200B;**[!UICONTROL Save]**。

## 编辑经理帐户详细信息 {#edit-manager-account}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**。

1. 通过以下任一方式选择帐户：

   * 选中帐户名称旁边的复选框，然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Edit]**。

   * 将光标悬停在帐户名称上，单击&#x200B;**...**，然后单击（/help/search-social-commerce/assets/edit-new.png“编辑”）。

1. 编辑[经理帐户设置](#manager-account-settings)。

1. 单击&#x200B;**[!UICONTROL Re-Authenticate]**&#x200B;并使用经理帐户凭据登录。

   搜索、Social和Commerce会自动捕获和存储身份验证令牌。

1. 在“搜索”、“社交”和“Commerce”中，单击&#x200B;**[!UICONTROL Save]**。

## 重新验证管理员帐户 {#reauthenticate-manager-account}

当OAuth令牌过期或失效时，对经理帐户重新进行身份验证。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**。

1. 将光标放在帐户名称上，单击&#x200B;**...**，然后单击&#x200B;**[!UICONTROL Reauthenticate]**。

1. 使用经理帐户凭据登录。

   搜索、Social和Commerce会自动捕获和存储新的身份验证令牌。

## 经理帐户设置 {#manager-account-settings}

**[!UICONTROL Manager Account ID]：**&#x200B;广告网络上经理帐户的唯一帐户ID。

**[!UICONTROL Mnaager Account Name]：**&#x200B;要在Search、Social和Commerce中为经理帐户显示的名称。

**[!UICONTROL Login Email]：**&#x200B;与经理帐户登录关联的电子邮件地址。 身份验证需要。

**[!UICONTROL Password]：** （可选）帐户的密码。 输入密码，以便帐户管理员根据需要刷新令牌。

>[!MORELIKETHIS]
>
>* [启用将目标上传到广告网络](/help/search-social-commerce/new-ui/goals/objectives/objective-upload-to-networks.md)
>* [管理通知](/help/search-social-commerce/new-ui/notifications-manage.md)

<!--
I don't see this yet in new UI:
>* [Upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
-->
