---
title: （新UI）管理广告网络帐户
description: 了解如何在新UI中为通过广告网络API同步的广告网络设置和管理帐户详细信息。
feature: Search Campaign Management
exl-id: a50b2943-7568-401c-be5b-ff6f62629488
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
source-git-commit: b568da9300e9adb8d189811c3c8b52516dfcef6f
workflow-type: tm+mt
source-wordcount: '3141'
ht-degree: 0%
---
# （新用户界面）通过API连接管理广告网络帐户

这些说明说明了如何通过API管理搜索、社交和Commerce同步的广告网络帐户，包括身份验证、连接刷新和状态检查。

要创建、编辑或重新验证帐户，您必须具有编辑帐户的权限。

有关每个广告网络可用功能的详细信息，请参阅[支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)。

## 关于[!UICONTROL Accounts]视图 {#account-view-about}

[!UICONTROL Manage] > [!UICONTROL Accounts]视图在筛选视图中列出了选定广告商帐户的所有广告网络帐户。 单击帐户名称以打开为该帐户筛选的[!UICONTROL Campaigns]视图。

### 帐户身份验证和访问状态 {#authentication-status}

身份验证和访问详细信息因广告网络和帐户可用的信息而异。 已启用或已成功验证的帐户可能仍缺少权限。

以下列显示帐户状态、身份验证和访问详细信息：

* **[!UICONTROL Status]：**&#x200B;帐户的工作状态，不同于其身份验证和权限。 启用的帐户可以与广告网络同步数据，并使用受支持的帐户管理和优化功能。 禁用帐户可停止Search、Social和Commerce中的活动。 帐户状态显示为&#x200B;**[!UICONTROL Enabled]**&#x200B;使用绿色指示符，为&#x200B;**[!UICONTROL Disabled]**&#x200B;使用红色指示符，为&#x200B;**[!UICONTROL Pending]**&#x200B;使用琥珀色指示符。 您可从视图或帐户设置[启用或禁用帐户](#enable-disable-account)。

* **[!UICONTROL Authenticated]：**&#x200B;帐户是否已验证：

  * **[!UICONTROL Yes]：**&#x200B;帐户已通过身份验证。

  * **[!UICONTROL No]：**&#x200B;帐户未通过身份验证。 当验证错误可用时，将光标悬停在红色警告图标上可查看错误。

  * **[!UICONTROL Not Applicable]：**&#x200B;身份验证不适用，因为您上载了帐户的数据，而不是通过API连接。

  * **[!UICONTROL Expiring in N days]**、**[!UICONTROL Expiring today]**&#x200B;或&#x200B;**[!UICONTROL Expired]：**&#x200B;当过期信息可用且令牌在14天或更短的时间内过期或已经过期时，令牌过期警告将替换&#x200B;**[!UICONTROL Yes]**。 单击警告图标以查看帐户的访问详细信息并[重新进行身份验证](#reauthenticate)。

* **[!UICONTROL Manager Account for Cross-Account Conversions]：** （仅限[!DNL Google Ads]帐户）用于跨帐户转换上载的关联管理器帐户的ID。 当管理器帐户存在错误时，ID旁边会显示一个警告图标。 要查看错误，请将光标悬停在图标上。 经理帐户的凭据与广告网络帐户的凭据不同。 要添加或刷新经理帐户凭据，请使用&#x200B;**[!UICONTROL Setup]** > **[!UICONTROL Manager Accounts]**。 请参阅&quot;[管理管理器帐户](/help/search-social-commerce/new-ui/set-up/manager-account-manage.md)&quot;。

* **[!UICONTROL Access Level]：**&#x200B;报告的帐户访问级别，如&#x200B;**[!UICONTROL Full]**、**[!UICONTROL Limited]**&#x200B;或&#x200B;**[!UICONTROL None]**，或者&#x200B;**[!UICONTROL Not Applicable]**（无访问级别值可用时）。

  缺少权限时，单击警告图标可查看帐户的访问详细信息。 **[!UICONTROL Access]**&#x200B;部分将权限列为&#x200B;**[!UICONTROL Granted]**&#x200B;或&#x200B;**[!UICONTROL Missing]**。 当影响详细信息可用时，**[!UICONTROL Not working]**&#x200B;部分将列出受影响的功能。 要[重新验证](#reauthenticate)并更新权限，请单击&#x200B;**[!UICONTROL Update Access]**。

