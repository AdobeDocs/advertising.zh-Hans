---
title: '[!UICONTROL Keyword Assist Report]'
description: 了解[!UICONTROL Keyword Assist Report]。
exl-id: 24e5854c-5696-43cd-ac21-64209f9f57d4
feature: Search Reports, Search Assist Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# [!UICONTROL Keyword Assist Report]

*广告商具有搜索、社交和Commerce点击跟踪以及Adobe Advertising、Adobe Analytics的转化跟踪（具有[!DNL Analytics]集成），或仅在信息源中使用令牌(`ef_id`)提供*

[!UICONTROL Keyword Assist Report]指示哪些关键字或版面可促进点击。 报表显示转化路径中收到点击的付费搜索关键词或投放位置的每个模式，并指示该模式对整体转化的贡献。 例如，您可以看到当用户首次单击因关键词搜索“皮鞋”而产生的广告，然后在关键词搜索“山羊皮鞋”后单击广告，然后下达订单时，发生的转化次数；或者，您可以看到在用户单击因超过10个关键词产生的广告后发生的转化次数。

报告结果包括转化路径中在广告商的搜索关键词或投放位置点击最多前N次的汇总数据
单击回顾和展示回顾窗口。 例如，如果选择路径大小为五(5)，则报表由转化路径组成，这些路径包括最多五个最早收到点击的关键字或投放位置，每个跟踪的点击模式对应一行。 每一行包括路径中的第一个关键字或放置以及导致转换的最后一个关键字或放置（即使最后一个关键字在指定的路径大小之外）。 默认情况下，这些行按路径中的事件数以升序排列。

>[!NOTE]
>
>如果报表包含来自启用了内容的搜索营销活动（不包括关键字）的版面，则[!UICONTROL Keyword]列会显示适用的广告组名称，例如“（广告组内容）您的广告组名称”。

您可以选择包含每行的聚合转化数据。 在报表中包括转化/收入列时，每种转化类型都以四列表示，分别显示a)转化总数、b)归因于该关键词模式的总体转化百分比、c)从第一个事件（第一个关键词）到转化的平均延迟（以天为单位）以及d)从最后一个事件（最后一个关键词）到转化的平均延迟（以天为单位）。 当转化路径包含的关键字数超过指定的路径大小时，报表将包含额外的行，这些行将聚合因较多的关键字而导致的转化数据（例如，包含六个关键字的点击的所有模式）。

您可以查看前18个月的数据。

## 可用列

以下是可用于每个报表的列。 默认自动包括默认列。 您可以从报表设置的列部分添加可用的自定义列。

| 列 | 默认？ | 描述 |
| ---- | ---- | ---- |
| [!UICONTROL 1st Keyword]至[!UICONTROL 5th Keyword] | 默认 | 在广告商的[点击回顾窗口](/help/search-social-commerce/glossary.md#c-d)和[展示回顾窗口](/help/search-social-commerce/glossary.md#i-j)内发生的转化路径中的五个最早的付费搜索关键词或投放位置点击。<br><br><b>注意：</b>如果报表包含来自支持内容的搜索营销活动（不包括关键字）的版面，则这些列显示适用的广告组名称，如“（广告组内容）您的广告组名称”。 |
| [!UICONTROL Path Size] | 默认 | 转化路径中在广告商的[点击回顾窗口](/help/search-social-commerce/glossary.md#c-d)和[展示回顾窗口](/help/search-social-commerce/glossary.md#i-j)内发生的关键字和/或版面数量。 |
| [!UICONTROL First Keyword] | 默认 | 转换路径中的第一个关键字或位置。 |
| [!UICONTROL Last Keyword] | 默认 | 导致转换的最后一个关键字或投放位置（即使最后关键字超出指定的路径大小也是如此）。 |
| \[特定于广告商的自定义（派生）量度\] | 自定义 | 您创建的自定义量度的值，它通过现有量度计算。 |
| \[特定于广告商的转化量度\] | 自定义 | 指定转化量度或网站参与量度的转化次数。 |
| [!UICONTROL % of Total] \[转化量度\] | 自动 | （在报表设置中不可用，但自动包含在每个包含的转化量度的报表输出中）归因于关键词和/或投放模式的项目组合中的整体转化百分比。 |
| [!UICONTROL 6th Keyword]至[!UICONTROL 10th Keyword] | 自定义 | 在广告商的[点击回顾窗口](/help/search-social-commerce/glossary.md#c-d)和[展示回顾窗口](/help/search-social-commerce/glossary.md#i-j)内发生的第六次到第十次付费搜索关键词或转化路径中的版面点击。<br><br><b>注意：</b>如果报表包含来自支持内容的搜索营销活动（不包括关键字）的版面，则这些列显示适用的广告组名称，如“（广告组内容）您的广告组名称”。 |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[转化量度\] | 自动 | （在报表设置中不可用，但自动包含在每个包含的转化量度的报表输出中）从第一个事件（在第一个关键词或投放位置）到转化的平均延迟（以天为单位）。 |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[转化量度\] | 自动 | （在报告设置中不可用，但自动包含在报告输出中）从上一个事件（在最后一个关键词或投放位置）到转换的平均延迟（以天为单位）。 |
| [!UICONTROL Path Frequency] | 自定义 | 此行的路径在转换前发生的次数。 |

>[!MORELIKETHIS]
>
>* [关于助理报告](assist-report-about.md)
>* [该[!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [该[!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [协助报告设置](assist-report-settings.md)
>* [生成协助报告](assist-report-generate.md)
