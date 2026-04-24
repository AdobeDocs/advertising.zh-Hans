---
title: Configure A/B tests for Adobe Advertising Search, Social, & Commerce ads in Adobe Target
description: Learn how to set up an A/B test in [!DNL Target] for your [!DNL Google Ads] and [!DNL Microsoft Advertising] ads in Search, Social, & Commerce.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
TQID: https://experienceleague.adobe.com/eu1dRdsQlJX4IlHLTUDyJ69r0txFvFUdzUiXpSAlpU8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 958
ht-degree: 0%

---

# Configure A/B tests in Adobe Target for Advertising Search, Social, &amp; Commerce ads

*Advertisers with Advertising Search, Social, &amp; Commerce only*

*[!DNL Google Ads]and [!DNL Microsoft Advertising] accounts only*

Adobe Advertising and Adobe Target make it easy to set up landing page experience A/B tests for digital advertising traffic [!DNL Google Ads] and [!DNL Microsoft Advertising] to:

* Improve conversion rates (CVR) and acquisition efficiency measures (such as CPA, CPL, and CAC).

* Deliver a more personalized landing page experience that&#39;s relevant to the ad (for example, matching the image/video creative, copy, keyword, or other advertising signal to the landing page).

You can also combine the native [[!DNL Analytics] for Advertising](/help/integrations/analytics/overview.md) and [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integration reporting dimensions that are integrated into Adobe Analytics to measure and visualize your test data with [!DNL Analytics] metrics and success events.

See the following sections for the prerequisites, instructions to set up A/B tests in [!DNL Target] for click-through traffic from ads in Search, Social, &amp; Commerce, and tips on how to measure and visualize your tests in [!DNL Analytics].

## 先决条件

### Required products

* Search, Social, &amp; Commerce
* [!DNL Target]

### Recommended products and integrations

* [!DNL Analytics]

* 用于Advertising的[[!DNL Analytics] 集成](/help/integrations/analytics/overview.md)<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)集成

## 步骤1：在[!DNL Target]中为搜索、社交和Commerce创建A/B测试活动

以下说明重点介绍与“搜索”、“社交”和“Commerce”用例相关的信息。

1. [登录到Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html)。

1. [创建A/B测试](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)：

   1. 在&#x200B;**[!UICONTROL Enter Activity URL]**&#x200B;字段中，输入测试的登陆页面URL。

   1. 在&#x200B;**[!UICONTROL Goal]**&#x200B;字段中，输入测试的成功量度。

      >[!NOTE]
      >
      >确保在[!DNL Target]中将[!DNL Analytics]启用为数据源，并选择正确的报表包。

   1. 将&#x200B;**[!UICONTROL Priority]**&#x200B;设置为`High`或`999`可防止在测试区段中的用户收到错误的现场体验时发生冲突。


   1. 在&#x200B;**[!UICONTROL Reporting Settings]**&#x200B;内，选择连接到您的Search、Social和Commerce帐户的&#x200B;**[!UICONTROL Company Name]**&#x200B;和&#x200B;**[!UICONTROL Report Suite]**。

      有关其他报告提示，请参阅“[报告最佳实践和疑难解答](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html)”。

   1. 在&#x200B;**[!UICONTROL Date Range]**&#x200B;字段中，为测试输入适当的开始日期和结束日期。

   1. 选择&#x200B;**[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**。 在&#x200B;**[!UICONTROL Value]**&#x200B;字段中，为搜索、社交和Commerce中的相关广告网络实体输入[!UICONTROL Network Account ID]、[!UICONTROL Network Campaign ID]、[!UICONTROL Network Adgroup ID]或[!UICONTROL Network Ad ID]。 这允许您为实体的点进受众使用[!DNL Target]查询字符串参数。

      您可以通过[将相关ID列添加到实体视图](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)来查找该ID。

      [!UICONTROL Accounts]视图")的[!UICONTROL Accounts]视图&rbrack;(/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID]列中的!&lbrack;[!UICONTROL Network Account ID]列

      如果您需要帮助，请与您的Adobe客户团队合作。

   1. 对于&#x200B;**[!UICONTROL Traffic Allocation Method]**，选择&#x200B;**[!UICONTROL Manual (Default)]**&#x200B;并按50/50拆分受众。

   1. 保存活动。

