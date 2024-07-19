---
title: 性能疑难解答
description: 参考常见的性能问题并了解如何对其进行故障诊断。
feature: DSP Optimization
exl-id: b87f8556-1908-40c1-9f98-fbdc6d9b59b1
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# 性能疑难解答

| 问题 | 可能的原因 | 要采取的操作 |
| --- | --- | --- |
| 投放无需花费 | 投放位置不包含广告，和/或广告无效。 | 验证所有预期的广告均已附加到投放位置并已批准和激活。<br><br>此外，查看投放位置是否包含自定义广告计划，这可能会限制每个广告的投放期限。 若要从“版面”视图中查看版面的广告计划，请单击版面名称旁边的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Ad schedule]**。 |
| | 受影响的日期不在配置的投放日期内。 | 检查投放日期在营销活动、包和投放级别&#x200B;是否有效。 |
| | 预算目标已实现和/或不够高。 | 检查营销活动、包和投放级别的预算设置。 |
| | 账户没有足够的资金。 | 要查看您的帐户是否资金充足，请转到&#x200B;**[!UICONTROL Settings]** > **[!UICONTROL Account]**&#x200B;并查看[!UICONTROL Usable Funds]的金额。 如果您需要添加更多基金，请与您的Adobe客户团队联系。 |
| | 没有可用的库存。 | 验证指定的清单源（[!UICONTROL Public]、[!UICONTROL Private]或[!UICONTROL On Demand]）是否为：<ul><li>正确设置。</li><li>激活并通过拍卖发送。</li><li>与适用的广告和投放类型兼容。</li></ul><br>如果清单来源全部有效且有效，则尽可能定位其他或所有清单来源。 |
| | 无可用用户。 | 检查指定的受众目标是否包含足够的活动用户。 如果没有，则通过添加更多受众来展开目标。 |
| 投放费用低 | 投放位置诊断报告的[!UICONTROL Non Bids]部分显示了投放位置未竞价的可能原因。 | [查看[!UICONTROL Non Bids]报表](/help/dsp/campaign-management/reports/placement-diagnostics.md)以了解投放位置未竞价的原因。 <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
| | 投放位置使用限制竞价的[预竞价筛选器](/help/dsp/campaign-management/placements/placement-settings.md)。 | 将预竞价筛选器的阈值降低5%，以评估支出和性能之间的平衡。 <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>请记住，使用多个投放位置目标（如预竞价筛选条件、地理位置、库存和受众）可能会累积限制竞价和支出。 |
| | 投放的获胜率很低。 | 增加[!UICONTROL Max Bid]以提高获胜率。<br><br><b>注意：</b>库存价格可能因投放位置的目标而有所不同。<br><br>10%的获胜率被认为是正常的。 |
| | 可用库存数量较少。 | 尽可能定位其他或所有库存来源。<br><br>请记住，使用多个投放位置目标（如预竞价筛选条件、地理位置、库存和受众）可能会累积限制竞价和支出。 |
| | 可用用户数较少。 | 检查指定的受众目标是否包含足够的活动用户。 如果没有，则通过添加更多受众来展开目标。<br><br>请记住，使用多个投放位置目标（如预竞价筛选条件、地理位置、库存和受众）可能会累积限制竞价和支出。 |
| | 该资源包中包含大量活动投放位置。 | 减少资源包中的活动投放位置数量或增加资源包总预算。<br><br>如果包具有许多版面，但预算不足，则DSP可能无法为每个版面分配足够的预算。 每个投放位置应有机会每天至少花费2美元。 例如，如果您的包的预算为10美元/天，则最好包括五个或更少的投放位置。&#x200B;AEM |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [位置设置](/help/dsp/campaign-management/placements/placement-settings.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
>* [营销活动设置](/help/dsp/campaign-management/campaigns/campaign-settings.md)
