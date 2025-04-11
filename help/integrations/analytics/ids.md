---
title: ' [!DNL Analytics]使用的Adobe Advertising ID'
description: ' [!DNL Analytics]使用的Adobe Advertising ID'
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: e8c8316418acf4a8c62beabcae2c1b7388dbc297
workflow-type: tm+mt
source-wordcount: '1758'
ht-degree: 0%

---

# [!DNL Analytics]使用的Adobe Advertising ID

*仅集成Adobe Advertising-Adobe Analytics的广告商*

*适用于Advertising DSP和[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising使用两个ID进行现场性能跟踪： *EF ID*&#x200B;和&#x200B;*AMO ID*。

当出现广告展示时，Adobe Advertising会创建AMO ID和EF ID值并将其存储。 当看到广告的访客进入网站而未单击广告时，[!DNL Analytics]通过[!DNL Analytics for Advertising] JavaScript代码从Adobe Advertising调用这些值。 对于浏览流量，[!DNL Analytics]生成一个补充ID (`SDID`)，用于将EF ID和AMO ID拼合到[!DNL Analytics]中。 对于点进流量，这些ID将使用`ef_id`和`s_kwcid`（对于AMO ID）查询字符串参数包含在登陆页面URL中。

Adobe Advertising会使用以下标准来区分网站的点进或浏览条目：

* 当用户查看了广告但未单击该广告后访问网站时，将会捕获浏览进入条目。 如果满足两个条件，[!DNL Analytics]记录一次浏览：

   * 在[点击回顾窗口](#lookback-a4adc)期间，访客没有[!DNL DSP]或[!DNL Search, Social, & Commerce]广告的点进次数。

   * 在[展示回顾窗口](#lookback-a4adc)期间，访客已看到至少一个[!DNL DSP]广告。 最后一次展示作为显示到达传递。

* 当网站访客在进入网站之前单击广告时，将捕获点进条目。 出现以下任一情况时，[!DNL Analytics]会捕获点进：

   * 该URL包含由Adobe Advertising添加到登陆页面URL的EF ID和AMO ID。

   * URL不包含跟踪代码，但Adobe Advertising JavaScript代码可检测过去两分钟内发生的点击。

![Adobe Advertising基于视图的[!DNL Analytics]集成](/help/integrations/assets/a4adc-view-through-process.png)

*图1：基于Adobe Advertising视图的[!DNL Analytics]集成*

![Adobe Advertising单击基于URL的[!DNL Analytics]集成](/help/integrations/assets/a4adc-click-through-process.png)

*图2： Adobe Advertising单击基于URL的[!DNL Analytics]集成*

## ADOBE ADVERTISING EF ID

EF ID是一个唯一令牌，Adobe Advertising将其用于关联在线点击或广告曝光。 EF ID存储在[an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)或[!DNL rVar] （保留的[!DNL eVar]）维度(Adobe Advertising EF ID)中，并跟踪单个浏览器或设备级别的每次广告点击或曝光。 EF ID主要用作将[!DNL Analytics]数据发送到Adobe Advertising以在Adobe Advertising中优化报表和竞价的密钥。

### EF ID格式

>[!NOTE]
>
>EF ID区分大小写。 如果[!DNL Analytics]实施强制将URL跟踪转换为小写，则Adobe Advertising不会识别EF ID。 这会影响Adobe Advertising竞价和报表，但对[!DNL Analytics]内的Adobe Advertising报表没有影响。

#### [!DNL Google Ads]个搜索广告

```
{gclid}:G:s
```

其中：

* `gclid`是[!DNL Google Click ID] (GCLID)。
* `s`是网络类型（“s”用于搜索）。

#### [!DNL Microsoft Advertising]个搜索广告

```
{msclkid}:G:s
```

其中：

* `msclkid`是[!DNL Microsoft Click ID] (MSCLKID)。
* `s`是网络类型（“s”用于搜索）。

#### 在其他搜索引擎上显示广告和搜索广告

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

其中：

* &lt;*Adobe Advertising访客ID*>是每位访客的唯一标识（如UhKVaAABCkJ0mDt）。 也调用了&#x200B;*冲浪者ID*。

* &lt;*timestamp*>是格式为YYYYYMMDDHHMMSS的时间(例如，20190821192533用于2019年、月08、日21、时间19:25:33)。

* &lt;*渠道类型*>是负责点击或曝光的渠道类型：

   * `d`点击DSP显示广告（显示点进）
   * 针对DSP显示广告（显示显示显示到达）的展示的`i`
   * `s`搜索广告的点击（搜索点进）。

示例`EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### [!DNL Analytics]中的EF ID Dimension

在[!DNL Analytics]报表中，您可以通过搜索[!UICONTROL EF ID]维度并使用[!UICONTROL EF ID Instance]量度来查找EF ID数据。

EF ID受Analysis Workspace中500,000个唯一标识符限制的约束。 一旦达到500k值，所有新跟踪代码都会报告在单行项目标题“[!UICONTROL Low Traffic]”下。 由于可能缺少报表保真度，EF ID不会进行分类，您不应将它们用于[!DNL Analytics]中的区段或报表。

## ADOBE ADVERTISING AMO ID {#amo-id}

AMO ID在较低的粒度级别跟踪每个唯一的广告组合，用于从Adobe Advertising中[!DNL Analytics]数据分类和广告量度（例如展示次数、点击量和成本）的提取。 AMO ID存储在[!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)或rVar维度(AMO ID)中，仅用于[!DNL Analytics]中的报表。

AMO ID也称为`s_kwcid`，有时发音为“[!DNL squid]”。

### 实施AMO ID的方法 {#amo-id-implement}

参数可通过以下方式之一添加到您的跟踪URL中：

* （推荐）实施服务器端插入功能时。

   * DSP客户：当最终用户查看带有Adobe Advertising像素的显示广告时，像素服务器会自动将s_kwcid参数附加到您的登陆页后缀。

   * 搜索、社交和Commerce客户：

      * 对于已为帐户或营销活动启用[!UICONTROL Auto Upload]设置的[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户，当最终用户单击带有Adobe Advertising像素的广告时，像素服务器会自动将s_kwcid参数附加到您的登陆页后缀。

      * 对于其他广告网络，或禁用了[!UICONTROL Auto Upload]设置的[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户，请手动将该参数添加到您的[帐户级别的附加参数](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}，这些参数会将其附加到您的基本URL。

* 未实施服务器端插入功能时：

   * DSP客户： [JavaScript代码](javascript.md)会自动记录点进和显示点进。 当浏览器不支持第三方Cookie时，您仍然可以跟踪以下广告类型的基于点击的转化：

      * 对于[!DNL Flashtalking]广告标记，请手动插入每个“[将 [!DNL Analytics for Advertising] 宏附加到 [!DNL Flashtalking] 广告标记](/help/integrations/analytics/macros-flashtalking.md)”的其他宏。 **注意：**&#x200B;如果贵组织与[!DNL Flashtalking]直接合作，并且您使用数据传递宏收集位于`https://support.flashtalking.com%2Fhc%2Fen-us%2Farticles%2F4409808166419-Accessing-Data-Pass-Macros`的[!DNL Flashtalking]支持文档的点击数据，则不需要执行此过程。

      * 对于[!DNL Google Campaign Manager 360]广告标记，请手动插入每个“[将 [!DNL Analytics for Advertising] 宏附加到 [!DNL Google Campaign Manager 360] 广告标记](/help/integrations/analytics/macros-google-campaign-manager.md)”的其他宏。

   * 搜索、社交和Commerce客户：

      * 对于（[!DNL Google Ads]和[!DNL Microsoft Advertising]）广告，请手动将AMO ID参数添加到登陆页面后缀，最好在[帐户级别](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}添加，除非需要对各个帐户组件进行不同的跟踪。

      * 对于所有其他广告网络上的广告，请手动将AMO ID参数添加到您的[帐户级别的附加参数](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}，这会将其附加到您的基本URL。

要实施服务器端插入功能或确定最适合您的企业的选项，请联系您的Adobe客户团队。

### AMO ID格式 {#amo-id-formats}

#### [!DNL DSP]的AMO ID格式

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

其中：

* `AC`指示显示渠道。

* `{TM_AD_ID}`是Adobe Advertising生成的字母数字广告键。 它使用了广告的唯一标识符，并用作将Adobe Advertising实体元数据转换为可读[!DNL Analytics]维度的键。

* `{TM_PLACEMENT_ID}`是Adobe Advertising生成的字母数字放置键。 它使用了投放的唯一标识符，并用作将Adobe Advertising实体元数据转换为可读[!DNL Analytics]维度的键。

示例AMO ID： AC！iIMvXqlOa6Nia2lDvtgw！GrVv6o2oV2qQLjQiXLC7

#### 搜索、社交和Commerce广告的AMO ID格式 {#amo-id-format-search}

这些参数因广告网络而异，但以下参数是所有参数共有的：

* `AL`指示搜索渠道。<!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}`是分配给广告商的唯一用户ID。

* `{sid}`已被广告商广告网络帐户的数值ID替换：[!DNL Google Ads]的&#x200B;*3*，[!DNL Microsoft Advertising]的&#x200B;*10*，[!DNL Meta]的&#x200B;*45*，[!DNL Yahoo! Display Network]的&#x200B;*86*，[!DNL Naver]的&#x200B;*87*，[!DNL Baidu]的&#x200B;*88*，[!DNL Yandex]的&#x200B;*90*，*94* [!DNL Yahoo Native]的[!DNL Yahoo! Japan Ads]、*105*（已弃用）或[!DNL Pinterest]的&#x200B;*106*（已弃用）。

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!88!{creative}!{placement}!{keywordid}`

其中：

* `{creative}`是广告网络的唯一创意数字ID。
* `{placement}`是点击了广告的网站。
* `{keywordid}`是触发广告的关键字的广告网络的唯一数值ID。

##### [!DNL Google Ads]

包括使用[!DNL Google Merchant Center]的购物营销活动。

* 使用最新AMO ID格式（支持营销活动和广告组级别报表以实现最佳效果营销活动以及草稿和实验营销活动）的帐户：

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* 所有其他帐户：

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

其中：

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}`是创意的[!DNL Google Ads]唯一数字ID。
* `{matchtype}`是触发广告的关键字的匹配类型：精确为`e`，短语为`p`，广泛为`b`。
* `{placement}`是广告被点击网站的域名。 值适用于以投放位置为目标的促销活动中的广告，以及内容网站上显示的以关键词为目标的促销活动中的广告。
* `{network}`指示发生点击的网络：[!DNL Google]搜索的`g`（仅关键词定向广告）、`s`搜索合作伙伴的（仅关键词定向广告）或显示网络的`d`（关键词定向或投放目标广告）。
* `{product_partition_id}`是与产品广告一起使用的产品组的广告网络的唯一数值ID。
* `{keyword}`是触发您的广告的特定关键词（在搜索网站上）或最佳匹配关键词（在内容网站上）。
* `{campaignid}`是广告网络的营销活动唯一数字ID。
* `{adgroupid}`是广告组的广告网络的唯一数字ID。

>[!NOTE]
>
>* 对于动态搜索广告，{keyword}填充了自动定位。
>* 当您为[!DNL Google]购物广告生成跟踪时，产品ID参数`{adwords_producttargetid}`将插入到关键词参数之前。 产品ID参数未出现在[!DNL Google Ads]帐户级别和营销活动级别的跟踪参数中。
>* 若要使用最新的AMO ID跟踪代码，请参阅“[更新 [!DNL Google Ads] 帐户](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)的AMO ID跟踪代码”<!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!45!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* 所有营销活动类型：

  `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}`

其中：

* `{AdId}`是广告网络的唯一创意数字ID。
* `{OrderItemId}`是关键词的广告网络的数字ID。
* `{CampaignId}`是广告网络的营销活动唯一数字ID。
* `{AdGroupId}`是广告组的广告网络的唯一数字ID。

>[!NOTE]
>
> 对于其营销活动没有[!UICONTROL Auto Upload]跟踪选项且尚未迁移到新格式的帐户，请手动更新每个登陆页面后缀以包含上述格式。
>与此同时，旧版格式（如下所示）仍然有效：
>* 搜索促销活动：
>  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* 购物营销活动（使用[!DNL Microsoft Merchant Center]）：
>  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* 受众网络营销活动：
>  `s_kwcid=AL!{userid}!10!{AdId}`

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!94!{creative}!{matchtype}!{network}!{keyword}`

