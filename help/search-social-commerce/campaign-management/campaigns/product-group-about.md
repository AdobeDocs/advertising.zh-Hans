---
title: 关于购物产品组
description: 了解购物营销活动中的购物产品组。
exl-id: ae270935-1464-4393-8b8c-745fee077522
feature: Search Campaign Management
source-git-commit: 4ed0d225dafcb07e8a563ef7e723cd247da5e1a9
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 0%

---

# 关于购物产品组

*[!DNL Google Ads]和 [!DNL Microsoft® Advertising] 仅限购物营销活动*

在购物营销活动中，您的产品组（而非关键词）决定了商户中心帐户中要显示购物广告的产品。 每个产品组都基于单个产品属性（如类别、产品类型、品牌、条件、产品ID或自定义标签），并对所有匹配产品使用相同的竞价。 您可以包含或排除每个组中产品的竞价。

您可以在广告组级别配置产品组，以确定商户中心帐户中的哪些产品出现在广告组的购物广告中。 即使广告组不包含广告实体，广告网络仍会显示产品的广告。

当同一产品包含在多个促销活动中时，广告网络首先使用促销活动优先级来确定哪个促销活动（及相关竞价）适用于广告拍卖。 如果所有促销活动具有相同的优先级，则具有最高竞价的促销活动符合条件。

有关详情 [!DNL Google] 购物营销活动和广告，请参阅&quot;[实施 [!DNL Google Ads] 购物营销活动](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)”和 [Google Ads文档](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&amp;rd=1). 有关详情 [!DNL Microsoft®] 购物营销活动，请参见&quot;[实施 [!DNL Microsoft® Advertising] 购物营销活动](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)”和 [[!DNL Microsoft® Advertising] 文档](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>不支持以下项目 [!DNL Google Ads] 在效果最佳的促销活动中列出组，这些促销活动将取代智能购物促销活动。 要管理和查看列表组的数据，请使用 [!DNL Google Ads] 编辑者。

## 产品组层次结构

在为广告组创建具有特定属性的产品组之前，必须首先创建一个名为“”的全包式产品组[!UICONTROL All Products]“ 从此父产品组，您可以为产品子集创建子产品组，也可以从子产品组创建孙子级。 为广告组创建第一个子产品组后，另一个产品组将命名为“[!UICONTROL Everything Else]”是使用默认广告组竞价自动创建的。 当您添加更多产品组时，[!UICONTROL Everything Else]“集团作出相应调整，使其构成所有不属于其他产品集团之产品。

在广告组中，您最多可以创建七个级别的产品组(不包括&quot;[!UICONTROL All Products]“)包括竞价或从竞价中排除，使一个或多个产品组在每个级别中定位相同的属性(例如， [!UICONTROL Brand]=Acme表示一个产品组和 [!UICONTROL Brand]=AcmePlus（对于同一级别的另一个）。 父产品组称为细分，最低细分级别称为单位。 您可以在设备级别设置竞价和跟踪模板，或完全排除竞价。 广告组的整个活动产品组集将按层次应用，以确定符合条件的产品。 例如，如果细分 [!UICONTROL All Products] 到 [!UICONTROL Brand]=AcmeBasic和 [!UICONTROL Brand]=AcmePlus ，然后进一步将这些产品组细分为 [!UICONTROL Condition]=新的和已设置的竞价，则只有具有AcmeBasic和AcmePlus品牌的新产品才能在广告中宣传或排除在广告之外。

![产品组集示例](/help/search-social-commerce/assets/product-group-list.png "产品组集示例")

![示例产品组层次结构](/help/search-social-commerce/assets/product-group-tree.png "示例产品组层次结构")

## 此 [!UICONTROL Product Groups] 视图

您可以在中创建和编辑产品组，并删除产品组及其子产品组。 [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] 视图。

## 购物产品组的跟踪和性能数据

(帐户/营销活动包含&quot;[!UICONTROL EF Redirect]”跟踪选项)以允许搜索、社交和商务跟踪产品组的转化， [使用跟踪URL工具为产品组生成跟踪URL](/help/search-social-commerce/tools/click-tracking-url-generate.md)，然后执行以下操作之一：

* (需要 [!DNL Google Ads]；的最佳实践 [!DNL Microsoft® Advertising])将跟踪URL添加到 [!DNL Tracking Template] “帐户”、“促销活动”或“产品组”设置中的字段。 为便于维护，请尽可能在最高级别添加它们。 不包括为帐户或营销活动指定的任何附加参数。

  >[!CAUTION]
  >
  >([!DNL Microsoft® Advertising])仅当您在产品信息源的自定义列中未包含“搜索”、“社交”和“商务”跟踪URL时，才使用此选项。 如果同时执行这两个操作，则URL将包含两个重定向，并将导致链接断开。

* ([!DNL Microsoft® Advertising] 仅限)将跟踪URL添加到中的产品数据 [!DNL Microsoft® Merchant Center] 帐户。 要实现此目的，请包含跟踪URL以及 `link` 或 `mobile_link` 字段（如果适用），位于名为的自定义列中 [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) 在产品信息源中。 使用此方法生成的URL不包含在Search、Social和Commerce的帐户或营销活动设置中指定的任何跟踪参数。

您可以在中查看有关产品组的数据 [该 [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md).

>[!MORELIKETHIS]
>
>* [管理购物产品组](product-group-manage.md)
>* [[!DNL Google Ads] 产品组设置](product-group-settings-google.md)
>* [实施 [!DNL Google Ads] 购物营销活动](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)
>* [[!DNL Microsoft® Advertising] 产品组设置](product-group-settings-microsoft.md)
>* [实施 [!DNL Microsoft® Advertising] 购物营销活动](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)
