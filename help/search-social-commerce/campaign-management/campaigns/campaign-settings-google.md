---
title: ’[!DNL Google Ads] 营销活动设置
description: 引用设置 [!DNL Google Ads] 营销活动。
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
source-git-commit: c7821f112757f695a6ab9da1fffb014b822e1ff3
workflow-type: tm+mt
source-wordcount: '2378'
ht-degree: 0%

---

# [!DNL Google Ads] campaign设置

## \[营销活动创建屏幕\]

**[!UICONTROL Campaign Type]：** （仅在营销活动创建期间可用）广告的放置位置以及营销活动可能包含的广告类型：

* *[!UICONTROL Search Network Only]：* 在搜索网络上显示广告，包括 [!DNL Google] 搜索结果和（可选）搜索合作伙伴站点。 您必须为每个广告组指定关键字。

* *[!UICONTROL Search with Display Select]：* 在搜索网络上显示广告(包括 [!DNL Google] 搜索结果和（可选）搜索合作伙伴网站)，并可能在展示型网站上显示广告。 在显示网络上， [!DNL Google Ads] 无论营销活动的竞价策略如何，都会使用自动竞价选择性地显示您的广告。 对于搜索广告，请指定每个广告组的关键字；对于展示广告，请指定投放位置，并可以选择为每个广告组指定关键字。

* *[!UICONTROL Shopping Network]：* 显示产品广告，其中 [!DNL Google] 根据您的产品在中自动生成 [!DNL Google Merchant Center] 日期 [!DNL Google Shopping]，旁边的区域 [!DNL Google] 搜索结果（独立于文本广告）和（可选）搜索合作伙伴网站。 对于营销活动中的每个广告组，您可以指定要广告的产品组。

* *[!UICONTROL Display Network Only]：* 在显示网络上显示广告。 对于每个广告组，您必须指定投放位置，并且可以选择指定关键字。

* *[!UICONTROL Performance Max]：* （Beta测试版功能）使用跨渠道显示和优化广告转化 [!DNL Google Ads] 明智的竞价。 在Campaign设置中，您必须指定一个或多个资产组，包括图像、徽标、标题、描述、可选视频和受众信号。 [!DNL Google Ads] 自动组合资产以根据渠道提供广告(例如 [!DNL YouTube]， [!DNL Gmail]，或 [!DNL Search])。

  **注释：**

   * 只有必需的设置可用。 对于可选设置，请登录 [!DNL Google Ads] 编辑者。

   * 链接到 [!DNL Google Merchant Center] 不支持产品馈送。

   * 不支持列出组。 要管理和查看列表组的数据，请登录 [!DNL Google Ads] 编辑者。

   * 支持混合优化。 竞价策略目标和营销活动预算在营销活动级别设置。

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]：** 帐户中唯一的促销活动名称。

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]：**（仅限现有的只读Gmail营销活动）是否：

* *[!UICONTROL Target and Bid]* 用于仅显示与满足广告组任何其他目标的目标受众相关联的用户使用的广告。

* *[!UICONTROL Bid Only]：*  用于即使向不与目标受众关联的用户显示广告，只要他们满足其他广告组级别的目标。 但是，您可以通过为特定受众设置更高的竞价来增加向这些受众显示广告的可能性。

**[!UICONTROL Status]：** 营销活动的显示状态： *活动* 或 *已暂停*. 新广告营销活动的默认设置为 *活动*.

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]：** （仅针对搜索网络的促销活动，包括购物促销活动）在广告网络的搜索合作伙伴网络上显示您的广告。 默认情况下，此选项为 *[!UICONTROL Off]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]：** 该活动的竞价策略：

* *[!UICONTROL Enhanced CPC]：* (不适用于性能最大化或现有的只读模式 [!DNL Gmail] 促销活动)使用广告网络的增强型每次点击成本(eCPC)模型，该模型允许广告网络自动更改每次点击成本(CPC)竞价，从而尝试使用广告网络(不在“搜索”、“社交”和“Commerce”中)中指定的转化来最大化转化率，同时尝试将平均CPC保持在最大CPC以下。

