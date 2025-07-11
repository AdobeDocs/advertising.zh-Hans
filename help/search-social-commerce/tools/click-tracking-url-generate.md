---
title: 生成点击跟踪URL
description: 了解如何手动生成Search、Social和Commerce点击跟踪URL。
exl-id: 43a36869-146a-4c5f-b4f2-eddfb856480b
feature: Search Tools, Search Tracking
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# 使用跟踪URL工具生成搜索、社交和Commerce点击跟踪URL

*仅具有Adobe Advertising转化跟踪的广告商*

有关何时必须手动生成和实施点击跟踪URL的信息，请参阅“[何时以及如何生成点击跟踪URL](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)”。

>[!NOTE]
>
>此功能未在相关广告帐户中实施跟踪模板或目标URL。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]**。

1. 从列表中选择广告网络帐户。

   （[!DNL Google Ads]关键字；文本、移动设备应用程序安装和动态搜索广告；投放位置；站点链接；以及产品组）将显示跟踪模板字段的跟踪标记。 它们不包括任何帐户级别的附加参数。 跳至步骤4。

   对于所有其他类型的标记，输入信息以生成标记。

1. （如有必要）生成标记：

   1. 通过以下方式之一指定登陆页面，并在请求时提供站点链接或产品名称：

      * 通过输入完整路径和文件名或者单击&#x200B;**[!UICONTROL Browse]**&#x200B;在设备或网络上查找文件来指定包含该信息的文件。 该文件必须是以制表符分隔的文本文件，每行有一个项目，格式如下：

         * （创意内容，标准广告） `**landing_page**`

           其中`landing_page`是有效的登陆页面URL或基本URL。

           示例： http://www.example.com/travel.html

         * （[!DNL Microsoft Advertising]个站点链接）`sitelink <tab> ** <tab> landing_page`

           其中`sitelink`是站点链接名称，`landing_page`是有效的登陆页面URL或基本URL。

           示例： `Careers <tab> ** <tab> http://www.example.com/careers.html`

           该文件最多可包含10,000行。

         * （[!DNL Google Merchant Center]产品组和[!DNL Microsoft Advertising]产品广告）`product name <tab> ** <tab> landing_page`

           其中`product name`是产品名称，`landing_page`是有效的登陆页面URL或基本URL。

           示例： `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           该文件最多可包含10,000行。

      * 在输入字段中，按照以下格式每行输入一个项目：

         * （创意内容，标准广告） `landing_page`

           其中`landing_page`是有效的登陆页面URL或基本URL。

           示例： http://www.example.com/travel.html

         * （[!DNL Microsoft Advertising]个站点链接）`sitelink**landing_page`

           其中`sitelink`是站点链接名称，`landing_page`是有效的登陆页面URL或基本URL。

           示例： `Careers**http://www.example.com/careers.html`

         * （[!DNL Google Merchant Center]产品组和[!DNL Microsoft Advertising]产品广告）`product name**landing_page`

           其中`product name`是产品名称，`landing_page`是有效的登陆页面URL或基本URL。

           示例： Acme PR208**http://www.example.com/travel.html

   1. 单击&#x200B;**[!UICONTROL Generate Tracking URLs]**。

1. （可选）从屏幕或输出页面复制URL（以“http”或“https”开头），并在搜索或社交帐户中实施它们。

对于具有目标URL的帐户，请在相应的[!UICONTROL Base URL]字段中输入值。

对于具有最终URL的帐户，请在相应的[!UICONTROL Tracking Template]字段中输入屏幕上的值。 必须在`&url=`参数（如`{lpurl}`）之后为最终URL添加参数。 对于[!DNL Yahoo! Japan Ads]帐户，请使用参数`{lpurl}`。 有关在跟踪模板中指示最终URL的[!DNL Google Ads]和[!DNL Microsoft Advertising]参数列表，请参阅[[!DNL Google Ads] 文档](https://support.google.com/google-ads/answer/6305348)（请参阅“可用[!DNL ValueTrack]参数”部分中的“仅跟踪模板”参数）和[[!DNL Microsoft Advertising] 文档](https://help.ads.microsoft.com/#apex/3/en/56799/2)。

>[!MORELIKETHIS]
>
>* [关于用于创建和解码跟踪标记的工具](tracking-tools-about.md)
>* [何时以及如何生成点击跟踪URL](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [解码搜索、社交和Commerce点击跟踪URL](click-tracking-url-decode.md)
