---
title: 管理投放位置
description: 了解如何创建和管理Google广告投放和负面投放，并为投放分配限制。
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
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: d3e38179ae119f35c184bee398edaaf456fab563
workflow-type: tm+mt
source-wordcount: '1390'
ht-degree: 0%
---
# 管理投放位置

*Beta功能*

仅&#x200B;*[!DNL Google Ads]个帐户*

投放位置是显示网络上可显示广告的位置。 投放设置包括最高竞价和可选跟踪参数。 投放级别设置会覆盖广告组或营销活动设置。 负值版面会阻止广告在指定网站上显示。

一旦您[使广告网络帐户可通过API连接访问](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md)，并且Search、Social和Commerce已将该帐户数据与广告网络同步，您便可以在针对显示网络的[支持的促销活动类型](/help/search-social-commerce/introduction/supported-inventory.md)中为广告组创建投放位置。 您还可以编辑和更改版面的状态，以及创建和删除负版面。

>[!NOTE]
>
>[!DNL Google Ads]不提供投放位置的广告级性能数据。

## 关于[!UICONTROL Placements]视图 {#placement-view-about}

[!UICONTROL Targeting] > [!UICONTROL Placements]视图包含选定广告商帐户的两个选项卡：

* [!UICONTROL Placements]选项卡列出了筛选视图中的所有可竞价投放位置。

* [!UICONTROL Negatives]选项卡列出了筛选视图中的所有负向版面。

查看页面需要[!UICONTROL View Placements]权限。 创建版面或负面版面、编辑版面、更改版面状态以及删除版面或负面版面需要[!UICONTROL Edit Placements]权限。

### 可用操作

