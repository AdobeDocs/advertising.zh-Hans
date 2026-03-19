---
title: 使用Adobe Advertising ID创建 [!DNL Marketing Channels] 规则
description: 了解如何使用Adobe Advertising ID为 [!DNL Analytics Marketing Channels]创建处理规则。
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 0813a8bddc1ecf238f4a62c4fcefd8584f32e152
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---

# 使用Adobe Advertising ID创建[!DNL Marketing Channels]处理规则

*仅集成Adobe Advertising-Adobe Analytics的广告商*

您可以使用Adobe Advertising ID （[AMO ID和EF ID](../ids.md)）在Adobe Analytics中配置[!DNL Marketing Channels]处理规则。 将Adobe Advertising ID用于特定于您的Adobe Advertising营销活动的规则。 处理规则的顺序决定了是否正确捕获了所有可能的数据。

## 处理规则中的AMO ID

AMO ID是用于报告[!DNL Analytics]中Adobe Advertising数据的主要跟踪代码。 AMO ID是由Adobe管理的动态值的连接，用于在[!DNL Analytics]内提供精细的报表。 它存储在[!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)或rVar维度(AMO ID)中。 可以通过两种方式在[!DNL Analytics]中设置AMO ID：

* 点进跟踪： Adobe Advertising在链接中设置了`s_kwcid`查询字符串参数，当发生点进时，[!DNL Analytics]会从登陆页面URL中选取该参数。

* 浏览跟踪（仅限[!DNL DSP]）： [!DNL Last Event Service]在服务器端检测到浏览并向[!DNL Analytics]发送AMO ID。 在这种情况下，URL不包含`s_kwcid`参数。

AMO ID中的动态值表示跟踪的营销渠道：

* AMO ID中的前缀可用于标识[!DNL Marketing Channels]中的顶级渠道。

* AMO ID正文中的字符短语表示更具体的促销活动类型。

* 后缀“vt”存在于[!DNL DSP]显示到达流量中，可用于创建单独的点进和显示到达[!DNL DSP]渠道。

可以忽略AMO ID的其余部分。

| [!UICONTROL AMO ID] | 渠道 | 规则逻辑 |
|--------|---------|--------------------|
| ！ctv（后缀） | [!UICONTROL DSP Connected TV ViewThrough] | 结尾为 |
| ！d！ （正文） | [!UICONTROL Display Network] | 包含 |
| ！g！ （正文） | [!UICONTROL Google Search] | 包含 |
| ！s！ （正文） | [!UICONTROL Search Partner] | 包含 |
| ！u！ （正文） | [!UICONTROL Smart Shopping Campaign] | 包含 |
| ！ytv！ （正文） | [!UICONTROL YouTube Video Ad] | 包含 |
| ！yts！ （正文） | [!UICONTROL YouTube Search Ad] | 包含 |
| ！vp！ （正文） | [!UICONTROL Google Video Partners] | 包含 |
| ！vt（后缀） | [!UICONTROL DSP ViewThrough] | 结尾为 |
| 艾尔！ （前缀） | [!UICONTROL Paid Search] | 开头为 |
| AC！ （前缀） | [!UICONTROL DSP Display] | 开头为 |

## 处理规则中的EF ID

AMO EF ID (EF ID)是[!DNL Analytics for Advertising]集成中使用的第二个跟踪代码。 其主要目的是跟踪[!DNL Analytics]事件数据并将其传递到Adobe Advertising。 每次发生点进或浏览时，都会生成一个唯一的EF ID，即使对于同一访客而言，该ID与同一广告完全相同。 [!DNL Analytics]报表用户界面中未使用EF ID，因为它通常超过[!DNL Analytics]中每个变量限制的500,000个唯一值，使其不可用于报表。 Adobe Advertising量度和元数据不应用于EF ID；而是仅应用于AMO ID。 在Adobe Advertising中优化促销活动需要添加的跟踪粒度，因此需要使用这两个ID。

虽然EF ID维度未直接在[!DNL Analytics]报表中使用，但EF ID可用于创建营销渠道。 EF ID后缀指示渠道（显示或搜索）以及访问是由点进还是显示到位驱动。 EF ID中的分隔符是冒号，而不是AMO ID中的感叹号。

