---
title: 使用Adobe AdvertisingID创建 [!DNL Marketing Channels] 规则
description: 了解如何使用Adobe AdvertisingID创建处理规则 [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# 使用Adobe AdvertisingID创建 [!DNL Marketing Channels] 处理规则

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

您可以使用Adobe AdvertisingID ([AMO ID和EF ID](../ids.md))以配置 [!DNL Marketing Channels] Adobe Analytics中的处理规则。 将Adobe AdvertisingID用于特定于您的Adobe Advertising促销活动的规则。

## 处理规则中的AMO ID

AMO ID是用于报告Adobe Advertising数据的主要跟踪代码 [!DNL Analytics]. AMO ID是由Adobe管理的动态值的连接，用于在 [!DNL Analytics]. 储存在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar维度(AMO ID)。 AMO ID可以设置 [!DNL Analytics] 有两种方式：

* 点进跟踪：Adobe Advertising设置 `s_kwcid` 链接中的查询字符串参数，以及 [!DNL Analytics] 发生点进时从登陆页面URL中选取参数。
* 显示到达跟踪([!DNL DSP] 仅限)：Last Event Service在服务器端检测浏览并将AMO ID发送到 [!DNL Analytics]. 在这种情况下，URL不包含 `s_kwcid` 参数。

AMO ID中的动态值表示跟踪的营销渠道：

* AMO ID中的前缀可用于标识中的顶级渠道 [!DNL Marketing Channels].

* AMO ID正文中的字符短语表示更具体的促销活动类型。

* 后缀“vt”存在于 [!DNL DSP] 显示到达流量，并可用于创建单独的点进和显示到达 [!DNL DSP] 渠道。

可以忽略其余的AMO ID。

| [!UICONTROL AMO ID] | 渠道 | 规则逻辑 |
|--------|---------|--------------------|
| 艾尔！ （前缀） | [!UICONTROL Paid Search] | 开头为 |
| AC！ （前缀） | [!UICONTROL DSP] | 开头为 |
| ！g！ （正文） | [!UICONTROL Google Search] | 包含 |
| ！s！ （正文） | [!UICONTROL Search Partner] | 包含 |
| ！d！ （正文） | [!UICONTROL Display Network] | 包含 |
| ！u！ （正文） | [!UICONTROL Smart Shopping Campaign] | 包含 |
| ！ytv！ （正文） | [!UICONTROL YouTube Video Ad] | 包含 |
| ！yts！ （正文） | [!UICONTROL YouTube Search Ad] | 包含 |
| ！vp！ （正文） | [!UICONTROL Google Video Partners] | 包含 |
| ！vt（后缀） | [!UICONTROL DSP View-through] | 结束于 |

### 使用AMO ID的处理规则示例

此 [!DNL Marketing Channels] 的处理规则 [!UICONTROL Paid Search] 渠道可能如下所示：

![示例 [!UICONTROL Paid Search] 规则](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

此 [!DNL Marketing Channels] 的处理规则 [!UICONTROL YouTube Video Ads] 渠道可能如下所示：

![示例 [!UICONTROL YouTube Video Ads] 规则](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> 请确保按特定顺序运行规则。 如果以上两个规则按顺序运行， [!DNL YouTube] 视频广告流量属于 [!UICONTROL Paid Search] 渠道，因为AMO ID都会以“AL！”开头。 并包含“！ytv！”。

## 处理规则中的EF ID

AMO EF ID (EF ID)是 [!DNL Analytics for Advertising] 集成。 其主要目的是跟踪和通过 [!DNL Analytics] 将事件数据导入Adobe Advertising。 每次发生点进或浏览时，都会生成一个唯一的EF ID，即使该ID与同一访客的广告完全相同。 EF ID未用于 [!DNL Analytics] 报表用户界面，因为它通常超过 [!DNL Analytics]，使其不可用于报表。 Adobe Advertising量度和元数据不应用于EF ID；而是仅应用于AMO ID。 在Adobe Advertising中优化促销活动需要添加的跟踪粒度，因此需要两个ID。

尽管EF ID维度并非直接用于 [!DNL Analytics] 在报表中，EF ID可用于创建营销渠道。 EF ID后缀指示渠道（显示或搜索）以及访问是由点进还是浏览驱动。 EF ID中的分隔符是冒号，而不是AMO ID中的感叹号。

| EF ID后缀 | 渠道 |
|-------|---------|
| ：s | [!UICONTROL Paid Search] |
| ：d | [!UICONTROL Display Click-through] |
| ：i | [!UICONTROL Display View-through] |

### 使用EF ID的处理规则示例

#### 显示点进规则

通过仅捕获点进次数来创建显示点进营销渠道。 由于点进和显示到达的AMO ID相同，因此此规则使用EF ID变量和 `ef_id` 查询字符串参数。

有时，点进次数通过URL（默认）进行跟踪。 在其他情况下，点进次数通过服务器端的Last Event Service进行跟踪，因此URL不包含 `ef_id` 参数。 因此，规则会检查EF ID变量或 `ef_id` 查询字符串参数以“：d”结尾。 使用&quot;`Any`”运算符，因为您希望为任一条件触发此规则。

![显示点进规则的示例](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### 显示浏览规则

要创建显示浏览渠道，请创建一个规则，其中EF ID以“：i”结尾。 由于访客未单击广告，因此浏览跟踪不包含 `ef_id` 或 `s_kwcid` 因此，该规则只需要一个条件。

![显示浏览规则示例](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [的基础知识 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [为什么渠道数据可能因Adobe Advertising和原因而异 [!DNL Marketing Channels]](mc-data-variances.md)
>* [使用 [!DNL Analytics Marketing Channels] 包含Adobe Advertising数据](mc-ac-data.md)
>* [视频：使用 [!DNL Marketing Channels] 用于Adobe Advertising报表](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [使用的Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md)
