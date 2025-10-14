---
title: 为什么渠道数据在Adobe Advertising和 [!DNL Marketing Channels]之间可能不同
description: 了解AMO ID跟踪的渠道数据为何与 [!DNL Analytics Marketing Channels]跟踪的渠道数据不同。
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# 为什么渠道数据在Adobe Advertising和[!DNL Marketing Channels]之间可能不同

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

用户了解Adobe Advertising与[!DNL Marketing Channels]数据集集成的常见问题是“什么原因导致AMO ID与[!DNL Marketing Channels]之间的数据差异？” 或者，有时候，“为什么数据会中断？ 我需要所有指标在报表中保持一致。” 幸运的是，差异并不表明数据“失灵”，而是可以预期，甚至可以预期。 让我们看一下为什么该集成是按这种方式设计的。

这两个数据集的主要用例不同：

* [!DNL Marketing Channels]： [!DNL Marketing Channels]的主要用例是将多个渠道中的数据与通用归因模型进行比较。 分析人员可以使用[!UICONTROL Marketing Channel]维度增加对渠道之间交互方式的洞察。 此洞察信息有助于促进宏观层面上有关如何投资于每个渠道的决策，并可引导深入了解每个渠道的访客如何与网站进行互动。

  因此，[!DNL Analytics] [!UICONTROL Marketing Channel]维度配置为捕获和跟踪所有渠道。 [!DNL Marketing Channels]还可以配置为捕获Advertising DSP显示到达和点进，并且它与其他营销渠道之间存在关联。

* Adobe AdvertisingAMO ID：Adobe AdvertisingAMO ID数据的主要用例是提供高级[!DNL Adobe Sensei]支持的竞价算法。 算法每天自动作出数千个微观级别的竞价决策，以最大限度地增加广告支出并实现[!DNL DSP]促销活动或[!DNL Search, Social, & Commerce]产品组合的目标。 算法可以连接到营销活动的转化数据越多，算法就越能做出这些竞价决策。

  为了收集此数据，[!DNL Analytics for Advertising]集成传递原始AMO ID，这些原始AMO ID可以转换为Adobe Analytics的AMO ID维度中的点进和浏览跟踪代码，该AMO ID维度存储为自定义变量(eVar)或保留变量(rVar)。 由于AMO ID维度中未设置其他渠道的点进次数，因此AMO ID维度无法跟踪来自这些其他渠道的进入。 结果是AMO ID将持续存在[!DNL Marketing Channels]个入口点。

有关Adobe Advertising跟踪的数据和[!DNL Analytics]跟踪的数据之间可能的数据差异的更多信息，请参阅“[介于 [!DNL Analytics] 和Adobe Advertising](../data-variances.md)之间的预期数据差异”。

>[!MORELIKETHIS]
>
>* [在 [!DNL Analytics] 和Adobe Advertising](/help/integrations/analytics/data-variances.md)之间的预期数据差异
>*  [!DNL Analytics Marketing Channels][&#128279;](mc-overview.md)的基础知识
>* [使用Adobe AdvertisingID创建 [!DNL Marketing Channels] 处理规则](mc-ids.md)
>* [对Adobe Advertising数据使用 [!DNL Analytics Marketing Channels] &#x200B;](mc-ac-data.md)
>* [视频：使用 [!DNL Marketing Channels] 进行Adobe Advertising报告](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=zh-Hans)
