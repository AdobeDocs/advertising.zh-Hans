---
title: 关于自定义报表
description: 了解用于手动或使用预配置的报表模板创建自定义报表的选项。
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: a643a2d255431c5ce93f2df092d92932d4cccc02
workflow-type: tm+mt
source-wordcount: '1623'
ht-degree: 0%

---

# 关于自定义报表

通过自定义报表，您可以使用促销活动维度（如广告商、版面、网站或地标）以及对您最重要的量度来自定义报表数据的内容和交付。 您可以：

* 在粒度级别完全配置营销活动效果报表。

* 从预配置的报表模板中进行选择，并可以选择进一步自定义它们。

您可以按照指定的条件（例如每15天或每月1日），在指定的时区的03:00生成一次报告，或安排每日、每周或每月生成一次报告。 生成报告后，您可以从[!UICONTROL Reports] > [!UICONTROL Custom Reports]或链接的[报告目标](/help/dsp/reports/report-destinations/report-destination-about.md)以下类型下载报告：

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* FTP SSL <!-- (in beta) -->
* SFTP

>[!NOTE]
>
>您还可以在相关促销活动管理视图[中查看促销活动](/help/dsp/campaign-management/reports/campaign-reports-about.md)的所有级别（促销活动、包、投放位置或广告）的按需数据。

## 可用报表类型

* **[!UICONTROL Custom]：**&#x200B;此报表是一个空白模板，您可以使用它创建自己的自定义报表，其中使用了大多数维度和量度。 [!UICONTROL Conversion]、[!UICONTROL Device]、[!UICONTROL Geo]和[!UICONTROL Site]报告是此模板的变体，具有针对其各自用例预先选择的列和维度。

