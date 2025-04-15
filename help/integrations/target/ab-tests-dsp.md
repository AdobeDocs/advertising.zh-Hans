---
title: 在Adobe Target中为Adobe Advertising DSP广告配置A/B测试
description: 了解如何在 [!DNL Target] 中为您的DSP广告设置A/B测试。
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: a69bef9d249514f5c494cff8d706b9df792eaf23
workflow-type: tm+mt
source-wordcount: '1413'
ht-degree: 0%

---

# 在Adobe Target中为Advertising DSP广告配置A/B测试

*仅使用Advertising DSP的广告商*

Adobe Advertising和Adobe Target使得营销人员能够更轻松地通过付费媒体和现场消息传递提供个性化的互联体验。 通过在产品之间共享信号，您可以：

* 通过将DSP促销活动中的客户广告曝光度与其网站上的体验关联，降低网站流失率。

* 通过使用Adobe Audience Manager曝光数据和点击馈送[!DNL Target]受众镜像广告消息传递的现场体验，从而建立A/B测试。

* 在Adobe Analytics中为[!DNL Target]使用简单的可视化图表，衡量统一消息对网站目标提升的影响。

请参阅以下部分以了解先决条件以及设置点进和浏览跟踪的说明，在DSP和[!DNL Target]之间实施信号共享，设置A/B测试活动，以及设置[!DNL Analytics] Analysis Workspace以查看测试数据。

如果您还有其他问题，请联系adcloud_support@adobe.com。

## 先决条件

此用例需要以下产品和集成：

* [!DNL Target]

* 用于Advertising的[[!DNL Analytics] 集成](/help/integrations/analytics/overview.md)<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)集成

* Audience Manager（仅对于浏览测试是必需的）

## 步骤1：设置点进框架 {#click-through-framework}

![点进框架](/help/integrations/assets/target-ct-framework.png)

将DSP宏添加到点进URL（用户点击广告并到达登陆页面时显示的URL）时，DSP通过在点进URL中包含`${TM_PLACEMENT_ID}`来自动捕获投放位置键。 此宏捕获字母数字版面密钥，而不是数字版面ID。

![点进URL已附加到登陆页面URL](/help/integrations/assets/target-ct-url.jpg)

### (仅限DSP)将DSP宏添加到您的点进URL

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

在[!DNL Flashtalking]或Google Campaign Manager 360中，手动更新每个广告的点进URL，以包含捕获AMO ID变量所需的宏。 AMO ID变量用于将点击数据发送到Adobe Analytics并共享A/B测试的放置键。 有关说明，请参阅以下页面：

* [将 [!DNL Analytics for Advertising] 宏附加到 [!DNL Flashtalking] 添加标记](/help/integrations/analytics/macros-flashtalking.md)。 **注意：**&#x200B;如果您的组织与[!DNL Flashtalking]直接合作，并且您根据[!DNL Flashtalking]支持文档(位于[https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros))使用数据传递宏跟踪`s_kwcid`和`ef_id`跟踪参数，则不需要执行此过程。

* [将 [!DNL Analytics for Advertising] 宏附加到 [!DNL Google Campaign Manager 360] 添加标记](/help/integrations/analytics/macros-google-campaign-manager.md)

请联系您的Adobe客户团队和Advertising解决方案小组(aac-advertising-solutions-group@adobe.com)，以检索所需的放置键并完成设置，并确保每个点进URL都填充了放置键。

## 步骤2：使用Audience Manager设置浏览框架 {#view-through-framework}

![浏览框架](/help/integrations/assets/targetr-vt-framework.png)

通过在广告标记和投放设置中添加Audience Manager展示事件像素，您可以为其他显示到达测试机会创建测试区段。

