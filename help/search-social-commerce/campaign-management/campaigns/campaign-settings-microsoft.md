---
title: “[!DNL Microsoft Advertising]营销活动设置”
description: 引用 [!DNL Microsoft Advertising] 营销活动的设置。
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
source-git-commit: 096271a2e9daddc20f7f5f4e0063fda21974c8a1
workflow-type: tm+mt
source-wordcount: '2001'
ht-degree: 0%

---

# [!DNL Microsoft Advertising]营销活动设置

## \[营销活动创建屏幕\]

**[!UICONTROL Campaign Type]：**（仅在营销活动创建期间可用）广告放置位置和广告类型
营销策划可能包含：

* *[!UICONTROL Search]：*&#x200B;在搜索网络上显示文本广告。

* *[!UICONTROL Shopping Network]：*&#x200B;在购物网络上显示产品广告 — 针对您[!DNL Microsoft Merchant Center]产品目录中的产品。

* *[!UICONTROL Audience]：*&#x200B;在[!DNL Microsoft Audience Network]上显示本机/显示广告。 您可以a)通过将营销活动链接到[!UICONTROL Shopping Settings]部分中的商户中心商店来自动生成基于信息源的广告，也可以b)使用文本资源和上传的图像创建响应式广告。 这两个选项都需要您创建具有用户定位的广告组。

* *[!UICONTROL Shopping Campaigns for Brands]：*&#x200B;通过搜索网络和受众网络中的链接零售商促销您的产品。 您可以为促销活动创建子广告组和产品组（要促销的应用程序）以及可选产品广告；[!DNL Microsoft Advertising]会自动为产品组创建广告。 对于品牌的购物促销活动，请使用竞价策略[!UICONTROL Manual CPC]；对于品牌的购物促销活动，请使用竞价策略[!UICONTROL Cost per Sale]。

* *[!UICONTROL Microsoft Store Ads Campaign]：*&#x200B;推广您在[!DNL Microsoft Store]中可用的应用和游戏。 您可以为促销活动创建子广告组、产品组和可选产品广告；[!DNL Microsoft Advertising]会自动为产品组创建广告。

* *[!UICONTROL Audience CTV Video]：*&#x200B;在受众网络上显示已连接的电视(CTV)视频广告。

* *[!UICONTROL Audience Video]：*&#x200B;在受众网络上显示标准视频广告。

* *[!UICONTROL Performance Max]：*&#x200B;使用[!DNL Microsoft Advertising]智能竞价显示所有网络中的多个广告类型。 在Campaign设置中，您必须指定一个或多个资产组，包括图像、徽标、标题、描述、可选的行动呼吁和受众信号。 广告网络会自动组合资产，以根据渠道提供广告。

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]：**&#x200B;帐户中唯一的促销活动名称。 最大长度为128个字符。

**[!UICONTROL Status]：**&#x200B;促销活动的显示状态： *活动*&#x200B;或&#x200B;*已暂停*。 新广告营销活动的默认值为&#x200B;*活动*。

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]：**&#x200B;营销活动的竞价策略：

* *[!UICONTROL Cost per Sale]：*（仅限购物营销活动）广告网络(而非Search、Social和Commerce)根据[!UICONTROL Target CPS]（每次销售的成本）优化竞价。 仅当单击产品广告导致24小时内销售时才付款。 **注意：**&#x200B;请勿在项目组合中包含采用此竞价策略的促销活动。 搜索、社交和Commerce优化不适用于具有此竞价策略的营销活动。

  保存具有此竞价策略的品牌的购物营销活动后，便无法更改竞价策略。 对于其他购物营销活动类型，此策略仅适用于新营销活动。

* *[!UICONTROL CPV]* （仅限受众CTV视频营销活动）使用每次查看成本(CPV)模型。 搜索、Social和Commerce不提供对项目组合中包含的采用此竞价策略的促销活动的优化。

* *[!UICONTROL Enhanced CPC]：* （受众、搜索和购物网络上的营销活动）使用广告网络的增强型每次点击成本(eCPC)模型，该模型允许广告网络自动更改每次点击成本(CPC)竞价，从而尝试使用广告网络内指定的转化(不在“搜索”、“社交”和“Commerce”中)来最大限度地提高转化率，同时尝试将平均CPC保持在最大CPC以下。

  当您将带eCPC的营销活动添加到经过优化的搜索、社交和Commerce产品组合时，Search、Social和Commerce会优化基本竞价，并且在启用“[!UICONTROL Auto adjust campaign budget limits]”选项的情况下，还会优化营销活动预算。 广告网络会优化所有竞价调整，并可能会在用户查询时根据专有数据和见解更改搜索、社交和Commerce生成的竞价。 **注意：**&#x200B;仅在广告网络上跟踪的总转化与项目组合目标一致时，才在项目组合中使用eCPC营销活动。

