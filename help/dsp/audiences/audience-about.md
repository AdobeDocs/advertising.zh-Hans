---
title: 关于Advertising DSP中的受众管理
description: 了解受众管理功能。
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# 关于Advertising DSP中的受众管理

在DSP中，您可以创建和管理受众区段和受众集，并将其用作投放的目标：

* 您可以通过创建和实施区段来收集您自己的第一方受众数据。 您稍后可以使用广告重新定位区段中的用户，或者阻止区段中的用户接收广告。 您可以创建以下类型的区段：

   * [自定义区段](/help/dsp/audiences/custom-segment-create.md) 跟踪a)从桌面、移动设备和CTV设备向广告展示的用户，以及b)访问特定网页的用户。

   * [CCPA选择退出销售区段](/help/dsp/audiences/ccpa-opt-out-segment-create.md) 要根据加州消费者隐私法案(CCPA)跟踪网站上消费者选择退出销售请求的用户ID。 您可以从选择退出销售请求中检索用户ID的每月报表。

      有关CCPA选择退出销售请求的Adobe广告支持的更多信息，请参阅 [Adobe广告对《加州消费者隐私法案》的支持：消费者选择退出支持](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* 您可以创建受众库，包括 [可重用受众](/help/dsp/audiences/reusable-audience-create.md). 保存的受众由任何可用受众区段和任何其他保存的受众组成。 您对保存的受众所做的任何更改会自动应用于定位或排除该受众的所有投放位置，并应用于包括保存的受众的所有其他受众。

   保存的受众允许媒体规划者根据需要对受众进行分组，具体做法是使用复杂的布尔逻辑包含和排除多个区段。 在构建受众时，将指示每个单独区段的大小和总受众大小。 然后，Campaign执行者只需选择一个或多个保存的受众作为投放目标，而无需为每个投放手动配置受众目标。

其他受众类型也可用于投放定位。

## 导入第一方和第三方数据区段

DSP可以从数据管理平台(DMP)导入您自己的第一方数据区段，并根据需要将其提供给任何一组广告商。

DSP是以下项的集成目标 [此 [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html)，从而允许您与批准广告商和用户共享经过身份验证的第一方区段，以激活营销活动。 要了解有关Real-Time CDP集成的更多信息，请参阅 [“源”部分](/help/dsp/audiences/sources/source-about.md).

DSP还可以导入自定义的第三方区段，包括第三方区段的复杂组合。 您可以根据需要向任何一组广告商提供区段。

有关更多信息，请与您的Adobe客户团队联系。

## 可用作投放目标的受众

您可以将投放位置定位到以下所有类型的受众。

* 所有用户创建的受众集(保存在DSP中)。

* 在DSP中创建的所有用户创建的受众区段：

   * 访问特定网页的用户和展示特定广告印象的用户适用的自定义区段。

   * 根据加州消费者隐私法案(CCPA)，对于在您的网站上提交选择退出销售请求的用户，CCPA选择退出销售受众区段。

* 您导入的所有第一方数据区段。

* 所有导入的自定义第三方数据区段。

* （仅针对美国的投放位置） [向30多家提供商的DSP客户提供的所有第三方数据区段](/help/dsp/audiences/third-party-data-providers.md)，包括 [!DNL Acxiom]， [!DNL Datalogix]， [!DNL eXelate] ([!DNL Nielsen])， [!DNL Lotame]， [!DNL Oracle]， [!DNL Quantcast]，以及更多功能。

   您可以定位特定的区段，这些区段根据受众数据定位用户（例如，具有特定人口统计信息、兴趣或意图和/或行为配置文件的用户）。 您可以按数据提供器和类别浏览，按名称或区段ID搜索区段，或按数据提供器、区段总大小、Web浏览器计数或设备计数筛选结果。

   第三方区段会产生额外费用，这些费用显示在每个区段名称旁边。

* (使用Adobe Experience Platform和的广告商 [!DNL Real-Time CDP]、Adobe Audience Manager或Adobe Analytics(仅使用Adobe广告JavaScript转化标记)您所有可用的第一方、第二方或第三方受众区段，均创建于 [!DNL Real-Time CDP]，在Audience Manager中创建，或从Audience Manager发布到Adobe Experience Cloud，或 [!DNL Analytics].

   使用分部的定价是预先协商的，在DSP中不可见。

   区段自 [!DNL Analytics] 可在创建或发布为Experience Cloud受众后大约一小时内可用。 直接来自Audience Manager或的区段 [!DNL Real-Time CDP] 会在您共享它们后的24小时内提供。

   >[!NOTE]
   >
   >请参阅相关文档 [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html)， [分析](https://experienceleague.adobe.com/docs/analytics.html)、和 [此 [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) 有关在这些解决方案中为区段设置和收集数据的信息。

## 受众规模数据

在保存的受众设置和投放位置设置中，您可以看到详细的受众规模数据：

* 系统会显示所有选定区段和已保存受众中经过重复数据删除的活跃受众总人数，您可以按设备类型（浏览器、移动设备或连接的电视机）查看详细信息。

   ![组合的受众规模](/help/dsp/assets/audience-size.png)

* 对于单个区段和已保存的受众，总受众规模和CPM（如果适用）显示在区段名称旁边。 您可以查看有关区段的更多详细信息，包括按设备类型（浏览器、移动设备或连接的电视机）显示的大小。 对于保存的受众，总大小是经过重复数据删除的总大小。

   ![单个区段的大小](/help/dsp/assets/audience-size-segment.png)

## 受众视图

### “所有受众”视图

在 [!UICONTROL All Audiences] 查看或受众库，您可以保存和管理可重用受众，其中包括受众区段组，甚至包括其他保存的受众。 您可以将受众用作多个投放位置的目标。 版面名称旁边显示了每个受众使用的版面数量。

您可以编辑、克隆、删除、导出或共享任何受众。

### 区段视图

在 [!UICONTROL Segments] 视图，则所有用户均可创建其他自定义区段。

此 [!UICONTROL Segments] 视图还列出了以下区段类型：

* 用户创建的所有自定义区段都可供用户使用。

   您可以查看所创建的任何自定义区段的跟踪标记，并与其他用户共享这些区段。 您还可以编辑或删除您创建的自定义区段。

   您无法编辑或共享其他用户与您共享的自定义区段。

* 用户可以使用所有导入的第一方区段。

   您无法编辑或共享与您共享的第一方区段。 如果您需要与其他用户共享第一方区段，请联系您的Adobe客户团队。

* 用户可用的所有自定义第三方区段。

   您无法编辑或共享与您共享的第三方区段。 如果您需要与其他用户共享第三方区段，请联系您的Adobe客户团队。

>[!MORELIKETHIS]
>
>* [创建可重复使用的受众](reusable-audience-create.md)
>* [受众设置](audience-settings.md)
>* [受众区段逻辑的语法](audience-segment-logic-syntax.md)
>* [创建和实施自定义区段](custom-segment-create.md)
>* [创建并实施 [!UICONTROL CCPA Opt-Out-of-Sale] 区段](ccpa-opt-out-segment-create.md)
>* [可用的第三方数据提供商](third-party-data-providers.md)
>* [置入设置](/help/dsp/campaign-management/placements/placement-settings.md)

