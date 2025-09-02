---
title: Adobe Advertising与Adobe Customer Journey Analytics之间的集成概述
description: 了解将Adobe Advertising与Adobe Customer Journey Analytics集成的选项。
feature: Integration with Adobe Customer Journey Analytics
exl-id: 57636259-f91a-404f-b972-994af67098b1
source-git-commit: 14f2bd22c44237a817443d48e798457e6c78312e
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Adobe Advertising与Customer Journey Analytics之间的集成概述

<!-- title? If I change, change refs throughout -->

使用Advertising DSP和&#x200B;*的[!DNL Advertising Search, Social, & Commerce]*&#x200B;广告商

Adobe Advertising与Adobe Customer Journey Analytics集成，可实现双向数据共享和报告。 您可以使用两个选项来设置集成：

* 同时具有[!DNL Analytics for Advertising]和Customer Journey Analytics的广告商具有通过[!DNL Analytics for Advertising]实现的相同功能，并在Customer Journey Analytics中添加了可视化图表。

  您仍可以使用Adobe Experience Platform Web SDK (`alloy.js`)或Adobe Experience Cloud Identity Service (`visitorAPI.js`)跟踪点进事件。 使用Advertising DSP的广告商仍将使用JavaScript代码片段来跟踪浏览事件。 Customer Journey Analytics中可用的数据包括：

   * 来自Customer Journey Analytics中Adobe Advertising的营销活动效果数据

   * 在Customer Journey Analytics中由[!DNL Google Ads]和[!DNL Microsoft Advertising]跟踪的网站活动和转化，每日更新

   * 来自Adobe Advertising中[!DNL Analytics]的归因数据，该数据可用于优化和报表

  在此使用案例中，您仍应可选[收集AMO ID和EF ID的历史数据，以便在Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md)中使用。

<!--
  In this use case, you don't need to perform any extra steps except to optionally [collect historical data for AMO IDs and EF IDs for use in Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
-->

* （即将推出的测试版功能）具有Customer Journey Analytics但不具有[!DNL Analytics for Advertising]的广告商可以使用[Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hans)在Adobe Advertising和Customer Journey Analytics之间原生交换数据。 您可以使用Cookie、哈希IP和通用ID （[!DNL LiveRamp RampIDs]和ID5 ID）跟踪网站事件，并将网站事件归因于付费媒体活动。 以下数据适用于促销活动、广告组、包、投放位置和关键词级别：

   * 来自Customer Journey Analytics中Adobe Advertising的营销活动效果数据

     **注意：**&#x200B;来自[!DNL Apple]和[!DNL Tiktok]的数据不可用。

   * 在Customer Journey Analytics中由[!DNL Google Ads]和[!DNL Microsoft Advertising]跟踪的网站活动和转化

   * Adobe Advertising中Customer Journey Analytics的归因数据，可用于优化和报表

  在此使用案例中，使用Web SDK跟踪网站事件（使用Cookie、哈希IP地址或通用ID），并将网站事件归因于[!DNL Google Ads]、[!DNL Microsoft Advertising]和[!DNL Meta]中的付费媒体活动以及Adobe DSP。 您还将使用Adobe Experience Platform进行数据收集。

## 如何启动Adobe Advertising与Customer Journey Analytics之间的本机集成

请联系您的Adobe客户团队，他们将会完成开始所需的初始配置，并将帮助您根据贵组织的需求规划实施和数据使用情况。

>[!MORELIKETHIS]
>
>* [先决条件](prerequisites.md)
>* [使用的 [!DNL Customer Journey Analytics]](ids.md)Adobe Advertising ID
>* Customer Journey Analytics中的[Adobe Advertising指标和维度](advertising-data-in-cja.md)
>* (Adobe Analytics用户) [收集在Adobe Customer Journey Analytics中使用的AMO ID和EF ID的历史数据](/help/integrations/analytics/rvars-to-evars.md)。