* *[!UICONTROL Manual CPC]*： （品牌的购物营销活动；[!DNL Microsoft Store Ads]营销活动；其他营销活动类型已弃用）使用每次点击成本(CPC)模型。 对于某些广告类型，您可以选择允许广告网络更改促销活动的竞价：

   * **[!UICONTROL Enable Enhanced CPC]** （默认禁用）：此选项与使用“[!UICONTROL Enhanced CPC]”选项相同。

* *[!UICONTROL Manual CPA]：* （[!DNL Microsoft Store Ads]个营销活动）使用每次客户获取成本(CPA)模型。

* *[!UICONTROL Manual CPM]* （仅限受众营销活动和受众视频营销活动）使用每千次展示成本(CPM)模型，您可以为其指定每1,000次查看展示的支出方式。 当具有此竞价策略的营销活动包含在项目组合中时，不会对其进行优化。

* *[!UICONTROL Maximize Clicks]：*（搜索和购物营销活动）广告网络(而不是Search、Social和Commerce)会优化竞价以最大化点击次数。 （可选）输入&#x200B;**[!UICONTROL Max CPC]**（每次点击成本）以确保广告网络为每次点击支付的金额不会超过特定金额。 **警告：**&#x200B;当您将具有此策略的营销活动添加到项目组合时，点击权重（不是项目组合目标）将驱动竞价。

* *[!UICONTROL Maximize Conversion Value]：* （搜索和购物/智能购物网络，效果最佳的促销活动）广告网络(而不是Search、Social和Commerce)会优化竞价以最大限度地实现转化价值。 （可选）输入&#x200B;**[!UICONTROL Target Return on Ad Spend]** (ROAS)作为百分比。 **注意：**&#x200B;请将此选项用于混合项目组合中的营销活动，但不用于标准项目组合。

* *[!UICONTROL Maximize Conversions]：* (搜索网络或受众网络上的效果最佳的促销活动和促销活动（但不包括受众视频或连接的电视）)广告网络(不包括Search、Social和Commerce)可优化竞价以最大限度地提高转化率。 （可选）输入&#x200B;**[!UICONTROL Target CPC]**（每次点击成本）。 对于受众营销活动，您还可以输入可选的&#x200B;**[!UICONTROL Target CPA]**（每次客户获取的成本）。 **注意：**&#x200B;请将此选项用于混合项目组合中的营销活动，但不用于标准项目组合。

* *[!UICONTROL Target CPA]：* （搜索网络上的促销活动）广告网络(不是Search、Social和Commerce)基于可选的&#x200B;**[!UICONTROL Target CPA]**（每次客户获取成本）优化竞价，这是您想要为客户获取（转化）支付的30天平均金额。 **注意：**&#x200B;将此选项用于具有任何支出策略（除[!UICONTROL Weekly]或[!UICONTROL Google Target CPA]之外）的混合项目组合（而非标准项目组合）中的营销活动。

  平均位置和CPC竞价数据不适用于具有此竞价策略的营销活动。

* *[!UICONTROL Target Impression Share]：* （搜索网络上的营销活动）广告网络(而不是Search、Social和Commerce)会优化竞价以实现目标展示份额和广告位置。 （可选）输入&#x200B;**[!UICONTROL Target Impression Share]**&#x200B;作为百分比、**[!UICONTROL Target Ad Position]**&#x200B;和&#x200B;**[!UICONTROL Max CPC]**（每次点击成本）。 **注意：**&#x200B;混合项目组合中不支持此选项。

* *[!UICONTROL Target Return on Ad Spend]：* （搜索和购物网络上的营销活动）广告网络(而不是Search、Social和Commerce)根据以百分比形式指定的&#x200B;**[!UICONTROL Target ROAS]**（广告支出回报率）优化竞价。 （可选）输入&#x200B;**[!UICONTROL Max CPC]**（每次点击成本）以确保广告网络为每次点击支付的金额不会超过特定金额。 **注意：**&#x200B;将此选项用于具有任何支出策略（除[!UICONTROL Weekly]或[!UICONTROL Google Target ROAS]之外）的混合项目组合（而非标准项目组合）中的营销活动。

  平均位置和CPC竞价数据不适用于具有此竞价策略的营销活动。

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]：** （仅适用于购物营销活动；对于现有营销活动为只读）所在的国家/地区
营销活动的产品已售出。 由于产品与目标国家/地区相关联，因此此设置确定在营销活动中广告的产品。

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft Merchant Center]：** （仅限受众营销活动；可选）将营销活动与特定商家中心商店链接，以获取基于自动馈送的广告而不是响应式广告。 选择此选项时，请指定[!UICONTROL Merchant ID]和[!UICONTROL Products]。 您需要为营销活动创建广告组，但不需要创建广告。

