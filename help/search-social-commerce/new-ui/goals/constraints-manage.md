---
title: 管理搜索竞价单位的限制
description: 了解限制条件，以限制旧版关键词级别项目组合中CPC促销活动中竞价单位的竞价。
feature: Search Campaign Management, Search Optimization
source-git-commit: 1113c9f6ff8446d075dc9b90441f4119eb657598
workflow-type: tm+mt
source-wordcount: '2649'
ht-degree: 0%

---

# 管理搜索竞价单位的限制

*仅适用于旧版关键词级别项目组合中的CPC促销活动中的竞价单位*

竞价单位约束是限制所有[竞价单位](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/glossary.html?lang=zh-Hans)的优化竞价以及与约束关联的成本和收入模型的规则。

## 关于约束

每个约束都适用于特定货币，并且可选地包括触发条件，在指定的数据评估期间必须满足这些条件才能应用规则。 要评估的数据可以包括渠道类型、匹配类型、点击数据、转化数据或派生量度。 例如，您可以将竞价限制在特定货币范围内，按指定金额连续增加或减少竞价，或根据项目组合的平均竞价进行竞价。 每个限制都有一个适用的开始日期，可以在特定日期到期或无限期应用。

设置限制后，您可以将其分配给特定竞价单位，或分配给特定广告组或促销活动中的所有竞价单位。 每个竞价单位可以有一个限制。 约束由子实体继承，但可以覆盖。 在最低级别分配的约束始终会覆盖在父级别分配的约束。 当您将约束分配给竞价单位时，无论竞价单位产生了多少收入，当竞价单位具有成本和收入模型时，竞价都会在该竞价单位的指定约束内运行。

>[!CAUTION]
>
>在为竞价单位分配约束时，您可以改写竞价优化系统的决策，并自行承担该竞价单位的ROI责任。

