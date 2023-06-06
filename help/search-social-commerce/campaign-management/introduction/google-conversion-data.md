---
title: ”[!DNL Google Ads] 转化数据”
description: 了解以下类型的信息 [!DNL Google Ads] — 跟踪的转化数据可在Search、Social和Commerce中使用。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# [!DNL Google Ads] 搜索、社交和商务中的转化数据

搜索、社交和商务自动同步 [!DNL Google Ads] — 跟踪了 [!DNL Google Ads] 将搜索和购物网络移入搜索、社交和商务，以便报告和优化。 搜索、社交和商务会同步“”的转化数据[!DNL Include in 'Conversions']”选项已启用，提取过去30天的数据，然后每天提取对数据所做的更改。

## 可用的转化数据

每项最多有三个交易属性 [[!DNL Google Ads] — 跟踪的转化](https://support.google.com/google-ads/answer/4677036) （您在中设置的） [!DNL Google Ads])，使用中配置的转化名称，自动在Search、Social和Commerce中可用 [!DNL Google Ads]. 每次转换的交易属性包括：

* `GGL*`  — （跟踪时）关键字的转化值总和，以“GGL”前缀开头（例如GGL Purchase）。

* `GGL_CT*`  — 转换次数（计数），以“GGL_CT”前缀（例如GGL_CT_Purchase）开头。

* `GGL_XD_CT*`  — （当可用于转化类型时，当您跟踪这些类型时）由Google测量的以“GGL_XD_CT_”前缀(例如GGL_XD_CT_Purchase)开头的跨设备转化次数（计数）。

从为帐户启用该功能之日起有数据可用，并且在09之前每天更新:00-10:00（广告商所在时区）。

[!DNL Google Ads] 记录每次转换的方式 [竞价单位](/help/search-social-commerce/glossary.md#a-b)，设备，然后单击日期（不是转换日期）。 归因基于中每个量度的默认归因设置 [!DNL Google Ads]；Adobe广告归因未计入中，因为单击事件级别数据不可用。 每天，Search、Social和Commerce提取前30天的转化数据，然后使用中的单击日期计算自前一天以来的任何增量转化 [!DNL Google Ads] 并将前一天指定为事务处理日期。 因此，随着每次点击跟踪新转化，历史数据可能会每天发生更改。 如果您将“搜索”、“社交”和“商务”中的数据与中的数据进行比较 [!DNL Google Ads]，使用查看或报告选项查看&quot;[!UICONTROL Conversions by: Click date]“”（不是按交易日期）。

所有量度都会自动显示在营销活动管理视图和基本报表中，并可用于组合目标以进行优化。

>[!NOTE]
>
>* 如果您有多个帐户具有相同的转化名称，则在Adobe广告中可能会看到重复的转化名称。 如果发生这种情况， [更改显示名称](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) 中的某个重复量度 [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. 当两个不同的量度具有相同的名称时，报表不准确。
>* 竞价单位级别的数据与中的数据匹配 [!DNL Google Ads] 在同一级别。 但是， [!DNL Google Ads]&#39;自己的更高级别的转化数据可能包含未归因到子竞价单位的更多转化。 搜索、Social和Commerce中的数据始终从竞价单位级别累计，因此，例如，促销活动级别报表的总数可能与Google Ads中的促销活动级别报表的总数不同。
>* 数据差异通常在晨同步后小于当天晚些时候（此时尚未同步其他转化）。 我们建议在早上验证数据。
>* 转化数据不可用于 [!DNL Google Display Network]， [!DNL Gmail]， [!DNL Mobile App]、和 [!DNL YouTube] 广告。 在比较以下位置的数据时，过滤掉这些类型的广告： [!DNL Google Ads] 包含搜索、社交和商务中的数据。
>* 数据 [!DNL Google Ads] 转化在受众或地理位置级别不可用，因此不用于自动优化RLSA和位置竞价调整。


## 如何比较中的转化数据 [!DNL Google Ads] 包含搜索、社交和商务中的数据

使用以下报表设置验证可比数据。

### 在中使用的报表设置 [!DNL Google Ads]

1. 在主工具栏中，选择 **[!DNL Reports]>[!DNL Report]**.

1. 选择 **[!DNL + Custom]>[!DNL Table]**.

1. 从左窗格中，指定报表中的行和列：

   1. 搜索 **[!DNL Day]** 字段并将其拖动到 [!DNL Row] 部分。

   1. 搜索 **[!DNL All conv].** 字段并将其拖动到 [!DNL Column] 部分。

   1. 搜索 **[!DNL Conversion action]** 字段并将其拖动到 [!DNL Column] 部分。

1. 在报表设置工具栏中，选择 **[!DNL Filter]>[!DNL Ad status]**，然后选择所有框。

1. 在报表设置工具栏中，选择 **[!DNL Download]>[!DNL Excel .csv]**.

### 要在Search、Social和Commerce中使用的报表设置

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. 在数据表上方的工具栏中，单击 **[!UICONTROL Create Report]**，将光标悬停在上方 **[!UICONTROL Basic Reports]**，然后单击 **[!UICONTROL Search Engine Account Report]**.

1. 在 [!UICONTROL Report Settings] 窗口中，指定以下报表设置：

   1. 在 **[!UICONTROL Conversions Based]** 在部分中，选择 **[!UICONTROL Click date]**.

   1. 指定用于 [!DNL Google Ads] 报告。

   1. 在 **[!UICONTROL Search/Content]** 部分，选择 **[!UICONTROL Search Only]**.

   1. 在 **[!UICONTROL Search Engine Hierarchy]** 部分，展开 [!UICONTROL Google Adwords] 部分并选择帐户。

   1. 打开 [!UICONTROL Columns] 选项卡，然后添加 [!DNL Google Ads] 要比较的指标（从“GGL”开始）。

1. 单击 **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [关于Search、Social和Commerce中的营销活动管理](campaign-management-about.md)
>* [实施广告网络帐户和营销活动概述](campaign-implemention-overview.md)
>* [监控和管理广告网络营销活动的效果](monitor-performance-campaigns.md)

