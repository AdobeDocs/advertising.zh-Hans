---
title: 品牌安全和媒体质量
description: 了解有关品牌安全和媒体质量功能的更多信息。
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
source-git-commit: 7ee798e11375863e776ac3e802efc9112280e750
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 0%

---

# 品牌安全和媒体质量

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSP提供了一套品牌保护功能，以确保您的每个营销活动在品牌安全的环境中都能吸引真正的用户。

我们的欺诈监视团队与业界领先的合作伙伴（如[!DNL Interactive Advertising Bureau]、[!DNL Trust and Accountability Group] [!DNL (TAG)]和[!DNL WhiteOps]）紧密合作，仔细管理我们平台上的库存。 通过主动管理我们的供应，DSP确保跨平台的所有广告商都免受非人为流量（机器人、爬网程序、数据中心流量和欺诈）的影响，并仅在品牌安全的环境中投放。

除了提供集中质量管理外，我们还相信可让广告商设计符合其品牌的控制措施。 DSP提供了与[!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science]和[!DNL Peer39]的集成，确保每个广告商都可以选择其所需的欺诈防护、上下文筛选和关键词定位级别。

## 质量计划

### 支持[!DNL Ads.txt]的清单验证

表示 [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt)的[[!DNL Ads.txt]是[!DNL Interactive Advertising Bureau] ([!DNL IAB])在2017年6月发起的一项计划，旨在促进在公开市场上正确呈现库存，从而打击非法流量来源和域欺骗。 参与的出版商和发行商通过将`ads.txt`页面保留在域的顶层（例如`example.com/ads.txt`），公开声明有权销售其数字库存的公司，以及这些关系的性质。

DSP通过读取每个发布者的`ads.txt`文件并允许您选择仅向已验证的[!DNL ads.txt]销售者购买来支持[!DNL ads.txt]。 例如，通过将我们看到的访问`nytimes.com`的卖家与《纽约时报》的`ads.txt`文件相匹配，我们可以识别哪些是合法的，哪些是非法的，如果投放位置配置为仅从经过验证的卖家处购买，我们将阻止违法者。<!-- can we actually mention NY Times? -->

您可以为每个广告商<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->设置默认的[!DNL ads.txt]控件，然后可选[将每个版面的设置](/help/dsp/campaign-management/placements/placement-settings.md)自定义为：

* 仅从域授权的直销商处购买库存

* 仅从域的授权直销人员和转销商购买库存

* 优先从域的授权直销商和经销商处购买库存

* 从所有卖家购买库存

### 平台欺诈监控

DSP与业界领先供应商（如[!DNL Whiteops]和[!DNL Integral Ad Science]）合作，建立了强大的内部工具和系统来管理我们平台上的欺诈行为。

此外，Adobe还与[!DNL IAB]和[!DNL TAG]密切合作，以确保能够利用诸如[!DNL ads.txt]（请参阅上一部分）、[!DNL IAB]机器人和蜘蛛程序列表以及[!DNL TAG]数据中心IP列表之类的工具，通过符合行业标准的强大欺诈阻止功能来保护我们的广告商。

我们的团队通过多维度质量方法监控异常和无效流量模式，确保受保护库存上的无效流量低于3%。 任何可疑的库存 — 包括特定域上的库存或者来自特定出版商或卖家的库存 — 都会立即在整个平台上被阻止。

### 库存映射、分层和分类

清单映射是在将新清单添加到我们的平台之前，对所有新清单所需的详细审查和载入流程。 此过程旨在确保DSP上所有库存的安全和质量。

* **映射：**&#x200B;我们的清单团队仔细审查每个域，评估以下方面：

   * 品牌安全

   * 广告类型验证

   * 通用内容、重复域和虚假广告投放

* **分层：**&#x200B;我们全面检查整个生态系统中的品牌存在，以便跨不同层对库存进行分类。 您可以[将投放位置](/help/dsp/campaign-management/placements/placement-settings.md)定位到这些层以获得所需的覆盖级别：

   * **[!UICONTROL T1]** — 国际知名品牌网站

   * **[!UICONTROL T2]** — 美观的网站，包括最新、最新、没有用户生成的内容，且通常缺乏全球知名度

   * **[!UICONTROL T3]** — 用户生成的内容和小范围内容

* **网站分类：**&#x200B;为确保内容定位和阻止更轻松，我们根据属性的内容为每个属性标记一个DSP定义的网站类别。 您可以根据版面目标[为每个版面](/help/dsp/campaign-management/placements/placement-settings.md)定位或排除这些网站类别。

### 全面支持站点阻止

DSP提供了全局阻止站点列表以及创建广告商和帐户的自定义阻止站点列表的选项。

#### DSP全局阻止的站点列表 {#global-blocked-sites}

DSP会维护一个全局阻止的站点列表，列出被认为不安全的站点以在其上运行广告。 此列表包含带有令人反感内容（例如仇恨或恐怖）的网站，以及被机器人、虚假预注册、不匹配的域和其他欺诈活动感染的网站。

作为我们根除欺诈广告商活动的品牌安全计划的一部分，将使用“阻止网站列表”图表中的措施对所有网站进行筛选。 所有未通过品牌安全检查的网站都会添加到全局阻止的网站列表中。 由于DSP动态管理此列表，因此根据最新的品牌安全分析，网站可以随时打开或关闭此列表。

如果将某个站点作为放置目标包含在全球阻止的站点列表中，则该站点会标有红色感叹号(！)。 这表示广告不会在标记的网站上运行。

>[!NOTE]
>
>您可以通过启用[投放位置设置](/help/dsp/campaign-management/placements/placement-settings.md)中的“[!UICONTROL Allow unscreened sites]”选项，选择绕过附加到受信任私人交易的标准显示广告的全局阻止站点列表。 如有必要，Adobe帐户团队还可以选择在交易的发布者设置中为公共（拍卖级别）交易禁用网站阻止。

#### 帐户级别和广告商级别的阻止站点列表

用户还可以维护帐户级别和广告商级别的阻止站点列表<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->，这些列表将自动用于所有投放。 除了全局阻止的站点列表之外，还应用较低级别的阻止的站点列表。

## 第三方集成

### 上下文过滤

上下文筛选允许您根据广告将投放的页面上下文来定位或阻止广告机会。 Adobe通过与行业领先供应商集成提供上下文过滤： [!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science]和[!DNL Peer39]。 当前筛选器的示例包括[!UICONTROL Adult Content]、[!UICONTROL Natural Disasters]、[!UICONTROL Legal Drinking Age]、[!UICONTROL MANGA]、[!UICONTROL Epidemics]和[!UICONTROL G-rated Sites]。

您可以为每个广告商<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->设置默认上下文筛选器控件，然后可选[自定义每个版面的设置](/help/dsp/campaign-management/placements/placement-settings.md)。 使用此功能时可能会收取额外费用。

![Comscore徽标](/help/dsp/assets/comscore-logo.png) ![DoubleVerify徽标](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science徽标](/help/dsp/assets/ias-logo.png) ![Peer39徽标](/help/dsp/assets/peer39-logo.png)

### 预竞价欺诈阻止

利用我们与[!DNL DoubleVerify]、[!DNL Integral Ad Science]和[!DNL Peer39]的第三方集成，阻止营销活动中的非人为流量。 这些集成提供了行业领先的预竞价阻止功能，以最大限度地减少营销活动中的常规和复杂无效流量（GIVT和SIVT）。

您可以为每个广告商<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->设置默认的竞价前欺诈阻止控件，然后可选[自定义每个投放位置的设置](/help/dsp/campaign-management/placements/placement-settings.md)。 使用此功能时可能会收取额外费用。

有关功能的更多信息，请直接联系您的首选供应商，或联系您的Adobe客户团队。

![DoubleVerify徽标](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science徽标](/help/dsp/assets/ias-logo.png) ![Peer39徽标](/help/dsp/assets/peer39-logo.png)

### 预竞价可视性 {#pre-bid-viewability}

由我们的行业领先合作伙伴[!DNL DoubleVerify]和[!DNL Integral Ad Science]提供支持的预竞价可视性过滤器允许广告商确保其促销活动在视频和显示内容库中达到预期的可视性性能目标。

您可以为每个广告商<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->设置默认可见性筛选器，然后可选[自定义每个版面的设置](/help/dsp/campaign-management/placements/placement-settings.md)。 使用此功能时可能会收取额外费用。

![DoubleVerify徽标](/help/dsp/assets/doubleverify-logo.png) ![整体广告科学徽标](/help/dsp/assets/ias-logo.png)

### 注意力定位和衡量

与[!DNL Adelaide]的[!DNL Adobe's]合作伙伴关系为广告商提供了对Adelaide量度“[!DNL Attention Units]”的支持，该量度基于眼睛跟踪、曝光和结果数据来测量媒体质量。

[位置级别竞价前注意目标定位](/help/dsp/campaign-management/placements/placement-settings.md)允许广告商定位特定注意级别以提高客户参与度。

此外，广告商可以为任何促销活动启用投放级别[!UICONTROL Attention Score]量度](/help/dsp/campaign-management/campaigns/campaign-settings.md#attention-measurement)（各展示次数中[!DNL Attention Units]的加权平均数）的[跟踪，以了解哪种投放策略产生的业务效果最佳。

每项单独功能需额外付费。

### 主题定位

DSP主题定位允许您利用我们行业领先的上下文合作伙伴[!DNL Comscore]来定位或阻止关键词列表。 主题定位可帮助您确保始终在符合您品牌的环境中提供广告，包括阻止有害内容或确保在可确保获得更大结果的环境中支出。

主题定位要求您直接使用合作伙伴平台创建自定义主题区段。 创建区段后，您可以在[!UICONTROL Audience Targeting]部分中为每个投放位置](/help/dsp/campaign-management/placements/placement-settings.md)定位或排除区段ID [。 此功能可能需要额外付费。

若要创建[!DNL Comscore]帐户和自定义主题区段，您可以在[https://agents.comscore.com](https://agents.comscore.com)上请求[!DNL Activation Segment Manager]的登录。 有关设置自定义区段的完整说明，请参阅[[!DNL Comscore] 帮助中心](https://comscoreactivation.zendesk.com/hc/)。 创建自定义区段时，[!DNL Segment Manager]中会显示这些区段的费用。

![Comscore徽标](/help/dsp/assets/comscore-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP已与[!DNL DoubleVerify]合作提供其[!DNL Authentic Brand Safety]定位解决方案，该解决方案允许您创建一组集中的品牌安全要求，以针对所有购买平台进行统一定位。

一旦您构建了具有必要定位的[!DNL DoubleVerify]品牌安全区段，您就可以在DSP中使用它来跨Web环境复制具有预竞价的竞价后块规则。

您可以为每个广告商<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->指定一个[!DNL DoubleVerify]区段ID，然后可选[为每个投放位置](/help/dsp/campaign-management/placements/placement-settings.md)启用或禁用[!UICONTROL Authentic Brand Safety]。 DSP按区段ID对帐户开单。

有关功能的详细信息，请直接联系[!DNL DoubleVerify]，或联系您的Adobe客户团队。

![DoubleVerify标志](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [位置设置](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
