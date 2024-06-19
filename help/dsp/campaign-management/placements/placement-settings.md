---
title: 投放设置
description: 请参阅可用版面设置的说明。
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: 74b7ccc97339663c8baba633ff2baedfb13cba80
workflow-type: tm+mt
source-wordcount: '3789'
ht-degree: 0%

---

# 投放设置

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** 投放位置名称。

>[!TIP]
>使用适合您情况的命名约定。 一个建议的命名惯例是“*\&lt;campaign name=&quot;&quot;>： \&lt;ad unit=&quot;&quot;>： \&lt;duration>： \&lt;targeting>*“

**[!UICONTROL Status]：** 投放状态： *[!UICONTROL Active]* （默认）或 *[!UICONTROL Paused]*.

>[!TIP]
>最佳实践是暂停投放位置，直到您准备好启动它。

**[!UICONTROL Details]：** （只读）适用的广告类型、创建或创建投放位置的帐户以及父营销活动。 要查看更多详细信息，请单击 **[!UICONTROL Show more]**.

**[!UICONTROL Templates]：** 打开现有版面模板的列表。 要从模板自动填充定位设置，请执行以下操作：

1. 执行以下任一操作：

   * 要重用模板中的所有目标，请选中模板名称旁边的复选框。

   * 要重用模板中的各个目标类型，请展开模板名称并选中要重用的目标类型旁边的复选框。

1. 单击 **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]：** （仅限视频广告格式）广告持续时间和/或广告规范，用于计算右侧的“预测”投影。 这些字段因广告类型而异。

**[!UICONTROL Environment]：** （仅限通用视频广告格式）要作为定位目标包含在投放位置中的设备环境（桌面、移动设备、联网电视）。 请至少指定一个。

在自定义报表中，放置级别维度“设备环境”表示目标环境。

**[!UICONTROL Placement tags]：** （可选）关键字或昵称可帮助您定位此位置。

## 目标

**[!UICONTROL Package]：** （可选）为其分配版面的资源包。 单击 ![编辑](/help/dsp/assets/edit.png) 选择现有包或创建包。 将投放位置分配给资源包时， [!UICONTROL Goals] 部分已更新程序包中的投放日期、投放目标和预算。

**[!UICONTROL Flight Dates]：** 投放的开始日期和结束日期。 当投放位置处于活动状态并分配给活动包或营销活动时，批准的广告有资格在投放过程中运行。

默认情况下，会自动填充资源包（如果适用）或营销活动的日期。

>[!NOTE]
>
>* 投放日期必须包含在营销活动投放日期和包投放日期中。

### 分配给具有包级别步调的包的位置

**[!UICONTROL Placement Funding]：** 如何为投放编列预算：

* *[!UICONTROL Optimize based on performance]：* 控制包级别的预算。
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]：* 允许您设置最小和/或最大置入预算。 至少指定一种预算类型：

   * *[!UICONTROL Maximum Budget]*：输入值和持续时间(*[!UICONTROL All time]*， *[!UICONTROL Daily]*， *[!UICONTROL Weekly]*， *[!UICONTROL Monthly]*)。

   * *[!UICONTROL Minimum Budget]*：最小预算占包预算的百分比。 当指定间隔上限时，最小预算值始终计算为间隔上限的百分比。 否则，它将计算为包预算的百分比。

**[!UICONTROL Max Bid]：** 为1000次展示支付的最大值。

**[!UICONTROL Placement Pre-bid Filters]：** 必须满足才能进行竞价的最多五个KPI阈值（例如最低可见性量度或点进率）。 您可以将预竞价筛选器用作优化策略，但请注意，每个规则都可能会限制此投放位置可以竞价的机会。 添加或编辑筛选器：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 执行以下任一操作：
   * 要添加过滤器，请执行以下操作：
      1. 单击 **[!UICONTROL Add Filter]**.
      1. 旁边 **[!UICONTROL Only bid if]**，选择一个量度，然后输入一个值。
   * 要删除过滤器，请单击 **[!UICONTROL X]** 在筛选行中。
1. 单击 **[!UICONTROL Save]**.

请参阅“ ”上每个预竞价过滤器的说明[投放位置级别预竞价过滤器及其使用方式](/help/dsp/optimization/optimization-pre-bid-filters.md)“

### 所有其他版面

