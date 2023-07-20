---
title: 优化目标及其使用方式
description: 引用可用的优化目标并查看何时使用它们。
feature: DSP Optimization
exl-id: ad684c99-7ae5-48eb-abfe-d48fd3d34cd0
source-git-commit: 2715dc78193f1f5239f0bc4689262df05c6770eb
workflow-type: tm+mt
source-wordcount: '1608'
ht-degree: 0%

---

# 优化目标及其使用方式

| 优化目标 | 描述 | 何时使用此目标 |
| -----------| ---------- | ---------- |
| [!UICONTROL Always Max Bid & Highest Clickthrough Rate] | 通过包级别优化，预算分配将优先考虑点击率最高的投放位置。<br><br>如果支出目标得以实现，拍卖评估将优先考虑CTR。 提交的竞价将始终是已设置的竞价 [!UICONTROL Max Bid]但是，如果配售支出良好，预计的CTR阈值将变得更加严格。 | 促销活动类型：品牌策略<br><br>基准：最高点进率<br><br>广告类型：前置广告、显示广告<br><br><b>注意：</b> 如果您有一个不需要超越的固定CPM目标和一个需要最大化的CTR目标，请使用此目标。 将最高出价设置为所需的CPM目标，DSP将在尝试花费全部预算的同时实现最佳的CTR。 |
| [!UICONTROL Always Max Bid & Highest Completion Rate] | 通过包级别优化，预算分配将优先考虑完成率最高的投放位置。<br><br>如果支出目标得以实现，拍卖评估将优先考虑完成率。 提交的竞价将始终是设置的最高竞价，但如果投放效果不错，则预测的完成率阈值将变得更加严格。 | 促销活动类型：品牌策略<br><br>基准：最高完成率<br><br>广告类型：仅前置广告<br><br><b>注意：</b> 如果您有一个无需超越的固定CPM目标和一个需要最大化的“完成率”目标，请使用此目标。 将最高出价设置为所需的CPM目标，DSP将在尝试花费全部预算时实现最佳完成率。 |
| [!UICONTROL Always Max Bid & Highest Engagement Rate] | 通过包级别优化，预算分配将优先考虑参与率最高的投放位置。<br><br>如果达到支出目标，拍卖评估将优先考虑参与率。 提交的竞价将始终是设置的最高竞价，但如果投放效果不错，则预测的参与率阈值将变得更加严格。 | 促销活动类型：品牌策略<br><br>基准：最高参与率<br><br>广告类型：仅限移动设备插播式广告<br><br><b>注意：</b> 如果您有一个不需要超越的固定CPM目标和需要最大化的参与目标，请使用此目标。 将最大竞价设置为所需的CPM目标，DSP将在尝试花费全部预算的同时实现尽可能最佳的参与率。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (Adobe – GroupM)] | 通过包级别优化，预算分配将优先处理可见率最高的投放位置。<br><br>如果支出目标得以实现，拍卖评估将优先考虑可见率。 提交的竞价将始终是设置的最高竞价，但如果投放效果不错，则预测可视性比率阈值将变得更加严格。 | 促销活动类型：品牌策略<br><br>基准：最高可视性比率<br><br>广告类型：仅限交互式前置广告<br><br><b>注意：</b> 此目标将始终使用投放位置级别的“最高出价”。<br><br>如果促销活动的可视性敏感度设置设为“标准（观看广告50%的时间连续两秒）”，则会将媒体评级委员会(MRC)可视性衡量标准用于促销活动。 如果促销活动设置为“严格（100%的广告查看次数和音频开启时间为50%持续时间）”，则促销活动会使用GroupM可见性度量标准。 理想情况下，您应该将促销活动设置与优化目标和预竞价过滤器设置相匹配。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (Adobe – MRC)] | 通过包级别优化，预算分配将优先处理可见率最高的投放位置。<br><br>如果支出目标得以实现，拍卖评估将优先考虑可见率。 提交的竞价将始终是设置的最高竞价，但如果投放效果不错，则预测可视性比率阈值将变得更加严格。 | 促销活动类型：品牌策略<br><br>基准：最高可视性比率<br><br>广告类型：仅限交互式前置广告<br><br><b>注意：</b> 此目标将始终使用投放位置级别的“最高出价”。<br><br>如果促销活动的可视性敏感度设置设为“标准（观看广告50%的时间连续两秒）”，则会将媒体评级委员会(MRC)可视性衡量标准用于促销活动。 如果促销活动设置为“严格（100%的广告查看次数和音频开启时间为50%持续时间）”，则促销活动会使用GroupM可见性度量标准。 理想情况下，您应该将促销活动设置与优化目标和预竞价过滤器设置相匹配。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (IAS – MRC)] | 通过包级别优化，预算分配将优先处理可见率最高的投放位置。<br><br>如果支出目标得以实现，拍卖评估将优先考虑可见率。 提交的竞价将始终是设置的最高竞价，但如果投放效果不错，则预测可视性比率阈值将变得更加严格。 | 促销活动类型：品牌策略<br><br>基准：最高可视性比率<br><br>广告类型：仅限交互式前置广告<br><br><b>注意：</b> 此目标将始终使用投放位置级别的“最高出价”。<br><br>当来自IAS的第三方数据通知算法时，此设置效果最佳。 仅当您为营销活动启用了IAS集成时，才使用此目标。 |
| [!UICONTROL Highest ROAS – Custom Goal] | （仅在包级别可用）预算分配将优先考虑广告支出回报率(ROAS)最高的投放位置。<br><br>拍卖评估将优先考虑ROAS。 如果支出目标得以实现，则DSP将在降低CPM与提高ROAS之间取得平衡。 | 营销活动类型：性能<br><br>基准：最高收入<br><br>广告类型：显示、原生和视频<br><br><b>注意：</b> 参见“[设置效果营销活动的最佳实践](/help/dsp/optimization/campaign-best-practices-performance.md)”以了解更多信息。 |
| [!UICONTROL Lowest CPA – Custom Goal] | （仅在包级别可用）预算分配将优先安排具有最低CPA的投放。<br><br>拍卖评估将优先考虑CPA。 如果支出目标得以实现，则DSP将在降低CPM与降低CPA之间取得平衡。 | 营销活动类型：性能<br><br>基准：最低CPA<br><br>广告类型：显示、原生和视频<br><br><b>注意：</b> 参见“[设置效果营销活动的最佳实践](/help/dsp/optimization/campaign-best-practices-performance.md)”以了解更多信息。 |
| [!UICONTROL Lowest Cost Per Click] | 通过包级别优化，预算分配将优先考虑CPC最低的投放位置。<br><br>拍卖评估将优先考虑中油。 如果支出目标得以实现，则DSP将在降低CPM与提高CTR以降低CPC之间达到平衡。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM和最高的点进率<br><br>广告类型：前置广告、显示广告<br><br><b>注意：</b> 使用此目标可达到最佳的CPC。 要保证最大CPM，请将其用作投放位置的最高出价。 |
| [!UICONTROL Lowest Cost Per Completion] | 通过包级别优化，预算分配将优先考虑每次完成成本最低的投放位置。<br><br>拍卖评估将优先考虑视频完成率(VCR)。 如果支出目标得以实现，则DSP将在降低CPM与增加VCR之间达到平衡，从而尝试降低每次完成的成本。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM和最高的完成率<br><br>广告类型：仅前置广告 |
| [!UICONTROL Lowest Cost Per Engagement] | 通过包级别优化，预算分配将优先考虑参与率最低的投放位置。<br><br>拍卖评估将优先考虑订婚率。 如果支出目标得以实现，则DSP将尝试在降低CPM与降低每次参与的成本之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM和最高的参与率<br><br>广告类型：仅限移动设备插播式广告 |
| [!UICONTROL Lowest CPM] | 通过包级别优化，预算分配将优先考虑CPM最低的投放位置。<br><br>拍卖评估将优先考虑CPM。 如果支出目标得以实现，则DSP将逐步降低CPM。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM<br><br>广告类型：前置广告、显示广告、CTV广告、原生广告、音频广告 |
| [!UICONTROL Lowest Cost Per View] | 其操作方式与最低CPM类似。 通过包级别优化，预算分配将优先考虑CPM最低的投放位置。<br><br>拍卖评估将优先考虑CPM。 如果支出目标得以实现，则DSP将逐步降低CPM。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM和最高的点进率<br><br>广告类型：前置广告、显示广告 |
| [!UICONTROL Lowest vCPM (Adobe - GroupM)] | 通过包级别优化，预算分配将优先考虑vCPM最低的投放位置。<br><br>拍卖评估将优先考虑vCPM。 如果支出目标得以实现，则DSP将尝试在降低CPM与提高可见性之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM和最高的vCPM<br><br>广告类型：前置广告、显示广告<br><br><b>注意：</b> 使用此目标可达到最佳的vCPM。<br><br>要保证最大CPM，请将其用作投放位置的最高出价。 |
| [!UICONTROL Lowest vCPM (Adobe - MRC)] | 通过包级别优化，预算分配将优先考虑vCPM最低的投放位置。<br><br>拍卖评估将优先考虑vCPM。 如果支出目标得以实现，则DSP将尝试在降低CPM与提高可见性之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM和最高的vCPM<br><br>广告类型：前置广告、显示广告<br><br><b>注意：</b> 使用此目标可达到最佳的vCPM。<br><br>要保证最大CPM，请将其用作投放位置的最高出价。 |
| [!UICONTROL Lowest vCPM (IAS - MRC)] | 通过包级别优化，预算分配将优先考虑vCPM最低的投放位置。<br><br>拍卖评估将优先考虑vCPM。 如果支出目标得以实现，则DSP将尝试在降低CPM与提高可见性之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM和最高的vCPM<br><br>广告类型：前置广告、显示广告<br><br><b>注意：</b> 使用此目标可达到最佳的vCPM。<br><br>要保证最大CPM，请将其用作投放位置的最高出价。<br><br>当来自IAS的第三方数据通知算法时，此设置效果最佳。 仅当您为营销活动启用了IAS集成时，才使用此目标。 |
| [!UICONTROL Lowest vCPM (Moat - GroupM)] | 通过包级别优化，预算分配将优先考虑vCPM最低的投放位置。<br><br>拍卖评估将优先考虑vCPM。 如果支出目标得以实现，则DSP将尝试在降低CPM与提高可见性之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM和最高的vCPM<br><br>广告类型：前置广告、显示广告<br><br><b>注意：</b> 使用此目标可达到最佳的vCPM。<br><br>要保证最大CPM，请将其用作投放位置的最高出价。<br><br>当来自的第三方数据时，此设置最有效 [!DNL Moat] 为算法提供信息。 仅在启用 [!DNL Moat] 营销活动集成。 |
| [!UICONTROL Lowest vCPM (Moat - MRC)] | 通过包级别优化，预算分配将优先考虑vCPM最低的投放位置。<br><br>拍卖评估将优先考虑vCPM。 如果支出目标得以实现，则DSP将尝试在降低CPM与提高可见性之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM和最高的vCPM<br><br>广告类型：前置广告、显示广告<br><br><b>注意：</b> 使用此目标可达到最佳的vCPM。<br><br>要保证最大CPM，请将其用作投放位置的最高出价。<br><br>当来自的第三方数据时，此设置最有效 [!DNL Moat] 为算法提供信息。 仅在启用 [!DNL Moat] 营销活动集成。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [设置效果营销活动的最佳实践](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [置入级别预竞价筛选器及其使用方式](optimization-pre-bid-filters.md)
>* [Campaign设置](/help/dsp/campaign-management/campaigns/campaign-settings.md)
