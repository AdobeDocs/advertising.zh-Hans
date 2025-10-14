---
title: ' [!DNL Marketing Channels]的基础知识'
description: 了解 [!DNL Analytics for Advertising] 用户应了解的 [!DNL Analytics Marketing Channels] 的关键信息。
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
source-git-commit: 29b49e8fa54580d7cdd62f9a10fd2616def4694b
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---

# [!DNL Analytics Marketing Channels]的基础知识

本页介绍[!DNL Analytics for Advertising]用户需要了解的有关[!DNL Analytics Marketing Channels]的关键信息。

有关[!DNL Marketing Channels]的完整文档，请参阅“[开始使用 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html?lang=zh-Hans)”。

## [!DNL Marketing Channels]概述

[!DNL Marketing Channels]是Adobe Analytics的关键功能。 [!DNL Marketing Channels]报表显示客户如何通过报表窗口到达您的网站，以及每个渠道如何影响收入或网站行为。

请考虑以下跨访问历程示例。 对您网站的每次访问都由访客从中输入的营销渠道指示。 首次访问（也称为首次接触渠道）是电子邮件。 “访问时显示2”是参与渠道，“免费搜索”被视为最后接触渠道。 如果您在[!UICONTROL Attribution IQ]内使用[!UICONTROL Last Touch Attribution]，免费搜索将获得$250转化事件的完整点数。 使用Experience CloudID服务，您可以将这些单独的访问捆绑在一起，以便按单个访客展示一个历程。

![营销渠道中的跨访问转化历程示例](/help/integrations/assets/a4adc-mc-sample-journey.png)

通过使用[!UICONTROL Marketing Channels]处理规则，您可以创建逻辑集来确定产生流量的渠道并在用户访问您的网站时跟踪每个渠道。 例如，[!UICONTROL Email]渠道将由单击时生成的唯一跟踪代码指示，在由Adobe Analytics记录时，该代码会将访问分类为源自电子邮件营销活动。

## 处理规则以及如何设置营销渠道

每次用户访问网站时，都会通过他们单击或直接在地址栏中键入的URL来访问。 当用户进入网站时，[!DNL Analytics]跟踪可用于确定促成访问的渠道的信息。

营销人员通常会向渠道URL附加查询字符串参数跟踪代码，以帮助跟踪渠道对其网站的影响。 您可以将[!DNL Marketing Channels]处理规则配置为侦听特定跟踪参数和值，以确定渠道，而无需任何其他跟踪。 例如，如果所有电子邮件促销活动URL都遵循格式`www.adobe.com?cid=email…`（其中URL包含查询字符串参数和值`cid=email`），则可以创建一个规则来侦听此跟踪代码并在[!UICONTROL Email]渠道中存储访问。

其他渠道没有可跟踪的URL路径，需要进一步逻辑进行识别。 例如，[!UICONTROL Earned Social]是一个要跟踪的重要渠道，在该渠道中，用户单击了另一个用户在社交网络上有机共享的链接。 但是，营销人员无法将查询字符串参数跟踪代码附加到共享的URL。 在这种情况下，您可以创建一个处理规则来侦听感兴趣的社交网络的反向链接域以及不存在用于确定渠道的付费跟踪代码。 然后，符合这些要求的访问将在“营销渠道”报表中跟踪为“已习得社交”。

Adobe建议与您的Analytics团队合作，构建一整套[!DNL Marketing Channels]处理规则，以跟踪与您的业务相关的所有渠道。 这样做可让您创建强大的归因报表。

要了解Adobe Advertising如何贡献创建自定义营销渠道所需的信号，请参阅&quot;[使用Advertising ID创建 [!DNL Marketing Channels] 规则](mc-ids.md)&quot;。

>[!MORELIKETHIS]
>
>* [使用Adobe AdvertisingID创建 [!DNL Marketing Channels] 处理规则](mc-ids.md)
>* [为什么渠道数据在Adobe Advertising和 [!DNL Marketing Channels]](mc-data-variances.md)之间可能不同
>* [对Adobe Advertising数据使用 [!DNL Analytics Marketing Channels] &#x200B;](mc-ac-data.md)
>* [视频：使用 [!DNL Marketing Channels] 进行Adobe Advertising报告](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=zh-Hans)
>* [概述 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