**[!UICONTROL Budget Goal]：** 总预算上限和预算间隔(*[!UICONTROL All time]*， *[!UICONTROL Daily]*， *[!UICONTROL Weekly]*， *[!UICONTROL Monthly]*)。

**[!UICONTROL Gross Budget Goal]：** （仅具有利润管理的营销活动中的投放位置）总预算上限和预算间隔(*[!UICONTROL All time]*， *[!UICONTROL Daily]*， *[!UICONTROL Weekly]*， *[!UICONTROL Monthly]*)。

**[!UICONTROL Optimization Goal]：**  包的优化目标。 请参阅“ ”上每个优化目标的说明[优化目标及其使用方式](/help/dsp/optimization/optimization-goals.md)“。

**[!UICONTROL Target Goal]：** 用于跟踪性能的目标目标。

>[!NOTE]
>
>此字段只是一个基准，不用于决策。

**[!UICONTROL Pace on]：** 步调的基础：

* **[!UICONTROL Budget goal]：** （默认）此选项会在分配的预算内尽可能多地提供展示次数。

* **[!UICONTROL Impressions]：** 此选项会一直提供展示次数，直到在指定间隔内达到指定数量为止。 选择此选项时，请指定展示次数和间隔： *[!UICONTROL All time]，* *[!UICONTROL Daily]，* *[!UICONTROL Monthly]，* 或 *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]：** 为1000次展示支付的最大值。

**[!UICONTROL Flight pacing]：** （仅限具有投放级别步调的投放）如何安排广告投放的步调：

* *[!UICONTROL Even]：* （默认）在每次飞行中统一安排投放，目标是在飞行前半段投放的50%。

* *[!UICONTROL Slightly Ahead]：* （默认）加快投放，使其在飞行时间的半程完成55-65%。

* *[!UICONTROL Frontload]：* 加速投放，使其在飞行中途完成65-75%。

* *[!UICONTROL Aggressive Frontload]：* 加速投放，使其在飞行中途完成75-85%。

**[!UICONTROL Intraday pacing]：** （仅限具有投放级别步调的投放）如何在投放中安排每天的广告投放步调：

* *[!UICONTROL Even]：* （默认）根据库存可用性调整交付。 通常，在拍卖量较高的白天，每小时会投放更多广告，而在早上和晚上投放的广告会更少。

* *[!UICONTROL ASAP]：* （默认）将投放速度加快到两倍 *平衡*.

  >[!CAUTION]
  >
  >此选项可能会对性能产生负面影响。 仅在您完全优先考虑投放并花费超过性能优化的时间时才使用它。

**[!UICONTROL Placement Pre-bid Filters]：** （可选）要发出竞价，最多必须满足五个过滤器。 您可以将预竞价筛选器用作优化策略，但请记住，每个规则可能会限制此投放位置可以竞价的机会。 添加或编辑筛选器：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 执行以下任一操作：
   * 要添加过滤器，请执行以下操作：
      1. 单击 **[!UICONTROL Add Filter]**.
      1. 旁边 **[!UICONTROL Only bid if]**，选择一个量度，然后输入一个值。
   * 要删除过滤器，请单击 **[!UICONTROL X]** 在筛选行中。
1. 单击 **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]：** （可选）要在投放位置中包含或排除广告的特定位置。 如果不指定任何位置，则会定向所有位置。

>[!NOTE]
>
>城市和DMA位置不适用于Roku投放。

要指定位置，请执行以下操作：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 执行以下任一操作：
   * 要包含或排除国家、州、市、DMA、联邦立法区或州立法区，请执行以下操作：
      1. 在左列中选择位置类型。
      1. （根据需要）单击某个位置以展开该位置。
      1. 在位置旁边，单击 *[!UICONTROL Include]* 将其包含为目标或 *[!UICONTROL Exclude]* 将其作为目标排除。
   * 要搜索邮政编码并包含或排除所有选定的结果，请执行以下操作：
      1. 单击 **[!UICONTROL Search Postal Code]**.
      1. 选择国家/地区。
      1. 输入城市名称，然后单击 ![编辑](/help/dsp/assets/search.png).
      1. 单击正确的搜索结果。
      1. 单击 *[!UICONTROL Include All]* 以包含所有位置作为目标或 *[!UICONTROL Exclude All]* 以排除所有位置作为目标。
   * 要输入或粘贴邮政编码，并包含或排除所有邮政编码，请执行以下操作：
      1. 单击 **[!UICONTROL Paste Postal Code]**.
      1. 选择国家/地区。
      1. 输入或粘贴最多1000个邮政编码。
