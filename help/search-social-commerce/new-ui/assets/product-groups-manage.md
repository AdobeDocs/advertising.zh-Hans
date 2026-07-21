---
title: 管理购物产品组
description: 了解、创建、编辑和删除购物产品组，并引用Google Ads和Microsoft Advertising的产品组设置。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: c074f430583e2d320eb4d47b4fc956c1822bd04a
workflow-type: tm+mt
source-wordcount: 2337
ht-degree: 0%

---


# 管理购物产品组

仅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]购物营销活动*

您可以在[!UICONTROL Product Groups]视图中（位于[!UICONTROL Assets] > [!UICONTROL Shopping]）创建和管理产品组。

您可以在[的[!UICONTROL Product Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/product-group-report.md)中查看有关产品组的数据。

## 什么是产品组？

在购物营销活动中，您的产品组（而非关键词）决定了商户中心帐户中要显示购物广告的产品。 每个产品组都基于单个产品属性（如类别、产品类型、品牌、条件、产品ID或自定义标签），并对所有匹配产品使用相同的竞价。 您可以包含或排除每个组中产品的竞价。

您可以在广告组级别配置产品组，以确定商户中心帐户中的哪些产品出现在广告组的购物广告中。 即使广告组不包含广告实体，广告网络仍会显示产品的广告。

当同一产品包含在多个促销活动中时，广告网络首先使用促销活动优先级来确定哪个促销活动（及相关竞价）适用于广告拍卖。 如果所有促销活动具有相同的优先级，则具有最高竞价的促销活动符合条件。

有关[!DNL Google]购物营销活动和广告的更多信息，请参阅[实施 [!DNL Google Ads] 购物营销活动](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)和[Google广告文档](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&rd=1)。 有关[!DNL Microsoft]购物营销活动的详细信息，请参阅[实施 [!DNL Microsoft Advertising] 购物营销活动](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)和[[!DNL Microsoft Advertising] 文档](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500)。

>[!NOTE]
>
>不支持在效果最佳的营销活动中列出[!DNL Google Ads]个组。 要管理和查看列表组的数据，请使用[!DNL Google Ads]编辑器。

### 产品组层次结构

在为广告组创建具有特定属性的产品组之前，必须首先创建一个名为“[!UICONTROL All Products]”的全包式产品组。 从此父产品组，您可以为产品子集创建子产品组，也可以从子产品组创建孙子级。 为广告组创建第一个子产品组后，将自动使用默认广告组竞价创建另一个名为“[!UICONTROL Everything Else]”的产品组。 当您添加更多产品组时，“[!UICONTROL Everything Else]”组会相应地进行调整，使其构成所有不在其他产品组中的产品。

在广告组内，您可以创建最多七个级别的产品组（不包括“[!UICONTROL All Products]”）以包含或排除投标，其中一个或多个产品组在每个级别中针对相同的属性（例如，一个产品组为[!UICONTROL Brand]=Acme，另一个产品组在同一级别为[!UICONTROL Brand]=AcmePlus）。 父产品组称为细分，最低细分级别称为单位。 您可以在设备级别设置竞价和跟踪模板，或完全排除竞价。 广告组的整个活动产品组集将按层次应用，以确定符合条件的产品。 例如，如果将[!UICONTROL All Products]细分为[!UICONTROL Brand]=AcmeBasic和[!UICONTROL Brand]=AcmePlus，然后进一步将每个产品组细分为[!UICONTROL Condition]=New和设置竞价，则只能广告或排除具有AcmeBasic和AcmePlus品牌的新产品。

![产品组集示例](/help/search-social-commerce/assets/product-group-list-new.png "产品组集示例")

![产品组层次结构示例](/help/search-social-commerce/assets/product-group-tree-new.png "产品组层次结构示例")

### 产品过滤器 {#product-filters}

<!-- I should be able to point to help in GGL and MS -->

另请参阅[!DNL Google Ads]帮助“[通过产品组管理购物营销活动](https://support.google.com/google-ads/answer/6275317)”和[!DNL Microsoft Advertising]帮助“[了解和使用产品组](https://help.ads.microsoft.com/#apex/bae/en/56782)”。

| 购物网络 | 产品Dimension | 属性 | 注释 |
|----|----|----|----|
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads]：[!UICONTROL Category=]<br><br>Microsoft：[!UICONTROL Category 1=]至[!UICONTROL Category 5=] | \[类别ID] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Brand=] | \[品牌\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Item ID=] | \[项目ID\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Condition] | [!UICONTROL New], [!UICONTROL Used], [!UICONTROL Refurbished], [!UICONTROL Unknown] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads]：[!UICONTROL Product Type (1st level)=]到[!UICONTROL Product Type (5th level)=]<br><br>[!DNL Microsoft]：[!UICONTROL Product Type=] | \[产品类型\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Custom Label 0=]至[!UICONTROL Custom Label 4=] | \[自定义标签的属性\] | — |
| [!DNL Google Ads] | 渠道= | [!UICONTROL Local], [!UICONTROL Online] | 要仅显示本地产品或在线产品的广告。<br><br><b>注意：</b>要为本地产品创建广告，必须启用“本地库存广告”选项，并且必须通过[!DNL Google Merchant Center]参与本地购物计划。 |
| [!DNL Google Ads] | [!UICONTROL ChannelExclusivity=] | [!UICONTROL SingleChannel], [!UICONTROL MultiChannel] | 是显示仅可用于单个渠道（仅本地或仅联机）的产品广告，还是可用于多个渠道（本地和联机）的产品广告。 |

