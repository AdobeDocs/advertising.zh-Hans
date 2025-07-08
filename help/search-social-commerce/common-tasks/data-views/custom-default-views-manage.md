---
title: 管理默认视图和自定义视图
description: 了解如何自定义默认视图和自定义视图。
exl-id: 1f240760-6186-471f-bf1a-3e0ee13ce550
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: cb65108fcc60c11b901e3b43c292ad5a94192b9f
workflow-type: tm+mt
source-wordcount: '2917'
ht-degree: 0%

---

# 管理默认视图和自定义视图

<!-- Doesn't include instructions for legacy Portfolios or Reports views -->

您的默认视图和自定义视图允许您自定义在搜索促销活动数据视图内显示的性能数据。 视图设置包括要包含的列、筛选器、日期范围、转化归因设置和其他高级设置，您可以暂时应用设置或保存它们。 （例外：您不能为默认视图保存筛选器。） 每个默认视图和常规自定义视图仅适用于特定视图（如[!UICONTROL Portfolios]或[!UICONTROL Campaigns]）和特定广告商帐户。 在旧版用户界面中，每个通用自定义视图适用于特定广告商的实体视图，因此不能包括属性列（例如实体名称或状态），这些属性列因实体类型而异。

每次登录时默认显示视图。 您可以创建其他自定义视图并随时应用它们。 您可以选择与可以查看广告商数据的所有其他用户共享您创建的任何自定义视图。<!-- I no longer see this in the legacy CM views - why? -->在您的视图列表中，其他人员共享的每个视图都以斜体显示，如“*表现最佳的营销活动*”。 只有创建自定义视图的人员可以将其删除。

在旧版用户界面中，每个视图都作为快捷方式在左侧面板的[!UICONTROL Custom Views]部分中提供。

## 应用默认或自定义视图

### （新UI）将默认视图或自定义视图应用于管理视图

1. 在数据表上方，单击当前应用的视图的名称（![视图](/help/search-social-commerce/assets/view.png "视图")）。

1. 根据需要，单击任意选项卡（[!UICONTROL All Views]、[!UICONTROL Private]、[!UICONTROL Shared by Me]和[!UICONTROL From Others]）以查找视图。

1. 将光标悬停在视图名称上并单击&#x200B;**[!UICONTROL Apply]**。

### （旧版UI）将默认或自定义视图应用于营销活动管理视图

* （默认视图）在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]** \> **\[实体类型\]**。

* （自定义视图）从左侧导航面板：

   1. 在左侧面板中，单击&#x200B;**[!UICONTROL Custom Views]**&#x200B;菜单以展开它。

      视图按适用的实体排序。

   1. 展开可用菜单。

      “[!UICONTROL Universal Views]”包含可用于所有实体视图的自定义视图。 所有其他自定义视图按实体类型分组。

   1. 单击视图名称。

      如果视图是通用视图或应用于当前实体，则根据视图配置重新显示数据表。 如果视图应用于其他实体，则根据视图配置显示适用实体的数据。

## 创建自定义视图 {#create-custom-view}

<!--
## (New UI) Create a custom view from management views

*Available in the [!UICONTROL Simulations], [!UICONTROL Portfolios], [!UICONTROL Campaigns], and [!UICONTROL Ad Groups] views*

Custom views are specific to a single view (such as the [!UICONTROL Portfolios] view).

1. Above the data table, click the name of the currently-applied view (![View](/help/search-social-commerce/assets/view.png "View")).

2. Click **[!UICONTROL Create View]**.



-->

## （旧版UI）从营销活动管理视图创建自定义视图

自定义视图仅适用于营销活动管理视图。

>[!NOTE]
>
>除了为自定义视图指定的视图设置外，还会保存当前列排序顺序。

1. 在数据表上方的工具栏右侧，单击当前视图的名称（可能是“[!UICONTROL Default]”）。

