---
title: 概述 [!DNL Analytics for Advertising]
description: 概述 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---

# 概述 [!DNL Analytics for Advertising]

*使用Advertising DSP和的广告商[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] 集成Adobe Analytics和Adobe Advertising以扩展和增强每个产品的功能。

该集成允许广告商跟踪其中的点进和浏览网站交互 [!DNL Analytics] 实例，允许品牌了解其广告支出如何导致网站参与和关键业务目标。

此外，Adobe Advertising可以访问庞大的第一方数据，这些数据 [!DNL Analytics] 收集使用 [!DNL Analytics] 标记已存在于网站上。 这允许进行更强大的历程管理、第一方再营销和付费媒体网站报告。 Adobe Advertising可以进一步使用 [!DNL Analytics] 支出和竞价优化数据。

如果工作得当， [!DNL Analytics for Advertising] 模糊两个传统角色之间的界线：广告历程管理（通过广告将用户发送到站点的行为）和通过web analytics理解网站参与。

主要优点：

* 发送 [!DNL Analytics] 直接用于Adobe Advertising进行第一方网站再营销的区段。
* 使用 [!DNL Analytics] 自定义和标准事件作为转化信号，用于优化付费媒体广告。
* 充分利用 [!DNL Analytics] Analysis Workspace ，以更好地了解站点入口点和访问行为。
* 实现Web分析人员与付费媒体团队之间的更紧密协作。
* 在中使用永久性Adobe Advertising浏览和点进ID [!DNL Analytics] 以了解站点参与情况。
* 使用在将数据或像素导出到广告服务器或其他DSP时无法实现的自定义量度、自定义维度和网站活动，在Analysis Workspace中增强传统的付费媒体报表。
* 充分利用 [!DNL Analytics] 已在您的网站上存在用于在Adobe Advertising中进行跟踪和优化的代码。

>[!TIP]
>
> 观看 [视频简介 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics).

## 将Analytics用于付费媒体报表

[!DNL Analytics for Advertising] 通过允许您：

* 在中使用永久性Adobe Advertising浏览和点进ID [!DNL Analytics] 以了解站点参与情况。
* 利用Analysis Workspace更好地了解网站入口点和访问行为。 您可以访问付费媒体维度和事件数据，包括Adobe Advertising促销活动实体名称（具体到投放位置和广告）及其相关指标，如点击次数、展示次数和成本。

使用 [!DNL Analytics] 作为付费媒体报表工具，您的组织需要Experience Cloud登录才能访问Analysis Workspace。 您的Adobe Advertising团队将帮助您将Adobe Advertising数据映射到Analysis Workspace中的各个报表包。 您可以将Adobe Advertising数据发送到任何报表包，但您应该了解已映射到Adobe Advertising的报表包和未映射的报表包。根据报表包，这可能会更改报告的数据。

[Adobe AdvertisingID位于 [!DNL Analytics]](ids.md) 像其他一样工作 [!DNL eVars]，具有自定义的永久过期时间。 默认情况下，归因回顾时间范围在Adobe Advertising实施期间设置为60天。 要更改此设置，请与您的Adobe客户团队合作。

Adobe Advertising维度会附加后缀“(AMO ID)”(例如“广告类型(AMO ID)”)。 请参阅&quot;[Analysis Workspace中的Adobe Advertising指标](advertising-metrics-in-analytics.md)”以获取可用维度的列表。

>[!NOTE]
>
> 在中查看Adobe Advertising数据（或任何数据集）时 [!DNL Analytics]，请注意，量度和报表基于在中设置的规则 [!DNL Analytics]. 数据可能不同于您在其他报表系统中看到的内容，例如广告服务器报表、 [!DNL DSP] 报表或搜索引擎报表。 要了解数据差异，请执行以下操作： [!DNL Analytics]，您需要知道 [!DNL eVar] 数据过期、访问定义、被视为最后接触归因与总持久归因及其他因素。 有关更多信息，请参阅 [之间的预期数据差异 [!DNL Analytics] 和Adobe Advertising](data-variances.md).

## 使用Analytics增强Adobe Advertising活动和Portfolio效果

不需要任何额外的像素， [!DNL Analytics for Advertising] 通过向Adobe Advertising发送两个主要信号，可实现更好的优化和更简单的受众分段：

* 要用作竞价信号的转换量度：
   * 标准量度，例如 [!UICONTROL Revenue] 和 [!UICONTROL Cart Views].
   * 网站参与量度，如页面查看和访问量度。
   * 自定义收入量度。
   * 保留的收入量度。
