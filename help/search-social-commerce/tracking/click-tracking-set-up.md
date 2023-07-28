---
title: 设置基于Cookie的点击跟踪
description: 了解如何设置和验证点击跟踪标记。
exl-id: 340aec08-a1a5-4aa5-b666-9c819c1709d0
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# 设置基于Cookie的点击跟踪

要跟踪Search、Social和Commerce的点击量，必须配置和验证以下元素。

1. (Adobe客户团队)将广告商设置为像素客户。

1. [为每个广告商的广告网络帐户和营销活动指定正确的跟踪选项](#set-up-click-tracking-options).

1. 如有必要， [生成跟踪URL并上传它们](#generate-upload-tracking-urls) 促销活动元素。

1. [验证一些点击跟踪URL的格式，然后对其进行测试以验证是否打开了正确的登陆页面](#validate-tracking-urls).

## 为广告网络帐户和营销活动设置跟踪选项 {#set-up-click-tracking-options}

*代理客户经理， [!DNL Adobe] 仅帐户管理员和管理员用户角色*

1. 对于每个广告网络帐户，执行以下操作：

   1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]>[!UICONTROL Accounts]**.

   1. 将光标悬停在帐户名称上，单击 ![菜单图标](/help/search-social-commerce/assets/arrow-dropdown-menu.png "菜单图标")，然后选择 **[!UICONTROL Edit]**.

   1. 单击 **[!UICONTROL Set Account Tracking]**.

   1. 对于 [!UICONTROL Tracking Type] 设置，选择 **[!UICONTROL EF Redirect]**.

   1. (允许Search、Social和Commerce与Adobe Analytics交换数据或跟踪中发生的转化 [!DNL Apple Safari])选择 [!UICONTROL Redirect Type] option **[!UICONTROL Token]**.

   1. （可选）打开 **[!UICONTROL Auto Upload]** 用于在Search、Social和Commerce下次与其同步时自动将新跟踪URL上传到广告网络的选项。 此值作为帐户中所有营销活动的默认值继承，但可以在营销活动级别覆盖。

1. 对于每个活动，请执行以下操作：

   1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]>[!UICONTROL Campaigns]**.

   1. 将光标悬停在促销活动名称上，单击 ![菜单图标](/help/search-social-commerce/assets/arrow-dropdown-menu.png "菜单图标")，然后选择 **[!UICONTROL Edit]**.

   1. 单击 **[!UICONTROL Set Campaign Tracking]**. 然后，选择选项以 **[!UICONTROL Override Account Tracking]**.

   1. 对于 [!UICONTROL Tracking Type] 设置，选择 **[!UICONTROL EF Redirect]**.

   1. (允许Search、Social和Commerce与Adobe Analytics交换数据或跟踪中发生的转化 [!DNL Apple Safari])选择 [!UICONTROL Redirect Type] option **[!UICONTROL Token]**.

   1. （可选）打开 **[!UICONTROL Auto Upload]** 用于在Search、Social和Commerce下次与其同步时自动将新跟踪URL上传到广告网络的选项。 此值作为帐户中所有营销活动的默认值继承，但可以在营销活动级别覆盖。

## 生成和上传跟踪URL {#generate-upload-tracking-urls}

请参阅&quot;[何时以及如何生成点击跟踪URL](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)“

### 测试点击跟踪网址的格式 {#validate-tracking-urls}

验证是否为点击跟踪URL打开了正确的登陆页面。

1. 通过向广告商的暂存环境发送流量来模拟广告点击：

   1. 在文本编辑器中，粘贴点击跟踪URL，将登陆页面URL更改为指向广告商暂存环境中的同一页面，然后将新URL粘贴到浏览器的地址栏中，然后按 **[!DNL Enter]** 键。

   1. 在浏览器存储的Cookie中查找Cookie。

   1. 在暂存网站上完成一个事务，并验证成功页面是否触发了正确的像素。 像素跟踪的实际参数因广告商和跟踪URL而异。 在以下示例中，广告商希望跟踪新应用程序的数量和新收入金额：

      对于新的最终用户（使用新的Cookie），应触发以下像素：

      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`

      如果Cookie不是最新的，则应触发以下像素：

      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


1. 对域中的多个点击跟踪URL重复此操作。

1. 对每个域重复步骤1，相应地使用不同的登陆页面。

1. 如果需要，请确认Search、Social和Commerce可以查看交易ID的像素(`ev_transid`)。

>[!MORELIKETHIS]
>
>* [何时以及如何生成点击跟踪URL](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
