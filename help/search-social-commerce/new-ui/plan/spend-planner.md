---
title: 使用[!UICONTROL Spend Planner]
description: 了解如何使用[!UICONTROL Spend Planner]确定项目组合间的最佳支出分配。
feature: Search Optimization, Search Portfolios, Search Simulations
source-git-commit: 723d50d11cd76471ac41d3bb007af4f5d1bfa32f
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 0%

---

# 使用[!UICONTROL Spend Planner]

<!-- When this becomes a menu item, move file and TOC entry accordingly -->

[!UICONTROL Spend Planner]（在旧版用户界面中称为“支出推荐工具”）可识别具有相同目标和货币的优化和活动项目组合中的最佳支出分配，以使您能够实现项目组合集收入最大化或目标化。

在查看具有每日预算的项目组合支出推荐报表时，您可以将任何项目组合的预算更改为推荐预算。

## [!UICONTROL Spend Planner]报告中的数据

对于具有目标[!UICONTROL Maximize Clicks]的项目组合，此报表包括支出建议和点击预测。 对于所有其他目标，该报告包括支出建议和收入预测。

支出推荐报表包括以下数据：

* 散点图显示了在最佳设置单个支出目标时，在组合设置的给定总成本下可以实现的预测最大收入或点击量。 包括每个收入点或点击点的预测成本。

* 两个圆环图，显示支出和预期收入，或按投资组合显示点击分布： 1\)当前支出目标和2\)提议支出目标。

* 每个项目组合的条形图，其中显示所有选定项目组合或建议的总支出目标的当前总每日支出目标时，显示建议的每日支出（成本）和预测的收入分配或点击分配。 您可以选择将推荐的支出目标应用于所选项目组合，这会对下一个竞价执行周期的竞价产生影响。

## （新UI）从[!UICONTROL Spend Planner] > [!UICONTROL Manage]视图生成[!UICONTROL Simulations]报告

<!-- The path will probably change, so then update the heading and instructions -->

1. 在主菜单中，单击&#x200B;**[!UICONTROL Plan]>[!UICONTROL Simulations]**。

1. 在数据表上方的工具栏中，单击![支出规划者](/help/search-social-commerce/assets/spend-planner-icon.png "支出规划者")。

   [!UICONTROL Spend Recommendation]工具将在旧版用户界面中打开。

1. 使用选定项目组合的当前组合预算查看数据：

   1. 选择项目组合目标。

   1. 选择货币。

   1. （可选）选择组合支出策略以进一步筛选组合列表。

   1. 选中要包含的每个项目组合旁边的复选框。 要选择所有项目组合，请选中[!UICONTROL Portfolios]旁边的复选框。

      仅列出具有选定参数的优化和活动项目组合。

   1. 单击&#x200B;**[!UICONTROL Update]**。

   1. （可选）要查看图表上任一点的成本和收入，请将光标悬停在该点上。

1. （可选）要查看使用新总支出目标的每个组合的建议每日支出和预测收入，请在[!UICONTROL Total Spend Target]字段中输入所有组合的建议每日支出总目标。 然后按&#x200B;**Enter**&#x200B;键。

   支出推荐工具使用来自每周模拟的数据，因此推荐的总支出与具有理想支出组合的建议支出目标最匹配。

## （旧版UI）从[!UICONTROL Spend Recommendation] > [!UICONTROL Optimization]视图生成[!UICONTROL Spend Recommendation]报告

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Optimization] >[!UICONTROL Spend Recommendation]**。

1. 使用选定项目组合的当前组合预算查看数据：

   1. 选择项目组合目标。

   1. 选择货币。

   1. （可选）选择组合支出策略以进一步筛选组合列表。

   1. 选中要包含的每个项目组合旁边的复选框。 要选择所有项目组合，请选中[!UICONTROL Portfolios]旁边的复选框。

      仅列出具有选定参数的优化和活动项目组合。

   1. 单击&#x200B;**[!UICONTROL Update]**。

   1. （可选）要查看图表上任一点的成本和收入，请将光标悬停在该点上。

1. （可选）要查看使用新总支出目标的每个组合的建议每日支出和预测收入，请在[!UICONTROL Total Spend Target]字段中输入所有组合的建议每日支出总目标。 然后按&#x200B;**Enter**&#x200B;键。

   支出推荐工具使用来自每周模拟的数据，因此推荐的总支出与具有理想支出组合的建议支出目标最匹配。

## 应用支出推荐

*仅具有每日预算的项目组合*

>[!NOTE]
>
>* 如果应用的更改将增加或减少任何项目组合的支出目标超过20%，则您将收到通知，并且必须批准更改。
>* 当投资组合的支出目标变化超过20%时，搜索、社交和Commerce需要长达3-4天的时间来调整其模型并实现新目标。

1. 查看具有每日预算的一个或多个项目组合的支出推荐报表。

1. 选中要应用建议支出目标的每个项目组合旁边的复选框。 要选择所有项目组合，请选中[!UICONTROL Select All Recommendations]旁边的复选框。

1. 单击&#x200B;**[!UICONTROL Apply Selected Recommendations]**。

1. （如果任何预算更改超过20%）在确认消息中，单击&#x200B;**[!UICONTROL Yes]**&#x200B;以批准更改。

## 打开数据或将数据保存到文件

您可以从[!UICONTROL Spend Recommendation]报表的任何部分导出报表数据。 您可以打开数据，也可以将数据另存为[!DNL Microsoft Excel]工作簿文件。

1. 为所选项目组合生成支出推荐报告。

1. 在报表上方，单击![下载](/help/search-social-commerce/assets/download-spend-recommendation.png "下载")。

   按照浏览器的正常过程打开或保存文件。  有关详细信息，请参阅浏览器的联机帮助。
