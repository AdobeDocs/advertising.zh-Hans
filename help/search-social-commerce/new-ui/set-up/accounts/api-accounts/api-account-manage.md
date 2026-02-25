---
title: （新UI）管理广告网络帐户
description: 了解如何在新UI中为通过广告网络API同步的广告网络设置和管理帐户详细信息。
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '2129'
ht-degree: 0%

---

# （新用户界面）通过API连接管理广告网络帐户

<!-- Besides just logging into an account, do you have to make any other choices once you're logged in (such as to give speciic permissions to SSC?  And what about oAuth tokens -- do we still use them? -->

*Beta功能*

<!-- Move out info about Naver into a separate page -->

以下是有关使用广告网络的API管理Search、Social和Commerce同步的广告网络帐户的说明。

<!-- Move out info about Naver into a separate page -->

有关每个广告网络可用功能的详细信息，请参阅[支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)。

## 创建广告网络帐户详细信息 {#create-account}

要启用帐户同步，您必须创建相应的帐户记录，该记录包含帐户访问凭据和跟踪选项，且状态为&#x200B;*已启用*。

>[!NOTE]
>
>要在广告网络上创建实际的帐户，请转到广告网络的网站。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 单击&#x200B;**[!UICONTROL Create Account]**。

1. 单击广告网络的名称，然后单击&#x200B;**[!UICONTROL Next]**。

1. （除[!DNL Yandex]之外的所有广告网络）使用广告商的凭据登录到广告网络。 选择“此帐户的帐户跟踪”选项。 然后，在右上角单击&#x200B;**[!UICONTROL Next]**。

1. 指定[帐户设置](#account-settings-api)：

   1. 在&#x200B;**[!UICONTROL Select Accounts]**&#x200B;选项卡上，指定常规帐户设置。 对于[!DNL Yandex]帐户，请指定帐户凭据。

   1. 单击&#x200B;**[!UICONTROL Setup Tracking]**&#x200B;选项卡，然后输入跟踪设置。

   1. （具有[[!DNL Adobe Analytics for Advertising] 集成](/help/integrations/analytics/overview.md)的广告商）单击“**[!UICONTROL Set up Adobe Analytics]**”选项卡，然后选择要用于跟踪和报告促销活动的所有[!DNL Analytics]报告包。

1. 单击&#x200B;**[!UICONTROL Save]**。

   帐户中所有促销活动的最近成本和点击数据在每小时Search、Social和Commerce中更新。 默认情况下，数据在最近5-10天内均可用，具体取决于广告网络。 但是，如有必要，项目启动团队可以检索过去60天的数据。

## 编辑广告网络帐户详细信息 {#edit-account}

要重新验证帐户设置以刷新连接或更新权限，请启用或禁用帐户上的活动，更改帐户上的默认跟踪参数，或更改[!DNL Analytics]报表包以用于跟踪和报告，然后编辑帐户详细信息。

>[!NOTE]
>
>要编辑广告网络上的实际帐户，请转到广告网络的网站。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 通过以下任一方式选择帐户：

   * 选中帐户名称旁边的复选框，然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Edit]**。

   * 将光标放在帐户名称上，单击&#x200B;**...**，然后单击&#x200B;**[!UICONTROL Edit]**。

