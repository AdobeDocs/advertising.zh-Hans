---
title: '[!DNL Google Ads]营销活动设置'
description: 引用 [!DNL Google Ads] 营销活动的设置。
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
source-git-commit: b321c807e3ab470068ad557ed428484d58e95ed4
workflow-type: tm+mt
source-wordcount: '2505'
ht-degree: 0%

---

# [!DNL Google Ads]营销活动设置

## \[营销活动创建屏幕\]

**[!UICONTROL Campaign Type]：** （仅在营销活动创建期间可用）广告的放置位置以及营销活动可能包含的广告类型：

* *[!UICONTROL Search Network Only]：*&#x200B;显示搜索网络上的广告，包括[!DNL Google]个搜索结果和（可选）搜索合作伙伴网站。 您必须为每个广告组指定关键字。

* *[!UICONTROL Search with Display Select]：*&#x200B;在搜索网络(包括[!DNL Google]个搜索结果和（可选）搜索合作伙伴网站)上显示广告，并可能在显示网络网站上显示广告。 在显示网络上，[!DNL Google Ads]使用自动竞价有选择地显示您的广告，而不管营销活动的竞价策略如何。 对于搜索广告，请指定每个广告组的关键字；对于展示广告，请指定投放位置，并可以选择为每个广告组指定关键字。

* *[!UICONTROL Shopping Network]：*&#x200B;显示产品广告，产品广告是[!DNL Google]根据您在[!DNL Google Merchant Center]上的[!DNL Google Shopping]中的产品、[!DNL Google]搜索结果旁边的区域（与文本广告分开）以及（可选）搜索合作伙伴网站自动生成的。 对于营销活动中的每个广告组，您可以指定要广告的产品组。

* *[!UICONTROL Display Network Only]：*&#x200B;在显示网络上显示广告。 对于每个广告组，您必须指定投放位置，并且可以选择指定关键字。

* *[!UICONTROL Performance Max]：*&#x200B;使用[!DNL Google Ads]智能竞价显示并优化跨渠道广告的转化。 在Campaign设置中，您必须指定一个或多个资产组，包括图像、徽标、标题、描述、可选视频和受众信号。 [!DNL Google Ads]自动组合资源以根据渠道（如[!DNL YouTube]、[!DNL Gmail]或[!DNL Search]）提供广告。

  **注释：**

   * 只有必需的设置可用。 对于可选设置，请登录到[!DNL Google Ads]编辑器。

   * 指向[!DNL Google Merchant Center]产品馈送的链接不受支持。

   * 不支持列出组。 要管理和查看列表组的数据，请登录[!DNL Google Ads]编辑器。

   * 支持混合优化。 竞价策略目标和营销活动预算在营销活动级别设置。

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]：**&#x200B;帐户中唯一的促销活动名称。

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]：**（仅限现有的只读Gmail营销活动）是否：

* *[!UICONTROL Target and Bid]*&#x200B;只向与目标受众相关联的用户显示广告，这些受众也满足广告组的任何其他目标。

* *[!UICONTROL Bid Only]：*&#x200B;若要显示广告，甚至向不与目标受众关联的用户显示，只要他们满足其他广告组级别的目标。 但是，您可以通过为特定受众设置更高的竞价来增加向这些受众显示广告的可能性。

**[!UICONTROL Status]：**&#x200B;促销活动的显示状态： *活动*&#x200B;或&#x200B;*已暂停*。 新广告营销活动的默认值为&#x200B;*活动*。

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]：** （仅针对搜索网络的营销活动，包括购物营销活动）在广告网络的搜索合作伙伴网络上显示您的广告。 默认情况下，此选项为&#x200B;*[!UICONTROL Off]*。

**[!UICONTROL AI Max Enabled]：** （仅针对搜索网络的营销活动；只读）是否启用了[[!UICONTROL AI Max]功能](https://support.google.com/google-ads/answer/15910366)： *[!UICONTROL On]*&#x200B;或&#x200B;*[!UICONTROL Off]*。

**[!UICONTROL AI Max Bundling]：** （仅针对搜索网络的营销活动；启用了AI Max功能的营销活动；只读）是否需要捆绑： *[!UICONTROL Not Required]*、*[!UICONTROL Required]*、*[!UICONTROL Unknown]*&#x200B;或&#x200B;*[!UICONTROL Unspecified]*。

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]：**&#x200B;营销活动的竞价策略：

