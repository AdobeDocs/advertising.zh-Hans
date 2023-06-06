---
title: 生成点击跟踪URL
description: 了解如何手动生成Search、Social和Commerce点击跟踪URL。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---

# 使用跟踪URL工具生成搜索、社交和商务点击跟踪URL

*仅具有Adobe广告转化跟踪的广告商*

有关何时必须手动生成和实施点击跟踪URL的信息，请参阅[何时以及如何生成点击跟踪URL](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).”

>[!NOTE]
>
>此功能未在相关广告帐户中实施跟踪模板或目标URL。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]**.

1. 从列表中选择广告网络帐户。

   ([!DNL Google Ads] 关键词、文本、移动应用程序安装和动态搜索广告、投放位置、站点链接和产品组)显示跟踪模板字段的跟踪标记。 它们不包括任何帐户级别的附加参数。 跳至步骤4。

   对于所有其他类型的标记，输入信息以生成标记。

1. （如有必要）生成标记：

   1. 通过下列方式之一指定登陆页面，并在请求时提供站点链接或产品名称：

      * 通过输入完整路径和文件名或通过单击指定包含信息的文件 **[!UICONTROL Browse]** 在设备或网络上查找文件。 该文件必须是以制表符分隔的文本文件，每行有一个项目，格式如下：

         * （创意内容、标准广告） `**landing_page**`

            位置 `landing_page` 是有效的登陆页面URL或基本URL。

            示例： http://www.example.com/travel.html

         * ([!DNL Microsoft® Advertising] sitelinks) `sitelink <tab> ** <tab> landing_page`

            位置 `sitelink` 是站点链接名称和 `landing_page` 是有效的登陆页面URL或基本URL。

            示例： `Careers <tab> ** <tab> http://www.example.com/careers.html`

            该文件最多可包含10,000行。

         * ([!DNL Google Merchant Center] 产品组和 [Microsoft® Advertising] 产品广告) `product name <tab> ** <tab> landing_page`

            位置 `product name` 是产品名称和 `landing_page` 是有效的登陆页面URL或基本URL。

            示例： `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

            该文件最多可包含10,000行。
      * 在输入字段中，按照以下格式每行输入一个项目：

         * （创意内容、标准广告） `landing_page`

            位置 `landing_page` 是有效的登陆页面URL或基本URL。

            示例： http://www.example.com/travel.html

         * ([!DNL Microsoft® Advertising] sitelinks) `sitelink**landing_page`

            位置 `sitelink` 是站点链接名称和 `landing_page` 是有效的登陆页面URL或基本URL。

            示例： `Careers**http://www.example.com/careers.html`

         * ([!DNL Google Merchant Center] 产品组和 [!DNL Microsoft® Advertising] 产品广告) `product name**landing_page`

            位置 `product name` 是产品名称和 `landing_page` 是有效的登陆页面URL或基本URL。

            示例： Acme PR208**http://www.example.com/travel.html
   1. 单击 **[!UICONTROL Generate Tracking URLs]**.



1. （可选）从屏幕或输出页面复制URL（以“http”或“https”开头），并在搜索或社交帐户中实施它们。

对于具有目标URL的帐户，请在相应的 [!UICONTROL Base URL] 字段。

对于具有最终URL的帐户，请在相应的字段中输入屏幕上的值 [!UICONTROL Tracking Template] 字段。 您必须在之后为最终URL添加参数 `&url=` 参数(例如 `{lpurl}`)。 对象 [!DNL Yahoo! Japan Ads] 帐户，使用参数 `{lpurl}`. 对于列表 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 参数指示跟踪模板中的最终URL，请参阅 [[!DNL Google Ads] 文档](https://support.google.com/google-ads/answer/6305348) （请参阅“可用ValueTrack参数”一节中的“仅跟踪模板”参数）以及 [[!DNL Microsoft® Advertising] 文档](https://help.ads.microsoft.com/#apex/3/en/56799/2).

>[!MORELIKETHIS]
>
>* [关于创建和解码跟踪标记的工具](tracking-tools-about.md)
>* [何时以及如何生成点击跟踪URL](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [解码搜索、社交和商务点击跟踪URL](click-tracking-url-decode.md)

