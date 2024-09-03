---
title: “[!DNL Microsoft Advertising]产品组设置”
description: 引用 [!DNL Microsoft Advertising] 购物产品组的设置。
exl-id: ea3a4137-1396-430f-9d6c-8e1e1f1f52c2
feature: Search Campaign Management
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# [!DNL Microsoft Advertising]产品组设置

## “所有产品”产品组

**[!UICONTROL Condition]：** （只读）所有产品

**[!UICONTROL Bid]：**（仅限包含的产品组）每次点击的最大成本(CPC)，这是为广告点击支付的最高金额。 此值仅用于没有子产品组的单位，而不用于广告组级别值。

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

此模板将覆盖更高级别的模板，并且仅用于没有子产品组的设备。

## 所有其他产品组

**[!UICONTROL Condition/Value]：** （对于现有产品组为只读）要定位的产品维度。 对于新产品组，输入要作为目标产品的维度和选定信息类别的资格属性（例如，按品牌定位时为“Acme”，按条件定位时为“New”）。

为特定产品维度（即，不是“所有产品”）创建产品组后，Search、Social和Commerce会自动为“其他所有产品”创建产品组。

有关可用产品维度的列表，请参阅“[购物营销活动产品过滤器](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)”。 根据营销活动的[!UICONTROL Inventory Filter]设置，您的维度列表可能会受到限制。

**[!UICONTROL Excluded]：** （对于新产品组为可选；对于现有产品组为只读）排除匹配产品的广告投标。

**[!UICONTROL Bid]：**（仅限包含的产品组）每次点击的最大成本(CPC)，这是为广告点击支付的最高金额。 此值仅用于没有子产品组的单位，而不用于广告组级别值。

<!-- **[!UICONTROL Tracking Template]:** -->

<!-- ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

此模板将覆盖更高级别的模板，并且仅用于没有子产品组的设备。

>[!MORELIKETHIS]
>
>* [关于购物产品组](product-group-about.md)
>* [管理购物产品组](product-group-manage.md)
>* [购物营销活动产品筛选器](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [实施 [!DNL Microsoft Advertising] 购物营销活动](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
