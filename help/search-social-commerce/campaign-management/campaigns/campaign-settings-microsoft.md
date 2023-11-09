---
title: ’[!DNL Microsoft® Advertising] 营销活动设置
description: 引用设置 [!DNL Microsoft® Advertising] 营销活动。
exl-id: c6d86fb8-48b0-40fd-bcfc-c4afdccd5283
feature: Search Campaign Management
source-git-commit: 236224a1d8e38862f70db63b3762b763f5703623
workflow-type: tm+mt
source-wordcount: '1116'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] campaign设置

## \[营销活动创建屏幕\]

**[!UICONTROL Campaign Type]：** （仅在营销活动创建期间可用）广告的放置位置以及营销活动可能包含的广告类型：

* *[!UICONTROL Search]：* 在搜索网络上显示文本广告。

* *[!UICONTROL Shopping Network]：* 显示产品广告 — 针对您在网站中 [!DNL Microsoft® Merchant Center] 产品目录 — 在购物网络中。

* *[!UICONTROL Audience]：* 在上显示本机/显示广告 [!DNL Microsoft® Audience Network]. 您可以a)通过将营销活动关联到中的商家中心商店，自动生成基于信息源的广告 [!UICONTROL Shopping Settings] 或b)使用文本资源和上传的图像创建响应式广告。 这两个选项都需要您创建具有用户定位的广告组。

* *[!UICONTROL Shopping Campaigns for Brands]：* （测试版功能）通过搜索和受众网络中的关联零售商促销您的产品。 您可以为促销活动创建子广告组和产品组（要促销的应用程序），并且 [!DNL Microsoft® Advertising] 自动为产品组创建广告。

* *[!UICONTROL Microsoft® Store Ads Campaign]：* （Beta版功能）推广以下网站中提供的应用程序和游戏： [!DNL Microsoft® Store]. 您可以为营销活动创建子广告组和产品组，以及 [!DNL Microsoft® Advertising] 自动为产品组创建广告。

* *[!UICONTROL Audience Video]：* （测试版功能）在受众网络上显示视频广告。

* *[!UICONTROL Audience Video]：* （Beta测试版功能）显示受众网络上的已连接电视(CTV)视频广告。

* *[!UICONTROL Performance Max]：* 显示所有网络中的多种广告类型。

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]：** 帐户中唯一的促销活动名称。 最大长度为128个字符。

**[!UICONTROL Status]：** 营销活动的显示状态： *活动* 或 *已暂停*. 新广告营销活动的默认设置为 *活动*.

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

* *[!UICONTROL CPV]* （仅限受众CTV视频促销活动）使用每次查看成本(CPV)模型。 <!-- Campaigns with this bid strategy aren't optimized when they're included in portfolios. -->

* *[!UICONTROL Enhanced CPC]：* （受众、搜索和购物网络上的营销活动）使用广告网络的增强型每次点击成本(eCPC)模型，该模型允许广告网络自动更改每次点击成本(CPC)竞价，从而尝试使用广告网络内指定的转化（不在“搜索”、“社交”和“商务”中）最大限度地提高转化率，同时尝试将平均CPC保持在最大CPC以下。

  当您将带eCPC的营销活动添加到经过优化的搜索、社交和商务产品组合时，搜索、社交和商务会优化基本竞价，如果“[!UICONTROL Auto adjust campaign budget limits]”选项已启用 — 营销活动预算。 广告网络会优化所有竞价调整，并可能会在用户查询时根据专有数据和见解更改搜索、社交和商务生成的竞价。 **注意：** 仅当广告网络上跟踪的总转化与项目组合目标一致时，才在项目组合中使用eCPC营销活动。