每行包括一个邮政编码，或者输入多个值，以逗号或制表符分隔。
      1. 单击 *[!UICONTROL Include All]* 以包含所有位置作为目标或 *[!UICONTROL Exclude All]* 以排除所有位置作为目标。
   * 要从 [!UICONTROL Included] 或 [!UICONTROL Excluded] 列表，单击 **[!UICONTROL X]** 右列的位置旁边。
1. 单击 **[!UICONTROL Done]**.

>[!NOTE]
>
>* 并非所有国家/地区都有省/市/自治区或邮政编码位置。
>* DMA（指定市场区域）、联邦立法区和州立法区仅适用于美国地区。

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]：** 作为目标包含或排除的清单源。 对于大多数置入类型，默认情况下包括所有库存类型以及每种类型的所有来源。 对象 [!DNL Roku] 投放位置，您必须指定库存类型和来源。 您可以从以下库存类型中进行选择：

* [!UICONTROL Public]：（除Roku之外的所有放置类型）DSP有权访问的所有未结Exchange库存。 您可以包含和排除公共清单。

  您可以按源或信息源查看列表。 在按信息源查看列表时，您可以按信息源名称、信息源密钥或选定的特征标记进行搜索。

* [!UICONTROL Private] | [!UICONTROL Roku Private]：您现有的私人交易（或现有的私人交易） [!DNL Roku] 交易： [!DNL Roku] （广告投放位置）以及您已在DSP中设置的发布者。 您可以包括（但不排除）公共库存。

  您可以按关键词、键值、交易ID或自定义标记搜索列表。

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*：（可选）覆盖竞价算法以至少对交易的固定价格和最低价格出价。

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]：全部 [溢价，无担保 [!UICONTROL On Demand] 库存](/help/dsp/inventory/on-demand-inventory-about.md) (或 [!UICONTROL On Demand] [!DNL Roku] 交易： [!DNL Roku] 您已订阅的) [!DNL DSP]. 您可以包含和排除 [!UICONTROL On Demand] 库存。

  您可以按源或信息源查看列表。 在按信息源查看列表时，您可以按信息源名称、信息源键或选定的发布者区域、类别标记或特征标记进行搜索。

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*：（可选）覆盖竞价算法以至少对交易的固定价格和最低价格出价。

要指定库存定位，请执行以下操作：

* 要排除清单类型，请清除名称旁边的复选框。
* 要定位库存类型，请执行以下操作：
   1. 选中清单类型名称旁边的复选框。
   1. （可选）更改源以包括：
      1. 单击 ![编辑](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] 和 [!UICONTROL On Demand] inventory)单击 **[!UICONTROL View by Source]** 或 **[!UICONTROL View by Feed]** 以更改源的列出方式。
      1. （适用时）根据需要筛选库存。
      1. 指定要包含和排除的源：
         * 要包含 [!UICONTROL Public] 或 [!UICONTROL On Demand] 源，单击 **[!UICONTROL Include]** 在源名称旁边。
         * 要包含 [!UICONTROL Private] 源：
            * 要在交易中包含所有库存，请单击 **[!UICONTROL Include all]** 在交易名称旁边。
            * 要包含单个库存来源，请展开交易名称，然后单击来源名称旁边的复选框。
         * 要排除 [!UICONTROL Public] 或 [!UICONTROL On source]，单击 **[!UICONTROL Exclude]** 在源名称旁边。
   1. （可选）要将包含定向信息的CSV文件下载到浏览器的下载位置，请单击 **[!UICONTROL Save & Export]**.
   1. 单击 **[!UICONTROL Save]**.

>[!TIP]
>
>如果您订阅了 [!UICONTROL On Demand] 清点，但找不到要定位的出版商或交易，然后检查交易的状态。 有关状态的更多信息，请参阅 [关于 [!DNL On Demand] 高级库存](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]：** （仅限视频投放）不包括出站流量。

流输出广告通常以弹出窗口或填充到内容中（在本机体验中）的形式出现，而不是在视频播放器中以常规视频广告的形式出现。

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]：** 要定位的流量类型。 选项包括 **[!UICONTROL Websites]** 和 **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]：** (可用时间 **[!UICONTROL Paste list of targeted sites]** 是 *[!UICONTROL Off]*)要定位的站点的质量。 第1层至第3层均符合品牌安全要求，并已由DSP映射团队进行审查和批准。

