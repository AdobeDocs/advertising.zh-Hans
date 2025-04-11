---
title: 将 [!DNL Analytics for Advertising] 宏附加到 [!DNL Flashtalking] 添加标记
description: 了解为什么以及如何将 [!DNL Analytics for Advertising] 宏添加到您的 [!DNL Flashtalking] ad标记
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: e8c8316418acf4a8c62beabcae2c1b7388dbc297
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# 将[!DNL Analytics for Advertising]宏附加到[!DNL Flashtalking]广告标记

*仅集成Adobe Advertising-Adobe Analytics的广告商*

*仅与[!DNL Flashtalking]没有直接伙伴关系的组织*

*仅适用于Advertising DSP*

如果您对Advertising DSP广告使用[!DNL Flashtalking]中的广告标记，则必须将跟踪参数附加到登陆页面URL。 要与[!DNL Flashtalking]使用Advertising DSP合作关系，请将Analytics for Advertising参数附加到登陆页面URL。 这些参数在登陆页面URL中记录AMO ID (`s_kwcid`)和`ef_id`查询字符串参数，从而允许Adobe Advertising将广告的点击数据发送到Adobe Analytics。

>[!NOTE]
>
>如果您的组织与[!DNL Flashtalking]有直接合作关系，则您无需执行此过程。 请改为登录到您的[!DNL Flashtalking]帐户并按照[!DNL Flashtalking]支持文档中的说明来使用`https://support.flashtalking.com%2Fhc%2Fen-us%2Farticles%2F4409808166419-Accessing-Data-Pass-Macros`上的数据传递宏收集点击数据。

为以下类型的[!DNL Analytics for Advertising]实施的[!DNL Flashtalking]显示广告和视频广告使用宏：

* **在其网站上实现的具有[!DNL Adobe] [!DNL Analytics for Advertising] JavaScript代码的广告商**： JavaScript代码已记录AMO ID (`s_kwcid`)和`ef_id`查询字符串参数。 但是，当不支持第三方Cookie时，使用宏会扩展跟踪以包含基于点击的转换。 最佳实践是将以下部分中的宏添加到广告标记，以捕获未通过JavaScript代码捕获的其他点进数据。

  >[!NOTE]
  >
  >JavaScript代码是一种仅在Cookie仍然可用时用于点击跟踪的解决方案。 停止Cookie后，需要实施以下宏。

* **其网站不使用[!DNL Analytics for Advertising] JavaScript代码而仅依赖[!DNL Analytics]服务器端转发获取点进数据的广告商**（不包含任何点进数据）：需要以下宏来报告您通过Adobe Advertising购买的广告所驱动的网站点击活动。

## 显示广告标记

在[!DNL Flashtalking]广告标记设置中，将以下宏附加到`Clicktag`字段中的点进URL的末尾：

```
[ftqs:[AdobeAMO]]
```

如果它是基础URL之后的第一个或唯一查询字符串，则使用`?`将其与基础URL分开。 如果基本URL包含多个查询字符串，则第一个字符串以`?`开头，每个后续字符串以`&`开头。

示例：

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## 视频广告标记

在[!DNL Flashtalking]广告标记设置中，将以下宏附加到`Clicktag`字段中的点进URL的末尾：

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

如果它是基础URL之后的第一个或唯一查询字符串，则使用`?`将其与基础URL分开。 如果基本URL包含多个查询字符串，则第一个字符串以`?`开头，每个后续字符串以`&`开头。

示例：

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>*  [!DNL Analytics]](/help/integrations/analytics/ids.md)使用的[Adobe Advertising ID
>* [将 [!DNL Analytics for Advertising] 宏附加到 [!DNL Google Campaign Manager 360] 添加标记](/help/integrations/analytics/macros-google-campaign-manager.md)

