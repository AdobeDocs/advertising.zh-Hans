---
title: 实施的先决条件和关键信息 [!DNL Analytics for Advertising]
description: 实施的先决条件和关键信息 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# 实施的先决条件和关键信息 [!DNL Analytics for Advertising]

*使用Advertising DSP和的广告商[!DNL Advertising Search]*

在将Adobe广告与Adobe Analytics集成之前，请查看以下信息。

## 在中报告Adobe广告数据的要求 [!DNL Analytics]

* 以下任一项：
   * Adobe Experience Platform Web SDK： `alloy.js`
   * Experience Cloud身份服务： `visitorAPI.js` 版本2.0或更高版本
* Adobe Analytics的任何版本(包括 [!DNL Prime]， [!DNL Premium]，或 [!DNL Ultimate])
* Adobe Analytics： `appMeasurement.js` 版本2.1或更高版本

>[!TIP]
>
>要提高数据保真度，请使用每个库的最新版本。

## 与Adobe广告共享Analytics区段的要求

* Experience Cloud身份服务： `visitorAPI.js` 版本2.1或更高版本
* Adobe Analytics： `appMeasurement.js` 版本1.8或更高版本

## 报告要求 [!DNL Analytics] Adobe广告中的数据

向Adobe广告实施团队提供以下信息：

* 此 [!DNL Analytics] 报告包ID，用于报告付费媒体活动和馈送网站活动，以便在Adobe广告中进行优化和报告
* 公司的Experience Cloud组织ID （组织ID）。

您可以在以下位置找到这两个ID： [Adobe Experience Cloud Debugger的“摘要”选项卡](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![“Experience Cloud Debugger摘要”屏幕](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Adobe广告中的数据 {#lookback-a4adc}

因为 [!DNL Analytics] 数据将发送到Adobe广告以供生成报表和进行优化，数据受为Adobe广告中的广告商配置的归因规则的约束，包括展示和点击回顾窗口。

![Adobe广告中的广告商级别回顾窗口设置](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe广告归因点击回顾窗口：首次点击后经过的天数，在此期间点击可归因于转化。 默认情况下，此值为60天；最大值为90天
* Adobe广告归因展示回顾时间范围：发生广告展示后的一段时间，在此时间内，展示可归因于转化。 默认情况下，此值为14天，最大值为30天

   >[!NOTE]
   >
   > 展示回顾窗口特定于Adobe广告，而不是 [!DNL Analytics for Advertising]，报告。

此 [!DNL Analytics for Advertising] JavaScript使用这些设置来确定多远才能将浏览进入条目或网站的点进条目视为有效。 有关如何确定显示到达和点进的详细信息，请参阅“[Analytics使用的Adobe广告ID](ids.md).”

## Adobe广告数据 [!DNL Analytics]

[!DNL Analytics] 在Analytics点击中设置Adobe广告ID (AMO ID)，具体取决于广告商的eVar持久性设置，该设置同时适用于点进和显示点进。 持久性设置是在AdobeAdvertising后端配置的，您的Adobe帐户团队可以对其进行更改。

* [!DNL Analytics for Advertising] eVar过期：对于AMO ID，默认情况下为60天

>[!NOTE]
>
>要针对不同的时间范围分段数据，您可以 [设置自定义区段](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) Analysis Workspace中的回溯时段不同。

## 支持的广告环境

* 搜索
* 显示
* 视频
* 在线视频
* 本机

有关每个渠道中支持的最新广告环境，请联系您的Adobe客户团队。

## 实施前注意事项

* Adobe广告实施团队将设置集成。

* 此集成不收取额外费用，服务器调用也不会产生额外费用 [!DNL Analytics] 或Adobe广告费。

* [!DNL Analytics for Advertising] 与广告服务器无关：任何广告服务器都可能会进行浏览到达或点进，并且在站点登录时生成适当的ID。

* 集成仅通过 [!DNL Analytics] 用于Adobe广告的标准事件和自定义事件，以便对后续付费媒体和广告工作进行竞价优化。 没有通过 [!DNL Analytics] 区段、计算量度和eVar用于Adobe广告以实现竞价优化。

* Adobe广告在中创建永久ID [!DNL Analytics] 基于用户进入网站前最后点击或查看的广告，基于 [点击和浏览回顾窗口](#lookback-a4adc) 在Adobe广告中配置。 如果网站访客的配置文件中同时具有两种类型的网站条目交互，并且点击在回顾期间内，则访客的点进ID将覆盖网站报表的浏览通过ID。

* [!DNL Analytics for Advertising] Adobe Analytics中的转化跟踪使用可配置的跟踪回顾窗口（默认为60天）。 Adobe广告报表反映在此跟踪回顾窗口结束之前的网站转化和参与度。

* 支持所有广告类型。 但是，并非所有广告环境都受支持。

   例如，不会跟踪已连接的电视(CTV)广告，因为CTV中不会发生点击，并且同一设备上不会发生转换。 但是，如果在桌面环境中查看了广告，则可能会跟踪一些浏览网站条目数据。

* [!DNL Analytics] 当前只跟踪转化并归因到同一设备上的访客。

* [!DNL Analytics for Advertising] 不支持应用程序内浏览转化功能。

* 对于使用服务器端转发实施的广告商，浏览转化跟踪不受支持 [!DNL Analytics].

### 补充ID

为站点实施Experience CloudIdentity服务后，包含来自的数据的点击 [!DNL Analytics] 或Adobe广告包含一个补充ID。

示例： `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

为了准确集成数据，使用的所有Adobe广告调用 [!DNL Analytics for Advertising] 用于交付内容或记录目标量度的活动必须具有相应的 [!DNL Analytics] 共享相同补充ID的点击。

当您在中进行故障诊断时 [!DNL Analytics]，请确保确认存在以下项的补充ID： [!DNL Analytics] 点击量。 在 [Adobe Experience Cloud调试器](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)，您可以在“Adobe广告”选项卡中看到此ID作为 `sdid` 参数。

>[!NOTE]
>
> 此实施的工作方式与 [!DNL Analytics for Target] 集成。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [适用于Analytics for Advertising的JavaScript代码](/help/integrations/analytics/javascript.md)