* *[!UICONTROL Tier 1]：* 全国知名的高端网站和应用程序。

* *[!UICONTROL Tier 2]：* 定位第1层以及知名度低于第1层的优质站点和应用程序。

* *[!UICONTROL Tier 3]：* 定位第1层至第2层以及符合特定受众要求的合法且品牌安全的站点和应用程序。 使用第3层进行覆盖或数据定位购买。

* *[!UICONTROL All Sites]：* 定位第1-3层以及尚未进行筛选或分类的新库存，您可以将这些库存用于范围。

>[!NOTE]
>
>库存特定于投放位置中的广告单元。

>[!TIP]
>
>对于性能营销活动，最佳实践是选择 *[!UICONTROL All Sites]*.

**[!UICONTROL Site Categories]：** (可选；在以下情况下可用： **[!UICONTROL Paste list of targeted sites]** 是 *[!UICONTROL Off]*)选定站点层中的站点类别，以包含或排除（但不能同时包含和排除）作为目标。 从DSP已根据主题映射的垂直网站列表中进行选择：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 指定要包含或排除的站点类别：
   * 要包含站点类别，请执行以下操作：
      1. 单击 **[!UICONTROL Include categories]**.
      1. 选中每个要定位的类别旁边的复选框。
   * 要排除站点类别，请执行以下操作：
      1. 单击 **[!UICONTROL Exclude categories]**.
      1. 选中要排除的每个类别旁边的复选框。
1. （可选）要将包含定向信息的CSV文件下载到浏览器的下载位置，请单击 **[!UICONTROL Export]**.
1. 单击 **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]：** (可选；在以下情况下可用： **[!UICONTROL Paste list of targeted sites]** 是 *[!UICONTROL Off]*)要排除的站点。 您可以搜索并选择站点，或者输入或粘贴域名：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 指定站点：
   * 要搜索站点：
      1. 单击 **[!UICONTROL Search]**.
      1. 输入关键字、选择站点层和/或选择站点类别。
      1. 在搜索结果中，选择要排除的站点：
         * 要排除单个站点，请选中相邻复选框。
         * （当可用结果超过50个时）要排除前50个结果，请单击 **[!UICONTROL Exclude these 50]**. 要排除所有搜索结果，请单击 **[!UICONTROL Exclude these \<*NN *\>]**.
   * 要输入域名，请执行以下操作：
      1. 单击 **[!UICONTROL Paste]**.
      1. 在单独行中输入一个或多个域名。
      1. 单击 **[!UICONTROL Exclude All]**.
1. 单击 **[!UICONTROL Done]** 等你完事了。

>[!NOTE]
>
>* 除了DSP之外，还会应用帐户级别和广告商级别的阻止网站列表 [全局阻止的站点列表](/help/dsp/introduction/features/brand-safety-media-quality.md)，其中包括被认为不安全的广告网站。
>* 阻止的站点列表始终覆盖目标站点列表。 如果投放位置同时排除并包含广告的相同目标，则排除该目标。

**[!UICONTROL Language]：** （可选）要定位的单一语言。

**[!UICONTROL Site List Preview]：** （只读）投放的所有已定向和阻止的站点。

您可以选择将目标和阻止站点的列表导出为逗号分隔值(CSV)文件。 要导出列表，请单击 **[!UICONTROL Export full site list]**，然后按照浏览器的正常过程打开或保存文件。

**[!UICONTROL Allow unscreened sites]：** （仅限标准显示投放位置）在未审核站点上启用广告投放。 当投放以私人库存为目标时，此选项可能会在阻止的网站上投放广告。

**[!UICONTROL Paste list of targeted sites]：** 仅允许您定位特定站点。 启用此选项后，将禁用其他站点定位选项。