### 可用操作

可用的操作取决于您的权限和帐户类型。

* [创建广告网络帐户详细信息](#create-account)

* [编辑广告网络帐户详细信息](#edit-account)

* [重新验证广告网络帐户](#reauthenticate)

* [启用或禁用广告网络帐户](#enable-disable-account)

* [将帐户数据与广告网络同步](sync-api-accounts.md)

* [在[!UICONTROL Accounts]视图中查看性能图](#account-performance-graph)

* [从[!UICONTROL Accounts]视图管理数据视图报告](#account-reports)

## 创建广告网络帐户详细信息 {#create-account}

要启用帐户同步，您必须创建相应的帐户记录，该记录包含帐户访问凭据和跟踪选项，且状态为&#x200B;*已启用*。

>[!NOTE]
>
>要在广告网络上创建实际的帐户，请转到广告网络的网站。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**。

1. 单击&#x200B;**[!UICONTROL Create Account]**。

1. 单击广告网络的名称以打开帐户设置。

1. （除[!DNL ChatGPT Ads]和[!DNL Yandex]之外的所有广告网络）在&#x200B;**[!UICONTROL Authenticate]**&#x200B;选项卡上，使用广告商的凭据在弹出窗口中完成登录，并授予请求的帐户访问权限。

   设置屏幕会自动更新，并在身份验证成功时显示&#x200B;**[!UICONTROL Authentication Successful]**。 如果需要重新打开登录窗口，请单击&#x200B;**[!UICONTROL Open login again]**。 如果浏览器阻止窗口，请编辑浏览器设置以允许站点的弹出窗口。

   对于[!DNL Meta Ads]，警告标识任何缺少的权限及其影响。 成功的身份验证不一定意味着所有请求的权限都被授予。

   单击&#x200B;**[!UICONTROL Next]**&#x200B;继续。

1. 在每个可用选项卡上指定[帐户设置](#account-settings-api)。 对于在弹出窗口中进行身份验证的帐户，请在&#x200B;**[!UICONTROL Select Accounts]**&#x200B;选项卡上选择要从&#x200B;**[!UICONTROL Linked Ad Accounts]**&#x200B;同步的帐户。

1. 单击&#x200B;**[!UICONTROL Save]**。

   帐户中所有促销活动的最近成本和点击数据在每小时Search、Social和Commerce中更新。 默认情况下，数据在最近5-10天内均可用，具体取决于广告网络。 但是，如有必要，项目启动团队可以检索过去60天的数据。

## 编辑广告网络帐户详细信息 {#edit-account}

要启用或禁用帐户上的活动，请更改帐户中的默认跟踪参数，或更改用于跟踪和报告的[!DNL Analytics]报表包，编辑帐户详细信息。 若要刷新连接或更新权限，您可以从帐户设置或[!UICONTROL Accounts]视图[重新验证帐户](#reauthenticate)。

>[!NOTE]
>
>要编辑广告网络上的实际帐户，请转到广告网络的网站。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**。

1. 通过以下任一方式选择帐户：

   * 选中帐户名称旁边的复选框，然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Edit]**。

   * 将光标放在帐户名称上，单击&#x200B;**...**，然后单击&#x200B;**[!UICONTROL Edit]**。

1. 编辑可用选项卡上的[帐户设置](#account-settings-api)。

1. 单击&#x200B;**[!UICONTROL Save]**。

   >[!NOTE]
   >
   >搜索、社交和Commerce必须将新帐户数据与广告网络上的帐户数据同步。 此事件每天自动发生一次，或者在Search、Social和Commerce检测到广告网络上的更改时更频繁。

## 重新验证广告网络帐户 {#reauthenticate}

*对于使用弹出身份验证的帐户；不适用于[!DNL ChatGPT Ads]或[!DNL Yandex]帐户*

要刷新广告网络连接或更新帐户的权限，请重新验证帐户。

1. （如果您在同一浏览器应用程序中登录到同一广告网络的其他帐户）注销除广告商帐户之外的任何其他帐户。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**。

1. 通过以下方式之一打开身份验证：

   * （当帐户的&#x200B;**[!UICONTROL Authenticated]**&#x200B;值为&#x200B;**[!UICONTROL No]**&#x200B;时）将光标悬停在帐户名称上，单击&#x200B;**...**，然后单击&#x200B;**[!UICONTROL Re authenticate]**（可用时）。

   * （显示令牌过期警告时）单击&#x200B;**[!UICONTROL Authenticated]**&#x200B;列中的警告图标，然后单击&#x200B;**[!UICONTROL Reauthenticate]**。

   * （缺少权限时）单击&#x200B;**[!UICONTROL Access Level]**&#x200B;列中的警告图标，然后单击&#x200B;**[!UICONTROL Update Access]**。

   * （从帐户设置中）选中帐户名称旁边的复选框，然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Edit]**，或将光标悬停在帐户名称上，单击&#x200B;**...**，然后单击&#x200B;**[!UICONTROL Edit]**。 在&#x200B;**[!UICONTROL Account Details]**&#x200B;选项卡的&#x200B;**[!UICONTROL Account Authentication]**&#x200B;中，单击&#x200B;**[!UICONTROL Re authenticate]**。

1. 使用广告商的凭据在弹出窗口中完成登录，并授予请求的帐户访问权限。

   当重新身份验证成功时，将自动保存新的访问令牌。 如果您还更改其他帐户设置，请单击&#x200B;**[!UICONTROL Save]**&#x200B;保存这些更改。

   对于[!DNL Meta Ads]，有一条信息消息标识在成功重新身份验证后仍然缺少的任何权限。 要识别受影响的功能，请查看[访问详细信息](#authentication-status)。

## 启用或禁用广告网络帐户 {#enable-disable-account}

当您启用广告网络帐户时，Search、Social和Commerce会将促销活动数据与帐户同步（如果支持），并为项目组合中的促销活动推送自动竞价和/或促销活动预算。 禁用广告网络帐户后，搜索、社交和Commerce将停止该帐户上的所有活动。 虽然仍会存储当帐户处于活动状态时收集的数据，但营销活动管理视图和报表并不包含禁用帐户时段的数据。 您稍后可以重新启用帐户以继续使用该帐户的活动。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**。

1. 执行以下任一操作：

   * （从[!UICONTROL Accounts]视图）：

     * （要启用帐户）选中帐户名称旁边的复选框，然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Enable]**。

     * （要禁用帐户）选中帐户名称旁边的复选框，然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Disable]**。

   * （从帐户设置）：

     1. 通过以下任一方式选择帐户：

        * 将光标放在帐户名称上，单击&#x200B;**...**，然后单击&#x200B;**[!UICONTROL Edit]**。

        * 选中帐户名称旁边的复选框，然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Edit]**。

     1. 在&#x200B;**[!UICONTROL Account Details]**&#x200B;选项卡上，打开&#x200B;**[!UICONTROL Account Enabled]**&#x200B;以启用帐户，或关闭它以禁用帐户。

     1. 单击&#x200B;**[!UICONTROL Save]**。

## 在[!UICONTROL Accounts]视图中查看性能图 {#account-performance-graph}

打开并配置一个性能图，其中包含指定日期范围和货币的过滤视图中的跨帐户总和最多三个量度。

### 查看性能图

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**。

1. 指定日期范围并为要查看其性能的帐户应用任何过滤器。

1. 在数据表的上方，单击![图表](/help/search-social-commerce/assets/charts.png "图表")。

1. （可选）使用&#x200B;**[!UICONTROL Currency]**&#x200B;和&#x200B;**[!UICONTROL Metrics]**&#x200B;指定货币，并指定最多三个量度以包括在图表中。

### 隐藏可见的性能图

* 在数据表的上方，单击![图表](/help/search-social-commerce/assets/charts.png "图表")。

## 从[!UICONTROL Accounts]视图管理数据视图报告 {#account-reports}

生成一份报表，其中包含[!UICONTROL Accounts]视图中一个或多个帐户的数据行，然后以Microsoft Excel工作表文件（XLSX格式）的形式下载该报表。 报表包括视图中指定日期范围内的可见列。

您可以删除已完成的报表和无法生成的报表。

### 生成具有已过滤数据行的报告

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**。

1. 指定日期范围并为要下载的数据应用任何过滤器。

1. 指定要下载其数据的帐户：

   * 要下载特定帐户的数据，请选中帐户旁边的复选框。

   * 要下载过滤视图中所有帐户的数据，请清除所有复选框。

1. 在数据表上方的工具栏中，单击![下载报表](/help/search-social-commerce/assets/download.png "下载报表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]对话框中，保留默认&#x200B;**[!UICONTROL Report Name]**&#x200B;或输入其他名称，然后单击&#x200B;**[!UICONTROL Generate]**。

   报告已添加到&#x200B;**[!UICONTROL Recently Generated]**&#x200B;列表。

1. （可选）要在文件完成后下载文件，请单击文件名旁边的![下载](/help/search-social-commerce/assets/download.png "下载")。

   将按照浏览器的正常过程下载文件。

### 下载已完成的报表

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**。

1. 在数据表上方的工具栏中，单击![下载报表](/help/search-social-commerce/assets/download.png "下载报表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]对话框的&#x200B;**[!UICONTROL Recently Generated]**&#x200B;列表中，单击文件名旁边的![下载](/help/search-social-commerce/assets/download.png "下载")。

   将按照浏览器的正常过程下载文件。

### 删除报告

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**。

1. 在数据表上方的工具栏中，单击![下载报表](/help/search-social-commerce/assets/download.png "下载报表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]对话框的&#x200B;**[!UICONTROL Recently Generated]**&#x200B;列表中，单击已完成报告或无法生成的报告名称旁边的![删除](/help/search-social-commerce/assets/delete-new.png "删除")。

1. 确认删除。

## 广告网络帐户设置 {#account-settings-api}

帐户设置因广告网络而异。 您可能看不到以下所有设置。

### [!UICONTROL Authenticate]选项卡

（在创建使用弹出身份验证的帐户时可见）使用广告商的凭据连接到广告网络。 该选项卡显示连接状态，并包括用于重新打开登录弹出窗口的&#x200B;**[!UICONTROL Open login again]**。

### [!UICONTROL Select Accounts]/[!UICONTROL Account Details]选项卡

**[!UICONTROL Account Name]：**&#x200B;要在Search、Social和Commerce中为帐户显示的名称。

>[!NOTE]
>
>如果您集成了“搜索”、“Social”和“Commerce-Adobe Analytics”，并更改了搜索帐户的名称，请让您的Adobe帐户团队更新映射。

**[!UICONTROL Linked Ad Accounts]：** （在创建使用弹出身份验证的帐户时可见）要同步的广告网络帐户。 从链接到网络登录的广告帐户中进行选择。

**[登录详细信息]：** （仅限[!DNL Yandex]帐户）要使用的帐户凭据：

* **[!UICONTROL Login]：**&#x200B;启用帐户API访问的登录名或ID。

* **[!UICONTROL Password]：**&#x200B;帐户的密码。

* **[!UICONTROL Access Key]：**&#x200B;要使用的开发人员帐户的访问密钥。

* **[!UICONTROL Application ID]：**&#x200B;要用于帐户的开发人员令牌。 所有[!DNL Yandex]帐户都使用相同的令牌。

* **[!UICONTROL Purse Campaign ID]：** （[!DNL Yandex]个帐户的“共享帐户”设置仅被禁用；可选）用于支付帐户中所有广告促销活动的促销活动的数字ID。

* **[!UICONTROL Finance Token]：** （[!DNL Yandex]个帐户的“共享帐户”设置仅被禁用；可选）用于财务相关API调用的开发人员令牌，例如，在广告商营销活动之间重新分配资金以实现组合优化。

**[!UICONTROL Currency]：** （只读）帐户使用的货币的缩写。 保存记录后，此值将自动填充为广告网络上的帐户配置的货币。

**[!UICONTROL Time Zone]：**&#x200B;广告商的时区。 保存记录后，此值将自动填充为广告商的Search、Social和Commerce帐户配置的时区。

**[!UICONTROL Login]：** （只读）用于登录帐户的用户帐户。

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]：**&#x200B;搜索、社交和Commerce将营销活动数据与帐户同步（如果支持），并针对项目组合中的营销活动推送自动竞价和/或营销活动预算。

**[!UICONTROL Account Authentication]> [!UICONTROL Re authenticate]：** （在您编辑使用弹出身份验证的帐户时可见）刷新连接或更新帐户权限。 当重新身份验证成功时，将自动保存新的访问令牌。

## [!UICONTROL Setup Tracking]选项卡

<!-- This should be the name of the whole left side of options -- they're all enabled/disabled depending on whether you enable our tracking -->

**[!UICONTROL Search, Social, & Commerce Tracking]：**&#x200B;是否使用Adobe Advertising转换跟踪服务启用跟踪。 此方法会生成唯一的点击跟踪ID，并将用户重定向到Adobe Advertising服务器进行跟踪，然后再将其发送到客户端的登陆页面。 此方法具有默认跟踪选项，您可以选择对这些选项进行自定义，还可以指定要附加到每个URL的参数。

要启用此功能，请打开&#x200B;**[启用跟踪]**。

>[!NOTE]
>
>* 如果更改此设置，则必须为帐户重新生成跟踪URL。
>* 营销活动级别的跟踪选项会覆盖帐户级别的设置。

**[!UICONTROL Tracking Type]：** （启用搜索、社交和Commerce跟踪时）将最终用户重定向到最终URL或目标URL的方法。 所选选项适用于帐户或营销活动中的所有竞价单位。 默认帐户级别设置继承自广告商的跟踪设置，默认营销活动级别设置继承自帐户设置。

* *[!UICONTROL Standard]：*&#x200B;要将最终用户重定向到指定的URL。

* *[!UICONTROL Token]：*&#x200B;要将最终用户重定向到URL，并将点击(`ef_id`)的Search、Social和Commerce ID记录为查询字符串参数，该参数用作令牌。 如果要报告离线交易，希望Search、Social和Commerce与Adobe Analytics交换数据，或者希望跟踪[!DNL Apple Safari]浏览器内发生的所有转化，请选择此选项。

>[!NOTE]
>
>* 如果您从[!UICONTROL Standard]切换到[!UICONTROL Token]，或者反之，则必须重新生成帐户的跟踪URL。
>* 您可以在营销策划级别覆盖帐户级别设置。

**[!UICONTROL Auto Update]：** （启用搜索、社交和Commerce跟踪时）标准化您的跟踪URL以实现跨浏览器和服务器的兼容性。 Search、Social和Commerce会在下次同步期间自动将以下内容上传到广告网络：(a)用于跟踪模板的搜索、Social和Commerce跟踪参数以及附加到最终URL的相同参数，或者(b)嵌入了Search、Social和Commerce跟踪代码的新目标URL。 对于具有[Adobe Advertising-Adobe Analytics集成](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)和服务器端AMO ID (s_kwcid)配置的广告商，该上传还包括您的[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户的[AMO ID参数](/help/integrations/analytics/ids.md#amo-id)。 默认帐户级别设置继承自广告商的跟踪设置。 您可以在营销策划级别覆盖帐户级别设置。

跟踪URL每天只更新不同步的实体（即添加的新实体和属性已更改的现有实体）。 因此，如果您将现有广告商/帐户/营销活动的此设置从“禁用”更改为“启用”，则不会为已同步的现有实体更新跟踪URL。 要将跟踪添加到现有已同步实体的URL，请联系您的Adobe客户团队，并请求执行一次性的手动同步过程。 自动上传流程可处理将来的更改。

**[!UICONTROL URL Encoding]：** （启用搜索、社交和Commerce跟踪时；帐户仅具有目标URL）对最终用户浏览器地址栏中的基本URL进行编码（如`%3D`而不是`=`）：

**[!UICONTROL Tracking Level]：** （启用搜索、社交和Commerce跟踪时；适用于帐户和营销活动级别；不适用于启用并行跟踪的广告网络）通过添加重定向并将参数附加到相关URL来跟踪点击量和收入的级别：

* *[!UICONTROL Keyword]：*&#x200B;只跟踪关键字级别的数据。 对[!DNL Yandex]不可用。

* *[!UICONTROL Ad]：*&#x200B;仅跟踪广告级别的数据。 对[!DNL Naver]不可用。

* *[!UICONTROL Keyword and Ad]：*&#x200B;在关键词和广告级别跟踪数据。 对[!DNL Naver]和[!DNL Yandex]不可用。

**[!UICONTROL Landing Page Suffix]** （仅限[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户；可选）要附加到最终URL末尾以跟踪信息的所有参数；包括您的企业必须跟踪的所有参数。

示例： `param1=value1&param2=value2`

使用Adobe Advertising点击跟踪的帐户必须在后缀中包含广告网络的点击标识符（[!DNL Microsoft Advertising]为`msclkid`；Google为`gclid`）。 具有Adobe Analytics集成的帐户必须使用AMO ID参数（以`s_kwcid`开头）。 如果该帐户具有服务器端AMO ID实施，则当用户单击广告时，参数会自动添加；否则，您必须在此处手动添加该参数。 查看 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)的[必需后缀格式和 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)的[必需后缀格式。

>[!NOTE]
>
>* [!UICONTROL Auto Update]跟踪设置未更新此字段。
>* 较低级别的最终URL后缀将覆盖帐户级别的后缀。 为便于维护，除非需要对各个帐户组件进行不同的跟踪，否则请仅使用帐户级别的后缀。 要在广告组级别或更低级别配置后缀，请使用广告网络的编辑器。

**帐户跟踪URL**： （仅限[!DNL Google Ads]、[!DNL LY Ads]和[!DNL Microsoft Advertising]帐户；可选）帐户的默认跟踪模板，它指定所有登入域外部重定向和跟踪参数，并将最终/登陆页面URL嵌入到参数中。 示例： `{lpurl}?source={network}&id=5`或`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`以包含重定向。

* 嵌入最终URL：

  * （仅限[!DNL Google Ads]和[!DNL Microsoft Advertising]）有关指示跟踪模板中最终URL的参数列表，请参阅[[!DNL Google Ads] 文档](https://support.google.com/google-ads/answer/6305348)中“可用的[!DNL ValueTrack]参数”部分中的（[!DNL Microsoft Advertising]仅限）[[!DNL Microsoft Advertising] 文档](https://help.ads.microsoft.com/#apex/3/en/56799)或（[!DNL Google Ads]仅限）跟踪模板参数。

  * （仅限[!DNL LY Ads]）使用参数`!{lpurl}`指示登陆页面URL。

* 您可以选择包含URL参数以及为营销活动定义的任何自定义参数，这些参数以&amp;号分隔，如`{lpurl}?matchtype={matchtype}&device={device}`。

* 您可以选择添加第三方重定向和跟踪。

* 当营销活动设置包括“[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]”时，Search、Social和Commerce会在您保存记录时自动为其自己的重定向和跟踪代码添加前缀。

>[!NOTE]
>
>* 对于[!DNL Google Ads]，请避免使用宏，这些宏不会替代来自启用并行跟踪的源的点击。 如果广告商必须使用宏，Adobe客户团队可与客户支持或实施团队合作来添加宏。
>* 最细粒度级别的跟踪模板将覆盖所有更高级别的值。 例如，如果帐户设置和关键字设置都包含一个值，则应用关键字值。
>* 如果您在广告、站点链接或关键词级别更新跟踪模板，则会重新提交相关广告以供审阅。 您可以在帐户、营销活动或广告组级别更新跟踪模板，而无需重新提交广告以供审批。

## [!UICONTROL Set up Adobe Analytics]选项卡

这些设置适用于具有[[!DNL Adobe Analytics for Advertising] 集成](/help/integrations/analytics/overview.md)的广告商。

**[!UICONTROL Adobe Analytics Report Suite]：**（可选）一个或多个Analytics报表包，Search、Social和Commerce会向其发送从广告网络收集的数据，包括帐户实体分类和点击数据。 此功能仅适用于受支持的广告网络。<!-- What are the repercussions of changing the suites? Timing of updated data? -->

对于要显示在报表包中的数据，必须(a)为帐户配置服务器端AMO ID功能，或者(b)启用设置为“[!UICONTROL Enable Advertising reporting in Analytics]”的广告商级别设置。 此外，必须将广告商的[!DNL Analytics]帐户配置为从Search、Social和Commerce接收数据。 有关更多信息，请与您的Adobe客户团队联系。

**[!UICONTROL Adobe Analytics Conversion Reporting]： [!UICONTROL Enable conversion reporting in Adobe Analytics]：** （[!DNL Meta Ads]个帐户；可选）将[AMO ID (s_kwcid)跟踪参数](/help/search-social-commerce/tracking/amo-id-tracking-parameter.md)附加到营销活动中的所有广告。 参数允许Adobe Analytics将转化与指定报表包中的Meta Ads促销活动以及实体分类和点击数据关联。

>[!MORELIKETHIS]
>
>* [关于广告网络帐户](../ad-network-account-about.md)
>* [管理商家中心帐户](/help/search-social-commerce/new-ui/set-up/manager-account-manage.md)
>* [更新 [!DNL Google Ads] 帐户的s_kwcid跟踪代码](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)
