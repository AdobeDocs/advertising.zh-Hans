---
title: 登录到DSP
description: 了解如何登录到DSP。
feature: DSP Introduction
exl-id: 1704cd75-81f8-4715-a177-69a03093ba1d
source-git-commit: a7e28cb2e37e1c9b6951f844b5f542ae2c8ac1a0
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# 登录到Adobe Advertising DSP

Adobe Advertising DSP正在过渡到Adobe Identity Management服务(IMS)以进行登录身份验证。 IMS提供对支持IMS的所有[!DNL Adobe]产品(包括Real-Time Customer Data Platform、Customer Journey Analytics、Target和Analytics)的单一登录(SSO)访问权限。 更改后：

* 您可以使用一个[!DNL Adobe ID]从Experience Cloud登录页面或旧版DSP登录页面跨[!DNL Adobe]产品登录。 您的[!DNL Adobe ID]提供用户配置文件管理。 在将来的版本中，您将能够从顶部菜单中更改DSP帐户、IMS组织帐户和[!DNL Adobe]产品。

* 支持企业身份验证。

* 您可以保持24小时的登录状态，而不是每小时登录一次。

您当前的DSP凭据将在2025年6月26日之前保持活动状态，以便您能够为更改做好准备。

## 使用旧版DSP登录进行身份验证

* 转到[advertising.adobe.com](https://advertising.adobe.com)，然后使用旧版DSP凭据登录。

## 使用[!DNL Adobe ID]进行身份验证

1. 打开以下任一登录屏幕：

   * 转到[advertising.adobe.com](https://advertising.adobe.com)。 在“[!UICONTROL Sign in with the Adobe Experience Cloud account]”下，单击&#x200B;**[!UICONTROL Continue]**。

   * 转到[experience.adobe.com](https://experience.adobe.com)。

1. 输入您的凭据：

   * 如果您已经使用[!DNL Adobe]帐户，请使用现有凭据登录。

   * 如果您没有[!DNL Adobe]帐户，请查找一封邀请您创建[!DNL Adobe]帐户的电子邮件。 您将收到每个DSP帐户的一个邀请。 按照电子邮件中的链接设置您的凭据。 如果您有多个DSP帐户，请按照相关说明关联它们。

1. 选择您的组织：

   * 如果出现提示，请选择**个人帐户”或&#x200B;**公司或学校帐户**。

   * 如果您有权访问多个IMS组织，请选择正确的IMS组织。

有关Experience Cloud界面（包括管理用户配置文件）的更多信息，请参阅“[Experience Cloud界面和管理](https://experienceleague.adobe.com/en/docs/core-services/interface/experience-cloud)”。

### 故障排除

有关一般登录问题，另请参阅“[解决Adobe帐户登录问题](https://helpx.adobe.com/manage-account/kb/account-password-sign-help.linkfree.html)”。

#### 启用新的[!DNL Adobe] IMS登录是否存在任何先决条件？

要添加新登录帐户，请与您的Adobe帐户团队共享电子邮件地址。 团队会将您的地址添加到已将DSP配置到的IMS组织的用户列表中。

同时，用户可以继续使用其旧版DSP凭据。

#### 使用Adobe IMS帐户登录后，我将被重定向回adobe.advertising.com登录页面。

与您的IMS组织管理员确认，您使用的电子邮件已添加到IMS组织。 如果管理员确认已将您添加到IMS组织，请让您的Adobe帐户团队配置您的帐户以使用DSP。

在此期间，您可以继续使用旧版DSP凭据。

#### 我使用错误的电子邮件地址登录，该地址让我登录到[!DNL Adobe]，但不提供DSP访问权限。

1. 转到[experience.adobe.com](https://experience.adobe.com)并注销。

1. 转到[advertising.adobe.com](https://advertising.adobe.com)并使用正确的电子邮件ID登录。

#### 我的[!DNL Adobe] IMS帐户和DSP帐户已注册其他电子邮件。 如何使用我的[!DNL Adobe] IMS帐户登录？

请让您的Adobe帐户团队配置现有的[!DNL Adobe] IMS帐户以使用DSP。
