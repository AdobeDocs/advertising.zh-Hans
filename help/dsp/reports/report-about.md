---
title: 关于自定义报表
description: 了解用于手动或使用预配置的报表模板创建自定义报表的选项。
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: 44f7f9b31afbe6b863acd389df641057b1e6dea1
workflow-type: tm+mt
source-wordcount: '1059'
ht-degree: 0%

---

# 关于自定义报表

通过自定义报表，您可以使用促销活动维度（如广告商、版面、网站或地标）以及对您最重要的量度来自定义报表数据的内容和交付。 您可以：

* 在粒度级别完全配置营销活动效果报表。

* 从预配置的报表模板中进行选择，并可以选择进一步自定义它们。

您可以生成一次报表，或根据指定条件（例如每15天或每月第一天）安排在指定时区的03:00生成报表。 生成报告后，您可以从[!UICONTROL Reports] > [!UICONTROL Custom Reports]或链接的[报告目标](/help/dsp/reports/report-destinations/report-destination-about.md)以下类型下载报告：

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* FTP SSL <!-- (in beta) -->
* SFTP

>[!NOTE]
>
>您还可以在相关促销活动管理视图](/help/dsp/campaign-management/reports/campaign-reports-about.md)中查看促销活动[的所有级别（促销活动、包、投放位置或广告）的按需数据。

## 可用报表类型

* **[!UICONTROL Custom]：**&#x200B;此报表是一个空白模板，您可以使用大多数维度和量度创建自己的自定义报表。 [!UICONTROL Conversion]、[!UICONTROL Device]、[!UICONTROL Geo]和[!UICONTROL Site]报告是此模板的变体，具有针对其各自用例预先选择的列和维度。

* 预配置的报告模板

   * **[!UICONTROL Billing]：**&#x200B;使用此报告了解关键计费指标，如按营销活动进行媒体计费的支出指标。 数据不可用于以通用ID为目标的投放位置。

     >[!NOTE]
     >
     >此报表包含有关计费区段的数据。 如果向用户或设备提供了属于多个区段的展示，则只有一个可计费区段会为该展示提供点数。

   * **[!UICONTROL Conversion]：**&#x200B;使用此报表可根据使用Adobe Advertising转化跟踪捕获的转化指标了解营销活动的执行情况。 此报表包含多点接触归因。

   * **[!UICONTROL Device]：**&#x200B;使用此预填充模板按设备相关的维度查看关键量度。

   * **[!UICONTROL Frequency (by Impression)]：**&#x200B;使用此报告了解向独特查看者显示的展示次数分布（例如，有多少独特查看者查看了一个展示次数、两个展示次数、三个展示次数等）。 数据按投放位置或营销活动提供。

     >[!NOTE]
     >
     >* 数据在2019年3月1日之后提供。
     >* 基于数据采样来估计频率。
     >* 对于某些库存，发布者不会传递设备标识符，这会阻止频率跟踪。 此报表仅包含设备标识符可用的展示次数。

   * **[!UICONTROL Frequency (by App/Site)]：**&#x200B;请使用此报表了解应用程序或站点访问的独特用户数。 您还可以查看仅通过特定应用程序或站点（“不同的独特用户”）访问的独特用户数。

     >[!NOTE]
     >
     >* 数据在2018年11月15日后可用。
     >* 对于某些私有库存，发布者不会传递设备标识符，这会阻止频率跟踪。

   * **[!UICONTROL Geo]**：使用此预填充模板按地理维度查看关键量度。

   * **[!UICONTROL Margin]：**&#x200B;使用此报表按促销活动或投放位置查看关键量度，如利润、利润和其他支出量度。 数据不可用于以通用ID为目标的投放位置。

   * **[!UICONTROL Segment]：**&#x200B;使用此预填充模板按区段查看关键量度。

     >[!NOTE]
     >
     >* 此报表旨在显示不同目标区段的表现。 它使用区段成员资格数据。 当向属于两个或更多目标区段的人员或设备提供展示时，此报表会为每个区段包含一行。 因此，此报表中的总计可能与实际交付不匹配。
     >* 区段的转化指标和自定义目标数据在2019年8月2日之后可用。 区段的所有其他数据均可在2018年6月1日后开始使用。

   * **[!UICONTROL Site]：**&#x200B;默认情况下，包括按网站列出的标准量度、媒体净支出总额和可计费净支出总额。

   * **[!UICONTROL Household Reach & Frequency]：**&#x200B;使用此报表可根据IP地址而不是设备/Cookie级别，在家庭级别查看跨广告格式的单个维度的展示次数、覆盖范围和频率。 利用这些见解优化您的媒体组合、提高性能并发现增量访问的机会。 有关详细信息，请参阅[家庭报表常见问题解答](/help/dsp/reports/faq-household-report.md)。 数据不可用于以通用ID为目标的投放位置。

   * **[!UICONTROL Household Conversions]：**&#x200B;使用此报表可查看基于IP地址的家庭级别（而非设备/Cookie级别）的浏览转化情况。 使用见解衡量和优化促销活动效果。 有关详细信息，请参阅[家庭报表常见问题解答](/help/dsp/reports/faq-household-report.md)。 数据不可用于以通用ID为目标的投放位置。

## 跨帐户报告 {#cross-account-reporting}

拥有多个DSP帐户的任何组织都可以根据需要选择在自定义报表中启用跨帐户数据。 例如，您可以授予帐户A访问帐户B数据的权限，并授予帐户B访问帐户C（但不访问帐户A）数据的权限。 要启用并配置此功能，请与您的Adobe客户团队联系。

为您的组织启用该功能后，您就可以按帐户[筛选](report-settings.md)以下任何报表类型： [!UICONTROL Custom]、[!UICONTROL Site]、[!UICONTROL Segment]、[!UICONTROL Geo]、[!UICONTROL Device]、[!UICONTROL Frequency (by Impression)]和[!UICONTROL Conversion]。

位于[!UICONTROL Settings] > [!UICONTROL Account]的帐户设置表示a)其数据可用于您的帐户的其他帐户，以及b)可以访问您帐户数据的其他帐户。

