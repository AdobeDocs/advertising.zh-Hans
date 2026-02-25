---
title: 配置用于数据上载的广告网络帐户
description: 了解如何设置和管理广告网络帐户的帐户详细信息。
feature: Search Campaign Management
exl-id: 7e8fb475-21f9-446b-a112-e0f27a4c4172
source-git-commit: 00565a6c9e784472fab9c9d223c83b0c7cbb91b1
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# 管理用于数据上传的广告网络帐户

<!-- Edit all, including title and metadata -->

以下说明用于管理您将为其上传帐户数据的广告网络帐户的帐户详细信息。

有关每个广告网络可用功能的详细信息，请参阅[支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)。

>[!NOTE]
>
>有关管理使用广告网络的API进行搜索、社交和Commerce同步的广告网络帐户的帐户详细信息的说明，请参阅“通过API连接管理广告网络帐户[”。](../api-accounts/api-account-manage.md)

## 创建帐户详细信息 {#create-account}

1. 单击&#x200B;**[!UICONTROL Create Account]**。

1. 单击广告网络的名称，然后单击&#x200B;**[!UICONTROL Next]**。

1. 指定[帐户设置](#account-settings)：

   1. 在&#x200B;**[!UICONTROL Account Details]**&#x200B;选项卡上，编辑帐户详细信息。

   1. （具有[[!DNL Adobe Analytics for Advertising] 集成](/help/integrations/analytics/overview.md)的广告商）单击“**[!UICONTROL Set up Adobe Analytics]**”选项卡，然后编辑用于跟踪和报告促销活动的[!DNL Analytics]报告包。

   1. （可选）在&#x200B;**[!UICONTROL Upload File]**&#x200B;选项卡上，上传帐户的数据文件。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 编辑帐户详细信息 {#edit-account}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 通过以下任一方式选择帐户：

   * 选中帐户名称旁边的复选框，然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Edit]**。

   * 将光标放在帐户名称上，单击&#x200B;**...**，然后单击&#x200B;**[!UICONTROL Edit]**。

1. 编辑[帐户设置](#account-settings-upload)：

   1. （可选）在&#x200B;**[!UICONTROL Account Details]**&#x200B;选项卡上，编辑帐户详细信息。

   1. （可选；具有[[!DNL Adobe Analytics for Advertising] 集成](/help/integrations/analytics/overview.md)的广告商）单击&#x200B;**[!UICONTROL Set up Adobe Analytics]**&#x200B;选项卡，然后编辑要用于跟踪和报告促销活动活动的[!DNL Analytics]报告包。

   1. （可选）在&#x200B;**[!UICONTROL Upload File]**&#x200B;选项卡上，上传帐户的数据文件。

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. 单击&#x200B;**[!UICONTROL Save]**。

## 启用或禁用广告网络帐户 {#enable-disable-account}

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

## 帐户设置 {#account-settings-upload}

### [!UICONTROL Account Details]选项卡

**[!UICONTROL Account Name]：**&#x200B;要在Search、Social和Commerce中为帐户显示的名称。

>[!NOTE]
>
>如果您集成了“搜索”、“Social”和“Commerce-Adobe Analytics”，并更改了搜索帐户的名称，请通知您的Adobe帐户团队，以便他们能够更新映射。

**[!UICONTROL Network Account ID]：**&#x200B;广告网络分配的帐户ID。 此ID仅用于报表。 搜索、社交和Commerce不会直接连接到广告网络帐户。

**[!UICONTROL Currency]：** （现有帐户的只读）用于帐户的货币的缩写。

**[!UICONTROL Time Zone]：** （现有帐户的只读）广告商的时区。

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]：**&#x200B;搜索、社交和Commerce允许自动获取指定S3存储段的数据。

## [!UICONTROL Setup Analytics]选项卡

**[!UICONTROL Adobe Analytics Report Suite]：** （具有[[!DNL Adobe Analytics for Advertising] 集成](/help/integrations/analytics/overview.md)的广告商；可选）您上传的广告网络数据（包括实体分类和帐户的点击数据）将上传到Search、Social和Commerce发送的一个或多个Analytics报表包。

对于要显示在报表包中的数据，必须(a)为帐户配置服务器端AMO ID功能，或者(b)启用设置为“[!UICONTROL Enable Advertising reporting in Analytics]”的广告商级别设置。 此外，必须将广告商的[!DNL Analytics]帐户配置为从Search、Social和Commerce接收数据。 有关更多信息，请与您的Adobe客户团队联系。

### [!UICONTROL Upload File]选项卡

（可选）上载帐户的数据文件。<!-- For instructions, see "[Upload offline account data for reporting and simulations](upload-account-data.md)." -->
