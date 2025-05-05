---
title: “[!DNL Microsoft Advertising]转换数据”
description: 了解Search、Social和Commerce中可用的 [!DNL Microsoft Advertising]跟踪的转化数据类型。
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
source-git-commit: b8a34f3d85947536eb92ee481966f84694250f29
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# 搜索、社交和Commerce中的[!DNL Microsoft Advertising]转化数据

搜索、Social和Commerce会自动同步您的[[!DNL Microsoft Advertising] 通用事件跟踪(UET)标记](https://help.ads.microsoft.com/#apex/ads/en/53056)所跟踪的所有网站转化次数（包括浏览转化次数），以便生成报告和进行优化。

所有量度都会自动在您的营销活动管理视图和基本报告中使用，并可用于优化[!DNL Microsoft Advertising]营销活动的项目组合目标。

## 可用的转化数据

搜索、Social和Commerce同步启用了“[!DNL Include in 'Conversions']”选项的转化数据，提取过去35天的数据，然后按广告商所在时区的09:00-10:00每天提取对数据所做的更改。 由于每次点击都会跟踪新转化，因此历史数据可能会每天发生更改。

使用[!DNL Microsoft Advertising]中配置的转化名称，每个[[!DNL Microsoft Advertising]跟踪的转化](https://help.ads.microsoft.com/apex/index/3/en-us/n5012)（您在[!DNL Microsoft Advertising]中设置）的两个量度在Search、Social和Commerce中自动可用。 每次转化的量度包括：

* `<conversion-name>` — 关键字的转化值（如Purchase）。

  >[!TIP]
  >
  >在包含具有最大转化值和目标ROAS竞价策略的[!DNL Microsoft Advertising]营销活动的项目组合的目标中使用此类型的转化量度。

* `CT_<conversion-name>` — 以“CT_”前缀（如CT_Purchase）开头的转换次数（计数）。

  >[!TIP]
  >
  >在包含[!DNL Microsoft Advertising]个营销活动且具有最大转化和目标CPA竞价策略的项目组合的目标中使用此类型的转化量度。

根据点击时间和自为帐户启用该功能之日起的转化/交易时间，数据可用。

[!DNL Microsoft Advertising]按[竞价单位](/help/search-social-commerce/glossary.md#a-b)、设备和点击日期（不是转换日期）记录每次转换。 归因基于[!DNL Microsoft Advertising]中每个量度的默认归因设置；Adobe Advertising归因未计入在内，因为点击事件级别数据不可用。

>[!NOTE]
>
>* 如果多个帐户具有相同的转化名称，则在Adobe Advertising中可能会看到重复的转化名称。 如果发生这种情况，请在[!UICONTROL Admin] > [!UICONTROL Conversions]中更改其中一个重复量度的显示名称[&#128279;](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md)。 当两个不同的量度具有相同的名称时，报表不准确。
>* 竞价单元级别的数据与同一级别广告网络中的数据匹配。 但是，广告网络自己的更高级别的转化数据可能包括未归因到子竞价单位的附加转化。 搜索、社交和Commerce中的数据始终从竞价单位级别汇总，因此，例如，促销活动级别的报表可能与广告网络中的促销活动级别报表具有不同的总计。
>* 通常，在早上同步之后，数据差异小于当天晚些时候，此时尚未同步其他转化。 我们建议在早上验证数据。
>* 在受众或地理位置级别没有可用数据，因此不用于自动优化RLSA和位置竞价调整。

## 如何将[!DNL Microsoft Advertising]中的转化数据与Search、Social和Commerce中的数据进行比较

使用以下报表设置验证可比数据。

### 要在[!DNL Microsoft Advertising]中使用的报表设置

按天生成所选转化操作的报表，并包括所有广告状态的数据。

### 要在“搜索”、“社交”和“Commerce”中使用的报表设置

在“搜索”、“社交”和“Commerce”中，使用查看或报表选项查看基于点击日期（而非交易日期）的转化。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Create Report]**，将光标悬停在&#x200B;**[!UICONTROL Basic Reports]**&#x200B;上，然后单击&#x200B;**[!UICONTROL Search Engine Account Report]**。

1. 在[!UICONTROL Report Settings]窗口中，指定以下报表设置：

   1. 在“**[!UICONTROL Conversions Based]** on”部分中，选择&#x200B;**[!UICONTROL Click date]**。

   1. 指定用于[!DNL Microsoft Advertising]报表的相同日期范围。

   1. 在&#x200B;**[!UICONTROL Search/Content]**&#x200B;部分中，选择&#x200B;**[!UICONTROL Search Only]**。

   1. 在&#x200B;**[!UICONTROL Search Engine Hierarchy]**&#x200B;部分中，展开[!UICONTROL Microsoft Advertising]部分并选择帐户。

   1. 打开[!UICONTROL Columns]选项卡，并添加要比较的[!DNL Microsoft Advertising]个量度。

1. 单击&#x200B;**[!UICONTROL Create]**。

>[!MORELIKETHIS]
>
>* [实施广告网络帐户和营销活动概述](campaign-implemention-overview.md)
>* [监视和管理广告网络营销活动的效果](monitor-performance-campaigns.md)
>* [查看为广告商跟踪的转化量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