| ef ID后缀 | 渠道 |
|-------|---------|
| :s | [!UICONTROL Paid Search Click-through] |
| :d | [!UICONTROL Display ClickThrough] |
| :i | [!UICONTROL Display ViewThrough] |

## Adobe Advertising处理规则的示例

以下示例规则集侧重于广告渠道（“付费搜索”、“显示点进”和“显示视图到达”）的规则。 此外，还演示了付费搜索检测的推荐规则（包括该规则如何与免费搜索营销渠道逻辑进行交互）以及免费反向链接域规则的可选更新。

**注意：**&#x200B;根据广告商的偏好，可以将显示区分为两个渠道或合并到单个渠道中。

在示例屏幕快照中包括了其他渠道，以说明广告渠道相对于典型实施中的其他渠道的推荐操作顺序。

>[!IMPORTANT]
>
>有关处理规则的顺序的信息，请参阅[规则 [!DNL Marketing Channels] 的](#rule-order)操作顺序。

![一组处理规则的示例](/help/integrations/assets/a4adc-mc-rule-set-example.png)

### 付费搜索规则

最佳实践是为[!UICONTROL Paid Search]规则包含两个带有“Any”运算符的条件：

* 成本/点击/展示数据包含AMO ID，因此请包含AMO ID。 AMO ID应以“AL！”开头 将点击/成本/展示数据正确分配给[!UICONTROL Paid Search].<!-- Is this just called AMO ID there, not s_kwcid=XXX? What's the difference? -->

* [!UICONTROL Paid Search]点进次数的URL始终包含`s_kwcid`查询字符串参数，因此请包含该参数，以确保在访客导航回登陆页面时执行正确的重复数据删除。 包括“AL！” ，以正确将click/cost/impression数据分配给`s_kwcid`。[!UICONTROL Paid Search]

不要将渠道值设置为AMO ID。 相反，请将其设置为反向链接域、搜索引擎+关键字或页面等。 （这与所有[!DNL Marketing Channels]相关）。

<!-- Explain that comment about relevancy -- do I need to repeat this for each rule example?  -->

![付费搜索规则示例](/help/integrations/assets/a4adc-mc-rule-paid-search.png "付费搜索规则示例")

### 免费搜索规则

对于[!UICONTROL Natural Search]，请确保您的[[!UICONTROL Paid Search]检测规则](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/t-paid-search-detection)包含`ef_id`和`s_kwcid`查询字符串参数。 （通常，当Advertising Search、Social和Commerce集成到[!DNL Analytics]中时会自动配置此项，但如果[!DNL Analytics]管理员在配置集成后更改了逻辑，请进行验证。）

将规则设置为“匹配免费搜索检测规则”（通常是此渠道的默认设置）。

![免费搜索规则示例](/help/integrations/assets/a4adc-mc-rule-natural-search.png "免费搜索规则示例")

### 显示点进规则#1

通过仅捕获点进次数来创建显示点进营销渠道。 由于点进和显示到达的AMO ID相同，因此此规则使用EF ID变量和`ef_id`查询字符串参数。

有时，点进次数通过URL（默认）进行跟踪。 在其他情况下，点进次数通过服务器端的Last Event Service进行跟踪，因此URL不包含`ef_id`参数。 因此，该规则会检查EF ID变量或`ef_id`查询字符串参数以“:d”结尾的条件。 使用“`Any`”运算符，因为您希望为任一条件触发此规则。

![第一个显示点进规则示例](/help/integrations/assets/a4adc-mc-rule-display-ct.png "第一个显示点进规则示例")

### 自然反向链接域规则

（可选）最佳实践是向标准[!UICONTROL Natural Referring Domains]规则添加一个包含“任意”运算符的“是访问的第一个页面”条件。 虽然此规则为可选规则，但它有助于防止在用户单击“返回”按钮返回登陆页面时设置自然反向链接的Edge情况。

![自然反向链接域规则示例](/help/integrations/assets/a4adc-mc-rule-natural-referring-domains.png "自然反向链接域规则示例")

### 显示CTV浏览规则

要跟踪[!DNL DSP]连接的电视(CTV)显示到达次数，请创建一个AMO ID以`"!ctv"`结尾的规则。 由于访客未单击广告，因此浏览跟踪在URL中不包含`ef_id`或`s_kwcid`，并且该规则只需要一个条件。

![显示CTV ViewThrough规则示例](/help/integrations/assets/a4adc-mc-rule-display-ctv-vt.png "显示CTV ViewThrough规则示例")

### 显示浏览规则

要创建显示ViewThrough渠道，请创建规则，其中EF ID以“:i”结尾。 由于访客未单击广告，因此浏览跟踪在URL中不包含`ef_id`或`s_kwcid`，并且该规则只需要一个条件。

![显示ViewThrough规则示例](/help/integrations/assets/a4adc-mc-rule-display-vt.png "显示ViewThrough规则示例")

### 显示点进规则#2

对于第二个显示点进规则，请将&#x200B;**AMO ID设置为“AC！”**。 存在第二条规则，用于捕获直接从Adobe Advertising进入[!DNL Analytics]的显示渠道的点击/成本/展示数据。 此数据归因于AMO ID，但不包括带有`ef_id`查询字符串的URL，因此这些点击不会与AMO EF ID关联，而该ID是第一个“显示点进”规则捕获的内容。

![第二个显示点进规则示例](/help/integrations/assets/a4adc-mc-rule-display-ct2.png "第二个显示点进规则示例")

## [!DNL Marketing Channels]规则的操作顺序 {#rule-order}

![Adobe Advertising相关规则的理想操作顺序](/help/integrations/assets/a4adc-mc-rule-order.png "Adobe Advertising相关规则的理想操作顺序")

* 将[!UICONTROL Paid Search] *放在* [!UICONTROL Natural Search]之前。 否则，可以将付费搜索数据分配给免费搜索。

* 将&#x200B;**第一个** [!UICONTROL Display ClickThrough] *放在* [!UICONTROL Natural Referring Domains]和[!UICONTROL Natural Social]之前。

* 当您使用[!UICONTROL CTV view-throughs]时，请将其放在&#x200B;*之前* [!UICONTROL Display ViewThroughs]。 否则，CTV显示到达次数将被捕获为Display ViewThrough。

* 将[!UICONTROL Display ViewThroughs] *放在*&#x200B;个其他渠道之后，但放在[!UICONTROL Internal]和[!UICONTROL Direct]之前，因为同一登陆事件中可能会发生显示到达和非[!DNL Advertising]点进。 例如，访客可能会看到Adobe Advertising广告，获得印象，然后通过[!UICONTROL Natural Search]访问网站。

  最佳实践是将其他渠道（除[!UICONTROL Internal]和[!UICONTROL Direct]之外）优先于显示到达次数。

* 某些广告商可能会选择将[!UICONTROL Display ViewThroughs]优先于[!UICONTROL Natural Referring Domains]。 通过交换两个规则的处理顺序来执行此操作。

* **second** [!UICONTROL Display ClickThrough]规则可用于捕获直接从Adobe Advertising进入[!DNL Analytics]的点击/成本/展示数据。 由于此数据仅归因于AMO ID，因此这些点击不会与AMO EF ID相关联。 如果不设置此规则，则所有点击/成本/展示数据都属于[!UICONTROL Direct]渠道，该渠道是不匹配[!DNL Marketing Channel]的任何数据的默认渠道。 此规则必须在&#x200B;*查看到达规则*&#x200B;之后出现，否则它将选取任何查看到达次数。

<!-- WORDING!!!!  Check on this, and if it's necessary still with the other info about order:  If you include additional marketing channels, be sure to run your rules in order of specificity. For example, say you create a processing rule for [!DNL YouTube] video ad traffic tracked by Advertising Search, Social, & Commerce. The AMO ID for video traffic starts with with "AL!" and contain "!ytv!". If you run the rule for Paid Search (for which the AMO ID starts with "AL!") and then run the rule for video traffic, the YouTube video ad traffic would all fall under the Paid Search channel. -->

>[!MORELIKETHIS]
>
>* [的 [!DNL Analytics Marketing Channels]](mc-overview.md)基础知识
>* [为什么渠道数据在Adobe Advertising和 [!DNL Marketing Channels]](mc-data-variances.md)之间可能不同
>* [对Adobe Advertising数据使用 [!DNL Analytics Marketing Channels] &#x200B;](mc-ac-data.md)
>* [视频：使用 [!DNL Marketing Channels] 进行Adobe Advertising报告](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [使用的 [!DNL Analytics]](/help/integrations/analytics/ids.md)Adobe Advertising ID