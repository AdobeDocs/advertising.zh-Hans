---
title: 管理广告网络帐户
description: 了解如何设置和管理广告网络帐户的帐户详细信息。
exl-id: 4038d03b-63e2-4953-89df-37f7b5f68652
feature: Search Campaign Management
source-git-commit: c2a1ce841a9dc99c57239f817dbd2065b91cdfb9
workflow-type: tm+mt
source-wordcount: '2082'
ht-degree: 0%

---

# 管理广告网络帐户

以下是有关创建和编辑广告网络帐户详细信息、刷新 [!DNL oAuth] 帐户的令牌，并禁用帐户。

有关每个广告网络可用功能的详细信息，请参阅&quot;[支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)“

## 创建广告网络帐户详细信息 {#create-account}

*仅限代理客户经理、Adobe客户经理和管理员用户角色*

要启用帐户的同步或跟踪，您必须创建相应的帐户记录，记录中包含帐户访问凭据和跟踪选项以及状态 *活动*.

>[!NOTE]
>
>* 新版本不支持此功能 [!DNL Baidu] 帐户。
>* 要在广告网络上创建实际的帐户，请转到广告网络的网站。

1. 在主菜单中，单击 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. 在数据表上方的工具栏中，单击 ![创建](/help/search-social-commerce/assets/add.png "创建").