当您将带eCPC的营销活动添加到经过优化的搜索、社交和Commerce产品组合时，Search、Social和Commerce会优化基本竞价，如果“[!UICONTROL Auto adjust campaign budget limits]”选项已启用 — 营销活动预算。 广告网络会优化所有竞价调整，并可能会在用户查询时根据专有数据和见解更改搜索、社交和Commerce生成的竞价。 **注意：** 仅当广告网络上跟踪的总转化与项目组合目标一致时，才在项目组合中使用eCPC营销活动。 <!-- Note to self: Within the ad network UI, you specify conversion goals either a) all conversion actions you've set to be included in "Conversions" at the account level or b) one or more individual conversions to use for optimization -->

* *[!UICONTROL Manual CPC]* （默认）：（不适用于效果最佳的营销活动）使用每次点击成本(CPC)模型。 您可以选择允许广告网络更改营销活动的竞价：

   * **[!UICONTROL Enable Enhanced CPC]** （默认禁用）：这与使用&#39;&#39;相同[!UICONTROL Enhanced CPC]”选项。

* *[!UICONTROL Maximize Clicks]：* （搜索、展示和购物营销活动）广告网络(而不是Search、Social和Commerce)可优化竞价以最大化点击次数。 （可选）输入 **[!UICONTROL Max CPC]** （每次点击成本），以确保广告网络为每次点击支付的金额不会超过特定金额。 **注意：** 将具有此策略的营销活动添加到项目组合时，竞价由点击权重驱动，而不是由项目组合目标驱动。

* *[!UICONTROL Maximize Conversion Value]：* （搜索、效果最佳化和智能购物营销活动）广告网络(而非Search、Social和Commerce)可优化竞价以实现转化价值的最大化。 （可选）输入 **[!UICONTROL Target Return on Ad Spend]** (ROAS)的百分比。 **注意：** 此选项适用于混合项目组合中的营销活动，但适用于标准项目组合中的营销活动。

* *[!UICONTROL Maximize Conversions]：* （搜索、展示和效果最佳促销活动）广告网络(而非Search、Social和Commerce)可优化竞价以最大限度地提高转化率。 （可选）输入 **[!UICONTROL Target CPA]** （每次收购成本）。 **注意：** 此选项适用于混合项目组合中的营销活动，但适用于标准项目组合中的营销活动。

* *[!UICONTROL Target CPA]：* （展示促销活动；现有的搜索促销活动）广告网络(而非Search、Social和Commerce)根据可选内容优化竞价 **[!UICONTROL Target CPA]** （每次购置成本），这是您要为一项购置（转化）支付的30天平均金额。 **注意：** 此选项用于具有任何支出策略的混合项目组合（而非标准项目组合）中的营销活动，但支出策略除外 [!UICONTROL Weekly] 或 [!UICONTROL Google Target CPA].

  平均位置和CPC竞价数据不适用于具有此竞价策略的营销活动。

  对于新的搜索促销活动， [!DNL Google Ads] 已将此竞价策略替换为 [!UICONTROL Maximize Conversions] 策略使用 [!UICONTROL Target CPA] 值。 对于使用此策略的现有搜索营销活动，您只能编辑目标值，这样做会将策略更改为 [!UICONTROL Maximize Conversions] 使用指定的策略 [!UICONTROL Target CPA] 值。

* *[!UICONTROL Target Impression Share]：* （搜索促销活动）广告网络(而非Search、Social和Commerce)会优化竞价以实现目标展示份额和广告位置。 （可选）输入 **[!UICONTROL Target Impression Share]** 以百分比表示， **[!UICONTROL Target Ad Position]**，和 **[!UICONTROL Max CPC]** （每次点击成本）。 **注意：** 项目组合不支持此选项。

