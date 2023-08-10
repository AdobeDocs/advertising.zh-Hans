---
title: 附加 [!DNL Analytics for Advertising] 宏到 [!DNL Flashtalking] 广告标记
description: 了解添加原因和方式 [!DNL Analytics for Advertising] 将宏添加到 [!DNL Flashtalking] 广告标记
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# 附加 [!DNL Analytics for Advertising] 宏到 [!DNL Flashtalking] 广告标记

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

*仅适用于Advertising DSP*

如果您使用的广告标记来自 [!DNL Flashtalking] 对于Advertising DSP广告，请将Analytics for Advertising参数附加到登陆页面URL。 参数记录AMO ID (`s_kwcid`)和 `ef_id` 登陆页面URL中的查询字符串参数，允许Adobe Advertising将广告的点击数据发送到Adobe Analytics。

将宏用于 [!DNL Flashtalking] 以下类型的显示广告和视频广告 [!DNL Analytics for Advertising] 实施：

* **使用的广告商 [!DNL Adobe] [!DNL Analytics for Advertising] 在其网站上实施的JavaScript代码**：JavaScript代码已记录AMO ID (`s_kwcid`)和 `ef_id` 查询字符串参数。 但是，当不支持第三方Cookie时，使用宏会扩展跟踪以包含基于点击的转换。 最佳实践是将以下部分中的宏添加到广告标记中，以捕获未通过JavaScript代码捕获的其他点进数据。

>[!NOTE]
>
>JavaScript代码是一种仅在Cookie仍然可用时用于点击跟踪的解决方案。 停止Cookie后，需要实施以下宏。

* **网站不使用 [!DNL Analytics for Advertising] JavaScript代码并依赖 [!DNL Analytics] 仅针对点进数据的服务器端转发** （不含任何浏览数据）：需要以下宏来报告通过Adobe Advertising购买的广告所驱动的网站点击活动。

## 显示广告标记

在 [!DNL Flashtalking] 添加标记设置时，将以下宏附加到中点进URL的末尾 `Clicktag` 字段：

```html
?[ftqs:[AdobeAMO]]
```

示例：  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

## 视频广告标记

在 [!DNL Flashtalking] 添加标记设置时，将以下宏附加到中点进URL的末尾 `Clicktag` 字段：

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

示例：  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [使用的Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [附加 [!DNL Analytics for Advertising] 宏到 [!DNL Google Campaign Manager 360] 广告标记](/help/integrations/analytics/macros-google-campaign-manager.md)
