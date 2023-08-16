---
title: 附加 [!DNL Analytics for Advertising] 宏到 [!DNL Google Campaign Manager 360] 广告标记
description: 了解添加原因和方式 [!DNL Analytics for Advertising] 将宏添加到 [!DNL Google Campaign Manager 360] 广告标记
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: aa41ba08ba83bfacbc2541c0f0d90336b3c36305
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# 附加 [!DNL Analytics for Advertising] 宏到 [!DNL Google Campaign Manager 360] 广告标记

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

*仅适用于Advertising DSP*

如果您使用的广告标记来自 [!DNL Google Campaign Manager 360] 对于Advertising DSP广告，请附加 [!DNL Analytics for Advertising] 参数到您的登陆页面URL，使用 [`%p` 宏](https://support.google.com/campaignmanager/table/6096962). 参数记录AMO ID (`s_kwcid`)和 `ef_id` 登陆页面URL中的查询字符串参数，允许Adobe Advertising将广告的点击数据发送到Adobe Analytics。

将宏用于 [!DNL Campaign Manager 360] 以下类型的显示广告和视频广告 [!DNL Analytics for Advertising] 实施：

* **使用的广告商 [!DNL Adobe] [!DNL Analytics for Advertising] 在其网站上实施的JavaScript代码**：JavaScript代码已记录AMO ID (`s_kwcid`)和 `ef_id` 查询字符串参数。 但是，当不支持第三方Cookie时，使用宏会扩展跟踪以包含基于点击的转换。 最佳实践是将以下部分中的宏添加到广告标记中，以捕获未通过JavaScript代码捕获的其他点进数据。

>[!NOTE]
>
>JavaScript代码是一种仅在Cookie仍然可用时用于点击跟踪的解决方案。 停止Cookie后，需要实施以下宏。

* **网站不使用 [!DNL Analytics for Advertising] JavaScript代码并依赖 [!DNL Analytics] 仅针对点进数据的服务器端转发** （不含任何浏览数据）：需要以下宏来报告通过Adobe Advertising购买的广告所驱动的网站点击活动。

## 将宏附加到 [!DNL Google Campaign Manager 360] 广告

范围 [!DNL Google Campaign Manager 360]，将附加到每个显示广告和视频广告的登陆页面URL中的以下参数： `%pamo=!;`

您可以通过多种方式指定登陆页面URL。 以下子部分包含每个选项的说明。

以下是带有后缀格式的登陆页面URL示例。

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>>* 如果登陆页面URL包含哈希符号(#)（这种情况不常见），请放置 `amo` 散列符号之前的参数。
>* 如果之后未包含其他参数，则 `amo` 参数，然后在其后面添加一个参数（例如，&amp;a=b）。 示例： `https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### 配置广告商级别的登陆页面URL后缀

1. 请参阅 [打开广告商属性的说明](https://support.google.com/campaignmanager/answer/2829344).
1. 在 [!UICONTROL Landing page URL suffix] 设置，包括 `%pamo!;` 在 [!UICONTROL URL suffix] 字段。

### 配置营销活动级别的登陆页面URL后缀

1. 请参阅 [有关打开营销活动属性的说明](https://support.google.com/campaignmanager/answer/2838056#set).
1. 在 [!UICONTROL Landing page URL suffix] 设置，包括 `%pamo!;` 在 [!UICONTROL URL suffix] 字段。

### 配置创意级别的登陆页面URL后缀

1. 打开创意资产。
1. 在 [!UICONTROL Click tags] 设置，包括 `%pamo!;` 在 [!UICONTROL Landing page] 单击标记的列。

## 如何 [!DNL Analytics for Advertising] 宏在DSP中展开

在DSP中，当您创建的广告包含 [!DNL Analytics for Advertising] 参数(`amo`)，则 `ef_id` 和 `s_kwcid` 宏会自动附加到单击URL中。 最佳做法是检查DSP中的标记，以确保 `ef_id` 和 `s_kwcid` 存在宏。

以下示例为 [!DNL Google Campaign Manager 360] [ins标记](https://support.google.com/campaignmanager/answer/6080468) 在DSP中显示的内容。

```
<ins class='dcmads' style='display:inline-block;width:160px;height:600px'
data-dcm-placement='N6482.2155306TUBEMOGUL/B23486129.261313631'
data-dcm-rendering-mode='iframe'
data-dcm-https-only
data-dcm-resettable-device-id=''
data-dcm-app-id='' data-dcm-click-tracker='${TM_CLICK_URL}'
data-dcm-param-amo='ef_id=${TM_USER_ID}:${TM_DATETIME}:d&s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}'>
<script src='https://www.googletagservices.com/dcm/dcmads.js'></script>
</ins>
```

当用户单击广告时， [!DNL Google Campaign Manager 360] 看到 `%pamo` （在URL后缀中）并动态插入 `amo` 参数移入URL。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [使用的Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [附加 [!DNL Analytics for Advertising] 宏到 [!DNL Flashtalking] 广告标记](macros-flashtalking.md)