**[!UICONTROL Sites]：** (可用时间 **[!UICONTROL Paste list of targeted sites]** 是 *[!UICONTROL On]*)要定位的站点。 您可以搜索并选择站点，或者输入或粘贴域名：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 指定站点：
   * 要搜索站点：
      1. 单击 **[!UICONTROL Search]**.
      1. 输入关键字、选择站点层和/或选择站点类别。
      1. 在搜索结果中，选择要包含的站点：
         * 要排除单个站点，请选中相邻复选框。
         * （当可用结果超过50个时）要包含前50个结果，请单击 **[!UICONTROL Include these 50]**. 要包含所有搜索结果，请单击 **[!UICONTROL Include these \<*NN *\>]**.
   * 要输入域名，请执行以下操作：
      1. 单击 **[!UICONTROL Paste]**.
      1. 在单独行中输入一个或多个域名。
      1. 单击 **[!UICONTROL Include All]**.
1. 单击 **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]：** 投放位置的任何受众目标，包括 [第三方区段、第一方区段、Adobe区段、自定义区段和已保存的受众](/help/dsp/audiences/audience-settings.md). 此外，还会显示所有选定区段和已保存受众中经过重复数据删除的总受众大小和活动受众大小。 您可以选择现有受众，创建以后可以重复使用的受众，或者选择特定的受众区段：

* 要选择现有受众，请单击 ![选择](/help/dsp/assets/chevron-down.png) 旁边 [!UICONTROL Included Audiences]，然后选择受众。
* 要创建受众，请单击 ![选择](/help/dsp/assets/chevron-down.png) 旁边 [!UICONTROL Included Audiences]，然后选择 **[!UICONTROL + Create Audience]**. 有关说明，请参阅 [创建可重复使用的受众](/help/dsp/audiences/reusable-audience-create.md)，从步骤3开始。
* 要选择特定的受众区段，请单击 **[!UICONTROL Select segments for this placement only]**. 选择区段逻辑；有关说明，请参阅&quot;[创建可重复使用的受众](/help/dsp/audiences/reusable-audience-create.md)“ 完成后，单击 **保存**.

**[!UICONTROL Excluded Audiences]：** 要针对投放位置排除的任何受众，包括满足以下条件的受众： [第三方区段、第一方区段、Adobe区段、自定义区段和已保存的受众](/help/dsp/audiences/audience-settings.md). 此外，还会显示所有已排除受众中经过重复数据删除的总受众人数和活动受众人数。 您可以选择现有受众，也可以创建一个以后可以重复使用的新受众：

* 要选择现有受众，请单击 ![选择](/help/dsp/assets/chevron-down.png) 旁边 [!UICONTROL Excluded Audiences]，然后选择受众。

* 要创建受众，请单击 ![选择](/help/dsp/assets/chevron-down.png) 旁边 [!UICONTROL Excluded Audiences]，然后选择 **+创建受众**. 有关说明，请参阅 [创建可重复使用的受众](/help/dsp/audiences/reusable-audience-create.md)，从步骤3开始。

**[!UICONTROL Targeting]：** 要定位的用户ID的类型。 在投放开始后（即，在投放开始后），无法更改此设置。

当您同时选择旧版ID和通用ID时，会为通用ID提供竞价偏好设置。

* *[!UICONTROL Legacy IDs (Cookies, MAIDS, CTV)]*：（默认）根据用户的Cookie、移动广告ID或连接的电视(CTV) ID定位用户。 根据浏览器、应用程序内或CTV清单选择ID。

