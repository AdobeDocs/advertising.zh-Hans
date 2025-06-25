---
title: ' [!DNL Analytics for Advertising]概述'
description: ' [!DNL Analytics for Advertising]概述'
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# [!DNL Analytics for Advertising]概述

使用Advertising DSP和&#x200B;[!DNL Advertising Search, Social, & Commerce]*的*&#x200B;广告商

[!DNL Analytics for Advertising]集成了Adobe Analytics和Adobe Advertising以扩展和增强每个产品的功能。

该集成允许广告商跟踪其[!DNL Analytics]实例中的点进和浏览网站互动，允许品牌了解其广告支出如何导致网站参与和关键业务目标。

此外，Adobe Advertising可以访问[!DNL Analytics]使用网站上已存在的[!DNL Analytics]标记收集的大量第一方数据。 这允许进行更强大的历程管理、第一方再营销和付费媒体网站报告。 Adobe Advertising可进一步使用[!DNL Analytics]数据进行支出和竞价优化。

如果正确使用，[!DNL Analytics for Advertising]将模糊两个传统角色之间的界线：广告历程管理（通过广告将用户发送到站点的行为）和通过Web分析了解该站点参与度。

主要优点：

* 将[!DNL Analytics]区段直接发送到Adobe Advertising以进行第一方网站再营销。
* 使用[!DNL Analytics]个自定义和标准事件作为转换信号，以优化付费媒体广告。
* 利用[!DNL Analytics] Analysis Workspace更好地了解网站入口点和访问行为。
* 实现Web分析人员与付费媒体团队之间的更紧密协作。
* 在[!DNL Analytics]内使用永久性Adobe Advertising浏览和点进ID来了解网站参与情况。
* 使用在将数据或像素导出到广告服务器或其他DSP时无法实现的自定义量度、自定义维度和网站活动，在Analysis Workspace中增强传统的付费媒体报表。
* 利用您的网站上已有的[!DNL Analytics]代码在Adobe Advertising中进行跟踪和优化。

