---
title: ‘[!DNL Microsoft Advertising] 转化数据
description: 了解以下类型的信息 [!DNL Microsoft Advertising] — 跟踪的转化数据可在Search、Social和Commerce中使用。
source-git-commit: 355796d65e5de0dba9111e77fc594a3e50e6ec5e
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] 搜索、社交和商务中的转化数据

搜索、社交和商务会自动同步您跟踪的所有转化 [Microsoft Advertising通用事件跟踪(UET)标记](https://about.ads.microsoft.com/solutions/tools/universal-event-tracking) 用于网站转化（包括浏览转化率），用于报表和优化。

所有量度都会自动显示在营销活动管理视图和基本报表中，并可用于优化Microsoft广告营销活动的项目组合目标。

## 可用的转化数据

搜索、社交和商务会同步“”的转化数据[!DNL Include in 'Conversions']”选项已启用，提取过去35天的数据，然后到09时每天提取对数据的更改:00-10:00（广告商所在时区）。 由于每次点击都会跟踪新转化，因此历史数据可能会每天发生更改。

每个属性有两个事务属性 [[!DNL Microsoft Advertising] — 跟踪的转化](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) （您在中设置的） [!DNL Microsoft Advertising])，使用中配置的转化名称，自动在Search、Social和Commerce中可用 [!DNL Microsoft Advertising]. 每次转换的交易属性包括：

* `<conversion-name>`  — 关键字的转化值（如Purchase）。

  >[!TIP]
  >
  >在项目组合的目标中使用此类型的属性，项目组合包括 [!DNL Microsoft Advertising] 具有最大转化值和目标ROAS竞价策略的促销活动。

* `CT_<conversion-name>`  — 以“CT_”前缀（例如CT_Purchase）开头的转换次数（计数）。

  >[!TIP]
  >
  >在项目组合的目标中使用此类型的属性，项目组合包括 [!DNL Microsoft Advertising] 具有最大转化次数和目标CPA竞价策略的营销活动。

数据根据点击时间和从为帐户启用该功能之日起的转化/交易时间提供。

<!-- verify below/ if equivalent

[!DNL Microsoft Advertising] records each conversion by [bid unit](/help/search-social-commerce/glossary.md#a-b), device, and click date (not conversion date). Attribution is based on the default attribution setting for each metric in [!DNL Microsoft Advertising]; Adobe Advertising attribution isn't factored in because click event-level data isn't available.
-->

>[!NOTE]
>
>* 如果多个帐户具有相同的转化名称，则在Adobe Advertising中可能会看到重复的转化名称。 如果发生这种情况， [更改显示名称](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) 中的某个重复量度 [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. 当两个不同的量度具有相同的名称时，报表不准确。
>* 竞价单位级别的数据与同一级别的广告网络中的数据相匹配。 但是，广告网络自己的较高级别的转化数据可能包括未归因到子竞价单位的附加转化。 搜索、Social和Commerce中的数据始终从竞价单位级别累计，因此，例如，促销活动级别报表的总计可能与广告网络中的促销活动级别报表的总计不同。
>* 数据差异通常在晨同步后小于当天晚些时候（此时尚未同步其他转化）。 我们建议在早上验证数据。
>* 由于受众或地理位置级别没有数据，因此不用于自动优化RLSA和位置竞价调整。

## 如何比较中的转化数据 [!DNL Microsoft Advertising] 包含搜索、社交和商务中的数据

使用以下报表设置验证可比数据。

### 在中使用的报表设置 [!DNL Microsoft Advertising]

按天生成所选转化操作的报告，并包括所有广告状态的数据。

### 要在Search、Social和Commerce中使用的报表设置

在Search、Social和Commerce中，使用查看或报表选项查看基于点击日期（而非交易日期）的转化。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. 在数据表上方的工具栏中，单击 **[!UICONTROL Create Report]**，将光标悬停在上方 **[!UICONTROL Basic Reports]**，然后单击 **[!UICONTROL Search Engine Account Report]**.

1. 在 [!UICONTROL Report Settings] 窗口中，指定以下报表设置：

   1. 在 **[!UICONTROL Conversions Based]** 在部分中，选择 **[!UICONTROL Click date]**.

   1. 指定用于 [!DNL Microsoft Advertising] 报告。

   1. 在 **[!UICONTROL Search/Content]** 部分，选择 **[!UICONTROL Search Only]**.

   1. 在 **[!UICONTROL Search Engine Hierarchy]** 部分，展开 [!UICONTROL Microsoft Advertising] 部分并选择帐户。

   1. 打开 [!UICONTROL Columns] 选项卡，然后添加 [!DNL Microsoft Advertising] 要比较的指标。

1. 单击 **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [实施广告网络帐户和营销活动概述](campaign-implemention-overview.md)
>* [监控和管理广告网络营销活动的效果](monitor-performance-campaigns.md)
>* [查看为广告商跟踪的交易记录属性](/help/search-social-commerce/admin/transaction-properties/transaction-property-view-tracked.html?lang=en)