* *[!UICONTROL Universal ID Beta]*：定位注重隐私的用户ID；选择一种ID类型。 可用的选项由以下区域中所选的地理目标决定： [!UICONTROL Geo-Targeting] 部分。 使用和 [[!DNL RampID] 直接导入到DSP的区段](/help/dsp/audiences/sources/source-import-liveramp-segments.md)， [DSP将PII转换为通用ID的区段](/help/dsp/audiences/sources/source-about.md)，或 [跟踪通用ID的自定义区段](/help/dsp/audiences/custom-segment-create.md).

   * *[!UICONTROL ID5]*：目标 [!DNL ID5] 根据电子邮件地址和其他信号概率创建的ID。<!-- What countries/geos are these available for? Everywhere?--> ID5 ID免费提供。 **注意：** 来自的第三方区段 [!DNL Eyeota] 可能包括ID5 ID。

   * *[!UICONTROL RampID]*：目标 [!DNL LiveRamp] [!DNL RampIDs] ，即使用他们的电子邮件地址登录到您网站的用户的数量。<!-- Verify --> [!DNL RampIDs] 适用于北美、澳大利亚和新西兰的用户。

   * *[!UICONTROL Unified ID2.0]*：目标 [!DNL Unified ID2.0] (UID2)使用用户的电子邮件地址登录到您的网站的ID。<!-- Verify -->[!DNL UID2 IDs] 不适用于欧洲经济区和其他一些国家的用户。 请参阅 [被禁止的国家/地区列表](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

  **[!UICONTROL Terms of service]**：使用通用ID的服务协议条款。 您或DSP帐户中的其他用户必须接受一次这些条款，然后才能将数据转换为新的ID类型。 对于签订托管服务合同的客户，您的Adobe客户团队将代表贵组织获得您的同意并接受相关条款。 要阅读术语，请单击 **>**. 要接受条款，请滚动到条款的底部并单击 **[!UICONTROL Accept]**.

**[!UICONTROL Cross Device Targeting]：** (在以下情况下可用： [营销活动配置为基于人员的跨设备定位](/help/dsp/campaign-management/campaigns/campaign-settings.md)，则只需定位旧版ID（而非通用ID），并且至少选择一个区段或受众。 允许您将定位扩展到用户的所有已知设备（根据促销活动设置中指定的设备图），甚至扩展到不在指定区段中的设备。 根据为营销活动指定的图表，可能会收取相关费用。 设备图数据仅在北美地区可用。

**[!UICONTROL Placement Cap]：** （可选）独特设备、通用ID或人员(取决于指定的 [!UICONTROL Cross Device Level] 促销活动和投放位置的 [!UICONTROL Targeting] 设置)可以从投放位置提供广告。 选项包括 *[!UICONTROL Unlimited]* 或每天、每周或每月的特定金额。

>[!NOTE]
>
> 您可以在营销活动、包和投放级别设置频率上限。 DSP遵循营销活动层次结构中最严格的频率限制。

**[!UICONTROL Secondary Cap]：** (可选；在包含数值时可用 [!UICONTROL Placement Cap])在主放置顶盖范围内的附加限制。 选择展示次数和时间段（例如，每12小时3次）。

**[!UICONTROL Day Parting]：** （可选）在一周中的特定日期和广告在一天中的特定时间运行。 要指定时段间隔，请执行以下操作：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 选择适用的时区。
1. 指定间隔：
   * 要选择预设间隔，请单击其中一个间隔按钮。 选项包括*[!UICONTROL Weekends]**， *[!UICONTROL Weekdays]*， *[!UICONTROL Morning]*， *[!UICONTROL Lunch]*， *[!UICONTROL Dinner]*，或 *[!UICONTROL Prime]* (primetime)。
   * 要手动选择间隔，请单击单元格内部，也可以拖动以选择间隔。
1. 单击 **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]：** (可选；适用于配置了以下各项的广告商： [!DNL Proximic by Comscore] 和 [!DNL Grapeshot] 区段)中的特定区段名称或ID [!DNL Proximic by Comscore] 和 [!DNL Grapeshot] 以包含为目标。 此功能可能需要额外付费。 要激活此功能并设置主题区段，请联系您的Adobe客户团队。

要指定主题定位，请执行以下操作：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 指定要定位的区段：
   1. 在左列中，选择合作伙伴(*[!UICONTROL Comscore]* 或 *[!UICONTROL Grapeshot]*)。
   1. 在输入字段中输入区段名称或区段ID。
1. （可选）要将包含主题信息的CSV文件下载到浏览器的“下载”位置，请单击 **[!UICONTROL Export]**.
1. 单击 **[!UICONTROL Save]**.

>[!TIP]
>
>* 主题定位限制了投放位置可以竞价的库存，因此使用主题定位仅占您总体购买的一小部分。
>
>* 在上设置区段中的任何负面定位 [!DNL Proximic by Comscore] 或 [!DNL Grapeshot].

**[!UICONTROL Device Targeting]：** （可选）要作为目标包含和排除的特定设备信息，包括设备类型、制造商、操作系统、浏览器和连接类型。 要指定设备定位，请执行以下操作：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 指定要包含和排除的设备详细信息：
   1. 在左列中，选择类别。
   1. 指定定位：
      * 要包含值，请单击 **[!UICONTROL Include]** 值名称旁边。
      * 要排除值，请单击 **[!UICONTROL Exclude]** 值名称旁边。
1. （可选）要将包含设备定向信息的CSV文件下载到浏览器的下载位置，请单击 **[!UICONTROL Export]**.
1. 单击 **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]：** （可选）特定互联网服务提供商(ISP)，以将目标包括或排除（但不能同时包括两者）作为目标。 要指定ISP定位，请执行以下操作：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 指定要包含或排除的ISP：
   * 要包括ISP，请执行以下操作：
      1. 单击 **[!UICONTROL Include ISPs]**.
      1. （可选）按关键字筛选列表。
      1. 选中每个要定位的ISP旁边的复选框。
   * 要排除ISP：
      1. 单击 **[!UICONTROL Exclude ISPs]**.
      1. （可选）按关键字筛选列表。
      1. 选中要排除的每个ISP旁边的复选框。
