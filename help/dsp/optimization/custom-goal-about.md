---
title: 关于自定义目标
description: 了解自定义目标，以定义针对最低CPA或最高ROAS优化的包中的成功事件。
feature: DSP Optimization
exl-id: 806450b9-ce32-4f5c-a2ac-ba8e435ce36d
source-git-commit: 6aa81fe4fd5ea6cb188b7f18b1574c26ddfcbb92
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# 关于自定义目标

自定义目标定义广告商实现其业务目标所需的成功事件。 每个使用优化目标的包»[!UICONTROL Highest Return on Ad Spend (ROAS)"] 或&quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]”必须包括有助于实现整体优化目标的自定义目标。 您可以创建自定义目标作为 *目标* 在 [!DNL Advertising Search, Social, & Commerce].

![自定义目标](/help/dsp/assets/objective-goals.png)

每个自定义目标由一个或多个转化量度以及这些量度的相对权重组成。 可用的转化量度包括使用Adobe Advertising转化像素并通过Adobe Analytics跟踪的所有量度。

>[!NOTE]
>
>* [!DNL Analytics] 维度和区段不可用于Adobe Advertising优化。
>* 要在DSP中使用Analytics事件，请与您的Adobe客户团队合作来配置广告商级别的集成。
>* [!DNL Analytics] 自定义事件遵循以下命名约定： `custom_event_[*event #*]_[*Analytics report suite ID*]`. 示例： `custom_event_16_examplersid`

例如，假设三个转化指标与某个促销活动中的特定包相关：价值20美元的“PDF下载”、价值30美元的“电子邮件注册”和价值40美元的“订单确认”。 如果要根据客户操作的一次性货币值来赋予权重，则属性的相对权重为1、2和1.5。

请参阅 [创建自定义目标的最佳实践](custom-goal-best-practices.md) 以获取有关如何配置自定义目标的提示。

一旦您 [创建自定义目标](custom-goal-create.md)，您可以 [将其分配给资源包](/help/dsp/campaign-management/packages/package-settings.md) 以使用Adobe Sensei优化报表和算法。

>[!MORELIKETHIS]
>
>* [创建自定义目标](custom-goal-create.md)
>* [构建自定义目标的最佳实践](custom-goal-best-practices.md)
>* [优化目标及其使用方式](optimization-goals.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何优化活动](optimization-how-dsp-optimizes-campaigns.md)