## [!UICONTROL Product Groups]视图

位于[!UICONTROL Assets] > [!UICONTROL Shopping]视图的[!UICONTROL Product Groups]视图列出了所选广告商帐户的筛选视图中的所有产品组。 您还可以创建和管理产品组。

### 可用操作<!-- Go through all -->

* [创建“[!UICONTROL All Products]”产品组](#product-group-create-all-products)

* [在现有产品组中创建子产品组节点](#node-add)

* 编辑产品组节点的设置：

  * [编辑任何设置](#node-edit)

  * [仅编辑[!UICONTROL Tracking Template]](#node-edit-tracking-template)

  * [仅编辑[!UICONTROL Max CPC]](#node-edit-maxcpc)

* [删除产品组节点](#node-delete)

* [将约束](#constraint-assign)分配给产品组，并[从产品组中删除约束](#constraint-unassign)

* [将标签分类](#classification-values-assign)分配给产品组，并[从产品组中删除标签分类](#classification-values-remove)

>[!NOTE]
>
>您可以通过上传[批量工作表文件](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)并将它们发布到广告网络，一次性创建和编辑大量产品组数据（包括标签和限制分配）。

## 创建“[!UICONTROL All Products]”产品组 {#product-group-create-all-products}

在创建具有特定属性的产品组之前，必须首先创建一个名为“[!UICONTROL All Products]”的全包式产品组。 每个广告组只能有一个“[!UICONTROL All Products]”组。

>[!TIP]
>
>若要同时创建多个帐户组件，请使用[营销活动批量处理工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Create Product Group]**。

1. 选择广告网络、帐户、营销活动和广告组，然后单击&#x200B;**[!UICONTROL Continue]**。

1. 指定[Google广告产品组设置](#google-ads-product-group-settings)或[Microsoft Advertising产品组设置](#microsoft-advertising-product-group-settings)。

1. 单击&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，请单击![编辑](/help/search-social-commerce/assets/edit-new.png "编辑")并更改[Google广告产品组设置](#google-ads-product-group-settings)或[Microsoft Advertising产品组设置](#microsoft-advertising-product-group-settings)。

1. 单击&#x200B;**[!UICONTROL Create]**。

## 在现有产品组中创建子产品组节点 {#product-group-create-child}

在为广告组至少创建了一个包含所有内容的“[!UICONTROL All Products]”组后，您可以为要包含在投标中或从投标中排除的产品子集创建子产品组节点，其中一个或多个产品组在每个级别均以相同的属性为目标（例如，一个产品组为[!UICONTROL Brand]=Acme，而另一个产品组在同一级别为[!UICONTROL Brand]=AcmePlus）。 您最多可以创建七个级别的子产品组节点，不包括“[!UICONTROL All Products]”。

>[!NOTE]
>
>您无法为“[!UICONTROL Everything Else]”产品组创建子产品组。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. （可选）要在树视图中查看产品组及其子产品组节点，请将光标悬停在产品组名称上，然后单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Tree View]**。

1. 将光标悬停在产品组名称上，然后单击&#x200B;**[!UICONTROL ...]>[!UICONTROL + Add Node]**。

1. 指定[Google广告产品组设置](#google-ads-product-group-settings)或[Microsoft Advertising产品组设置](#microsoft-advertising-product-group-settings)。

1. 单击&#x200B;**[!UICONTROL Center]**。

## 编辑产品组节点的任何设置 {#node-edit}

您可以编辑广告组中包含的单位产品组节点（不含子产品组节点的产品组）的竞价和跟踪模板。 不能编辑排除的部件产品组或已包括或已排除的分区节点的任何信息，这些子分区节点是具有子产品组节点的产品组。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. （可选）要在树视图中查看产品组及其子产品组节点，请将光标悬停在产品组名称上，然后单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Tree View]**。

1. 将光标悬停在产品组名称上，然后单击&#x200B;**[!UICONTROL ...]>[!UICONTROL + Edit Node]**。

1. 编辑[Google广告产品组设置](#google-ads-product-group-settings)或[Microsoft Advertising产品组设置](#microsoft-advertising-product-group-settings)。

1. 单击&#x200B;**[!UICONTROL Update]**。

## 仅编辑产品组节点的[!UICONTROL Tracking Template] {#node-edit-tracking-template}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. 将光标悬停在产品组名称上，然后单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Tree View]**&#x200B;以在树视图中查看产品组及其子产品组节点。

1. 在&#x200B;**[!UICONTROL Tracking Template]**&#x200B;列中，单击![编辑](/help/search-social-commerce/assets/edit-new.png "编辑")。

1. 更改&#x200B;**[!UICONTROL Tracking Template]**&#x200B;值，然后单击&#x200B;**[!UICONTROL Save]**。

## 仅编辑产品组节点的[!UICONTROL Max CPC] {#node-edit-maxcpc}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. 将光标悬停在产品组名称上，然后单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Tree View]**&#x200B;以在树视图中查看产品组及其子产品组节点。

1. 在&#x200B;**[!UICONTROL Max CPC]**&#x200B;列中，单击![编辑](/help/search-social-commerce/assets/edit-new.png "编辑")。

1. 更改&#x200B;**[!UICONTROL Max CPC]**&#x200B;值，然后单击&#x200B;**[!UICONTROL Save]**。

## 删除产品组节点 {#node-delete}

您可以删除任何产品组（当其他产品组位于同一级别时，除外“其他所有产品”组），该组用于确定您的商户中心帐户中的哪些产品包含在广告组的购物广告中。 删除产品组将删除所有子产品组。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. 将光标悬停在产品组名称上，然后单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Tree View]**&#x200B;以在树视图中查看产品组及其子产品组节点。

1. 单击&#x200B;**[!UICONTROL Status]**&#x200B;列并选择&#x200B;**[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Delete]**。

## 将限制分配给所选产品组 {#constraint-assign}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. 选中要为其分配单个约束的每个产品组旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**。

1. 选择约束。

1. 单击&#x200B;**[!UICONTROL Assign Now]**。

## 从所选产品组删除约束 {#constraint-unassign}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. 选中要从中取消分配约束的每个产品组旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 单击&#x200B;**[!UICONTROL Confirm]**。

## 将分类值分配给产品组 {#classification-values-assign}

>[!NOTE]
>
>标签值由子实体继承，因此除非要覆盖继承的值，否则不要为子实体输入值。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. 选中要为其分配标签值的每个产品组旁边的复选框。

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

## 从产品组中删除标签分类值 {#classification-values-remove}

删除分类值将删除与帐户组件及其所有子组件的关联。 分类值的报表数据不再可用于这些组件。 删除分类值不会删除该值，也不会删除帐户组件。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Assets]>[!UICONTROL Shopping]**。

1. 选中将从中删除标签值的每个产品组旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**。

1. 选中要从所选实体中移除的每个分类值旁边的复选框。

   要选择所有分配的值，请单击&#x200B;**[!UICONTROL Select All]**。 要取消选择所有分配的值，请单击&#x200B;**[!UICONTROL Deselect All]**。

1. 单击&#x200B;**[!UICONTROL Unassign Selected]**。

## [!DNL Google Ads]产品组设置 {#google-ads-product-group-settings}

### “所有产品”产品组

**[!UICONTROL Network]：** （仅限新产品组）广告网络。

**[!UICONTROL Account]：** （仅限新产品组）广告网络帐户名称。

**[!UICONTROL Campaign]：** （仅限新产品组）营销活动。

**[!UICONTROL Ad Group]：**（仅限新产品组）广告组。

**[!UICONTROL Condition]**&#x200B;或&#x200B;**[!UICONTROL Condition Type]：** （只读）所有产品

**[!UICONTROL Condition Value]：** （仅限现有产品组）  

**[!UICONTROL Bid]**&#x200B;或&#x200B;**[!UICONTROL Max CPC]：**（仅包括产品组）每次点击的最大成本(CPC)，这是为广告点击支付的最高金额。 此值仅用于没有子产品组的单位，而不用于广告组级别值。

{{$include /help/_includes/tracking-template-google.md}}

此模板将覆盖更高级别的模板，并且仅用于没有子产品组的设备。 不包括为帐户或营销活动指定的任何附加参数。 不包括为帐户或营销活动指定的任何附加参数。

### 所有其他产品组

**[!UICONTROL Condition Type]**&#x200B;和&#x200B;**[!UICONTROL Condition Value]：** （现有产品组的只读）要定位的产品维度。 对于新产品组，输入要作为目标产品的维度和选定信息类别的资格属性（例如，按品牌定位时为“Acme”，按条件定位时为“New”）。

为特定产品维度（即，不是“所有产品”）创建产品组后，Search、Social和Commerce会自动为“其他所有产品”创建产品组。

有关可用产品维度的列表，请参阅“[产品筛选器](#product-filters)”。 根据营销活动的[!UICONTROL Inventory Filter]设置，您的维度列表可能会受到限制。

**[!UICONTROL Excluded]：** （对于新产品组为可选；对于现有产品组为只读）排除匹配产品的广告投标。

**[!UICONTROL Max CPC]：**（仅限包含的产品组）每次点击的最大成本(CPC)，这是为广告点击支付的最高金额。 此值仅用于没有子产品组的单位，而不用于广告组级别值。

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-google.md}}
-->

{{tracking-template-google}}

此模板将覆盖更高级别的模板，并且仅用于没有子产品组的设备。

## [!DNL Microsoft Advertising]产品组设置 {#microsoft-advertising-product-group-settings}

### “所有产品”产品组

**[!UICONTROL Network]：** （仅限新产品组）广告网络。

**[!UICONTROL Account]：** （仅限新产品组）广告网络帐户名称。

**[!UICONTROL Campaign]：** （仅限新产品组）营销活动。

**[!UICONTROL Ad Group]：**（仅限新产品组）广告组。

**[!UICONTROL Condition]**&#x200B;或&#x200B;**[!UICONTROL Condition Type]：** （只读）所有产品

**[!UICONTROL Condition Value]：** （仅限现有产品组）  

**[!UICONTROL Bid]**&#x200B;或&#x200B;**[!UICONTROL Max CPC]：**（仅包括产品组）每次点击的最大成本(CPC)，这是为广告点击支付的最高金额。 此值仅用于没有子产品组的单位，而不用于广告组级别值。

**[!UICONTROL Base URL]：** （仅限新产品组）未使用<!-- Not sure this is supposed to be there; it's not showing for an existing product group: {{$include /help/_includes/base-url-keyword-ad-sitelink.md}} -->

{{$include /help/_includes/tracking-template-microsoft.md}}

此模板将覆盖更高级别的模板，并且仅用于没有子产品组的设备。

### 所有其他产品组

**[!UICONTROL Condition Type]**&#x200B;和&#x200B;**[!UICONTROL Condition Value]：** （现有产品组的只读）要定位的产品维度。 对于新产品组，输入要作为目标产品的维度和选定信息类别的资格属性（例如，按品牌定位时为“Acme”，按条件定位时为“New”）。

为特定产品维度（即，不是“所有产品”）创建产品组后，Search、Social和Commerce会自动为“其他所有产品”创建产品组。

有关可用产品维度的列表，请参阅“[产品筛选器](#product-filters)”。 根据营销活动的[!UICONTROL Inventory Filter]设置，您的维度列表可能会受到限制。

**[!UICONTROL Excluded]：** （对于新产品组为可选；对于现有产品组为只读）排除匹配产品的广告投标。

**[!UICONTROL Max CPC]：**（仅限包含的产品组）每次点击的最大成本(CPC)，这是为广告点击支付的最高金额。 此值仅用于没有子产品组的单位，而不用于广告组级别值。

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

此模板将覆盖更高级别的模板，并且仅用于没有子产品组的设备。

>[!MORELIKETHIS]
>
>* [实施 [!DNL Google Ads] 购物营销活动](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
>* [实施 [!DNL Microsoft Advertising] 购物营销活动](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
>* [该[!UICONTROL Product Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/product-group-report.md)