1. （可选）要将包含ISP定位信息的CSV文件下载到浏览器的下载位置，请单击 **[!UICONTROL Export]**.
1. 单击 **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]：** 类型 [!DNL Comscore]， [!DNL DoubleVerify]， [!DNL Integral Ad Science]、和 [!DNL Peer39] 要应用的上下文过滤器。 为新投放位置选择了广告商级别的默认值，但您可以更改设置：

* [!UICONTROL DoubleVerify]：

   * **[!UICONTROL Block sites that are]：** （可选）默认情况下阻止一种或多种类型的库存上下文。 可能需额外付费。

* [!UICONTROL Peer 39]：

   * **目标站点：** （可选）默认情况下，要定位一种或多种类型的库存属性。 可能需额外付费。

* [!UICONTROL ComScore]：

   * **阻止满足以下条件的站点：** （可选）默认情况下阻止一种或多种类型的库存属性。 可能需额外付费。

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]：** （可选）默认情况下阻止广告的成人内容程度： *[!UICONTROL Do Not Block]* （默认）， *[!UICONTROL Standard]*，或 *[!UICONTROL Strict]*. 可能需额外付费。

   * **[!UICONTROL Alcohol Content]：** （可选）默认情况下阻止广告的酒精含量级别： *[!UICONTROL Do Not Block]* （默认）， *[!UICONTROL Standard]*，或 *[!UICONTROL Strict]*. 可能需额外付费。

**[!UICONTROL Pre-bid fraud blocking]：** 要基于欺诈性流量和通过测量的可疑活动阻止的站点类型 [!DNL DoubleVerify]， [!DNL Integral Ad Science]、和 [!DNL Peer39]. 为新投放位置选择了广告商级别的默认值，但您可以更改设置：

* [!UICONTROL DoubleVerify]：

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]：** 默认情况下，会阻止所有100%的无效流量（包括被劫持设备上的流量）以便新放置。 可能需额外付费。

   * **[!UICONTROL Also block sites with]：** （可选）额外级别的欺诈和无效流量，会导致DSP默认阻止广告：  *[!UICONTROL None]* （默认情况下，不会阻止其他流量）， *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*， *[!UICONTROL >4% Average Fraud/IVT levels]*， *[!UICONTROL >6% Average Fraud/IVT levels]*， *[!UICONTROL >10% Average Fraud/IVT levels]*，或 *[!UICONTROL >25% Average Fraud/IVT levels]*. 可能需额外付费。

* [!UICONTROL Peer 39]：

   * **[!UICONTROL Block sites that are]：** （可选）一种或多种类型的欺诈(默认情况下，会导致DSP阻止广告)： *[!UICONTROL Fraud]* （会以欺诈方式阻止所有网站）， *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*，和/或 *[!UICONTROL Fraud: Zero Ads]*. 可能需额外付费。

* [!UICONTROL Integral Ad Science]：

   * **[!UICONTROL Block sites that are]：** （可选）一种可疑、导致DSP默认阻止广告的网站或应用程序活动： *[!UICONTROL None]* （默认情况下，不会基于可疑活动阻止广告）， *[!UICONTROL Suspicious Activity - High Risk]*，或 *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. 可能需额外付费。

**[!UICONTROL Ads.txt filtering]：**

