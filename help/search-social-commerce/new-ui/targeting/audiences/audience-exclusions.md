---
title: 管理营销活动和广告组的受众排除
description: 了解Google Ads和Microsoft Advertising受众排除项，包括如何删除Google Ads排除项。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 7e7dcde9fb195e04025a1a8d89e792ff562b053f
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%
---
# 管理营销活动和广告组的受众排除

仅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户*

受众排除可阻止向特定[受众](audience-manage.md)中的用户显示促销活动或广告组中的广告。

对于[!DNL Google Ads]帐户，您可以排除任何受众类型。 对于[!DNL Microsoft Advertising]帐户，您只能排除动态二次营销受众。

>[!NOTE]
>
>排除项始终会覆盖[受众目标](audience-targets-manage.md)。

## 关于[!UICONTROL Exclusions]视图 {#audience-exclusions-view-about}

[!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Exclusions]视图在选定广告商的筛选视图中列出了受众排除。

查看数据需要[!UICONTROL View Audiences]权限。 选择行并删除支持的排除项需要[!UICONTROL Edit Audience Exclusions]权限。

### 可用操作

<!--
Restricted to internal beta users:

* [Configure audience exclusions](#audience-exclusions-create)
-->

* [删除受众排除项](#audience-exclusions-delete)

* [将选定行中的所有数据复制到剪贴板](#copy-to-clipboard)

<!--
Restricted to internal beta users: audience exclusion creation.

## Configure audience exclusions {#audience-exclusions-create}

Creating exclusions requires the [!UICONTROL Edit Audience Exclusions] permission in addition to internal beta access.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Exclusions]** tab.

1. Click **[!UICONTROL Create Exclusion]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select one or more audiences from the account. You can search the list.

   [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

1. Select the campaigns or ad groups from which to exclude the audiences:

   * Select each applicable campaign or ad group for exclusion.

   * To view a campaign's ad groups, expand the campaign.

   * Use the list's search controls to find specific campaigns or ad groups.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.
-->

## 删除受众排除项 {#audience-exclusions-delete}

仅&#x200B;*[!DNL Google Ads]个排除项*

您可以删除一个或多个[!DNL Google Ads]受众排除。 此视图不支持删除[!DNL Microsoft Advertising]排除项。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Audiences]**，然后单击&#x200B;**[!UICONTROL Exclusions]**&#x200B;选项卡。

1. （可选）筛选列表以包含特定受众排除项。

1. 选中要删除的每个[!DNL Google Ads]排除项旁边的复选框。 请勿在所选内容中包含来自其他广告网络的排除项。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。

## 将选定行中的所有数据复制到剪贴板 {#copy-to-clipboard}

根据应用的筛选条件和视图中可见的列，复制选定行中的可见信息。 信息将另存为制表符分隔值(TSV)。

1. 选中要复制其数据的每一行旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Copy]**。

>[!MORELIKETHIS]
>
>* [管理受众](audience-manage.md)
>* [管理营销活动和广告组的受众目标](audience-targets-manage.md)
