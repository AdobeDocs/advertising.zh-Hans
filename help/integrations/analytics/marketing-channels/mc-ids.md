---
title: 使用Adobe AdvertisingID创建 [!DNL Marketing Channels] 规则
description: 了解如何使用Adobe AdvertisingID为 [!DNL Analytics Marketing Channels]创建处理规则。
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 96a0add168c7fb7a6d80cf1b81ef4b315fbba89f
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# 使用Adobe AdvertisingID创建[!DNL Marketing Channels]处理规则

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

您可以使用Adobe AdvertisingID （[AMO ID和EF ID](../ids.md)）在Adobe Analytics中配置[!DNL Marketing Channels]处理规则。 将Adobe AdvertisingID用于特定于您的Adobe Advertising促销活动的规则。

## 处理规则中的AMO ID

AMO ID是用于报告[!DNL Analytics]中Adobe Advertising数据的主要跟踪代码。 AMO ID是由Adobe管理的动态值的连接，用于在[!DNL Analytics]内提供精细报表。 它存储在[!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)或rVar维度(AMO ID)中。 可以通过两种方式在[!DNL Analytics]中设置AMO ID：

* 点进跟踪：Adobe Advertising在链接中设置了`s_kwcid`查询字符串参数，当发生点进时，[!DNL Analytics]会从登陆页面URL中选取该参数。
* 浏览跟踪（仅限[!DNL DSP]）： Last Event Service在服务器端检测到浏览并向[!DNL Analytics]发送AMO ID。 在这种情况下，URL不包含`s_kwcid`参数。

AMO ID中的动态值表示跟踪的营销渠道：

* AMO ID中的前缀可用于标识[!DNL Marketing Channels]中的顶级渠道。

* AMO ID正文中的字符短语表示更具体的促销活动类型。

* 后缀“vt”存在于[!DNL DSP]显示到达流量中，可用于创建单独的点进和显示到达[!DNL DSP]渠道。

可以忽略AMO ID的其余部分。

| [!UICONTROL AMO ID] | 渠道 | 规则逻辑 |
|--------|---------|--------------------|
| ！ctv（后缀） | [!UICONTROL DSP Connected TV View-through] | 结尾为 |
| ！d！ （正文） | [!UICONTROL Display Network] | 包含 |
| ！g！ （正文） | [!UICONTROL Google Search] | 包含 |
| ！s！ （正文） | [!UICONTROL Search Partner] | 包含 |
| ！u！ （正文） | [!UICONTROL Smart Shopping Campaign] | 包含 |
| ！ytv！ （正文） | [!UICONTROL YouTube Video Ad] | 包含 |
| ！yts！ （正文） | [!UICONTROL YouTube Search Ad] | 包含 |
| ！vp！ （正文） | [!UICONTROL Google Video Partners] | 包含 |
| ！vt（后缀） | [!UICONTROL DSP View-through] | 结尾为 |
| 艾尔！ （前缀） | [!UICONTROL Paid Search] | 开头为 |
| AC！ （前缀） | [!UICONTROL DSP] | 开头为 |

### 使用AMO ID的处理规则示例

[!UICONTROL Paid Search]渠道的[!DNL Marketing Channels]处理规则可能如下所示：

![示例[!UICONTROL Paid Search]规则](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

[!UICONTROL YouTube Video Ads]渠道的[!DNL Marketing Channels]处理规则可能如下所示：

![示例[!UICONTROL YouTube Video Ads]规则](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> 请确保按具体顺序运行规则。 如果以上两个规则按顺序运行，[!DNL YouTube]视频广告流量将全部归入[!UICONTROL Paid Search]渠道下，因为AMO ID将以“AL！”开头。 并包含“！ytv！”。

## 处理规则中的EF ID

AMO EF ID (EF ID)是[!DNL Analytics for Advertising]集成中使用的第二个跟踪代码。 其主要目的是跟踪并将[!DNL Analytics]事件数据传递到Adobe Advertising。 每次发生点进或浏览时，都会生成一个唯一的EF ID，即使对于同一访客而言，该ID与同一广告完全相同。 [!DNL Analytics]报表用户界面中未使用EF ID，因为它通常超过[!DNL Analytics]中每个变量限制的500,000个唯一值，使其不可用于报表。 Adobe Advertising量度和元数据不应用于EF ID；而是仅应用于AMO ID。 在Adobe Advertising中优化促销活动需要添加的跟踪粒度，因此需要使用两个ID。

虽然EF ID维度未直接在[!DNL Analytics]报表中使用，但EF ID可用于创建营销渠道。 EF ID后缀指示渠道（显示或搜索）以及访问是由点进还是显示到位驱动。 EF ID中的分隔符是冒号，而不是AMO ID中的感叹号。

| ef ID后缀 | 渠道 |
|-------|---------|
| ：s | [!UICONTROL Paid Search] |
| ：d | [!UICONTROL Display Click-through] |
| ：i | [!UICONTROL Display View-through] |

### 使用EF ID的处理规则示例

#### 显示点进规则

通过仅捕获点进次数来创建显示点进营销渠道。 由于点进和显示到达的AMO ID相同，因此此规则使用EF ID变量和`ef_id`查询字符串参数。

有时，点进次数通过URL（默认）进行跟踪。 在其他情况下，点进次数通过服务器端的Last Event Service进行跟踪，因此URL不包含`ef_id`参数。 因此，该规则会检查EF ID变量或`ef_id`查询字符串参数以“：d”结尾的条件。 使用“`Any`”运算符，因为您希望为任一条件触发此规则。

![显示点进规则的示例](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### 显示浏览规则

要创建显示浏览渠道，请创建一个规则，在该规则中EF ID以“：i”结尾。 由于访客未单击广告，因此浏览跟踪在URL中不包含`ef_id`或`s_kwcid`，因此该规则只需要一个条件。

![显示浏览规则示例](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>*  [!DNL Analytics Marketing Channels]](mc-overview.md)的[基础知识
>* [为什么渠道数据在Adobe Advertising和 [!DNL Marketing Channels]](mc-data-variances.md)之间可能不同
>* [对Adobe Advertising数据使用 [!DNL Analytics Marketing Channels] ](mc-ac-data.md)
>* [视频：使用 [!DNL Marketing Channels] 进行Adobe Advertising报告](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>*  [!DNL Analytics]](/help/integrations/analytics/ids.md)使用的[Adobe AdvertisingID
