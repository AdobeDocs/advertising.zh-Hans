---
title: 管理广告网络帐户
description: 了解如何设置和管理广告网络帐户的帐户详细信息。
exl-id: 4038d03b-63e2-4953-89df-37f7b5f68652
feature: Search Campaign Management
source-git-commit: 304b3589109fe9ddf4d2f0df84c7fa45aa3726d2
workflow-type: tm+mt
source-wordcount: '2078'
ht-degree: 0%

---

# 管理广告网络帐户

<!-- Probably need to change the page title. If I update the filename, get B. to create a redirect to the new URL. -->

以下说明用于创建和编辑广告网络帐户详细信息、刷新帐户的[!DNL oAuth]令牌以及禁用帐户。

<!-- Move out info about Naver?  Then change to the following:  Following are instructions for creating and editing account details for an ad network account that Search, Social, & Commerce will sync using the ad network's API; refreshing the [!DNL oAuth] token for an account; and disabling accounts. -->

<!-- Also update Description metadata to "Learn how to set up and manage account details for an ad network account synced via the ad network API." -->

有关每个广告网络可用功能的详细信息，请参阅[支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)。

## 创建广告网络帐户详细信息 {#create-account}

*仅限代理客户经理、Adobe客户经理和管理员用户角色*

要启用帐户的同步或跟踪，您必须创建包含帐户访问凭据和跟踪选项且状态为&#x200B;*活动*&#x200B;的相应帐户记录。

>[!NOTE]
>
>* 不支持新的[!DNL Baidu]帐户。
>* 要在广告网络上创建实际的帐户，请转到广告网络的网站。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]** \> **[!UICONTROL Accounts]**。

1. 在数据表上方的工具栏中，单击![创建](/help/search-social-commerce/assets/add.png "创建")。

