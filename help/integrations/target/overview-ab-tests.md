---
title: 在Adobe Target中为Adobe Advertising广告配置A/B测试
description: 了解如何在中设置A/B测试 [!DNL Target] 用于您的DSP广告。
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: 1dbe8da7122b38dd11a242c453d71a832b31eee8
workflow-type: tm+mt
source-wordcount: '1551'
ht-degree: 0%

---

# 在Adobe Target中为Advertising DSP广告配置A/B测试

<!-- In title and Heading1:  DSP and [!DNL Advertising Search, Social, & Commerce] Ads -->

<!-- Add [!UICONTROL and [!DNL tags throughout as needed. -->

<!-- Break into sub-files, or just leave as one? -->

*仅使用Advertising DSP的广告商*

Adobe Advertising和Adobe Target使得营销人员能够更轻松地通过付费媒体和现场消息传递提供个性化的互联体验。 通过在产品之间共享信号，您可以：

* 通过将DSP促销活动中的客户广告曝光度与其网站上的体验关联，降低网站流失率。

* 通过使用Adobe Audience Manager曝光数据和点击馈送Target受众来镜像广告消息传递的现场体验，从而建立A/B测试。

* 在Adobe Analytics中使用简单的可视化图表来衡量统一消息对网站目标提升的影响 [!DNL Target].

请参阅以下部分，了解先决条件以及设置点进和浏览跟踪以及在DSP和之间实施信号共享的说明。 [!DNL Target] 和设置A/B测试活动，并设置 [!DNL Analytics] Analysis Workspace以查看测试数据。

如果您还有其他问题，请联系adcloud_support@adobe.com。

## 先决条件

此用例需要以下产品和集成：

* [!DNL Target]

* [[!DNL Analytics] 适用于广告](/help/integrations/analytics/overview.md) 集成<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] 对象 [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) 集成

* Audience Manager（仅对于浏览测试是必需的）

## 步骤1：设置点进框架 {#click-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![点进框架](/help/integrations/assets/target-ct-framework.png)

将DSP宏添加到点进URL（用户单击广告并到达登陆页面时显示的URL）时，DSP通过包含以下内容自动捕获投放位置键 `${TM_PLACEMENT_ID}` 点进URL中。 此宏捕获字母数字版面密钥，而不是数字版面ID。

![点进URL已附加到登陆页面URL](/help/integrations/assets/target-ct-url.jpg)

### (仅限DSP)将DSP宏添加到您的点进URL

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

在Flash对话或Google Campaign Manager 360中，手动更新每个广告的点进URL，以包含捕获AMO ID变量所需的宏。 AMO ID变量用于将点击数据发送到Adobe Analytics并共享A/B测试的放置键。 有关说明，请参阅以下页面：

* [附加 [!DNL Analytics for Advertising] 宏到 [!DNL Flashtalking] 广告标记](/help/integrations/analytics/macros-flashtalking.md)

* [附加 [!DNL Analytics for Advertising] 宏到 [!DNL Google Campaign Manager 360] 广告标记](/help/integrations/analytics/macros-google-campaign-manager.md)

请联系您的Adobe客户团队和广告解决方案小组(aac-advertising-solutions-group@adobe.com)，以检索所需的版面密钥并完成设置，并确保每个点进URL都填入了版面密钥。

## 步骤2：使用Audience Manager设置浏览框架 {#view-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![浏览框架](/help/integrations/assets/targetr-vt-framework.png)

通过在广告标签和投放设置中添加Audience Manager展示事件像素，您可以为其他显示到达测试机会创建测试区段。

1. 在广告标记和DSP投放设置中实施Audience Manager展示事件像素。

   有关说明，请参阅&quot;[从Advertising DSP Campaigns收集媒体接触数据](/help/integrations/audience-manager/media-data-integration/collect.md)“

   确保添加 [DSP宏](/help/dsp/campaign-management/macros.md) 用于捕获您希望展示事件像素传递回的所有数据，包括 `${TM_PLACEMENT_ID_NUM}` 用于表示数值版面ID。

   >[!NOTE]
   >
   >点击跟踪URL包括 `${TM_PLACEMENT_ID}` 字母数字放置键的宏，而不是 `${TM_PLACEMENT_ID_NUM}` 用于表示数值版面ID。

1. 从DSP展示数据配置Audience Manager区段：

   1. 验证区段数据是否可用：

      1. [搜索信号](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html) 对于 [键值对](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html) 确定区段用户分组到哪个级别。

         使用 [支持的键](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html) ，其值与添加到Audience Manager展示事件像素的宏相对应。

         例如，要对特定版面用户进行分组，请使用 `d_placement` 键。 对于该值，使用DSP宏捕获的实际数字放置ID(例如2501853) `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

         如果搜索结果显示了键值对的用户计数，这表示像素放置正确且数据正在流动，则继续下一步。

   1. [创建基于规则的特征](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) 用于在Audience Manager中创建区段。

      * 为特征命名，使其在测试活动中易于识别。 将特征存储在您喜欢的任何文件夹中。

      * 选择 `Ad Cloud` 作为 **数据源**.

      * 对于特征表达式，请使用 `d_event` 作为 **键** 和 `imp` 作为 **值**.

   1. [设置测试区段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html) 对于Audience Manager中的新特征，选择 `Ad Cloud` 作为 **数据源**.

      Audience Manager会自动将区段拆分为接收标准登陆页面体验的控制组，以及接收个性化现场体验的测试组。

## 步骤3：在Target中设置“A/B测试”活动

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

以下说明突出显示与DSP用例相关的信息。 有关完整说明，请参阅“”。

1. [登录到Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [创建A/B测试](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)：

   1. 在 **输入活动URL** 字段中，输入测试的登陆页面URL。

      >[!NOTE]
      >
      >您可以使用多个URL来测试浏览网站条目。 有关更多信息，请参阅&quot;[多页面活动](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html)“ 通过创建 [网站进入报表](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) 在Analytics中。

   1. 在 **目标** 字段中，输入测试的成功量度。

      >[!NOTE]
      >
      >确保 [!DNL Analytics] 在中启用为数据源 [!DNL Target]，并选择正确的报表包。

   1. 设置 **优先级** 到 `High` 或 `999` 以防止在测试区段中的用户收到错误的现场体验时发生冲突。

   1. 范围 **报表设置**，选择 **公司名称** 和 **报表包** 已连接到您的DSP帐户。

      有关其他报表提示，请参阅&quot;[报表最佳实践和疑难解答](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html)“

   1. 在 **日期范围** 字段中，输入测试的相应起始日期和终止日期。

   1. 将受众添加到活动：

      1. 选择 [您之前在Audience Manager中创建的区段来测试浏览受众](#view-through-framework).

      1. 选择 **网页** > **登陆页面** > **查询**，并在中输入DSP放置键 **值** 用于为点进受众使用Target查询字符串参数的字段。

   1. 对于 **流量分配方法**，选择 **手动（默认）** 然后把观众分成五成半。

   1. 保存活动。

1. 使用 [!DNL Target] [可视化体验编辑器](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) 对A/B测试登陆页面模板进行设计更改。

   * 体验A：请勿编辑，因为这是无个性化的默认/控制登陆页面体验。

   * 体验B：使用 [!DNL Target] 用于根据测试中包含的资产自定义登陆页面模板的用户界面（例如标题、文案、按钮放置和创意）。

   >[!NOTE]
   >
   >例如，创意测试用例，请与您的Adobe客户团队联系。

## 第4步：设置您的 [!DNL Analytics for Target] Analysis Workspace位于 [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T)是一种跨解决方案的集成，它允许广告商创建 [!DNL Target] 活动基于 [!DNL Analytics] 转化指标和受众区段，然后使用衡量结果 [!DNL Analytics] 作为报表源。 该活动的所有报表和区段均基于 [!DNL Analytics] 数据收集。

有关详情 [!DNL Analytics for Target]，包括实施说明的链接，请参阅&quot;[将Adobe Analytics作为Adobe Target报表源(A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)“。

### 设置 [!DNL Analytics for Target] 面板

在Analysis Workspace中，配置 [!DNL Analytics for Target panel] 分析 [!DNL Target] 活动和体验。 请牢记以下有关您的报告的重要指针和信息。

#### 量度

* 在工作区中创建一个面板，该面板特定于运行测试的Adobe Advertising促销活动、包或投放位置。 使用概要可视化图表显示同一报表中的Adobe Advertising度量和Target测试性能。

* 优先使用现场量度（例如访问和转化）来衡量绩效。

* 了解来自Adobe Advertising的汇总媒体量度（例如展示次数、点击量和成本）无法与Target量度匹配。

#### Dimension

以下维度与 [!DNL Analytics for Target]：

* **Target活动**：A/B测试的名称

* **Target体验**：活动中使用的登陆页面体验的名称

* **Target活动** > **体验**：同一行中的活动名称和体验名称

### Analytics疑难解答 [!DNL Target] 数据

在Analysis Workspace中，如果您发现活动和体验数据很少或未填充数据，请执行以下操作：

* 验证Target和Analytics是否使用了相同的补充数据ID (SDID)。 您可以使用验证SDID值 [Adobe Experience Cloud调试器](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) 在营销活动将用户引导到的登陆页面上。

[Adobe Debugger中的补充数据ID (SDID)值](/help/integrations/assets/target-troubleshooting-sdid.png)

* 在同一登录页上，验证a)“解决方案”>“目标”下的Adobe Debugger中显示的主机名是否与b)中显示的“跟踪服务器”相匹配 [!DNL Target] （在“目标和设置”>“报表设置”下）。

  [!DNL Analytics For Target] 需要 [!DNL Analytics] 要以调用形式发送的跟踪服务器 [!DNL Target] 到 [!DNL Modstats] Analytics的数据收集服务器。<!-- just "to Analytics?"-->

[Adobe Debugger中的主机名值](/help/integrations/assets/target-troubleshooting-hostname.png)

[Target中的跟踪服务器值](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 进一步阅读

* [将Target与Analytics集成](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) — 介绍如何在Analysis Workspace中设置Target报表。
* [A/B测试概述](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html)  — 介绍可与DSP广告一起使用的A/B测试活动。
* [体验和选件](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html)  — 解释 [!DNL Target] 用于确定向DSP测试用户展示的现场内容的工具。
* [信号、特征和区段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html)  — 定义一些有助于进行DSP显示到达测试的Audience Manager工具。
* [Analytics for Advertising概述](/help/integrations/analytics/overview.md)  — 引入了Analytics for Advertising，它允许您跟踪Analytics实例中的点进和浏览网站交互。

<!-- 
>[!MORELIKETHIS]
>
>* 
-->
