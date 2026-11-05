---
title: 管理营销活动和广告组的受众目标
description: 了解如何管理Google广告和Microsoft Advertising的受众目标及其竞价调整。
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
source-wordcount: '562'
ht-degree: 0%
---
# 管理营销活动和广告组的受众目标

仅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户*

[!DNL Google Ads]营销活动和广告组以及[!DNL Microsoft Advertising]广告组可以定位来自同一广告网络的特定[受众](audience-manage.md)。 广告网络决定了受众必须有多大才能成为目标。

受众目标可将现有受众与营销活动或广告组关联。 您可以编辑现有目标的竞价调整和状态。

>[!NOTE]
>
>[受众排除项](audience-exclusions.md)始终覆盖目标。

## 关于[!UICONTROL Targets]视图 {#audience-targets-view-about}

[!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Targets]视图在筛选视图中列出了选定广告商的受众目标。

查看数据需要[!UICONTROL View Audiences]权限。 编辑、更改目标的状态以及删除目标需要[!UICONTROL Edit Audience Targets]权限。

### 可用操作

<!--
Restricted to internal beta users:

* [Configure audience targets](#audience-targets-create)
-->

* [编辑受众目标竞价调整和状态](#audience-targets-edit)

* [更改受众目标的状态或删除受众目标](#audience-targets-status)

* [将选定行中的所有数据复制到剪贴板](#copy-to-clipboard)

<!--
Restricted to internal beta users: audience target creation.

## Configure audience targets {#audience-targets-create}

Creating targets requires the [!UICONTROL Edit Audience Targets] permission in addition to internal beta access.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Targets]** tab.

1. Click **[!UICONTROL Create Target]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select one or more audiences from the account. You can search the list.

   [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

1. Select the campaigns or ad groups to target:

   * Select each applicable campaign or ad group for inclusion.

   * To view a campaign's ad groups, expand the campaign.

   * Use the list's search controls to find specific campaigns or ad groups.

   You can't configure a target for both a parent campaign and a child ad group that automatically uses the target.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

1. (Optional) [Set a bid adjustment](#audience-targets-edit) for the new targets.
-->

## 编辑受众目标竞价调整和状态 {#audience-targets-edit}

您可以一次编辑一个或多个受众目标。 您的更改将应用于所有选定的目标。

>[!NOTE]
>
>当父营销活动使用CPC竞价策略并且在配置为自动优化受众目标竞价调整值的项目组合中时，Search、Social和Commerce会自动优化竞价修饰符。 未优化[!DNL Microsoft Advertising]动态再营销受众目标的竞价修饰符。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Audiences]**，然后单击&#x200B;**[!UICONTROL Targets]**&#x200B;选项卡。

1. 选中要编辑的每个目标旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Edit]**。

1. 编辑&#x200B;**[!UICONTROL Bid Modifier]**&#x200B;或&#x200B;**[!UICONTROL Status]**，或同时编辑两者。 查看[编辑设置](#audience-targets-edit-settings)。

   字段保持不变，以保留现有值。

1. （可选）展开&#x200B;**[!UICONTROL ADDITIONAL DETAILS]**&#x200B;并输入&#x200B;**[!UICONTROL Project Name]**&#x200B;和&#x200B;**[!UICONTROL Description]**。

1. 单击&#x200B;**[!UICONTROL Save]**。

您还可以直接在数据表中编辑单个目标的竞价调整，方法是单击&#x200B;**[!UICONTROL Bid Adjustment]**&#x200B;列中的该目标的值。

## 更改受众目标的状态或删除受众目标 {#audience-targets-status}

您可以暂停活动的受众目标以禁用对该目标的竞价，稍后通过激活它来恢复竞价。 您还可以删除活动或暂停的目标。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Audiences]**，然后单击&#x200B;**[!UICONTROL Targets]**&#x200B;选项卡。

1. （可选）筛选列表以包含特定的受众目标。

1. 选中要更改其状态的每个目标旁边的复选框。

1. 在批量操作工具栏中，单击下列选项之一：

   * **[!UICONTROL Activate]**&#x200B;以激活所选目标。

   * **[!UICONTROL Pause]**&#x200B;以暂停所选目标。

   * **[!UICONTROL Delete]**&#x200B;以删除所选目标。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。

## 将选定行中的所有数据复制到剪贴板 {#copy-to-clipboard}

根据应用的筛选条件和视图中可见的列，复制选定行中的可见信息。 信息将另存为制表符分隔值(TSV)。

1. 选中要复制其数据的每一行旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Copy]**。

## 受众目标编辑设置 {#audience-targets-edit-settings}

**[!UICONTROL Bid Modifier]：**&#x200B;如何更改受众竞价调整：

* *[!UICONTROL Set To]：*&#x200B;将现有竞价调整替换为指定的百分比。

* *[!UICONTROL Increase]：*&#x200B;将现有值增加指定的百分比。

* *[!UICONTROL Decrease]：*&#x200B;按指定的百分比减少现有值。

对于[!UICONTROL Increase]和[!UICONTROL Decrease]，请输入非负值。

对于设置的值，0%不调整竞价。 其他支持的值介于–90%到900%之间。 例如，如果关键词级别的竞价为1 USD，而受众竞价调整为50%，则该受众的竞价将增加到1.50 USD。

**[!UICONTROL Status]：**&#x200B;选择&#x200B;**[!UICONTROL Active]**&#x200B;以启用竞价，选择&#x200B;**[!UICONTROL Paused]**&#x200B;以禁用目标的竞价。

>[!MORELIKETHIS]
>
>* [管理受众](audience-manage.md)
>* [管理营销活动和广告组的受众排除](audience-exclusions.md)
