---
title: 实施的先决条件和关键信息 [!DNL Analytics for Advertising]
description: 实施的先决条件和关键信息 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 8481227a8ccb1f1e6e715e34e14732967110c168
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# 实施的先决条件和关键信息 [!DNL Analytics for Advertising]

*具有广告 DSP 和[!DNL Advertising Search, Social, & Commerce]*

在将 Adobe Advertising 与 Adobe Analytics 集成之前，请查看以下信息。

## 在 [!DNL Analytics]

* 以下任一情况：
   * Adobe Experience Platform Web SDK： `alloy.js`
   * Experience Cloud Identity Service： `visitorAPI.js` 版本 2.0 或更高版本
* 任何版本的 Adobe Analytics（包括 [!DNL Prime]、 [!DNL Premium]或 [!DNL Ultimate]）
* Adobe Analytics： `appMeasurement.js` 版本 2.1 或更高版本
* （宣传DSP客户）一个 [广告 DSP JavaScript 代码段](javascript.md) ，部署在您的网页中，用于跟踪浏览型访问。

>[!TIP]
>
>要提高数据保真度，请使用每个库的最新版本。

## 与 Adobe Advertising 共享分析细分的要求

* Experience Cloud Identity Service： `visitorAPI.js` 版本 2.1 或更高版本
* Adobe Analytics： `appMeasurement.js` 版本 1.8 或更高版本

## 在 Adobe Advertising 中报告 [!DNL Analytics] 数据的要求

为 Adobe Advertising 实施团队提供以下内容：

* 报表包 ID， [!DNL Analytics] 用于报告付费媒体活动以及提供网站活动，以便在 Adobe Advertising 中进行优化和报告
* 公司的 Experience Cloud 组织 ID（组织 ID）。

您可以在 Adobe Experience Cloud 调试器的](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)“[摘要”选项卡上找到这两个 ID。

![Experience Cloud 调试器摘要屏幕](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Adobe 广告中的数据 {#lookback-a4adc}

由于数据会发送到 Adobe Advertising 进行报告和优化，因此 [!DNL Analytics] 数据受归因规则（包括展示和点击回溯窗口）的约束，这些规则是在 Adobe Advertising 中为广告客户配置的。

![Adobe Advertising 中的广告客户级回溯窗口设置](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe 广告归因点击回溯窗口：首次点击发生后，点击可归因于转化的天数。 默认情况下，此值为 60 天;最长为 90 天
* Adobe 广告归因展示回顾窗口：广告展示发生后可以将展示归因于转化的天数。 默认情况下，此值为 14 天;最长为 30 天

  >[!NOTE]
  >
  > 展示回顾窗口特定于 Adobe 广告，而不是 [!DNL Analytics for Advertising]报告。

[!DNL Analytics for Advertising] JavaScript 使用这些设置来确定将网站的查看型条目或点击型条目视为有效的回溯时间。有关如何确定浏览型和点击型的更多信息，请参阅“[Analytics](ids.md) 使用的 Adobe 广告 ID”。

## Adobe 广告数据 [!DNL Analytics]

[!DNL Analytics] 在 Analytics（分析）匹配中设置 Adobe 广告 ID （AMO ID），但须遵守广告客户的 [!DNL eVar] 持久性设置，该设置同时适用于点击率和浏览型。 持久性设置是在 Adobe Advertising 后端配置的，您的 Adobe 帐户团队可以更改它。

* [!DNL Analytics for Advertising][!DNL eVar]过期时间：AMO ID 默认为 60 天

>[!NOTE]
>
>要细分不同时间范围的数据，您可以在 [分析工作区中设置具有不同回溯窗口的自定义区段](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) 。

## 支持的广告环境

* 搜索
* 显示
* 视频
* 在线视频
* 联网电视
* 本地

请联系您的 Adobe 帐户团队，了解每个渠道中支持的最新广告环境。

## 实施之前需要了解的事项

* Adobe Advertising 实施团队负责设置集成。

* 不会为此集成收取额外费用，服务器调用也不会产生额外费用 [!DNL Analytics] 或 Adobe 广告费用。

* [!DNL Analytics for Advertising] 与广告服务器无关：任何广告服务器都可能发生浏览型或点击型，并且在输入网站时会生成正确的 ID。

* 该集成仅 [!DNL Analytics] 将标准事件和自定义事件传递给 Adobe Advertising，以便对后续付费媒体和广告工作进行出价优化。 它不会传递 [!DNL Analytics] 细分、计算指标和 [!DNL eVars] Adobe 广告以进行出价优化。

* Adobe Advertising 会根据用户进入网站之前最后点击或查看的广告，基于 Adobe Advertising 中配置的[点击和浏览回溯窗口](#lookback-a4adc)，在 中创建[!DNL Analytics]持久 ID。如果网站访问者的配置文件中同时具有两种类型的网站入口互动，并且点击是在回溯期内进行的，则访问者的点击链接型 ID 将覆盖网站报告的浏览型 ID。

* [!DNL Analytics for Advertising] Adobe Analytics 中的转化跟踪使用可配置的跟踪回溯窗口（默认为 60 天）。 Adobe 广告报告反映通过此跟踪回溯窗口结束的网站转化率和互动度。

* 支持所有广告类型。 但是，并非所有广告环境都受支持。

* [!DNL Analytics] 目前，系统仅跟踪转化并将其归因于同一设备上的访问者。

* [!DNL Analytics for Advertising] 不支持应用内浏览型转化。

* 使用服务器端转发实现 [!DNL Analytics]的广告客户不支持浏览型跟踪。

### 补充身份证

在为网站实施 Experience Cloud 身份服务后，包含来自 Adobe Advertising 的数据 [!DNL Analytics] 的点击中就会包含一个补充 ID。

例： `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

为了准确集成数据，活动用于 [!DNL Analytics for Advertising] 投放内容或记录目标指标的所有 Adobe 广告调用都必须具有共享相同补充 ID 的相应 [!DNL Analytics] 匹配。

在 中进行 [!DNL Analytics]故障排除时，请务必确认命中存在 [!DNL Analytics] 补充 ID。 在 Adobe Experience Cloud 调试器](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)中[，您可以在“Adobe 广告”选项卡中看到此 ID 作为`sdid`参数。

>[!NOTE]
>
> 此实现的工作方式与 [!DNL Analytics for Target] 集成类似。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [用于广告分析的 JavaScript 代码](/help/integrations/analytics/javascript.md)