1. 在广告标记和DSP投放设置中实施Audience Manager展示事件像素。

   有关说明，请参阅“[从Advertising DSP营销活动中收集媒体曝光数据](/help/integrations/audience-manager/media-data-integration/collect.md)”。

   确保添加[DSP宏](/help/dsp/campaign-management/macros.md)以捕获希望展示事件像素传回的所有数据，包括数字版面ID的`${TM_PLACEMENT_ID_NUM}`。

   >[!NOTE]
   >
   >点击跟踪URL包含字母数字放置键的`${TM_PLACEMENT_ID}`宏，而不是数字放置ID的`${TM_PLACEMENT_ID_NUM}`。

1. 从DSP展示数据配置Audience Manager区段：

   1. 验证区段数据是否可用：

      1. [搜索[键值对](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html)的信号](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html)，以确定在哪个级别对区段用户进行分组。

         使用一个[支持的键](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html)，该键的值对应于您添加到Audience Manager展示事件像素中的宏。

         例如，若要针对特定位置对用户进行分组，请使用`d_placement`键。 对于该值，使用DSP宏`${TM_PLACEMENT_ID_NUM}`捕获的实际数字放置ID(如2501853)。<!-- Explain where to find the placement ID, other than in a custom report. -->

         如果搜索结果显示了键值对的用户计数，这表示像素放置正确且数据正在流动，则继续下一步。

   1. [为在Audience Manager中创建区段创建创建基于规则的特征](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html)。

      * 为特征命名，使其在测试活动中易于识别。 将特征存储在您喜欢的任何文件夹中。

      * 选择`Ad Cloud`作为&#x200B;**[!UICONTROL Data Source]**。

      * 对于特征表达式，使用`d_event`作为&#x200B;**[!UICONTROL Key]**，使用`imp`作为&#x200B;**[!UICONTROL Value]**。

   1. [在Audience Manager中为新特征设置测试区段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html)，选择`Ad Cloud`作为&#x200B;**[!UICONTROL Data Source]**。

      Audience Manager会自动将区段拆分为接收标准登陆页面体验的控制组和接收个性化现场体验的测试组。

## 步骤3：在[!DNL Target]中为DSP设置A/B测试活动

以下说明重点介绍与DSP用例相关的信息。

1. [登录到Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html)。

1. [创建A/B测试](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)：

   1. 在&#x200B;**[!UICONTROL Enter Activity URL]**&#x200B;字段中，输入测试的登陆页面URL。

      >[!NOTE]
      >
      >您可以使用多个URL来测试浏览网站条目。 有关详细信息，请参阅“[多页面活动](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html)”。 通过在Analytics中创建[网站条目报告](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/integrations/adobe-advertising-dsp/create-advertising-cloud-site-entry-reports)，可以轻松通过页面URL识别热门条目。

   1. 在&#x200B;**[!UICONTROL Goal]**&#x200B;字段中，输入测试的成功量度。

      >[!NOTE]
      >
      >确保在[!DNL Target]中将[!DNL Analytics]启用为数据源，并选择正确的报表包。

   1. 将&#x200B;**[!UICONTROL Priority]**&#x200B;设置为`High`或`999`可防止在测试区段中的用户收到错误的现场体验时发生冲突。

   1. 在&#x200B;**[!UICONTROL Reporting Settings]**&#x200B;内，选择连接到您的DSP帐户的&#x200B;**[!UICONTROL Company Name]**&#x200B;和&#x200B;**[!UICONTROL Report Suite]**。

      有关其他报告提示，请参阅“[报告最佳实践和疑难解答](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html)”。

   1. 在&#x200B;**[!UICONTROL Date Range]**&#x200B;字段中，为测试输入适当的开始日期和结束日期。

   1. 将受众添加到活动：

      1. 选择您之前在Audience Manager中创建的[区段以测试浏览受众](#view-through-framework)。

      1. 选择&#x200B;**[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**，然后在&#x200B;**[!UICONTROL Value]**&#x200B;字段中输入DSP放置键以使用点进受众的Target查询字符串参数。

   1. 对于&#x200B;**[!UICONTROL Traffic Allocation Method]**，选择&#x200B;**[!UICONTROL Manual (Default)]**&#x200B;并按50/50拆分受众。

   1. 保存活动。

1. 使用[Target可视化体验编辑器](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)对A/B测试登陆页面模板进行设计更改。

   * 体验A：请勿编辑，因为这是无个性化的默认/控制登陆页面体验。

   * 体验B：使用[!DNL Target]用户界面根据测试中包含的资产（如标题、文案、按钮放置和创意）自定义登陆页面模板。

   >[!NOTE]
   >
   >例如，创意测试用例，请联系您的Adobe客户团队。

## 步骤4：在[!DNL Analytics]中设置您的[!DNL Analytics for Target] Analysis Workspace

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T)是一种跨解决方案的集成，它允许广告商根据[!DNL Analytics]转化指标和受众区段创建[!DNL Target]活动，然后使用[!DNL Analytics]作为报表源度量结果。 该活动的所有报表和区段都基于[!DNL Analytics]数据收集。

