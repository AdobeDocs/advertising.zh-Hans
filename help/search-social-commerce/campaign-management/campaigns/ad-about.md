---
title: 管理广告
description: 了解Search、Social和Commerce中的广告，包括可用的广告类型。
exl-id: 01bd211d-fe6b-4329-90e1-0e54d626c125
feature: Search Campaign Management
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# 关于广告

仅&#x200B;*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads]、[!DNL Yandex]和现有[!DNL Baidu]帐户*

广告可以显示在目标网站上（针对内容或针对版面的促销活动）；用户搜索广告组中的关键字之一（针对搜索促销活动）或搜索您网站上的内容时（针对[!DNL Google Ads]仅限搜索促销活动的动态搜索广告）；或者用户执行与您的[!DNL Google Merchant Center]或[!DNL Microsoft Merchant Center]产品信息源中的项目之一相关的搜索时（针对[!DNL Google Ads]中的购物广告或[!DNL Microsoft Advertising]促销活动中的产品广告）。

## 可用广告类型

您可以在同步的广告网络帐户中创建和管理广告组支持的广告类型：

* 在针对搜索网络的营销活动中针对广告组&#x200B;**文本广告或扩展文本广告**。 文本广告可以包含覆盖广告组或营销活动级别参数的可选跟踪参数。 根据广告网络，您可以创建扩展/扩展文字广告或标准文字广告。

* 针对[!DNL Microsoft Audience Network]上[!DNL Microsoft Advertising]营销活动的跨设备、本机&#x200B;**受众广告**。 根据促销活动设置，您有两个受众广告选项：

   * 如果促销活动链接到商户中心商店，则让广告网络使用商店的产品信息，自动为促销活动生成基于广告馈送的广告。 您无需为营销活动创建基于信息源的广告，但必须创建具有用户定位的广告组。

   * 如果促销活动未链接到商家中心帐户，则使用响应式广告格式创建基于图像的受众广告，其中包含多个文本和图像资源。 广告网络使用最有效的广告元素组合来组合广告，并在[!DNL MSN]、[!DNL Outlook.com]和[!DNL Microsoft Edge]等网站上显示它们。

* 搜索网络上[!DNL Google Ads]促销活动的&#x200B;**仅限呼叫的广告**。 仅限呼叫的广告是包含电话号码的文字广告。 您可以选择使用[!DNL Google Ads]分配的转接号码进行高级呼叫报告。

* 在搜索促销活动中&#x200B;**扩展了[!DNL Google Ads]和[!DNL Microsoft Advertising]动态搜索广告组的动态搜索广告**（现在在广告网络上仅称为“动态搜索广告”）。 动态搜索广告使用网站中的内容而不是关键字来确定何时显示广告。 广告网络动态生成标题，选择登陆页面URL和显示URL，并自动生成最终URL。

  您可以通过为广告组设置特定的动态搜索目标，在网站中定义其内容用于定位动态搜索广告的页面。 对于[!DNL Google Ads]，您可以在Search、Social和Commerce中创建动态搜索目标；对于[!DNL Microsoft Advertising]，您必须在[!DNL Microsoft Advertising]中创建它们。 在[!DNL Google Ads]个营销活动中，您可以选择在营销活动的“[!DNL DSA Options]”部分指定网站域和语言，而不是在创建动态搜索目标时指定，或者作为创建动态搜索目标的补充。

  当用户的搜索词与您基于关键词的营销活动中的某个关键词完全匹配时，将显示来自基于关键词的营销活动的广告，而不是动态搜索广告。 当用户搜索词广泛匹配或与您的某个关键字匹配的短语并且动态搜索广告的广告排名较高时，广告网络会显示动态搜索广告而不是以关键字为目标的广告。

  有关动态搜索广告的更多信息，请参阅[[!DNL Google Ads] 文档](https://support.google.com/google-ads/answer/2471185)和[[!DNL Microsoft Advertising] 文档](https://help.ads.microsoft.com/#apex/ads/en/56794)。

* 针对[!DNL Microsoft Advertising]搜索营销活动的&#x200B;**多媒体广告**。 多媒体广告是以突出的主线和侧栏位置显示的大型图像广告，并且每页只显示一个多媒体广告。 它们可以包括多个文本和图像资产，例如响应式广告，并且广告网络使用最有效的广告元素组合来组合广告。 多媒体广告不会取代文本广告投放。

* 购物网络上&#x200B;**[!DNL Microsoft Advertising]产品（购物）广告**&#x200B;的促销行。 购物广告使用您现有的[!DNL Microsoft Merchant Center]产品信息源中的产品（而不是关键字）来确定显示广告的方式和位置。 广告文案和登陆页面URL是根据信息源中的产品信息自动生成的，但是，您可以选择设置促销行以将其包含在广告组中。

  通过从[!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups]视图为广告组设置单独的产品组，您可以控制哪些产品与您的[!DNL Microsoft Advertising]购物广告一起显示。

  有关产品/购物广告工作流的详细信息，请参阅[实施 [!DNL Microsoft Advertising] 购物营销活动](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)。  有关产品广告的其他信息，请参阅[Microsoft Advertising文档](https://help.ads.microsoft.com/#apex/3/en/51082)。

* 搜索网络中[!DNL Google Ads]和[!DNL Microsoft Advertising]营销活动的响应式搜索广告。 该广告网络动态地组合来自一组广告标题和描述的基于文本的响应式搜索广告，从而有利于共同表现良好的组合。 广告最多包含三个标题、两个描述，以及来自基本URL和可选path1和path2字段的可自定义URL。 您可以选择将广告标题和说明固定到特定职位。

>[!NOTE]
>
>[!DNL Google Ads]不在其本机编辑器之外提供有关显示为广告的文本组合的数据。 有关每个文本组合报表的更多信息，请参阅[Google广告文档](https://support.google.com/google-ads/answer/7684791)。

## [!UICONTROL Ads]视图

您可以从[!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads]视图创建、编辑和更改广告状态。

## 广告级别的效果数据

广告级别的数据适用于大多数广告类型。

但是，它不适用于[!DNL Google Ads]动态搜索广告(DSA)、最佳效果、智能购物和[!DNL YouTube]营销活动。 预计营销活动的广告级别数据总数与营销活动数据总数之间存在差异。

| 广告网络/营销活动/广告类型 | 数据可用性 |
|---|---|
| [!DNL Google Ads]动态搜索广告(DSA) | 营销活动、广告组 |
| 最大[!DNL Google Ads]性能 | 营销活动 |
| [!DNL Google Ads]购物，智能购物 | 营销活动、广告组 |
| [!DNL Google Ads] [!DNL YouTube] | 营销活动、广告组 |

>[!MORELIKETHIS]
>
>* [管理广告](ad-manage.md)
