---
title: 关于购物产品组
description: 了解购物营销活动中的购物产品组。
exl-id: ae270935-1464-4393-8b8c-745fee077522
feature: Search Campaign Management
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# 关于购物产品组

仅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]购物营销活动*

在购物营销活动中，您的产品组（而非关键词）决定了商户中心帐户中要显示购物广告的产品。 每个产品组都基于单个产品属性（如类别、产品类型、品牌、条件、产品ID或自定义标签），并对所有匹配产品使用相同的竞价。 您可以包含或排除每个组中产品的竞价。

您可以在广告组级别配置产品组，以确定商户中心帐户中的哪些产品出现在广告组的购物广告中。 即使广告组不包含广告实体，广告网络仍会显示产品的广告。

当同一产品包含在多个促销活动中时，广告网络首先使用促销活动优先级来确定哪个促销活动（及相关竞价）适用于广告拍卖。 如果所有促销活动具有相同的优先级，则具有最高竞价的促销活动符合条件。

有关[!DNL Google]购物营销活动和广告的更多信息，请参阅[实施 [!DNL Google Ads] 购物营销活动](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)和[Google广告文档](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&amp;rd=1)。 有关[!DNL Microsoft]购物营销活动的详细信息，请参阅[实施 [!DNL Microsoft Advertising] 购物营销活动](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)和[[!DNL Microsoft Advertising] 文档](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500)。

>[!NOTE]
>
>不支持在效果最佳的促销活动中列出各个组的[!DNL Google Ads]，这些组将取代智能购物促销活动。 要管理和查看列表组的数据，请使用[!DNL Google Ads]编辑器。

## 产品组层次结构

在为广告组创建具有特定属性的产品组之前，必须首先创建一个名为“[!UICONTROL All Products]”的全包式产品组。 从此父产品组，您可以为产品子集创建子产品组，也可以从子产品组创建孙子级。 为广告组创建第一个子产品组后，将自动使用默认广告组竞价创建另一个名为“[!UICONTROL Everything Else]”的产品组。 当您添加更多产品组时，“[!UICONTROL Everything Else]”组会相应地进行调整，使其构成所有不在其他产品组中的产品。

在广告组内，您可以创建最多七个级别的产品组（不包括“[!UICONTROL All Products]”）以包含或排除投标，其中一个或多个产品组在每个级别中针对相同的属性（例如，一个产品组为[!UICONTROL Brand]=Acme，另一个产品组在同一级别为[!UICONTROL Brand]=AcmePlus）。 父产品组称为细分，最低细分级别称为单位。 您可以在设备级别设置竞价和跟踪模板，或完全排除竞价。 广告组的整个活动产品组集将按层次应用，以确定符合条件的产品。 例如，如果将[!UICONTROL All Products]细分为[!UICONTROL Brand]=AcmeBasic和[!UICONTROL Brand]=AcmePlus，然后进一步将每个产品组细分为[!UICONTROL Condition]=New和设置竞价，则只能广告或排除具有AcmeBasic和AcmePlus品牌的新产品。

![产品组集示例](/help/search-social-commerce/assets/product-group-list.png "产品组集示例")

![产品组层次结构示例](/help/search-social-commerce/assets/product-group-tree.png "产品组层次结构示例")

## [!UICONTROL Product Groups]视图

您可以在[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups]视图中创建和编辑产品组，并删除产品组及其子产品组。

## 购物产品组的跟踪和性能数据

（具有“[!UICONTROL EF Redirect]”跟踪选项的帐户/营销活动）要允许Search、Social和Commerce跟踪产品组的转化，请[使用“跟踪URL”工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)生成产品组的跟踪URL，然后执行以下操作之一：

* （[!DNL Google Ads]必需；[!DNL Microsoft Advertising]的最佳实践）将跟踪URL添加到帐户、营销活动或产品组设置中的[!DNL Tracking Template]字段。 为便于维护，请尽可能在最高级别添加它们。 不包括为帐户或营销活动指定的任何附加参数。

  >[!CAUTION]
  >
  >([!DNL Microsoft Advertising])仅当未在产品信息源的自定义列中包含搜索、社交和Commerce跟踪URL时，才使用此选项。 如果同时执行这两个操作，则URL将包含两个重定向，并导致链接断开。

* （仅限[!DNL Microsoft Advertising]）将跟踪URL添加到[!DNL Microsoft Merchant Center]帐户内的产品数据中。 为此，请在产品信息源中名为[`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0)的自定义列中包含跟踪URL以及`link`或`mobile_link`字段中的值（如果适用）。 使用此方法生成的URL不包含在Search、Social和Commerce的帐户或营销活动设置中指定的任何跟踪参数。

您可以在[的[!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md)中查看有关产品组的数据。

>[!MORELIKETHIS]
>
>* [管理购物产品组](product-group-manage.md)
>* [[!DNL Google Ads] 产品组设置](product-group-settings-google.md)
>* [实施 [!DNL Google Ads] 购物营销活动](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
>* [[!DNL Microsoft Advertising] 产品组设置](product-group-settings-microsoft.md)
>* [实施 [!DNL Microsoft Advertising] 购物营销活动](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
