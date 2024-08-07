---
title: 查看职位安排预测报表
description: 查看投放位置的特定定位策略的展示次数、花费和最佳最高出价预测值。
feature: DSP Placements
exl-id: 6ff228b2-b656-493e-a299-98c7a68a0f51
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---

# 查看职位安排预测报表

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

投放位置预测工具显示特定定位策略的预测展示次数、花费和最佳最高竞价。 预测是根据投放位置提供的总体库存和可用的独特用户数来计算的。

>[!NOTE]
>
>* 投放预测计算不考虑邮政编码。
>* 对于仅具有计划性保证(PG)目标的投放位置，不会生成任何预测，因为可用性和支出是确定性的。

## 预测中的信息

预测包括以下信息：

* **[!UICONTROL Summary]：**

   * **[!UICONTROL Estimated CPM]：**&#x200B;目标设置预计可达到的每千次展示的估计成本(eCPM)。

   * **[!UICONTROL Budget]：**&#x200B;定位设置的预计预算。

   * **[!UICONTROL Impression]：**&#x200B;定位设置的预计展示次数。

* **[!UICONTROL Budget Yield Curve]：**&#x200B;如果所有其他定位设置相同，投放位置在不同预算级别可投放的预计展示次数。

* **[!UICONTROL Max Bid Yield Curve]：**&#x200B;当所有其他定位设置相同时，位于不同最高出价级别的投放位置的预计支出。

* **[!UICONTROL Message]：**&#x200B;提供有关预测输出的信息，包括无法生成预测的任何方案。 它还突出显示由于缺少数据而审核但未在该场景中考虑的任何定位设置。

### 预算计算

* 对于未分配给资源包的版面，使用版面预算进行计算。 在飞行中，计算相同的总体预算。

* 对于资源包中的版面，将使用分配给该版面的预算进行计算。 在投放期间，将计算分配给投放位置的预算，并将其包含在消息中。

* 对于投放中添加到包中的投放位置，预算会根据投放位置数量进行平均分配。 当投放位置上线时，将计算资源包分配的预算。

## 要求

* 最低支出：每日25美元或相当于每次投放的当地货币。

* 最大支出：每天15,000美元或相当于每次投放的当地货币。

* 最小最高出价、最大最高出价：按投放类型列出最低最高出价（适用于预算产出率曲线）和最高出价（适用于最高出价产出率曲线）。 这些值在全球都是真实值，不考虑地区差异。 有时，这些值对于目标区域可能过高或过低。

* 历史数据：当有足够的历史数据时，投放位置预测可用。 以下是历史数据可能不足时的示例：

   * 投放位置将定位营销活动的新区域。

   * 投放位置将定向营销活动的新库存交易。

   * 投放位置为营销活动使用新的广告类型。

     投放位置通常是供应方平台定义的多个广告模板的集合。 因此，即使投放位置已存在很长时间，如果基础广告模板是新的，则预测工具无法创建预测。

## 打开职位安排预测报表

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 单击营销活动的名称，然后单击&#x200B;**[!UICONTROL Placements]**。

1. 在投放位置名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit]**。

1. 找到右上角的&#x200B;**[!UICONTROL Forecast]**&#x200B;部分。 如有必要，请单击![预测](/help/dsp/assets/placement-forecast.png)。

   >[!NOTE]
   >
   >* 有时，预测可能由于浏览器缓存而不可用。 如果发生这种情况，请清除缓存并重试。

>[!MORELIKETHIS]
>
>* Campaign Management视图中的[性能报告类型](campaign-reports-about.md)
>* [查看位置诊断报告](/help/dsp/campaign-management/reports/placement-diagnostics.md)
>* [位置设置](/help/dsp/campaign-management/placements/placement-settings.md)
