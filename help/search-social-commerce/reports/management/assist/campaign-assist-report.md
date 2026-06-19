---
title: '[!UICONTROL Campaign Assist Report]'
description: 了解[!UICONTROL Campaign Assist Report]。
exl-id: c89b4c9f-16d5-4e1a-a73f-6cc99dd3f526
feature: Search Reports, Search Assist Reports
TQID: https://experienceleague.adobe.com/9CQ9aS6g0C1lCEYQbGEjctsZXEtIqjLOl5ohP45YFSU
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 857
ht-degree: 1%

---

# [!UICONTROL Campaign Assist Report]

*广告商具有搜索、社交和Commerce点击跟踪以及来自Adobe Advertising、Adobe Analytics（具有[!DNL Analytics]集成）的转化跟踪，或仅在信息源中使用令牌(`ef_id`)提供*

[!UICONTROL Campaign Assist Report]指示哪些营销活动协助了转换过程。 报告其广告导致一次或多次转化的每种营销活动模式对您的整体转化率的贡献情况。 例如，您可以查看当用户首先看到来自促销活动A的广告，然后单击来自促销活动B的广告，然后下达订单时发生的转化次数。 同样，您可以查看用户与10个以上营销活动的广告交互后发生的转化次数。

报表结果包括转化路径中每种营销活动模式的汇总数据（最早N个营销活动），这些汇总数据用于广告商的[点击回顾窗口](/help/search-social-commerce/glossary.md#c-d)和[展示回顾窗口](/help/search-social-commerce/glossary.md#i-j)内发生的事件。 例如，如果选择路径大小为五(5)，则报表将包括转化路径，其中最多包含五个最早的促销活动，每个模式一行用于跟踪其事件的促销活动。 每一行会显示一个营销活动模式，包括路径中的第一个营销活动以及导致转化的最后一个营销活动（即使最后一个营销活动超出指定的路径大小也是如此）。 默认情况下，这些行按路径中的促销活动数量以升序排列。

您可以选择为每行包含聚合转化数据，包括自定义量度。 在报表中包含转化/收入列时，每种转化类型都会用四列表示，分别显示a)转化总数、b)归因于该营销活动模式的整体转化百分比、c)从第一个事件（在第一个营销活动中）到转化的平均延迟（以天为单位）以及d)从最后一个事件（在最后一个营销活动中）到转化的平均延迟（以天为单位）。 当转化路径包含的促销活动多于指定的路径大小时，报表将包含额外的行，这些行将汇总因较高的促销活动数（例如，包含六个促销活动的所有模式）而导致的转化数据。

您还可以选择在促销活动名称（如`<campaign name> (Google) click`）之后包含广告网络和/或事件类型。

您可以查看前18个月的数据。

>[!TIP]
>
>如果您的品牌关键字与通用关键字位于不同的营销活动中，则报表会指示您的品牌关键字是否对转化有贡献。

## 可用列

以下是可用于每个报表的列。 默认自动包括默认列。 您可以从报表设置的列部分添加可用的自定义列。

| 列 | 默认？ | 描述 |
| ---- | ---- | ---- |
| [!UICONTROL 1st Campaign]至[!UICONTROL 5th Campaign] | 默认 | 转化路径中在广告商的[点击回顾窗口](/help/search-social-commerce/glossary.md#c-d)和[展示回顾窗口](/help/search-social-commerce/glossary.md#i-j)内出现的最早五个营销活动。<br><br>如果您在实体名称后包含任何报告选项以指示广告网络、帐户名称或事件类型，则该信息将包含在营销活动名称（如“`"<"campaign name> [Google] [Account1] [impression]`”）之后。 |
| [!UICONTROL Path Size] | 默认 | 转化路径中在广告商的[点击回顾窗口](/help/search-social-commerce/glossary.md#c-d)和[展示回顾窗口](/help/search-social-commerce/glossary.md#i-j)内发生的营销活动数。 |
| [!UICONTROL First Campaign] | 默认 | 转化路径中的第一个营销活动。 |
| [!UICONTROL Last Campaign] | 默认 | 导致转换的上一个营销活动（即使最后一个关键字在指定的路径大小之外也是如此。）<br><br>如果您在实体名称后包括任何报告选项以指示广告网络、帐户名称或事件类型，则该信息将包括在营销活动名称（如`"<"campaign name> [Google] [Account1] [impression]`&quot;）之后。 |
| \[特定于广告商的自定义（派生）量度\] | 自定义 | 您创建的自定义量度的值，它通过现有量度计算。 |
| \[特定于广告商的转化量度\] | 自定义 | 指定转化量度或网站参与量度的转化次数。 |
| [!UICONTROL % of Total] \[转化量度\] | 自动 | （在报表设置中不可用，但自动包含在每个包含的转化量度的报表输出中）因营销活动模式导致的指定转化量度的转化次数。 |
| [!UICONTROL 6th Campaign]至[!UICONTROL 20th Campaign] | 自定义 | 转化路径中在广告商的[点击回顾窗口](/help/search-social-commerce/glossary.md#c-d)和[展示回顾窗口](/help/search-social-commerce/glossary.md#i-j)内发生的第六到第二十个营销活动。<br><br>如果您在实体名称后包含任何报告选项以指示广告网络、帐户名称或事件类型，则该信息将包含在营销活动名称（如“`"<"campaign name> [Baidu] [Account1] [click]`”）之后。 |
| [!UICONTROL Avg. Conv. Latency (First Campaign To Conversion)] \[转化量度\] | 自动 | （在报表设置中不可用，但自动包含在每个包含的转化量度的报表输出中）从第一个事件（在第一个营销活动中）到转化的平均延迟（以天为单位）。 |
| [!UICONTROL Avg. Conv. Latency (Last Campaign To Conversion)] \[转化量度\] | 自动 | （在报表设置中不可用，但自动包含在报表输出中）从上一个事件（在最后一个营销活动中）到转化的平均延迟（以天为单位）。 |
| [!UICONTROL EF Campaign ID] | 自定义 | Search、Social和Commerce分配给营销活动的数值ID。 |
| [!UICONTROL EF Portfolio Group ID] | 自定义 | 项目组合所属的项目组合组的数值ID。 |
| [!UICONTROL EF Search Engine ID] | 自定义 | Search、Social和Commerce分配给广告网络的数值ID：[!DNL Google Ads]的<i>[!UICONTROL 3]</i>、[!DNL Microsoft Advertising]的<i>[!UICONTROL 10]</i>、[!DNL Meta]的<i>[!UICONTROL 45]</i>、[!DNL Yahoo! Display Network]的<i>[!UICONTROL 86]</i>、[!DNL Naver]的<i>[!UICONTROL 87]</i>、[!DNL Baidu]的<i>[!UICONTROL 88]</i>、[!DNL Yandex]的<i>[!UICONTROL 90]</i>、[!DNL LY Ads]的<i>[!UICONTROL 94]</i>（以前的[!DNL Yahoo! Japan Ads]）、[!DNL Yahoo Native]的<i>[!UICONTROL 105]</i>（已弃用）或[!DNL Pinterest]的<i>[!UICONTROL 106]</i>（已弃用）。 |
| [!UICONTROL Portfolio ID] | 自定义 | 数值项目组合ID。 |
| [!UICONTROL User SE Account ID] | 自定义 | Search、Social和Commerce分配给广告网络的数值ID。 |

>[!MORELIKETHIS]
>
>* [关于助理报告](assist-report-about.md)
>* [该[!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [该[!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [协助报告设置](assist-report-settings.md)
>* [生成协助报告](assist-report-generate.md)
