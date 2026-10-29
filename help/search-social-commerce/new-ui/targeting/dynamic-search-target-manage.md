---
title: 管理[!DNL Google Ads]动态搜索目标
description: 了解如何创建和管理[!DNL Google Ads]动态搜索目标。
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/MsSy-p-WSroc3FyiHx6kvcTohEaWOqJCzqbl91mNwK0'
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
source-git-commit: f907f445c70ce64368dfa7e77d4cd1900ecc7113
workflow-type: tm+mt
source-wordcount: '1504'
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

## [!UICONTROL Auto Targets]视图 {#auto-target-view-about}

[!UICONTROL Targeting] > [!UICONTROL Auto Targets]视图列出了所选广告商帐户的筛选视图中的所有动态搜索目标。 您还可以管理动态搜索目标。

查看数据需要[!UICONTROL View Auto Targets]权限。 创建目标并编辑其竞价或状态需要[!UICONTROL Edit Auto Targets]权限。

### 可用操作

* [创建动态搜索目标](#auto-target-create)

* [编辑动态搜索目标的设置](#auto-target-edit)

* [更改动态搜索目标的状态或删除动态搜索目标](#auto-target-status)

* [将选定行中的所有数据复制到剪贴板](#copy-to-clipboard)

* [将约束](#constraint-assign)分配给动态搜索目标，并[从动态搜索目标中移除约束](#constraint-unassign)

* [将标签分类](#classification-values-assign)分配给动态搜索目标，并[从动态搜索目标中删除标签分类](#classification-values-remove)

>[!NOTE]
>
>您可以通过上传[批量工作表文件](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)并将它们发布到广告网络，同时创建和编辑大量目标数据（包括标签和限制分配）。

## 创建[!DNL Google Ads]动态搜索目标 {#auto-target-create}

您可以创建动态搜索目标来定义网站中的页面（即广告显示URL中使用的域），这些页面的内容用于定位同一广告组中的动态搜索广告。

您可以定位所有索引页面，或者指定最多三个条件。

>[!NOTE]
>
>要最佳跟踪性能，请使用[!UICONTROL All]选项为每个营销活动仅创建一个广告组的目标。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**。

1. 在数据表上方，单击&#x200B;**[!UICONTROL Create Auto Target]**。

1. 在&#x200B;**[!UICONTROL Basic Settings]**&#x200B;中，选择广告网络、帐户、营销活动和广告组。

1. 指定剩余的[动态搜索目标设置](#auto-target-create-settings)。

1. 单击&#x200B;**[!UICONTROL Review and Save]**。

1. 查看设置。 要更改任何设置，请在适用的部分中单击![编辑](/help/search-social-commerce/assets/edit-new.png "编辑") **[!UICONTROL Edit]**&#x200B;并更改设置。

1. 单击&#x200B;**[!UICONTROL Create]**。

## 编辑[!DNL Google Ads]动态搜索目标设置 {#auto-target-edit}

您可以编辑一个或多个动态搜索目标的状态或最高竞价。 您无法更改已定位的标准。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**。

1. 选中要编辑的每一行旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Edit]**。

1. 在&#x200B;**[!UICONTROL Edit Auto Targets]**&#x200B;面板中，编辑[状态和竞价设置](#auto-target-edit-settings)。

   您的更改将应用于所有选定的目标。 未更改的设置将保留其现有值。

   当所选目标使用多种货币时，将禁用竞价编辑。 您仍然可以更改其状态。

1. 单击&#x200B;**[!UICONTROL Save]**。

您还可以通过单击单个目标的竞价值，直接在数据表中编辑该目标的竞价。

## 更改[!DNL Google Ads]动态搜索目标的状态或将其删除 {#auto-target-status}

您可以暂停活动的动态搜索目标，以停止将其用于同一广告组中的动态搜索广告。 您可以稍后通过将目标的状态更改回“活动”来恢复使用该目标。 您还可以删除动态搜索目标。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**。

1. （可选）筛选列表以包含特定的动态搜索目标。

1. 执行以下任一操作：

   * 要更改某个目标的状态，请单击&#x200B;**[!UICONTROL Status]**&#x200B;列中的该目标的值，然后选择&#x200B;**[!UICONTROL Active]**&#x200B;或&#x200B;**[!UICONTROL Paused]**。

   * 要更改多个目标的状态，请选中每个目标旁边的复选框，单击批量操作工具栏中的&#x200B;**[!UICONTROL Edit]**，在&#x200B;**[!UICONTROL Edit Auto Targets]**&#x200B;面板中选择&#x200B;**[!UICONTROL Status]**，然后单击&#x200B;**[!UICONTROL Save]**。

   * 要删除一个或多个目标，请选中每个目标旁边的复选框，单击批量操作工具栏中的&#x200B;**[!UICONTROL ...]>[!UICONTROL Delete]**，然后单击确认消息中的&#x200B;**[!UICONTROL Confirm]**。

## 将选定行中的所有数据复制到剪贴板 {#copy-to-clipboard}

根据应用的筛选条件和视图中可见的列，复制选定行中的可见信息。 信息将另存为制表符分隔值(TSV)。

1. 选中要复制其数据的每一行旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Copy]**。

## 管理动态搜索目标的约束分配 {#constraints}

### 为动态搜索目标分配约束 {#constraint-assign}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**。

1. 选中要为其分配单个约束的每个动态搜索目标旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Bid Constraint]**。

1. 选择约束。

1. 单击&#x200B;**[!UICONTROL Assign Now]**。

### 从所选动态搜索目标中移除约束 {#constraint-unassign}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**。

1. 选中要从中取消分配约束的每个动态搜索目标旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Bid Constraint]**。

1. 单击&#x200B;**[!UICONTROL Confirm]**。

## 管理动态搜索目标的分类值 {#classification-values}

### 将分类值分配给动态搜索目标 {#classification-values-assign}

>[!NOTE]
>
>标签值由子实体继承，因此，除非要覆盖继承的值，否则不要为动态搜索目标输入值。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**。

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

### 从动态搜索目标中删除标签分类值 {#classification-values-remove}

删除分类值将删除与帐户组件及其所有子组件的关联。 分类值的报表数据不再可用于这些组件。 删除分类值不会删除该值，也不会删除帐户组件。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**。

1. 选中将从中删除标签值的每个动态搜索目标旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**。

1. 选中要从所选实体中移除的每个分类值旁边的复选框。

   要选择所有分配的值，请单击&#x200B;**[!UICONTROL Select All]**。 要取消选择所有分配的值，请单击&#x200B;**[!UICONTROL Deselect All]**。

1. 单击&#x200B;**[!UICONTROL Unassign Selected]**。

## [!DNL Google Ads]动态搜索目标设置 {#dynamic-search-target-settings}

### 创建过程中可用的设置 {#auto-target-create-settings}

#### [!UICONTROL Auto Target Details]

**自动定位：**&#x200B;内容用于定位广告组中的动态搜索广告的索引页面：

* *[!UICONTROL All]* （默认）：定位所有索引页。

* *[!UICONTROL Specific]：*&#x200B;定位匹配三个条件的页面。 选择条件并输入其值。 要添加另一个条件，请单击&#x200B;**[!UICONTROL And]**。 这些标准将与AND相结合，因此页面必须匹配所有指定的标准。 单击&#x200B;**[!UICONTROL Reset]**&#x200B;以清除条件。

  * *[!UICONTROL Category]：*&#x200B;页面的[!DNL Google Ads]内容类别等于指定的值。 输入一个值。

  * *[!UICONTROL URL]：*&#x200B;页面的URL包含指定的值，如`shoes.example.com`。 请输入有效的URL。

  * *[!UICONTROL Page Title]：*&#x200B;页面标题包含指定的文本。 输入一个值。

  * *[!UICONTROL Page Content]：*&#x200B;页面内容包含指定的文本。 输入一个值。

创建目标后无法更改目标标准。

**[!UICONTROL Status]：**&#x200B;目标的状态：

* *[!UICONTROL Active]* （默认）：启用竞价。

* *[!UICONTROL Paused]：*&#x200B;禁用竞价。

**[!UICONTROL Bid]：**&#x200B;目标的最大每次点击成本(CPC)。 此值将覆盖广告组级别的竞价。 该字段是可选的；在输入竞价时，最小值为0.01（以帐户币种表示）。

>[!NOTE]
>
>如果目标在优化的产品组合中，则应用指定的CPC竞价一天。 之后，优化功能根据自己的计算来设置投标。

### 编辑过程中可用的设置 {#auto-target-edit-settings}

#### [!UICONTROL Auto Target Details]

**[!UICONTROL Status]：**&#x200B;选择&#x200B;**[!UICONTROL Active]**&#x200B;或&#x200B;**[!UICONTROL Paused]**。

#### [!UICONTROL Bid details]

当所选目标使用多种货币时，将禁用竞价编辑。

**[!UICONTROL Bid adjustment]：**&#x200B;如何更改最大竞价：

* *[!UICONTROL Set to]：*&#x200B;用[!UICONTROL Set value]中的金额替换每个出价。

* *[!UICONTROL Increase]：*&#x200B;在[!UICONTROL Set value]中按金额或百分比增加每个出价。

* *[!UICONTROL Decrease]：*&#x200B;按[!UICONTROL Set value]中的金额或百分比减少每个出价。

**[!UICONTROL Modifier type]：** （对于[!UICONTROL Increase]和[!UICONTROL Decrease]）选择&#x200B;**[!UICONTROL Currency]**&#x200B;或&#x200B;**[!UICONTROL Percentage]**。

**[!UICONTROL Set value]：**&#x200B;新出价，或者更改每个出价的金额或百分比。 最小值为0.01。

**[!UICONTROL Max limit]：** （可选，适用于[!UICONTROL Increase]和[!UICONTROL Decrease]）帐户币种的限制。 对于提高，这是生成的最大出价。 对于降低，这是生成的最低出价。 输入限制时，最小值为0.01。

>[!MORELIKETHIS]
>
>* [（新UI）管理搜索竞价单位的约束](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [（新UI）管理标签分类](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