将营销活动链接到商店并保存设置后，便无法更改此选项。

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Products]：** （仅链接到商户中心商店的受众营销活动）要广告的产品。 默认情况下，已选择&#x200B;*[!UICONTROL All products]*。 要仅广告具有特定属性的产品，请选择&#x200B;*[!UICONTROL Filter products]*&#x200B;并指定最多七个产品维度和属性组合，以筛选您的产品。 所有指定的值都必须适用于为产品显示的广告。 例如，要显示Acme宠物用品广告，您可以创建过滤器`Custom Label 1=animals`、`Category=pet supplies`和`Brand=Acme Pet Supplies`。

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]：** （仅限效果最佳的促销活动）广告的语言，它应该与您的广告可以显示的网站语言匹配。 [!DNL Microsoft Advertising]根据各种信号确定用户的语言，包括用户的查询、发布者的国家/地区以及用户的语言设置。

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

**[!UICONTROL Negative Websites]：** （仅显示/本地网络上的营销活动；可选）显示网络上不希望显示广告的站点。 请输入有效的URL，如www.example.com。 要指定多个字符串，请用逗号分隔它们，或者在单独的行中输入它们。

有关可用性的信息，请参阅Microsoft Advertising帮助“防止广告出现在特定网站](https://help.ads.microsoft.com/#apex/bae/en/14061/0)”。[

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

**[!UICONTROL Track Product Group]：** （仅适用于[!UICONTROL EF Redirect]）未实现

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] （每个资产组）

**[!UICONTROL Asset Group Name]：**&#x200B;资源文件夹（资源组）的名称。

**[!UICONTROL Asset Group Status]：**&#x200B;资源组的状态： *[!UICONTROL Active]*&#x200B;或&#x200B;*[!UICONTROL Paused]*。

**[!UICONTROL Final URL]：**&#x200B;从资产组创建的所有广告的最终URL。

**[!UICONTROL Images]：**&#x200B;广告的最多20张图像，其中包括至少一个正方形图像和一个横向图像。 请参阅[[!DNL Microsoft Advertising] 图像指南](https://help.ads.microsoft.com/#apex/ads/en/60204/0)。 您可以上传图像或从[!UICONTROL Asset Library]中选择图像，但无法在同一操作中同时选择两者。

* 要上传图像，请执行以下操作：

   1. 在[!UICONTROL Upload from Device]选项卡上，单击&#x200B;**[!UICONTROL +]**&#x200B;并从设备或网络中选择图像。

   1. 对于每个图像：

      1. 选择纵横比。

      1. 根据需要拖动并放置裁切框以选择图像的可查看部分，并在可能的情况下调整图像的可查看部分的大小。

      1. （可选）选择其他纵横比，并根据需要为每个选定的纵横比重新定位和调整图像大小。

         为每个选定的纵横比创建一个资源。

      1. 单击&#x200B;**[!UICONTROL Proceed]**。

   1. 指定完图像后，单击&#x200B;**[!UICONTROL Upload]**。

* 要从[!UICONTROL Asset Library]中选择图像，请单击&#x200B;**[!UICONTROL Asset Library]**&#x200B;并选择图像。

**[!UICONTROL Logos]：**&#x200B;至少一个徽标。 您最多可以包含五个。 请参阅[[!DNL Microsoft Advertising] 资产准则](https://help.ads.microsoft.com/#apex/ads/en/60204/0)。 您可以上传图像或从[!UICONTROL Asset Library]中选择图像，但无法在同一操作中同时选择两者。

* 要上传图像，请执行以下操作：

   1. 在[!UICONTROL Upload from Device]选项卡上，单击&#x200B;**[!UICONTROL +]**&#x200B;并从设备或网络中选择图像。

   1. 对于每个图像：

      1. 选择纵横比。

      1. 根据需要拖动并放置裁切框以选择图像的可查看部分，并在可能的情况下调整图像的可查看部分的大小。

      1. （可选）选择其他纵横比，并根据需要为每个选定的纵横比重新定位和调整图像大小。

         为每个选定的纵横比创建一个资源。

      1. 单击&#x200B;**[!UICONTROL Proceed]**。

   1. 指定完图像后，单击&#x200B;**[!UICONTROL Upload]**。

