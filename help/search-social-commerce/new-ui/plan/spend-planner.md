---
title: 使用[!UICONTROL Spend Planner]
description: 了解如何生成、下载和应用项目组合预算推荐，以帮助您在项目组合中实现最佳支出分配。
feature: Search Optimization, Search Portfolios
exl-id: 966b8968-68b6-4385-9efb-e639a6729362
TQID: https://experienceleague.adobe.com/8BAQij06MRhxYoCoFNjhHsgC4o38lQnj9vpmTzYyqGg
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c2296997-5d79-4905-b32e-99b5aa892429id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: e0e44e7b2102ce3c7ec27c5dc4c50d46f1def4cf
workflow-type: tm+mt
source-wordcount: 1020
ht-degree: 0%

---

# 使用[!UICONTROL Spend Planner]

[!UICONTROL Spend Planner]（在旧版用户界面中称为“[!UICONTROL Spend Recommendation Tool]”）标识具有相同目标和货币的已优化和活动项目组合中的最佳支出分配，以使您可以最大化项目组合集的收入或目标目标。

在查看具有每日预算的项目组合支出推荐报表时，您可以将任何项目组合的预算更改为推荐预算。

## [!UICONTROL Spend Planner]报告中的数据

对于具有目标[!UICONTROL Maximize Clicks]的项目组合，此报表包括支出建议和点击预测。 对于所有其他目标，该报告包括支出建议和收入预测。

支出推荐报表包括以下数据：

* 散点图显示了在最佳设置单个支出目标时，在组合设置的给定总成本下可以实现的预测最大收入或点击量。 包括每个收入点或点击点的预测成本。

* 两个圆环图，显示支出和预期收入，或按投资组合显示点击分布： 1\)当前支出目标和2\)提议支出目标。

* 每个项目组合的条形图，其中显示所有选定项目组合或建议的总支出目标的当前总每日支出目标时，显示建议的每日支出（成本）和预测的收入分配或点击分配。 您可以选择将推荐的支出目标应用于所选项目组合，这会对下一个竞价执行周期的竞价产生影响。

## 可用操作

* 从[新用户界面](#spend-recommendations-generate)或[旧用户界面](#spend-recommendations-generate-legacy)生成[!UICONTROL Spend Planner]报告

* [将支出推荐](#spend-recommendations-apply)应用于相应的项目组合。

* [打开支出推荐报表数据或将支出推荐报表数据保存到文件](#spend-recommendations-download)

## （新UI）生成[!UICONTROL Spend Planner]报告 {#spend-recommendations-generate}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Plan]>[!UICONTROL Spend Planner]**。

1. 使用选定项目组合的当前组合预算查看数据：

   1. 单击&#x200B;**[!UICONTROL Select Objective]**。

   1. 选择项目组合目标。

   1. 选择货币。

   1. （可选）选择组合支出策略以进一步筛选组合列表。

   1. 选中要包含的每个项目组合旁边的复选框。

      仅列出具有选定参数的优化和活动项目组合。

   1. 单击&#x200B;**[!UICONTROL Update]**。

   1. （可选）要查看图表上任一点的成本和收入，请将光标悬停在该点上。

1. （可选）要下载建议的分配和每个产品组合的预期收入，请单击右列[!UICONTROL Portfolio Allocation]旁边的![下载](/help/search-social-commerce/assets/download-spend-recommendation.png "下载")。

   按照浏览器的正常过程打开或保存文件。 有关详细信息，请参阅浏览器的联机帮助。

1. （可选）要查看使用不同总支出目标的每个项目组合的建议每日支出和预期收入，请在[!UICONTROL Total Spend Target]字段中输入所有项目组合的建议每日支出总目标。 然后按&#x200B;**Enter**&#x200B;键。

   支出推荐工具使用来自每周模拟的数据，因此推荐的总支出与具有理想支出组合的建议支出目标最匹配。

## （旧版UI）从[!UICONTROL Optimization] > [!UICONTROL Spend Recommendation]视图生成[!UICONTROL Spend Recommendation]报告 {#spend-recommendations-generate-legacy}

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

## （新UI）应用支出推荐 {#spend-recommendations-apply}

*仅具有每日预算的项目组合*

>[!NOTE]
>
>* 如果应用的更改将增加或减少任何项目组合的支出目标超过20%，则必须批准更改。
>* 当投资组合的支出目标变化超过20%时，搜索、社交和Commerce需要长达3-4天的时间来调整其模型并实现新目标。

1. [为具有每日预算的一个或多个项目组合生成支出推荐报告](#spend-recommendations-generate)。

1. 选中要应用建议支出目标的每个项目组合旁边的复选框。 要选择所有项目组合，请选中&#x200B;**[!UICONTROL Select All Recommendations]**&#x200B;旁边的复选框。

1. 单击&#x200B;**[!UICONTROL Apply Selected Recommendations]**。

1. （如果任何预算更改超过20%）在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**&#x200B;以批准更改。

## （旧版UI）应用支出推荐 {#spend-recommendations-apply-legacy}

*仅具有每日预算的项目组合*

>[!NOTE]
>
>* 如果应用的更改将增加或减少任何项目组合的支出目标超过20%，则必须批准更改。
>* 当投资组合的支出目标变化超过20%时，搜索、社交和Commerce需要长达3-4天的时间来调整其模型并实现新目标。

1. [为具有每日预算的一个或多个项目组合生成支出推荐报告](#spend-recommendations-generate-legacy)。

1. 选中要应用建议支出目标的每个项目组合旁边的复选框。 要选择所有项目组合，请选中&#x200B;**[!UICONTROL Select All Recommendations]**&#x200B;旁边的复选框。

1. 单击&#x200B;**[!UICONTROL Apply Selected Recommendations]**。

1. （如果任何预算更改超过20%）在确认消息中，单击&#x200B;**[!UICONTROL Yes]**&#x200B;以批准更改。

## （新UI）打开数据或将数据另存为[!DNL Microsoft Excel]工作簿文件 {#spend-recommendations-download}

您可以打开或保存以下两种图表中的数据：a)显示成本点和每项成本的预期收入的折线图，以及b)当前和建议的媒体组合的圆环图。 [这看起来与Portfolio分配报表相同 — 它们应该有何不同？]

1. [为所选项目组合生成支出推荐报告](#spend-recommendations-generate)。

1. 在报表上方，单击![下载](/help/search-social-commerce/assets/download-spend-recommendation.png "下载")。

   按照浏览器的正常过程打开或保存文件。 有关详细信息，请参阅浏览器的联机帮助。

## （旧版UI）打开数据或将数据另存为[!DNL Microsoft Excel]工作簿文件 {#spend-recommendations-download-legacy}

1. 为所选项目组合生成支出推荐报告。

1. 在报表的右上角，单击![下载](/help/search-social-commerce/assets/download-spend-recommendation.png "下载")。

   按照浏览器的正常过程打开或保存文件。 有关详细信息，请参阅浏览器的联机帮助。