* 预配置的报告模板

   * **[!UICONTROL All-in Cost BETA]**：(仅同时具有Advertising Creative和Advertising DSP的广告商；测试版功能)使用此报表可查看Advertising DSP为Adobe Creative提供的广告服务产生了多少费用。 您可以在促销活动、资源包、版面和广告级别查看创意、属性、目标和其他数据。

   * **[!UICONTROL Billing]：**&#x200B;使用此报告了解关键计费指标，如按营销活动进行媒体计费的支出指标。 数据不可用于以通用ID为目标的投放位置。

     >[!NOTE]
     >
     >此报表包含有关计费区段的数据。 如果向用户或设备提供了属于多个区段的展示，则只有一个可计费区段会为该展示提供点数。

   * **[!UICONTROL Content]：**&#x200B;请使用此报告按照指定的内容维度（如流派、生产质量和内容评级）了解展示投放和其他量度，以便优化定位并确保品牌安全。 除了内容维度之外，该报表还包含大多数标准维度、量度和过滤器。 按内容维度的数据可用于[!DNL Freewheel]、[!DNL Index]、[!DNL Magnite]、[!DNL Microsoft]、[!DNL Nexxen]、[!DNL Pubmatic]、[!DNL Sharethrough]和[!DNL Triplelift]。 内容信号在竞价流期间由发布者传递，并受可用性限制。

   * **[!UICONTROL Conversion]：**&#x200B;请使用此报表根据通过Adobe Advertising转化跟踪捕获的转化量度，了解营销活动的执行情况。 此报表包含多点接触归因。

   * **[!UICONTROL Custom Creative]：** (仅使用Advertising Creative的广告商)使用此报告可跨Advertising Creative广告体验监控性能。

   * **[!UICONTROL Device]：**&#x200B;使用此预填充模板按设备相关的维度查看关键量度。

   * **[!UICONTROL Frequency (by Impression)]：**&#x200B;使用此报告了解向独特查看者显示的展示次数分布（例如，有多少独特查看者查看了一个展示次数、两个展示次数、三个展示次数等）。 数据按投放位置或营销活动提供。

     >[!NOTE]
     >
     >* 数据在2019年3月1日后可用。
     >* 基于数据采样来估计频率。
     >* 对于某些库存，发布者不会传递设备标识符，这会阻止频率跟踪。 此报表仅包含设备标识符可用的展示次数。

   * **[!UICONTROL Frequency (by App/Site)]：**&#x200B;使用此报告了解应用程序或网站访问您广告的独特用户数。 您还可以查看仅通过特定应用程序或网站访问广告的唯一用户数（“不同的唯一用户”）。

     >[!NOTE]
     >
     >* 数据在2018年11月15日后可用。
     >* 对于某些私有库存，发布者不会传递设备标识符，这会阻止频率跟踪。

   * **[!UICONTROL Geo]**：使用此预填充模板按地理维度查看关键量度。

   * **[!UICONTROL Household Conversions]：**&#x200B;使用此报表可查看基于IP地址的家庭级别（而非设备/Cookie级别）的浏览转化情况。 使用见解衡量和优化促销活动效果。 有关详细信息，请参阅[家庭报表常见问题解答](/help/dsp/reports/faq-reports.md)。 数据不可用于以通用ID为目标的投放位置。

   * **[!UICONTROL Household Reach & Frequency]：**&#x200B;使用此报表可根据IP地址而不是设备/Cookie级别，在家庭级别查看跨广告格式的单个维度的展示次数、覆盖范围和频率。 利用这些见解优化您的媒体组合、提高性能并发现增量访问的机会。 有关详细信息，请参阅[家庭报表常见问题解答](/help/dsp/reports/faq-reports.md)。 数据不可用于以通用ID为目标的投放位置。

   * **[!UICONTROL Margin]：**&#x200B;使用此报表按促销活动或投放位置查看关键量度，如利润、利润和其他支出量度。 数据不可用于以通用ID为目标的投放位置。

   * **[!UICONTROL Path to Conversion]：**&#x200B;请使用此报告确定如何优化预算并根据表现最佳的广告交互序列对广告进行个性化设置。 报表会显示同一家庭中导致指定数据范围内每个选定转化量度的交互点序列。 报表在首次交互和转化之间使用指定的回顾时间段，并可包含一个维度：

      * [!UICONTROL Channel Assist Type]：显示以下营销渠道如何协助转换过程：[!UICONTROL Audio Impression]、[!UICONTROL CTV Impression]、[!UICONTROL Display Click]、[!UICONTROL Display Impression]、[!UICONTROL Native Click]、[!UICONTROL Native Impression]、[!UICONTROL Search Click]、[!UICONTROL Video Click]或[!UICONTROL Video Impression]。

      * [!UICONTROL Campaign ID]或[!UICONTROL Campaign Name]：显示哪些营销活动协助了转换过程。

      * [!UICONTROL Ad ID]或[!UICONTROL Ad Name]显示哪些DSP广告产生了转化。

      * [!UICONTROL Ad ID & Paid Keyword (SSC)]或[!UICONTROL Ad Name & Paid Keyword (SSC)]显示哪些Search、Social和Commerce关键字导致了转化。

     报表中的列包括“[!UICONTROL Event #1]”到“[!UICONTROL Event #10]”、“[!UICONTROL Path Length]”、“% \&lt;转化量度名称1\>”、“% \&lt;转化量度名称2\>”等。

     包括最近的10个交互点。 路径行按转化次数排序。

     若要将此报告与[!DNL Advanced Measurement Services]和Adobe Analytics创建的报告进行比较，请参阅“[关于自定义报告的常见问题解答](/help/dsp/reports/faq-reports.md)”。

   * **[!UICONTROL Path Length]：**&#x200B;使用此报表跟踪一段时间内转化所需的用户交互点数，以便您选择最佳广告频率。 此报表按路径长度（交互点）显示转化次数，例如用户仅有一个广告交互、两个广告交互等后发生的转化次数。 报表可以包含多个转化量度的数据，并在首次交互和转化之间使用指定的回顾时间段。 报表中的列包括“[!UICONTROL Path Length]”、“[!UICONTROL Number of] \&lt;转化量度名称1\>”、“% \&lt;转化量度名称1\>”、“\&lt;转化量度名称2\>”、“% \&lt;转化量度名称2\>”等。

     显示每个路径长度不超过10的数据；将路径长度大于10的数据分组在一起。

   * **[!UICONTROL Segment]：**&#x200B;使用此预填充模板按区段查看关键量度。

     >[!NOTE]
     >
     >* 此报表旨在显示不同目标区段的表现。 它使用区段成员资格数据。 当向属于两个或更多目标区段的人员或设备提供展示时，此报表会为每个区段包含一行。 因此，此报表中的总计可能与实际交付不匹配。
     >* 区段的转化量度和自定义目标数据在2019年8月2日之后可用。 区段的所有其他数据自2018年6月1日后开始可用。

   * **[!UICONTROL Site]：**&#x200B;默认情况下，包括按网站列出的标准量度、媒体净支出总额和可计费净支出总额。

   * **[!UICONTROL Time to Conversion]：**&#x200B;使用此报告可确定最佳的归因回顾时间范围，并识别转化时间较长的营销活动，这可能会受益于重新定位。 此报表按自上次交互（广告曝光或点击）到转化的时间长度（以天为单位）显示转化的次数。 报表可以包含多个转化量度的数据，并在首次交互和转化之间使用指定的回顾时间段。 报表中的列包括“[!UICONTROL Time Taken (in days)]”、“[!UICONTROL Number of] \&lt;转化量度名称1\>”、“% \&lt;转化量度名称1\>”、“\&lt;转化量度名称2\>”、“% \&lt;转化量度名称2\>”等。 需要超过回顾期间的转化将分组在一行中（例如，如果报表使用的回顾期间为30天，则所有需要超过30天的转化将分组在一行中，其中的“[!UICONTROL Time Taken (in days)]”值为“30+”）。

## 跨帐户报告 {#cross-account-reporting}

任何拥有多个DSP帐户的组织都可以根据需要选择在自定义报表中启用跨帐户数据。 例如，您可以授予帐户A访问帐户B数据的权限，并授予帐户B访问帐户C（但不访问帐户A）数据的权限。 要启用并配置此功能，请联系您的Adobe客户团队。

为您的组织启用该功能后，您就可以按帐户[筛选](report-settings.md)以下任何报表类型： [!UICONTROL Custom]、[!UICONTROL Site]、[!UICONTROL Segment]、[!UICONTROL Geo]、[!UICONTROL Device]、[!UICONTROL Frequency (by Impression)]和[!UICONTROL Conversion]。

位于[!UICONTROL Settings] > [!UICONTROL Account]的帐户设置表示a)其数据可用于您的帐户的其他帐户，以及b)可以访问您帐户数据的其他帐户。