>[!NOTE]
>
>* 活动约束仅限制优化旧关键词级别项目组合中已分配竞价单位的竞价。 对于混合项目组合中、活动项目组合中或不在项目组合中的竞价单位，它们将被忽略。 **提示：**&#x200B;在项目组合设置中，打开项目组合选项“自动调整促销活动预算限制”。 建议的“多个”值为“1”。
> * 对于数据不足以生成成本和收入模型的竞价单位，将忽略竞价约束。
>* （具有CPC或eCPC竞价策略的营销活动）当竞价限制与项目组合级别竞价限制冲突时，该限制将覆盖项目组合级别限制。 例如，如果产品组合的最低竞价为5美元，但是您将产品组合中的竞价单位限制为最低竞价为3美元，则竞价单位将竞价为3美元或更高。 但是，约束竞价单位的总体支出由组合的[“围绕约束的支出”参数](#spend-around-constraints)决定。
>* 约束对基本竞价起作用。 对基本竞价的任何类型的竞价调整（如提高移动设备上的最终用户的竞价）都可以将竞价移动到约束允许范围之外。 例如，如果约束要求最大CPC为6美元，则基础竞价已为6美元，并且产品组合自动优化移动设备的竞价调整(50%-60%)，则最大CPC为9.00-9.60美元（而不是6美元）。

### 约束类型 {#constraint-types}

* **[!UICONTROL Bid]：**&#x200B;将出价限制在货币范围。

* **[!UICONTROL Bid Shift]：**&#x200B;在竞价范围内，按指定数量连续更改所有关联竞价单位的优化竞价。 竞价转移导致相关项目组合因竞价转移导致的总支出过多或过低，而不管项目组合的“围绕约束支出”设置如何。 注意：如果当前CPC竞价已等于或大于最大竞价，或等于或小于最小竞价，则忽略限制并且不更改竞价。 此外，竞价转移约束不适用于数据不足无法生成成本和收入模型的竞价单位。

* **[!UICONTROL Incremental Bidding]：** （仅适用于没有展示次数的关键字）以指定速率递增或递减出价，直到出价达到指定目标为止。

* **[!UICONTROL Search Engine Min Bid]：** （仅限[!DNL Google Ads]帐户）使用搜索引擎确定的最小CPC出价作为您的最小出价。 随着搜索引擎更改其最低出价，您的出价也会相应地更改。 您可以选择为所有关联的竞价单位指定其他竞价限制。

* **[!UICONTROL Impression Share]：** （仅具有完全匹配项的[!DNL Google Ads]和[!DNL Microsoft Advertising] CPC促销活动）当广告在最小展示份额和最大展示份额之间时，将竞价限制在货币范围。 **注意：**&#x200B;当约束不具成本效益时，优化功能可能会覆盖它。

### 何时应用约束

限制竞价单位的一些原因包括：

* 用于快速显示未经测试的关键字和广告。

* 降低新项目组合、帐户、营销活动和广告组的风险。 例如，在启动项目组合之前，您可以设置高流量竞价单位的最大竞价，然后每天逐渐提高值。 这允许竞价模式每天进行调整，而不会出现竞价大幅上涨的风险。

* 确保不会将具有高转化率的尾关键字竞价降低。

* 标出对您的品牌或促销活动至关重要的特定术语。

### 可在何处查看UI中有关约束的信息

除了打开[[!UICONTROL Constraints]视图](#constraints-view)之外，您还可以通过以下方式查看与您的约束相关的信息：

* 所有约束都是名为“[!UICONTROL Constraints]”的单个[标签分类](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/label-classifications/classification-about.html?lang=zh-Hans)的标签值。

   * “[!UICONTROL Constraints]”包含在默认和自定义视图设置以及计划报告的“[!UICONTROL Classifications]”列表中。 可随处添加列，以查看分配给相关实体的约束。

   * 当您下载批量处理工作表时，“[!UICONTROL Constraints]”在[!UICONTROL Download Bulksheet]”对话框中适用实体的“[!UICONTROL Classifications]”列下列出。 当包含列时，下载的批量工作表将包含分配给相关图元的任何约束。

  [!UICONTROL Constraints]分类未包含在[!UICONTROL Label Classifications]视图中 — [!UICONTROL Constraints]视图是独立的。 [!UICONTROL Constraints]分类也不包含在30个标签的分类限制中。

* [[!UICONTROL Constraint Report]](/help/search-social-commerce/reports/management/basic-advanced/constraint-report.md)包含使用标签分类架构的约束的成本、点击次数和（可选）转化数据。

### [!UICONTROL Constraints]视图 {#constraints-view}

[!UICONTROL Goals] > [!UICONTROL Constraints]视图列出了您的所有约束。 可用列包括限制状态；限制类型、开始和结束日期；与限制关联的促销活动、广告组、关键字、广告、投放位置、自动目标和产品组的数量；展示次数、点击量和成本数据；以及所有可见转化量度的收入数据。<!-- Clarify why "Ads" is listed, unless it's to identify the relevant ads -->

>[!IMPORTANT]
>
>[!UICONTROL Constraints]视图中的行的性能数据可能与为其分配约束的顶级实体的性能数据不匹配。 由于在最低级别分配的限制始终会覆盖在父级别分配的限制，因此分配给促销活动或广告组的限制可能不会始终分配给子广告组和关键字。 例如，如果为促销活动A分配了限制A，则促销活动A中的所有广告组和关键字会自动继承限制A。但是，这些广告组和关键字稍后可以分配给其他约束，例如约束B，然后它们就会失去与约束A的关联。

>[!NOTE]
>
>从相关实体管理视图（例如，营销活动级别约束的[!UICONTROL Campaigns]视图）将约束分配给竞价单位，并取消对它们的分配。

#### 可用操作

* [创建约束](#constraint-create)。

* [编辑约束设置](#constraint-edit)。

* [更改约束的状态](#constraint-change-status)。

## 创建约束 {#constraint-create}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Goals]>[!UICONTROL Constraints]**。

1. 在数据表上方的右上角工具栏中，单击&#x200B;**[!UICONTROL Create Constraint]**。

1. 输入[约束设置](#constraint-settings)。

   若要在[!UICONTROL Constraint Type]选项卡和[!UICONTROL Conditions]选项卡之间移动，请单击要打开的选项卡，或单击[!UICONTROL Next]和[!UICONTROL Back]按钮。

1. 单击&#x200B;**[!UICONTROL Review and Save]**&#x200B;以查看设置。

1. 单击&#x200B;**[!UICONTROL Save]**。

创建限制后，您可以[将其分配给促销活动、广告组、关键字、版面和单元级别的产品组](#constraint-assign)。

## 编辑约束设置 {#constraint-edit}

一次可以编辑一个约束的设置。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Goals]>[!UICONTROL Constraints]**。

1. （可选）从工具栏[&#128279;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)或[列标题](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)筛选列表。

1. 选中要编辑的约束旁边的复选框。

1. 在批量操作工具栏中，单击![编辑](/help/search-social-commerce/assets/edit-new.png "编辑")。

1. 编辑[约束设置](#constraint-settings)。

   若要在[!UICONTROL Constraint Type]选项卡和[!UICONTROL Conditions]选项卡之间移动，请单击要打开的选项卡，或单击[!UICONTROL Next]和[!UICONTROL Back]按钮。

1. 单击&#x200B;**[!UICONTROL Review and Save]**&#x200B;以查看设置。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 更改约束的状态 {#constraint-change-status}

您可以暂停任何活动约束以将其禁用。 您稍后可以通过将状态更改回&#x200B;*活动*&#x200B;来启用它。

您也可以删除约束，这将删除与帐户组件的所有关联，并使该约束不可用于将来使用。 限制的报表数据不再可用。 **注意：**&#x200B;若要仅解除限制与帐户组件的关联，请参阅“[从搜索竞价单位取消分配限制](#constraints-unassign)”。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Goals]>[!UICONTROL Constraints]**。

1. （可选）从工具栏[&#128279;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)或[列标题](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)筛选列表。

1. 选中每个状态要更改的约束旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在批量操作工具栏中，单击状态按钮：

   * 要激活所有选定的行，请单击![激活](/help/search-social-commerce/assets/activate-new.png "激活")。

   * 要暂停所有选定的行，请单击![暂停](/help/search-social-commerce/assets/pause-new.png "暂停")。

   * 要删除所有选定的行，请单击![删除](/help/search-social-commerce/assets/delete-new.png "删除")。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。

## 约束设置 {#constraint-settings}

| 选项卡 | 参数 | 描述 |
|---|---|---|
| \[基本信息\] | [!UICONTROL Constraint Name] | 约束的唯一名称。 |
| | [!UICONTROL Currency] | 任何适用的竞价单位竞价的币种。 将忽略使用不同货币的竞价单位。 |
| | [!UICONTROL Status] | 约束的状态：<ul><li>**活动：** （默认）约束在指定的条件和日期范围内应用。</li><li>**已暂停：**&#x200B;未应用约束。</li></ul> |
| [!UICONTROL Constraint Type] | [!UICONTROL Constraint Type] | 约束的类型。 有关限制类型和每个类型的合格广告网络的说明，请参阅“[限制类型](#constraint-types)”。 |
| | [!UICONTROL Start Date] | 约束生效的第一天。 默认值为当天。 若要更改日期，请输入日期或单击![日历](/help/search-social-commerce/assets/calendar-new.png "日历")以打开日历并选择日期。 |
| | [结束日期] | 限制是否将在特定日期失效。 要无限期地应用限制（例如，当竞价单位对于公司的品牌很重要时），请将此字段留空。 要在特定日期结束限制，请输入日期或单击![日历](/help/search-social-commerce/assets/calendar-new.png "日历")以打开日历并选择日期。 **注意：**&#x200B;该限制无法在明天之前过期。 |
| | [!UICONTROL Set constraint options for Bid] | （仅限[!UICONTROL Bid]个约束）设置包括：<ul><li>**[!UICONTROL Min Bid]：**&#x200B;相关竞价单位的最低基本竞价。</li><li>**[!UICONTROL Max Bid]：**&#x200B;相关竞价单位的最大基本竞价。</li></ul> |
| | [!UICONTROL Set constraint options for Bid Shift] | （仅限[!UICONTROL Bid Shift]个约束）要连续应用于基本竞价的竞价转移类型和金额：<ul><li>*[!UICONTROL Increases]：*&#x200B;按指定的百分比或货币值增加出价。 输入要更改的金额，然后选择&#x200B;*$*&#x200B;或&#x200B;*%*。 同时输入一个&#x200B;**[!UICONTROL Max Limit]**，它是应用约束时的最高可能出价（上限）。 **注意：**&#x200B;如果当前CPC竞价已等于或大于[!UICONTROL Max Limit]，则忽略该限制且不更改竞价。</li><li>*[!UICONTROL Decreases]：*&#x200B;按指定的百分比或货币值减少出价。 输入要更改的数量，然后选择&#x200B;*$或%*。 同时输入一个&#x200B;**[!UICONTROL Min Limit]**，这是应用约束时可能的最低竞价（下限）。 **注意：**&#x200B;如果当前CPC竞价已等于或小于[!UICONTROL Min Limit]，则忽略该限制且不更改竞价。</li></ul>**注释：**<ul><li>竞价转移将导致相关项目组合因竞价转移导致的总金额而超支或超支，而不考虑项目组合的“[!UICONTROL Spend Around Constraints]”设置。</li><li>如果您为约束指定了结束日期，并且优化功能正在自动调整项目组合中促销活动的支出限制，则竞价不会简单地恢复到结束日期之后的原始金额，而是会调整为最佳金额。</li><li>竞价班次不适用于数据不足无法生成成本和收入模型的竞价单位。</li></ul> |
| | [!UICONTROL Set constraint options for Incremental Bidding] | （仅限[!UICONTROL Incremental Bidding]个约束）竞价目标，以及递增或递减竞价到达到目标为止的次数和频率：<ul><li>**[!UICONTROL Bid target]：**&#x200B;目标竞价金额。</li><li>**[!UICONTROL Incrementally change bids by]**&#x200B;和&#x200B;**[类型]：**&#x200B;要增量增加或减少竞价的数目，以及按货币值(**$**)还是百分比(*%*)更改竞价。</li><li>**[!UICONTROL Every __ days]：**&#x200B;增量竞价的频率。</li></ul>例如，假设某个关键字的当前出价为100美分，并且您希望每天更改出价10%，直到达到500美分的出价目标为止。 在设置限制后的第1天，该关键字的竞价为110美分（当前竞价+ 10%）。 在第2天，出价为120美分（当前出价为第1天+ 20%），以此类推。 但是，如果竞价目标为50美分，而其他参数相同，则竞价会递减直至竞价达到50美分。 |
| | [!UICONTROL Set constraint options for Search Engine Min Bid] | （[!UICONTROL Search Engine Min Bid]个约束）使用在Google上搜索结果的第一页上显示竞价单位所需的最低竞价([!UICONTROL Google First Page CPC])。 （可选）输入&#x200B;**[!UICONTROL Min Bid]**&#x200B;值和/或&#x200B;**[!UICONTROL Max Bid]**&#x200B;值以定义约束的合格竞价范围。 例如，如果您指定[!UICONTROL Min Bid]为2.50 USD和[!UICONTROL Max Bid]为4 USD，那么如果[!DNL Google Ads]第一页竞价低于2.50 USD或高于4 USD，则您将不会对竞价单位投标。 |
| | [!UICONTROL Set constraint options for Impression Share] | （仅限[!UICONTROL Impression Share]个约束）设置包括：<ul><li>**[!UICONTROL Min Bid]** （可选）相关竞价单位的最低基本竞价。</li><li>**[!UICONTROL Max Bid]：**（可选）相关竞价单位的最大基本竞价。</li><li>**[!UICONTROL Min Impression Share]：**&#x200B;最低展示份额（百分比）将触发适用竞价单位的约束。 必须介于10和90之间。 **注意：**&#x200B;当约束不具成本效益时，优化功能可能会覆盖它。</li><li>**[!UICONTROL Max Impression Share]：**&#x200B;最高展示份额（百分比）将触发适用竞价单位的约束。 它必须介于10和90之间。**注意：**&#x200B;当约束不具成本效益时，优化功能可能会覆盖它。</li></ul>> |
| [!UICONTROL Conditions] | [!UICONTROL Condition Type] | 是否将条件应用于约束：<ul><li>*[!UICONTROL No Condition]：* （默认）在指定的日期范围内无条件应用约束。</li><li>*[!UICONTROL Satisfy]：*&#x200B;只有在指定的数据评估期间满足指定的条件时，才应用约束。</li></ul> |
| | [!UICONTROL Data Evaluation Period] | （设置条件时）为指定条件评估数据的时段。 如果选择&#x200B;*[!UICONTROL Custom date range]，*，请通过以`MM-DD-YYYY`格式输入每个日期（如2026年3月29日的03-29-2026）或单击![日历按钮](/help/search-social-commerce/assets/calendar-new.png "日历按钮")打开日历并选择每个日期来指定&#x200B;**[!UICONTROL Start Date]**&#x200B;和&#x200B;**[!UICONTROL End Date]**。 |
| | [!UICONTROL When to Apply Constraints] | （设置条件时）必须满足多少个筛选条件才能应用约束：<ul><li>*[!UICONTROL Match All Filters]：*&#x200B;在满足每个指定的筛选条件时应用约束。</li><li>*[!UICONTROL Match Any Filters]：*&#x200B;在至少满足一个指定的筛选条件时应用约束。</li></ul> |
| | [!UICONTROL Filters] | （设置条件时）必须满足的一个或多个标准。 要创建过滤器，请从列表中选择一个属性或量度。 对于属性（如[!UICONTROL Channel Type]），请在列表中选择适用的值。 对于量度（如[!UICONTROL Clicks]），请选择运算符，然后输入适用的值。 例如，要仅返回点击次数超过100次的竞价单位，请选择&#x200B;**点击次数**，选择&#x200B;**大于**，然后在输入字段中输入`100`。</li></ul> |

## 为搜索竞价单位分配约束 {#constraint-assign}

您可以将竞价单位限制应用于任何促销活动、广告组、关键字、投放位置、单位级别的购物产品组（最低级别的细分）或动态搜索目标。

每个图元只能有一个约束。 可将单个约束同时分配给一个或多个图元。

>[!NOTE]
>
>如果您稍后编辑广告的关键字或广告副本（从而创建新关键字或广告），则约束不会分配给新实体。

1. 从主菜单中，打开相关的管理视图。

   例如，要在营销活动级别分配约束，请转到[!UICONTROL Manage] > [!UICONTROL Campaigns]。

   <!-- for [campaigns](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md), [ad groups](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md), [keywords](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md), or [placements](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md). And ADD LINKS WHEN AVAILABLE for shopping product groups and dynamic search targets. -->

1. （可选）从工具栏[&#128279;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)或[列标题](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)筛选列表。

1. 选中要为其分配单个约束的每个图元旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**。

1. 选择约束。

1. 单击&#x200B;**[!UICONTROL Assign Now]**。

## 从搜索竞价单位中取消分配约束 {#constraints-unassign}

**注意：**&#x200B;要删除约束，使其不可用于将来使用，请参阅“[更改约束的状态](#constraint-change-status)”。

1. 在主菜单中，打开相关的管理视图。

   例如，要取消分配营销活动级别的约束，请转到[!UICONTROL Manage] > [!UICONTROL Campaigns]。

1. 选中要从中取消指定约束的每个图元旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**。

1. 单击&#x200B;**[!UICONTROL Confirm]**。

>[!MORELIKETHIS]
>
>* [管理营销活动的限制分配](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [管理广告组的限制分配](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [管理关键字的约束分配](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md)
>* [管理投放位置的约束分配](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md)
>* [该[!UICONTROL Constraint Report]](/help/search-social-commerce/reports/management/basic-advanced/constraint-report.md)