* *[!UICONTROL Target Return on Ad Spend]：*  （展示和购物营销活动；现有的搜索营销活动）广告网络(而不是Search、Social和Commerce)根据指定的来优化竞价 **[!UICONTROL Target ROAS]** （广告支出回报率），以百分比表示。 **注意：** 此选项用于具有任何支出策略的混合项目组合（而非标准项目组合）中的营销活动，但支出策略除外 [!UICONTROL Weekly] 或 [!UICONTROL Google Target ROAS].

  平均位置和CPC竞价数据不适用于具有此竞价策略的营销活动。

  对于新的搜索促销活动， [!DNL Google Ads] 已将此竞价策略替换为 [!UICONTROL Maximize Conversion Value] 策略使用 [!UICONTROL Target Return on Ad Spend value]. 对于使用此策略的现有搜索营销活动，您只能编辑目标值，这样做会将策略更改为 [!UICONTROL Maximize Conversion Value] 使用指定的策略 [!UICONTROL Target Return on Ad Spend] 值。

* *[!UICONTROL Viewable CPM]：* （现有，只读） [!DNL Gmail] 仅限促销活动)广告网络(而非Search、Social和Commerce)仅对测量为可查看的广告投标。 **注意：** 任何类型的项目组合均不支持对此策略进行优化。

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]：** （仅限购物营销活动；现有营销活动为只读）营销活动产品销售的国家/地区。 由于产品与目标国家/地区相关联，因此此设置确定在营销活动中广告的产品。

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]：** (仅限购物营销活动；已参与本地购物计划的广告商 [!DNL Google Merchant Center] 位于美国、英国、DE、FR、JP和AU的商店；可选)允许 [!DNL Google Ads] 以自动将本地库存信息添加到Google.com上的购物广告中。

**提示：** 如果使用此设置，请勿在中排除本地广告 [!UICONTROL Inventory Filter] 设置。

**注意：** 本地库存广告需要两个额外的源来 [!DNL Google Merchant Center]  — 一个包含您的本地产品数据，另一个包含您的本地产品清单。 请参阅 [!DNL Google Ads] 文档，以了解有关 [本地购物广告](https://www.google.com/retail/local-inventory-ads/).

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]：** （仅限搜索和显示网络）促销活动中广告的一个或多个目标语言。

[!DNL Google Ads] 根据用户的语言确定用户的语言 [!DNL Google] 语言设置或搜索查询、当前页面或最近查看页面的语言 [!DNL Google Display Network].

**[!UICONTROL Location Targets]：** 要作为目标包含或排除的特定用户地理位置。 默认情况下，会定位所有位置。 您可以在任意位置组合中包括和排除用户。 排除项始终会覆盖包含项。

* 要定位所有位置，请勿选择任何位置。

* 要定位或排除特定位置，请执行以下操作：

   * （国家/地区、州/省、大都市区域或城市）单击 **[!UICONTROL Location Target]** (![位置目标](/help/search-social-commerce/assets/location-target.png "位置目标"))并找到要包含和排除的位置：

      * 要包括一个位置及其子位置，请单击它旁边的圆圈一次，以便显示一个蓝色复选标记(![包括](/help/search-social-commerce/assets/include.png "包括"))中显示。

      * 要排除某个位置，请单击该位置旁边的圆圈两次，以便显示一个红色复选标记(![排除](/help/search-social-commerce/assets/exclude.png "排除"))中显示。

      * 要将位置展开到其子组件中（例如美国的州、都市区或城市），请单击位置名称。

      * 要搜索位置，请在输入字段中输入或粘贴位置的前三个字符。 在搜索结果中，单击 **[!UICONTROL Include]** 要包含或的位置旁边 **[!UICONTROL Exclude]** 位于要排除的位置旁边。

   * （地址附近的位置；仅限包含的目标）单击 **[!UICONTROL Radius Target]** (![Radius目标](/help/search-social-commerce/assets/radius-target.png "Radius目标"))，然后单击 **[!UICONTROL Address]**. 输入地址和目标地址周围以英里或公里为单位的半径，然后单击 **[!UICONTROL Add]**.

   * （地理坐标附近的位置；仅包含目标）单击 **[!UICONTROL Radius Target]** (![Radius目标](/help/search-social-commerce/assets/radius-target.png "Radius目标"))，然后单击 **[!UICONTROL Coordinate]**. 输入目标位置周围的纬度和经度以及半径（以英里或公里为单位），然后单击 **[!UICONTROL Add]**.

