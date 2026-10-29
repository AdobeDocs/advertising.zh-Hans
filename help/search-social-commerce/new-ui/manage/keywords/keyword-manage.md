---
title: 管理关键字
description: 了解如何创建和管理可竞价和负关键字并将约束分配给关键字。
feature: Search Optimization, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: d3e38179ae119f35c184bee398edaaf456fab563
workflow-type: tm+mt
source-wordcount: '1282'
ht-degree: 0%
---
# 管理关键字

*Beta功能*

仅&#x200B;*[!DNL Google Ads]、[!DNL LY Ads]、[!DNL Microsoft Advertising]、[!DNL Yandex]和现有[!DNL Baidu]帐户*

关键字是与广告关联的单词或短语。 关键词设置包括关键词匹配类型、关键词触发广告时使用的最大竞价以及（对于某些广告网络）可选的跟踪参数。 关键字级别的设置会覆盖广告组或营销活动设置。 负关键字会阻止为匹配搜索显示广告。

一旦您[使广告网络帐户可通过API连接访问](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md)，并且Search、Social和Commerce已将该帐户数据与广告网络同步，您就可以在[支持的促销活动类型](/help/search-social-commerce/introduction/supported-inventory.md)中为搜索广告组创建关键字。 您还可以编辑和更改关键字的状态，以及创建和删除负关键字。

有关每个广告网络可用功能的详细信息，请参阅[支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)。

## 关于[!UICONTROL Keywords]视图 {#keyword-view-about}

[!UICONTROL Manage] > [!UICONTROL Keywords]视图包含选定广告商帐户的两个选项卡：

* [!UICONTROL Keywords]选项卡列出了筛选视图中的所有可竞价关键字。

* [!UICONTROL Negatives]选项卡列出了筛选视图中的所有负关键字。

### 可用操作