1. 指定 [帐户设置](#account-settings)：

   1. 单击广告网络的名称，然后单击 **[!UICONTROL Next]**.

   1. 在 **[!UICONTROL Account Details]** 部分，输入帐户详细信息。

      对于使用登录授权类型&#39;&#39;的广告网络[!UICONTROL oAuth]，”允许搜索、社交和商务使用访问帐户 [OAuth授权协议](https://oauth.net/2/)：

      1. 输入 **[!UICONTROL Login]** 帐户的值，也可以输入密码，然后单击 **[!UICONTROL Authenticate]**.

         最佳实践是使用登录来获取对帐户的API访问权限。 在要加密并保存密码时输入密码，以便Adobe帐户团队可以根据需要刷新令牌。

      1. （如果您未登录到广告商的帐户）请登录到广告商的广告帐户。 最佳实践是使用凭据来API访问帐户。

      1. 在“请求权限/访问权限”屏幕中，单击按钮确认权限。

      1. 在打开的弹出窗口中复制身份验证字符串，并将该字符串粘贴到 **[!UICONTROL oAuth Token]** 字段。

      1. 指定剩余帐户详细信息。

   1. 单击 **[!UICONTROL Set Account Tracking]**，并输入跟踪设置。

1. 单击 **[!UICONTROL Post]**.

   在大约24小时内，可在Search、Social和Commerce中找到帐户中所有营销活动的最新成本和点击数据。 默认情况下，数据在最近5-10天内均可用，具体取决于广告网络。 但是，如有必要，项目启动团队可以检索过去60天的数据。

## 编辑广告网络帐户详细信息 {#edit-account}

*仅限代理客户经理、Adobe客户经理和管理员用户角色*

如果帐户凭据发生更改，您想要跨帐户更改默认跟踪参数，或者想要启用或禁用帐户的活动，然后编辑帐户详细信息。

>[!NOTE]
>
>要编辑广告网络上的实际帐户，请转到广告网络的网站。

1. 在主菜单中，单击 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. 将光标悬停在帐户名称上，单击 ![更多](/help/search-social-commerce/assets/more-filters.png "更多")，然后选择 **[!UICONTROL Edit]**.

1. 编辑 [帐户设置](#account-settings)：

   1. （可选）编辑帐户详细信息。

   1. （可选）单击 **[!UICONTROL Set Account Tracking]**，并编辑跟踪设置。

1. 单击 **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >搜索、社交和商务必须将新帐户数据与广告网络上的帐户数据同步。 这种情况每天自动发生一次，或者在Search、Social和Commerce检测到广告网络上的更改时更加频繁。

## 刷新搜索帐户的oAuth访问令牌 {#refresh-oauth-tokens}

*仅限代理客户经理、Adobe客户经理和管理员用户角色*

如果搜索、社交和商业部门使用访问帐户， [OAuth授权协议](https://oauth.net/2/) 并且帐户凭据发生更改，或者需要其他访问权限才能支持Search、Social和Commerce中的新功能，则必须获取帐户的新访问令牌。

如果您的新功能需要新令牌，您的Adobe客户团队将通知您。

1. （如果您在同一浏览器应用程序中登录到同一广告网络的其他帐户）注销除广告商帐户之外的任何其他帐户。

1. 在主菜单中，单击 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. 将光标悬停在帐户名称上，单击 ![更多](/help/search-social-commerce/assets/more-filters.png "更多")，然后选择 **[!UICONTROL Edit]**.

1. 获取新的访问令牌：

   1. 单击 **[!UICONTROL Get oAuth Token]**.

   1. （如果您未登录到广告商的帐户）请登录到广告商的广告帐户。 最佳实践是使用凭据来API访问帐户。

   1. 在“请求权限/访问权限”屏幕中，单击按钮确认权限。

   1. 在打开的弹出窗口中复制身份验证字符串，并将该字符串粘贴到 **[!UICONTROL oAuth Token]** 字段。

1. 单击 **[!UICONTROL Post]**.

## 启用或禁用广告网络帐户 {#enable-disable-account}

*仅限代理客户经理、Adobe客户经理和管理员用户角色*

当您启用广告网络帐户时，Search、Social和Commerce会将促销活动数据与帐户同步（如果支持），并为项目组合中的促销活动推送自动竞价和/或促销活动预算。当您禁用广告网络帐户时，Search、Social和Commerce将停止该帐户上的所有活动。 虽然仍会存储当帐户处于活动状态时收集的数据，但营销活动管理视图和报表并不包含禁用帐户时段的数据。 您稍后可以重新启用帐户以继续使用该帐户的活动。

1. 在主菜单中，单击 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. 执行以下任一操作：

   * （要更改单个帐户的状态）将光标悬停在帐户名称上，单击 ![更多](/help/search-social-commerce/assets/more-filters.png "更多")，然后选择 **[!UICONTROL Edit]**. 更改 **[!UICONTROL Status]** 到 *已启用* 或 *已禁用*，然后单击 **[!UICONTROL Post]**.

   * （要更改一个或多个帐户的状态），请执行以下操作：

      1. 选中每个帐户旁边的复选框。

         有关选择多行的提示，请参阅&quot;[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)“

      1. 在数据表上方的工具栏中，单击 ![“激活”图标](/help/search-social-commerce/assets/activate.png "“激活”图标") 启用帐户或 ![“禁用”图标](/help/search-social-commerce/assets/disable.png "“禁用”图标") 以禁用帐户。

## 广告网络帐户设置 {#account-settings}

>[!NOTE]
>
>只有代理客户经理， [!DNL Adobe] 帐户管理员和管理员用户可以配置帐户设置。

### 帐户详细信息

**[!UICONTROL SE Account ID]：** (除以下帐户外的所有帐户： [!DNL Naver] 和 [!DNL Yandex] 帐户；仅对新帐户可编辑)广告网络分配的帐户ID。

>[!NOTE]
>
>此处不支持广告网络管理器帐户。 为确定经理帐户 [!DNL Microsoft Advertising] 或 [!DNL Yandex]，分别使用主帐户ID或MCC帐户字段。 至 [设置凭据 [!DNL Google Ads] 经理帐户](/help/search-social-commerce/admin/manager-accounts.md)，转到 [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]：** 要在Search、Social和Commerce中为帐户显示的名称。

>[!NOTE]
>
>如果您集成了Search、Social和Commerce-Adobe Analytics，并更改了搜索帐户的名称，请通知您的Adobe帐户团队，以便他们能够更新映射。

**[!UICONTROL Login Details]： \[登录类型\]** - ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] 仅限于)是否授权通过以下方式登录帐户：

* *[!UICONTROL oAuth]* （默认）：使用 [[!DNL OAuth] 授权协议](https://oauth.net/2/).

* *[!UICONTROL Password]：* 使用客户端的密码。

对象 [!DNL Microsoft Advertising] 帐户，仅限 [!DNL oAuth]-authorized logins可以使用。

**[!UICONTROL Login Details]： [!UICONTROL Login]：** (所有广告网络，除 [!DNL Naver])登录名或ID以启用对帐户的API访问。

**[!UICONTROL Login Details]： [!UICONTROL OAuth Token]：** ([!DNL Microsoft Advertising] [!DNL oAuth]-enabled以及除以下网络之外的所有其他网络 [!DNL Meta] 和 [!DNL Yandex])帐户的令牌，用于授权使用 [[!DNL OAuth] 授权协议](https://oauth.net/2/).

**[!UICONTROL Login Details]： [!UICONTROL Password]：** (所有广告网络，除 [!DNL Naver])帐户的密码。 对于上的启用密码的帐户 [!DNL Microsoft Advertising]， [!DNL Yahoo! Japan Ads]、和 [!DNL Yandex]，此字段为必填字段。 对象 [!DNL oAuth]-enabled accounts，此字段为可选字段；当要加密并保存密码以便帐户管理员根据需要刷新令牌时，请使用该字段。

**[!UICONTROL Login Details]： [!UICONTROL Access Key]：** ([!DNL Yandex] 仅限帐户)要使用的开发人员帐户的访问密钥。

**[!UICONTROL Currency]：** 用于帐户的货币的缩写。 此字段对于新字段可编辑 [!DNL Naver] 帐户。 对于所有其他搜索网络，保存记录后，该值将自动填充为广告网络上的帐户配置的货币。

**[!UICONTROL Landing Page Suffix]** ([!DNL Google Ads] 和 [!DNL Microsoft Advertising] 仅限帐户；可选)附加到最终URL末尾的任何参数以跟踪信息；包括您的企业必须跟踪的所有参数。

示例： `param1=value1&param2=value2`

使用Adobe Advertising点击跟踪的帐户必须包含广告网络的点击标识符(`msclkid` 对象 [!DNL Microsoft Advertising]； `gclid` (对于Google)。 具有Adobe Analytics集成的帐户必须使用AMO ID参数(以 `s_kwcid`)。 如果该帐户具有服务器端AMO ID实施，则当用户单击广告时，参数会自动添加；否则，您必须在此处手动添加该参数。 请参阅 [所需的后缀格式 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) 和 [所需的后缀格式 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* 此字段未由更新 [!UICONTROL Auto Upload] 跟踪设置。
>* 较低级别的最终URL后缀将覆盖帐户级别的后缀。 为便于维护，除非需要对各个帐户组件进行不同的跟踪，否则请仅使用帐户级别的后缀。 要在广告组级别或更低级别配置后缀，请使用广告网络的编辑器。

**时区：** (除以下项之外的所有广告网络 [!DNL Baidu] 和 [!DNL Yahoo! Display Network])广告商的时区。 此字段可编辑，对于新字段为可选 [!DNL Naver] 帐户。 对于所有其他搜索网络，保存记录后，该值将自动填充为广告商的搜索、社交和商务帐户配置的时区。

**状态：** 搜索、社交和商务中的帐户状态：

* *已启用：* 搜索、Social和Commerce可将营销活动数据与帐户同步（如果支持），并针对项目组合中的营销活动推送自动竞价和/或营销活动预算。
* *已禁用：* 搜索、社交和商务会停止帐户上的所有活动。 虽然会存储当帐户处于活动状态时收集的数据，但营销活动管理视图和报表并不包含与帐户暂停时间相关的数据。 您稍后可以重新激活帐户以继续使用该帐户的活动。

**跟踪模板** - ([!DNL Google Ads]， [!DNL Microsoft Advertising]、和 [!DNL Yahoo! Japan Ads] 仅限帐户；可选)帐户的默认跟踪模板，它指定所有登陆域重定向和跟踪参数，并将最终页面/登陆页面URL嵌入到参数中。 示例： `{lpurl}?source={network}&id=5` 或 `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` 以包含重定向。

* 嵌入最终URL：

   * ([!DNL Google Ads] 和 [!DNL Microsoft Advertising] （仅限）有关用于指示跟踪模板中最终URL的参数列表，请参阅([!DNL Microsoft Advertising] 仅限) [[!DNL Microsoft Advertising] 文档](https://help.ads.microsoft.com/#apex/3/en/56799) 或([!DNL Google Ads] 仅限)“可用”部分中的“仅限跟踪模板”参数 [!DNL ValueTrack] 参数” [[!DNL Google Ads] 文档](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] 仅限)使用参数 `!{lpurl}` 以指示登陆页面URL。

* 您可以选择包含URL参数以及为促销活动定义的任何自定义参数，这些参数之间以&amp;号分隔，例如 `{lpurl}?matchtype={matchtype}&device={device}`.

* 您可以选择添加第三方重定向和跟踪。

* 当营销活动设置包括&quot;[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]，”在保存记录时，Search、Social和Commerce会自动为自己的重定向和跟踪代码添加前缀。

>[!NOTE]
>
>* 对象 [!DNL Google Ads]，请避免使用宏，这些宏不会替代来自启用并行跟踪的源的点击。 如果广告商必须使用宏，则Adobe客户团队应与客户支持或实施团队合作来添加宏。
>* 最细粒度级别的跟踪模板将覆盖所有更高级别的值。 例如，如果帐户设置和关键字设置都包含一个值，则应用关键字值。
>* 如果您在广告、站点链接或关键词级别更新跟踪模板，则会重新提交相关广告以供审阅。 您可以在帐户、营销活动或广告组级别更新跟踪模板，而无需重新提交广告以供审批。

**[!UICONTROL Master Account ID]：** ([!DNL Microsoft Advertising] 仅限帐户)与帐户关联的代理/管理帐户的ID。

**[!UICONTROL MCC Account]：** ([!DNL Yandex] 仅限帐户；可选)与帐户关联的代理/管理帐户。 要删除现有关联，请选择“[!UICONTROL No MCC Account]“

**[!UICONTROL Application ID]：** ([!DNL Yandex] 仅限帐户)用于帐户的开发人员令牌。 相同的令牌适用于所有 [!DNL Yandex] 帐户。

**[!UICONTROL Purse Campaign ID]：** ([!DNL Yandex] 仅禁用共享帐户设置的帐户；可选)将用于支付帐户中所有广告促销活动的促销活动数字ID。

**[!UICONTROL Finance Token]：** ([!DNL Yandex] 仅禁用共享帐户设置的帐户；可选)用于财务相关API调用的开发人员令牌，如在广告商的促销活动之间重新分配钱包，这是组合优化所必需的。

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

**[!UICONTROL Track Product Group]：** (用于 [!UICONTROL EF Redirect] 仅)未实现

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **S_kwcid格式** -(现有 [!DNL Google Ads] 帐户，适用于具有Adobe Advertising-Adobe Analytics集成且尚未为其迁移AMO ID (s_kwcid)的广告商

此帐户使用旧版的AMO ID跟踪代码格式，允许Adobe Advertising与Adobe Analytics共享该帐户的相关数据。 此 [最新格式](/help/integrations/analytics/ids.md#amo-id-formats) 包含营销活动ID和广告组ID的参数，要准确报告营销活动和广告组级别的 [!DNL Google Ads] Analytics中的效果最佳营销活动以及草稿和实验营销活动：

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

如果此帐户需要在营销活动和广告组级别报告，请单击 [!UICONTROL Edit] （铅笔）图标，然后 **[!UICONTROL Migrate to new s_kwcid format]** 以更改为新格式。 对于不包含这些促销活动类型的帐户，迁移到新格式是可选的，但建议这样做。

有关完整说明，请参阅&quot;[更新的AMO ID跟踪代码 [!DNL Google Ads] 帐户](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)“

**报表包名称** -(仅适用于带令牌的EF重定向；带有Adobe Advertising-Adobe Analytics集成的广告商；可选)一个或多个Analytics报表包，Search、Social和Commerce会向其发送从广告网络收集的数据，包括实体分类和帐户的点击数据。 此功能仅适用于受支持的广告网络。

对于要在报表包中显示的数据，必须(a)为帐户配置服务器端AMO ID功能，或者(b)将广告商级别设置为&quot;[!UICONTROL Enable tracking for SAINT feeds]必须启用&#39;&#39;。 此外，广告商的Analytics帐户必须配置为从Search、Social和Commerce接收数据。 有关更多信息，请与您的Adobe客户经理联系。

>[!MORELIKETHIS]
>
>* [关于广告网络帐户](ad-network-account-about.md)
>* [管理商户中心帐户](merchant-account-manage.md)
>* [更新的s_kwcid跟踪代码 [!DNL Google Ads] 帐户](update-amo-id-google.md)
