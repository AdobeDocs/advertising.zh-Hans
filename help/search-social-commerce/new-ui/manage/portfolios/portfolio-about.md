---
title: （新UI）关于项目组合
description: 了解项目组合。
feature: Search Portfolios, Search Optimization
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# （新UI）关于项目组合

*Beta功能*

您可以使用项目组合（与投资组合类似）集体管理广告营销活动。 组合是指一组针对单个业务目标而优化的广告营销活动或广告集（包括其关联的关键字和广告）。 目标可以包括多个加权转化和单个预算或绩效目标（例如每月预算或目标ROI）。 由于单个营销活动/广告集、关键词和广告的执行方式可能各不相同（例如，它们可能花费不同的金额或实现不同的ROI），因此优化功能会使用AI驱动模型引导整个项目组合以共同实现目标。 组合中的所有营销活动使用相同的货币。

某些用户角色可以创建和配置项目组合。 根据项目组合类型，项目组合设置可能包括项目组合目标、分配的活动、支出策略、任何项目组合级别的竞价约束以及建模和优化参数。 当您准备好进行搜索、Social和Commerce以开始优化项目组合时，请将状态更改为“已优化”。

您可以选择将项目组合分组到项目组合组中，以便查看整个组的组合点击和收入数据。 从[旧版UI](/help/search-social-commerce/getting-started/ui-switch.md)创建项目组合组。

根据您的角色，您可以生成性能模拟，这些模拟使用预测建模来标识最佳支出点和详细的预测准确度报表。<!-- Mention this now? In addition, all users can use the Spend Recommendation Tool to identify the optimal budget distribution across portfolios. -->

## 通过竞价策略提供优化支持 {#optimization-by-bid-strategy}

营销活动有资格根据营销活动或广告组竞价策略进行优化。

>[!NOTE]
>
>“智能竞价”和“自动竞价”经常互换使用，但它们不是一回事。 智能竞价仅引用使用拍卖时间竞价的[!DNL Google Ads]和[!DNL Microsoft Advertising]自动竞价策略，这意味着广告网络会在每次拍卖时优化转化或转化值。

<!-- Add "Frequency of Bidding (or other actions, like adjusting campaign budget or bid adjustment values?) -->

| 竞价策略 | 明智的竞价？ | 关键字/产品组级别的竞价？ | 支持级别 | 目标类型 | 竞价单位 | Adobe设置了哪些内容？ | 广告网络设置什么？ |
|---|---|---|---|---|---|---|---|
| 手动CPC （仅[!DNL Google Ads]选项） | — | 是 | 创建、编辑、优化 | 具有任何权重值的单属性或多属性目标 | 关键字+匹配类型+促销活动 | 关键字竞价、促销活动预算、竞价调整值 | 不适用 |
| ECPC（增强CPC） | 是 | 是 | 创建、编辑、优化 | 具有任何权重值的单属性或多属性目标 | 关键字+匹配类型+促销活动 | 关键词竞价、营销活动预算 | 实时调整竞价 |
| 最大化点击次数[^1] | — | — | 创建、编辑、优化 | 无；仅针对点击次数进行优化 | 营销活动 | 营销活动预算 | 实时调整竞价以最大限度地提高预算内的点击次数 |
| 最大化转化<br>（无论是否有TCPA） | 是 | — | 创建、编辑、优化 | 使用权重1的单属性目标 | 营销活动或广告组([!DNL Google Ads])<br>仅限营销活动([!DNL Microsoft Advertising]) | 促销活动预算，设置<br>TCPA时的目标CPA可以是[!DNL Microsoft Advertising]中的独立竞价策略) | 实时调整竞价以在预算内最大化订单/商机，在设置目标时实现CPA目标 |
| 最大化转化值<br>（无论是否有TROAS） | 是 | — | 创建、编辑、优化 | 具有任何权重值的多属性目标，或权重值大于1的单属性目标（表示货币值） | 营销活动或广告组([!DNL Google Ads])<br>仅限营销活动([!DNL Microsoft Advertising]) | 促销活动预算，设置<br>TROAS时的目标ROAS可以是[!DNL Microsoft Advertising]中的独立竞价策略) | 实时调整竞价以最大限度地提高预算内的收入/利润，从而在设置目标时实现ROAS目标 |
| 目标展示份额 | — | — | 创建，编辑 | 不适用 | 不适用 | 不适用 — 无法分配给项目组合 | 实时调整竞价以实现展示份额目标 |

[^1]：广告网络上的[!UICONTROL Maximize Clicks]竞价策略设置与Search、Social和Commerce目标[!UICONTROL Maximize Clicks]不同。 如果竞价策略为[!UICONTROL Maximize Clicks]，则应仅将其分配给具有营销活动级别或广告组级别优化的项目组合，而不是具有关键词级别优化的项目组合。

## Portfolio状态 {#portfolio-status}

项目组合可以具有以下状态：

<!-- **Link to include file for "Portfolio status"** -->

{{$include /help/_includes/search-portfolio-status.md}}

## [!UICONTROL Portfolios]视图

[!UICONTROL Portfolios]视图列出了您的现有项目组合，其中包含可自定义的性能数据。 您可以[自定义视图](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)中的列，并从工具栏[或](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)列标题[筛选数据以包含特定项目组合](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)。

<!-- No options yet to edit anything within the grid, view bid changes, add a portfolio to a portfolio group, edit the Target column, or import/export DOW targets. -->

### 可用操作

<!-- Update with any new options -->

<!-- within row:
* [Rename a portfolio](portfolio-rename.md)

* [View the constraints for a portfolio](portfolio-view-constraint.md)

* [View the change history for a portfolio](portfolio-view-change-history.md)
-->

* [创建项目组合](portfolio-create.md)

* [复制项目组合](portfolio-duplicate.md)

* [编辑项目组合设置](portfolio-edit.md)

* [使用批量工作表文件批量编辑项目组合设置](portfolio-bulksheets.md)

* [查看项目组合绩效详细信息](portfolio-details.md)

* [在[!UICONTROL Portfolios]视图中下载数据](portfolio-view-report.md)

>[!MORELIKETHIS]
>
>* [创建项目组合](portfolio-create.md)
>* [复制项目组合](portfolio-duplicate.md)
>* [编辑项目组合](portfolio-edit.md)
>* [从[!UICONTROL Portfolios]视图管理数据视图报告](portfolio-view-report.md)