## [!UICONTROL Custom Reports]视图

[!UICONTROL Reports] > [!UICONTROL Custom Reports]列出了您的现有报告，包括已生成的报告、计划将来生成的报告以及失败的报告。 “[!UICONTROL Report Run]”列显示从2024年8月22日开始触发报告的日期。 默认情况下，将列出用户创建的所有未存档报表，最新的报表位于顶部。 您可以按状态（报表是定期还是单次）、报表类型、目标类型和报表创建者进一步筛选列表。

您可以创建新自定义报告，编辑现有报告或复制它们以创建新报告，立即运行报告，下载过去四个月的任何报告实例和删除报告。

## 报表状态 {#custom-report-status}

* **[!UICONTROL Yet to start]：**&#x200B;报告从未运行。

* **[!UICONTROL Report generating]：**&#x200B;当前正在创建报告。

* **[!UICONTROL Ready to download]：** （仅定期报告）报告的一个或多个实例可供下载，并且已计划多个报告实例。

* **[!UICONTROL Failed]：**&#x200B;报告作业失败。 要了解报表包的单个报表实例失败的原因，请单击[!UICONTROL Download]旁边的![向下箭头](/help/dsp/assets/chevron-down.png "向下箭头")。 失败的报表作业指示有错误图标(![错误指示器](/help/dsp/assets/indicator-critical.png "错误指示器"))。 将光标悬停在错误图标上可查看错误说明。

* **[!UICONTROL Completed]：**&#x200B;对于非周期性报表，报表已完成。 对于定期报表，已完成所有报表实例。 您可以下载过去四个月内完成的所有报表。

* **[!UICONTROL Archived]：**&#x200B;报告已存档，无法运行。 当报表生成多次失败，则会设置此状态。 目前，您无法从用户界面设置此状态。

>[!MORELIKETHIS]
>
>* [创建自定义报告](/help/dsp/reports/report-create.md)
>* [下载自定义报告](/help/dsp/reports/report-download.md)
>* [自定义报表设置](/help/dsp/reports/report-settings.md)
>* [有关家庭报告的常见问题解答](/help/dsp/reports/faq-household-report.md)
>* Campaign Management视图中的[性能报告类型](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [可用报告列](/help/dsp/reports/report-columns.md)
>* [关于[!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