* *[!UICONTROL Enhanced CPC]：*&#x200B;已弃用。 [!DNL Google Ads]已于2025年3月15日开始自动将现有[增强CPC竞价策略](https://support.google.com/google-ads/answer/2464964)更改为手动CPC。

* *[!UICONTROL Manual CPC]*（默认）：（不适用于效果最佳的促销活动）使用每次点击成本(CPC)模型。 您可以选择允许广告网络更改营销活动的竞价：

   * **[!UICONTROL Enable Enhanced CPC]**（默认禁用）：这与使用“[!UICONTROL Enhanced CPC]”选项相同，该选项已弃用。 [!DNL Google Ads]已于2025年3月15日开始自动将现有[增强CPC竞价策略](https://support.google.com/google-ads/answer/2464964)更改为手动CPC。

* *[!UICONTROL Maximize Clicks]：* （搜索、展示和购物营销活动）广告网络(而不是Search、Social和Commerce)会优化竞价以最大化点击次数。 （可选）输入&#x200B;**[!UICONTROL Max CPC]**（每次点击成本）以确保广告网络为每次点击支付的金额不会超过特定金额。 **注意：**&#x200B;当您将具有此策略的营销活动添加到项目组合时，竞价由点击权重驱动，而不是由项目组合目标驱动。

* *[!UICONTROL Maximize Conversion Value]：* （搜索、效果最佳化和智能购物营销活动）广告网络(而不是Search、Social和Commerce)会优化竞价以最大限度地实现转化价值。 （可选）输入&#x200B;**[!UICONTROL Target Return on Ad Spend]** (ROAS)作为百分比。 **注意：**&#x200B;请将此选项用于混合项目组合中的营销活动，但不用于标准项目组合。 在混合项目组合中，Search、Social和Commerce会优化营销活动级别或（如果可用）广告组级别的Target ROAS。

* *[!UICONTROL Maximize Conversions]：* （搜索、显示和效果最佳的促销活动）广告网络(而不是Search、Social和Commerce)会优化竞价以最大限度地提高转化率。 （可选）输入&#x200B;**[!UICONTROL Target CPA]**（每次购置成本）。 **注意：**&#x200B;请将此选项用于混合项目组合中的营销活动，但不用于标准项目组合。 在混合项目组合中，“搜索”、“社交”和“Commerce”可优化营销活动级别或（如果可用）广告组级别的Target CPA。

* *[!UICONTROL Target CPA]：*（展示型促销活动）广告网络(不是Search、Social和Commerce)根据可选的&#x200B;**[!UICONTROL Target CPA]**（每次收购成本）优化竞价，这是您为一次收购（转化）支付的30天平均金额。 **注意：**&#x200B;将此选项用于具有任何支出策略（除[!UICONTROL Weekly]或[!UICONTROL Google Target CPA]之外）的混合项目组合（而非标准项目组合）中的营销活动。 在混合项目组合中，“搜索”、“社交”和“Commerce”可优化营销活动级别或（如果可用）广告组级别的Target CPA。

  平均位置和CPC竞价数据不适用于具有此竞价策略的营销活动。

* *[!UICONTROL Target Impression Share]：* （搜索促销活动）广告网络(而不是Search、Social和Commerce)会优化竞价以实现目标展示份额和广告位置。 （可选）输入&#x200B;**[!UICONTROL Target Impression Share]**&#x200B;作为百分比、**[!UICONTROL Target Ad Position]**&#x200B;和&#x200B;**[!UICONTROL Max CPC]**（每次点击成本）。 **注意：**&#x200B;项目组合中不支持此选项。

* *[!UICONTROL Target Return on Ad Spend]：*（展示和购物营销活动）广告网络(不是Search、Social和Commerce)基于以百分比指定的指定&#x200B;**[!UICONTROL Target ROAS]**（广告支出回报率）优化竞价。 **注意：**&#x200B;将此选项用于具有任何支出策略（除[!UICONTROL Weekly]或[!UICONTROL Google Target ROAS]之外）的混合项目组合（而非标准项目组合）中的营销活动。 在混合项目组合中，Search、Social和Commerce会优化营销活动级别或（如果可用）广告组级别的Target ROAS。

  平均位置和CPC竞价数据不适用于具有此竞价策略的营销活动。

* *[!UICONTROL Viewable CPM]：* （仅限现有、只读[!DNL Gmail]个促销活动）广告网络(而非Search、Social和Commerce)仅对测量为可查看的广告投标。 **注意：**&#x200B;任何类型的项目组合均不支持此策略的优化。

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]：** （仅适用于购物营销活动；对于现有营销活动为只读）所在的国家/地区
营销活动的产品已售出。 由于产品与目标国家/地区相关联，因此此设置确定在营销活动中广告的产品。

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]：** （仅限购物营销活动；广告商已参与本地购物计划，并在美国、英国、DE、FR、JP和AU拥有[!DNL Google Merchant Center]家商店；可选）允许[!DNL Google Ads]自动将您的本地库存信息添加到Google.com上的购物广告中。