1. 指定[帐户设置](#account-settings)：

   1. 单击广告网络的名称，然后单击&#x200B;**[!UICONTROL Next]**。

   1. 在&#x200B;**[!UICONTROL Account Details]**&#x200B;部分中，输入帐户详细信息。

      对于使用登录授权类型“[!UICONTROL oAuth]”的广告网络，允许Search、Social和Commerce使用[OAuth授权协议](https://oauth.net/2/)访问该帐户：

      1. 输入帐户的&#x200B;**[!UICONTROL Login]**&#x200B;值，或者输入密码，然后单击&#x200B;**[!UICONTROL Authenticate]**。

         最佳实践是使用登录来获取对帐户的API访问权限。 在要加密并保存密码时输入密码，以便Adobe帐户团队可以根据需要刷新令牌。

      1. （如果您未登录到广告商的帐户）请登录到广告商的广告帐户。 最佳实践是使用凭据来API访问帐户。

      1. 在“请求权限/访问权限”屏幕中，单击按钮确认权限。

      1. 在打开的弹出窗口中复制身份验证字符串，并将该字符串粘贴到&#x200B;**[!UICONTROL oAuth Token]**&#x200B;字段中。

      1. 指定剩余帐户详细信息。

   1. 单击&#x200B;**[!UICONTROL Set Account Tracking]**，然后输入跟踪设置。

1. 单击&#x200B;**[!UICONTROL Post]**。

   可在24小时左右的时间内在Search、Social和Commerce中找到帐户中所有促销活动的最新成本和点击数据。 默认情况下，数据在最近5-10天内均可用，具体取决于广告网络。 但是，如有必要，项目启动团队可以检索过去60天的数据。

## 编辑广告网络帐户详细信息 {#edit-account}

*仅限代理客户经理、Adobe客户经理和管理员用户角色*

如果帐户凭据发生更改，您想要跨帐户更改默认跟踪参数，或者想要启用或禁用帐户的活动，然后编辑帐户详细信息。

>[!NOTE]
>
>要编辑广告网络上的实际帐户，请转到广告网络的网站。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]** \> **[!UICONTROL Accounts]**。

1. 将光标放在帐户名称上，单击![更多](/help/search-social-commerce/assets/more-filters.png "更多")，然后选择&#x200B;**[!UICONTROL Edit]**。

1. 编辑[帐户设置](#account-settings)：

   1. （可选）编辑帐户详细信息。

   1. （可选）单击&#x200B;**[!UICONTROL Set Account Tracking]**，然后编辑跟踪设置。

1. 单击&#x200B;**[!UICONTROL Post]**。

   >[!NOTE]
   >
   >搜索、社交和Commerce必须将新帐户数据与广告网络上的帐户数据同步。 此事件每天自动发生一次，或者在Search、Social和Commerce检测到广告网络上的更改时更频繁。

## 刷新搜索帐户的oAuth访问令牌 {#refresh-oauth-tokens}

*仅限代理客户经理、Adobe客户经理和管理员用户角色*

如果Search、Social和Commerce使用[OAuth授权协议](https://oauth.net/2/)访问帐户且帐户凭据发生更改，或者需要其他访问权限才能支持Search、Social和Commerce中的新功能，则必须获取帐户的新访问令牌。

如果新功能需要新令牌，您的Adobe客户团队将通知您。

1. （如果您在同一浏览器应用程序中登录到同一广告网络的其他帐户）注销除广告商帐户之外的任何其他帐户。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]** \> **[!UICONTROL Accounts]**。

1. 将光标放在帐户名称上，单击![更多](/help/search-social-commerce/assets/more-filters.png "更多")，然后选择&#x200B;**[!UICONTROL Edit]**。

1. 获取新的访问令牌：

   1. 单击&#x200B;**[!UICONTROL Get oAuth Token]**。

   1. （如果您未登录到广告商的帐户）请登录到广告商的广告帐户。 最佳实践是使用凭据来API访问帐户。

   1. 在“请求权限/访问权限”屏幕中，单击按钮确认权限。

   1. 在打开的弹出窗口中复制身份验证字符串，并将该字符串粘贴到&#x200B;**[!UICONTROL oAuth Token]**&#x200B;字段中。

1. 单击&#x200B;**[!UICONTROL Post]**。

## 启用或禁用广告网络帐户 {#enable-disable-account}

*仅限代理客户经理、Adobe客户经理和管理员用户角色*

当您启用广告网络帐户时，Search、Social和Commerce会将促销活动数据与帐户同步（如果支持），并为项目组合中的促销活动推送自动竞价和/或促销活动预算。 禁用广告网络帐户后，搜索、社交和Commerce将停止该帐户上的所有活动。 虽然仍会存储当帐户处于活动状态时收集的数据，但营销活动管理视图和报表并不包含禁用帐户时段的数据。 您稍后可以重新启用帐户以继续使用该帐户的活动。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]** \> **[!UICONTROL Accounts]**。

1. 执行以下任一操作：

   * （要更改单个帐户的状态）将光标悬停在帐户名称上，单击![更多](/help/search-social-commerce/assets/more-filters.png "更多")，然后选择&#x200B;**[!UICONTROL Edit]**。 将&#x200B;**[!UICONTROL Status]**&#x200B;更改为&#x200B;*已启用*&#x200B;或&#x200B;*已禁用*，然后单击&#x200B;**[!UICONTROL Post]**。

   * （要更改一个或多个帐户的状态），请执行以下操作：

      1. 选中每个帐户旁边的复选框。

         有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

      1. 在数据表上方的工具栏中，单击![激活图标](/help/search-social-commerce/assets/activate.png "激活图标")以启用帐户，或单击![“禁用”图标](/help/search-social-commerce/assets/disable.png "“禁用”图标")以禁用帐户。

## 广告网络帐户设置 {#account-settings}

>[!NOTE]
>
>只有代理帐户管理员、[!DNL Adobe]帐户管理员和管理员用户可以配置帐户设置。

### 帐户详细信息

**[!UICONTROL SE Account ID]：** （除[!DNL Naver]和[!DNL Yandex]帐户之外的所有帐户；仅对于新帐户可编辑）广告网络分配的帐户ID。

>[!NOTE]
>
>此处不支持广告网络管理器帐户。 要为[!DNL Microsoft Advertising]或[!DNL Yandex]标识经理帐户，请分别使用主帐户ID或MCC帐户字段。 要[设置 [!DNL Google Ads] 经理帐户](/help/search-social-commerce/admin/manager-accounts.md)的凭据，请转到[!UICONTROL Admin] \> [!UICONTROL Manager Accounts]。

**[!UICONTROL Account Name]：**&#x200B;要在Search、Social和Commerce中为帐户显示的名称。

>[!NOTE]
>
>如果您集成了“搜索”、“Social”和“Commerce-Adobe Analytics”，并更改了搜索帐户的名称，请让您的Adobe帐户团队更新映射。

**[!UICONTROL Login Details]： \[登录类型\]** - （仅限[!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center]）是否使用以下方式授权登录帐户：

* *[!UICONTROL oAuth]* （默认）：使用[[!DNL OAuth] 授权协议](https://oauth.net/2/)。

* *[!UICONTROL Password]：*&#x200B;要使用客户端密码。

对于[!DNL Microsoft Advertising]帐户，只能使用[!DNL oAuth]授权的登录。

**[!UICONTROL Login Details]： [!UICONTROL Login]：** （除[!DNL Naver]之外的所有广告网络）用于启用帐户API访问的登录名或ID。

**[!UICONTROL Login Details]： [!UICONTROL OAuth Token]：** （[!DNL Microsoft Advertising] [!DNL oAuth]已启用，以及[!DNL Meta]和[!DNL Yandex]以外的所有其他网络）帐户令牌可使用[[!DNL OAuth] 授权协议](https://oauth.net/2/)授权登录。

**[!UICONTROL Login Details]： [!UICONTROL Password]：** （除[!DNL Naver]之外的所有广告网络）帐户的密码。 对于[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads]和[!DNL Yandex]上启用密码的帐户，此字段必填。 对于启用了[!DNL oAuth]的帐户，此字段为可选字段；当您要加密并保存密码以便帐户管理员根据需要刷新令牌时，可使用该字段。

**[!UICONTROL Login Details]： [!UICONTROL Access Key]：** （仅限[!DNL Yandex]帐户）要使用的开发人员帐户的访问密钥。

**[!UICONTROL Currency]：**&#x200B;帐户使用的货币的缩写。 对于新[!DNL Naver]帐户，此字段可编辑。 对于所有其他搜索网络，保存记录后，该值将自动填充为广告网络上的帐户配置的货币。

**[!UICONTROL Landing Page Suffix]** （仅限[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户；可选）要附加到最终URL末尾以跟踪信息的所有参数；包括您的企业必须跟踪的所有参数。

示例： `param1=value1&param2=value2`

使用Adobe Advertising点击跟踪的帐户必须在后缀中包含广告网络的点击标识符(`msclkid`为[!DNL Microsoft Advertising]；Google为`gclid`)。 具有Adobe Analytics集成的帐户必须使用AMO ID参数（以`s_kwcid`开头）。 如果该帐户具有服务器端AMO ID实施，则当用户单击广告时，参数会自动添加；否则，您必须在此处手动添加该参数。 查看[的 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)必需后缀格式和[的 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)必需后缀格式。

>[!NOTE]
>
>* [!UICONTROL Auto Upload]跟踪设置未更新此字段。
>* 较低级别的最终URL后缀将覆盖帐户级别的后缀。 为便于维护，除非需要对各个帐户组件进行不同的跟踪，否则请仅使用帐户级别的后缀。 要在广告组级别或更低级别配置后缀，请使用广告网络的编辑器。

**时区：** （除[!DNL Baidu]和[!DNL Yahoo! Display Network]之外的所有广告网络）广告商的时区。 此字段对于新[!DNL Naver]帐户是可编辑和可选的。 对于所有其他搜索网络，保存记录后，该值将自动填充为广告商的Search、Social和Commerce帐户配置的时区。

**状态：**&#x200B;搜索、社交和Commerce中的帐户状态：

* *已启用：*&#x200B;搜索、社交和Commerce将营销活动数据与帐户同步（如果支持），并针对项目组合中的营销活动推送自动竞价和/或营销活动预算。
* *已禁用：*&#x200B;搜索、社交和Commerce停止帐户上的所有活动。 虽然会存储当帐户处于活动状态时收集的数据，但营销活动管理视图和报表并不包含与帐户暂停时间相关的数据。 您稍后可以重新激活帐户以继续使用该帐户的活动。

**跟踪模板** - （仅限[!DNL Google Ads]、[!DNL Microsoft Advertising]和[!DNL Yahoo! Japan Ads]帐户；可选）帐户的默认跟踪模板，它指定所有登入域重定向和跟踪参数，并将最终/登陆页面URL嵌入到参数中。 示例： `{lpurl}?source={network}&id=5`或`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`以包含重定向。

* 嵌入最终URL：

   * （仅限[!DNL Google Ads]和[!DNL Microsoft Advertising]）有关指示跟踪模板中最终URL的参数列表，请参阅[!DNL Microsoft Advertising]文档[[!DNL Microsoft Advertising] 中“可用的](https://help.ads.microsoft.com/#apex/3/en/56799)参数”部分中的（[!DNL Google Ads]仅限）[!DNL ValueTrack]文档[[!DNL Google Ads] 或（](https://support.google.com/google-ads/answer/6305348)仅限）跟踪模板参数。

   * （仅限[!DNL Yahoo! Japan Ads]）使用参数`!{lpurl}`指示登陆页面URL。

* 您可以选择包含URL参数以及为营销活动定义的任何自定义参数，这些参数以&amp;号分隔，如`{lpurl}?matchtype={matchtype}&device={device}`。

* 您可以选择添加第三方重定向和跟踪。

* 当营销活动设置包括“[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]”时，Search、Social和Commerce会在您保存记录时自动为其自己的重定向和跟踪代码添加前缀。

>[!NOTE]
>
>* 对于[!DNL Google Ads]，请避免使用宏，这些宏不会替代来自启用并行跟踪的源的点击。 如果广告商必须使用宏，则Adobe客户团队应与客户支持或实施团队合作来添加宏。
>* 最细粒度级别的跟踪模板将覆盖所有更高级别的值。 例如，如果帐户设置和关键字设置都包含一个值，则应用关键字值。
>* 如果您在广告、站点链接或关键词级别更新跟踪模板，则会重新提交相关广告以供审阅。 您可以在帐户、营销活动或广告组级别更新跟踪模板，而无需重新提交广告以供审批。

**[!UICONTROL Master Account ID]：** （仅限[!DNL Microsoft Advertising]帐户）与该帐户关联的代理/管理帐户的ID。

**[!UICONTROL MCC Account]：** （仅限[!DNL Yandex]个帐户；可选）与该帐户关联的代理/管理帐户。 要删除现有关联，请选择“[!UICONTROL No MCC Account]”。

**[!UICONTROL Application ID]：** （仅限[!DNL Yandex]帐户）要用于帐户的开发人员令牌。 所有[!DNL Yandex]帐户都使用相同的令牌。

**[!UICONTROL Purse Campaign ID]：** （[!DNL Yandex]个帐户的“共享帐户”设置仅被禁用；可选）用于支付帐户中所有广告促销活动的促销活动的数字ID。

**[!UICONTROL Finance Token]：** （[!DNL Yandex]个帐户的“共享帐户”设置仅被禁用；可选）用于财务相关API调用的开发人员令牌，如在广告商的促销活动之间重新分配钱包中的款项，这是组合优化所必需的。

### 帐户跟踪

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]：** （仅适用于[!UICONTROL EF Redirect]）未实现

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **S_kwcid格式：** (现有[!DNL Google Ads]帐户适用于具有Adobe Advertising-Adobe Analytics集成且尚未迁移AMO ID (s_kwcid)的广告商)

此帐户使用旧版的AMO ID跟踪代码格式，从而允许Adobe Advertising与Adobe Analytics共享该帐户的相关数据。 [最新格式](/help/integrations/analytics/ids.md#amo-id-formats)包含促销活动ID和广告组ID的参数，在Analytics中，要在促销活动和广告组级别准确报告效果最佳的[!DNL Google Ads]促销活动以及草稿和实验促销活动，必须使用这些参数：

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

如果此帐户需要在营销活动和广告组级别报告，请单击[!UICONTROL Edit]（铅笔）图标，然后单击&#x200B;**[!UICONTROL Migrate to new s_kwcid format]**&#x200B;以更改为新格式。 对于不包含这些促销活动类型的帐户，迁移到新格式是可选的，但建议这样做。

有关完整说明，请参阅“[更新 [!DNL Google Ads] 帐户](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)的AMO ID跟踪代码”。

**报表包名称：**(仅适用于带令牌的EF重定向；带有Adobe Advertising-Adobe Analytics集成的广告商；可选)一个或多个Analytics报表包，Search、Social和Commerce会向其发送从广告网络收集的数据，包括实体分类和帐户的点击数据。 此功能仅适用于受支持的广告网络。

对于要显示在报表包中的数据，必须(a)为帐户配置服务器端AMO ID功能，或者(b)启用设置为“[!UICONTROL Enable Advertising reporting in Analytics]”的广告商级别设置。 此外，必须将广告商的Analytics帐户配置为从Search、Social和Commerce接收数据。 有关更多信息，请与您的Adobe客户团队联系。

>[!MORELIKETHIS]
>
>* [关于广告网络帐户](ad-network-account-about.md)
>* [管理商家中心帐户](merchant-account-manage.md)
>* [更新 [!DNL Google Ads] 帐户的s_kwcid跟踪代码](update-amo-id-google.md)
