---
title: 管理购物产品组
description: 了解如何在购物营销活动中创建和管理购物产品组。
exl-id: cf818b87-ee4b-4cf5-a4e8-0b9a7fc32182
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# 管理购物产品组

仅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]购物营销活动*

您可以在[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups]视图中创建和编辑产品组，并删除产品组及其子产品组。

## 创建“[!UICONTROL All Products]”产品组

在创建具有特定属性的产品组之前，必须首先创建一个名为“[!UICONTROL All Products]”的全包式产品组。 每个广告组只能有一个“[!UICONTROL All Products]”组。

>[!TIP]
>
>若要同时创建多个帐户组件，请使用[营销活动批量处理工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]>[!UICONTROL Product Groups]**。

1. 在数据表上方的工具栏中，单击![创建](/help/search-social-commerce/assets/add.png "创建")。

1. 选择广告网络、帐户、营销活动和广告组，然后单击&#x200B;**[!UICONTROL Continue]**。

1. 指定[[!DNL Google Ads] 产品组设置](product-group-settings-google.md)或[[!DNL Microsoft Advertising] 产品组设置](product-group-settings-microsoft.md)。

1. 单击&#x200B;**[!UICONTROL Post]**。

## 在现有产品组中创建子产品组节点

在为广告组至少创建了一个包含所有内容的“[!UICONTROL All Products]”组后，您可以为要包含在投标中或从投标中排除的产品子集创建子产品组节点，其中一个或多个产品组在每个级别均以相同的属性为目标（例如，一个产品组为[!UICONTROL Brand]=Acme，而另一个产品组在同一级别为[!UICONTROL Brand]=AcmePlus）。 您最多可以创建七个级别的子产品组节点，不包括“[!UICONTROL All Products]”。

>[!NOTE]
>
>您无法为“[!UICONTROL Everything Else]”产品组创建子产品组。

>[!TIP]
>
>若要同时创建多个帐户组件，请使用[营销活动批量处理工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]>[!UICONTROL Product Groups]**。

1. （可选）要在树视图中查看产品组及其子产品组节点，请将光标悬停在产品组名称上，单击![菜单图标](/help/search-social-commerce/assets/arrow-dropdown-menu.png "菜单图标")，然后选择&#x200B;**[!UICONTROL Tree View]**。

1. 将光标悬停在产品组名称上，单击![箭头下拉菜单](/help/search-social-commerce/assets/arrow-dropdown-menu.png "箭头下拉菜单")，然后选择&#x200B;**[!UICONTROL + Add Node]**。

1. 指定[[!DNL Google Ads] 产品组设置](product-group-settings-google.md)或[[!DNL Microsoft Advertising] 产品组设置](product-group-settings-microsoft.md)，包括产品维度和属性。

1. 单击&#x200B;**[!UICONTROL Post]**。

## 编辑产品组节点设置

您可以编辑广告组中包含的单位产品组节点（不含子产品组节点的产品组）的竞价和跟踪模板。 不能编辑排除的部件产品组或已包括或已排除的分区节点的任何信息，这些子分区节点是具有子产品组节点的产品组。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]>[!UICONTROL Product Groups]**。

1. （可选）要在树视图中查看产品组及其子产品组节点，请将光标悬停在产品组名称上，单击![菜单图标](/help/search-social-commerce/assets/arrow-dropdown-menu.png "菜单图标")，然后选择&#x200B;**[!UICONTROL Tree View]**。

1. 执行以下任一操作：

   1. （要编辑单个产品组节点的设置）将光标悬停在产品组名称上，单击![菜单图标](/help/search-social-commerce/assets/arrow-dropdown-menu.png "菜单图标")，然后选择&#x200B;**[!UICONTROL + Edit Node]**。

   1. （要编辑一个或多个广告组的设置），请执行以下操作：

      1. 选中每个节点旁边的复选框。

         有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

      1. 在数据表上方的工具栏中，单击![编辑](/help/search-social-commerce/assets/edit.png "编辑")。

1. 编辑[[!DNL Google Ads] 产品组设置](product-group-settings-google.md)或[[!DNL Microsoft Advertising] 产品组设置](product-group-settings-microsoft.md)。

   对于多个节点，您的更改将应用于所有选定的节点。 对于[!UICONTROL Bid]字段，您可以选择将现有值更改为指定值，或者增加或减少金额指定百分比或货币金额，但有限制。 对于[!UICONTROL Tracking Template]字段，您可以将现有值更改为指定值，将现有字符串替换为指定字符串，将指定前缀添加到每个值的开头，或者在每个值的末尾附加后缀。

1. （可选）单击&#x200B;**[!UICONTROL Additional Details]**，并选择性地输入项目名称和描述。

1. 单击&#x200B;**[!UICONTROL Post]**。

## 删除产品组节点

您可以删除任何产品组（当其他产品组位于同一级别时，除外“其他所有产品”组），该组用于确定您的商户中心帐户中的哪些产品包含在广告组的购物广告中。 删除产品组将删除所有子产品组。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]>[!UICONTROL Product Groups]**。

1. （可选）筛选列表以包含特定的产品组。

1. 执行以下任一操作：

   * 要删除一个产品组，请单击&#x200B;**[!UICONTROL Status]**&#x200B;列并选择&#x200B;**[!UICONTROL Delete]**。

   * 要删除一个或多个产品组，请执行以下操作：

      1. 选中要删除的每个产品组旁边的复选框。

         有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

      1. 在工具栏中，单击![更多](/help/search-social-commerce/assets/more.png "更多")并选择&#x200B;**[!UICONTROL Delete]**。

      1. 在确认消息中，单击&#x200B;**[!UICONTROL Delete]**。

>[!MORELIKETHIS]
>
>* [关于购物产品组](product-group-about.md)
>* [[!DNL Google Ads] 产品组设置](product-group-settings-google.md)
>* [[!DNL Microsoft Advertising] 产品组设置](product-group-settings-microsoft.md)
