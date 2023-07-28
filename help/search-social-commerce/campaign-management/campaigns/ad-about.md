---
title: 管理广告
description: 了解Search、Social和Commerce中的广告，包括可用的广告类型。
exl-id: 92ae631a-c35a-40ec-9d40-ebce13e3311b
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 0%

---

# 关于广告

*[!DNL Baidu]， [!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan Ads]、和 [!DNL Yandex] 仅限帐户*

广告可以显示在目标网站上（针对内容或针对版面的促销活动）；当用户搜索广告组中的某个关键字（针对搜索促销活动）或搜索您网站上的内容时（针对中的动态搜索广告） [!DNL Google Ads] （仅限搜索的市场活动）；或者用户执行与您的项目之一相关的搜索时， [!DNL Google Merchant Center] 或 [!DNL Microsoft® Merchant Center] 产品信息源（购物广告） [!DNL Google Ads] 或产品广告位于 [!DNL Microsoft® Advertising] 营销活动)。

## 可用广告类型

您可以在同步的广告网络帐户中创建和管理广告组支持的广告类型：

* **文本广告或扩展的文本广告** 适用于营销活动中定位搜索网络的广告组。 文本广告可以包含覆盖广告组或营销活动级别参数的可选跟踪参数。 根据广告网络，您可以创建扩展/扩展文字广告或标准文字广告。

* 跨设备，本机 **受众广告** 对象 [!DNL Microsoft® Advertising] 上的营销活动 [!DNL Microsoft® Audience Network]. 根据促销活动设置，您有两个受众广告选项：

   * 如果促销活动链接到商户中心商店，则让广告网络使用商店的产品信息，自动为促销活动生成基于广告馈送的广告。 您无需为营销活动创建基于信息源的广告，但必须创建具有用户定位的广告组。

   * 如果促销活动未链接到商家中心帐户，则使用响应式广告格式创建基于图像的受众广告，其中包含多个文本和图像资源。 广告网络使用最有效的广告元素组合来组合广告，并在之类的网站上显示它们 [!DNL MSN]， [!DNL Outlook.com]、和 [!DNL Microsoft® Edge].

* **仅限呼叫的广告** 对象 [!DNL Google Ads] 搜索网络上的营销活动。 仅限呼叫的广告是包含电话号码的文字广告。 您可以选择使用 [!DNL Google Ads] — 为高级呼叫报告分配了转接号码。

* **扩展的动态搜索广告** （现在在广告网络上称为“动态搜索广告”） [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 搜索营销活动中的动态搜索广告组。 动态搜索广告使用网站中的内容而不是关键字来确定何时显示广告。 广告网络动态生成标题，选择登陆页面URL和显示URL，并自动生成最终URL。

  您可以通过为广告组设置特定的动态搜索目标，在网站中定义其内容用于定位动态搜索广告的页面。 对象 [!DNL Google Ads]，您可以在Search、Social和Commerce中创建动态搜索目标； [!DNL Microsoft® Advertising]，您必须在中创建它们 [!DNL Microsoft® Advertising]. 在 [!DNL Google Ads] 营销活动，您可以选择在营销活动的“ ”中指定网站域和语言[!DNL DSA Options]”部分，而不是创建动态搜索目标，或者是在创建动态搜索目标之外的部分。

  当用户的搜索词与您基于关键词的营销活动中的某个关键词完全匹配时，将显示来自基于关键词的营销活动的广告，而不是动态搜索广告。 当用户搜索词广泛匹配或与您的某个关键字匹配的短语并且动态搜索广告的广告排名较高时，广告网络会显示动态搜索广告而不是以关键字为目标的广告。

  有关动态搜索广告的更多信息，请参阅 [[!DNL Google Ads] 文档](https://support.google.com/google-ads/answer/2471185) 和 [[!DNL Microsoft® Advertising] 文档](https://help.ads.microsoft.com/#apex/ads/en/56794).

* **多媒体广告** 对象 [!DNL Microsoft® Advertising] 搜索营销活动。 多媒体广告是以突出的主线和侧栏位置显示的大型图像广告，并且每页只显示一个多媒体广告。 它们可以包括多个文本和图像资产，例如响应式广告，并且广告网络使用最有效的广告元素组合来组合广告。 多媒体广告不会取代文本广告投放。

* 促销行 **[!DNL Microsoft® Advertising]产品（购物）广告** 在购物网上。 购物广告会使用您现有的产品 [!DNL Microsoft® Merchant Center] 由产品信息源（而不是关键字）决定显示广告的方式和位置。 广告文案和登陆页面URL是根据信息源中的产品信息自动生成的，但是，您可以选择设置促销行以将其包含在广告组中。

  您可以控制哪些产品与一起显示 [!DNL Microsoft® Advertising] 通过为广告组设置单独的产品组，从 [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] 视图。

  有关产品/购物广告工作流的更多信息，请参阅&quot;[实施 [!DNL Microsoft® Advertising] 购物营销活动](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)“  有关产品广告的其他信息，请参阅 [Microsoft® Advertising文档](https://help.ads.microsoft.com/#apex/3/en/51082).

* 的响应式搜索广告 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 搜索网络上的营销活动。 该广告网络动态地组合来自一组广告标题和描述的基于文本的响应式搜索广告，从而有利于共同表现良好的组合。 广告最多包含三个标题、两个描述，以及来自基本URL和可选path1和path2字段的可自定义URL。 您可以选择将广告标题和说明固定到特定职位。

>[!NOTE]
>
>[!DNL Google Ads] 请勿在其本机编辑器之外提供显示为广告的文本组合的数据。 有关每个文本组合报表的更多信息，请参阅 [Google Ads文档](https://support.google.com/google-ads/answer/7684791).

## 此 [!UICONTROL Ads] 视图

您可以从创建、编辑和更改广告状态 [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads] 视图。

## 广告级别的效果数据

广告级别的数据适用于大多数广告类型。

但是，它不适用于 [!DNL Google Ads] 动态搜索广告(DSA)、最佳性能、智能购物和 [!DNL YouTube] 营销活动。 预计营销活动的广告级别数据总数与营销活动数据总数之间存在差异。

| 广告网络/营销活动/广告类型 | 数据可用性 |
|---|---|
| [!DNL Google Ads] 动态搜索广告(DSA) | 营销活动、广告组 |
| [!DNL Google Ads] 最高性能 | 营销活动 |
| [!DNL Google Ads] 购物，智能购物 | 营销活动、广告组 |
| [!DNL Google Ads] [!DNL YouTube] | 营销活动、广告组 |

>[!MORELIKETHIS]
>
>* [管理广告](ad-manage.md)