1. 编辑[帐户设置](#account-settings-api)：

   1. （可选）在&#x200B;**[!UICONTROL Account Details]**&#x200B;选项卡上，编辑帐户详细信息。

   1. （可选）单击&#x200B;**[!UICONTROL Setup Tracking]**&#x200B;选项卡，然后编辑跟踪设置。

   1. （可选；具有[[!DNL Adobe Analytics for Advertising] 集成](/help/integrations/analytics/overview.md)的广告商）单击&#x200B;**[!UICONTROL Set up Adobe Analytics]**&#x200B;选项卡，然后编辑要用于跟踪和报告促销活动活动的[!DNL Analytics]报告包。

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. 单击&#x200B;**[!UICONTROL Save]**。

   >[!NOTE]
   >
   >搜索、社交和Commerce必须将新帐户数据与广告网络上的帐户数据同步。 此事件每天自动发生一次，或者在Search、Social和Commerce检测到广告网络上的更改时更频繁。

## 重新验证广告网络帐户 {#reauthenticate}

要刷新广告网络连接或更新帐户的权限，请重新验证帐户。

1. （如果您在同一浏览器应用程序中登录到同一广告网络的其他帐户）注销除广告商帐户之外的任何其他帐户。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

<!-- For Bing and Yandex, the right-click menu includes "Re authenticate." Clarify why just those types -->

1. 通过以下任一方式选择帐户：

   * 选中帐户名称旁边的复选框，然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Edit]**。

   * 将光标放在帐户名称上，单击&#x200B;**...**，然后单击&#x200B;**[!UICONTROL Edit]**。

1. 在&#x200B;**[!UICONTROL Account Details]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Re authenticate]**&#x200B;并使用广告商的凭据登录到广告网络。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 启用或禁用广告网络帐户 {#enable-disable-account}

当您启用广告网络帐户时，Search、Social和Commerce会将促销活动数据与帐户同步（如果支持），并为项目组合中的促销活动推送自动竞价和/或促销活动预算。 禁用广告网络帐户后，搜索、社交和Commerce将停止该帐户上的所有活动。 虽然仍会存储当帐户处于活动状态时收集的数据，但营销活动管理视图和报表并不包含禁用帐户时段的数据。 您稍后可以重新启用帐户以继续使用该帐户的活动。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 执行以下任一操作：

   * （从[!UICONTROL Accounts]视图）：

      * （要启用帐户）选中帐户名称旁边的复选框，然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Activate]**。

      * （要禁用帐户）选中帐户名称旁边的复选框，然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Pause]**。

   * （从帐户设置）：

      1. 通过以下任一方式选择帐户：

         * 将光标放在帐户名称上，单击&#x200B;**...**，然后单击&#x200B;**[!UICONTROL Edit]**。

         * 选中帐户名称旁边的复选框，然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Edit]**。

      1. 在&#x200B;**[!UICONTROL Account Details]**&#x200B;选项卡上，关闭&#x200B;**[!UICONTROL Account enabled]**。

      1. 单击&#x200B;**[!UICONTROL Save]**。

## 广告网络帐户设置 {#account-settings-api}

帐户设置因广告网络而异。 您可能看不到以下所有设置。

<!-- When you're creating new accounts only; not sure that you'll have anything to do here once you've authenticated

### Authenticate tab

-->

### [!UICONTROL Select Accounts]/[!UICONTROL Account Details]选项卡

**[!UICONTROL Account Name]：**&#x200B;要在Search、Social和Commerce中为帐户显示的名称。

>[!NOTE]
>
>如果您集成了“搜索”、“Social”和“Commerce-Adobe Analytics”，并更改了搜索帐户的名称，请让您的Adobe帐户团队更新映射。

**[!DNL [广告网络]帐户]：** （在创建帐户时可见）要同步的广告网络帐户。

**[登录详细信息]：** （仅限Yandex帐户）要使用的帐户凭据：

* **[!UICONTROL Login]：**&#x200B;启用帐户API访问的登录名或ID。

* **[!UICONTROL Password]：**&#x200B;帐户的密码。

* **[!UICONTROL Access Key]：**&#x200B;要使用的开发人员帐户的访问密钥。

* **[!UICONTROL Application ID]：**&#x200B;要用于帐户的开发人员令牌。 所有[!DNL Yandex]帐户都使用相同的令牌。

* **[!UICONTROL Purse Campaign ID]：** （[!DNL Yandex]个帐户的“共享帐户”设置仅被禁用；可选）用于支付帐户中所有广告促销活动的促销活动的数字ID。

* **[!UICONTROL Finance Token]：** （[!DNL Yandex]个帐户的“共享帐户”设置仅被禁用；可选）用于财务相关API调用的开发人员令牌，如在广告商的促销活动之间重新分配钱包中的款项，这是组合优化所必需的。