**提示：**&#x200B;如果使用此设置，请勿在[!UICONTROL Inventory Filter]设置中排除本地广告。

**注意：**&#x200B;本地库存广告需要向[!DNL Google Merchant Center]另外提供两个馈送 — 一个包含本地产品数据，另一个包含本地产品库存。 有关[!DNL Google Ads]本地购物广告[的更多信息，请参阅](https://www.google.com/retail/local-inventory-ads/)文档。

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]：** （仅限搜索和显示网络）促销活动中广告的一个或多个目标语言。

[!DNL Google Ads]根据用户的[!DNL Google]语言设置或搜索查询的语言、当前页面或最近在[!DNL Google Display Network]上查看的页面确定用户的语言。

**[!UICONTROL Location Targets]：**&#x200B;要作为目标包含或排除的特定用户地理位置。 默认情况下，会定位所有位置。 您可以在任意位置组合中包括和排除用户。 排除项始终会覆盖包含项。

* 要定位所有位置，请勿选择任何位置。

* 要定位或排除特定位置，请执行以下操作：

   * （国家/地区、州、大都市区域或城市）单击&#x200B;**[!UICONTROL Location Target]** （![位置目标](/help/search-social-commerce/assets/location-target.png "位置目标")）并找到要包含和排除的位置：

      * 若要包含位置及其子位置，请单击相邻圆圈一次，以便显示蓝色复选标记（![包含](/help/search-social-commerce/assets/include.png "包含")）。

      * 要排除某个位置，请单击相邻圆圈两次，以便显示红色复选标记（![排除](/help/search-social-commerce/assets/exclude.png "排除")）。

      * 要将位置展开到其子组件中（例如美国的州、都市区或城市），请单击位置名称。

      * 要搜索位置，请在输入字段中输入或粘贴位置的前三个字符。 在搜索结果中，单击要包含的位置旁边的&#x200B;**[!UICONTROL Include]**&#x200B;或要排除的位置旁边的&#x200B;**[!UICONTROL Exclude]**。

   * （地址附近的位置；仅限包含的目标）单击&#x200B;**[!UICONTROL Radius Target]** （![Radius目标](/help/search-social-commerce/assets/radius-target.png "Radius目标")），然后单击&#x200B;**[!UICONTROL Address]**。 输入地址和目标地址周围的英里或公里半径，然后单击&#x200B;**[!UICONTROL Add]**。

   * （地理坐标附近的位置；仅限包含的目标）单击&#x200B;**[!UICONTROL Radius Target]** （![Radius目标](/help/search-social-commerce/assets/radius-target.png "Radius目标")），然后单击&#x200B;**[!UICONTROL Coordinate]**。 输入目标位置周围的纬度和经度以及半径（以英里或公里为单位），然后单击&#x200B;**[!UICONTROL Add]**。

* （为包含的目标位置添加竞价调整）输入竞价调整值：

* 0%：不调整此位置中广告的竞价。

* \[从–90%到300%的其他值\]：增加或减少此位置广告的竞价。

**注释：**

* 由于[!DNL Google Ads]提供的用于将冲浪者位置映射到位置目标的数据存在限制，因此Search、Social和Commerce不为以下位置目标提供自动调整的竞价调整：

   * 半径目标。

   * 在州/省/地区/县/州级别下的某些位置，[!DNL Google Ads]不会在其冲浪者的URL中发送父级位置，包括机场和美国国会选区。

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]：** （仅限显示网络）要定位的特定移动运营商；运营商已排序
按国家/地区划分。 如果不选择任何项，则所有项都会被定向。

