---
title: 管理商家帐户
description: 了解如何设置和管理商户中心帐户的帐户详细信息。
exl-id: 7d940e45-ea49-470b-98d0-0196593228cb
feature: Search Campaign Management
source-git-commit: cb65108fcc60c11b901e3b43c292ad5a94192b9f
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# 管理商家帐户

*仅限代理客户经理、Adobe客户经理和管理员用户角色*

搜索、Social和Commerce可以每天下载并显示广告商的Google商户中心或Microsoft商户中心帐户的产品数据。 此外，Search、Social和Commerce可以根据商户帐户的内容自动创建广告。要直接使用Search、Social和Commerce中的产品数据，您必须创建相应的帐户记录，其中包含帐户访问凭据以及已启用&#x200B;*的访问权限*。

>[!NOTE]
>
>您无法删除商家帐户记录。 通过将帐户类型更改为&#x200B;*已禁用*，您可以禁用对帐户的访问。

## 创建商家帐户详细信息 {#create-merchant-account}

*仅限代理客户经理、Adobe客户经理和管理员用户角色*

要查看商户帐户的产品数据并生成跟踪模板，以及根据数据创建广告，您必须创建相应的帐户记录，该记录包含帐户访问凭据并具有对帐户&#x200B;*已启用*&#x200B;的访问权限。

>[!NOTE]
>
>要在商家网络上创建实际的帐户，请访问该网络的网站。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]**，这将打开到[!UICONTROL Accounts]选项卡。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Create Account]**。

1. 指定[商家帐户设置](#merchant-account-settings)：

   1. 在[!UICONTROL Product Source]菜单中，选择商家中心。

   <!--

   1. ([!DNL Meta Ads] accounts only) Log in to the [!DNL Meta Ads] account.

   And are there additional steps just for Meta? If so, create a separate procedure for it.
   
   -->

   1. （[!DNL Google Ads]帐户必需；[!DNL Microsoft Advertising]帐户可选）允许Search、Social和Commerce使用[[!DNL OAuth] 授权协议](https://oauth.net/2/)访问该帐户：

      1. （仅限[!DNL Microsoft Advertising]帐户）选择&#x200B;**[!UICONTROL oAuth]**。

      1. 单击&#x200B;**[!UICONTROL Enable Connection]**。

      1. （如果您未登录到广告商的帐户）请登录到广告商的帐户。 最佳实践是使用凭据来访问商户中心帐户的内容API。

      1. 在请求访问/权限屏幕中，单击按钮确认权限。

      1. 在打开的弹出窗口中复制身份验证字符串，并将该字符串粘贴到&#x200B;**[!UICONTROL oAuth Token]**&#x200B;字段中。

      1. 指定其他帐户设置。

1. 单击&#x200B;**[!UICONTROL Save]**。

   下次进行每日同步后，可在Search、Social和Commerce中找到帐户中所有产品的属性数据（大约为用户的当地时区06:00）。 然后，您可以使用产品数据通过清单馈送来自动创建广告。

## 编辑商家帐户详细信息 {#edit-merchant-account}

*仅限代理客户经理、Adobe客户经理和管理员用户角色*

如果帐户凭据发生更改，或者您希望停止检索和使用商户帐户的数据，则编辑帐户详细信息。

>[!NOTE]
>
>要编辑商家网络上的实际帐户，请转到该网络的网站。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]\> [!UICONTROL Campaigns] \>[!UICONTROL Products]**，这将打开到[!UICONTROL Accounts]选项卡。

1. 在帐户名称旁边，单击![查看/编辑设置](/help/search-social-commerce/assets/settings.png "查看/编辑设置")。

1. 编辑[商家帐户设置](#merchant-account-settings)。

1. 单击&#x200B;**[!UICONTROL Save]**。

>[!NOTE]
>
>搜索、社交和Commerce必须将新帐户数据与商家网络上的帐户数据同步。 此调用每天大约在用户本地时区的06:00自动发生一次。

## 禁用对商户帐户的访问 {#disable-merchant-account}

*仅限代理客户经理、Adobe客户经理和管理员用户角色*

禁用商家帐户时，Search、Social和Commerce不会登录该帐户，因此不会检索更新的产品数据。 在启用帐户时收集的数据仍会存储，并且使用产品数据创建的现有广告不会根据馈送模板和馈送数据设置进行更新、暂停或删除。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** ，这将打开到[!UICONTROL Accounts]选项卡。

1. 在帐户名称旁边，单击![查看/编辑设置](/help/search-social-commerce/assets/settings.png "查看/编辑设置")。

1. 将[!UICONTROL EF Account Type]更改为&#x200B;**[!UICONTROL Disabled]**。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 商家帐户设置 {#merchant-account-settings}

>[!NOTE]
>
>只有代理帐户管理员、[!DNL Adobe]帐户管理员和管理员用户角色可以配置商家帐户设置。

**[!UICONTROL Product Source]：**&#x200B;商家网络。 您无法更改现有帐户的值。

**[!UICONTROL OAuth Token]：** （仅限[!DNL Google Merchant Center]帐户）帐户令牌用于授权使用[[!DNL OAuth] 授权协议](https://oauth.net/2/)登录。

**[!UICONTROL Auth Type]：** （仅限[!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center]）是否使用以下方式授权登录帐户：

* *[!UICONTROL Client login]：*&#x200B;使用客户端的登录名。

* *[!UICONTROL oAuth]* （默认）：使用[[!DNL OAuth] 授权协议](https://oauth.net/2/)。

**[!UICONTROL Access Key]：** （仅限[!DNL Microsoft Merchant Center]）开发人员帐户要使用的访问密钥。

**[!UICONTROL Account Name]：**&#x200B;在Search、Social和Commerce中为帐户显示的名称。

**[!UICONTROL Login]：**&#x200B;帐户的登录名或ID。

**[!UICONTROL Password]：**&#x200B;帐户的密码。

**[!UICONTROL Confirm Password]：**&#x200B;帐户的密码。

**[!UICONTROL EF Account Type]：** Search、Social和Commerce是否访问该帐户：

* *[!UICONTROL Enabled]*（默认）： Search、Social和Commerce可以登录帐户以检索产品数据。

* *[!UICONTROL Disabled]：* Search、Social和Commerce未登录到帐户，因此未检索更新的产品数据。 在启用帐户时收集的数据仍会存储，并且使用产品数据创建的现有广告不会根据馈送模板和馈送数据设置进行更新、暂停或删除。

**[!UICONTROL Account ID]：**&#x200B;商家帐户ID。 如果您只有一个具有指定登录信息的帐户，则此值是可选的。

**[!UICONTROL Time Zone]：**&#x200B;广告商的时区。 使用为广告商的搜索、社交和Commerce帐户信息（在创建帐户时设置）配置的相同时区。 您无法更改现有帐户的值。

>[!MORELIKETHIS]
>
>* [关于广告网络帐户](ad-network-account-about.md)
>* [管理广告网络帐户](ad-network-account-manage.md)
