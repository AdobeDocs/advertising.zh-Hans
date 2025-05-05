---
title: 将 [!DNL Analytics for Advertising] 宏附加到 [!DNL Google Campaign Manager 360] 添加标记
description: 了解为什么以及如何将 [!DNL Analytics for Advertising] 宏添加到您的 [!DNL Google Campaign Manager 360] ad标记
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: aa41ba08ba83bfacbc2541c0f0d90336b3c36305
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# 将[!DNL Analytics for Advertising]宏附加到[!DNL Google Campaign Manager 360]广告标记

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

*仅适用于Advertising DSP*

如果您对Advertising DSP广告使用[!DNL Google Campaign Manager 360]中的广告标记，请使用[`%p`宏](https://support.google.com/campaignmanager/table/6096962)将[!DNL Analytics for Advertising]参数附加到登陆页面URL。 参数在登陆页面URL中记录AMO ID (`s_kwcid`)和`ef_id`查询字符串参数，允许Adobe Advertising将广告的点击数据发送到Adobe Analytics。

为以下类型的[!DNL Analytics for Advertising]实施的[!DNL Campaign Manager 360]显示广告和视频广告使用宏：

* **在其网站上实现的具有[!DNL Adobe] [!DNL Analytics for Advertising] JavaScript代码的广告商**： JavaScript代码已记录AMO ID (`s_kwcid`)和`ef_id`查询字符串参数。 但是，当不支持第三方Cookie时，使用宏会扩展跟踪以包含基于点击的转换。 最佳实践是将以下部分中的宏添加到广告标记，以捕获未通过JavaScript代码捕获的其他点进数据。

>[!NOTE]
>
>JavaScript代码是一种仅在Cookie仍然可用时用于点击跟踪的解决方案。 停止Cookie后，需要实施以下宏。

* **其网站不使用[!DNL Analytics for Advertising] JavaScript代码而仅依赖[!DNL Analytics]服务器端转发获取点进数据的广告商**（不包含任何点进数据）：需要以下宏来报告您通过Adobe Advertising购买的广告在网站上的点击活动。

## 将宏附加到[!DNL Google Campaign Manager 360]广告

在[!DNL Google Campaign Manager 360]内，将每个显示广告和视频广告的以下参数附加到登陆页面URL： `%pamo=!;`

您可以通过多种方式指定登陆页面URL。 以下子部分包含每个选项的说明。

以下是带有后缀格式的登陆页面URL示例。

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>&#x200B;>* 如果登陆页面URL包含不常见的哈希符号(#)，请将`amo`参数放在哈希符号之前。
>* 如果未在`amo`参数后面包含其他参数，则在该参数后面添加一个参数（例如，&amp;a=b）。 示例： `https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### 配置广告商级别的登陆页面URL后缀

1. 请参阅[有关打开广告商属性](https://support.google.com/campaignmanager/answer/2829344)的说明。
1. 在[!UICONTROL Landing page URL suffix]设置中，将`%pamo!;`包含在[!UICONTROL URL suffix]字段中。

### 配置营销活动级别的登陆页面URL后缀

1. 请参阅[有关打开营销活动属性](https://support.google.com/campaignmanager/answer/2838056#set)的说明。
1. 在[!UICONTROL Landing page URL suffix]设置中，将`%pamo!;`包含在[!UICONTROL URL suffix]字段中。

### 配置创意级别的登陆页面URL后缀

1. 打开创意资产。
1. 在[!UICONTROL Click tags]设置中，将`%pamo!;`包含在点击标记的[!UICONTROL Landing page]列中。

## 如何在DSP中展开[!DNL Analytics for Advertising]宏

在DSP中，当您创建包含[!DNL Analytics for Advertising]参数(`amo`)的广告时，`ef_id`和`s_kwcid`宏会自动附加到单击URL中。 最佳做法是检查DSP中的标记，以确保`ef_id`和`s_kwcid`宏存在。

以下是[!DNL Google Campaign Manager 360] [ins标记](https://support.google.com/campaignmanager/answer/6080468)在DSP中显示的示例。

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

当用户单击广告时，[!DNL Google Campaign Manager 360]会在URL后缀中看到`%pamo`，并动态地将`amo`参数的值插入到URL中。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>*  [!DNL Analytics][&#128279;](/help/integrations/analytics/ids.md)使用的Adobe AdvertisingID
>* [将 [!DNL Analytics for Advertising] 宏附加到 [!DNL Flashtalking] 添加标记](macros-flashtalking.md)
