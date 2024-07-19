---
title: 投放位置级别预竞价过滤器及其使用方式
description: 引用可用的投放位置级别预竞价过滤器，并了解如何使用它们。
feature: DSP Optimization
exl-id: 34a15666-7ca2-416d-9064-8638ca81e5b3
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# 投放位置级别预竞价过滤器及其使用方式

| 预竞价筛选器 | 描述 | 何时使用此过滤器 |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | 设置拍卖可能导致点进的概率的最小预测阈值。 例如，如果将阈值设置为0.1%，则只有在预测的点击概率大于或等于0.1%时才对拍卖投标。<br><br><b>注意：</b>筛选器在优化目标之前应用。 因此，非常严格的筛选条件可以防止支出。 | 当您的点进率(CTR)具有最低KPI目标，并且当CTR低于阈值时您不希望花费预算时使用。 此过滤器可能比较严格，因此设置现实的目标很重要。 根据对投放位置的其他限制，目标为0.03%到0.07%通常是一个良好的起点。 您可以根据需要在网站级别优化此项以帮助改进量度。<br><br>如果您的目标是实现最小的CTR和最佳的CPM，则推荐的设置是将[!UICONTROL Click Through Rate]筛选器与优化目标“[!UICONTROL Lowest CPM]”相结合。 如果您的目标是最大CPM，而没有实现过度目标的实际好处，以及最小CTR，则将[!UICONTROL Click Through Rate]筛选器与优化目标“[!UICONTROL Always Max Bid + Highest CTR]”配对可能更合适。 |
| [!UICONTROL 100% Completion Rate] | 设置在对展示出价之前必须满足的必需最低完成率。 | 当营销活动的主要目标是完成率时，使用此过滤器。 其他定位参数中的系数，但建议起始百分比为65%。 |
| [!UICONTROL Player Size - Adobe] | 使用来自DSP的数据设置所需的最低播放器大小。 当满足[!UICONTROL Player Size]阈值时，您可以对展示出价。 | 使用确保您使用来自DSP的数据提供全集播放器库存。 |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | 使用来自[!DNL Moat]或[!DNL Integral Ad Science] ([!DNL IAS])的数据设置所需的最小播放器大小。 当满足[!UICONTROL Player Size]阈值时，您可以对展示出价。 | 用于确保您使用平台范围的[!DNL Moat]或[!DNL IAS]数据提供全集播放器库存。<br><br><b>注意：</b>仅当营销活动配置为使用[!DNL Moat]或[!DNL IAS]数据时才使用此筛选器。 |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | 使用DSP可视性数字和度量设置所需的最小可视性百分比。 当满足指定的阈值时，您可以对展示出价。<br><br><b>注释：</b><ul><li>如果营销活动的[!UICONTROL Viewability Sensitivity]设置为“[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]”，则将[!DNL Media Rating Council] (MRC)可见性度量标准用于该营销活动。 如果[!UICONTROL Viewability Sensitivity]设置是“[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]”，则将[!DNL GroupM]可见性度量标准用于该营销活动。</li><li>Adobe测量定义与第三方定义不同，因此可能与第三方数据略有差异。</li></ul> | 最佳实践是将优化目标和任何预竞价筛选器设置与促销活动的[!UICONTROL Viewability Sensitivity]设置相匹配。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [DSP如何优化您的营销活动](optimization-how-dsp-optimizes-campaigns.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
>* [位置设置](/help/dsp/campaign-management/placements/placement-settings.md)
>* [营销活动设置](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [优化目标及其使用方式](optimization-goals.md)
