---
title: '[!UICONTROL Channel Assist Report]'
description: 了解 [!UICONTROL Channel Assist Report].
exl-id: 49616327-72e9-49c6-90b9-91c7486e8417
feature: Search Reports, Search Assist Reports
source-git-commit: 97111c6cd38098cac72b8773390afd254a017d1d
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# 此 [!UICONTROL Channel Assist Report]

*具有搜索、社交和商务点击跟踪以及来自Adobe Advertising的转化跟踪的广告商，Adobe Analytics(具有 [!DNL Analytics] 集成)，或使用令牌在馈送中提供(`ef_id`)仅限*

此 [!UICONTROL Channel Assist Report] 指示各种营销渠道(搜索、Social和Commerce中的搜索或社交；或Advertising DSP中的显示或视频)如何辅助转化过程。 报表会显示导致一个或多个转化的每种事件类型模式对您的整体转化率的贡献情况。 例如，您可以看到当用户首先看到展示广告展示，然后单击搜索广告，然后下达订单时发生的转化次数；或者，您可以看到在用户与10个以上的广告进行交互后发生的转化次数。 事件类型包括搜索点击次数、显示展示次数和点击次数、视频展示次数和点击次数，以及其他展示次数和其他点击次数。 <!-- [DSP metrics may show up as "Other Path Length (<length>)" or empty; we're supposed to fill in more values for DSP at some point.] -->

报告结果包括转化路径中发生的每种事件类型模式的汇总数据（最多N个最早的事件类型） [单击回顾窗口](/help/search-social-commerce/glossary.md#c-d) 和 [展示回顾窗口](/help/search-social-commerce/glossary.md#i-j). 例如，如果选择路径大小为五(5)，则报表将包括最多包含五个最早事件的转化路径，其中每个跟踪的事件类型模式占一行（例如“搜索点击”，然后“显示展示”）。 每一行显示一个事件模式，包括路径中的第一个事件和导致转换的最后一个事件（即使最后一个事件在指定的路径大小之外也是如此）。 默认情况下，这些行按路径中的事件数以升序排列。

您可以选择包含每行的聚合转化数据。 在报表中包含转化/收入列时，每种转化类型都以四列表示，分别显示a)转化总数、b)归因于该事件模式的总体转化百分比、c)从第一个事件到转化的平均延迟（以天为单位）以及d)从最后一个事件到转化的平均延迟（以天为单位）。 当转化路径包含的事件数超过指定的路径大小时，报表会包含额外的行，这些行会聚合因事件数较多导致的转化数据（例如，包含六个事件类型的所有模式）。

您可以查看前18个月的数据。

## 可用列

以下是可用于每个报表的列。 默认自动包括默认列。 您可以从报表设置的列部分添加可用的自定义列。

| 列 | 默认？ | 描述 |
| ---- | ---- | ---- |
| [!UICONTROL 1st Event] 到 [!UICONTROL 5th Event] | 默认 | 转化路径中在广告商发生的五个最早的事件类型 [单击回顾窗口](/help/search-social-commerce/glossary.md#c-d) 和 [展示回顾窗口](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Path Size] | 默认 | 转化路径中在广告商发生的事件类型数 [单击回顾窗口](/help/search-social-commerce/glossary.md#c-d) 和 [展示回顾窗口](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Event Type] | 默认 | 转化路径中第一个（最早）事件的事件类型。 |
| [!UICONTROL Last Event Type] | 默认 | 导致转换的最后一个事件的事件类型（即使最后一个事件在指定的路径大小之外也是如此）。 |
| \[特定于广告商的自定义（派生）量度\] | 自定义 | 您创建的自定义量度的值，它通过现有量度计算。 |
| \[广告商特定的事务属性\] | 自定义 | 指定事务属性或网站参与度量的转化次数。 |
| [!UICONTROL % of Total] \[事务属性\] | 自动 | （在报表设置中不可用，但自动包含在所包含每个交易属性的报表输出中）归因于事件模式的项目组合中的总转化百分比。 |
| [!UICONTROL 6th Event] 到 [!UICONTROL 30th Event] | 自定义 | 转化路径中在广告商发生的第六到第三十个事件类型 [单击回顾窗口](/help/search-social-commerce/glossary.md#c-d) 和 [展示回顾窗口](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[事务属性\] | 自动 | （在报表设置中不可用，但自动包含在每个包含的事务属性的报表输出中）从第一个事件到转换的平均延迟（以天为单位）。 |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[事务属性\] | 自动 | （在报表设置中不可用，但自动包含在报表输出中）从上次事件到转换的平均延迟（以天为单位）。 |
| [!UICONTROL Path Frequency] | 自定义 | 此行的路径在转换前发生的次数。 |

>[!MORELIKETHIS]
>
>* [关于协助报告](assist-report-about.md)
>* [此 [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [此 [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [协助报表设置](assist-report-settings.md)
>* [生成协助报告](assist-report-generate.md)
