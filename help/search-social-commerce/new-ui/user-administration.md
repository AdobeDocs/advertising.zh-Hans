---
title: （新UI）用户管理
description: 了解如何管理用户访问权限。
feature: Search Introduction
exl-id: bfc43692-cfb6-468f-90df-a808a21a0c23
TQID: 'https://experienceleague.adobe.com/b28N5zmqqdZ6Yvg2swGLWv260fWsMUgjK2eW1DDn-uo'
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9c0e1d04187ee5f80d4b5899ab36833f202b16a
workflow-type: tm+mt
source-wordcount: 1082
ht-degree: 0%

---

# （新UI）搜索、社交和商务的用户管理

某些用户可以使用[Adobe Admin Console](https://helpx.adobe.com/enterprise/using/admin-console.html)管理对新的“搜索、社交和Commerce”用户界面的访问权限，该位置是管理所有Adobe权限和用户管理的中心位置。 用户分为最终用户和管理员。 如果您是管理员，您的Adobe客户团队会通知您。 如果您是管理员，请参阅以下部分以确定管理用户的权限和工作流。

## 管理员类型

Admin Console提供多种类型的管理员。 搜索、社交和Commerce需要以下管理员类型和权限。 如果要委派用户管理任务，可以添加其他类型。

**系统管理员：**&#x200B;管理组织的所有产品（包括组织的所有客户端实例）的超级用户。 （客户端实例与旧版广告商帐户相同，每个组织ID具有一个或多个实例）。 系统管理员可以在Admin Console中为组织执行所有管理任务，也可以将管理功能委派给组织的任何产品的其他用户。

**产品管理员：**&#x200B;管理对特定[!DNL Adobe]产品（如Search、Social和Commerce）的访问权限以及该产品的用户权限。 产品管理员可以为产品创建产品配置文件，为产品创建（但不删除）用户和用户组，在产品配置文件中添加或删除用户和用户组，以及在产品中添加或删除其他产品管理员。

<!-- 
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## 默认产品配置文件

产品配置文件与角色类似，它为用户授予了使用特定产品的特定服务的权限。

搜索、社交和商务的新用户界面具有以下默认产品配置文件，这些配置文件提供不同的功能和服务子集。 您无法编辑默认产品配置文件的产品权限或删除默认产品配置文件。 但是，产品管理员、产品配置文件管理员和系统管理员可以根据需要创建和管理具有不同可用权限子集的其他产品配置文件。

* **[!UICONTROL Basic Optimization]：**&#x200B;适用于需要具有基本设置访问权限的标准项目组合管理和规划功能的用户。

* **[!UICONTROL Expert Optimization]：**&#x200B;适用于需要完整项目组合设置访问权限（包括高级专家级控制）的高级用户。 包括所有性能计划、目标、活动、设置和报表管理权限。

* **[!UICONTROL Read-Only Optimization]：**&#x200B;适用于需要了解项目组合、模拟和营销活动而无需编辑或创建功能的用户。

* **[!UICONTROL \[Optimization\] Admin]：**&#x200B;授予对所有可用功能的完全访问权限，并允许用户创建新的客户端实例（与旧版广告商帐户相同，每个组织ID具有一个或多个实例）。 除非您拥有适当的业务理由，否则不要将此权利分配给任何人。

### 每个产品配置文件的功能

<!-- These don't correspond exactly to the GUI menu -->

复选标记(✓)表示该权限包含在产品配置文件中。

**Portfolio管理**

| 权限 | 基本 | 专家 | 只读 | 管理员 |
|---|---|---|---|---|
| 查看项目组合 | ✓ | ✓ | ✓ | ✓ |
| 查看Portfolio设置 | ✓ | ✓ | ✓ | ✓ |
| 查看Portfolio性能详细信息 | ✓ | ✓ | ✓ | ✓ |
| 查看Portfolio组 | ✓ | ✓ | ✓ | ✓ |
| 编辑Portfolio组 | ✓ | ✓ | | ✓ |
| 编辑基本Portfolio设置 | ✓ | | | |
| 编辑Expert Portfolio设置 | | ✓ | | ✓ |

<!--
Noone has permissions as of 6/1; spelling [sic]:
| Edit Advance Portfolio Settings | | | | |
-->

**性能计划管理**

| 权限 | 基本 | 专家 | 只读 | 管理员 |
|---|---|---|---|---|
| 查看模拟 | ✓ | ✓ | ✓ | ✓ |
| 创建模拟 | ✓ | ✓ | | ✓ |
| 查看支出推荐 | | ✓ | | ✓ |
| 应用支出推荐 | | ✓ | | ✓ |

**目标管理**

| 权限 | 基本 | 专家 | 只读 | 管理员 |
|---|---|---|---|---|
| 查看目标 | ✓ | ✓ | ✓ | ✓ |
| 编辑目标 | ✓ | ✓ | | ✓ |
| 查看转化值规则 | ✓ | ✓ | ✓ | ✓ |
| 编辑转化值规则 | | ✓ | | ✓ |
| 查看转化 | | ✓ | | ✓ |
| 编辑转化 | | ✓ | | ✓ |
| 查看转化可见性 | | ✓ | | ✓ |

**促销活动管理**

| 权限 | 基本 | 专家 | 只读 | 管理员 |
|---|---|---|---|---|
| 查看营销活动 | ✓ | ✓ | ✓ | ✓ |
| 编辑营销活动 | ✓ | ✓ | | ✓ |
| 查看广告组 | ✓ | ✓ | ✓ | ✓ |
| 编辑广告组 | ✓ | ✓ | | ✓ |
| 广告视图 | ✓ | ✓ | ✓ | ✓ |
| 广告编辑 | | ✓ | | ✓ |
| 关键字视图 | ✓ | ✓ | ✓ | ✓ |
| 受众视图 | ✓ | ✓ | ✓ | ✓ |
| 自动定位视图 | ✓ | ✓ | ✓ | ✓ |
| 创意视图 | ✓ | ✓ | ✓ | ✓ |
| 扩展视图 | ✓ | ✓ | ✓ | ✓ |
| 标签分类视图 | ✓ | ✓ | ✓ | ✓ |
| 投放位置视图 | ✓ | ✓ | ✓ | ✓ |
| “推荐”视图 | ✓ | ✓ | ✓ | ✓ |
| 查看批量工作表 | | ✓ | | ✓ |
| 编辑批量工作表 | ✓ | ✓ | ✓ | ✓ |

**报告管理**

| 权限 | 基本 | 专家 | 只读 | 管理员 |
|---|---|---|---|---|
| 查看历史记录日志 | ✓ | ✓ | ✓ | ✓ |
| 查看计划报表 | ✓ | ✓ | ✓ | ✓ |
| 编辑计划报告 | | ✓ | | ✓ |

**安装程序管理**

| 权限 | 基本 | 专家 | 只读 | 管理员 |
|---|---|---|---|---|
| 查看帐户 | ✓ | ✓ | ✓ | ✓ |
| 编辑帐户 | | ✓ | | ✓ |
| 查看MCC帐户 | ✓ | ✓ | ✓ | ✓ |
| 编辑MCC帐户 | | ✓ | | ✓ |

## 管理员任务

### 登录到Adobe Admin Console，并将其打开到Search、Social和Commerce

>[!PREREQUISITES]
>
>您必须对Search、Social和Commerce具有某种类型的管理员访问权限才能登录到Admin Console。

1. 转到https://adminconsole.adobe.com/enterprise/ 。

1. （如果您未登录到CX Enterprise ）登录到CX Enterprise ：

   1. 输入您的[!DNL Adobe] ID，然后单击&#x200B;**[!UICONTROL Continue]**。

   1. 选择**[!UICONTROL Personal Account]”或&#x200B;**[!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. 选择适用的CX Enterprise组织。

      Admin Console将打开至[!UICONTROL Overview]选项卡。

   1. 在[!UICONTROL Product & services]下，单击“[!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name]”。

      产品页面将打开，以显示搜索、社交和Commerce的[!UICONTROL Product profiles]选项卡。 其他选项卡包括[!UICONTROL Users]和[!UICONTROL Product Admins]。

### 系统管理员的工作流

对于Search、Social和Commerce的每个客户端实例，请遵循此工作流。

1. [登录到Adobe Admin Console并将其打开以搜索、社交和Commerce](#open-admin-console)。

1. （可选） [添加其他系统管理员](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise)作为备份。

1. 通过[添加产品管理员](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise)来委派产品和用户管理。

### 面向产品管理员的工作流

对于Search、Social和Commerce的每个客户端实例，请遵循此工作流。

1. [登录到Adobe Admin Console并将其打开以搜索、社交和Commerce](#open-admin-console)。

1. 根据需要，批量创建最终用户[个别](https://helpx.adobe.com/enterprise/using/manage-users-individually.html)或[](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html)。

1. （可选）为实例创建[用户组](https://helpx.adobe.com/enterprise/using/user-groups.html)并将用户分配给每个用户组。

   如果实例具有多个用户，请创建用户组，以确保根据用户的专业技能级别为其分配正确的用户档案。 （请参阅步骤4 ，将用户组分配给产品配置文件。） 您可以根据业务线、用户访问需求、用户聘用日期或其他条件创建用户组。

   >[!IMPORTANT]
   >
   >用户组名称应明确传达用户组应分配的权限。 例如，如果要创建具有“只读”权限的用户组，请在用户组名称中包含“只读”，如“Acme_Uk_ReadOnly”或“Acme_ReadOnly”。

1. （可选） [使用定义的权限集创建自定义产品配置文件](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html)。

   除了四个可用的默认产品配置文件之外，还提供了自定义配置文件。

   组织的每个产品配置文件必须具有唯一的名称。 如果您的组织使用多个Search、Social和Commerce实例（例如，Acme_US和Acme_JP），则您无法在多个实例中复制产品配置文件名称。 **最佳实践：**&#x200B;使用命名约定`<Name>_<Instance>,`，如“Implements_Only_JP”。

   **警告：**&#x200B;产品权限非常细微。 配置自定义产品配置文件时要小心，否则可能会忽略要包含的功能。

1. [手动或批量将每个用户或用户组分配给相关的产品配置文件](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html)。

## 完整的用户管理指南和其他链接

* 有关使用Adobe Admin Console进行用户管理的更多信息，请参阅《[Adobe企业和团队管理指南](https://helpx.adobe.com/enterprise/admin-guide.html)》，包括[Admin Console概述](https://helpx.adobe.com/enterprise/using/admin-console.html)。

* Admin Console： [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
