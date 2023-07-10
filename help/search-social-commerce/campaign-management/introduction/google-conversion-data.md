---
title: ‘[!DNL Google Ads] 转化数据
description: 了解以下类型的信息 [!DNL Google Ads] — 跟踪的转化数据可在Search、Social和Commerce中使用。
exl-id: a7ee8e72-aa7d-4e90-b765-b7b01308762d
source-git-commit: 29cda72cac949663cd2df822cf7223335a14504d
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 0%

---

# [!DNL Google Ads] 搜索、社交和商务中的转化数据

搜索、社交和商务自动同步 [!DNL Google Ads] — 跟踪了 [!DNL Google Ads] 将搜索和购物网络移入搜索、社交和商务，以便报告和优化。

所有量度都会自动显示在营销活动管理视图和基本报表中，并可用于组合目标以进行优化。

## 可用的转化数据

搜索、社交和商务会同步“”的转化数据[!DNL Include in 'Conversions']”选项已启用，提取过去35天的数据，然后到09时每天提取对数据的更改:00-10:00（广告商所在时区）。 由于每次点击都会跟踪新转化，因此历史数据可能会每天发生更改。

每项最多有三个交易属性 [[!DNL Google Ads] — 跟踪的转化](https://support.google.com/google-ads/answer/4677036) （您在中设置的） [!DNL Google Ads])，使用中配置的转化名称，自动在Search、Social和Commerce中可用 [!DNL Google Ads]. 每次转换的交易属性包括：

* `GGL*`  — （跟踪时）关键字的转化值，以“GGL”前缀开头（例如GGL Purchase）。

* `GGL_CT*`  — 转换次数（计数），以“GGL_CT”前缀（例如GGL_CT_Purchase）开头。

* `GGL_XD_CT*`  — （当可用于转化类型时，当您跟踪这些类型时）由Google测量的以“GGL_XD_CT_”前缀(例如GGL_XD_CT_Purchase)开头的跨设备转化次数（计数）。

[!DNL Google Ads] 记录每次转换的方式 [竞价单位](/help/search-social-commerce/glossary.md#a-b)，设备，然后单击日期（不是转换日期）。 归因基于中每个量度的默认归因设置 [!DNL Google Ads]；Adobe Advertising归因未计入中，因为单击事件级别数据不可用。

>[!NOTE]
>
>* 如果多个帐户具有相同的转化名称，则在Adobe Advertising中可能会看到重复的转化名称。 如果发生这种情况， [更改显示名称](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) 中的某个重复量度 [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. 当两个不同的量度具有相同的名称时，报表不准确。
>* 竞价单位级别的数据与中的数据匹配 [!DNL Google Ads] 在同一级别。 但是， [!DNL Google Ads]&#39;自己的更高级别的转化数据可能包含未归因到子竞价单位的更多转化。 搜索、Social和Commerce中的数据始终从竞价单位级别累计，因此，例如，促销活动级别报表的总数可能与Google Ads中的促销活动级别报表的总数不同。
>* 数据差异通常在晨同步后小于当天晚些时候（此时尚未同步其他转化）。 我们建议在早上验证数据。
>* 转化数据不可用于 [!DNL Google Display Network]， [!DNL Gmail]， [!DNL Mobile App]、和 [!DNL YouTube] 广告。 在比较以下位置的数据时，过滤掉这些类型的广告： [!DNL Google Ads] 包含搜索、社交和商务中的数据。
>* 数据 [!DNL Google Ads] 转化在受众或地理位置级别不可用，因此不用于自动优化RLSA和位置竞价调整。

## 如何比较中的转化数据 [!DNL Google Ads] 包含搜索、社交和商务中的数据

如果您将“搜索”、“社交”和“商务”中的数据与中的数据进行比较 [!DNL Google Ads]，使用查看或报表选项查看基于点击日期（而非交易日期）的转化。

使用以下报表设置验证可比数据。

### 在中使用的报表设置 [!DNL Google Ads]

按天生成所选转化操作的报告，并包括所有广告状态的数据。

<!-- 

1. In the main toolbar, select **[!DNL Reports] > [!DNL Report]**.

1. Select **[!DNL + Custom] > [!DNL Table]**.

1. From the left pane, specify the rows and columns in the report:
   
   1. Search for the **[!DNL Day]** field and it drag to the [!DNL Row] section.

   1. Search for the **[!DNL All conv].** field and it drag to the [!DNL Column] section.

   1. Search for the **[!DNL Conversion action]** field and it drag to the [!DNL Column] section.

1. In the report settings toolbar, select **[!DNL Filter] > [!DNL Ad status]**, and then select all boxes.

1. In the report settings toolbar, select **[!DNL Download] > [!DNL Excel .csv]**.

-->

### 要在Search、Social和Commerce中使用的报表设置

在Search、Social和Commerce中，使用查看或报表选项查看基于点击日期（而非交易日期）的转化。

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
>* [实施广告网络帐户和营销活动概述](campaign-implemention-overview.md)
>* [监控和管理广告网络营销活动的效果](monitor-performance-campaigns.md)
>* [查看为广告商跟踪的交易记录属性](/help/search-social-commerce/admin/transaction-properties/transaction-property-view-tracked.md)
