---
title: 品牌安全和媒体质量
description: 了解有关品牌安全和媒体质量功能的更多信息。
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
source-git-commit: c8cad651585210d46cb0237e1843952e5e5cec3e
workflow-type: tm+mt
source-wordcount: '1348'
ht-degree: 0%

---

# 品牌安全和媒体质量

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSP提供了一套品牌保护功能，以确保您的每个营销活动在品牌安全的环境中都能吸引真正的用户。

我们的欺诈监控团队与行业领先合作伙伴(例如 [!DNL Interactive Advertising Bureau]， [!DNL Trust and Accountability Group] [!DNL (TAG)]、和 [!DNL WhiteOps]，以便仔细策划我们平台上的库存。 通过主动管理我们的供应，DSP确保跨平台的所有广告商都免受非人为流量（机器人、爬网程序、数据中心流量和欺诈）的影响，并仅在品牌安全的环境中投放。

除了提供集中质量管理外，我们还相信可让广告商设计符合其品牌的控制措施。 DSP提供与 [!DNL Comscore]， [!DNL DoubleVerify]， [!DNL Integral Ad Science]， [!DNL Oracle Data Cloud]、和 [!DNL Peer39]，确保每个广告商都可以选择其所需的欺诈防护、上下文过滤和关键词定位级别。

## 质量计划

### 使用进行库存验证 [!DNL Ads.txt] 支持

[[!DNL Ads.txt]，表示 [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) 是贵机构发起的一项计划， [!DNL Interactive Advertising Bureau] ([!DNL IAB])，以促进在公开市场上适当地呈现库存，从而打击非法流量来源和域名欺骗。 参与计划的出版商和分销商公开声明获授权销售其数字库存的公司，以及这些关系的性质，方法是 `ads.txt` 域顶级的页面(如 `example.com/ads.txt`)。

DSP支持 [!DNL ads.txt] 通过阅读每个出版商的 `ads.txt` 文件并提供仅从已验证客户处购买的选项 [!DNL ads.txt] 卖家。 例如，通过匹配销售者，我们看到访问 `nytimes.com` 《纽约时报》 `ads.txt` 文件，我们可以识别哪些是合法的，哪些是非法的，如果位置仅配置为从经过验证的卖家处购买，我们将阻止违法者。 <!-- can we actually mention NY Times? -->

您可以设置默认值 [!DNL ads.txt] 每个广告商的控件<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然后（可选） [自定义每个投放位置的设置](/help/dsp/campaign-management/placements/placement-settings.md) 至：

* 仅从域授权的直销商处购买库存

* 仅从域的授权直销人员和转销商购买库存

* 优先从域的授权直销商和经销商处购买库存

* 从所有卖家购买库存

### 平台欺诈监控

DSP与业界领先的供应商(如 [!DNL Whiteops] 和 [!DNL Integral Ad Science].

此外，Adobe还与 [!DNL IAB] 和 [!DNL TAG] 确保强大的行业标准欺诈拦截功能来保护我们的广告商，并利用以下工具 [!DNL ads.txt] （请参阅上一节）， [!DNL IAB] 机器人和蜘蛛列表，以及 [!DNL TAG] 数据中心IP列表。

我们的团队通过多维度质量方法监控异常和无效流量模式，确保受保护库存上的无效流量低于3%。 任何可疑的库存 — 包括特定域上的库存或者来自特定出版商或卖家的库存 — 都会立即在整个平台上被阻止。

### 库存映射、分层和分类

清单映射是在将新清单添加到我们的平台之前，对所有新清单所需的详细审查和载入流程。 此过程旨在确保DSP上所有库存的安全和质量。

* **映射：** 我们的库存团队仔细审查每个域，评估以下方面：

   * 品牌安全

   * 广告类型验证

   * 通用内容、重复域和虚假广告投放

* **分层：** 我们在整个生态系统中全面检查品牌的存在情况，以跨不同层分类库存。 您可以 [定位投放位置](/help/dsp/campaign-management/placements/placement-settings.md) 到这些层以获得所需的覆盖级别：

   * **[!UICONTROL T1]**  — 国际知名品牌网站

   * **[!UICONTROL T2]**  — 美观的站点，具有最新、最新、没有用户生成的内容，并且通常缺乏全球知名度

   * **[!UICONTROL T3]**  — 用户生成的内容和小范围内容

* **站点分类：** 为确保轻松定位和阻止内容，我们根据资产的内容使用DSP定义的网站类别来标记每个资产。 您可以 [为每个投放位置定位或排除这些站点类别](/help/dsp/campaign-management/placements/placement-settings.md) 基于投放目标。

### 全面支持站点阻止

DSP提供了全局阻止站点列表以及创建广告商和帐户的自定义阻止站点列表的选项。

#### DSP全局阻止的站点列表 {#global-blocked-sites}

DSP会维护一个全局阻止的站点列表，列出被认为不安全的站点以在其上运行广告。 此列表包含带有令人反感内容（例如仇恨或恐怖）的网站，以及被机器人、虚假预注册、不匹配的域和其他欺诈活动感染的网站。

作为我们根除欺诈广告商活动的品牌安全计划的一部分，将使用“阻止网站列表”图表中的措施对所有网站进行筛选。 所有未通过品牌安全检查的网站都会添加到全局阻止的网站列表中。 由于DSP动态管理此列表，因此根据最新的品牌安全分析，网站可以随时打开或关闭此列表。

如果将某个站点作为放置目标包含在全球阻止的站点列表中，则该站点会标有红色感叹号(！)。 这表示广告不会在标记的网站上运行。

>[!NOTE]
>
>您可以通过启用&#39;&#39;，选择性地绕过与受信任的私人交易关联的标准显示广告的全局阻止站点列表[!UICONTROL Allow unscreened sites]中的“ ”选项 [投放设置](/help/dsp/campaign-management/placements/placement-settings.md). 如有必要，Adobe帐户团队还可以选择在交易的发布者设置中为公共（拍卖级别）交易禁用网站阻止。

#### 帐户级别和广告商级别的阻止站点列表

用户还可以维护帐户级别和广告商级别的阻止站点列表<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->，自动用于所有投放。 除了全局阻止的站点列表之外，还应用较低级别的阻止的站点列表。

## 第三方集成

### 上下文过滤

上下文筛选允许您根据广告将投放的页面上下文来定位或阻止广告机会。 Adobe通过与行业领先供应商集成提供上下文过滤： [!DNL Comscore]， [!DNL DoubleVerify]， [!DNL Integral Ad Science]、和 [!DNL Peer39]. 当前过滤器的示例包括 [!UICONTROL Adult Content]， [!UICONTROL Natural Disasters]， [!UICONTROL Legal Drinking Age]， [!UICONTROL MANGA]， [!UICONTROL Epidemics]、和 [!UICONTROL G-rated Sites].

您可以为每个广告商设置默认的上下文过滤器控件<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然后（可选） [自定义每个投放位置的设置](/help/dsp/campaign-management/placements/placement-settings.md). 使用此功能时可能会收取额外费用。

![Comscore徽标](/help/dsp/assets/comscore-logo.png) ![DoubleVerify徽标](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science徽标](/help/dsp/assets/ias-logo.png) ![Peer39徽标](/help/dsp/assets/peer39-logo.png)

### 预竞价欺诈阻止

利用我们的第三方集成 [!DNL Comscore]， [!DNL DoubleVerify]， [!DNL Integral Ad Science]、和 [!DNL Peer39] 阻止非人为流量进入您的营销活动。 这些集成提供了行业领先的预竞价阻止功能，以最大限度地减少营销活动中的常规和复杂无效流量（GIVT和SIVT）。

您可以为每个广告商设置默认的竞价前欺诈阻止控制<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然后（可选） [自定义每个投放位置的设置](/help/dsp/campaign-management/placements/placement-settings.md). 使用此功能时可能会收取额外费用。

有关功能的更多信息，请直接联系您的首选供应商，或联系您的Adobe客户团队。

![Comscore徽标](/help/dsp/assets/comscore-logo.png) ![DoubleVerify徽标](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science徽标](/help/dsp/assets/ias-logo.png) ![Peer39徽标](/help/dsp/assets/peer39-logo.png)

### 预竞价可视性 {#pre-bid-viewability}

由我们行业领先合作伙伴提供支持的竞价前可见性过滤器 [!DNL DoubleVerify]， [!DNL Oracle Advertising] ([!DNL Moat])，和 [!DNL Integral Ad Science] 允许广告商确保其促销活动在视频和显示内容库中满足其所需的可见性性能目标。

您可以为每个广告商设置默认可见性过滤器<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然后（可选） [自定义每个投放位置的设置](/help/dsp/campaign-management/placements/placement-settings.md). 使用此功能时可能会收取额外费用。

![DoubleVerify徽标](/help/dsp/assets/doubleverify-logo.png) ![oracle广告徽标](/help/dsp/assets/oracle-advertising-logo.png) ![Integral Ad Science徽标](/help/dsp/assets/ias-logo.png)

### 主题定位

DSP主题定位允许您利用我们行业领先的上下文合作伙伴来定位或阻止关键词列表 [!DNL Comscore] 和 [!DNL Oracle Data Cloud] (以前称为 [!DNL Grapeshot])。 主题定位可帮助您确保始终在符合您品牌的环境中提供广告，包括阻止有害内容或确保在可确保获得更大结果的环境中支出。

主题定位要求您直接使用合作伙伴平台创建自定义主题区段。 创建区段后，您可以 [在中定位或排除区段ID [!UICONTROL Audience Targeting] 每个投放位置的区域](/help/dsp/campaign-management/placements/placement-settings.md). 此功能可能需要额外付费。

要创建自定义主题区段，请执行以下操作：

* 创建 [!DNL Comscore] 帐户和创建自定义区段，您可以请求登录 [!DNL Activation Segment Manager] 在 [https://agents.comscore.com](https://agents.comscore.com). 请参阅 [[!DNL Comscore] 帮助中心](https://comscoreactivation.zendesk.com/hc/) 有关设置自定义区段的完整说明。 在中可以查看自定义区段的费用 [!DNL Segment Manager] 创建它们时。

* 开始使用 [!DNL Oracle Data Cloud]，联系人 [!DNL Oracle Data Cloud] 或您的Adobe客户团队。

![Comscore徽标](/help/dsp/assets/comscore-logo.png) ![Grapeshot徽标](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP已与 [!DNL DoubleVerify] 以提供 [!DNL Authentic Brand Safety] 定位解决方案，可让您创建一组集中的品牌安全要求，以针对所有购买平台进行定位以实现一致性。

一旦构建了 [!DNL DoubleVerify] 具有必要定位的品牌安全区段，您可以在DSP中使用它来跨Web环境复制具有预竞价的竞价后块规则。

您可以指定 [!DNL DoubleVerify] 每个广告商的区段ID<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然后（可选） [启用或禁用 [!UICONTROL Authentic Brand Safety] 每个投放位置](/help/dsp/campaign-management/placements/placement-settings.md). DSP按区段ID对帐户开单。

有关功能的更多信息，请联系 [!DNL DoubleVerify] 或直接联系您的Adobe客户团队。

![DoubleVerify徽标](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [投放设置](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
