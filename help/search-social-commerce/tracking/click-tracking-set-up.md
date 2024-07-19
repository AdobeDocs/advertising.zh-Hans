---
title: 设置基于Cookie的点击跟踪
description: 了解如何设置和验证点击跟踪标记。
exl-id: 3f2b09bc-9794-41d1-89fc-0d239bad2fb1
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# 设置基于Cookie的点击跟踪

要跟踪Search、Social和Commerce的点击量，必须配置和验证以下元素。

1. (Adobe客户团队)将广告商设置为像素客户。

1. [为每个广告商的广告网络帐户和营销活动指定正确的跟踪选项](#set-up-click-tracking-options)。

1. 如有必要，[生成跟踪URL并为某些促销活动元素上载它们](#generate-upload-tracking-urls)。

1. [验证一些点击跟踪URL的格式，并测试它们以验证是否打开了正确的登陆页面](#validate-tracking-urls)。

## 为广告网络帐户和营销活动设置跟踪选项 {#set-up-click-tracking-options}

*仅代理帐户管理员、[!DNL Adobe]帐户管理员和管理员用户角色*

1. 对于每个广告网络帐户，执行以下操作：

   1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]>[!UICONTROL Accounts]**。

   1. 将光标悬停在帐户名称上，单击![菜单图标](/help/search-social-commerce/assets/arrow-dropdown-menu.png "菜单图标")，然后选择&#x200B;**[!UICONTROL Edit]**。

   1. 单击&#x200B;**[!UICONTROL Set Account Tracking]**。

   1. 对于[!UICONTROL Tracking Type]设置，选择&#x200B;**[!UICONTROL EF Redirect]**。

   1. (要允许Search、Social和Commerce与Adobe Analytics交换数据或跟踪[!DNL Apple Safari]中发生的转化)请选择[!UICONTROL Redirect Type]选项&#x200B;**[!UICONTROL Token]**。

   1. （可选）打开&#x200B;**[!UICONTROL Auto Upload]**&#x200B;选项，以便下次在Search、Social和Commerce与其同步时将新跟踪URL自动上传到广告网络。 此值作为帐户中所有营销活动的默认值继承，但可以在营销活动级别覆盖。

1. 对于每个活动，请执行以下操作：

   1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]>[!UICONTROL Campaigns]**。

   1. 将光标悬停在促销活动名称上，单击![菜单图标](/help/search-social-commerce/assets/arrow-dropdown-menu.png "菜单图标")，然后选择&#x200B;**[!UICONTROL Edit]**。

   1. 单击&#x200B;**[!UICONTROL Set Campaign Tracking]**。 然后选择选项&#x200B;**[!UICONTROL Override Account Tracking]**。

   1. 对于[!UICONTROL Tracking Type]设置，选择&#x200B;**[!UICONTROL EF Redirect]**。

   1. (要允许Search、Social和Commerce与Adobe Analytics交换数据或跟踪[!DNL Apple Safari]中发生的转化)请选择[!UICONTROL Redirect Type]选项&#x200B;**[!UICONTROL Token]**。

   1. （可选）打开&#x200B;**[!UICONTROL Auto Upload]**&#x200B;选项，以便下次在Search、Social和Commerce与其同步时将新跟踪URL自动上传到广告网络。 此值作为帐户中所有营销活动的默认值继承，但可以在营销活动级别覆盖。

## 生成和上传跟踪URL {#generate-upload-tracking-urls}

请参阅“[何时以及如何生成点击跟踪URL](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)”。

### 测试点击跟踪网址的格式 {#validate-tracking-urls}

验证是否为点击跟踪URL打开了正确的登陆页面。

1. 通过向广告商的暂存环境发送流量来模拟广告点击：

   1. 在文本编辑器中，粘贴点击跟踪URL，将登陆页面URL更改为指向广告商暂存环境中的同一页面，然后将新URL粘贴到浏览器的地址栏中，然后按&#x200B;**[!DNL Enter]**&#x200B;键。

   1. 在浏览器存储的Cookie中查找Cookie。

   1. 在暂存网站上完成一个事务，并验证成功页面是否触发了正确的像素。 像素跟踪的实际参数因广告商和跟踪URL而异。 在以下示例中，广告商希望跟踪新应用程序的数量和新收入金额：

      对于新的最终用户（使用新的Cookie），应触发以下像素：

      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`

      如果Cookie不是最新的，则应触发以下像素：

      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


1. 对域中的多个点击跟踪URL重复此操作。

1. 对每个域重复步骤1，相应地使用不同的登陆页面。

1. 如果需要，请确认Search、Social和Commerce可以看到测试期间生成的交易ID (`ev_transid`)的像素。

>[!MORELIKETHIS]
>
>* [何时以及如何生成点击跟踪URL](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
