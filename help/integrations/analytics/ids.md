---
title: ' [!DNL Analytics]使用的Adobe Advertising ID'
description: ' [!DNL Analytics]使用的Adobe Advertising ID'
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: d1e2e92532b1f930420436c66c687676a2b7de6a
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 0%

---

# [!DNL Analytics]使用的Adobe Advertising ID

*仅集成Adobe Advertising-Adobe Analytics的广告商*

*适用于Advertising DSP和[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising使用两个ID进行现场性能跟踪： *EF ID*&#x200B;和&#x200B;*AMO ID*。

当出现广告展示时，Adobe Advertising会创建AMO ID和EF ID值并将其存储。 当看到广告的访客进入网站而未单击广告时，[!DNL Analytics]通过[!DNL Analytics for Advertising] JavaScript代码从Adobe Advertising调用这些值。 对于浏览流量，[!DNL Analytics]生成一个补充ID (`SDID`)，用于将EF ID和AMO ID拼合到[!DNL Analytics]中。 对于点进流量，这些ID将使用`ef_id`和`s_kwcid`（对于AMO ID）查询字符串参数包含在登陆页面URL中。

Adobe Advertising会使用以下标准来区分网站的点进或浏览条目：

* 当用户查看了广告但未单击该广告后访问网站时，将会捕获浏览进入条目。 如果满足两个条件，[!DNL Analytics]记录一次浏览：

   * 在[!DNL DSP]点击回顾窗口[!DNL Search, Social, & Commerce]期间，访客没有[或](/help/integrations/analytics/prerequisites.md#lookback-a4adc)广告的点进次数。

   * 在[!DNL DSP]展示回顾窗口[期间，访客已看到至少一个](/help/integrations/analytics/prerequisites.md#lookback-a4adc)广告。 最后一次展示作为显示到达传递。

* 当网站访客在进入网站之前单击广告时，将捕获点进条目。 出现以下任一情况时，[!DNL Analytics]会捕获点进：

   * 该URL包含由Adobe Advertising添加到登陆页面URL的EF ID和AMO ID。

   * URL不包含跟踪代码，但Adobe Advertising JavaScript代码可检测过去两分钟内发生的点击。

![Adobe Advertising基于视图的[!DNL Analytics]集成](/help/integrations/assets/a4adc-view-through-process.png)

*图1：基于Adobe Advertising视图的[!DNL Analytics]集成*

![Adobe Advertising单击基于URL的[!DNL Analytics]集成](/help/integrations/assets/a4adc-click-through-process.png)

*图2： Adobe Advertising单击基于URL的[!DNL Analytics]集成*

## ADOBE ADVERTISING EF ID

{{$include /help/_includes/ef-id.md}}

### EF ID格式 {#ef-id-formats}

{{$include /help/_includes/ef-id-formats.md}}

### [!DNL Analytics]中的EF ID Dimension

在[!DNL Analytics]报表中，您可以通过搜索[!UICONTROL EF ID]维度并使用[!UICONTROL EF ID Instance]量度来查找EF ID数据。

EF ID受Analysis Workspace中500,000个唯一标识符限制的约束。 一旦达到500k值，所有新跟踪代码都会报告在单行项目标题“[!UICONTROL Low Traffic]”下。 由于可能缺少报表保真度，EF ID不会进行分类，您不应将它们用于[!DNL Analytics]中的区段或报表。

## ADOBE ADVERTISING AMO ID {#amo-id}

{{$include /help/_includes/amo-id.md}}

## AMO ID格式 {#amo-id-formats}

{{$include /help/_includes/amo-id.md}}

### 实施AMO ID的方法 {#amo-id-implement}

参数可通过以下方式之一添加到您的跟踪URL中：

* （推荐）实施服务器端插入功能时。

   * DSP客户：当最终用户查看带有Adobe Advertising像素的显示广告时，像素服务器会自动将s_kwcid参数附加到您的登陆页后缀。

   * 搜索、社交和Commerce客户：

      * 对于已为帐户或营销活动启用[!DNL Google Ads]设置的[!DNL Microsoft Advertising]和[!UICONTROL Auto Upload]帐户，当最终用户单击带有Adobe Advertising像素的广告时，像素服务器会自动将s_kwcid参数附加到您的登陆页后缀。

      * 对于其他广告网络，或禁用了[!DNL Google Ads]设置的[!DNL Microsoft Advertising]和[!UICONTROL Auto Upload]帐户，请手动将该参数添加到您的[帐户级别的附加参数](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}，这些参数会将其附加到您的基本URL。

* 未实施服务器端插入功能时：

   * DSP客户： [JavaScript代码](javascript.md)会自动记录点进和显示点进。 当浏览器不支持第三方Cookie时，您仍然可以跟踪以下广告类型的基于点击的转化：

      * 对于[!DNL Flashtalking]广告标记，请手动插入每个“[将 [!DNL Analytics for Advertising] 宏附加到 [!DNL Flashtalking] 广告标记](/help/integrations/analytics/macros-flashtalking.md)”的其他宏。 **注意：**&#x200B;如果您的组织与[!DNL Flashtalking]直接合作，并且您根据`s_kwcid`支持文档(位于`ef_id`https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros[!DNL Flashtalking])使用数据传递宏跟踪[和](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros)跟踪参数，则不需要执行此过程。

      * 对于[!DNL Google Campaign Manager 360]广告标记，请手动插入每个“[将 [!DNL Analytics for Advertising] 宏附加到 [!DNL Google Campaign Manager 360] 广告标记](/help/integrations/analytics/macros-google-campaign-manager.md)”的其他宏。

   * 搜索、社交和Commerce客户：

      * 对于（[!DNL Google Ads]和[!DNL Microsoft Advertising]）广告，请手动将AMO ID参数添加到登陆页面后缀，最好在[帐户级别](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}添加，除非需要对各个帐户组件进行不同的跟踪。

      * 对于所有其他广告网络上的广告，请手动将AMO ID参数添加到您的[帐户级别的附加参数](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}，这会将其附加到您的基本URL。

要实施服务器端插入功能或确定最适合您的企业的选项，请联系您的Adobe客户团队。

### [!DNL Analytics]中的AMO ID Dimension

在Analytics报表中，您可以通过搜索[!UICONTROL AMO ID]维度并使用[!UICONTROL AMO ID Instances]量度来查找AMO ID数据。 [!UICONTROL AMO ID]维度包含捕获的所有AMO ID值，而[!UICONTROL AMO ID Instances]量度表示网站捕获AMO ID值的频率。 例如，如果同一搜索广告被点击四次，但Analytics跟踪了七个网站条目，则[!UICONTROL AMO ID Instances]将是七(7)，[!UICONTROL Clicks]将是四(4)。

对于[!DNL Analytics]内的任何报表或审核，最佳实践是将AMO ID与其相应的实例结合使用。 有关详细信息，请参阅“在[和Adobe Advertising之间的预期数据差异”中的“ [!DNL Analytics for Advertising]](data-variances.md#data-validation)针对[!DNL Analytics]的点进数据验证”。

## 关于Analytics分类

在[!DNL Analytics]中，[分类](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html)是给定跟踪代码（如帐户、促销活动或广告）的元数据。 Adobe Advertising使用分类对原始Adobe Advertising数据进行分类，以便在生成报表时能够以不同的方式（例如按广告类型或促销活动）显示数据。 分类构成了[!DNL Analytics]中Adobe Advertising报表的基础，可与AMO指标（如[!UICONTROL Adobe Advertising Cost]、[!UICONTROL Adobe Advertising Impressions]和[!UICONTROL AMO Clicks]）以及自定义和标准现场事件（如[!UICONTROL Visits]、[!UICONTROL Leads]、[!UICONTROL Orders]和[!UICONTROL Revenue]）一起使用。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [在 [!DNL Analytics] 和Adobe Advertising](data-variances.md)之间的预期数据差异
