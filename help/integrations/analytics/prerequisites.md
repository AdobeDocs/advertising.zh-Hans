---
title: 实施的先决条件和关键信息 [!DNL Analytics for Advertising]
description: 实施的先决条件和关键信息 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 08e54e2b-ed9b-4489-8de5-ab1379b7133c
source-git-commit: 3fd9323e6b6a525392aff67cc116bd649f2936b1
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# 实施的先决条件和关键信息 [!DNL Analytics for Advertising]

*使用Advertising DSP和[!DNL Advertising Search]*

在将Adobe广告与Adobe Analytics集成之前，请查看以下信息。

## 在中报告Adobe广告数据的要求 [!DNL Analytics]

* 以下任一项：
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Experience Cloud标识服务： `visitorAPI.js` 版本2.0或更高版本
* 任何版本的Adobe Analytics(包括 [!DNL Prime], [!DNL Premium]或 [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` 版本2.1或更高版本

>[!TIP]
>
>要提高数据保真度，请使用每个库的最新版本。

## 与Adobe广告共享Analytics区段的要求

* Experience Cloud标识服务： `visitorAPI.js` 版本2.1或更高版本
* Adobe Analytics: `appMeasurement.js` 版本1.8或更高版本

## 报告要求 [!DNL Analytics] Adobe广告中的数据

为Adobe广告实施团队提供以下信息：

* 的 [!DNL Analytics] 报表包ID，用于报告付费媒体活动并提供网站活动，以在Adobe广告中优化和报告
* 公司的Experience Cloud组织ID（组织ID）。

您可以在 [Adobe Experience Cloud Debugger的“摘要”选项卡](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Experience Cloud Debugger摘要屏幕](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Adobe广告中的数据 {#lookback-a4adc}

因为 [!DNL Analytics] 数据会发送到Adobe广告以进行报告和优化，则数据受属性规则(包括为Adobe广告中的广告商配置的展示和点击回顾窗口)的约束。

![Adobe广告中的广告商级别回顾窗口设置](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe广告归因点击回顾窗口：首次单击后发生的天数，在该天数内，点击可归因于转化。 默认情况下，此值为60天；最长为90天
* Adobe广告归因展示回顾窗口：广告展示后可将展示归因于转化的天数。 默认情况下，此值为14天；最长为30天

   >[!NOTE]
   >
   > 展示回顾窗口专用于Adobe广告，而不是 [!DNL Analytics for Advertising]、报表。

的 [!DNL Analytics for Advertising] JavaScript使用这些设置来确定在多久之前将站点的显示到达条目或点进条目视为有效。 有关如何确定显示到达和点进的详细信息，请参阅[AdobeAnalytics使用的广告ID](ids.md).&quot;

## Adobe中的广告数据 [!DNL Analytics]

[!DNL Analytics] 在Analytics点击中设置Adobe广告ID(AMO ID)，但受广告商的eVar持久性设置的约束，该设置同时适用于点进和显示到达。 持久性设置在Adobe广告后端配置，并且 [!DNL Adobe] 客户团队可以更改。

* [!DNL Analytics for Advertising] eVar过期：AMO ID默认为60天

>[!NOTE]
>
>要对不同时间范围的数据进行分段，您可以 [设置自定义区段](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) Analysis Workspace中具有不同的回顾窗口。

## 支持的广告环境

* 搜索
* 显示
* 视频
* 在线视频
* 本机

联系您的 [!DNL Adobe] 帐户团队以了解每个渠道中最新受支持的广告环境。

## 实施前注意事项

* Adobe广告实施团队将设置集成。

* 此集成不会产生额外费用，服务器调用也不会产生额外费用 [!DNL Analytics] 或Adobe广告费。

* [!DNL Analytics for Advertising] 与广告服务器无关：显示到达或点进可能会从任何广告服务器发生，并且在登入网站时会生成相应的ID。

* 集成仅通过 [!DNL Analytics] 标准事件和自定义事件来Adobe广告，以优化后续付费媒体和广告工作的竞价。 它不会通过 [!DNL Analytics] 区段、计算量度和eVar来Adobe广告以进行竞价优化。

* Adobe广告在 [!DNL Analytics] 根据用户进入网站前点击或查看的最后一个广告，基于 [点击和查看回顾窗口](#lookback-a4adc) 在Adobe广告中配置。 如果网站访客在其配置文件中具有两种类型的网站登录交互，并且该点击位于回顾期内，则访客的点进ID将覆盖网站报表的显示到达ID。

* [!DNL Analytics for Advertising] Adobe Analytics中的转化跟踪使用可配置的跟踪回顾窗口（默认为60天）。 Adobe广告报表反映在此跟踪回顾窗口的末尾的网站转化和参与度。

* 支持所有广告类型。 但是，并非所有广告环境都受支持。

   例如，不跟踪连接的电视(CTV)广告，因为CTV中不会进行点击，并且同一设备上不会进行转化。 但是，如果在桌面环境中查看广告，则可能会跟踪一些浏览网站登入数据。

* [!DNL Analytics] 当前只跟踪转化并将其归因于同一设备上的访客。

* [!DNL Analytics for Advertising] 不支持应用程序内显示到达转化。

* 使用的服务器端转发实施的广告商不支持显示到达跟踪 [!DNL Analytics].

### 补充ID

为网站实施Experience Cloud标识服务后，即会生成包含 [!DNL Analytics] 或Adobe广告包含补充ID。

示例： `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

为了实现准确的Adobe集成， [!DNL Analytics for Advertising] 用于交付内容或记录目标量度的活动必须具有相应的 [!DNL Analytics] 点击，以共享相同的补充ID。

当您在 [!DNL Analytics]，请确保确认 [!DNL Analytics] 点击量。 在 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)，您可以在“Adobe广告”选项卡中将此ID视为 `sdid` 参数。

>[!NOTE]
>
> 此实施的工作方式与 [!DNL Analytics for Target] 集成。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [适用于Analytics for Advertising的JavaScript代码](/help/integrations/analytics/javascript.md)