* （为包含的目标位置添加竞价调整）输入竞价调整值：

* 0%：不调整此位置中广告的竞价。

* \[从–90%到300%的其他值\]：增加或减少此位置广告的竞价。

**注意：**

* 搜索、社交和Commerce不为以下位置目标提供自动调整竞价调整，因为数据存在以下限制 [!DNL Google Ads] 提供将浏览者位置映射到位置目标的功能：

   * 半径目标。

   * 省/市/自治区/直辖市/地区/县/市/自治州以下的一些位置 [!DNL Google Ads] 不会将家长位置发送到冲浪者的URL，包括机场和美国国会选区。

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]：** （仅限显示网络）要定位的特定移动运营商；这些运营商按国家/地区排序。 如果不选择任何项，则所有项都会被定向。

**[!UICONTROL Mobile Carriers]：** （仅限显示网络）要定位的特定操作系统。 如果不选择任何项，则所有项都会被定向。

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

**[!UICONTROL Track Product Group]：** (用于 [!UICONTROL EF Redirect] 仅)未实现

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] （每个资产组）

**[!UICONTROL Asset Group Name]：** 资产组的名称。 链接到 [!DNL Google Merchant Center] 不支持产品馈送。

**[!UICONTROL Asset Group Status]：** 资产组的状态： *[!UICONTROL Active]* 或 *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]：** 从资产组创建的所有广告的最终URL。 <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]：** 广告最多包含15个图像，包括以下大小：1)至少三个正方形图像，2)至少三个横向图像，以及3)至少一个纵向图像。 请参阅 [[!DNL Google Ads] 图像规范](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). 您可以上传图像，也可以从中选择 [!UICONTROL Asset Library]  — 但不是两人在同一个操作中。

* 要上传图像，请执行以下操作：

   1. 在 [!UICONTROL Upload from Device] 选项卡，单击 **[!UICONTROL +]** 并从设备或网络中选择图像。

   1. 对于每个图像：

      1. 选择纵横比。

      1. 根据需要拖动并放置裁切框以选择图像的可查看部分，并在可能的情况下调整图像的可查看部分的大小。

      1. （可选）选择其他纵横比，并根据需要为每个选定的纵横比重新定位和调整图像大小。

         为每个选定的纵横比创建一个资源。

      1. 单击 **[!UICONTROL Proceed]**.

   1. 指定完图像后，单击 **[!UICONTROL Upload]**.

* 要从中选择图像，请执行以下操作： [!UICONTROL Asset Library]，单击 **[!UICONTROL Asset Library]** 并选择图像。

**[!UICONTROL Logos]：** 至少一个正方形(1:1)徽标和一个横向(4:1)徽标。 每种尺寸最多可包含5个。 请参阅 [[!DNL Google Ads] 徽标规范](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). 您可以上传图像，也可以从中选择 [!UICONTROL Asset Library]  — 但不是两人在同一个操作中。

* 要上传图像，请执行以下操作：

   1. 在 [!UICONTROL Upload from Device] 选项卡，单击 **[!UICONTROL +]** 并从设备或网络中选择图像。

   1. 对于每个图像：

      1. 选择纵横比。

      1. 根据需要拖动并放置裁切框以选择图像的可查看部分，并在可能的情况下调整图像的可查看部分的大小。

      1. （可选）选择其他纵横比，并根据需要为每个选定的纵横比重新定位和调整图像大小。

         为每个选定的纵横比创建一个资源。

      1. 单击 **[!UICONTROL Proceed]**.

   1. 指定完图像后，单击 **[!UICONTROL Upload]**.

* 要从中选择图像，请执行以下操作： [!UICONTROL Asset Library]，单击 **[!UICONTROL Asset Library]** 并选择图像。

**[!UICONTROL Videos]：** （可选）至少一个，最多五个， [!DNL YouTube] 至少10秒长的视频。 您可以输入URL或从中选择 [!UICONTROL Asset Library]  — 但不是两人在同一个操作中。

* 要输入URL，请执行以下操作：

   1. 在 [!UICONTROL Enter Video Url] 选项卡，输入URL。

   1. （可选）要添加其他URL，请单击 **[!UICONTROL + Add]** 并输入URL。

