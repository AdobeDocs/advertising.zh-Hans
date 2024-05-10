---
title: 使用的Adobe AdvertisingID [!DNL Analytics]
description: 使用的Adobe AdvertisingID [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1684'
ht-degree: 0%

---

# 使用的Adobe AdvertisingID [!DNL Analytics]

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

*适用于Advertising DSP和[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising使用两个ID进行网站上的性能跟踪： *EF ID* 和 *AMO ID*.

当出现广告展示时，Adobe Advertising会创建AMO ID和EF ID值并将其存储。 当查看过广告的访客未单击广告而进入网站时， [!DNL Analytics] 通过Adobe Advertising调用这些值 [!DNL Analytics for Advertising] JavaScript代码 对于显示到达流量， [!DNL Analytics] 生成补充ID (`SDID`)，用于将EF ID和AMO ID拼合到 [!DNL Analytics]. 对于点进流量，使用将这些ID包含在登陆页面URL中 `ef_id` 和 `s_kwcid` （对于AMO ID）查询字符串参数。

Adobe Advertising使用以下条件区分网站的点进或浏览条目：

* 当用户查看了广告但未单击该广告后访问网站时，将会捕获浏览进入条目。 [!DNL Analytics] 如果满足两个条件，则记录一次浏览：

   * 访客没有针对的点进次数 [!DNL DSP] 或 [!DNL Search, Social, & Commerce] 广告时段 [单击回顾窗口](#lookback-a4adc).

   * 访客已看到至少一个 [!DNL DSP] 广告时段 [展示回顾窗口](#lookback-a4adc). 最后一次展示作为显示到达传递。

* 当网站访客在进入网站之前单击广告时，将捕获点进条目。 [!DNL Analytics] 出现以下任一情况时捕获点进：

   * 该URL包含由Adobe Advertising添加到登陆页面URL的EF ID和AMO ID。

   * 该URL不包含跟踪代码，但Adobe AdvertisingJavaScript代码会检测前两分钟内的点击量。

![基于Adobe Advertising视图 [!DNL Analytics] 集成](/help/integrations/assets/a4adc-view-through-process.png)

*图1：基于Adobe Advertising视图 [!DNL Analytics] 集成*

![Adobe Advertising点击基于URL [!DNL Analytics] 集成](/help/integrations/assets/a4adc-click-through-process.png)

*图2：Adobe Advertising基于URL的点击 [!DNL Analytics] 集成*

## ADOBE ADVERTISINGEF ID

EF ID是一个唯一令牌，Adobe Advertising可使用它将Activity与在线点击或广告曝光度关联。 EF ID存储在中 [一个 [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或 [!DNL rVar] (已保留 [!DNL eVar])维度(Adobe AdvertisingEF ID)进行跟踪，并跟踪在单个浏览器或设备级别出现的每次广告点击或曝光。 EF ID主要用作发送的键 [!DNL Analytics] 用于Adobe Advertising中的报表和竞价优化的Adobe Advertising数据。

### EF ID格式

>[!NOTE]
>
>EF ID区分大小写。 如果 [!DNL Analytics] 实施强制URL跟踪为小写，然后Adobe Advertising无法识别EF ID。 这会影响Adobe Advertising竞价和报表，但不会影响中的Adobe Advertising报表 [!DNL Analytics].

#### [!DNL Google Ads] 搜索广告

```
{gclid}:G:s
```

其中：

* `gclid` 是 [!DNL Google Click ID] (GCLID)。
* `s` 是网络类型（“s”表示搜索）。

#### [!DNL Microsoft Advertising] 搜索广告

```
{msclkid}:G:s
```

其中：

* `msclkid` 是 [!DNL Microsoft Click ID] (MSCLKID)。
* `s` 是网络类型（“s”表示搜索）。

#### 在其他搜索引擎上显示广告和搜索广告

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

其中：

* &lt;*Adobe Advertising访客ID*>是每个访客的唯一ID（例如UhKVaAABCkJ0mDt）。 也称为 *冲浪者ID*.

* &lt;*时间戳*>是采用YYYYMMDDHHMMSS格式的时间(例如，20190821192533 for Year 2019， Month 08， Day 21， Time 19:25:33)。

* &lt;*渠道类型*>是造成点击或曝光的渠道类型：

   * `d` (表示点击DSP显示广告（显示点进）
   * `i` 对于DSP展示广告的展示（展示展示展示到达）
   * `s` （搜索点进）。

示例 `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### 中的EF IDDimension [!DNL Analytics]

在 [!DNL Analytics] 报表中，您可以通过搜索 [!UICONTROL EF ID] 维并使用 [!UICONTROL EF ID Instance] 量度。

EF ID受Analysis Workspace中500,000个唯一标识符限制的约束。 一旦达到500k值，所有新跟踪代码都会报告在单行项目标题&#39;&#39;下[!UICONTROL Low Traffic]“ 由于可能会丢失报表保真度，因此EF ID不会进行分类，您不应将它们用于中的区段或报表 [!DNL Analytics].

## ADOBE ADVERTISINGAMO ID {#amo-id}

AMO ID在较低的粒度级别跟踪每个唯一的广告组合，用于 [!DNL Analytics] 数据分类和从Adobe Advertising摄取广告量度（例如展示次数、点击量和成本）。 AMO ID存储在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar维度(AMO ID)，专门用于在以下位置生成报表： [!DNL Analytics].

AMO ID也称为 `s_kwcid`，有时发音为“[!DNL the squid]“

### 实施AMO ID的方法 {#amo-id-implement}

参数可通过以下方式之一添加到您的跟踪URL中：

* （推荐）实施服务器端插入功能时。

   * DSP客户：当最终用户查看带有Adobe Advertising像素的显示广告时，像素服务器会自动将s_kwcid参数附加到登陆页面后缀。

   * 搜索、社交和Commerce客户：

      * 对象 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 帐户具有 [!UICONTROL Auto Upload] 为帐户或营销活动启用的设置，当最终用户单击带有Adobe Advertising像素的广告时，像素服务器会自动将s_kwcid参数附加到您的登陆页后缀。

      * 对于其他广告网络，或 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 帐户具有 [!UICONTROL Auto Upload] 设置已禁用，手动将参数添加到您的 [帐户级别的附加参数](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}，以将其附加到基本URL中。

* 未实施服务器端插入功能时：

   * DSP客户： [JavaScript代码](javascript.md) 自动记录点进和显示点进。 当浏览器不支持第三方Cookie时，您仍然可以跟踪以下广告类型的基于点击的转化：

      * 对象 [!DNL Flashtalking] 添加标记，手动为每个&#39;&#39;插入其他宏[附加 [!DNL Analytics for Advertising] 宏到 [!DNL Flashtalking] 广告标记](/help/integrations/analytics/macros-flashtalking.md)“

      * 对象 [!DNL Google Campaign Manager 360] 添加标记，手动为每个&#39;&#39;插入其他宏[附加 [!DNL Analytics for Advertising] 宏到 [!DNL Google Campaign Manager 360] 广告标记](/help/integrations/analytics/macros-google-campaign-manager.md)“

   * 搜索、社交和Commerce客户：

      * 对于([!DNL Google Ads] 和 [!DNL Microsoft Advertising])广告，请手动将AMO ID参数添加到登陆页面后缀，最好在 [帐户级别](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} 除非需要对各个帐户组件进行不同的跟踪。

      * 对于所有其他广告网络上的广告，请手动将AMO ID参数添加到您的 [帐户级别的附加参数](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}，以将其附加到基本URL中。

要实施服务器端插入功能，或确定最适合您企业的选项，请与您的Adobe客户团队联系。

### AMO ID格式 {#amo-id-formats}

#### AMO ID格式 [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

其中：

* `AC` 指示显示渠道。

* `{TM_AD_ID}` 是Adobe Advertising生成的字母数字广告键。 它使用广告的唯一标识符，并用作将Adobe Advertising实体元数据转换为可读数据的键 [!DNL Analytics] 维度。

* `{TM_PLACEMENT_ID}` 是Adobe Advertising生成的字母数字放置键。 它使用投放的唯一标识符，并用作将Adobe Advertising实体元数据转换为可读的键值 [!DNL Analytics] 维度。

示例AMO ID： AC！iIMvXqlOa6Nia2lDvtgw！GrVv6o2oV2qQLjQiXLC7

#### 搜索、社交和Commerce广告的AMO ID格式 {#amo-id-format-search}

这些参数因广告网络而异，但以下参数是所有参数共有的：

* `AL` 指示搜索渠道。 <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` 是分配给广告商的唯一用户ID。

* `{sid}` 将由广告商广告网络帐户的数值ID替换： *3* 对象 [!DNL Google Ads]， *10* 对象 [!DNL Microsoft Advertising]， *45* 对象 [!DNL Meta]， *86* 对象 [!DNL Yahoo! Display Network]， *87* 对象 [!DNL Naver]， *88* 对象 [!DNL Baidu]， *90* 对象 [!DNL Yandex]， *94* 对象 [!DNL Yahoo! Japan Ads]， *105* 对象 [!DNL Yahoo Native] （已弃用），或 *106* 对象 [!DNL Pinterest] （已弃用）。

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

其中：

* `{creative}` 是广告网络的创意唯一数字ID。
* `{placement}` 是点击了广告的网站。
* `{keywordid}` 是触发广告的关键字对应的广告网络的唯一数值ID。

##### [!DNL Google Ads]

其中包括使用的购物营销活动 [!DNL Google Merchant Center].

* 使用最新AMO ID格式（支持营销活动和广告组级别报表以实现最佳效果营销活动以及草稿和实验营销活动）的帐户：

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* 所有其他帐户：

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

其中：

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` 是 [!DNL Google Ads] 创意内容的唯一数值ID。
* `{matchtype}` 是触发广告的关键字的匹配类型： `e` 确切地说， `p` 用于短语，或 `b` 对布洛德来说。
* `{placement}` 是广告被点击的网站的域名。 值适用于以投放位置为目标的促销活动中的广告，以及内容网站上显示的以关键词为目标的促销活动中的广告。
* `{network}` 指示发生单击的网络： `g` 对象 [!DNL Google] 搜索（仅适用于以关键词为目标的广告）， `s` （仅适用于关键词定向广告），或 `d` 适用于展示网络（适用于关键词定向或投放定向广告）。
* `{product_partition_id}` 是用于产品广告的产品组的广告网络的唯一数值ID。
* `{keyword}` 是触发广告的特定关键词（在搜索网站上）或最佳匹配关键词（在内容网站上）。
* `{campaignid}` 是营销活动的广告网络的唯一数字ID。
* `{adgroupid}` 是广告组的广告网络的唯一数字ID。

>[!NOTE]
>
>* 对于动态搜索广告， {keyword} 使用自动定位填充。
>* 在为生成跟踪时 [!DNL Google] 购物广告、产品ID参数、 `{adwords_producttargetid}`，，插入在keyword参数之前。 产品ID参数未出现在 [!DNL Google Ads] 帐户级别和促销活动级别的跟踪参数。
>* 要使用最新的AMO ID跟踪代码，请参阅[更新的AMO ID跟踪代码 [!DNL Google Ads] 帐户](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)“ <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* 搜索促销活动：

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* 购物营销活动(使用 [!DNL Microsoft Merchant Center])：

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* 受众网络营销活动：

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

其中：

* `{AdId}` 是广告网络的创意唯一数字ID。
* `{OrderItemId}` 是关键词的广告网络的数字ID。
* `{CriterionId}` 是用于产品广告的产品组的广告网络的数字ID。

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

其中：

* `{creative}` 是广告网络的创意唯一数字ID。
* `{matchtype}` 是触发广告的关键字的匹配类型： `be` 确切地说， `bp` 用于短语，或 `bb` 对布洛德来说。
* `{network}` 指示发生单击的网络： `n` （本机或） `s` 进行搜索。
* `{keyword}` 是触发广告的关键字。

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

其中：

* `{ad_id}` 是广告网络的创意唯一数字ID。
* `{source_type}` 显示广告的网站类型： *b* 搜索时， *c* 用于上下文（内容），或 *ct* 类别。
* `{phrase_id}` 是关键词的广告网络的数字ID。

### 中的AMO IDDimension [!DNL Analytics]

在Analytics报表中，您可以通过搜索 [!UICONTROL AMO ID] 维并使用 [!UICONTROL AMO ID Instances] 量度。 此 [!UICONTROL AMO ID] 维度包含捕获的所有AMO ID值，而 [!UICONTROL AMO ID Instances] 量度表示网站捕获AMO ID值的频率。 例如，如果同一搜索广告被点击四次，但Analytics跟踪了七个网站条目，则 [!UICONTROL AMO ID Instances] 将会是七(7)和 [!UICONTROL Clicks] 就是四(4)

对于中的任何报告或审核，在 [!DNL Analytics]，最佳做法是将AMO ID与其相应的实例结合使用。 有关更多信息，请参阅&quot;[的点进数据验证 [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot;预期数据差异： [!DNL Analytics] 和Adobe Advertising。”

## 关于Analytics分类

在 [!DNL Analytics]， a [分类](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) 是给定跟踪代码（如帐户、促销活动或广告）的元数据。 Adobe Advertising使用分类对原始Adobe Advertising数据进行分类，以便在生成报表时能够以不同的方式（例如按广告类型或促销活动）显示数据。 分类构成了Adobe Advertising报表的基础 [!DNL Analytics] 并且可以与AMO量度一起使用，例如 [!UICONTROL Adobe Advertising Cost]， [!UICONTROL Adobe Advertising Impressions]、和 [!UICONTROL AMO Clicks]，以及自定义和标准的现场事件，例如 [!UICONTROL Visits]， [!UICONTROL Leads]， [!UICONTROL Orders]、和 [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [之间的预期数据差异 [!DNL Analytics] 和Adobe Advertising](data-variances.md)
