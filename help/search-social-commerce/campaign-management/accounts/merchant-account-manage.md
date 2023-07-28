---
title: 管理商家帐户
description: 了解如何设置和管理商户中心帐户的帐户详细信息。
exl-id: eca58f55-f056-46b3-b192-2849690e8bcc
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# 管理商家帐户

*仅限代理客户经理、Adobe客户经理和管理员用户角色*

Search、Social &amp; Commerce每天可以下载并显示广告商的Google商户中心或Microsoft商户中心帐户的任何产品数据。 此外，搜索、Social和Commerce可以根据商户帐户的内容自动创建广告。要直接使用Search、Social和Commerce中的产品数据，您必须创建相应的帐户记录，其中包含帐户访问凭据和访问权限 *已启用*.

>[!NOTE]
>
>您无法删除商家帐户记录。 您可以将帐户类型更改为，以禁用对帐户的访问 *已禁用*.

## 创建商家帐户详细信息 {#create-merchant-account}

*仅限代理客户经理、Adobe客户经理和管理员用户角色*

要查看商户帐户的产品数据和生成跟踪模板，以及根据数据创建广告，您必须创建相应的帐户记录，其中包含帐户访问凭据以及帐户的访问权限 *已启用*.

>[!NOTE]
>
>要在商家网络上创建实际的帐户，请访问该网络的网站。

1. 在主菜单中，单击 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]**，此时将打开 [!UICONTROL Accounts] 选项卡。

1. 在数据表上方的工具栏中，单击 **[!UICONTROL Create Account]**.

1. 指定 [商家帐户设置](#merchant-account-settings)：

   1. 在 [!UICONTROL Product Source] 菜单，选择商家中心。

   1. (需要 [!DNL Google Ads] 帐户；可选 [!DNL Microsoft Advertising] 帐户)允许搜索、社交和商务使用访问帐户 [[!DNL OAuth] 授权协议](https://oauth.net/2/)：

      1. ([!DNL Microsoft Advertising] 仅限帐户)选择 **[!UICONTROL oAuth]**.

      1. 单击 **[!UICONTROL Enable Connection]**.

      1. （如果您未登录到广告商的帐户）请登录到广告商的帐户。 最佳实践是使用凭据来访问商户中心帐户的内容API。

      1. 在请求访问/权限屏幕中，单击按钮确认权限。

      1. 在打开的弹出窗口中复制身份验证字符串，并将该字符串粘贴到 **[!UICONTROL oAuth Token]** 字段。

      1. 指定其他帐户设置。

1. 单击 **[!UICONTROL Save]**.

   下次每日同步流程（大约为用户当地时区的06:00）后，可在Search、Social &amp; Commerce中找到帐户中所有产品的属性数据。 然后，您可以使用产品数据通过清单馈送来自动创建广告。

## 编辑商家帐户详细信息 {#edit-merchant-account}

*仅限代理客户经理、Adobe客户经理和管理员用户角色*

如果帐户凭据发生更改，或者您希望停止检索和使用商户帐户的数据，则编辑帐户详细信息。

>[!NOTE]
>
>要编辑商家网络上的实际帐户，请转到该网络的网站。

1. 在主菜单中，单击 **[!UICONTROL Search]\> [!UICONTROL Campaigns] \>[!UICONTROL Products]**，此时将打开 [!UICONTROL Accounts] 选项卡。

1. 在帐户名称旁边，单击 ![查看/编辑设置](/help/search-social-commerce/assets/settings.png "查看/编辑设置").

1. 编辑 [商家帐户设置](#merchant-account-settings).

1. 单击 **[!UICONTROL Save]**.

>[!NOTE]
>
>搜索、Social和Commerce必须将新帐户数据与商家网络上的帐户数据同步。 此调用每天大约在用户本地时区的06:00自动发生一次。

## 禁用对商户帐户的访问 {#disable-merchant-account}

*仅限代理客户经理、Adobe客户经理和管理员用户角色*

禁用商家帐户时，搜索、社交和商务不会登录到帐户，因此不会检索更新的产品数据。 在启用帐户时收集的数据仍会存储，并且使用产品数据创建的现有广告不会根据馈送模板和馈送数据设置进行更新、暂停或删除。

1. 在主菜单中，单击 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** ，此时将打开 [!UICONTROL Accounts] 选项卡。

1. 在帐户名称旁边，单击 ![查看/编辑设置](/help/search-social-commerce/assets/settings.png "查看/编辑设置").

1. 更改 [!UICONTROL EF Account Type] 到 **[!UICONTROL Disabled]**.

1. 单击 **[!UICONTROL Save]**.

## 商家帐户设置 {#merchant-account-settings}

>[!NOTE]
>
>只有代理客户经理， [!DNL Adobe] 帐户管理员和管理员用户角色可以配置商家帐户设置。

**[!UICONTROL Product Source]：** 商户网络。 您无法更改现有帐户的值。

**[!UICONTROL OAuth Token]：** ([!DNL Google Merchant Center] 仅限帐户)帐户令牌，用于授权使用 [[!DNL OAuth] 授权协议](https://oauth.net/2/).

**[!UICONTROL Auth Type]：** ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] 仅限于)是否授权通过以下方式登录帐户：

* *[!UICONTROL Client login]：* 使用客户端的登录名。

* *[!UICONTROL oAuth]* （默认）：使用 [[!DNL OAuth] 授权协议](https://oauth.net/2/).

**[!UICONTROL Access Key]：** ([!DNL Microsoft Merchant Center] 仅限)开发人员帐户要使用的访问密钥。

**[!UICONTROL Account Name]：** 在“搜索”、“社交”和“商务”中显示的帐户名称。

**[!UICONTROL Login]：** 帐户的登录名或ID。

**[!UICONTROL Password]：** 帐户的密码。

**[!UICONTROL Confirm Password]：** 帐户的密码。

**[!UICONTROL EF Account Type]：** 搜索、社交和商务是否将访问帐户：

* *[!UICONTROL Enabled]* （默认）： Search、Social和Commerce可以登录帐户以检索产品数据。

* *[!UICONTROL Disabled]：* Search、Social和Commerce不会登录到帐户，因此不会检索更新的产品数据。 在启用帐户时收集的数据仍会存储，并且使用产品数据创建的现有广告不会根据馈送模板和馈送数据设置进行更新、暂停或删除。

**[!UICONTROL Account ID]：** 商家帐户ID。 如果您只有一个具有指定登录信息的帐户，则此值是可选的。

**[!UICONTROL Time Zone]：** 广告商的时区。 使用为广告商的搜索、社交和商务帐户信息（在创建帐户时设置）配置的相同时区。 您无法更改现有帐户的值。

>[!MORELIKETHIS]
>
>* [关于广告网络帐户](ad-network-account-about.md)
>* [管理广告网络帐户](ad-network-account-manage.md)