1. 指定[自定义视图设置](#view-settings)：

   1. （可选）要使数据设置在所有实体视图（对于[!UICONTROL Campaigns]、[!UICONTROL Ads]等）中可用，请选择&#x200B;**[!UICONTROL Universal View]**。

      启用或禁用此选项后，不能将更改保存到现有视图，但可以使用更改创建新视图。

   1. （可选）若要使该视图对可以查看广告商数据的所有其他用户可用，请将&#x200B;**[!UICONTROL Shared]**&#x200B;滑块移动到&#x200B;*[!UICONTROL Yes]*。

   1. （可选）在&#x200B;**[!UICONTROL Columns]**&#x200B;选项卡上，更改可用于该选项卡的列、列的顺序以及行的排序方式。

   1. （可选）单击&#x200B;**[!UICONTROL Filters]**&#x200B;选项卡，然后指定要应用的任何筛选器。

      仅当量度的值满足指定的条件时，应用过滤器才会返回行，无论该量度是否作为列包含在报表中。

   1. （可选）单击&#x200B;**[!UICONTROL Date]**&#x200B;选项卡，然后更改默认日期设置。

   1. （可选）单击&#x200B;**[!UICONTROL Additional Settings]**&#x200B;选项卡，然后更改设置。

1. 单击&#x200B;**[!UICONTROL Save as New]**。

1. 输入新视图的名称，然后单击&#x200B;**[!UICONTROL Save]**。

   >[!TIP]
   >
   >使用有助于识别其所应用选项卡和信息的名称（例如“暂停的促销活动”或“前50个广告”）。

### 编辑默认或自定义视图

1. 打开视图设置：

   * （如果已应用视图）在数据表上工具栏的右侧，单击当前视图的名称（可能是“[!UICONTROL Default]”）。

   * （未应用的自定义视图）在左侧面板中，单击![自定义视图](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "自定义视图")以展开[!UICONTROL Custom Views]菜单。 单击自定义视图名称。

1. 编辑[视图设置](#view-settings)：

   1. （可选）要启用或禁用所有搜索实体视图（对于[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]等）中的数据设置，请选择或取消选择&#x200B;**[!UICONTROL Universal View]**。

      不能将更改保存到现有视图，但可以创建具有此更改的新视图。

   1. （可选；仅您创建的自定义视图）如果该视图尚未公开，请将&#x200B;**[!UICONTROL Shared]**&#x200B;滑块移动到&#x200B;*[!UICONTROL Yes]*&#x200B;以使其对可以查看广告商数据的所有其他用户可用。

   1. （可选）在&#x200B;**[!UICONTROL Columns]**&#x200B;选项卡上，更改可用于该选项卡的列、列的顺序以及行的排序方式。

   1. （可选）单击&#x200B;**[!UICONTROL Filters]**&#x200B;选项卡，然后编辑要应用的筛选器。

      仅当量度的值满足指定的条件时，应用过滤器才会返回行，无论该量度是否作为列包含在报表中。

      >[!NOTE]
      >
      >您可以将对筛选器的更改应用到默认视图设置，但不能保存更改。

   1. （可选）单击&#x200B;**[!UICONTROL Date]**&#x200B;选项卡并更改默认日期设置。

   1. （可选）单击&#x200B;**[!UICONTROL Additional Settings]**&#x200B;选项卡并更改设置。

1. 应用或保存设置：

   * 要暂时应用设置而不将其保存到视图，请单击&#x200B;**[!UICONTROL Apply]**。

     这些设置将应用于选项卡，直到您离开顶级管理视图或（如果适用）[查看其他广告商的数据](/help/search-social-commerce/common-tasks/change-advertiser.md)为止。

   * （对于您创建的默认视图和自定义视图）要将设置保存到当前视图，请单击&#x200B;**[!UICONTROL Save]**。

   * 要将设置保存到新的自定义视图中，请单击&#x200B;**[!UICONTROL Save As]**。 在[!UICONTROL Enter New Custom View Name]窗口中，输入新视图的名称，然后单击&#x200B;**[!UICONTROL Save]**。

## 将默认视图重置为系统默认设置

恢复默认视图设置将删除已保存的所有设置，并重新应用系统默认设置。

系统默认设置因选项卡而异。 对于大多数选项卡，系统默认视图显示启用帐户中处于活动状态的项目（例如，仅处于活动状态的促销活动中的活动广告组）的前一天数据，其中数据按成本排序，转化数据基于交易日期。

1. 在左侧面板中，单击![自定义视图](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "自定义视图")以展开[!UICONTROL Custom Views]菜单。

   视图按适用的实体排序。

1. 在视图名称旁边，单击![还原为默认设置](/help/search-social-commerce/assets/restore.png "还原为默认设置")。

## 删除自定义视图

您可以删除创建的任何自定义视图。

如果删除应用于当前选项卡的自定义视图，该选项卡将继续显示自定义视图，直到您移出视图集（例如，从[!UICONTROL Search]菜单中的视图移至[!UICONTROL Reports]菜单）或（如果适用）当您[查看其他广告商的数据](/help/search-social-commerce/common-tasks/change-advertiser.md)为止。

1. 在左侧面板中，单击![自定义视图](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "自定义视图")以展开[!UICONTROL Custom Views]菜单。

1. 将光标悬停在自定义视图名称上，然后单击![删除](/help/search-social-commerce/assets/delete.png "删除")。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Continue]**。

## 默认和自定义视图设置 {#view-settings}

| **选项卡** | **字段** | **描述** |
| --- | --- | --- |
| [在所有选项卡之上] | 名称 | 视图的唯一名称。 您无法编辑默认视图的名称。<p><b>提示：</b>请使用有助于识别所应用选项卡和信息的名称（如“暂停的促销活动”或“前50个广告”）。 |
|   | 通用视图 | 使数据设置在所有实体视图（营销活动、广告等）中可用。 通用视图可以包括量度和标签分类列，但不能包括属性列（例如实体名称和状态），因为它们按实体类型不同 — 以及所有其他视图属性也不同。 任何筛选条件都会应用到实体视图（如果适用），否则将被忽略。 所有量度过滤器都将在本地进行评估（例如，对于\> 1000次点击，促销活动视图显示超过1000次点击的促销活动，广告组视图显示超过1000次点击的广告组）。<p>通用视图的属性列是从实体的默认视图中提取的。 您可以在默认视图设置中更改特定实体的默认属性列。<p>启用或禁用此选项后，不能将更改保存到现有视图，但可以使用更改创建新视图。 |
|   | 共享 | （仅限自定义视图；可选）将该视图提供给可以查看广告商数据的所有其他用户。 其他用户无法编辑或删除视图，但他们可以从设置中创建新视图。 在您的视图列表中，其他人员共享的每个视图都以斜体显示，例如“_表现最佳的营销活动_”。 |
| 列 | 选定的列和排序 | 显示的数据列及其顺序：<ul><li> （要添加列）在“可用列”列表中，单击列名称，然后将其拖到“选定列和排序”列表中，或单击![向右箭头](/help/search-social-commerce/assets/chevron-right.png)将其移动到该处。</li><li>（要更改列的水平位置）在“所选列和排序”列表中，单击列名称，然后将其拖动到所需位置，或单击![向上箭头](/help/search-social-commerce/assets/chevron-up.png)或![向下箭头](/help/search-social-commerce/assets/chevron-down.png)将其移动到所需位置。 顶列的名称显示在左列。</li><li>（要删除列）在“选定的列和排序”列表中，单击列名称，然后将其拖到“可用的列”列表中，或单击![向左箭头](/help/search-social-commerce/assets/chevron-left.png)将其移动到该处。</li></ul><b>筛选数据</b><p>要仅列出特定类型的数据，请单击列表旁边的任何图标：<ul><li>搜索组件的属性名称和ID的![属性图标](/help/search-social-commerce/assets/properties-icon.png)，如状态</li><li>标准流量量度（例如展示次数和点击次数）的![流量图标](/help/search-social-commerce/assets/traffic-metrics-icon.png)</li><li>![收入图标](/help/search-social-commerce/assets/revenue-metrics-icon.png)（用于为广告商跟踪的转化量度，包括从Analytics同步的转化和网站参与量度）</li><li>![自定义图标](/help/search-social-commerce/assets/custom-metrics-icon.png) （适用于广告商创建的自定义派生量度）</li><li>![分类图标](/help/search-social-commerce/assets/classifications-icon.png)（用于标签分类）。</li></ul> <b>其他备注：</b><ul><li>要添加、创建或编辑新量度，请参阅“创建自定义量度”、“编辑自定义量度”和“删除自定义量度”。</li><li>如果报表包含使用不同货币的帐户的数据，则基于货币的列（例如成本和CPC）不包含总计。</li><li>您可以[从列标题菜单](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md)临时编辑列集，以及从[图标[!UICONTROL Columns]编辑和排序列集。 ](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md)（![列图标](/help/search-social-commerce/assets/custom-columns.png "列图标")）。</li></ul> |
|   | 排序方式 | 作为数据排序依据的列。 每种报表类型的默认值均不同。 |
|   | 排序顺序 | 是以&#x200B;**升序**&#x200B;还是&#x200B;**降序**&#x200B;顺序对数据排序。 移动滑块以选择一个选项。 |
| 过滤器 | [筛选器定义] | （可选）要应用于数据的过滤器。 仅当列的值满足指定的条件时，应用过滤器才会返回行。<p>对于要应用的每个过滤器：<ol><li>在“添加筛选器”菜单中，选择一个列名称。 该列表包含所有可用的列，并按列类型排序，属性列在前。</li><li>在列上定义过滤器</li></ol>（带有输入字段的筛选器）从第二个菜单中选择运算符，然后输入适用的值。 值不区分大小写。 完成后，单击![复选图标](/help/search-social-commerce/assets/select.png)。<p>例如，如果您选择了“点击量”列并且只想返回点击量超过100次的行，请选择&#x200B;_\>_&#x200B;并在输入字段中输入`100`。<p>根据数据类型，可用运算符可能包括<i>大于</i>、<i>小于</i>、<i>等于</i>、<i>包含</i>、<i>不包含</i>、<i>开头为</i>、<i>结尾为</i>、<i>无值</i>或<i>具有值</i> <i>在</i>之前、<i>在</i>之后，或<i>无日期</i>。<p>（不带输入字段的筛选器）单击“选择列表项”菜单旁边的![向下箭头](/help/search-social-commerce/assets/arrow-down-expand.png)，然后选中要包含的每个值旁边的复选框。 完成后，单击![复选图标](/help/search-social-commerce/assets/select.png)。<p><b>注释：</b><ul><li>您可以将对筛选器的更改应用到默认视图设置，但不能保存更改。</li><li>您还可以在视图中[临时更改适用的筛选器](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)。</li></ul> |
|   | 仅包含具有性能数据的行 | （仅限广告组、关键字、产品组、投放位置和自动定位视图） <p>仅包含指定日期期间具有性能数据的行。 默认情况下，选择此选项可缩短页面加载时间。 <p><b>警告</b>：如果取消选择该选项，并且视图包含许多没有性能数据的实体，则显示数据所需的时间会更长。<p> <b>注意</b>：您可以应用对筛选器的更改，但不能将更改保存到默认视图设置。 默认视图始终仅显示具有性能数据的实体。 |
| 日期 | 日期范围 | (当选择“Include date range”（包含日期范围）时)<p>要为其生成数据的日期范围。 选择一个选项：<ul><li><i>[预设范围]</i>：常用时间增量列表，范围从<i>今天</i>到<i>最近180天</i>。 从列表中选择一个；默认值是<i>昨天</i>。 注意：<i>上个月</i>、<i>最近3个月</i>和<i>最近6个月</i>显示前一个日历月份的数据。</li><li><i>自定义日期范围：</i>指定开始日期和结束日期。 以YYYY/MM/DD或M/D/YYYY格式输入日期，或单击字段旁边的![日历图标](/help/search-social-commerce/assets/calendar.png)并选择日期。</li></ul> |
|   | 比较 | 将指定日期范围的数据与第二个日期范围的数据进行比较。 选择此选项时，将为每个常规数据列添加两个额外的列。 例如，报表不仅包括“展示次数”的一列，还包括“展示次数范围1”、“展示次数范围2”和“展示次数差异”的列。<p><b>注释：</b><ul><li>对于派生量度，不显示“差异”列。</li><li>比较大日期范围的报表可能需要更长的时间才能生成。</li></ul> |
|   | 比较格式 | 如何表示“[_数据字段_]&#x200B;差异”列中两个选定日期范围中的数据之间的差异。 选择一个选项：<ul><li><i>差异</i>（默认值）：将差异显示为数值。</li><li><i>%更改</i>：以百分比显示差异。</li></ul> |
| 其他设置 | 使用默认值 | 应用在广告商级别的转化归因设置中指定的归因设置。 |
|   | 归因规则 | (仅限使用Adobe Advertising基于像素的转化跟踪服务的广告商)在选项卡中，如何在一系列导致转化的事件中归因转化数据（可能跨多个广告渠道和项目组合）。 默认情况下，将选择在广告商级别转化归因设置中指定的规则。<ul><li> <i>第一个事件</i>：将转化归因于广告商的点击回顾时间范围内的系列中的第一个付费点击，如果没有发生付费点击，则归因于广告商的展示回顾时间范围内的最后一个展示。</li><li><i>权重第一个事件更多</i>：将转化归因于在广告商的点击回顾窗口和展示回顾窗口内发生的系列中的所有事件，但给予第一个事件的权重最大，随后给予以下事件的权重较小。 当转换之前同时有付费点击和展示时，指定的展示覆盖权重进一步应用于展示。 当转换之前只有印象时，根据广告商的浏览权而不是印象覆盖权对印象进行加权。</li><li><i>均匀分布</i>：将转化平均归因于在广告商的点击回顾窗口和展示回顾窗口内发生的系列中的每个事件。 当转换之前同时有付费点击和展示时，指定的展示覆盖权重进一步应用于展示。 当转换之前只有印象时，根据广告商的浏览权而不是印象覆盖权对印象进行加权。</li><li><i>权重最后一个事件更多</i>：将转化归因于在广告商的点击回顾窗口和展示回顾窗口内发生的系列中的所有事件，但会给予最后一个事件最大的权重，并依次减少对前面事件的权重。 当转换之前同时有付费点击和展示时，指定的展示覆盖权重进一步应用于展示。 当转换之前只有印象时，根据广告商的浏览权而不是印象覆盖权对印象进行加权。</li><li><i>上次事件</i>（默认）：将转化归因于广告商的点击回顾窗口内系列中的上次付费点击，如果未发生付费点击，则归因于广告商的展示回顾窗口内的上次展示。</li><li><i>U形</i>：将转化归因于在广告商的点击回顾窗口和展示回顾窗口内发生的系列中的所有事件，但将最大权重赋予第一个事件和最后一个事件，依次减少对转化路径中间事件的权重。 当转换之前同时有付费点击和展示时，指定的展示覆盖权重进一步应用于展示。 当转换之前只有印象时，根据广告商的浏览权而不是印象覆盖权对印象进行加权。</li></ul><p><b>注释：</b><ul><li>除上一个事件之外，所有归因规则仅适用于具有Adobe Advertising点击跟踪以及来自Adobe Advertising或Adobe Analytics的转化跟踪（与Analytics集成）的广告商。</li><li>归因规则适用于任何渠道中的付费广告点击次数。 它们不适用于付费搜索广告的展示次数，此类展示次数无法在事件级别进行跟踪。</li><li>当您使用任何归因规则（一个“最后一个事件”规则除外）报告转化数据时，导致转化的事件可能会发生在多个项目组合中。 如果是这样，则仅当这些组合中的广告或关键字包含在视图中时，视图才会包含转化数据。</li><li>对于默认视图，我们建议您保留默认归因规则，该规则用于在竞价优化期间计算每个竞价单位的[目标值](/help/search-social-commerce/glossary.md#o-p)（以前称为“加权收入”）。</li></ul> |
|   | 转化基于 | 如何报告转化数据：<ul><li><i>交易日期</i>（默认值）：查看交易日期在指定时间段内发生的交易。 这表示在指定的时间段内赚取的收入。</li><li><i>单击日期</i>：查看在指定时间段内发生的单击所导致的交易。 当项目组合在点击和交易之间存在重大延迟时，此选项可用于计算项目组合的每次点击历史收入，它指示一段时间内预期的收入行为。 |