其中：

* `{creative}`是广告网络的唯一创意数字ID。
* `{matchtype}`是触发广告的关键字的匹配类型：精确为`be`，短语为`bp`，广泛为`bb`。
* `{network}`指示发生点击的网络： `n`用于本机，或`s`用于搜索。
* `{keyword}`是触发广告的关键字。

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!90!{ad_id}!{source_type}!!!{phrase_id}`

其中：

* `{ad_id}`是广告网络的唯一创意数字ID。
* `{source_type}`是显示广告的网站类型：搜索为&#x200B;*b*，上下文（内容）为&#x200B;*c*，类别为&#x200B;*ct*。
* `{phrase_id}`是关键词的广告网络的数字ID。

### [!DNL Analytics]中的AMO ID Dimension

在Analytics报表中，您可以通过搜索[!UICONTROL AMO ID]维度并使用[!UICONTROL AMO ID Instances]量度来查找AMO ID数据。 [!UICONTROL AMO ID]维度包含捕获的所有AMO ID值，而[!UICONTROL AMO ID Instances]量度表示网站捕获AMO ID值的频率。 例如，如果同一搜索广告被点击四次，但Analytics跟踪了七个网站条目，则[!UICONTROL AMO ID Instances]将是七(7)，[!UICONTROL Clicks]将是四(4)。

对于[!DNL Analytics]内的任何报表或审核，最佳实践是将AMO ID与其相应的实例结合使用。 有关详细信息，请参阅“在[!DNL Analytics]和Adobe Advertising之间的预期数据差异”中的“[针对 [!DNL Analytics for Advertising]](data-variances.md#data-validation)的点进数据验证”。

## 关于Analytics分类

在[!DNL Analytics]中，[分类](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html)是给定跟踪代码（如帐户、促销活动或广告）的元数据。 Adobe Advertising使用分类对原始Adobe Advertising数据进行分类，以便在生成报表时能够以不同的方式（例如按广告类型或促销活动）显示数据。 分类构成了[!DNL Analytics]中Adobe Advertising报表的基础，可与AMO指标（如[!UICONTROL Adobe Advertising Cost]、[!UICONTROL Adobe Advertising Impressions]和[!UICONTROL AMO Clicks]）以及自定义和标准现场事件（如[!UICONTROL Visits]、[!UICONTROL Leads]、[!UICONTROL Orders]和[!UICONTROL Revenue]）一起使用。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [在 [!DNL Analytics] 和Adobe Advertising](data-variances.md)之间的预期数据差异