* 要从[!UICONTROL Asset Library]中选择图像，请单击&#x200B;**[!UICONTROL Asset Library]**&#x200B;并选择图像。

**[!UICONTROL Headlines]：**&#x200B;至少有三个最多15个简短标题，每个标题最多30个字符。 您可以输入文本或从[!UICONTROL Asset Library]中选择资源，但不能在同一个操作中同时输入和选择资源。

* 要输入文本，请执行以下操作：

   1. 在[!UICONTROL Enter Text]选项卡上，输入文本。

   1. （可选）要添加其他文本字符串，请单击&#x200B;**[!UICONTROL + Add]**&#x200B;并输入该字符串。

* 要从[!UICONTROL Asset Library]中选择资源，请单击&#x200B;**[!UICONTROL Asset Library]**&#x200B;并选择资源。

**[!UICONTROL Long Headlines]：**&#x200B;至少有一个长标题，最多五个长标题，每个标题最多为90个字符。 您可以输入文本或从[!UICONTROL Asset Library]中选择资源，但不能在同一个操作中同时输入和选择资源。

* 要输入文本，请执行以下操作：

   1. 在[!UICONTROL Enter Text]选项卡上，输入文本。

   1. （可选）要添加其他文本字符串，请单击&#x200B;**[!UICONTROL + Add]**&#x200B;并输入该字符串。

* 要从[!UICONTROL Asset Library]中选择资源，请单击&#x200B;**[!UICONTROL Asset Library]**&#x200B;并选择资源。

**[!UICONTROL Descriptions]：**&#x200B;至少有两个（最多5个）描述，每个描述最多包含90个字符。 您可以输入文本或从[!UICONTROL Asset Library]中选择资源，但不能在同一个操作中同时输入和选择资源。

* 要输入文本，请执行以下操作：

   1. 在[!UICONTROL Enter Text]选项卡上，输入文本。

   1. （可选）要添加其他文本字符串，请单击&#x200B;**[!UICONTROL + Add]**&#x200B;并输入该字符串。

* 要从[!UICONTROL Asset Library]中选择资源，请单击&#x200B;**[!UICONTROL Asset Library]**&#x200B;并选择资源。

**[!UICONTROL Call to Action]：**&#x200B;要包含在广告中的行动号召。 默认情况下，已选择&#x200B;*[!UICONTROL Act Now]*。

**[!UICONTROL Business Name]：**&#x200B;业务名称，最多25个字符。 它不能包含脚本、HTML或其他标记语言。

**[!UICONTROL Audience Signal]：**（可选） [!DNL Microsoft Advertising]受众用作营销活动的受众信号。 [!DNL Microsoft Advertising]机器学习模型使用受众来查找要定位的类似Web浏览者，并且还可能会向未指定为信号的受众显示广告，以帮助您实现性能目标。 选择最有可能转化的受众。

>[!NOTE]
>受众信号与[广告组级别受众目标](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md)不同。

<!-- **[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** -->

{{$include /help/_includes/display-path1-2.md}}

**[!UICONTROL Add new asset group]：**&#x200B;允许您指定另一个资源组。

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]：**&#x200B;是&#x200B;*[!UICONTROL Use account conversion goals for this campaign]* （默认）还是&#x200B;*[!UICONTROL Use campaign specific conversion goals]*。 如果选择指定营销活动的转化目标，则从所有可用目标列表中选择目标。 **注意：**&#x200B;目标每天进行同步，因此可能无法列出之前24小时内创建的目标。 若要更新列表，[请手动同步广告网络数据](/help/search-social-commerce/campaign-management/campaigns/sync-network.md)。

>[!TIP]
>
>如果促销活动是混合项目组合的一部分，则最佳实践是使用与项目组合目标中的转化目标匹配的促销活动级别目标；包括其他转化目标可能会影响项目组合性能。
>
> 但是，对于混合项目组合中您[将目标上传到广告网络](/help/search-social-commerce/tools/objective-upload-to-networks.md)的促销活动，请在广告网络的编辑器中执行以下操作，而不是此处： a)将上传的搜索、社交和Commerce项目组合目标量度（以“O_ACS_OBJ”开头）添加为促销活动的转化目标，以及b)添加任何包含由[!DNL Microsoft Advertising]通用事件跟踪(UET)标记跟踪的转化的促销活动目标，因为广告网络跟踪的量度未上传到具有目标的广告网络。

>[!MORELIKETHIS]
>
>* [管理营销活动](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