>[!TIP]
>
> 观看[视频介绍 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html?lang=zh-Hans#analytics)。

## 将Analytics用于付费媒体报表

insight [!DNL Analytics for Advertising]通过允许您：

* 在[!DNL Analytics]内使用永久性Adobe Advertising浏览和点进ID来了解网站参与情况。
* 利用Analysis Workspace更好地了解网站入口点和访问行为。 您可以访问付费媒体维度和事件数据，包括Adobe Advertising促销活动实体名称（具体到投放位置和广告）及其相关指标，如点击次数、展示次数和成本。

要使用[!DNL Analytics]作为您的付费媒体报告工具，您的组织需要具有Analysis Workspace访问权限的Experience Cloud登录。 您的Adobe Advertising团队将帮助您将Adobe Advertising数据映射到Analysis Workspace中的各个报表包。 您可以将Adobe Advertising数据发送到任何报表包，但您应该了解已映射到Adobe Advertising的报表包和未映射的报表包。根据报表包，这可能会更改报告的数据。

 [!DNL Analytics][&#128279;](ids.md)内的Adobe Advertising ID与其他[!DNL eVars]一样工作，具有自定义的永久过期时间。 默认情况下，在Adobe Advertising实施期间，归因回顾时间范围设置为60天。 要更改此设置，请与您的Adobe客户团队合作。

Adobe Advertising维度会附加后缀“(AMO ID)”(如“广告类型(AMO ID)”)。 有关可用维度的列表，请参阅“[Analysis Workspace中的Adobe Advertising指标](advertising-metrics-in-analytics.md)”。

>[!NOTE]
>
> 在[!DNL Analytics]中查看Adobe Advertising数据（或任何数据集）时，请注意，量度和报表基于[!DNL Analytics]中设置的规则。 数据可能不同于您在其他报表系统中看到的内容，例如广告服务器报表、[!DNL DSP]报表或搜索引擎报表。 要了解[!DNL Analytics]中的数据差异，您需要知道[!DNL eVar]数据何时过期、访问定义的内容、被视为最后接触归因与总持久归因的内容以及其他因素。 有关详细信息，请参阅[在 [!DNL Analytics] 和Adobe Advertising](data-variances.md)之间的预期数据差异。

## 使用Analytics为Adobe Advertising活动和项目组合提供支持

无需任何额外的像素，[!DNL Analytics for Advertising]可通过向Adobe Advertising发送两个主要信号，实现更好的优化和更简单的受众分段：

* 要用作竞价信号的转换量度：
   * 标准量度，如[!UICONTROL Revenue]和[!UICONTROL Cart Views]。
   * 网站参与量度，如页面查看和访问量度。
   * 自定义收入量度。
   * 保留的收入量度。
* 在[!DNL Analytics]中创建并发布到Experience Cloud的区段。

  您可以在[!DNL DSP]和付费搜索广告中使用[!DNL Analytics]区段进行第一方网站重定位。

  （仅限[!DNL Search, Social, & Commerce]）具有[!DNL Analytics]但不具有Audience Manager的广告商也可以从与Google共享的[!DNL Analytics]区段中创建Experience Cloud网站基于标签的受众（再营销列表）和客户匹配受众（客户列表）。

### 作为竞价信号的网站转化量度

您可以使用[!DNL Analytics]中的标准事件和自定义事件在Adobe Advertising中构建加权目标。 目标为您的[!DNL DSP]包和搜索、Social和Commerce项目组合的竞价决策提供信息。

对于搜索、社交和Commerce混合项目组合中的[!DNL Google Ads]和[!DNL Google Microsoft Advertising]营销活动，您可以选择直接将目标（包括目标中的任何[!DNL Analytics]事件）上传到广告网络，在广告网络中，这些目标可用作帐户级别和营销活动级别自定义转化目标的转化操作。

>[!NOTE]
>
> 您无法将计算指标从[!DNL Analytics]映射到Adobe Advertising。

您的Adobe Advertising团队将帮助您识别适用于付费媒体性能的事件，并将其映射到Adobe Advertising，这些事件在[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Admin] > [!UICONTROL Conversions]中列出。

有关可用量度的列表，请参阅“[Adobe Advertising中的Analytics量度](analytics-data-in-advertising.md)”。

### 用于网站重定向的Analytics区段

Adobe Advertising可以使用[!DNL Analytics]与Advertising DSP之间的本机Experience Cloud Audiences集成，为Experience Cloud和[!DNL Search, Social, & Commerce]广告摄取[!DNL Analytics]区段以进行再营销。

要访问[!DNL Analytics]区段，广告商帐户必须启用[Experience Cloud ID服务](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hans)。 启用ID服务后，所有Experience Cloud区段(包括在[!DNL Analytics]中创建并发布到Experience Cloud的区段、在Adobe Audience Manager中创建的区段、在Experience Cloud中使用[!DNL People core service]创建的区段，以及在Adobe Experience Platform中创建并通过Audience Manager发送到Adobe Advertising的区段)在处理完毕后即在Adobe Advertising中可用。

[!DNL Analytics]区段在24小时内可用，每天更新。

有关Experience Cloud受众服务的详细信息，请参阅[Experience Cloud受众](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=zh-Hans)。

## 如何使用集成的示例 {#integration-examples}

### 在Analysis Workspace中使用Adobe Advertising数据

要了解如何使用Adobe Advertising数据在Analysis Workspace中创建可视化报表，请参阅视频“[Workspace和报表简介](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html?lang=zh-Hans)”。

#### 在报表中使用连接的电视显示到达转换

*仅限Advertising DSP用户*

您可以通过将CTV设备上的广告曝光与网站转化关联，来衡量连接电视(CTV)促销活动的全面漏斗有效性。 新的[!UICONTROL Landing Type]筛选器“[!UICONTROL View-through (CTV)]”会将[!UICONTROL Click Through]、[!UICONTROL View Through]和[!UICONTROL View Through (CTV)]值的转换拆分为单独的行。

要查看您的CTV浏览转化量度，请使用Analysis Workspace中的“版面”视图或“营销渠道”视图。

使用“版面”视图：

1. 在报表视图中包括CTV支出投放位置。

1. 包括所需的量度，如“展示次数”、“点击次数”等。

1. 应用以下过滤器：

   广告平台： `Advertising Cloud DSP`

   登陆页面： `View-Through (CTV)`

使用“营销渠道”视图：

1. 包括维度`Marketing Channel`。

1. 包括所需的量度，如“展示次数”、“点击次数”等。

1. 应用以下过滤器：

   广告平台： `Advertising Cloud DSP`

   登陆页面： `View-Through (CTV)`

### 创建Adobe Advertising功能板

要了解如何根据Analysis Workspace中的目标跟踪Adobe Advertising数据，请参阅视频“使用Adobe Analytics创建Adobe Advertising功能板[&#128279;](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html?lang=zh-Hans)”。

### 将Adobe Advertising ID用于网站登入分析

要了解如何创建Adobe Advertising站点登入报表以监测每周时间、每天时间、浏览器和地理影响，请参阅视频[创建Adobe Advertising站点登入报表](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html?lang=zh-Hans)。

## 如何启动[!DNL Analytics for Advertising]实施

请联系您的Adobe客户团队，他们将会完成开始所需的初始配置，并将帮助您根据贵组织的需求规划实施和数据使用情况。

>[!MORELIKETHIS]
>
>* [视频： [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html?lang=zh-Hans)简介
>* [实施的先决条件和关键信息 [!DNL Analytics for Advertising]](prerequisites.md)
>* Analytics使用的[Adobe Advertising ID](ids.md)
>* 适用于Analytics for Advertising的[JavaScript代码](/help/integrations/analytics/javascript.md)
>* [在 [!DNL Analytics] 和Adobe Advertising](data-variances.md)之间的预期数据差异
>* Analysis Workspace中的[Adobe Advertising指标](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* Adobe Advertising中的[[!DNL Analytics] 数据](/help/integrations/analytics/analytics-data-in-advertising.md)