* [创建关键字](#keyword-create)

* [创建负关键字](#keyword-negative-create)

* [编辑关键词设置](#keyword-edit)

* [更改关键字和负关键字的状态或将其删除](#keyword-status)

* [将选定行中的所有数据复制到剪贴板](#copy-to-clipboard)

* [将约束分配给关键字，并从关键字中取消约束分配](#keyword-constraints)

* [将标签分类](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)分配给关键字

## 创建关键字 {#keyword-create}

>[!TIP]
>
>若要同时创建大量关键字，请使用[营销活动批量工作表](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Keywords]**。

1. 在&#x200B;**[!UICONTROL Keywords]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Create Keywords]**。

1. 在&#x200B;**[!UICONTROL Basic Settings]**&#x200B;步骤中，选择网络、帐户、营销活动和广告组。

1. 输入[[!DNL Baidu] 关键字设置](keyword-settings-baidu.md)、[[!DNL Google Ads] 关键字设置](keyword-settings-google.md)、[[!DNL LY Ads] 关键字设置](keyword-settings-yahoo-japan.md)、[[!DNL Microsoft Advertising] 关键字设置](keyword-settings-microsoft.md)或[[!DNL Yandex] 关键字设置](keyword-settings-yandex.md)。

   在一个操作中，最多可以输入或粘贴2000个关键字。 用逗号分隔多个关键字，或在单独的行中输入它们。

   >[!NOTE]
   >
   >如果帐户或营销活动设置仅在广告级别指定跟踪，则Search、Social和Commerce不会生成关键词跟踪。

1. 单击&#x200B;**[!UICONTROL Review and Save]**。

1. 查看设置。 要更改任何设置，请在适用的部分中单击![编辑](/help/search-social-commerce/assets/edit-new.png "编辑") **[!UICONTROL Edit]**&#x200B;并更改设置。

1. 单击&#x200B;**[!UICONTROL Create]**。

## 编辑关键词设置 {#keyword-edit}

更改关键字文本或匹配类型可以删除现有关键字并创建新关键字，具体取决于广告网络。 有关详细信息，请参阅广告网络的关键字设置。

>[!TIP]
>
>若要同时编辑大量关键词数据（包括不同广告网络上的关键词），请使用[营销活动批量工作表](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Keywords]**。

1. 在&#x200B;**[!UICONTROL Keywords]**&#x200B;选项卡上，选中要编辑的每个关键字旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Edit]**。

1. 编辑[[!DNL Baidu] 关键字设置](keyword-settings-baidu.md)、[[!DNL Google Ads] 关键字设置](keyword-settings-google.md)、[[!DNL LY Ads] 关键字设置](keyword-settings-yahoo-japan.md)、[[!DNL Microsoft Advertising] 关键字设置](keyword-settings-microsoft.md)或[[!DNL Yandex] 关键字设置](keyword-settings-yandex.md)。

   对于多个关键字，您只能编辑所有选定关键字通用的字段，并且您的更改将应用于所有选定关键字。 对于某些字母数字字段，您可以将现有值更改为指定值，将现有字符串替换为指定字符串，添加前缀或附加后缀。 对于某些货币字段，您可以将现有值更改为指定值，或者按指定百分比或货币金额增加或减少金额，但有限制。

1. 单击&#x200B;**[!UICONTROL Review and Save]**。

1. 查看设置。 要更改任何设置，请在适用的部分中单击![编辑](/help/search-social-commerce/assets/edit-new.png "编辑") **[!UICONTROL Edit]**&#x200B;并更改设置。

1. 单击&#x200B;**[!UICONTROL Update]**。

## 创建负关键字 {#keyword-negative-create}

仅&#x200B;*[!DNL Google Ads]、[!DNL LY Ads]、[!DNL Microsoft Advertising]和现有[!DNL Baidu]帐户*

您可以为定位搜索或显示/本机网络的搜索广告组或营销活动创建负关键字。

>[!NOTE]
>
>您还可以在[广告组设置](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md)和[促销活动设置](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)中创建和编辑负关键字。

>[!TIP]
>
>若要同时创建大量负关键字，请使用[营销活动批量工作表](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Keywords]**。

1. 在&#x200B;**[!UICONTROL Negatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Create Negatives]**，然后单击&#x200B;**[!UICONTROL Campaign Negative Keyword]**&#x200B;或&#x200B;**[!UICONTROL Ad Group Negative Keyword]**。

1. 选择网络、帐户、营销活动和（对于广告组级别的负关键字）广告组。

1. 输入负关键字。 使用以下语法，不带减号(`-`)：

   * 负广泛匹配： `keyword` （不受[!DNL Microsoft Advertising]支持）

   * 负面短语匹配： `"keyword"`

   * 完全匹配的负值： `[keyword]`

   用逗号分隔多个值，或在单独的行中输入它们。 在一个操作中，最多可以输入或粘贴2000个负关键字。 以下要求和限制适用：

   * 最大字符长度： [!DNL Baidu]： 30个单字节或15个双字节；[!DNL Microsoft Advertising]： 100个单字节或50个双字节；[!DNL Google Ads]和[!DNL LY Ads]： 80个单字节或40个双字节。

   * [!DNL Baidu]仅允许每个广告组的每个关键字有一个匹配类型。 例如，广告组1不能同时包括`"keyword"`和`[keyword]`。

   * [!DNL Google Ads]：每个关键字最多可包含10个单词，并且只能包含字母、数字和以下特殊字符：空格`# $ & _ - " [ ] ' + . / :`

1. 单击&#x200B;**[!UICONTROL Review and Save]**。

1. 查看设置。 要更改任何设置，请在适用的部分中单击![编辑](/help/search-social-commerce/assets/edit-new.png "编辑") **[!UICONTROL Edit]**&#x200B;并更改设置。

1. 单击&#x200B;**[!UICONTROL Create]**。

## 更改关键字和负关键字的状态 {#keyword-status}

您可以暂停活动、可竞价的搜索关键词以禁用对该关键词的竞价。 您稍后可以通过将状态更改回“活动”来恢复竞价。

您还可以删除活动或暂停的搜索关键字或负关键字。 已删除的关键字将从广告网络删除。 当您将其包含在数据过滤器中时，它们仍可见，但无法进行更改。

### 激活或暂停关键词

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Keywords]**。

1. 在&#x200B;**[!UICONTROL Keywords]**&#x200B;选项卡上，选择性地筛选列表，然后选中要更改其状态的每个关键字旁边的复选框。

1. 在批量操作工具栏中，更改状态：

   * 要激活暂停的关键字，请单击&#x200B;**[!UICONTROL Activate]**。

   * 要暂停活动关键字，请单击&#x200B;**[!UICONTROL Pause]**。

### 删除关键字或负关键字

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Keywords]**。

1. 在&#x200B;**[!UICONTROL Keywords]**&#x200B;或&#x200B;**[!UICONTROL Negatives]**&#x200B;选项卡上，选择性地筛选列表，然后选中要删除的每个关键字或负关键字旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。

## 将选定行中的所有数据复制到剪贴板 {#copy-to-clipboard}

根据应用的筛选条件和视图中可见的列，复制选定行中的可见信息。 信息将另存为制表符分隔值(TSV)。

1. 选中要复制其数据的每一行旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Copy]**。

## 管理关键字的约束分配 {#keyword-constraints}

您可以为营销活动、广告组、关键字、版面、单元级别产品组和动态搜索目标分配和移除竞价限制。 每个图元只能有一个约束。

约束由子实体继承，因此除非要覆盖继承的值，否则无需为子实体分配约束。

取消指定约束会删除与帐户组件及其所有子组件的关联，并且这些组件不再能使用该约束的报告数据。 取消指定约束并不会删除约束或帐户组件本身。

>[!NOTE]
>
>* 如果您稍后编辑非可变广告的关键字或广告副本（从而创建新关键字或广告），则约束不会分配给新实体。
>* 活动约束仅限制优化旧关键词级别项目组合中已分配竞价单位的竞价。 对于活跃项目组合中的竞价单位、混合项目组合中的竞价单位或不在项目组合中的竞价单位，它们将被忽略。

### 为关键字分配约束 {#keyword-constraint-assign}

可以将单个约束指定给一个或多个关键字。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Keywords]**。

1. 在&#x200B;**[!UICONTROL Keywords]**&#x200B;选项卡上，选中要为其分配单个约束的每个关键字旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**。

1. 选择约束。

1. 单击&#x200B;**[!UICONTROL Assign Now]**。

### 从关键字取消分配约束 {#keyword-constraint-unassign}

取消指定约束并不会删除它。 要删除约束条件，使其不可用于将来使用，请参阅优化指南中有关“竞价约束条件”的一章中的“删除搜索竞价单位的约束条件”，该章节可从搜索、社交和Commerce中获取。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Keywords]**。

1. 在&#x200B;**[!UICONTROL Keywords]**&#x200B;选项卡上，选中要从中取消分配约束的每个关键字旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 单击&#x200B;**[!UICONTROL Confirm]**。

>[!MORELIKETHIS]
>
>* [[!DNL Baidu] 关键字设置](keyword-settings-baidu.md)
>* [[!DNL Google Ads] 关键字设置](keyword-settings-google.md)
>* [[!DNL LY Ads] 关键字设置](keyword-settings-yahoo-japan.md)
>* [[!DNL Microsoft Advertising] 关键字设置](keyword-settings-microsoft.md)
>* [[!DNL Yandex] 关键字设置](keyword-settings-yandex.md)
>* [管理搜索竞价单位的约束](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [管理标签分类](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