* *[!UICONTROL Manual CPC]*：(品牌购物活动； [!DNL Microsoft Store Ads] 营销活动；已弃用 [!DNL Microsoft® Advertising] （在2021年用于其他促销活动类型）使用每次点击成本(CPC)模型。 对于某些广告类型，您可以选择允许广告网络更改促销活动的竞价：

   * **[!UICONTROL Enable Enhanced CPC]** （默认禁用）：这与使用&#39;&#39;相同[!UICONTROL Enhanced CPC]”选项。

* *[!UICONTROL Manual CPA]：* ([!DNL Microsoft Store Ads] 促销活动)使用每次客户获取成本(CPA)模型。

* *[!UICONTROL Manual CPM]* （仅限受众营销活动和受众视频营销活动）使用每千次展示成本(CPM)模型，您可以根据该模型指定每1,000次查看的展示要花费哪些成本。 当具有此竞价策略的营销活动包含在项目组合中时，不会对其进行优化。

* *[!UICONTROL Maximize Clicks]：* （搜索和购物营销活动）广告网络（而非搜索、社交和商务）会优化竞价以最大限度地提高点击次数。 （可选）输入 **[!UICONTROL Max CPC]** （每次点击成本），以确保广告网络为每次点击支付的金额不会超过特定金额。 **注意：** 将具有此策略的营销活动添加到项目组合时，竞价由点击权重驱动，而不是由项目组合目标驱动。

* *[!UICONTROL Maximize Conversion Value]：* （搜索和购物/智能购物网络，效果最佳的促销活动）广告网络（而不是搜索、社交和商务）会优化竞价以实现转化价值的最大化。 （可选）输入 **[!UICONTROL Target Return on Ad Spend]** (ROAS)的百分比。 **注意：** 此选项适用于混合项目组合中的营销活动，但适用于标准项目组合中的营销活动。

* *[!UICONTROL Maximize Conversions]：* (搜索网络上的营销活动 <!-- future: and audience network -->、效果最佳促销活动)广告网络（而不是搜索、社交和商务）会优化竞价以实现转化的最大化。 （可选）输入 **[!UICONTROL Target CPC]** （每次点击成本）<!-- future: ; for audience campaigns, you can also enter an optional [!UICONTROL Target CPA] (cost per acquisition) -->. **注意：** 此选项适用于混合项目组合中的营销活动，但适用于标准项目组合中的营销活动。

* *[!UICONTROL Target CPA]：* （搜索网络上的促销活动）广告网络（而非搜索、社交和商务）根据可选内容优化竞价 **[!UICONTROL Target CPA]** （每次购置成本），这是您要为一项购置（转化）支付的30天平均金额。 **注意：** 此选项用于具有任何支出策略的混合项目组合（而非标准项目组合）中的营销活动，但支出策略除外 [!UICONTROL Weekly] 或 [!UICONTROL Google Target CPA].

  平均位置和CPC竞价数据不适用于具有此竞价策略的营销活动。

* *[!UICONTROL Target Impression Share]：* （搜索网络上的营销活动）广告网络（而非搜索、社交和商务）会优化竞价以实现目标展示份额和广告位置。 （可选）输入 **[!UICONTROL Target Impression Share]** 以百分比表示， **[!UICONTROL Target Ad Position]**，和 **[!UICONTROL Max CPC]** （每次点击成本）。 **注意：** 混合项目组合中不支持此选项。

* *[!UICONTROL Target Return on Ad Spend]：*  （搜索和购物网络上的营销活动）广告网络（而非搜索、社交和商务）根据您的网站优化竞价。 **[!UICONTROL Target ROAS]** （广告支出回报率），以百分比表示。 （可选）输入 **[!UICONTROL Max CPC]** （每次点击成本），以确保广告网络为每次点击支付的金额不会超过特定金额。 **注意：** 此选项用于具有任何支出策略的混合项目组合（而非标准项目组合）中的营销活动，但支出策略除外 [!UICONTROL Weekly] 或 [!UICONTROL Google Target ROAS].

  平均位置和CPC竞价数据不适用于具有此竞价策略的营销活动。

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]：** （仅限购物营销活动；现有营销活动为只读）营销活动产品销售的国家/地区。 由于产品与目标国家/地区相关联，因此此设置确定在营销活动中广告的产品。

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft® Merchant Center]：** （仅限受众营销活动；可选）将营销活动与特定商家中心商店链接到基于自动馈送的广告而不是响应式广告。 选择此选项时，请指定 [!UICONTROL Merchant ID] 和 [!UICONTROL Products]. 您需要为营销活动创建广告组，但不需要创建广告。

将营销活动链接到商店并保存设置后，便无法更改此选项。

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}


**[!UICONTROL Products]：** （仅限链接到商户中心商店的受众营销活动）要广告的产品。 默认情况下， *[!UICONTROL All products]* 已选中。 要仅广告具有特定属性的产品，请选择 *[!UICONTROL Filter products]* 并指定最多7个用于筛选产品的产品维度和属性组合。 所有指定的值都必须适用于为产品显示的广告。 例如，要显示Acme宠物用品广告，您可以创建过滤器 `Custom Label 1=animals`， `Category=pet supplies`、和 `Brand=Acme Pet Supplies`.

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

**[!UICONTROL Negative Websites]：** （仅限显示网络上的营销活动；可选）显示网络上不希望显示广告的站点。 请输入有效的URL，如www.example.com。 要指定多个字符串，请用逗号分隔它们，或者在单独的行中输入它们。

有关可用性的信息，请参阅Microsoft® Advertising帮助»[防止广告出现在特定网站上](https://help.ads.microsoft.com/#apex/bae/en/14061/0)“

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

**[!UICONTROL Track Product Group]：** (用于 [!UICONTROL EF Redirect] 仅)未实现

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]：** 是否要 *[!UICONTROL Use account conversion goals for this campaign]* （默认）或 *[!UICONTROL Use campaign specific conversion goals]*. 如果选择指定营销活动的转化目标，则从所有可用目标列表中选择目标。 **注意：** 目标每天进行同步，因此可能无法列出之前24小时内创建的目标。 要更新列表， [手动同步广告网络数据](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

如果促销活动属于项目组合，则使用与项目组合目标相同的转化目标。 使用不同的转化目标可能会影响项目组合的性能。

>[!MORELIKETHIS]
>
>* [管理营销活动](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