**[!UICONTROL Mobile Carriers]：** （仅显示网络）要定位的特定操作系统。 如果不选择任何项，则所有项都会被定向。

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## [!UICONTROL DSA Options]

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## [!UICONTROL Customer Acquisition Goals]

**[!UICONTROL Customer Acquisition]：** （仅限性能最高和搜索促销活动）如何为新客户和现有客户分配竞价：

* *[!UICONTROL Bid equally for new and existing customers]*

* *[!UICONTROL Bid higher for new customers than for existing customers]*

  **注意：**&#x200B;要使用此设置，您必须首先为[!DNL Google Ads]帐户或（如果适用）经理帐户激活新的客户获取目标。 目标在转化设置中定义符合条件的现有客户列表和新客户的附加转化值。 请参阅[!DNL Google Ads]帮助“[激活新的客户获取目标](https://support.google.com/google-ads/answer/14007601)”中的步骤1-2。

* *[!UICONTROL Only bid for new customers]*

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

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

**[!UICONTROL Asset Group Name]：**&#x200B;资源组的名称。 指向[!DNL Google Merchant Center]产品馈送的链接不受支持。

**[!UICONTROL Asset Group Status]：**&#x200B;资源组的状态： *[!UICONTROL Active]*&#x200B;或&#x200B;*[!UICONTROL Paused]*。

**[!UICONTROL Final URL]：**&#x200B;从资产组创建的所有广告的最终URL。<!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]：**&#x200B;广告的最多15个图像，包括以下大小：1)至少三个正方形图像，2)至少三个横向图像，以及3)至少一个纵向图像。 查看[[!DNL Google Ads] 图像规范](https://support.google.com/google-ads/answer/10724492?hl=en&ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications)。 您可以上传图像或从[!UICONTROL Asset Library]中选择图像，但无法在同一操作中同时选择两者。

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

**[!UICONTROL Logos]：**&#x200B;至少一个正方形(1:1)徽标和一个横向(4:1)徽标。 每种尺寸最多可包含5个。 查看[[!DNL Google Ads] 徽标规范](https://support.google.com/google-ads/answer/10724492?hl=en&ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications)。 您可以上传图像或从[!UICONTROL Asset Library]中选择图像，但无法在同一操作中同时选择两者。

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

**[!UICONTROL Videos]：**（可选）至少1个、最多5个、长度至少10秒的[!DNL YouTube]视频。 您可以输入URL或从[!UICONTROL Asset Library]中选择它们，但不能在同一个操作中同时输入和选择URL。

* 要输入URL，请执行以下操作：

   1. 在[!UICONTROL Enter Video Url]选项卡上，输入URL。

   1. （可选）要添加其他URL，请单击&#x200B;**[!UICONTROL + Add]**&#x200B;并输入该URL。

* 要从[!UICONTROL Asset Library]中选择视频，请单击&#x200B;**[!UICONTROL Asset Library]**&#x200B;并选择视频。

**[!UICONTROL Headlines]：**&#x200B;至少3个、最多5个简短标题，每个标题最多30个字符。 至少一个标题必须至少为15个字符或更少。 如果在[!DNL Google Ads]内设置了用于启用最终URL扩展的营销活动级别选项，则[!DNL Google Ads]会根据登陆页面内容将此值替换为自定义标题。

您可以输入文本或从[!UICONTROL Asset Library]中选择资源，但不能在同一个操作中同时输入和选择资源。

* 要输入文本，请执行以下操作：

   1. 在[!UICONTROL Enter Text]选项卡上，输入文本。

   1. （可选）要添加其他文本字符串，请单击&#x200B;**[!UICONTROL + Add]**&#x200B;并输入该字符串。

* 要从[!UICONTROL Asset Library]中选择资源，请单击&#x200B;**[!UICONTROL Asset Library]**&#x200B;并选择资源。

**[!UICONTROL Long Headlines]：**&#x200B;至少有一个长标题，最多五个长标题，每个标题最多为90个字符。 您可以输入文本或从[!UICONTROL Asset Library]中选择资源，但不能在同一个操作中同时输入和选择资源。

* 要输入文本，请执行以下操作：

   1. 在[!UICONTROL Enter Text]选项卡上，输入文本。

   1. （可选）要添加其他文本字符串，请单击&#x200B;**[!UICONTROL + Add]**&#x200B;并输入该字符串。

* 要从[!UICONTROL Asset Library]中选择资源，请单击&#x200B;**[!UICONTROL Asset Library]**&#x200B;并选择资源。

