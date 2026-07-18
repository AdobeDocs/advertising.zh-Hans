---
title: 管理 [!DNL Google Ads] 动态搜索目标
description: 了解如何创建和管理 [!DNL Google Ads] 动态搜索目标。
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/MsSy-p-WSroc3FyiHx6kvcTohEaWOqJCzqbl91mNwK0'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 82db1b4d0d8703229a4002e932d5b2f52f845814
workflow-type: tm+mt
source-wordcount: 718
ht-degree: 0%

---

# 管理[!DNL Google Ads]动态搜索目标

仅&#x200B;*[!DNL Google Ads]个帐户*

您可以为使用搜索网络的[!DNL Google Ads]营销活动创建、编辑和更改动态搜索目标的状态。

## 什么是动态搜索目标？

动态搜索目标定义广告网络使用网站中的所有页面还是部分页面来定位动态搜索广告。 在广告组级别配置动态搜索目标；它们适用于同一广告组中的所有动态搜索广告。

根据您的促销活动设置，动态搜索目标可能是必需或可选的：

* 如果未在营销活动的“[!UICONTROL DSA Options]”部分指定网站域和语言，则必须创建动态搜索目标。

* 在营销活动的“[!UICONTROL DSA Options]”部分指定网站域和语言时，您可以选择创建动态搜索目标。

  [!DNL Google Ads]会根据使用这些设置指定的网站内容自动显示您的动态搜索广告。

要最佳跟踪性能，请为每个动态搜索目标配置一个广告组的营销活动，并包含定向所有标准的广告组。

有关[!DNL Google Ads]动态搜索广告的更多信息，请参阅https://support.google.com/google-ads/answer/2471185。

## [!UICONTROL Auto Targets]视图

[!UICONTROL Auto Targets]视图列出了所选广告商帐户的筛选视图中的所有动态搜索目标。

您可以在[!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Auto Targets]视图中创建、编辑和更改动态搜索目标的状态。

您还可以[将标签](/help/search-social-commerce/campaign-management/label-classifications/classification-values-assign-campaign-management.md)应用于任何目标。

### 可用操作

<!--
* Create a dynamic search target

* Edit the settings for a dynamic search target

* Change the status of dynamic search targets
-->

