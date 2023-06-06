---
title: ”[!DNL Microsoft Advertising] campaign设置”
description: 引用设置 [!DNL Microsoft Advertising] 营销活动。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] campaign设置

## \[营销活动创建屏幕\]

**[!UICONTROL Campaign Type]：** （仅在营销活动创建期间可用）广告的放置位置以及营销活动可能包含的广告类型：

* *[!UICONTROL Search and Display Network]：* 仅在搜索网络上显示文本广告。

* *[!UICONTROL Shopping Network]：* 在中为您的产品显示产品广告和mdashl [!DNL Microsoft Merchant Center] 产品目录 — 在购物网络上

* *[!UICONTROL Audience]：* 在上显示本机/显示广告 [!DNL Microsoft Audience Network]. 您可以(a)通过将营销活动链接到中的商家中心商店，自动生成基于信息源的广告。 [!UICONTROL Shopping Settings] 或b)使用文本资源和上传的图像创建响应式广告。 这两个选项都需要您创建具有用户定位的广告组。

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]：** 帐户中唯一的促销活动名称。 最大长度为128个字符。

**[!UICONTROL Status]：** 营销活动的显示状态： *活动* 或 *已暂停*. 新广告营销活动的默认值为 *活动*.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]：** 该活动的竞价策略：

* *[!UICONTROL Enhanced CPC]：* （受众、搜索和购物网络上的营销活动）使用广告网络的增强型每次点击成本(eCPC)模型，该模型允许广告网络自动更改每次点击成本(CPC)竞价，从而尝试使用广告网络（不在“搜索、社交和商务”中）中指定的转化，最大化转化，同时尝试将平均CPC保持在最大CPC以下。

当您将带eCPC的营销活动添加到优化的搜索、社交和商务产品组合时，搜索、社交和商务会优化基本竞价，如果“[!UICONTROL Auto adjust campaign budget limits]”选项已启用 — 营销活动预算。 广告网络会优化所有竞价调整，并可能会在用户查询时根据专有数据和见解更改搜索、社交和商务生成的竞价。 **注意：** 仅当广告网络上跟踪的总转化率与项目组合目标一致时，才在项目组合中使用eCPC营销活动。

* *[!UICONTROL Manual CPC]* （默认）：(已弃用 [!DNL Microsoft Advertising] （2021年）使用每次点击成本(CPC)模型。 您可以选择允许广告网络更改促销活动的竞价：

   * **[!UICONTROL Enable Enhanced CPC]** （默认情况下处于禁用状态）：这与使用&quot;[!UICONTROL Enhanced CPC]”选项。

* *[!UICONTROL Manual CPM]* （仅限受众网络上的营销活动）使用每千次展示成本(CPM)模型，您可以根据此模型指定每1000次查看的展示要花费什么。 当具有此竞价策略的营销活动包含在项目组合中时，不会对其进行优化。

* *[!UICONTROL Maximize Clicks]：* （搜索和购物营销活动）广告网络（而不是搜索、社交和商务）会优化竞价以最大化点击次数。 （可选）输入 **[!UICONTROL Max CPC]** （每次点击成本）以确保广告网络为每一次点击支付的费用不超过特定金额。 **注意：** 当您将使用此策略的营销活动添加到项目组合时，竞价由点击权重驱动，而不是由项目组合目标驱动。

* *[!UICONTROL Maximize Conversion Value]：* （搜索和购物/智能购物网络）广告网络（而不是搜索、社交和商务）会优化竞价以实现转化价值的最大化。 （可选）输入 **[!UICONTROL Target Return on Ad Spend]** (ROAS)的百分比。 **注意：** 此选项适用于混合项目组合中的营销活动，但不适用于标准项目组合。

* *[!UICONTROL Maximize Conversions]：* (搜索网络上的营销活动 <!-- future: and audience network -->)广告网络（而不是Search、Social和Commerce）会优化竞价以实现最大转化率。 （可选）输入 **[!UICONTROL Target CPC]** （每次点击成本）<!-- future: ; for audience campaigns, you can also enter an optional [!UICONTROL Target CPA] (cost per acquisition) -->. **注意：** 此选项适用于混合项目组合中的营销活动，但不适用于标准项目组合。

* *[!UICONTROL Target CPA]：* （搜索网络上的营销活动）广告网络（而非搜索、社交和商务）基于可选内容优化竞价 **[!UICONTROL Target CPA]** （每次购置成本），这是您要为一项购置（转化）支付的30天平均金额。 **注意：** 此选项适用于混合项目组合（但不是标准项目组合）中具有任何支出策略的营销活动，但支出策略除外 [!UICONTROL Weekly] 或 [!UICONTROL Google Target CPA].

   使用此竞价策略的营销活动的平均位置和CPC竞价数据不可用。

* *[!UICONTROL Target Impression Share]：* （搜索网络上的营销活动）广告网络（而不是搜索、社交和商务）优化竞价以实现目标展示份额和广告位置。 （可选）输入 **[!UICONTROL Target Impression Share]** 以百分比表示， **[!UICONTROL Target Ad Position]**，和 **[!UICONTROL Max CPC]** （每次点击成本）。 **注意：** 混合项目组合不支持此选项。

* *[!UICONTROL Target Return on Ad Spend]：*  （搜索和购物网络上的营销活动）广告网络（而不是搜索、社交和商务）根据您的网站优化竞价 **[!UICONTROL Target ROAS]** （广告支出回报率），以百分比表示。 （可选）输入 **[!UICONTROL Max CPC]** （每次点击成本）以确保广告网络为每一次点击支付的费用不超过特定金额。 **注意：** 此选项适用于混合项目组合（但不是标准项目组合）中具有任何支出策略的营销活动，但支出策略除外 [!UICONTROL Weekly] 或 [!UICONTROL Google Target ROAS].

   使用此竞价策略的营销活动的平均位置和CPC竞价数据不可用。

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]：** （仅限购物营销活动；现有营销活动为只读）营销活动产品销售的国家/地区。 由于产品与目标国家/地区相关联，因此此设置确定在营销活动中广告的产品。

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft Merchant Center]：** （仅限受众营销活动；可选）将营销活动与特定商家中心商店链接到基于自动馈送的广告而不是响应式广告。 选择此选项时，请指定 [!UICONTROL Merchant ID] 和 [!UICONTROL Products]. 您需要为营销活动创建广告组，但不需要创建广告。

将营销活动链接到商店并保存设置后，便无法更改此选项。

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}


**[!UICONTROL Products]：** （仅限链接到商户中心商店的受众营销活动）要广告的产品。 默认情况下， *[!UICONTROL All products]* 已选中。 要仅广告具有特定属性的产品，请选择 *[!UICONTROL Filter products]* 并指定最多七个产品维度和属性组合，从中筛选产品。 所有指定的值都必须适用于为产品显示的广告。 例如，要显示Acme宠物用品广告，您可以创建过滤器 `Custom Label 1=animals`， `Category=pet supplies`、和 `Brand=Acme Pet Supplies`.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## [!UICONTROL DSA Options]

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]：** （仅限显示/原生网络上的营销活动；可选）显示网络上不想显示广告的站点。 输入有效的URL，如www.example.com。 要指定多个字符串，请用逗号分隔它们，或在单独行中输入它们。

有关可用性的信息，请参阅Microsoft Advertising帮助»[防止广告出现在特定网站上](https://help.ads.microsoft.com/#apex/bae/en/14061/0).”

## [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]：** (对于 [!UICONTROL EF Redirect] only)未实现

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

>[!MORELIKETHIS]
>
>* [管理营销活动](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)

