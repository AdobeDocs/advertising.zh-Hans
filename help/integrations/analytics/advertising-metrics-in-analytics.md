---
title: Analysis Workspace中的Adobe Advertising指标
description: Analysis Workspace中的Adobe Advertising指标和分类
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
TQID: https://experienceleague.adobe.com/CLPeE8g0Mix4Scq90qCd-s-tCUuBmkTBrkBWT1aPEhw
autotag-review: '2026-04-13T23:29:38.865Z'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: f2860a4b-f905-4545-bead-1bbc92564592
subfeature_v2:
  - id: cfd751d4-ee56-4323-8fd1-dc174b031709
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 05f5454a520027b33ebe4e2fe8583569cb19e5df
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# Analysis Workspace中的Adobe Advertising指标

*仅集成Adobe Advertising-Adobe Analytics的广告商*

>[!NOTE]
>
>* Adobe Advertising每天将流量指标和分类传递给[!DNL Analytics]。
>* [!DNL Analytics]实时捕获Adobe Advertising点进和显示点进。
>* 对于[!DNL Search, Social, & Commerce]，大多数广告网络和营销活动类型都支持此功能。 有关详细信息，请参阅[指南中的&quot;](/help/search-social-commerce/introduction/supported-inventory.md)支持的清单[!DNL Search, Social, & Commerce]&quot;。

## 来自Adobe Advertising的流量指标

除“[!DNL Analytics]”外，[!UICONTROL AMO ID Instances]中的Adobe Advertising流量量度通常以“Adobe Advertising”开头。 但是，对于最初使用自定义事件（而不是保留事件）创建点击次数、成本和展示次数的量度的长期客户，这些量度仍以“AMO”开头。

有关列表，请参阅&quot;[Adobe Advertising指标](https://experienceleague.adobe.com/zh-hans/docs/analytics/components/metrics/amo-metrics)&quot;。

<!--

| Traffic Metric | Description |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] or (some legacy customers) [!UICONTROL AMO Clicks] | The number of total Adobe Advertising clicks. |
| [!UICONTROL Adobe Advertising Cost] or (some legacy customers) [!UICONTROL AMO Cost] | The Adobe Advertising spend in the currency of the report suite. |
| [!UICONTROL Adobe Advertising Impressions] or (some legacy customers) [!UICONTROL AMO Impressions] | The number of Adobe Advertising impressions. |
| [!UICONTROL Adobe Advertising Measurable Impressions] | The number of impressions that were served for which viewability instrumentation successfully initialized. This value is calculated as (instrumented impressions - the number of unmeasurable impressions). |
| [!UICONTROL Adobe Advertising Minutes Viewed] | The number of minutes an Adobe Advertising video was viewed. |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | The number of impressions that were determined to be not viewable. This value is calculated as ([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable]). |
| [!UICONTROL Adobe Advertising Viewable Impressions] | The number of impressions that were measured to be viewable according to the placement configuration. |
| [!UICONTROL Adobe Advertising Views] | The number of views on an ad. A view is counted when the viewer initiates the Adobe Advertising video. |
| [!UICONTROL Adobe Advertising Views 25% Complete] | The number of views for which at least 25% of an Adobe Advertising video was watched. |
| [!UICONTROL Adobe Advertising Views 50% Complete] | The number of views for which at least 50% of an Adobe Advertising video was watched. |
| [!UICONTROL Adobe Advertising Views 75% Complete] | The number of views for which at least 75% of an Adobe Advertising video was watched. |
| [!UICONTROL Adobe Advertising Views 100% Complete] | The number of views for which 100% of an Adobe Advertising video was watched. |
| [!UICONTROL AMO ID Instances] | The number of times the [!UICONTROL AMO ID] is set. |

-->

## Adobe Advertising分类

查看AMO ID维度[的](https://experienceleague.adobe.com/zh-hans/docs/analytics/components/dimensions/amo-id#classifications)分类。
<!--

>[!NOTE]
>
>All Adobe Advertising dimensions in [!DNL Analytics] are followed by "[!DNL (AMO ID)]."

| Dimension | Applicable Adobe Advertising Data  | Description |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | Advertising DSP or the search engine name |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The account name. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | RTB ([!DNL DSP]) or the ad network name ([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The campaign name. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The package ([!DNL DSP]) or portfolio ([!DNL Search, Social, & Commerce]) name. |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | The placement name. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] data | The ad group name. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] data | The keyword. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | The search match type. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | The keyword and match type. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The ad type, such as `text`, `video`, `display`, or `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data |The ad type ([!DNL DSP]) or ad title ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The ad description ([!DNL DSP]) or ad body ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | The URL displayed in the ad. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | The destination URL for the ad. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | Whether the landing page entry was a view-through or a click-through. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] data | The product target for a product listing ad. |

-->

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
>* Adobe Advertising中的[[!DNL Analytics] 数据](/help/integrations/analytics/analytics-data-in-advertising.md)
