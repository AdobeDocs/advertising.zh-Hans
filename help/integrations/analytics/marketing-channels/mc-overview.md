---
title: 的基础知识 [!DNL Marketing Channels]
description: 了解关于以下内容的关键信息 [!DNL Analytics Marketing Channels] 该 [!DNL Analytics for Advertising] 用户应该理解。
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
source-git-commit: 29b49e8fa54580d7cdd62f9a10fd2616def4694b
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---

# 的基础知识 [!DNL Analytics Marketing Channels]

本页介绍有关以下内容的关键信息 [!DNL Analytics Marketing Channels] 该 [!DNL Analytics for Advertising] 用户需要了解。

有关的完整文档 [!DNL Marketing Channels]，请参见&quot;[开始使用 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html)“

## 概述 [!DNL Marketing Channels]

[!DNL Marketing Channels] 是Adobe Analytics的一项关键功能。 [!DNL Marketing Channels] 报表显示客户如何通过报表窗口访问您的网站，以及每个渠道如何影响收入或网站行为。

请考虑以下跨访问历程示例。 对您网站的每次访问都由访客从中输入的营销渠道指示。 首次访问（也称为首次接触渠道）是电子邮件。 “访问时显示2”是参与渠道，“免费搜索”被视为最后接触渠道。 如果您使用 [!UICONTROL Last Touch Attribution] 范围 [!UICONTROL Attribution IQ]，免费搜索将获得250美元转化事件的完整点数。 使用Experience CloudID服务，您可以将这些单独的访问捆绑在一起，以便按单个访客展示一个历程。

![营销渠道中的跨访问转化历程示例](/help/integrations/assets/a4adc-mc-sample-journey.png)

通过使用 [!UICONTROL Marketing Channels] 对于处理规则，您可以创建一组逻辑来确定产生流量的渠道并在用户访问您的网站时跟踪每个渠道。 例如， [!UICONTROL Email] 渠道将由单击时生成的唯一跟踪代码指示，在由Adobe Analytics记录时，该代码会将访问分类为源自电子邮件营销活动。

## 处理规则以及如何设置营销渠道

每次用户访问网站时，都会通过他们单击或直接在地址栏中键入的URL来访问。 当用户进入网站时， [!DNL Analytics] 跟踪可用于确定导致访问的渠道的信息。

营销人员通常会向渠道URL附加查询字符串参数跟踪代码，以帮助跟踪渠道对其网站的影响。 您可以配置 [!DNL Marketing Channels] 处理规则，监听特定跟踪参数和值以确定渠道，而无需任何其他跟踪。 例如，如果所有电子邮件促销活动URL都遵循格式 `www.adobe.com?cid=email…` (其中，URL包含查询字符串参数和值 `cid=email`)，然后您可以创建一个规则来侦听此跟踪代码并在中存储访问 [!UICONTROL Email] 渠道。

其他渠道没有可跟踪的URL路径，需要进一步逻辑进行识别。 例如， [!UICONTROL Earned Social]（用户在其中单击另一个用户在社交网络上有机共享的链接）是重要的跟踪渠道。 但是，营销人员无法将查询字符串参数跟踪代码附加到共享的URL。 在这种情况下，您可以创建一个处理规则来侦听感兴趣的社交网络的反向链接域以及不存在用于确定渠道的付费跟踪代码。 然后，符合这些要求的访问将在“营销渠道”报表中跟踪为“已习得社交”。

Adobe建议与您的Analytics团队合作，构建一套 [!DNL Marketing Channels] 用于跟踪与您的业务相关的所有渠道的处理规则。 这样做可让您创建强大的归因报表。

要了解Adobe Advertising如何贡献创建自定义营销渠道所需的信号，请参阅&quot;[使用广告ID创建 [!DNL Marketing Channels] 规则](mc-ids.md)“

>[!MORELIKETHIS]
>
>* [使用Adobe AdvertisingID创建 [!DNL Marketing Channels] 处理规则](mc-ids.md)
>* [为什么渠道数据可能因Adobe Advertising和渠道而异 [!DNL Marketing Channels]](mc-data-variances.md)
>* [使用 [!DNL Analytics Marketing Channels] 包含Adobe Advertising数据](mc-ac-data.md)
>* [视频：使用 [!DNL Marketing Channels] 用于Adobe Advertising报表](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [概述 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