**[!UICONTROL Network Account ID]：** (除[!DNL Yandex]外的所有广告网络由广告网络分配的帐户ID。

>[!NOTE]
>
>此处不支持广告网络管理器帐户。 要为[!DNL Microsoft Advertising]标识经理帐户，请分别使用主帐户ID或MCC帐户字段。 要[设置 [!DNL Google Ads] 经理帐户](/help/search-social-commerce/admin/manager-accounts.md)的凭据，请转到[!UICONTROL Admin] \> [!UICONTROL Manager Accounts]。

**[!UICONTROL Currency]：** （只读）帐户使用的货币的缩写。 保存记录后，此值将自动填充为广告网络上的帐户配置的货币。

**[!UICONTROL Time Zone]：**&#x200B;广告商的时区。 保存记录后，此值将自动填充为广告商的Search、Social和Commerce帐户配置的时区。

**[!UICONTROL Login]：** （只读）用于登录帐户的用户帐户。

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]：**&#x200B;搜索、社交和Commerce将营销活动数据与帐户同步（如果支持），并针对项目组合中的营销活动推送自动竞价和/或营销活动预算。

## [!UICONTROL Setup Tracking]选项卡

<!-- This should be the name of the whole left side of options -- they're all enabled/disabled depending on whether you enable our tracking -->

**[!UICONTROL Search, Social, & Commerce Tracking]：**&#x200B;是否使用Adobe Advertising转换跟踪服务启用跟踪。 此方法会生成唯一的点击跟踪ID，并将用户重定向到Adobe Advertising服务器进行跟踪，然后再将其发送到客户端的登陆页面。 此方法具有默认跟踪选项，您可以选择对这些选项进行自定义，还可以指定要附加到每个URL的参数。

要启用此功能，请打开&#x200B;**[启用跟踪]**。

>[!NOTE]
>
>* 如果更改此设置，则必须为帐户重新生成跟踪URL。
>* 营销活动级别的跟踪选项会覆盖帐户级别的设置。

**[!UICONTROL Tracking Type]：** (启用搜索、社交和Commerce跟踪时)将最终用户重定向到最终URL或目标URL的方法。 所选选项适用于帐户或营销活动中的所有竞价单位。 默认帐户级别设置继承自广告商的跟踪设置，默认营销活动级别设置继承自帐户设置。

* *[!UICONTROL Standard]：*&#x200B;仅将最终用户重定向到指定的URL。

* *[!UICONTROL Token]：*&#x200B;要将最终用户重定向到URL，并将点击(`ef_id`)的Search、Social和Commerce ID记录为查询字符串参数，该参数用作令牌。 如果要报告离线交易，希望Search、Social和Commerce与Adobe Analytics交换数据，或者希望跟踪[!DNL Apple Safari]浏览器内发生的所有转化，请选择此选项。

>[!NOTE]
>
>* 如果您从[!UICONTROL Standard]切换到[!UICONTROL Token]，或者反之，则必须重新生成帐户的跟踪URL。
>* 您可以在营销策划级别覆盖帐户级别设置。

