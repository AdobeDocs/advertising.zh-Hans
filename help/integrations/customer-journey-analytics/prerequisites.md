---
title: 将Adobe Advertising与Customer Journey Analytics集成的先决条件
description: 将Adobe Advertising与Customer Journey Analytics集成的先决条件
feature: Integration with Adobe Customer Journey Analytics
exl-id: 4bd14178-5003-4da6-9034-d070c57f0e9b
source-git-commit: 9e89f91f31c756e21db3f5b2b7c87991166e4859
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---

# 将Adobe Advertising与Customer Journey Analytics集成的先决条件

使用Advertising DSP和&#x200B;*的[!DNL Advertising Search, Social, & Commerce]*&#x200B;广告商

* 同时具有[!DNL Analytics for Advertising]和Customer Journey Analytics的广告商：

   * Adobe Customer Journey Analytics<!-- any specific version? -->

   * [ [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md)的所有其他先决条件。

* (Beta功能)具有Customer Journey Analytics但不具有[!DNL Analytics for Advertising]的广告商：

   * Adobe Experience Platform Web SDK库： `alloy.js`

     用于Web SDK的[!DNL Org ID]和用于Adobe Advertising广告商帐户的必须相同。 您可以在Adobe Experience Cloud Debugger[的](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=zh-Hans)摘要选项卡中找到此ID。

     ![Experience Cloud Debugger的“摘要”屏幕](/help/integrations/assets/a4adc-debugger-summary.png)

     您需要获得Experience Platform站点管理员的支持才能创建Experience Platform数据流和XDM架构。

   * Adobe Customer Journey Analytics<!-- any specific version? -->

     您需要获得内部Web分析人员的支持，才能设置与数据集的连接并配置报表。

>[!TIP]
>
>要提高数据保真度，请使用每个库的最新版本。

>[!MORELIKETHIS]
>
>* [概述](overview.md)
>* (Adobe Analytics用户) [收集在Adobe Customer Journey Analytics中使用的AMO ID和EF ID的历史数据](/help/integrations/analytics/rvars-to-evars.md)。