* [将约束分配给动态搜索目标](#constraint-assign)，并从动态搜索目标[取消分配约束](#constraint-unassign)

* [将标签分类](#classification-values-assign)分配给动态搜索目标，并[从动态搜索目标中删除标签分类](#classification-values-remove)

>[!NOTE]
>
>您可以通过上传[批量工作表文件](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)并将它们发布到广告网络，同时创建和编辑大量目标数据（包括标签和限制分配）。

<!--
Not available yet:

## Create a [!DNL Google Ads] dynamic search target

You can create dynamic search targets to define pages in your websites (that is, the domains used in your ads' display URLs) whose content is used to target your dynamic search ads in the same ad group.

You can target all criteria or up to three individual criteria.

>[!NOTE]
>
>To best track performance, create an "[!UICONTROL All Targets]" target for only one ad group per campaign.

>[!TIP]
>
>To create many account components at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network, the account, the campaign, and the ad group, and then click **[!UICONTROL Continue]**.

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

1. Click **[!UICONTROL Post]**.

## Edit [!DNL Google Ads] dynamic search target settings

You can edit the status or maximum bid for a [!DNL Google Ads] dynamic search target. You can't change the criteria that are targeted.

>[!TIP]
>
>To edit large amounts of data at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. Select the check box next to each row to edit.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

   For multiple targets, your changes are applied to all of the selected targets. For the [!UICONTROL Bid field], you have options to change existing values to a specified value or to either increase or decrease the amount by a specified percentage or monetary amount, with a limit.

1. Save the data:

   * (Single targets) Click **[!UICONTROL Post]**.
   
   * (Multiple ad groups) Click **[!UICONTROL Post Now]**.

## Change the status of [!DNL Google Ads] dynamic search targets

You can pause any active dynamic search target in a supported campaign type to stop using them for dynamic search ads in the same ad group. You can later use them as targets by changing the ad status back to active.

You can also delete any dynamic target.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. (Optional) Filter the list to include specific dynamic targets.

1. Do either of the following:
   
   * To change the status of one dynamic target, click in the **[!UICONTROL Status]** column and change the status.
   
   * To delete one or more dynamic targets, do the following:
   
     1.  Select the check box next to each dynamic target you want to delete.
     
        For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."
     
     1. In the toolbar, click ![More](/help/search-social-commerce/assets/more.png "More") and select **[!UICONTROL Delete]**.
     
     1. In the confirmation message, click **[!UICONTROL Delete]**.

## [!DNL Google Ads] dynamic search target settings {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (Required when you don't specify a website domain and language in the campaign's [!UICONTROL DSA Options] section; read-only for existing targets) Dynamic search targets for the ad group:

* *[!UICONTROL All Targets]* (the default): Targets all indexed pages.

* *\[Specific Targets\]:* Targets up to three criteria for the indexed pages. When you select this, you must specify the criteria by specifying information categories and specific values for which to target ads (for example, "URL contains shoes.example.com"). To specify more than one criteria, click **[!UICONTROL + And]**. Target criteria include:

  * *[!UICONTROL Category]:* To show ads for indexed pages with a specific [!DNL Google Ads] content category.

  * *[!UICONTROL URL]:* To show ads for indexed pages with a specific URL, where the value may be included anywhere within the URL.

  * *[!UICONTROL Page Title]:* To show ads for indexed pages with specific text in the page title.

  * *[!UICONTROL Page Content]:* To show ads for indexed pages with specific content.

**Status:** The status of the target settings:

* *[!UICONTROL Active]* (the default): Enables bidding.

* *[!UICONTROL Paused]:* Disables bidding.

* *[!UICONTROL Deleted]* (existing targets only): Deletes the target settings.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** The maximum cost per click (CPC) for an ad or cost per 1000 impressions (CPM) for an ad, as applicable for the ad network and campaign pricing model. This value overrides the ad group-level value.

>[!NOTE]
>
>If the target is in an optimized portfolio, then the specified CPC bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations.

-->

## 从新[!UICONTROL Auto Targets]视图为选定的动态搜索目标分配约束 {#constraint-assign}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Target]>[!UICONTROL Auto Targets]**。

1. 选中要为其分配单个约束的每个动态搜索目标旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**。

1. 选择约束。

1. 单击&#x200B;**[!UICONTROL Assign Now]**。

## 从新[!UICONTROL Auto Targets]视图中取消分配选定动态搜索目标的约束 {#constraint-unassign}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Auto Targets]**。

1. 选中要从中取消分配约束的每个动态搜索目标旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 单击&#x200B;**[!UICONTROL Confirm]**。

## 将分类值分配给动态搜索目标 {#classification-values-assign}

>[!NOTE]
>
>标签值由子实体继承，因此除非要覆盖继承的值，否则不要为子实体输入值。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Target]>[!UICONTROL Auto Targets]**。

1. 选中要为其分配标签值的每个动态搜索目标旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在批量操作工具栏中，单击&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**。

1. 对于每个适用的分类值，执行以下操作：

   1. 在&#x200B;**[!UICONTROL Classifications]**&#x200B;列中，指定分类：

      * 要使用现有分类，请单击分类名称以将其展开。

      * 要创建分类，请单击列标题中的[!UICONTROL +]。 在输入字段中，输入分类名称，然后单击![保存](/help/search-social-commerce/assets/save-checkmark.png "保存")以立即保存分类。 要使用新分类，请单击分类名称以将其展开。

        名称必须包含[个32-126](https://www.asciitable.com/)的ASCII字符，最大长度为27个单字节字符。

   1. 在&#x200B;**[!UICONTROL Value Name]**&#x200B;列中，指定所选分类的值：

      * 要使用现有值，请选择该值。

      * 要创建值，请在列标题中单击[!UICONTROL +]。 在输入字段中，输入值，然后单击![保存](/help/search-social-commerce/assets/save-checkmark.png "保存")以立即保存该值并默认选择它。

        最大长度为100个字符，可包含ASCII和非ASCII字符。

1. 单击&#x200B;**+[!UICONTROL Assign Now]**。

## 从动态搜索目标中删除标签分类值{#classification-values-remove}

删除分类值将删除与帐户组件及其所有子组件的关联。 分类值的报表数据不再可用于这些组件。 删除分类值不会删除该值，也不会删除帐户组件。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Target]>[!UICONTROL Auto Targets]**。

1. 选中将从中删除标签值的每个动态搜索目标旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**。

1. 选中要从所选实体中移除的每个分类值旁边的复选框。

   要选择所有分配的值，请单击&#x200B;**[!UICONTROL Select All]**。 要取消选择所有分配的值，请单击&#x200B;**[!UICONTROL Deselect All]**。

1. 单击&#x200B;**[!UICONTROL Unassign Selected]**。

>[!MORELIKETHIS]
>
>* [（新UI）管理搜索竞价单位的约束](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [（新UI）管理标签分类](/help/search-social-commerce/new-ui/reports/label-classifications-manage.md)