**[!UICONTROL Descriptions]：**&#x200B;至少有两个描述，最多四个描述，每个描述最多包含90个字符。 至少要有一个不超过30个字符的描述。 您可以输入文本或从[!UICONTROL Asset Library]中选择资源，但不能在同一个操作中同时输入和选择资源。

* 要输入文本，请执行以下操作：

   1. 在[!UICONTROL Enter Text]选项卡上，输入文本。

   1. （可选）要添加其他文本字符串，请单击&#x200B;**[!UICONTROL + Add]**&#x200B;并输入该字符串。

* 要从[!UICONTROL Asset Library]中选择资源，请单击&#x200B;**[!UICONTROL Asset Library]**&#x200B;并选择资源。

**[!UICONTROL Call to Action]：**&#x200B;要包含在广告中的call to action。 默认情况下，已选择&#x200B;*[!UICONTROL Automated]*，[!DNL Google Ads]将选择call to action。 您可以根据需要选择其它活动。

**[!UICONTROL Business Name]：**&#x200B;业务名称，最多25个字符。

**[!UICONTROL Audience Signal]：**（可选） [!DNL Google Ads]受众用作营销活动的受众信号。 [!DNL Google Ads]机器学习模型使用受众来查找要定位的类似Web浏览者，并且还可能会向未指定为信号的受众显示广告，以帮助您实现性能目标。 选择最有可能转化的受众。

>[!NOTE]
>受众信号不同于[营销活动级别和广告组级别的受众目标](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md)。

**[!UICONTROL Primary Status]：** （性能最佳的营销活动中的现有资源组的只读字段）为什么资源组会或不会以满负荷提供服务。 它考虑资产组状态以及其他信号，例如政策和质量审批。 值可能包括&#x200B;*合格，* *有限，* *不合格，* *已暂停，* *待处理，* *已移除，* *未知，*&#x200B;或未指定&#x200B;*未指定。*<!-- GGL also has a Primary Status field for campaigns; if we ever sync that, then we'll need to distinguish between them. -->

**[!UICONTROL Primary Status Reason]：** （性能最佳的营销活动中现有资源组的只读字段）有关资源组主要状态的更多详细信息。 值可能包括&#x200B;*ASSET_GROUP_DISAPPROVED，* *ASSET_GROUP_LIMITED，* *ASSET_GROUP_PAUSED，* *ASSET_GROUP_REMOVED，* *ASSET_GROUP_UNDER_REVIEW，* *CAMPAIGN_ENDED，* *CAMPAIGN_PAUSED，* *CAMPING_PENDING，* *CAMPAIGN_REMOVED，* *未知，*&#x200B;或&#x200B;*未指定。*

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]：**&#x200B;是&#x200B;*[!UICONTROL Use account conversion goals for this campaign]* （默认）还是&#x200B;*[!UICONTROL Use campaign specific conversion goals]*。 如果选择指定营销活动的转化目标，请选择标准目标和/或创建营销活动的自定义目标。

目标每天进行同步，因此可能无法列出之前24小时内创建的现有目标。 若要更新列表，[请手动同步广告网络数据](/help/search-social-commerce/campaign-management/campaigns/sync-network.md)。

要创建自定义转化目标，请单击&#x200B;**[!UICONTROL + Add custom goal]**，输入自定义目标名称，选择要包含在自定义目标中的[转化操作](https://support.google.com/google-ads/answer/6032150)，然后单击&#x200B;**[!UICONTROL Save]**。 **注意：**&#x200B;每个营销活动只能有一个自定义目标。

>[!TIP]
>
>如果促销活动是混合项目组合的一部分，则最佳实践是使用与项目组合目标中的转化目标匹配的促销活动级别目标；包括其他转化目标可能会影响项目组合性能。
>
>但是，对于混合项目组合中您[将目标上传到广告网络](/help/search-social-commerce/tools/objective-upload-to-networks.md)的促销活动，请在广告网络的编辑器中（而不是此处）执行以下操作：a)将上传的搜索、社交和Commerce项目组合目标量度（以“O_ACS_OBJ”开头）添加为促销活动的转化操作，以及b)添加任何包含[!DNL Google]跟踪的转化的促销活动目标，因为广告网络跟踪的量度未上传到具有目标的广告网络。

>[!MORELIKETHIS]
>
>* [管理营销活动](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
