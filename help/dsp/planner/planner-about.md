---
title: 关于DSP Planner工具
description: 了解规划者工具，以根据指定的预算和定位标准预测连接电视(CTV)投放位置的独特范围。
feature: DSP Planner
exl-id: b25d4ac5-e85f-4a38-8765-6c5261987668
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---

# 关于DSP Planner工具

<!-- rename all titles/descriptions from "CTV reach planner" to "campaign reach planner" -->

*Beta功能*

在您开始购买库存之前，规划者工具可帮助您根据指定的预算和定位标准预测联网电视(CTV)投放的家庭级独特触及率。 在评估多个覆盖范围计划后，您可以实施最符合包和投放位置中所需结果的计划。

Planner工具使用过去90天的历史竞价、展示次数和到达率数据来估计计划配置的唯一到达率、平均CPM、平均频率和展示次数。

## 计划员预测

每个预测均由到达预算预测曲线组成，该曲线显示了使用计划设置可以实现的到达量。 将光标移动到可视化图表上可查看预算较高的增量访问机会。

![计划员预测](/help/dsp/assets/planner-forecast.png "计划员预测")

预测输出还包含[!UICONTROL Inventory Breakdown]部分，该部分显示不同发布者如何促进独特范围，从而提供有价值的发现机会。

>[!NOTE]
>
>* [!UICONTROL Inventory Breakdown]部分仅显示专用和[!UICONTROL On Demand]清单的数据。
>* 显示的两个发布者的估计唯一范围可能重叠。

## 规划者视图

在[!UICONTROL Planner]视图中，您可以查看现有CTV覆盖计划并创建新覆盖计划。

您还可以编辑、复制、导出、存档或重新生成任何计划的预测。

## 常见问题解答

+++规划者工具支持哪些类型的库存？

规划者工具支持所有类型的库存，包括计划性保证(PG)、私有市场(PMP)、[!UICONTROL On Demand]和公共。 要生成准确的预测，请将过去7天内至少5万次展示的交易包含在内。

+++

+++为什么我看到&quot;[!UICONTROL Unable to generate forecast]&quot;？

此错误的最常见原因之一是预算不足或最高出价不足。 为获得最佳结果，请使用最低预算5000美元。 如果选择[!UICONTROL Connected TV]媒体类型，请输入至少10美元的最大出价。

此外，请确保包含的出版商或交易处于活跃状态并具有最近的展示活动。

+++

+++我基于预测构建了一个投放位置，但它没有达到触及预测所指示的独特触及量。 为什么？

范围预测只是一个估计值，并且实际结果可能会因为多种经常变化的因素而有所不同，例如季节性、竞价竞争力和供需。 虽然它并不完全准确，但最适合用于定向分析可能带来最佳结果的促销活动策略。

+++

+++计划员是否可以使用相同的输入设置生成不同的预测结果？

计划员根据最新观察数据生成预测，因此预测输出可能在不同时间有所不同，即使计划设置保持相同。 考虑为同一计划生成多个预测，并为每个计划导出结果。

+++

+++我可以保存计划员预测输出吗？

可以，您可以通过单击右上角的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Export]**&#x200B;将预测导出到[!DNL Microsoft Excel]电子表格中。 电子表格使用两个数据列捕获到达预算曲线中显示的信息：[!UICONTROL Budget]和[!UICONTROL Reach]。

>[!MORELIKETHIS]
>
>* [关于DSP Planner工具](planner-about.md)
>* [创建连接的电视访问计划](planner-create.md)
>* [复制连接的电视访问计划](planner-duplicate.md)
>* [编辑连接的电视访问计划](planner-edit.md)
>* [导出连接的电视访问计划](planner-export.md)
>* [重新生成连接电视到达计划的预测](planner-forecast.md)
>* [存档连接的电视访问计划](planner-archive.md)
>* [已连接电视访问计划的设置](planner-settings.md)