* 要从选择视频，请执行以下操作 [!UICONTROL Asset Library]，单击 **[!UICONTROL Asset Library]** 并选择视频。

**[!UICONTROL Headlines]：** 至少3个、最多5个简短标题，每个标题最多30个字符。 至少一个标题必须至少为15个字符或更少。 如果在中设置了用于启用最终URL扩展的营销活动级别选项 [!DNL Google Ads]，则 [!DNL Google Ads] 将此值替换为基于登陆页面内容的自定义标题。

您可以输入文本或从中选择资源 [!UICONTROL Asset Library]  — 但不是两人在同一个操作中。

* 要输入文本，请执行以下操作：

   1. 在 [!UICONTROL Enter Text] 选项卡，输入文本。

   1. （可选）要添加其他文本字符串，请单击 **[!UICONTROL + Add]** 并输入字符串。

* 要从中选择资源，请执行以下操作 [!UICONTROL Asset Library]，单击 **[!UICONTROL Asset Library]** 并选择资源。

**[!UICONTROL Long Headlines]：** 至少有一条，最多五条，每条最多有90个字符的长标题。 您可以输入文本或从中选择资源 [!UICONTROL Asset Library]  — 但不是两人在同一个操作中。

* 要输入文本，请执行以下操作：

   1. 在 [!UICONTROL Enter Text] 选项卡，输入文本。

   1. （可选）要添加其他文本字符串，请单击 **[!UICONTROL + Add]** 并输入字符串。

* 要从中选择资源，请执行以下操作 [!UICONTROL Asset Library]，单击 **[!UICONTROL Asset Library]** 并选择资源。

**[!UICONTROL Descriptions]：** 至少有两个（最多四个）描述，每个描述最多包含90个字符。 至少要有一个不超过30个字符的描述。 您可以输入文本或从中选择资源 [!UICONTROL Asset Library]  — 但不是两人在同一个操作中。

* 要输入文本，请执行以下操作：

   1. 在 [!UICONTROL Enter Text] 选项卡，输入文本。

   1. （可选）要添加其他文本字符串，请单击 **[!UICONTROL + Add]** 并输入字符串。

* 要从中选择资源，请执行以下操作 [!UICONTROL Asset Library]，单击 **[!UICONTROL Asset Library]** 并选择资源。

**[!UICONTROL Call to Action]：** 要包含在广告中的行动号召。 默认情况下， *[!UICONTROL Automated]* 已选中，并且 [!DNL Google Ads] 选择行动号召。 您可以根据需要选择其它活动。

**[!UICONTROL Business Name]：** 公司名称，最长为25个字符。

**[!UICONTROL Audience Signal]：** （可选） [!DNL Google Ads] 用作营销活动受众信号的受众。 [!DNL Google Ads] 机器学习模型使用受众来查找要定位的相似网上冲浪者，并且还可能会向未指定为信号的受众显示广告，以帮助您实现性能目标。 选择最有可能转化的受众。

>[!NOTE]
>受众信号不同于以 [营销活动级别和广告组级别受众目标](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Add new asset group]：** 用于指定其他资产组。

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]：** 是否要 *[!UICONTROL Use account conversion goals for this campaign]* （默认）或 *[!UICONTROL Use campaign specific conversion goals]*. 如果选择指定营销活动的转化目标，请选择标准目标和/或创建营销活动的自定义目标。

目标每天进行同步，因此可能无法列出之前24小时内创建的现有目标。 要更新列表， [手动同步广告网络数据](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

要创建自定义转化目标，请单击 **[!UICONTROL + Add custom goal]**，输入自定义目标名称，选择 [转化操作](https://support.google.com/google-ads/answer/6032150) 以包含在自定义目标中，然后单击 **[!UICONTROL Save]**. **注意：** 每个营销活动只能有一个自定义目标。

>[!TIP]
>
>如果促销活动属于项目组合，则使用与项目组合目标相同的转化目标。 使用不同的转化目标可能会影响项目组合的性能。

>[!MORELIKETHIS]
>
>* [管理营销活动](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)

