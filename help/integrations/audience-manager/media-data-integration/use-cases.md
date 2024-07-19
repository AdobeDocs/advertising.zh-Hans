---
title: 用例
description: 了解与Audience Manager共享Advertising DSP媒体数据的用例
feature: Integration with Adobe Audience Manager
exl-id: 1d961799-b8be-499a-8db6-b59762d96bf1
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# 在Adobe Audience Manager中捕获媒体曝光数据的用例

*仅使用Advertising DSP的广告商*

*仅具有Adobe Advertising-Adobe Audience Manager集成的广告商*

以下是一些让您能够从在Audience Manager中捕获Advertising DSP媒体曝光数据<!-- ad impression data? -->中受益的方法。

## 回访间隔和频率管理

通过在Audience Manager中捕获展示数据，可创建已展示特定广告或营销策划的用户区段，从而增强频度管理。 如果要提高频率，可以将这些区段用于广告定位；如果要限制频率，则可以将这些区段用于广告抑制。

此外，通过Audience Manager[!DNL Segment Builder]，您可以将[回访间隔和频率控件](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html)应用于包含可操作信号的任何[基于规则的特征](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html)。 例如，这可让您限制在媒体促销活动中向某个用户展示特定创意内容的次数。 阅读“[即时跨设备抑制](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)”以了解如何执行此操作。<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## 顺序消息传递

通过捕获展示数据，您可以创建已展示给促销活动或广告的用户区段，并将此区段用于顺序消息传送或抑制。 例如，您可以通过显示创意内容`456`，重新定位看到创意内容`123`但未单击或转换的用户。

若要在Audience Manager中执行此示例，请按照以下步骤操作：<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. 创建一个特征来捕获看到创意内容的用户。

   例如，要命名特征`Creative Trait 123`，请使用以下特征规则：

   ```
   d_creative == 123 AND d_event == imp
   ```

1. 创建一个特征以捕获单击或转换的用户。

   例如，要命名此特征`Click and Converter`，请使用以下特征规则：

   ```
   d_event == click OR d_event=conv
   ```

1. 创建名为`Retarget Users`的区段以填充看到创意`123`但未单击或转换的用户。 使用以下特征规则：

   ```
   Creative Trait 123 AND NOT Click and Converter
   ```

1. 将区段`Retarget Users`映射到目标，并使用创意`456`定位目标中的用户。

## [!DNL Adobe Audience Analytics]和营销活动曝光数据

一旦营销活动的展示和点击数据在Audience Manager中可用，您即可创建接触或交互特定营销活动或策略的用户的特征和区段。 通过[[!DNL Audience Analytics] 集成](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)，您的Audience Manager区段可以与[!DNL Analytics]同步以供进一步分析。 潜在用例包括：

* **DSP与[!DNL Advertising Search, Social, & Commerce]广告之间的交互分析：**&#x200B;标准[[!DNL Analytics for Advertising] 集成](/help/integrations/analytics/overview.md)不提供有关DSP与[!DNL Search, Social, & Commerce]之间的交互的分析，因为两个渠道使用的AMO ID都遵循AMO ID归因规则，搜索点击会覆盖该规则的显示显示显示显示显示显示到达。 通过在Audience Manager中创建DSP曝光区段，您可以使用[!DNL Audience Analytics]来分析[!DNL Analytics]中DSP和[!DNL Search, Social, & Commerce]广告之间的交互。

* **频度分析：**&#x200B;您可以根据用户接触到特定广告或营销活动的次数，在Audience Manager中创建区段。 然后，您可以分析Analytics中的不同风险区段，以了解用户行为如何根据DSP风险数量的变化而变化。

## [!DNL Audience Optimization Reports]

您可以利用[Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html)来识别营销活动中区段的潜在效果机会。 这些报表将促销活动展示次数、点击次数和转化数据与区段量度相结合，以提供以区段为中心的优化和有效渠道组合信息。

### 相关Audience Optimization报告的类型

| 报表 | 描述 |
| ------ | ----------- |
| [[!UICONTROL Segment Performance]报告](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | 按展示次数和转化率比较已映射和未映射的区段。 |
| [[!UICONTROL Trend Analysis and Volume Analysis]报告]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | 返回各种广告维度的展示次数、点进率和转化率数据。 |
| [[!UICONTROL Optimal Frequency]报告](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | 帮助您在提供的展示次数和转化次数之间实现最佳平衡。 它允许您先调整要显示的展示次数，然后再开始看到递减的退货。 |
| [[!UICONTROL Unique User Reach]报告](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | 气泡图，其中每个气泡的大小与所选维度的独特用户数成正比。 |

### 注意事项

* 如果[!DNL Audience Optimization Reports]用户具有基于角色的访问控制(RBAC)，则[!DNL Adobe Customer Care]必须配置广告商ID与组织的Audience Manager数据源集成代码之间的映射。 然后，管理员用户可以向不同用户提供基于RBAC的权限。

* [!DNL Audience Optimization Reports]中的转换报表需要最终用户进行一些设置。 用户必须填充元数据文件。

* [!DNL Audience Optimization Reports]不支持更改营销活动元数据（如营销活动名称或投放位置名称）。

* 仅当搜索广告的点击次数与展示次数相关联时，[!DNL Audience Optimization Reports]中才会包含这些点击次数。 换言之，搜索点击被视为展示后的转化。 因此，许多搜索点击可能未包含在[!DNL Audience Optimization Reports]中。

>[!MORELIKETHIS]
>
>* [将DSP媒体曝光数据发送到Adobe Audience Manager的概述](overview.md)
>* [从Advertising DSP营销活动中收集点击和展示数据](collect.md)
