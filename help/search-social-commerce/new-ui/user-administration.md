---
title: 用户管理
description: 了解如何。
feature: Search Introduction
source-git-commit: 5a4c608d8c8371c24cf220cc5eed9a39989dc850
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 0%

---

# （新UI）搜索、社交和商务的用户管理

某些用户可以使用Adobe Admin Console管理对新的“搜索、社交和Commerce”用户界面的访问，这是管理所有Adobe权利和用户管理的中心位置。 用户分为最终用户和管理员。 如果您是管理员，您的Adobe客户团队将通知您。 如果您是管理员，请参阅以下部分以确定管理用户的权限和工作流。<!-- How can you see what your user role is, or will your Adobe Account Team tell you? -->

## 相关类型的管理员

Admin Console提供多种类型的管理员，但只有以下管理员类型和权限与Search、Social和Commerce相关。

**系统管理员：**&#x200B;组织的超级用户。 系统管理员可以在Admin Console中为组织执行所有管理任务，还可以将管理功能委派给其他用户（产品管理员）。&lt;！— 、产品配置文件管理员和用户组管理员。   — 我想只有我们的产品管理员？  验证。—>

**产品管理员：**&#x200B;管理对特定[!DNL Adobe]产品(如Search、Social和Commerce)的访问权限及其用户对该产品的权利。 产品管理员可以为产品创建产品配置文件，创建（但不删除）用户和用户组，在产品配置文件中添加或删除用户和用户组，以及在产品中添加或删除其他产品管理员。

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## 默认产品配置文件

产品配置文件与角色类似，它为用户授予了使用特定产品的特定服务的权限。

搜索、社交和商务的新用户界面具有以下默认产品配置文件，这些配置文件提供不同的功能和服务子集。 您无法编辑或删除默认的产品配置文件。 但是，系统管理员可以根据需要创建和管理具有不同权限子集的其他产品配置文件。

* **基本优化：**&#x200B;此配置文件提供以下功能：

   * 目标：完全访问

   * 模拟：完全访问

   * Portfolio组：完全访问权限

   * 项目组合：创建/编辑对目标、营销活动和支出管理的项目组合设置的访问权限；对其余项目组合设置的只读访问权限。

   * 营销活动：对营销活动设置的只读访问权限（无创建、编辑或删除功能可用）；对限制和项目组合分配的完全访问权限<!-- Is that the correct wording? -->

   * 广告组：对广告组设置的只读访问权限（无创建、编辑或删除功能可用）；对约束和项目组合分配的完全访问权限<!-- Is that the correct wording? -->

  此访问级别是仍在学习使用Search、Social和Commerce的用户的首选。

* **专家优化：**&#x200B;此配置文件提供以下功能：

   * 目标：完全访问

   * 模拟：完全访问

   * Portfolio组：完全访问权限

   * 项目组合：完全访问

   * 营销活动：对营销活动列表的只读访问权限（尚无营销活动创建、编辑或删除功能）；对限制和项目组合分配的完全访问权限<!-- Is that the correct wording? -->

   * 广告组：对广告组列表的只读访问权限（尚无营销活动创建、编辑或删除功能可用）；对限制和项目组合分配的完全访问权限<!-- Is that the correct wording? -->

  此访问级别建议搜索、社交和Commerce的专家用户使用。

* **只读：**&#x200B;此配置文件提供了以下功能：

   * 目标：只读访问权限

   * 模拟：只读访问

   * Portfolio组：只读访问权限

   * 项目组合：只读访问权限

   * 营销活动：只读访问权限

   * 广告组：只读访问权限

* **管理员：**&#x200B;此配置文件授予对所有可用功能的完全访问权限，并允许用户创建新的客户端实例。 除非您拥有适当的业务理由，否则不要将此权利分配给任何人。

<!-- Do I need to include this? If so, adjust wording as needed

## Product-specific instances

 -->

## 管理员任务

### 登录到Adobe Admin Console，并将其打开到Search、Social和Commerce

>[!PREREQUISITES]
>
>您必须具有管理员访问权限&lt;！哪一种？ 产品管理员、系统管理员，但我确定还有产品配置文件管理员或用户组管理员（可能是内部组 — 请选中） — >转至Search、Social和Commerce。

1. 转到https://adminconsole.adobe.com/enterprise/ 。

1. (如果您未登录到Experience Cloud)登录到Experience Cloud：

   1. 输入您的[!DNL Adobe] ID，然后单击&#x200B;**[!UICONTROL Continue]**。

   1. 选择&#x200B;**[!UICONTROL Personal Account]”或&#x200B;**&#x200B;[!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. 选择适用的Experience Cloud组织。

   1. 在产品和服务下，单击“[!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name]”。

   默认情况下，产品页面会打开搜索、社交和Commerce的[!UICONTROL Product profiles]选项卡。 其他选项卡包括[!UICONTROL Users]和[!UICONTROL Product Admins]。

### 系统管理员的工作流

1. [登录到Adobe Admin Console并将其打开以搜索、社交和Commerce](#open-admin-console)。

1. 通过[添加产品管理员](https://helpx.adobe.com/cn/enterprise/using/admin-roles.html#enterprise)来委派产品和用户管理。

<!-- what else? -->

### 面向产品管理员的工作流

1. [登录到Adobe Admin Console并将其打开以搜索、社交和Commerce](#open-admin-console)。

1. 根据需要，批量创建最终用户[个别](https://helpx.adobe.com/cn/enterprise/using/manage-users-individually.html)或[&#128279;](https://helpx.adobe.com/cn/enterprise/using/bulk-upload-users.html)。

1. （可选）为每个产品实例创建[用户组](https://helpx.adobe.com/cn/enterprise/using/user-groups.html)，并将用户分配给每个用户组。

   如果实例具有多个用户，请创建用户组，以确保根据用户的专业技能级别为其分配正确的用户档案。 （请参阅步骤4 ，将用户组分配给产品配置文件。） 您可以根据业务线、用户访问需求、用户聘用日期或其他条件创建用户组。

   >[!IMPORTANT]
   >
   >用户组名称应明确传达用户组应分配的权限。 例如，如果要创建具有“只读”权限的用户组，请在用户组名称中包含“只读”，如“Acme_Uk_ReadOnly”或“Acme_ReadOnly”。

1. （可选） [使用定义的权限集创建自定义产品配置文件](https://helpx.adobe.com/cn/enterprise/using/manage-product-profiles.html)。

   除了四个可用的默认产品配置文件之外，还提供了自定义配置文件。

   组织的每个产品配置文件必须具有唯一的名称。 如果您的组织使用多个Search、Social和Commerce实例（例如，Acme_US和Acme_JP），则您无法在多个实例中复制产品配置文件名称。 **最佳实践：**&#x200B;使用命名约定`<Name>_<Instance>,`，如“Implements_Only_JP”。

1. [手动或批量将每个用户或用户组分配给相关的产品配置文件](https://helpx.adobe.com/cn/enterprise/using/manage-product-profiles.html)。

## 完整的用户管理指南和其他链接

* 有关使用Adobe Admin Console进行用户管理的更多信息，请参阅《[Adobe企业和团队管理指南](https://helpx.adobe.com/cn/enterprise/admin-guide.html)》，包括[Admin Console概述](https://helpx.adobe.com/cn/enterprise/using/admin-console.html)。

* Admin Console： [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
