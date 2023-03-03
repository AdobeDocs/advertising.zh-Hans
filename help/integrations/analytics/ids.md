---
title: 使用的Adobe广告ID [!DNL Analytics]
description: 使用的Adobe广告ID [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 0%

---

# 使用的Adobe广告ID [!DNL Analytics]

*仅具有AdobeAdvertising-Adobe Analytics集成的广告商*

*适用于Advertising DSP和[!DNL Advertising Search]*

Adobe广告使用两个ID进行网站上的效果跟踪： *EF ID* 和 *AMO ID*.

当出现广告展示时，Adobe广告会创建AMO ID和EF ID值并将其存储。 当已查看广告的访客未单击广告而进入网站时， [!DNL Analytics] 通过Adobe广告调用这些值 [!DNL Analytics for Advertising] JavaScript代码 对于显示到达流量， [!DNL Analytics] 生成补充ID (`SDID`)，用于将EF ID和AMO ID拼合到 [!DNL Analytics]. 对于点进流量，使用将这些ID包含在登陆页面URL中 `s_kwcid` 和 `ef_id` 查询字符串参数。

Adobe广告使用以下条件区分网站的点进或浏览进入条目：

* 当用户查看了广告但未单击该广告后访问网站时，将捕获浏览进入条目。 [!DNL Analytics] 如果满足两个条件，则记录一次浏览：
   * 访客没有针对的点进次数 [!DNL DSP] 或 [!DNL Search] 广告时段 [单击回顾窗口](#lookback-a4adc).
   * 访客已看到至少一个 [!DNL DSP] 广告时段 [展示回顾窗口](#lookback-a4adc). 最后一次展示作为显示到达传递。
* 当网站访客在进入网站之前单击广告时，将捕获点进条目。 [!DNL Analytics] 在以下任一情况发生时捕获点进：
   * 该URL包含由Adobe广告添加到登陆页面URL的EF ID和AMO ID。
   * URL不包含跟踪代码，但AdobeAdvertising JavaScript代码可检测过去两分钟内的点击量。

![基于Adobe广告视图 [!DNL Analytics] 集成](/help/integrations/assets/a4adc-view-through-process.png)

*图1：基于Adobe广告视图 [!DNL Analytics] 集成*

![Adobe广告点击基于URL [!DNL Analytics] 集成](/help/integrations/assets/a4adc-click-through-process.png)

*图2：Adobe广告点击基于URL [!DNL Analytics] 集成*

## Adobe广告EF ID

EF ID是Adobe广告用于将活动与在线点击或广告曝光度关联的唯一令牌。 EF ID存储在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar(保留eVar)维度(Adobe广告EF ID)，并跟踪单个浏览器或设备级别的每个广告点击或曝光。 EF ID主要用作发送的密钥 [!DNL Analytics] 用于Adobe广告的数据，以便在Adobe广告中优化报表和竞价。

### EF ID格式

>[!NOTE]
>
>EF ID区分大小写。 如果 [!DNL Analytics] 实施强制URL跟踪为小写，然后Adobe广告将无法识别EF ID。 这将影响Adobe广告的竞价和报表，但不会影响Adobe广告报表中的 [!DNL Analytics].

#### [!DNL Google Ads] 搜索广告

```
{gclid}:G:s
```

其中：

* `gclid` 是 [!DNL Google Click ID] (GCLID)。
* `s` 是网络类型（“s”表示搜索）。

#### Microsoft Advertising搜索广告

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

* &lt;*Adobe的广告访客ID*>是每位访客的唯一ID（例如UhKVaAAABCkJ0mDt）。 也称为 *冲浪者ID*.

* &lt;*时间戳*>是采用YYYYMMDDHHMMSS格式的时间(例如，20190821192533为2019年、月8日、第21天、时间19):25:33)。

* &lt;*渠道类型*>是造成点击或曝光的渠道类型：

   * `d` 单击DSP显示广告（显示点进）
   * `i` 用于展示DSP展示型广告（展示浏览次数）
   * `s` （搜索点进）。

示例 `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### 中的EF IDDimension [!DNL Analytics]

In [!DNL Analytics] 报表中，您可以通过搜索 [!UICONTROL EF ID] 维并使用 [!UICONTROL EF ID Instance] 量度。

EF ID受Analysis Workspace中500,000个唯一标识符限制的约束。 一旦达到500k值，所有新的跟踪代码都会报告在一行项目标题下&quot;[!UICONTROL Low Traffic].” 由于可能会丢失报表保真度，因此EF ID不会进行分类，您不应将它们用于中的区段或报表 [!DNL Analytics].

## Adobe广告AMO ID

AMO ID在粒度较低的级别跟踪每个唯一的广告组合，用于 [!DNL Analytics] 数据分类以及从Adobe广告引入广告量度（例如展示次数、点击量和成本）。 AMO ID存储在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar维度(AMO ID)，专门用于在以下位置生成报表： [!DNL Analytics].

AMO ID也称为 `s_kwcid`，有时发音为“[!DNL the squid].”

### AMO ID格式 [!DNL DSP]

```
<Channel ID>!<Ad ID>!<Placement ID>
```

其中：

* &lt;*渠道ID*>可以是：

   * `AC` = Advertising DSP
   * `AL` 对象 [!DNL Advertising Search]

* &lt;*广告ID*>用作Adobe广告生成的广告唯一标识符。 它是将Adobe广告实体元数据转换为可读元数据的键 [!DNL Analytics] 维度。

* &lt;*版面ID*>是Adobe广告生成的投放位置唯一标识符。 它是将Adobe广告实体元数据转换为可读元数据的键 [!DNL Analytics] 维度。

示例AMO ID： AC！iIMvXqlOa6Nia2lDvtgw！GrVv6o2oV2qQLjQiXLC7

### AMO ID格式 [!DNL Search]

的AMO ID [!DNL Search] 遵循每个搜索引擎的不同格式。 所有搜索引擎的格式均以下列内容开头：

```
AL!{userid}!{sid}
```

其中：

* `AL` 是广告网络的渠道ID。
* `{userid}` 是Adobe广告分配给广告商的唯一数字用户ID。
* `{sid}` 是Adobe广告用于指定广告网络的数值ID，例如 `3` 对象 [!DNL Google Ads] 或 `10` 对象 [!DNL Microsoft Advertising].

以下是几个广告网络的完整AMO ID格式。 有关其他广告网络的AMO ID格式，请联系您的Adobe客户团队。

AMO ID格式 [!DNL Google Ads]：

```
AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

其中：

* `{creative}` 是 [!DNL Google Ads] 创意的唯一数值ID。
* `{matchtype}` 是触发广告的关键字的匹配类型： `e` 确切地说， `p` 用于短语，或 `b` 对布洛德来说。
* `{placement}` 是被点击广告的网站的域名。 值适用于以投放位置为目标的促销活动中的广告，以及内容网站上显示的以关键词为目标的促销活动中的广告。
* `{network}` 指示发生点击的网络：  `g` 对象 [!DNL Google] 搜索（仅适用于关键词定向广告）， `s` （仅适用于关键词定向广告），或 `d` （针对关键词或投放位置定向广告）的显示网络。
* `{keyword}` 是触发广告的特定关键词（在搜索网站上）或最佳匹配关键词（在内容网站上）。

AMO ID格式 [!DNL Microsoft Advertising]：

```
AL!{userid}!{sid}!{AdId}!{OrderItemId}
```

其中：

* `{AdId}` 是 [!DNL Microsoft Advertising] 创意的唯一数值ID。
* `{OrderItemId}` 是 [!DNL Microsoft Advertising] 关键字的数值ID。

### 中的AMO IDDimension [!DNL Analytics]

在Analytics报表中，您可以通过搜索 [!UICONTROL AMO ID] 维并使用 [!UICONTROL AMO ID Instance] 量度。 此 [!UICONTROL AMO ID] dimension包含捕获的所有AMO ID值，而 [!UICONTROL AMO ID Instance] 量度表示网站捕获AMO ID值的频率。 例如，如果同一搜索广告被点击四次，但Analytics跟踪了七个网站条目，则 [!UICONTROL AMO ID Instance] 将会是七(7)和 [!UICONTROL Clicks] 就是四(4)。

对于中的任何报告或审核 [!DNL Analytics]，最佳做法是将AMO ID与其相应的实例结合使用。 有关更多信息，请参阅“[数据验证 [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot;在&quot;预期数据差异，介于 [!DNL Analytics] 以及Adobe广告。”

## 关于Analytics分类

In [!DNL Analytics]， a [分类](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) 是给定跟踪代码（如帐户、促销活动或广告）的元数据段。 Adobe广告使用分类对原始Adobe广告数据进行分类，以便在生成报表时能够以不同的方式（例如按广告类型或促销活动）显示数据。 分类构成了Adobe广告报表的基础 [!DNL Analytics] 并且可以与AMO量度一起使用，例如 [!UICONTROL AMO Cost]， [!UICONTROL AMO Impressions]、和 [!UICONTROL AMO Clicks]，以及自定义和标准现场事件，例如 [!UICONTROL Visits]， [!UICONTROL Leads]， [!UICONTROL Orders]、和 [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [之间的预期数据差异 [!DNL Analytics] 和Adobe广告](data-variances.md)