## [!UICONTROL Custom Reports]视图

[!UICONTROL Reports] > [!UICONTROL Custom Reports]列出了您的现有报告，包括已生成的报告、计划将来生成的报告以及失败的报告。 “[!UICONTROL Report Run]”列显示从2024年8月22日开始触发报告的日期。 默认情况下，将列出用户创建的所有未存档报表，最新的报表位于顶部。 您可以按状态（报表是定期还是单次）、报表类型、目标类型和报表创建者进一步筛选列表。

您可以创建新自定义报告，编辑现有报告或复制它们以创建新报告，立即运行报告，下载过去四个月的任何报告实例和删除报告。

## 报表状态 {#custom-report-status}

* **[!UICONTROL Yet to start]：**&#x200B;报告从未运行。

* **[!UICONTROL Report generating]：**&#x200B;当前正在创建报告。

* **[!UICONTROL Ready to download]：** （仅定期报告）报告的一个或多个实例可供下载，并且已计划多个报告实例。

* **[!UICONTROL Failed]：**&#x200B;报告作业失败。 要了解报表包的单个报表实例失败的原因，请单击![旁边的](/help/dsp/assets/chevron-down.png "向下箭头")向下箭头[!UICONTROL Download]。 失败的报表作业指示有错误图标(![错误指示器](/help/dsp/assets/indicator-critical.png "错误指示器"))。 将光标悬停在错误图标上可查看错误说明。

* **[!UICONTROL Completed]：**&#x200B;对于非周期性报表，报表已完成。 对于定期报表，已完成所有报表实例。 您可以下载过去四个月内完成的所有报表。

* **[!UICONTROL Archived]：**&#x200B;报告已存档，无法运行。 当报表生成多次失败，则会设置此状态。 目前，您无法从用户界面设置此状态。

>[!MORELIKETHIS]
>
>* [创建自定义报告](/help/dsp/reports/report-create.md)
>* [下载自定义报告](/help/dsp/reports/report-download.md)
>* [自定义报表设置](/help/dsp/reports/report-settings.md)
>* [有关家庭报告的常见问题解答](/help/dsp/reports/faq-reports.md)
>* 营销活动管理视图中的[性能报表类型](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [可用报告列](/help/dsp/reports/report-columns.md)
>* [关于[!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