1. 使用[Target可视化体验编辑器](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)对A/B测试登陆页面模板进行设计更改。

   * 体验A：请勿编辑，因为这是无个性化的默认/控制登陆页面体验。

   * 体验B：使用[!DNL Target]用户界面根据测试中包含的资产（如标题、文案、按钮放置和创意）自定义登陆页面模板。

   >[!NOTE]
   >
   >例如，创意测试用例，请联系您的Adobe客户团队。

## 步骤2：在[!DNL Analytics]中设置您的[!DNL Analytics for Target] Analysis Workspace

[!DNL Analytics for Target] (A4T)是一种跨解决方案的集成，它允许广告商根据[!DNL Analytics]转化指标和受众区段创建[!DNL Target]活动，然后使用[!DNL Analytics]作为报表源度量结果。 该活动的所有报表和区段都基于[!DNL Analytics]数据收集。

有关[!DNL Analytics for Target]的详细信息（包括指向实施说明的链接），请参阅“[Adobe Analytics作为Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)的报表源”。

### 设置[!DNL Analytics for Target]面板

在Analysis Workspace中，配置[!DNL Analytics for Target panel]以分析您的[!DNL Target]活动和体验。 请牢记以下有关您的报告的重要指针和信息。

#### 量度

* 在工作区中创建特定于运行测试的Adobe Advertising帐户、营销活动或广告组<!-- only applicable entities? -->的面板。 使用摘要可视化图表在与[!DNL Target]测试性能相同的报表中显示Adobe Advertising量度。

* 优先使用现场量度（例如访问和转化）来衡量绩效。

* 了解Adobe Advertising中的汇总媒体量度（例如展示次数、点击量和成本）无法与[!DNL Target]量度匹配。

#### 维度

以下维度与[!DNL Analytics for Target]相关：

* **目标活动**： A/B测试的名称

* **Target体验**：活动中使用的登陆页面体验的名称

* **Target活动** > **体验**：同一行中的活动名称和体验名称

### 针对[!DNL Target]数据的分析疑难解答

在Analysis Workspace中，如果您发现活动和体验数据很少或未填充数据，请执行以下操作：

* 验证是否对[!DNL Target]和[!DNL Analytics]使用了相同的[!UICONTROL Supplemental Data ID] (SDID)。 您可以使用促销活动将用户引导至的登陆页面上的[Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html)来验证SDID值。

  [Adobe Debugger中的补充数据ID (SDID)值](/help/integrations/assets/target-troubleshooting-sdid.png)

* 在同一登录页上，验证a) Adobe Debugger中[!UICONTROL Solutions] > [!UICONTROL Target]下显示的[!UICONTROL Hostname]与b) [!DNL Target]中显示的[!UICONTROL Tracking Server]匹配（在[!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]下）。

  [!DNL Analytics For Target]要求在Analytics的[!DNL Target]到[!DNL Modstats]数据收集服务器的调用中发送[!DNL Analytics]跟踪服务器。<!-- just "to Analytics?"-->

  [Adobe Debugger中的主机名值](/help/integrations/assets/target-troubleshooting-hostname.png)

  [Target中的跟踪服务器值](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 进一步阅读

* [将Target与Analytics集成](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) — 说明如何在Analysis Workspace中设置[!DNL Target]报表。
* [A/B测试概述](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) — 介绍可与Search、Social和Commerce广告一起使用的A/B测试活动。
* [概述 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) — 介绍[!DNL Analytics for Advertising]，它允许您跟踪Analytics实例中的点进和浏览网站交互。

>[!MORELIKETHIS]
>
>* [在Adobe Target中为Advertising DSP广告配置A/B测试](ab-tests-dsp.md)