* 在中创建的区段 [!DNL Analytics] 并发布到Experience Cloud。

  您可以使用 [!DNL Analytics] 中用于第一方网站重定位的区段 [!DNL DSP] 和付费搜索广告。

  ([!DNL Search, Social, & Commerce] 仅限)广告商使用 [!DNL Analytics] 但是，Audience Manager无法从创建基于Google网站标签的受众（再营销列表）和客户匹配受众（客户列表） [!DNL Analytics] 与Experience Cloud共享的区段。

### 作为竞价信号的网站转化量度

您可以从以下位置使用标准事件和自定义事件： [!DNL Analytics] 在Adobe Advertising中构建加权目标。 目标为以下项目的竞价决策提供信息 [!DNL DSP] 包和搜索项目组合。

>[!NOTE]
>
> 您无法从以下位置映射计算量度 [!DNL Analytics] Adobe Advertising。

您的Adobe Advertising团队将帮助您识别适用于付费媒体性能的事件并将其映射到Adobe Advertising中，这些事件在 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions].

请参阅&quot;[Adobe Advertising中的Analytics量度](analytics-data-in-advertising.md)”以获取可用量度的列表。

### 用于网站重定向的Analytics区段

Adobe Advertising可以摄取 [!DNL Analytics] 用于Advertising DSP和再营销的区段 [!DNL Search, Social, & Commerce] 使用本机Experience Cloud受众集成的广告，介于 [!DNL Analytics] 和Experience Cloud。

要访问 [!DNL Analytics] 区段，广告商帐户需要具有 [Experience CloudID服务](https://experienceleague.adobe.com/docs/id-service/using/home.html) 已启用。 启用ID服务后，所有Experience Cloud区段(包括在 [!DNL Analytics] 并发布到Experience Cloud，在Adobe Audience Manager中创建的区段，在Experience Cloud中创建的区段，使用 [!DNL People core service]、以及在Adobe Experience Platform中创建并通过Audience Manager发送到Adobe Advertising的区段)一旦经过处理，即可在Adobe Advertising中使用。

[!DNL Analytics] 区段可在24小时内提供，并每天更新。

有关Experience Cloud受众服务的更多信息，请参阅 [Experience Cloud受众](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## 如何使用集成的示例 {#integration-examples}

### 在Analysis Workspace中使用Adobe Advertising数据

要了解如何在Analysis Workspace中使用Adobe Advertising数据创建可视化报表，请观看视频»[Workspace和报表简介](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html)“

#### 在报表中使用连接的电视显示到达转换

*仅限Advertising DSP用户*

您可以通过将CTV设备上的广告曝光与网站转化关联，来衡量连接电视(CTV)促销活动的全面漏斗有效性。 新 [!UICONTROL Landing Type] 过滤器&#39;&#39;[!UICONTROL View-through (CTV)]”将转化拆分为单独的行 [!UICONTROL Click Through]， [!UICONTROL View Through]、和 [!UICONTROL View Through (CTV)] 值。

要查看您的CTV浏览转化量度，请使用Analysis Workspace中的“版面”视图或“营销渠道”视图。

使用“版面”视图：

1. 在报表视图中包括CTV支出投放位置。

1. 包括所需的量度，如“展示次数”、“点击次数”等。

1. 应用以下过滤器：

   广告平台： `Advertising Cloud DSP`

   登陆页面： `View-Through (CTV)`

使用“营销渠道”视图：

1. 包含维度 `Marketing Channel`.

1. 包括所需的量度，如“展示次数”、“点击次数”等。

1. 应用以下过滤器：

   广告平台： `Advertising Cloud DSP`

   登陆页面： `View-Through (CTV)`

### 创建Adobe Advertising仪表板

要了解如何根据Analysis Workspace中的目标跟踪Adobe Advertising数据，请观看视频»[使用Adobe Analytics创建Adobe Advertising功能板](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html)“

### 使用Adobe AdvertisingID进行网站条目分析

要了解如何创建Adobe Advertising站点登入报表以监测每周的某天、每天的某个时间、浏览器和地理影响，请观看视频”[创建Adobe Advertising站点登入报表](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html)“

>[!MORELIKETHIS]
>
>* [视频：简介 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [实施的先决条件和关键信息 [!DNL Analytics for Advertising]](prerequisites.md)
>* [Analytics使用的Adobe AdvertisingID](ids.md)
>* [适用于Analytics for Advertising的JavaScript代码](/help/integrations/analytics/javascript.md)
>* [之间的预期数据差异 [!DNL Analytics] 和Adobe Advertising](data-variances.md)
>* [Analysis Workspace中的Adobe Advertising指标](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe Advertising中的数据](/help/integrations/analytics/analytics-data-in-advertising.md)