哪个级别 [Ads.txt](https://iabtechlab.com/ads-txt-about/) 预竞价筛选，通过应用每个出版商的“授权数字卖家”列表来使用。 为新投放位置选择了广告商级别的默认值，但您可以更改设置：

* *[!UICONTROL Opt out of ads.txt (default)]*：从所有销售者处购买库存。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*：优先从域的授权直接销售者和经销商处购买库存。
* *[!UICONTROL Ads.txt sellers only]*：仅从域的授权直接销售者和经销商购买库存。
* *[!UICONTROL Ads.txt sellers only]*：仅从域的授权直销商处购买库存。

**[!UICONTROL DoubleVerify Authentic Brand Safety]：** (广告商配置了 [!UICONTROL DoubleVerify Authentic Brand Safety] option)启用 [!DNL DoubleVerify Authentic Brand Safety]，它会阻止使用为指定区段ID配置的自定义品牌安全规则在竞价后展示次数。 DSP会根据在广告商设置中指定的区段ID的使用情况向您的帐户收费。

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] 投放)第三方跟踪供应商由批准 [!DNL Roku] include [!DNL Acxiom]， [!DNL comScore]， [!DNL Data Plus Math]， [!DNL Experian]， [!DNL Factual]， [!DNL Kantar]， [!DNL Marketing Evolution]， [!DNL Neustar]， [!DNL Nielsen]， [!DNL Nielsen Catalina Solutions]， [!DNL NinthDecimal]， [!DNL Oracle]， [!DNL Placed]， [!DNL Polk]、和 [!DNL Research Now].

**[!UICONTROL Event Pixels]：** （可选）默认情况下，要附加到投放位置中所有新广告的第三方事件跟踪像素。 要指定事件像素，请执行以下操作：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 执行以下任一操作：
   * 要选择现有像素，请选中像素行中的复选框。
   * 要创建像素，请执行以下操作：
      1. 单击 **[!UICONTROL Create]**.
      1. 输入以下信息：
         * **[!UICONTROL Pixel name]：** 像素名称；最大长度为500个字符。 使用有助于您轻松识别像素的名称。
         * **[!UICONTROL Pixel event fires on]：** 触发像素触发的事件。 可用的事件因广告类型而异。
         * **[!UICONTROL Pixel type]：** 像素是否为 *[!UICONTROL IMG URL]* （1x1像素图像文件）， *[!UICONTROL HTML]*，或 *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]：** 像素图像的URL。
      1. 单击 **[!UICONTROL Create and attach]**.
   1. 单击 **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]：** （可选）默认情况下，要附加到投放位置中所有新广告的转化跟踪像素。 要指定转换像素，请执行以下操作：

1. 单击 ![编辑](/help/dsp/assets/edit.png).
1. 执行以下任一操作：
   * 要选择现有像素，请选中像素行中的复选框。
   * 要创建像素，请执行以下操作：
      1. 单击 **[!UICONTROL Create]**.
      1. 输入以下信息：
         * **[!UICONTROL Conversion pixel name]：** 像素名称；最大长度为500个字符。 使用有助于您轻松识别像素的名称。
         * **[!UICONTROL Conversion category]：** 转换的类型。
         * **[!UICONTROL Impression conversion window]：** 发生广告展示的天数，在此天数内，展示可以归因于转化。 默认值为30天。
         * **[!UICONTROL Click conversion window]：** 发生广告点击的天数，在此天数内，点击可归因于转化。 默认值为30天。
         * **[!UICONTROL Notes]：** （可选）有关像素的描述或其他信息。
      1. 单击 **[!UICONTROL Create and attach]**.
      1. 在相关网页上实施转换像素：
         1. 在主菜单中，转到 **[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]**.
         1. 在像素行中，单击 **[!UICONTROL edit]**.
         1. 将值复制到 [!UICONTROL HTML Tag] 和 [!UICONTROL Flash Tag] 根据需要向广告商或网站联系人提供的字段。

            广告商的IT部门或其他组可能需要计划标记部署或通知标记部署。
   1. 单击 **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]：** （可选）作为每1000次展示的不可计费成本跟踪的静态第三方费率。 除非输入其他值，否则系统会自动为新投放位置应用包级别默认值（如果适用）。

>[!NOTE]
>
>可记帐费用反映在 [!UICONTROL Net CPM] 量度。

>[!MORELIKETHIS]
>
>* [关于版面管理](placement-about.md)
>* [创建投放位置](placement-create.md)
>* [编辑版面](placement-edit.md)
>* [管理投放位置的竞价乘数](placement-manage-bid-multipliers.md)
>* [查看投放位置的更改日志](placement-change-log.md)
>* [键盘快捷键](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [关于Campaign Management的常见问题解答](/help/dsp/campaign-management/faq-campaign-management.md)
