---
title: 概述 [!DNL Analytics for Advertising]
description: 概述 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 0%

---

# 概述 [!DNL Analytics for Advertising]

*使用Advertising DSP和的广告商[!DNL Advertising Search]*

[!DNL Analytics for Advertising] 集成了Adobe Analytics和Adobe广告，以扩展和增强每个产品的功能。

通过集成，广告商可以跟踪其网站中的点进和浏览网站交互 [!DNL Analytics] 实例数，允许品牌了解其广告支出如何导致网站参与度和关键业务目标。

此外，Adobe广告可以访问庞大的第一方数据，这些数据 [!DNL Analytics] 收集方式 [!DNL Analytics] 标记已存在于站点上。 这允许进行更强大的历程管理、第一方再营销和付费媒体网站报告。 Adobe广告可以进一步使用 [!DNL Analytics] 支出和竞价优化数据。

如果工作得当， [!DNL Analytics for Advertising] 模糊了两个传统角色之间的界限：广告历程管理（通过广告将用户发送到站点的行为）和通过Web分析了解站点参与度。

主要优点：

* 发送 [!DNL Analytics] 区段直接Adobe广告以进行第一方网站再营销。
* 使用 [!DNL Analytics] 自定义和标准事件作为转化信号，用于优化付费媒体广告。
* 充分利用 [!DNL Analytics] Analysis Workspace ，以更好地了解站点入口点和访问行为。
* 实现Web分析人员与付费媒体团队之间更紧密的协作。
* 在中使用永久性Adobe广告浏览进入和点进ID [!DNL Analytics] 以了解站点参与情况。
* 将数据或像素导出到广告服务器或其他DSP时，无法通过自定义量度、自定义维度和网站活动在Analysis Workspace中增强传统的付费媒体报表。
* 充分利用 [!DNL Analytics] 网站上已存在的用于Adobe广告跟踪和优化的代码。