有关[!DNL Analytics for Target]的详细信息（包括指向实施说明的链接），请参阅“[Adobe Analytics作为Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)的报表源”。

### 设置[!DNL Analytics for Target]面板

在Analysis Workspace中，配置[!DNL Analytics for Target panel]以分析您的[!DNL Target]活动和体验。 请牢记以下有关您的报告的重要指针和信息。

#### 量度

* 在工作区中创建一个面板，该面板特定于运行测试的Adobe Advertising营销活动、包或投放位置。 使用摘要可视化图表在与[!DNL Target]测试性能相同的报表中显示Adobe Advertising量度。

* 优先使用现场量度（例如访问和转化）来衡量绩效。

* 了解Adobe Advertising中的汇总媒体量度（例如展示次数、点击量和成本）无法与[!DNL Target]量度匹配。

#### 维度

以下维度与[!DNL Analytics for Target]相关：

* **[!UICONTROL Target Activities]**： A/B测试的名称

* **[!UICONTROL Target Experiences]**：活动中使用的登陆页面体验的名称

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]**：同一行中的活动名称和体验名称

### 针对[!DNL Target]数据的分析疑难解答

在Analysis Workspace中，如果您发现活动和体验数据很少或未填充数据，请执行以下操作：

* 验证是否对[!DNL Target]和[!DNL Analytics]使用了相同的[!UICONTROL Supplemental Data ID] (SDID)。 您可以在促销活动将用户引导至的登陆页面上使用[Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html)来验证SDID值。

[Adobe Debugger中的补充数据ID (SDID)值](/help/integrations/assets/target-troubleshooting-sdid.png)

* 在同一登录页上，验证a) Adobe Debugger中[!UICONTROL Solutions] > [!UICONTROL Target]下显示的[!UICONTROL Hostname]与b) [!DNL Target]中显示的[!UICONTROL Tracking Server]匹配（在[!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]下）。

  [!DNL Analytics For Target]要求在Analytics的[!DNL Target]到[!DNL Modstats]数据收集服务器的调用中发送[!DNL Analytics]跟踪服务器。<!-- just "to Analytics?"-->

[Adobe Debugger中的主机名值](/help/integrations/assets/target-troubleshooting-hostname.png)

[Target中的跟踪服务器值](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 进一步阅读

* [将Target与Analytics集成](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) — 说明如何在Analysis Workspace中设置[!DNL Target]报表。
* [A/B测试概述](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) — 介绍可与DSP广告一起使用的A/B测试活动。
* [体验和选件](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) — 介绍[!DNL Target]用于确定DSP测试用户向其公开的现场内容的工具。
* [信号、特征和区段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) — 定义一些有助于进行DSP浏览测试的Audience Manager工具。
* [Analytics for Advertising概述](/help/integrations/analytics/overview.md) — 介绍Analytics for Advertising，它允许您跟踪Analytics实例中的点进和浏览网站交互。

>[!MORELIKETHIS]
>
>* [在Adobe Target中为Advertising Search、Social和Commerce Ads配置A/B测试](ab-tests-search.md)
