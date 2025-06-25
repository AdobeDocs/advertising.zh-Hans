---
title: '[!DNL Google Ads]转化数据'
description: 了解Search、Social和Commerce中可用的 [!DNL Google Ads]跟踪的转化数据类型。
exl-id: a4634410-446b-4e2e-a52f-22a494f731f9
feature: Search Campaign Management, Conversions
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# 搜索、社交和Commerce中的[!DNL Google Ads]转化数据

Search、Social和Commerce会自动将[!DNL Google Ads]搜索和购物网络上所有营销活动的[!DNL Google Ads]跟踪的转化数据同步到Search、Social和Commerce中，以便生成报表和进行优化。

所有量度都会自动在您的营销活动管理视图和基本报表中可用，也可用于组合目标以进行优化。

## 可用的转化数据

搜索、Social和Commerce同步启用了“[!DNL Include in 'Conversions']”选项的转化数据，提取过去35天的数据，然后按广告商所在时区的09:00-10:00每天提取对数据所做的更改。 由于每次点击都会跟踪新转化，因此历史数据可能会每天发生更改。

使用[!DNL Google Ads]中配置的转化名称，在Search、Social和Commerce中为[[!DNL Google Ads]跟踪的每次转化](https://support.google.com/google-ads/answer/4677036)（您在[!DNL Google Ads]中设置）自动提供最多三个量度。 每次转化的量度包括：

<!--

* `<conversion-name>` &mdash; (When you track it) The conversion value for the keyword, beginning with the "GGL" prefix (such as GGL Purchase).

`CT_<conversion-name>` &mdash; The number (count) of conversions, beginning with the "GGL_CT" prefix (such as GGL_CT_Purchase).

* `XD_<conversion-name>` &mdash; (When available for the conversion type, when you track them) The number (count) of cross-device conversions, as measured by Google, beginning with the "GGL_XD_CT_" prefix (such as GGL_XD_CT_Purchase).

-->

* `GGL*` — （跟踪时）关键字的转化值，以“GGL”前缀开头（如GGL Purchase）。

* `GGL_CT*` — 以“GGL_CT”前缀（如GGL_CT_Purchase）开头的转换次数（计数）。

* `GGL_XD_CT*` — （当可用于转化类型时，当您跟踪这些类型时）由Google测量的跨设备转化次数（计数），以“GGL_XD_CT_”前缀(例如GGL_XD_CT_Purchase)开头。

[!DNL Google Ads]按[竞价单位](/help/search-social-commerce/glossary.md#a-b)、设备和点击日期（不是转换日期）记录每次转换。 归因基于[!DNL Google Ads]中每个量度的默认归因设置；Adobe Advertising归因未计入中，因为点击事件级别数据不可用。

>[!NOTE]
>
>* 如果您有多个帐户具有相同的转化名称，则您可能会在Adobe Advertising中看到重复的转化名称。 如果发生这种情况，请在[!UICONTROL Admin] > [!UICONTROL Conversions]中更改其中一个重复量度的显示名称[&#128279;](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md)。 当两个不同的量度具有相同的名称时，报表不准确。
>* 竞价单位级别的数据与同一级别[!DNL Google Ads]中的数据匹配。 但是，[!DNL Google Ads]自己的更高级别的转化数据可能包含未归因到子竞价单位的附加转化。 搜索、Social和Commerce中的数据始终从竞价单位级别汇总，因此，例如，促销活动级别报表的总数可能与Google Ads中的促销活动级别报表的总数不同。
>* 通常，在早上同步之后，数据差异小于当天晚些时候，此时尚未同步其他转化。 我们建议在早上验证数据。
>* 转化数据对于[!DNL Google Display Network]、[!DNL Gmail]、[!DNL Mobile App]和[!DNL YouTube]广告不可用。 在将[!DNL Google Ads]中的数据与Search、Social和Commerce中的数据比较时，筛选掉这些类型的广告。
>* [!DNL Google Ads]转化数据在受众或地理位置级别不可用，因此不用于自动优化RLSA和位置竞价调整。

## 如何将[!DNL Google Ads]中的转化数据与Search、Social和Commerce中的数据进行比较

如果您将“搜索”、“社交”和“Commerce”中的数据与[!DNL Google Ads]中的数据进行比较，请使用查看或报表选项来查看基于点击日期（而非交易日期）的转化。

使用以下报表设置验证可比数据。

### 要在[!DNL Google Ads]中使用的报表设置

按天生成所选转化操作的报表，并包括所有广告状态的数据。

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

### 要在“搜索”、“社交”和“Commerce”中使用的报表设置

在“搜索”、“社交”和“Commerce”中，使用查看或报表选项查看基于点击日期（而非交易日期）的转化。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Create Report]**，将光标悬停在&#x200B;**[!UICONTROL Basic Reports]**&#x200B;上，然后单击&#x200B;**[!UICONTROL Search Engine Account Report]**。

1. 在[!UICONTROL Report Settings]窗口中，指定以下报表设置：

   1. 在“**[!UICONTROL Conversions Based]** on”部分中，选择&#x200B;**[!UICONTROL Click date]**。

   1. 指定用于[!DNL Google Ads]报表的相同日期范围。

   1. 在&#x200B;**[!UICONTROL Search/Content]**&#x200B;部分中，选择&#x200B;**[!UICONTROL Search Only]**。

   1. 在&#x200B;**[!UICONTROL Search Engine Hierarchy]**&#x200B;部分中，展开[!UICONTROL Google Adwords]部分并选择帐户。

   1. 打开[!UICONTROL Columns]选项卡，并添加要比较的[!DNL Google Ads]量度（以“GGL”开头）。

1. 单击&#x200B;**[!UICONTROL Create]**。

>[!MORELIKETHIS]
>
>* [实施广告网络帐户和营销活动概述](campaign-implemention-overview.md)
>* [监视和管理广告网络营销活动的效果](monitor-performance-campaigns.md)
>* [查看为广告商跟踪的转化量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
>* [为 [!DNL Google Ads]](/help/search-social-commerce/admin/conversion-metrics/conversion-tag-google.md)创建转化标记
>* [上载离线转化数据以进行增强型转化](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
