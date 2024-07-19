---
title: Analysis Workspace中的Adobe Advertising指标
description: Analysis Workspace中的Adobe Advertising指标
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: da69280679a4e0c5ce04f55ee94ce984745395ff
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---

# Analysis Workspace中的Adobe Advertising指标

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

>[!NOTE]
>
>* Adobe Advertising每天将流量指标和维度传递给[!DNL Analytics]。
>* [!DNL Analytics]实时捕获Adobe Advertising点进和显示点进。
>* 对于[!DNL Search, Social, & Commerce]，大多数广告网络和营销活动类型都支持此功能。 有关详细信息，请参阅[!DNL Search, Social, & Commerce]指南中的&quot;[支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)&quot;。

## 来自Adobe Advertising的流量量度

除“[!UICONTROL AMO ID Instances]”外，[!DNL Analytics]中的Adobe Advertising流量量度通常以“Adobe Advertising”开头。 但是，对于最初使用自定义事件（而不是保留事件）创建点击次数、成本和展示次数的量度的长期客户，这些量度仍以“AMO”开头。

| 流量量度 | 描述 |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks]或（一些旧客户）[!UICONTROL AMO Clicks] | Adobe Advertising总点击次数。 |
| [!UICONTROL Adobe Advertising Cost]或（一些旧客户）[!UICONTROL AMO Cost] | Adobe Advertising支出（以报表包的货币表示）。 |
| [!UICONTROL Adobe Advertising Impressions]或（一些旧客户）[!UICONTROL AMO Impressions] | Adobe Advertising展示次数。 |
| [!UICONTROL Adobe Advertising Measurable Impressions] | 提供的可见性检测已成功初始化的展示次数。 此值的计算方式为（仪器展示次数 — 无法测量的展示次数）。 |
| [!UICONTROL Adobe Advertising Minutes Viewed] | Adobe Advertising视频被查看的分钟数。 |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | 被确定为不可查看的展示次数。 此值计算为([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable])。 |
| [!UICONTROL Adobe Advertising Viewable Impressions] | 根据版面配置测量为可查看的展示次数。 |
| [!UICONTROL Adobe Advertising Views] | 广告的查看次数。 当查看器启动Adobe Advertising视频时，将计为一个视图。 |
| [!UICONTROL Adobe Advertising Views 25% Complete] | 观看了至少25%的Adobe Advertising视频的次数。 |
| [!UICONTROL Adobe Advertising Views 50% Complete] | 观看了至少50%的Adobe Advertising视频的次数。 |
| [!UICONTROL Adobe Advertising Views 75% Complete] | 观看了至少75%的Adobe Advertising视频的次数。 |
| [!UICONTROL Adobe Advertising Views 100% Complete] | 100%观看了Adobe Advertising视频的观看次数。 |
| [!UICONTROL AMO ID Instances] | 设置[!UICONTROL AMO ID]的次数。 |

## Adobe AdvertisingDimension

>[!NOTE]
>
>[!DNL Analytics]中的所有Adobe Advertising维度都后跟“[!DNL (AMO ID)]”。

| 维度 | 适用的Adobe Advertising数据 | 描述 |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP]和[!DNL Search, Social, & Commerce]数据 | Advertising DSP或搜索引擎名称 |
| [!UICONTROL Account (AMO ID] | [!DNL DSP]和[!DNL Search, Social, & Commerce]数据 | 帐户名称。 |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP]和[!DNL Search, Social, & Commerce]数据 | RTB ([!DNL DSP])或广告网络名称([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP]和[!DNL Search, Social, & Commerce]数据 | 营销活动名称。 |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP]和[!DNL Search, Social, & Commerce]数据 | 包([!DNL DSP])或项目组合([!DNL Search, Social, & Commerce])名称。 |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP]数据 | 投放位置名称。 |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce]数据 | 广告组名称。 |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce]数据 | 关键字。 |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce]数据 | 搜索匹配类型。 |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce]数据 | 关键字和匹配类型。 |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP]和[!DNL Search, Social, & Commerce]数据 | 广告类型，如`text`、`video`、`display`或`native`。 |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP]和[!DNL Search, Social, & Commerce]数据 | 广告类型([!DNL DSP])或广告标题([!DNL Search, Social, & Commerce])。 |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP]和[!DNL Search, Social, & Commerce]数据 | 广告说明([!DNL DSP])或广告正文([!DNL Search, Social, & Commerce])。 |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce]数据 | 广告中显示的URL。 |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce]数据 | 广告的目标URL。 |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP]和[!DNL Search, Social, & Commerce]数据 | 登陆页面条目是浏览还是点进。 |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce]数据 | 产品列表广告的产品目标。 |

## 适用于Adobe Advertising的有用自定义计算指标

考虑为您的Adobe Advertising数据创建以下量度。

* 登陆页面实例的点击量([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks])：这是点击了广告并进入登陆页面的用户百分比。
* 可衡量的比率([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100)
* 可见展示速率([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100)
* 每次查看成本([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Views])
* 每次点击成本([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks])

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Adobe Advertising中的数据](/help/integrations/analytics/analytics-data-in-advertising.md)