* [创建投放位置](#placement-create)

* [创建负面投放位置](#placement-negative-create)

* [编辑投放设置](#placement-edit)

* [更改版面的状态或删除版面和负版面](#placement-status)

* [将选定行中的所有数据复制到剪贴板](#copy-to-clipboard)

* [将约束分配给投放位置，并从投放位置中取消分配约束](#placement-constraints)

* [将标签分类分配给投放位置](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)

## 创建投放位置 {#placement-create}

>[!TIP]
>
>要同时创建大量投放位置，请使用[营销活动批量处理工作表](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Placements]**。

1. 在&#x200B;**[!UICONTROL Placements]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Create Placement]**。

1. 在&#x200B;**[!UICONTROL Basic Settings]**&#x200B;步骤中，选择网络、帐户、营销活动和广告组。

1. 输入[位置设置](#placement-create-settings)。

   要创建多个投放位置，请使用逗号分隔网站URL。

1. 单击&#x200B;**[!UICONTROL Review and Save]**。

1. 查看设置。 要更改任何设置，请在适用的部分中单击![编辑](/help/search-social-commerce/assets/edit-new.png "编辑") **[!UICONTROL Edit]**&#x200B;并更改设置。

1. 单击&#x200B;**[!UICONTROL Create]**。

## 创建负面投放位置 {#placement-negative-create}

您可以为针对显示网络的[!DNL Google Ads]营销活动或广告组创建负版面。

>[!NOTE]
>
>您还可以在[广告组设置](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md)和[促销活动设置](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)中创建和编辑负版面。

>[!TIP]
>
>若要一次创建大量负面投放位置，请使用[营销活动批量处理工作表](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Placements]**。

1. 在&#x200B;**[!UICONTROL Negatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Create Negative]**，然后单击&#x200B;**[!UICONTROL Campaign Negative]**&#x200B;或&#x200B;**[!UICONTROL Ad Group Negative]**。

1. 在&#x200B;**[!UICONTROL Basic Settings]**&#x200B;步骤中，选择网络、帐户、营销活动，以及（对于广告组级别的负面投放）广告组。

1. 在&#x200B;**[!UICONTROL Manage Websites]**&#x200B;步骤中，输入负网站URL，如`www.example.com`或`example.com/shoes`。

   用逗号分隔多个URL。 此表单接受网站URL，而不接受主题或类别字符串。

1. 单击&#x200B;**[!UICONTROL Review and Save]**。

1. 查看设置。 要更改任何设置，请在适用的部分中单击![编辑](/help/search-social-commerce/assets/edit-new.png "编辑") **[!UICONTROL Edit]**&#x200B;并更改设置。

1. 单击&#x200B;**[!UICONTROL Create]**。

## 编辑投放设置 {#placement-edit}

您可以编辑一个或多个投放位置的状态、竞价、基本URL和跟踪模板。 您无法更改目标网站URL或编辑已删除的投放位置。

>[!TIP]
>
>若要一次编辑大量投放位置数据，请使用[营销活动批量工作表](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Placements]**。

1. 在&#x200B;**[!UICONTROL Placements]**&#x200B;选项卡上，选中要编辑的每个投放位置旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Edit]**。

1. 在&#x200B;**[!UICONTROL Edit Placements]**&#x200B;面板中，编辑[位置设置](#placement-edit-settings)。

   对于多个投放位置，您的更改将应用于所有选定的投放位置。 您可以将竞价设置为指定值或者通过指定百分比或货币金额来增加或减少竞价，但需设置限制。 对于URL，可以替换现有值、查找和替换文本、添加前缀或附加后缀。

   当所选投放位置使用多种货币时，将禁用竞价编辑。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 更改投放位置和负面投放位置的状态 {#placement-status}

您可以暂停活动、可竞价的投放位置以禁用对该投放位置的竞价。 您稍后可以通过将状态更改回“活动”来恢复竞价。

您还可以删除活动或暂停的投放位置或负投放位置。 已删除的投放位置将从广告网络中删除。 当您将其包含在数据过滤器中时，它们仍可见，但无法进行更改。

### 激活或暂停投放

1. 在主菜单中，单击&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Placements]**。

1. 在&#x200B;**[!UICONTROL Placements]**&#x200B;选项卡上，根据需要筛选列表，然后选中要更改其状态的每个版面旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Edit]**。

1. 在&#x200B;**[!UICONTROL Placement Details]**&#x200B;部分中，更改&#x200B;**[!UICONTROL Status]**：

   * 要激活暂停的投放位置，请选择&#x200B;**[!UICONTROL Active]**。

   * 要暂停活动投放位置，请选择&#x200B;**[!UICONTROL Paused]**。

1. 单击&#x200B;**[!UICONTROL Save]**。

### 删除版面或负版面

1. 在主菜单中，单击&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Placements]**。

1. 在&#x200B;**[!UICONTROL Placements]**&#x200B;或&#x200B;**[!UICONTROL Negatives]**&#x200B;选项卡上，选择性地筛选列表，然后选中要删除的每个版面或负面版面旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。

## 将选定行中的所有数据复制到剪贴板 {#copy-to-clipboard}

根据应用的筛选条件和视图中可见的列，复制选定行中的可见信息。 信息将另存为制表符分隔值(TSV)。

1. 选中要复制其数据的每一行旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Copy]**。

## 管理投放位置的限制分配 {#placement-constraints}

您可以为营销活动、广告组、关键字、版面、单元级别产品组和动态搜索目标分配和移除竞价限制。 每个图元只能有一个约束。

约束由子实体继承，因此除非要覆盖继承的值，否则无需为子实体分配约束。

取消指定约束会删除与帐户组件及其所有子组件的关联，并且这些组件不再能使用该约束的报告数据。 取消指定约束并不会删除约束或帐户组件本身。

>[!NOTE]
>
>* 如果您稍后编辑非可变广告的关键字或广告副本（从而创建新关键字或广告），则约束不会分配给新实体。
>* 活动约束仅限制优化旧关键词级别项目组合中已分配竞价单位的竞价。 对于活跃项目组合中的竞价单位、混合项目组合中的竞价单位或不在项目组合中的竞价单位，它们将被忽略。

### 将限制分配给投放位置 {#placement-constraint-assign}

可以将单个约束分配给一个或多个位置。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Placements]**。

1. 在&#x200B;**[!UICONTROL Placements]**&#x200B;选项卡上，选中要为其分配单个约束的每个投放位置旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Assign]>[!UICONTROL Bid Constraint]**。

1. 选择约束。

1. 单击&#x200B;**[!UICONTROL Assign Now]**。

### 从投放位置取消分配约束 {#placement-constraint-unassign}

取消指定约束并不会删除它。 要删除约束条件，使其不可用于将来使用，请参阅[管理搜索竞价单位的约束条件](/help/search-social-commerce/new-ui/goals/constraints-manage.md#constraint-change-status)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Placements]**。

1. 在&#x200B;**[!UICONTROL Placements]**&#x200B;选项卡上，选中要从中取消分配约束的每个放置旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Unassign]>[!UICONTROL Bid Constraint]**。

1. 单击&#x200B;**[!UICONTROL Confirm]**。

## 投放设置 {#placement-settings}

### 创建投放位置时的设置 {#placement-create-settings}

#### [!UICONTROL Basic Settings]

**[!UICONTROL Network]：**&#x200B;广告网络。 仅支持[!DNL Google Ads]。

**[!UICONTROL Account]：**&#x200B;广告网络帐户。

**[!UICONTROL Campaign]：**&#x200B;营销活动。

**[!UICONTROL Ad Group]：**&#x200B;广告组。

#### [!UICONTROL Placement Details]

显示网络中可显示广告的&#x200B;**[!UICONTROL Placements]：**&#x200B;个站点。 输入有效的网站URL，如`www.example.com`、`example.com`或`example.com/shoes`。 用逗号分隔多个URL。 URL不能包含问号(`?`)。

若要改为排除网站，请[从[!UICONTROL Targeting] > [!UICONTROL Placements] > [!UICONTROL Negatives]选项卡中创建负面投放位置](#placement-negative-create)，或者使用广告组和促销活动设置。

**[!UICONTROL Status]：**&#x200B;投放位置的显示状态： *[!UICONTROL Active]* （启用竞价）或&#x200B;*[!UICONTROL Paused]* （禁用竞价）。

#### [!UICONTROL Bids]

**[!UICONTROL Bid]：**（可选）基于投放位置的广告的最大每次点击成本(CPC)或每千次可视展示成本(vCPM)，具体取决于促销活动竞价策略。 此值将覆盖广告组级别的竞价。

#### [!UICONTROL Tracking URLs]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/base-url-google-note.md}}

{{$include /help/_includes/tracking-template-google.md}}

>[!NOTE]
>
>新UI创建表单要求基本URL和跟踪模板（指定后）以`http://`或`https://`开头。

### 编辑投放位置时的设置 {#placement-edit-settings}

[!UICONTROL Edit Placements]面板支持一个或多个选定版面的以下设置。 您无法更改目标网站URL。

#### [!UICONTROL Placement Details]

**[!UICONTROL Status]：** *[!UICONTROL Active]*&#x200B;或&#x200B;*[!UICONTROL Paused]*。

#### [!UICONTROL Bid Details]

**[!UICONTROL Bid adjustment]：**&#x200B;如何更改竞价：

* *[!UICONTROL Set to]：*&#x200B;将现有竞价替换为指定值。

* *[!UICONTROL Increase]：*&#x200B;按指定的金额或百分比增加现有出价。

* *[!UICONTROL Decrease]：*&#x200B;按指定的金额或百分比减少现有出价。

**[!UICONTROL Modifier type]：** （对于增加或减少）调整使用&#x200B;*[!UICONTROL Currency]*&#x200B;还是&#x200B;*[!UICONTROL Percentage]*。

**[!UICONTROL Set value]：**&#x200B;新出价或调整金额。 最小值为0.01。

**[!UICONTROL Max limit]：** （用于增加或减少；可选）调整后竞价的限制。 对于增加，这是最高出价；对于减少，这是最低出价。 最小限制值为0.01。

当所选投放位置使用多种货币时，将禁用竞价编辑。

#### [!UICONTROL Tracking Urls]

**[!UICONTROL Base Url]**，**[!UICONTROL Tracking Template]：**&#x200B;对于每个字段，选择如何修改值：

* *[!UICONTROL Set To]：*&#x200B;替换该值。 输入以`http://`或`https://`开头的有效网站URL。

* *[!UICONTROL Find/Replace]：*&#x200B;替换值中的指定文本。 输入要查找的文本和替换文本。

* *[!UICONTROL Add Suffix]：*&#x200B;将文本附加到值。 输入后缀文本。

* *[!UICONTROL Add Prefix]：*&#x200B;在值的开头添加文本。 输入前缀文本。

>[!NOTE]
>
>所有新的基本URL必须是以`http://`或`https://`开头的有效URL。

>[!MORELIKETHIS]
>
>* [管理搜索竞价单位的约束](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [管理标签分类](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
