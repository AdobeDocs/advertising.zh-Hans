---
title: 管理 [!DNL Google Ads] 投放位置
description: 了解如何创建和管理可竞价投放 [!DNL Google Ads] 广告组。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# 管理 [!DNL Google Ads] 投放位置

*[!DNL Google Ads]仅限帐户*

您可以在中创建和编辑广告组的版面 [支持的营销活动类型](/help/search-social-commerce/introduction/supported-inventory.md) 以内的显示网络为目标 [已同步广告网络帐户](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)

## 创建 [!DNL Google Ads] 投放位置

>[!TIP]
>
>要同时创建多个投放位置，请使用 [营销活动批量处理工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Placements]**.

1. 
   1. 在数据表上方的工具栏中，单击 ![创建](/help/search-social-commerce/assets/add.png "创建").

1. 选择广告网络、帐户、营销活动和广告组，然后单击 **[!UICONTROL Continue]**.

1. 配置 [投放设置](#placement-settings).

1. 单击 **[!UICONTROL Post]**.

## 编辑 [!DNL Google Ads] 投放位置

>[!TIP]
>
>要一次编辑多个投放位置，请使用 [营销活动批量处理工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Keywords]**.

1. 选中要编辑的每一行旁边的复选框。

   有关选择多行的提示，请参阅&quot;[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).”

1. 在数据表上方的工具栏中，单击 ![编辑](/help/search-social-commerce/assets/edit.png "编辑") .

1. 编辑 [投放设置](#placement-settings).

   对于多个投放位置，您的更改将应用于所有选定的投放位置。 对于某些字母数字字段，您可以将现有值更改为指定值，将现有字符串替换为指定字符串，在每个值的开头添加指定前缀，或者在每个值的结尾附加后缀。 对于某些货币字段，您可以将现有值更改为指定值，或者按指定百分比或货币金额增加或减少金额（具有限制）。

1. 保存数据：

   * （单个投放位置）单击 **[!UICONTROL Post]**.

   * （多个投放位置）单击 **[!UICONTROL Post Now]**.

## 置入设置 {#placement-settings}

### [!UICONTROL Placement Details]

**[!UICONTROL Placements]：** 内容网络上可显示广告的站点。 输入有效的URL，如www.example.com、example.com或www.example.com/shoes/kids。 要指定多个字符串，请使用逗号分隔它们，或在分隔行中输入它们。URL不能包含问号(`?`)。 **注意：** 您可以 [排除网站投放位置](placement-negative-create.md) 从 [!UICONTROL Placements] > [!UICONTROL Negatives] 在广告组和营销活动设置中查看和。

**[!UICONTROL Status]：** 投放位置的显示状态： *活动* （启用竞价；默认）， *已暂停* （禁用竞价），或 *已删除* （删除投放位置；仅限现有投放位置）。

### [!UICONTROL Bids]

**[!UICONTROL Bid]：** （可选）基于投放位置的广告的最大每次点击成本(CPC)或每千次可视展示成本(vCPM)，具体取决于促销活动竞价策略。 此值将覆盖广告组级别的竞价。

<!-- If the placement is in a standard optimized portfolio, then the specified bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations. -->

### [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URL]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- note -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [关于投放](placement-about.md)
>* [创建负版面](placement-negative-create.md)
>* [更改投放位置和负投放位置的状态](placement-status-edit.md)

