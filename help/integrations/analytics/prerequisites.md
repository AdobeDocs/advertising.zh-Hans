---
title: 实施 [!DNL Analytics for Advertising]的先决条件和关键信息
description: 实施 [!DNL Analytics for Advertising]的先决条件和关键信息
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 1559c2cb83e32d90f4b2fe959d07c4e588d9becf
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# 实施[!DNL Analytics for Advertising]的先决条件和关键信息

使用Advertising DSP和&#x200B;[!DNL Advertising Search, Social, & Commerce]*的*&#x200B;广告商

在将Adobe Advertising与Adobe Analytics集成之前，请查看以下信息。

## 在[!DNL Analytics]中报告Adobe Advertising数据的要求

* 以下任一项：
   * Adobe Experience Platform Web SDK： `alloy.js`
   * Experience Cloud标识服务： `visitorAPI.js`版本2.0或更高版本
* Adobe Analytics的任何版本（包括[!DNL Prime]、[!DNL Premium]或[!DNL Ultimate]）
* Adobe Analytics：`appMeasurement.js`版本2.1或更高版本
* (Advertising DSP客户)在网页中部署了[Advertising DSP JavaScript代码片段](javascript.md)以跟踪浏览访问。

>[!TIP]
>
>要提高数据保真度，请使用每个库的最新版本。

## 与Adobe Advertising共享Analytics区段的要求

* Experience Cloud标识服务： `visitorAPI.js`版本2.1或更高版本
* Adobe Analytics：`appMeasurement.js`版本1.8或更高版本

## 在Adobe Advertising中报告[!DNL Analytics]数据的要求

向Adobe Advertising实施团队提供以下信息：

* 用于报告付费媒体活动和馈送网站活动以在Adobe Advertising中优化和报表的[!DNL Analytics]报表包ID
* 公司的Experience Cloud组织ID (Org ID)。

您可以在Adobe Experience Cloud Debugger[&#128279;](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=zh-Hans)的摘要选项卡中找到这两个ID。

![Experience Cloud Debugger摘要屏幕](/help/integrations/assets/a4adc-debugger-summary.png)

## Adobe Advertising中的[!DNL Analytics]数据 {#lookback-a4adc}

由于[!DNL Analytics]数据会被发送到Adobe Advertising以进行报表和优化，因此数据受归因规则的约束，包括为Adobe Advertising中的广告商配置的展示和点击回顾窗口。

Adobe Advertising![&#128279;](/help/integrations/assets/a4adc-lookbacks.png)中的广告商级别的回溯时段设置

* Adobe Advertising归因点击回顾窗口：首次单击后经过的天数，在此期间点击可归因于转化。 默认情况下，此值为60天，最大值为90天
* Adobe Advertising归因展示回顾时间范围：广告展示发生后，展示可归因于转化的天数。 默认情况下，此值为14天，最大值为30天

  >[!NOTE]
  >
  > 展示回顾时间范围特定于Adobe Advertising，而不是[!DNL Analytics for Advertising]报表。

[!DNL Analytics for Advertising] JavaScript使用这些设置来确定在多久之前将浏览进入条目或网站的点进条目视为有效。 有关如何确定显示到达和点进的详细信息，请参阅[Analytics使用的Adobe AdvertisingID](ids.md)。

## [!DNL Analytics]中的数据Adobe Advertising

[!DNL Analytics]在Analytics点击中设置Adobe AdvertisingID (AMO ID)，具体取决于广告商的[!DNL eVar]持久性设置，该设置同时适用于点进和显示点进。 持久性设置是在Adobe Advertising后端配置的，您的Adobe客户团队可以更改此设置。

* [!DNL Analytics for Advertising] [!DNL eVar]过期：AMO ID默认为60天

>[!NOTE]
>
>若要针对不同的时间范围对数据进行分段，您可以在Analysis Workspace中[设置具有不同回顾时间范围的自定义区段](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=zh-Hans)。

## 支持的广告环境

* Search
* 显示
* 视频
* 在线视频
* 已连接电视
* 原生

有关每个渠道中支持的最新广告环境，请联系您的Adobe客户团队。

## 实施前注意事项

* Adobe Advertising实施团队负责设置集成。

* 此集成不收取额外费用，服务器调用也不会产生额外的[!DNL Analytics]或Adobe Advertising费用。

* [!DNL Analytics for Advertising]与广告服务器无关：任何广告服务器都可能发生浏览或点进，并在站点登录时生成适当的ID。

* 该集成仅传递[!DNL Analytics]个标准和自定义事件来Adobe Advertising优化后续付费媒体和广告工作的竞价。 它不会传递[!DNL Analytics]区段、计算量度和[!DNL eVars]来Adobe Advertising竞价优化。

* Adobe Advertising根据Adobe Advertising中配置的[点击和浏览回看窗口](#lookback-a4adc)，在[!DNL Analytics]内基于用户进入网站之前上次点击或查看的播发创建永久ID。 如果网站访客的配置文件中同时具有两种类型的网站条目交互，并且点击在回顾期间内，则访客的点进ID将覆盖网站报表的浏览通过ID。

* Adobe Analytics中的[!DNL Analytics for Advertising]转化跟踪使用可配置的跟踪回顾窗口（默认为60天）。 Adobe Advertising报表反映在此跟踪回顾窗口末尾的网站转化和参与情况。

* 支持所有广告类型。<!--Clarify what this might include. It used to include CTV, but not anymore: However, not all ad environments are supported. -->

* 当前仅将[!DNL Analytics]转化跟踪并归因到同一设备上的访客。

* [!DNL Analytics for Advertising]不支持应用程序内显示到达转换。

* 使用[!DNL Analytics]的服务器端转发实施的广告商不支持浏览跟踪。

### 补充ID

为站点实施Experience Cloud标识服务后，包含[!DNL Analytics]或Adobe Advertising中的数据的点击将包含补充ID。

示例： `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

为了准确的数据集成，[!DNL Analytics for Advertising]活动用于交付Adobe Advertising或记录目标量度的所有内容调用必须具有共享相同补充ID的相应[!DNL Analytics]点击。

在[!DNL Analytics]中进行故障诊断时，请务必确认[!DNL Analytics]点击存在补充ID。 在[Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=zh-Hans)中，您可以在“Adobe Advertising”选项卡中看到此ID作为`sdid`参数。

>[!NOTE]
>
> 此实现的工作方式与[!DNL Analytics for Target]集成类似。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* 适用于Analytics for Advertising的[JavaScript代码](/help/integrations/analytics/javascript.md)