**[!UICONTROL Auto Update]：** (启用搜索、社交和Commerce跟踪时)标准化您的跟踪URL以实现跨浏览器和服务器的兼容性。 Search、Social和Commerce会在下次同步期间自动将以下内容上传到广告网络：(a)用于跟踪模板的搜索、Social和Commerce跟踪参数以及附加到最终URL的相同参数，或者(b)嵌入了Search、Social和Commerce跟踪代码的新目标URL。 对于具有[Adobe Advertising-Adobe Analytics集成](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)和服务器端AMO ID (s_kwcid)配置的广告商，该上传还包括您的[和](/help/integrations/analytics/ids.md#amo-id)帐户的[!DNL Google Ads]AMO ID参数[!DNL Microsoft Advertising]。 默认帐户级别设置继承自广告商的跟踪设置。 您可以在营销策划级别覆盖帐户级别设置。

跟踪URL每天只更新不同步的实体（即添加的新实体和属性已更改的现有实体）。 因此，如果您将现有广告商/帐户/营销活动的此设置从“禁用”更改为“启用”，则不会为已同步的现有实体更新跟踪URL。 要将跟踪添加到现有已同步实体的URL，请联系您的Adobe客户团队，并请求执行一次性的手动同步过程。 自动上传流程将处理未来的更改。

**[!UICONTROL URL Encoding]：** (启用搜索、社交和Commerce跟踪时；帐户仅具有目标URL)对最终用户浏览器地址栏中的基本URL进行编码（如`%3D`而不是`=`）：

**[!UICONTROL Tracking Level]：** (启用搜索、社交和Commerce跟踪时；适用于帐户和营销活动级别；不适用于启用并行跟踪的广告网络)应通过添加重定向（在相关时）并将参数附加到相关URL来跟踪点击次数和收入的级别：

* *[!UICONTROL Keyword]：*&#x200B;只跟踪关键字级别的数据。 对[!DNL Yandex]不可用。

* *[!UICONTROL Ad]：*&#x200B;仅跟踪广告级别的数据。 对[!DNL Naver]不可用。

* *[!UICONTROL Keyword and Ad]：*&#x200B;在关键词和广告级别跟踪数据。 对[!DNL Naver]和[!DNL Yandex]不可用。

**[!UICONTROL Landing Page Suffix]** （仅限[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户；可选）要附加到最终URL末尾以跟踪信息的所有参数；包括您的企业必须跟踪的所有参数。

示例： `param1=value1&param2=value2`

使用Adobe Advertising点击跟踪的帐户必须在后缀中包含广告网络的点击标识符(`msclkid`为[!DNL Microsoft Advertising]；Google为`gclid`)。 具有Adobe Analytics集成的帐户必须使用AMO ID参数（以`s_kwcid`开头）。 如果该帐户具有服务器端AMO ID实施，则当用户单击广告时，参数会自动添加；否则，您必须在此处手动添加该参数。 查看[的 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)必需后缀格式和[的 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)必需后缀格式。

>[!NOTE]
>
>* [!UICONTROL Auto Update]跟踪设置未更新此字段。
>* 较低级别的最终URL后缀将覆盖帐户级别的后缀。 为便于维护，除非需要对各个帐户组件进行不同的跟踪，否则请仅使用帐户级别的后缀。 要在广告组级别或更低级别配置后缀，请使用广告网络的编辑器。

**帐户跟踪URL**： （仅限[!DNL Google Ads]、[!DNL Microsoft Advertising]和[!DNL Yahoo! Japan Ads]帐户；可选）帐户的默认跟踪模板，它指定所有登入域外部重定向和跟踪参数，并将最终/登陆页面URL嵌入到参数中。 示例： `{lpurl}?source={network}&id=5`或`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`以包含重定向。

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

## [!UICONTROL Setup Analytics]选项卡

**[!UICONTROL Adobe Analytics Report Suite]：** （具有[[!DNL Adobe Analytics for Advertising] 集成](/help/integrations/analytics/overview.md)的广告商；可选）一个或多个Analytics报表包，Search、Social和Commerce会向其发送从广告网络收集的数据，包括帐户实体分类和点击数据。 此功能仅适用于受支持的广告网络。

对于要显示在报表包中的数据，必须(a)为帐户配置服务器端AMO ID功能，或者(b)启用设置为“[!UICONTROL Enable Advertising reporting in Analytics]”的广告商级别设置。 此外，必须将广告商的[!DNL Analytics]帐户配置为从Search、Social和Commerce接收数据。 有关更多信息，请与您的Adobe客户团队联系。

>[!MORELIKETHIS]
>
>* [关于广告网络帐户](../ad-network-account-about.md)
>* [管理商家中心帐户](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
>* [更新 [!DNL Google Ads] 帐户的s_kwcid跟踪代码](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)
