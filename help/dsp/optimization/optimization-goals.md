---
title: 优化目标及其使用方式
description: 引用可用的优化目标并查看何时使用它们。
feature: DSP Optimization
exl-id: ad684c99-7ae5-48eb-abfe-d48fd3d34cd0
source-git-commit: 0a858fb9437439d2755f1a9679b0849c614293b7
workflow-type: tm+mt
source-wordcount: '1761'
ht-degree: 0%

---

# 优化目标及其使用方式

| 优化目标 | 描述 | 何时使用此目标 |
| -----------| ---------- | ---------- |
| [!UICONTROL Always Max Bid & Highest Clickthrough Rate] | 通过包级别优化，预算分配可优先处理点击率最高的投放位置。<br><br>拍卖评估将优先考虑CTR以实现支出目标。 提交的竞价始终是已设置的竞价 [!UICONTROL Max Bid]但是，如果配售支出良好，则预测的CTR阈值将变得更加严格。 | 促销活动类型：品牌策略<br><br>基准：最高点进率<br><br>广告类型：前置广告、显示广告<br><br><b>注意：</b> 如果您有一个不需要超越的固定CPM目标和一个必须最大化的CTR目标，请使用此目标。 将最高出价设置为所需的CPM目标，DSP在尝试花费全部预算的同时实现最佳的CTR。 |
| [!UICONTROL Always Max Bid & Highest Completion Rate] | 通过包级别优化，预算分配可优先处理完成率最高的投放位置。<br><br>拍卖评估将优先处理完成率，以实现支出目标。 提交的竞价始终是设置的最高竞价，但如果投放位置花费愉快，则预测的完成率阈值会变得更加严格。 | 促销活动类型：品牌策略<br><br>基准：最高完成率<br><br>广告类型：仅前置广告<br><br><b>注意：</b> 如果您有一个不需要超越的固定CPM目标和必须最大化的“完成率”目标，请使用此目标。 将最高出价设置为所需的CPM目标，DSP在尝试支出全部预算时实现最佳完成率。 |
| [!UICONTROL Always Max Bid & Highest Engagement Rate] | 通过包级别优化，预算分配可优先处理参与率最高的投放位置。<br><br>拍卖评估优先考虑实现支出目标的参与率。 提交的竞价始终是设置的最大竞价，但如果投放效果不错，则预测的参与率阈值会变得更加严格。 | 促销活动类型：品牌策略<br><br>基准：最高参与率<br><br>广告类型：仅限移动设备插播式广告<br><br><b>注意：</b> 如果您有不需要超越的固定CPM目标和必须最大化的参与目标，请使用此目标。 将最高出价设置为所需的CPM目标，DSP在尝试花费全部预算的同时实现最佳参与率。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (Adobe - GroupM)] | 通过包级别优化，预算分配可优先处理可见率最高的投放位置。<br><br>拍卖评估优先考虑实现支出目标的可见率。 提交的竞价始终是设置的“最高竞价”，但如果投放效果不错，则预测可视性比率阈值会变得更加严格。 | 促销活动类型：品牌策略<br><br>基准：最高可视性比率<br><br>广告类型：仅限交互式前置广告<br><br><b>注意：</b> 此目标始终使用投放位置级别的“最高出价”。<br><br>如果促销活动的可见度敏感度设置设为“标准（观看广告50%的时间连续两秒）”，则将使用媒体评级委员会(MRC)的可见度测量标准进行促销活动。 如果促销活动设置为“严格（100%的广告在视图和音频中持续50%的时间）”，则为促销活动使用GroupM可视性测量标准。 理想情况下，您应该将促销活动设置与优化目标和预竞价过滤器设置相匹配。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (Adobe - MRC)] | 通过包级别优化，预算分配可优先处理可见率最高的投放位置。<br><br>拍卖评估优先考虑实现支出目标的可见率。 提交的竞价始终是设置的“最高竞价”，但如果投放效果不错，则预测可视性比率阈值会变得更加严格。 | 促销活动类型：品牌策略<br><br>基准：最高可视性比率<br><br>广告类型：仅限交互式前置广告<br><br><b>注意：</b> 此目标始终使用投放位置级别的“最高出价”。<br><br>如果促销活动的可见度敏感度设置设为“标准（观看广告50%的时间连续两秒）”，则将使用媒体评级委员会(MRC)的可见度测量标准进行促销活动。 如果促销活动设置为“严格（100%的广告在视图和音频中持续50%的时间）”，则为促销活动使用GroupM可视性测量标准。 理想情况下，您应该将促销活动设置与优化目标和预竞价过滤器设置相匹配。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (IAS - MRC)] | 通过包级别优化，预算分配可优先处理可见率最高的投放位置。<br><br>拍卖评估优先考虑实现支出目标的可见率。 提交的竞价始终是设置的“最高竞价”，但如果投放效果不错，则预测可视性比率阈值会变得更加严格。 | 促销活动类型：品牌策略<br><br>基准：最高可视性比率<br><br>广告类型：仅限交互式前置广告<br><br><b>注意：</b> 此目标始终使用投放位置级别的“最高出价”。<br><br>当来自IAS的第三方数据通知算法时，此设置最有效。 仅当您为营销活动启用了IAS集成时才使用此目标。 |
| [!UICONTROL Always Max Bid and Maximize Reach] | 此目标尝试始终使用投放级别在给定展示次数的情况下实现最大的家庭覆盖率 [!UICONTROL Max Bid]. 如果达到了支出目标，DSP将变得更有选择性，只有在有机会实现递增的独特触及时才可以投标。 | 促销活动类型：品牌策略<br><br>基准：最大化范围<br><br>广告类型：前置广告、显示广告、CTV广告、本机广告、音频广告和通用视频广告 |
| [!UICONTROL Highest Return on Ad Spend (ROAS)] | （仅在包级别可用）预算分配将优先处理具有指定自定义目标中包含的最终转化事件的最高ROAS的投放位置，同时考虑到自定义目标中的任何其他加权顶部漏斗事件（例如网站访问和购物车添加）。 您可以指定优化模型是只应从基于点击的转化中学习，还是同时从基于点击和基于展示的转化中学习。<br><br>拍卖评估优先考虑ROAS。 支出目标得以实现，然后DSP在降低CPM与提高ROAS之间取得平衡。 | 营销活动类型：性能<br><br>基准：最高收入<br><br>广告类型：显示、本机、视频、CTV和通用视频<br><br><b>注意：</b> 请参阅&quot;[设置效果活动的最佳实践](/help/dsp/optimization/campaign-best-practices-performance.md)”以了解更多信息。 |
| [!UICONTROL Lowest Cost per Acquisition (CPA)] | （仅在包级别可用）预算分配将优先处理具有指定自定义目标中包含的最终转化事件最低CPA的投放位置，同时考虑到自定义目标中的任何其他加权顶部漏斗事件（例如网站访问和购物车添加）。 您可以指定优化模型是只应从基于点击的转化中学习，还是同时从基于点击和基于展示的转化中学习。<br><br>拍卖评估优先考虑CPA。 在实现支出目标后，DSP在降低CPM与降低CPA之间取得平衡。 | 营销活动类型：性能<br><br>基准：最低CPA<br><br>广告类型：显示、本机、视频、CTV和通用视频<br><br><b>注意：</b> 请参阅&quot;[设置效果活动的最佳实践](/help/dsp/optimization/campaign-best-practices-performance.md)”以了解更多信息。 |
| [!UICONTROL Lowest Cost per Click] | 通过包级别优化，预算分配可优先安排CPC最低的投放位置。<br><br>拍卖评估优先考虑CPC。 在实现支出目标后，DSP在降低CPM与提高CTR以降低CPC之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM和最高的点进率<br><br>广告类型：前置广告、显示广告<br><br><b>注意：</b> 使用此目标可达到最佳的CPC。 要保证最大CPM，请将其用作投放位置的最高出价。 |
| [!UICONTROL Lowest Cost per Completion] | 通过包级别优化，预算分配可优先处理每次完成成本最低的投放位置。<br><br>拍卖评估优先考虑视频完成率(VCR)。 在实现支出目标后，DSP会在降低CPM的同时增加VCR，以尝试降低每次完成的成本。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM和最高的完成率<br><br>广告类型：仅前置广告 |
| [!UICONTROL Lowest Cost per Engagement] | 通过包级别优化，预算分配可优先处理参与率最低的投放位置。<br><br>拍卖评估优先考虑参与率。 在实现支出目标后，DSP会尝试在降低CPM与降低每次参与的成本之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM和最高的参与率<br><br>广告类型：仅限移动设备插播式广告 |
| [!UICONTROL Lowest Cost per Reach] | 该目标试图在给定预算的情况下实现家庭覆盖的最大化。 正在实现支出目标，则根据实现增量独特触及的机会的不同，竞价会有所不同。 | 促销活动类型：品牌策略<br><br>基准：高效每次访问成本<br><br>广告类型：前置广告、显示广告、CTV广告、本机广告、音频广告和通用视频广告 |
| [!UICONTROL Lowest Cost per View] | 其操作方式与最低CPM类似。 通过包级别优化，预算分配可优先处理具有最低CPM的投放位置。<br><br>拍卖评估优先考虑CPM。 在实现支出目标后，DSP会逐步降低CPM。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM和最高的点进率<br><br>广告类型：前置广告、显示广告 |
| [!UICONTROL Lowest CPM] | 通过包级别优化，预算分配可优先处理具有最低CPM的投放位置。<br><br>拍卖评估优先考虑CPM。 在实现支出目标后，DSP会逐步降低CPM。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM<br><br>广告类型：前置广告、显示广告、CTV广告、原生广告、音频广告 |
| [!UICONTROL Lowest vCPM (Adobe - GroupM)] | 通过包级别优化，预算分配可优先处理具有最低vCPM的投放位置。<br><br>拍卖评估优先考虑vCPM。 在实现支出目标后，DSP会尝试在降低CPM与提高可见性之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM和最高的vCPM<br><br>广告类型：前置广告、显示广告<br><br><b>注意：</b> 使用此目标可达到最佳的vCPM。<br><br>要保证最大CPM，请将其用作投放位置的最高出价。 |
| [!UICONTROL Lowest vCPM (Adobe - MRC)] | 通过包级别优化，预算分配可优先处理具有最低vCPM的投放位置。<br><br>拍卖评估优先考虑vCPM。 在实现支出目标后，DSP会尝试在降低CPM与提高可见性之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM和最高的vCPM<br><br>广告类型：前置广告、显示广告<br><br><b>注意：</b> 使用此目标可达到最佳的vCPM。<br><br>要保证最大CPM，请将其用作投放位置的最高出价。 |
| [!UICONTROL Lowest vCPM (IAS - MRC)] | 通过包级别优化，预算分配可优先处理具有最低vCPM的投放位置。<br><br>拍卖评估优先考虑vCPM。 在实现支出目标后，DSP会尝试在降低CPM与提高可见性之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM和最高的vCPM<br><br>广告类型：前置广告、显示广告<br><br><b>注意：</b> 使用此目标可达到最佳的vCPM。<br><br>要保证最大CPM，请将其用作投放位置的最高出价。<br><br>当来自IAS的第三方数据通知算法时，此设置最有效。 仅当您为营销活动启用了IAS集成时才使用此目标。 |
| [!UICONTROL Lowest vCPM (Moat - GroupM)] | 通过包级别优化，预算分配可优先处理具有最低vCPM的投放位置。<br><br>拍卖评估优先考虑vCPM。 在实现支出目标后，DSP会尝试在降低CPM与提高可见性之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM和最高的vCPM<br><br>广告类型：前置广告、显示广告<br><br><b>注意：</b> 使用此目标可达到最佳的vCPM。<br><br>要保证最大CPM，请将其用作投放位置的最高出价。<br><br>当来自的第三方数据时，此设置最有效 [!DNL Moat] 正在通知算法。 仅在启用 [!DNL Moat] 营销活动集成。 |
| [!UICONTROL Lowest vCPM (Moat - MRC)] | 通过包级别优化，预算分配可优先处理具有最低vCPM的投放位置。<br><br>拍卖评估优先考虑vCPM。 在实现支出目标后，DSP会尝试在降低CPM与提高可见性之间取得平衡。 | 促销活动类型：品牌策略<br><br>基准：高效的CPM和最高的vCPM<br><br>广告类型：前置广告、显示广告<br><br><b>注意：</b> 使用此目标可达到最佳的vCPM。<br><br>要保证最大CPM，请将其用作投放位置的最高出价。<br><br>当来自的第三方数据时，此设置最有效 [!DNL Moat] 正在通知算法。 仅在启用 [!DNL Moat] 营销活动集成。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [设置效果活动的最佳实践](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [投放位置级别预竞价过滤器及其使用方式](optimization-pre-bid-filters.md)
>* [Campaign设置](/help/dsp/campaign-management/campaigns/campaign-settings.md)
