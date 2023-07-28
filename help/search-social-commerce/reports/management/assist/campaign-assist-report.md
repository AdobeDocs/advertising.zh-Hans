---
title: '[!UICONTROL Campaign Assist Report]'
description: 了解 [!UICONTROL Campaign Assist Report].
exl-id: 7fbc9c17-c77d-485b-8d51-5e5a153d7a2b
feature: Search Reports, Search Assist Reports
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# 此 [!UICONTROL Campaign Assist Report]

*具有搜索、社交和商务点击跟踪以及来自Adobe Advertising的转化跟踪的广告商，Adobe Analytics(具有 [!DNL Analytics] 集成)，或使用令牌在馈送中提供(`ef_id`)仅限*

此 [!UICONTROL Campaign Assist Report] 指示哪些营销活动协助了转换过程。 报告其广告导致一次或多次转化的每种营销活动模式对您的整体转化率的贡献情况。 例如，您可以查看当用户首先看到来自促销活动A的广告，然后单击来自促销活动B的广告，然后下达订单时发生的转化次数。 同样，您可以查看用户与10个以上营销活动的广告交互后发生的转化次数。

报表结果包括转化路径中每种营销活动模式的汇总数据（最早N个营销活动），适用于广告商的转化路径中发生的事件 [单击回顾窗口](/help/search-social-commerce/glossary.md#c-d) 和 [展示回顾窗口](/help/search-social-commerce/glossary.md#i-j). 例如，如果选择路径大小为五(5)，则报表将包括转化路径，其中最多包含五个最早的促销活动，每个模式一行用于跟踪其事件的促销活动。 每一行会显示一个营销活动模式，包括路径中的第一个营销活动以及导致转化的最后一个营销活动（即使最后一个营销活动超出指定的路径大小也是如此）。 默认情况下，这些行按路径中的促销活动数量以升序排列。

您可以选择为每行包含聚合转化数据，包括自定义量度。 在报表中包含转化/收入列时，每种转化类型都会用四列表示，分别显示a)转化总数、b)归因于该营销活动模式的整体转化百分比、c)从第一个事件（在第一个营销活动中）到转化的平均延迟（以天为单位）以及d)从最后一个事件（在最后一个营销活动中）到转化的平均延迟（以天为单位）。 当转化路径包含的促销活动多于指定的路径大小时，报表将包含额外的行，这些行将汇总因较高的促销活动数（例如，包含六个促销活动的所有模式）而导致的转化数据。

您也可以选择在促销活动名称之后包含广告网络和/或事件类型，例如 `<campaign name> (Google) click`.

您可以查看前18个月的数据。

>[!TIP]
>
>如果您的品牌关键字与通用关键字位于不同的营销活动中，则报表会指示您的品牌关键字是否对转化有贡献。

## 可用列

以下是可用于每个报表的列。 默认自动包括默认列。 您可以从报表设置的列部分添加可用的自定义列。

| 列 | 默认？ | 描述 |
| ---- | ---- | ---- |
| [!UICONTROL 1st Campaign] 到 [!UICONTROL 5th Campaign] | 默认 | 转化路径中发生在广告商网站中的最早五个营销活动 [单击回顾窗口](/help/search-social-commerce/glossary.md#c-d) 和 [展示回顾窗口](/help/search-social-commerce/glossary.md#i-j).<br><br>如果您在实体名称后包含任何报告选项来指示广告网络、帐户名称或事件类型，则该信息将包含在促销活动名称后(例如 `"<"campaign name> [Google] [Account1] [impression]`“)。 |
| [!UICONTROL Path Size] | 默认 | 转化路径中在广告商发生的促销活动数 [单击回顾窗口](/help/search-social-commerce/glossary.md#c-d) 和 [展示回顾窗口](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Campaign] | 默认 | 转化路径中的第一个营销活动。 |
| [!UICONTROL Last Campaign] | 默认 | 导致转化的最后一个营销活动（即使最后一个关键词在指定的路径大小之外也是如此）。<br><br>如果您在实体名称后包含任何报告选项来指示广告网络、帐户名称或事件类型，则该信息将包含在促销活动名称后(例如 `"<"campaign name> [Google] [Account1] [impression]`“)。 |
| \[特定于广告商的自定义（派生）量度\] | 自定义 | 您创建的自定义量度的值，它通过现有量度计算。 |
| \[广告商特定的事务属性\] | 自定义 | 指定事务属性或网站参与度量的转化次数。 |
| [!UICONTROL % of Total] \[事务属性\] | 自动 | （在报表设置中不可用，但自动包含在所包含每个交易属性的报表输出中）因营销活动模式导致的指定交易属性的转化次数。 |
| [!UICONTROL 6th Campaign] 到 [!UICONTROL 20th Campaign] | 自定义 | 转化路径中在广告商中发生的第六到第二十个营销活动 [单击回顾窗口](/help/search-social-commerce/glossary.md#c-d) 和 [展示回顾窗口](/help/search-social-commerce/glossary.md#i-j).<br><br>如果您在实体名称后包含任何报告选项来指示广告网络、帐户名称或事件类型，则该信息将包含在促销活动名称后(例如 `"<"campaign name> [Baidu] [Account1] [click]`“)。 |
| [!UICONTROL Avg. Conv. Latency (First Campaign To Conversion)] \[事务属性\] | 自动 | （在报表设置中不可用，但自动包含在每个交易属性的报表输出中）从第一个事件（在第一个营销活动中）到转化的平均延迟（以天为单位）。 |
| [!UICONTROL Avg. Conv. Latency (Last Campaign To Conversion)] \[事务属性\] | 自动 | （在报表设置中不可用，但自动包含在报表输出中）从上一个事件（在最后一个营销活动中）到转化的平均延迟（以天为单位）。 |
| [!UICONTROL EF Campaign ID] | 自定义 | Search、Social和Commerce分配给营销活动的数值ID。 |
| [!UICONTROL EF Portfolio Group ID] | 自定义 | 项目组合所属的项目组合组的数值ID。 |
| [!UICONTROL EF Search Engine ID] | 自定义 | 搜索、社交和商务分配给广告网络的数值ID： <i>[!UICONTROL 3]</i> 对象 [!DNL Google Ads]， <i>[!UICONTROL 10]</i> 对象 [!DNL Microsoft® Advertising]， <i>[!UICONTROL 45]</i> 对象 [!DNL Meta]， <i>[!UICONTROL 86]</i> 对象 [!DNL Yahoo! Display Network]， <i>[!UICONTROL 87]</i> 对象 [!DNL Naver]， <i>[!UICONTROL 88]</i> 对象 [!DNL Baidu]， <i>[!UICONTROL 90]</i> 对象 [!DNL Yandex]， <i>[!UICONTROL 94]</i> 对象 [!DNL Yahoo! Japan Ads]， <i>[!UICONTROL 105]</i> 对象 [!DNL Yahoo Native] （已弃用），或 <i>[!UICONTROL 106]</i> 对象 [!DNL Pinterest] （已弃用）。 |
| [!UICONTROL Portfolio ID] | 数值项目组合ID。 |
| [!UICONTROL User SE Account ID] | 搜索、社交和商务分配给广告网络的数值ID。 |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [关于协助报告](assist-report-about.md)
>* [此 [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [此 [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [协助报表设置](assist-report-settings.md)
>* [生成协助报告](assist-report-generate.md)
