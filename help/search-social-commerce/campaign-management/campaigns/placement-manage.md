---
title: 管理 [!DNL Google Ads] 版面
description: 了解如何为 [!DNL Google Ads] 广告组创建和管理可出价投放。
exl-id: 80cb6fc6-e778-4b19-9e52-e0b57bde0d73
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# 管理[!DNL Google Ads]个版面

仅&#x200B;*[!DNL Google Ads]个帐户*

您可以在[支持的营销活动类型](/help/search-social-commerce/introduction/supported-inventory.md)中创建和编辑广告组的版面，该活动类型以[同步的广告网络帐户](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)中的显示网络为目标

## 创建[!DNL Google Ads]投放位置

>[!TIP]
>
>要同时创建多个投放位置，请使用[营销活动批量处理工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Placements]**。

1. &#x200B;
   1. 在数据表上方的工具栏中，单击![创建](/help/search-social-commerce/assets/add.png "创建")。

1. 选择广告网络、帐户、营销活动和广告组，然后单击&#x200B;**[!UICONTROL Continue]**。

1. 配置[位置设置](#placement-settings)。

1. 单击&#x200B;**[!UICONTROL Post]**。

## 编辑[!DNL Google Ads]版面

>[!TIP]
>
>若要同时编辑多个投放位置，请使用[营销活动批量处理工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Keywords]**。

1. 选中要编辑的每一行旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在数据表上方的工具栏中，单击![编辑](/help/search-social-commerce/assets/edit.png "编辑") 。

1. 编辑[位置设置](#placement-settings)。

   对于多个投放位置，您的更改将应用于所有选定的投放位置。 对于某些字母数字字段，可以将现有值更改为指定值，将现有字符串替换为指定字符串，在每个值的开头添加指定前缀，或者在每个值的结尾附加后缀。 对于某些货币字段，您可以将现有值更改为指定值，或者按指定百分比或货币金额增加或减少金额（具有限制）。

1. 保存数据：

   * （单个投放位置）单击&#x200B;**[!UICONTROL Post]**。

   * （多个投放位置）单击&#x200B;**[!UICONTROL Post Now]**。

## 投放设置 {#placement-settings}

### [!UICONTROL Placement Details]

您的广告可以出现在内容网络上的&#x200B;**[!UICONTROL Placements]：**&#x200B;个站点。 输入有效的URL，例如www.example.com、example.com或www.example.com/shoes/kids。 要指定多个字符串，请用逗号分隔它们，或者在单独的行中输入它们。 URL不能包含问号(`?`)。 **注意：**&#x200B;您可以[从[!UICONTROL Placements] > [!UICONTROL Negatives]视图、广告组和营销活动设置中排除网站版面](placement-negative-create.md)。

**[!UICONTROL Status]：**&#x200B;投放位置的显示状态： *活动*（启用竞价；默认值）、*已暂停*（禁用竞价）或&#x200B;*已删除*（删除投放位置；仅删除现有投放位置）。

### [!UICONTROL Bids]

**[!UICONTROL Bid]：**（可选）基于投放位置的广告的最大每次点击成本(CPC)或每千次可视展示成本(vCPM)，具体取决于促销活动竞价策略。 此值将覆盖广告组级别的竞价。

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
>* [关于版面](placement-about.md)
>* [创建负版面](placement-negative-create.md)
>* [更改版面和负版面的状态](placement-status-edit.md)
