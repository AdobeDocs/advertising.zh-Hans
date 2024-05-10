---
title: 在Adobe Target中为Adobe Advertising搜索、社交和Commerce广告配置A/B测试
description: 了解如何在中设置A/B测试 [!DNL Target] 您的 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 搜索、社交和Commerce中的广告。
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# 在Adobe Target中为Advertising Search、Social和Commerce广告配置A/B测试

*仅具有Advertising Search、Social和Commerce的广告商*

*[!DNL Google Ads]和 [!DNL Microsoft Advertising] 仅限帐户*

通过Adobe Advertising和Adobe Target，可以轻松为数字广告流量设置登陆页面体验A/B测试 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 至：

* 提高转化率(CVR)和获取效率措施（例如CPA、CPL和CAC）。

* 提供与广告相关的更个性化的登陆页面体验（例如，将图像/视频创意、文案、关键字或其他广告信号匹配到登陆页面）。

您还可以将本地的 [[!DNL Analytics] 适用于广告](/help/integrations/analytics/overview.md) 和 [[!DNL Analytics] 对象 [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) 集成报表维度，这些维度已集成到Adobe Analytics中以通过测量和可视化您的测试数据 [!DNL Analytics] 量度和成功事件。

请参阅以下部分，了解中的先决条件以及设置A/B测试的说明 [!DNL Target] 有关来自Search、Social和Commerce中广告的点进流量，以及有关如何在中测量和可视化测试的提示 [!DNL Analytics].

## 先决条件

### 所需产品

* 搜索、社交和Commerce
* [!DNL Target]

### 推荐的产品和集成

* [!DNL Analytics]

* [[!DNL Analytics] 适用于广告](/help/integrations/analytics/overview.md) 集成<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] 对象 [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) 集成

## 步骤1：在中创建A/B测试活动 [!DNL Target] 用于搜索、社交和Commerce

以下说明重点介绍与“搜索”、“社交”和“Commerce”用例相关的信息。

1. [登录到Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [创建A/B测试](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)：

   1. 在 **[!UICONTROL Enter Activity URL]** 字段中，输入测试的登陆页面URL。

   1. 在 **[!UICONTROL Goal]** 字段中，输入测试的成功量度。

      >[!NOTE]
      >
      >确保 [!DNL Analytics] 在中启用为数据源 [!DNL Target]，并选择正确的报表包。

   1. 设置 **[!UICONTROL Priority]** 到 `High` 或 `999` 以防止在测试区段中的用户收到错误的现场体验时发生冲突。


   1. 范围 **[!UICONTROL Reporting Settings]**，选择 **[!UICONTROL Company Name]** 和 **[!UICONTROL Report Suite]** 已连接到您的搜索、社交和Commerce帐户。

      有关其他报表提示，请参阅&quot;[报表最佳实践和疑难解答](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html)“

   1. 在 **[!UICONTROL Date Range]** 字段中，输入测试的相应起始日期和终止日期。

   1. 选择 **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. 在 **[!UICONTROL Value]** 字段中，输入 [!UICONTROL Network Account ID]， [!UICONTROL Network Campaign ID]， [!UICONTROL Network Adgroup ID]，或 [!UICONTROL Network Ad ID] 搜索、社交和Commerce中的相关广告网络实体。 这允许您使用 [!DNL Target] 实体的点进受众的查询字符串参数。

      ID查找方式 [将相关ID列添加到实体视图](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] 中的列 [!UICONTROL Accounts] 视图](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] 中的列 [!UICONTROL Accounts] 视图")

      如果您需要帮助，请与您的Adobe客户团队合作。

   1. 对于 **[!UICONTROL Traffic Allocation Method]**，选择 **[!UICONTROL Manual (Default)]** 然后把观众分成五成半。

   1. 保存活动。

1. 使用 [Target可视化体验编辑器](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) 对A/B测试登陆页面模板进行设计更改。

   * 体验A：请勿编辑，因为这是无个性化的默认/控制登陆页面体验。

   * 体验B：使用 [!DNL Target] 用于根据测试中包含的资产自定义登陆页面模板的用户界面（例如标题、文案、按钮放置和创意）。

   >[!NOTE]
   >
   >例如，创意测试用例，请与您的Adobe客户团队联系。

## 第2步：设置您的 [!DNL Analytics for Target] Analysis Workspace位于 [!DNL Analytics]

[!DNL Analytics for Target] (A4T)是一种跨解决方案的集成，它允许广告商创建 [!DNL Target] 活动基于 [!DNL Analytics] 转化指标和受众区段，然后使用衡量结果 [!DNL Analytics] 作为报表源。 该活动的所有报表和区段均基于 [!DNL Analytics] 数据收集。

有关详情 [!DNL Analytics for Target]，包括实施说明的链接，请参阅&quot;[将Adobe Analytics作为Adobe Target报表源(A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)“。

### 设置 [!DNL Analytics for Target] 面板

在Analysis Workspace中，配置 [!DNL Analytics for Target panel] 分析 [!DNL Target] 活动和体验。 请牢记以下有关您的报告的重要指针和信息。

#### 量度

* 在工作区中创建特定于Adobe Advertising帐户、营销活动或广告组的面板<!-- only applicable entities? --> 运行测试的对象。 使用摘要可视化图表显示同一报表中的Adobe Advertising指标。 [!DNL Target] 测试性能。

* 优先使用现场量度（例如访问和转化）来衡量绩效。

* 了解来自Adobe Advertising的汇总媒体量度（例如展示次数、点击量和成本）无法与 [!DNL Target] 量度。

#### Dimension

以下维度与 [!DNL Analytics for Target]：

* **Target活动**：A/B测试的名称

* **Target体验**：活动中使用的登陆页面体验的名称

* **Target活动** > **体验**：同一行中的活动名称和体验名称

### Analytics疑难解答 [!DNL Target] 数据

在Analysis Workspace中，如果您发现活动和体验数据很少或未填充数据，请执行以下操作：

* 验证是否相同 [!UICONTROL Supplemental Data ID] (SDID)同时用于 [!DNL Target] 和 [!DNL Analytics]. 您可以使用验证SDID值 [Adobe Experience Cloud调试器](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) 在营销活动将用户引导到的登陆页面上。

[Adobe Debugger中的补充数据ID (SDID)值](/help/integrations/assets/target-troubleshooting-sdid.png)

* 在同一登陆页面上，验证a) [!UICONTROL Hostname] 在Adobe Debugger中显示在 [!UICONTROL Solutions] > [!UICONTROL Target] 匹配b) [!UICONTROL Tracking Server] 显示位置 [!DNL Target] 对于活动(在 [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings])。

  [!DNL Analytics For Target] 需要 [!DNL Analytics] 要以调用形式发送的跟踪服务器 [!DNL Target] 到 [!DNL Modstats] Analytics的数据收集服务器。<!-- just "to Analytics?"-->

[Adobe Debugger中的主机名值](/help/integrations/assets/target-troubleshooting-hostname.png)

[Target中的跟踪服务器值](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 进一步阅读

* [将Target与Analytics集成](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html)  — 说明如何设置 [!DNL Target] Analysis Workspace中的报表。
* [A/B测试概述](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html)  — 介绍可与Search、Social和Commerce广告一起使用的A/B测试活动。
* [Analytics for Advertising概述](/help/integrations/analytics/overview.md)  — 引入了Analytics for Advertising，它允许您跟踪Analytics实例中的点进和浏览网站交互。

>[!MORELIKETHIS]
>
>* [在Adobe Target中为Advertising DSP广告配置A/B测试](ab-tests-dsp.md)