>[!TIP]
>
> 观看 [视频简介 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## 将Analytics用于付费媒体报表

[!DNL Analytics for Advertising] 通过允许您：

* 在中使用永久性Adobe广告浏览进入和点进ID [!DNL Analytics] 以了解站点参与情况。
* 利用Analysis Workspace更好地了解网站入口点和访问行为。 您可以访问付费媒体维度和事件数据，包括Adobe广告促销活动实体名称（具体到投放位置和广告）及其相关指标，如点击次数、展示次数和成本。

使用 [!DNL Analytics] 作为付费媒体报表工具，贵组织需要拥有Analysis Workspace访问权限的Experience Cloud登录。 您的Adobe广告团队将帮助您将Adobe广告数据映射到Analysis Workspace中的各个报表包。 您可以将Adobe广告数据发送到任何报表包，但您应该了解已映射到Adobe广告的报表包和未映射的报表包。根据报表包，这可能会更改报告的数据。

[Adobe广告ID [!DNL Analytics]](ids.md) 其工作方式与其他eVar类似，具有自定义的永久性过期时间。 默认情况下，归因回顾时间范围在Adobe广告实施期间设置为60天。 要更改此设置，请与您的Adobe帐户团队合作。

Adobe广告维度会附加后缀“(AMO ID)”(例如“广告类型(AMO ID)”)。 参见“[Analysis Workspace中的Adobe广告量度](advertising-metrics-in-analytics.md)”以获取可用维度的列表。

>[!NOTE]
>
> 当您在中查看Adobe广告数据（或任何数据集）时 [!DNL Analytics]，请注意，量度和报表基于在中设置的规则 [!DNL Analytics]. 数据可能不同于您在其他报表系统中看到的内容，例如广告服务器报表， [!DNL DSP] 报表或搜索引擎报表。 要了解数据差异，请执行以下操作： [!DNL Analytics]，您需要了解eVar数据何时过期、什么定义访问、什么被视为最后接触归因与总持久归因，以及其他因素。 有关更多信息，请参阅 [之间的预期数据差异 [!DNL Analytics] 和Adobe广告](data-variances.md).

## 使用Analytics为Adobe广告促销活动和Portfolio提供支持

不需要任何额外的像素， [!DNL Analytics for Advertising] 通过向Adobe广告发送两个主要信号，可实现更好的优化和更简单的受众分段：

* 要用作竞价信号的转化量度：
   * 标准量度，例如 [!UICONTROL Revenue] 和 [!UICONTROL Cart Views].
   * 网站参与量度，例如页面查看和访问量度。
   * 自定义收入量度。
   * 保留的收入量度。
* 在中创建的区段 [!DNL Analytics] 并发布到Experience Cloud。

   您可以使用 [!DNL Analytics] 中用于第一方网站重定位的区段 [!DNL DSP] 以及付费搜索广告。

   ([!DNL Search] 仅限)广告商使用 [!DNL Analytics] 但是Audience Manager无法从以下位置创建基于Google网站标签的受众（再营销列表）和客户匹配受众（客户列表） [!DNL Analytics] 与Experience Cloud共享的区段。

### 网站转化量度作为竞价信号

您可以从以下位置使用标准事件和自定义事件： [!DNL Analytics] 在Adobe广告中构建加权目标。 目标为您的投标决策提供信息 [!DNL DSP] 包和搜索项目组合。

>[!NOTE]
>
> 您无法从以下位置映射计算指标 [!DNL Analytics] Adobe广告。

您的Adobe广告团队将帮助您识别适用于付费媒体表现的事件，并将其映射到Adobe广告中，这些事件将显示在 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

参见“[Adobe广告中的Analytics量度](analytics-data-in-advertising.md)”以获取可用量度列表。

### 用于网站重定向的Analytics区段

Adobe广告可以摄取 [!DNL Analytics] 用于Advertising DSP和再营销的区段 [!DNL Search] 使用本机Experience Cloud受众集成的广告，介于 [!DNL Analytics] 和Experience Cloud。

要访问 [!DNL Analytics] 区段，广告商帐户需要具有 [Experience CloudID服务](https://experienceleague.adobe.com/docs/id-service/using/home.html) 已启用。 启用ID服务后，所有Experience Cloud区段(包括在 [!DNL Analytics] 并发布到Experience Cloud、在Adobe Audience Manager中创建的区段，以及使用在Experience Cloud中创建的区段 [!DNL People core service]、以及在Adobe Experience Platform中创建并通过Audience Manager发送到Adobe广告的区段)一经处理，即可在Adobe广告中使用。

[!DNL Analytics] 区段可在24小时内提供，并每天更新。

有关Experience Cloud受众服务的更多信息，请参阅 [Experience Cloud受众](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## 如何使用集成的示例

### 在Analysis Workspace中使用Adobe广告数据

要了解如何在Analysis Workspace中使用Adobe广告数据创建可视化报表，请观看视频»[Workspace和报表简介](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).”

### 创建Adobe广告功能板

要了解如何根据Analysis Workspace中的目标跟踪Adobe广告数据，请观看视频»[使用Adobe Analytics创建Adobe广告功能板](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html).”

### 将Adobe广告ID用于网站登入分析

要了解如何创建Adobe广告网站登入报表以监测每周的某天、每天的某个时间、浏览器和地理影响，请观看视频”[创建Adobe广告网站登入报表](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html).”

>[!MORELIKETHIS]
>
>* [视频：简介 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [实施的先决条件和关键信息 [!DNL Analytics for Advertising]](prerequisites.md)
>* [Analytics使用的Adobe广告ID](ids.md)
>* [适用于Analytics for Advertising的JavaScript代码](/help/integrations/analytics/javascript.md)
>* [之间的预期数据差异 [!DNL Analytics] 和Adobe广告](data-variances.md)
>* [Analysis Workspace中的Adobe广告量度](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe广告中的数据](/help/integrations/analytics/analytics-data-in-advertising.md)

