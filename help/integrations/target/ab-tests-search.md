---
title: 在Adobe Target中为Adobe Advertising搜索、社交和Commerce广告配置A/B测试
description: 了解如何在 [!DNL Target] 中为搜索、社交和Commerce中的 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 广告设置A/B测试。
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# 在Adobe Target中为Advertising搜索、社交和Commerce广告配置A/B测试

*仅使用Advertising Search、Social和Commerce的广告商*

仅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户*

通过Adobe Advertising和Adobe Target，可以轻松为数字广告流量[!DNL Google Ads]和[!DNL Microsoft Advertising]设置登陆页面体验A/B测试，以便：

* 提高转化率(CVR)和获取效率措施（例如CPA、CPL和CAC）。

* 提供与广告相关的更个性化的登陆页面体验（例如，将图像/视频创意、文案、关键字或其他广告信号匹配到登陆页面）。

您还可以合并已集成到Adobe Analytics中的Advertising[&#128279;](/help/integrations/analytics/overview.md)的本机[[!DNL Analytics] 和 [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=zh-Hans)的[!DNL Analytics] 集成报表维度，以便通过[!DNL Analytics]指标和成功事件测量和可视化您的测试数据。

请参阅以下部分以了解先决条件、在[!DNL Target]中为来自Search、Social和Commerce中的广告的点进流量设置A/B测试的说明，以及有关如何在[!DNL Analytics]中测量和可视化测试的提示。

## 先决条件

### 所需产品

* 搜索、社交和Commerce
* [!DNL Target]

### 推荐的产品和集成

* [!DNL Analytics]

* 用于Advertising的[[!DNL Analytics] 集成](/help/integrations/analytics/overview.md)<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=zh-Hans)集成

## 步骤1：在[!DNL Target]中为搜索、Social和Commerce创建A/B测试活动

以下说明重点介绍与“搜索”、“社交”和“Commerce”用例相关的信息。

1. [登录到Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html?lang=zh-Hans)。

1. [创建A/B测试](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=zh-Hans)：

   1. 在&#x200B;**[!UICONTROL Enter Activity URL]**&#x200B;字段中，输入测试的登陆页面URL。

   1. 在&#x200B;**[!UICONTROL Goal]**&#x200B;字段中，输入测试的成功量度。

      >[!NOTE]
      >
      >确保在[!DNL Target]中将[!DNL Analytics]启用为数据源，并选择正确的报表包。

   1. 将&#x200B;**[!UICONTROL Priority]**&#x200B;设置为`High`或`999`可防止在测试区段中的用户收到错误的现场体验时发生冲突。


   1. 在&#x200B;**[!UICONTROL Reporting Settings]**&#x200B;内，选择连接到您的Search、Social和Commerce帐户的&#x200B;**[!UICONTROL Company Name]**&#x200B;和&#x200B;**[!UICONTROL Report Suite]**。

      有关其他报告提示，请参阅“[报告最佳实践和疑难解答](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html?lang=zh-Hans)”。

   1. 在&#x200B;**[!UICONTROL Date Range]**&#x200B;字段中，为测试输入适当的开始日期和结束日期。

   1. 选择&#x200B;**[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**。 在&#x200B;**[!UICONTROL Value]**&#x200B;字段中，为搜索、社交和Commerce中的相关广告网络实体输入[!UICONTROL Network Account ID]、[!UICONTROL Network Campaign ID]、[!UICONTROL Network Adgroup ID]或[!UICONTROL Network Ad ID]。 这允许您为实体的点进受众使用[!DNL Target]查询字符串参数。

      您可以通过[将相关ID列添加到实体视图](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)来查找该ID。

      [!UICONTROL Accounts]视图")的[!UICONTROL Accounts]视图&rbrack;(/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID]列中的!&lbrack;[!UICONTROL Network Account ID]列

      如果您需要帮助，请与您的Adobe客户团队合作。

   1. 对于&#x200B;**[!UICONTROL Traffic Allocation Method]**，选择&#x200B;**[!UICONTROL Manual (Default)]**&#x200B;并按50/50拆分受众。

   1. 保存活动。

1. 使用[Target可视化体验编辑器](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=zh-Hans)对A/B测试登陆页面模板进行设计更改。

   * 体验A：请勿编辑，因为这是无个性化的默认/控制登陆页面体验。

   * 体验B：使用[!DNL Target]用户界面根据测试中包含的资产（如标题、文案、按钮放置和创意）自定义登陆页面模板。

   >[!NOTE]
   >
   >例如，创意测试用例，请联系您的Adobe客户团队。

## 步骤2：在[!DNL Analytics]中设置您的[!DNL Analytics for Target] Analysis Workspace

[!DNL Analytics for Target] (A4T)是一种跨解决方案的集成，它允许广告商根据[!DNL Analytics]转化指标和受众区段创建[!DNL Target]活动，然后使用[!DNL Analytics]作为报表源度量结果。 该活动的所有报表和区段都基于[!DNL Analytics]数据收集。

有关[!DNL Analytics for Target]的详细信息（包括指向实施说明的链接），请参阅“[Adobe Analytics作为Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=zh-Hans)的报表源”。

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

* 验证是否对[!DNL Target]和[!DNL Analytics]使用了相同的[!UICONTROL Supplemental Data ID] (SDID)。 您可以在促销活动将用户引导至的登陆页面上使用[Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html?lang=zh-Hans)来验证SDID值。

[Adobe Debugger中的补充数据ID (SDID)值](/help/integrations/assets/target-troubleshooting-sdid.png)

* 在同一登录页上，验证a) Adobe Debugger中[!UICONTROL Solutions] > [!UICONTROL Target]下显示的[!UICONTROL Hostname]与b) [!DNL Target]中显示的[!UICONTROL Tracking Server]匹配（在[!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]下）。

  [!DNL Analytics For Target]要求在Analytics的[!DNL Target]到[!DNL Modstats]数据收集服务器的调用中发送[!DNL Analytics]跟踪服务器。<!-- just "to Analytics?"-->

[Adobe Debugger中的主机名值](/help/integrations/assets/target-troubleshooting-hostname.png)

[Target中的跟踪服务器值](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 进一步阅读

* [将Target与Analytics集成](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html?lang=zh-Hans) — 说明如何在Analysis Workspace中设置[!DNL Target]报表。
* [A/B测试概述](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html?lang=zh-Hans) — 介绍可与Search、Social和Commerce广告一起使用的A/B测试活动。
* [Analytics for Advertising概述](/help/integrations/analytics/overview.md) — 介绍Analytics for Advertising，它允许您跟踪Analytics实例中的点进和浏览网站交互。

>[!MORELIKETHIS]
>
>* [在Adobe Target中为Advertising DSP Ads配置A/B测试](ab-tests-dsp.md)
