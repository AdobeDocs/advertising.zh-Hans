---
title: 将 [!DNL Marketing Channels] 用于Adobe Advertising数据
description: 了解如何在 [!DNL Analytics Marketing Channels]中使用Adobe Advertising数据。
feature: Integration with Adobe Analytics
exl-id: 522c7f01-1138-477d-8018-36030caab55e
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# 将[!DNL Analytics Marketing Channels]用于Adobe Advertising数据

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

通过使用Adobe Advertising和[!DNL Analytics Marketing Channels]报表，您可以获得关于数字媒体如何影响网站活动的宝贵见解。

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

下图显示了Adobe Advertising和[!DNL Marketing Channels]如何跟踪构成一个访客历程的单独访问。 [!DNL Analytics]中的Adobe Advertising报表仅限于使用AMO ID通过Adobe Advertising进行交易的付费显示、搜索、社交和商业渠道广告。 但是，[!DNL Marketing Channels]跟踪在[!DNL Marketing Channels]处理规则中配置的所有渠道。

![Adobe Advertising和[!DNL Marketing Channels]如何跟踪访客历程中的个人访问](/help/integrations/assets/a4adc-mc-sample-journey2.png)

在首次访问中，用户通过电子邮件营销活动进入网站，执行了10次页面查看，然后离开。 在第二次访问中，用户通过显示广告进入网站，执行了10次页面查看，然后离开。 在第三次访问中，用户通过免费搜索进入网站，执行了5次页面查看，执行了$250的转换，最后是左侧访问。 注意[!DNL Marketing Channels]与Adobe Advertising之间的跟踪差异。 Adobe Advertising在此历程中跟踪的唯一渠道是[!UICONTROL Display]。 Adobe Advertising跟踪[!UICONTROL Display]渠道访问，并将后续参与数据（如页面查看次数）和转化归因于该广告的影响。 [!DNL Marketing Channels]则提供所有渠道的完整视图。

由于AMO ID会在访客的历程中持续存在，因此您可以使用AMO ID数据来了解Adobe Advertising如何影响其他营销渠道。 默认情况下，AMO ID [会保留60天](/help/integrations/analytics/overview.md)，但您可以根据需要配置持久性。

## 如何结合Adobe Advertising和营销渠道数据来分析媒体效果

在[!DNL Analytics]内，您可以将保留付费广告数据的Adobe Advertising与[!DNL Marketing Channels]综合访问数据相结合，更好地分析您的媒体效果，从而更好地影响客户历程。

以下分析使用Adobe Advertising数据显示了各种版本的显示广告如何影响网站转化。 这三列使用的转化量度相同，但每列的情况却有所不同：

* 列1查看访客历程中持续保留的AMO ID数据。 列1表示641应用程序启动一度通过浏览或点进事件与Adobe Advertising广告链接。 此视图不考虑任何其他[!DNL Marketing Channels]归因。

* 但是，在[!DNL Marketing Channels]数据集中，641应用程序启动将归因于其他营销渠道。 最后两列采用“641应用程序启动”并将数据限制为[!UICONTROL Display Click-Through]和[!UICONTROL Display View-Through]渠道，显示最后接触归因模型中发生的转化。

![显示广告如何影响网站转化示例](/help/integrations/assets/a4adc-mc-display-impact.png)

您可以进一步分析此内容。 您可以进一步按营销渠道细分Adobe Advertising行，以查看Adobe Advertising转化在哪里归因于641应用程序启动。 您已经知道，其中5次转化归属于最后接触显示点进，19次归属于最后接触显示显示显示点进。 尽管如此，仍有617项应用程序开始归因于其他营销渠道。 您可以将“最近联系渠道”维度拖放到Advertising DSP行项目的顶部，以显示其余应用程序启动的渠道归因，并显示显示渠道的跨渠道影响。

![如何添加最近联系渠道维度](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

现在，您可以查看其余应用程序启动次数的归因。 电子邮件获得357个保持有AMO ID的最近联系申请开始的点数。 通过这种类型的分析，您可以了解Adobe Advertising展示广告对所有渠道的影响。 由于只有一个数据集和归因模型，因此这种类型的分析将不可用。

显示渠道的跨渠道影响示例![](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

您可以使用设置为“100%栈叠”的栈栈图来显示一段时间内的趋势数据，从而进一步改进分析。 此可视化图表使得更容易监测哪些最近联系营销渠道受展示营销活动的影响更大。

显示渠道的趋势性跨渠道影响的![示例](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>*  [!DNL Analytics Marketing Channels][&#128279;](mc-overview.md)的基础知识
>* [使用Adobe AdvertisingID创建 [!DNL Marketing Channels] 处理规则](mc-ids.md)
>* [为什么渠道数据在Adobe Advertising和 [!DNL Marketing Channels]](mc-data-variances.md)之间可能不同
>* [视频：使用 [!DNL Marketing Channels] 进行Adobe Advertising报告](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=zh-Hans)
>* [概述 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
