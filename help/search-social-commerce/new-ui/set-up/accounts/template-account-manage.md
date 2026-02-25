---
title: （新UI）仅管理 [!DNL Naver] 帐户以进行跟踪
description: 了解如何在 [!DNL Naver] 帐户的新UI中设置和管理帐户详细信息。
feature: Search Campaign Management
source-git-commit: 0de2a01905727314ca6c0792c5efaf6450548293
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# （新UI）仅管理[!DNL Naver]帐户以进行跟踪

*Beta功能*

以下说明用于管理[[!DNL Naver] 帐户](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)以跟踪、报告和可视化您直接从广告网络购买的广告的性能。 搜索、Social和Commerce不会将数据与广告网络同步、提供自动竞价，也不会提供任何类型的优化或模拟。

有关可用功能的详细信息，请参阅[支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)。

## 创建广告网络帐户详细信息 {#create-account}

要启用帐户跟踪，您必须创建包含帐户访问凭据且状态为&#x200B;*已启用*&#x200B;的相应帐户记录。

>[!NOTE]
>
>要在广告网络上创建实际的帐户，请转到广告网络的网站。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 单击&#x200B;**[!UICONTROL Create Account]**。

1. 单击广告网络的名称，然后单击&#x200B;**[!UICONTROL Next]**。

1. 指定[帐户设置](#account-settings-naver)：

   1. 在&#x200B;**[!UICONTROL Enter Account Details]**&#x200B;选项卡上，指定常规帐户设置。

   1. （具有[[!DNL Adobe Analytics for Advertising] 集成](/help/integrations/analytics/overview.md)的广告商）单击“**[!UICONTROL Set up Adobe Analytics]**”选项卡，然后选择要用于跟踪和报告促销活动的所有[!DNL Analytics]报告包。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 编辑广告网络帐户详细信息 {#edit-account}

要更改帐户名称、更改帐户状态或更改用于跟踪和报告的[!DNL Analytics]报表包，请编辑帐户详细信息。

>[!NOTE]
>
>要编辑广告网络上的实际帐户，请转到广告网络的网站。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 通过以下任一方式选择帐户：

   * 选中帐户名称旁边的复选框，然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Edit]**。

   * 将光标放在帐户名称上，单击&#x200B;**...**，然后单击&#x200B;**[!UICONTROL Edit]**。

1. 编辑[帐户设置](#account-settings-api)：

   1. （可选）在&#x200B;**[!UICONTROL Account Details]**&#x200B;选项卡上，编辑帐户详细信息。

   1. （可选；具有[[!DNL Adobe Analytics for Advertising] 集成](/help/integrations/analytics/overview.md)的广告商）单击&#x200B;**[!UICONTROL Set up Adobe Analytics]**&#x200B;选项卡，然后编辑要用于跟踪和报告促销活动活动的[!DNL Analytics]报告包。

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. 单击&#x200B;**[!UICONTROL Save]**。

<!-- What does this do?

## Enable or disable ad network accounts {#enable-disable-account}

When you enable an ad network account, Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios. When you disable an ad network account, Search, Social, & Commerce stops all activity on the account. Data collected while the account was active is still stored, but the campaign management views and reports don't include data for the time period in which the account is disabled. You can later re-enable the account to resume activity with the account.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Do either of the following:

   * (From the [!UICONTROL Accounts] view):

     * (To enable the account) Select the check box next to the account name, and then click **[!UICONTROL Activate]** in the bulk actions toolbar.

     * (To disable the account) Select the check box next to the account name, and then click **[!UICONTROL Pause]** in the bulk actions toolbar.

   * (From the account settings):
   
     1. Select the account in either of the following ways:
     
        * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.
        
        * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.
        
     1. On the **[!UICONTROL Account Details]** tab, turn off **[!UICONTROL Account enabled]**.

     1. Click **[!UICONTROL Save]**.

-->

## 广告网络帐户设置 {#account-settings-api}

### [!UICONTROL Account Details]选项卡

#### [!UICONTROL Enter Account Details]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]：**&#x200B;要在Search、Social和Commerce中为帐户显示的名称。

>[!NOTE]
>
>如果您集成了“搜索”、“Social”和“Commerce-Adobe Analytics”，并更改了搜索帐户的名称，请让您的Adobe帐户团队更新映射。

**[!UICONTROL Network Account ID]：**&#x200B;广告网络分配的帐户ID。

**[!UICONTROL Currency]：**&#x200B;帐户使用的货币的缩写。

**[!UICONTROL Time Zone]：**&#x200B;广告商的时区。

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]：**&#x200B;搜索、社交和Commerce将营销活动数据与帐户同步（如果支持），并针对项目组合中的营销活动推送自动竞价和/或营销活动预算。

## [!UICONTROL Setup Analytics]选项卡

**[!UICONTROL Adobe Analytics Report Suite]：** （具有[[!DNL Adobe Analytics for Advertising] 集成](/help/integrations/analytics/overview.md)的广告商；可选）您上传的广告网络数据（包括实体分类和帐户的点击数据）将上传到Search、Social和Commerce发送的一个或多个Analytics报表包。

对于要显示在报表包中的数据，必须(a)为帐户配置服务器端AMO ID功能，或者(b)启用设置为“[!UICONTROL Enable Advertising reporting in Analytics]”的广告商级别设置。 此外，必须将广告商的[!DNL Analytics]帐户配置为从Search、Social和Commerce接收数据。 有关更多信息，请与您的Adobe客户团队联系。

>[!MORELIKETHIS]
>
>* [实施 [!DNL Naver] 仅跟踪帐户](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [关于广告网络帐户](/help/search-social-commerce/new-ui/set-up/accounts/ad-network-account-about.md)
