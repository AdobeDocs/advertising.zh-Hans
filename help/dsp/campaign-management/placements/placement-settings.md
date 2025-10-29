---
title: 投放设置
description: 请参阅可用版面设置的说明。
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: f8f877552018de50649fbba22c56452775e72df3
workflow-type: tm+mt
source-wordcount: '4436'
ht-degree: 0%

---

# 投放设置

## [!UICONTROL Basics]

**[!UICONTROL Placement name]**&#x200B;投放位置名称。

>[!TIP]
>使用适合您情况的命名约定。 一个建议的命名惯例是“*\&lt;营销活动名称\>： \&lt;广告单位\>： \&lt;持续时间\>： \&lt;定位\>*”。

**[!UICONTROL Status]：**&#x200B;投放状态： *[!UICONTROL Active]* （默认）或&#x200B;*[!UICONTROL Paused]*。

>[!TIP]
>最佳实践是暂停投放位置，直到您准备好启动它。

**[!UICONTROL Details]：**（只读）适用的广告类型、创建或投放位置的帐户以及父营销活动。 若要查看更多详细信息，请单击&#x200B;**[!UICONTROL Show more]**。

**[!UICONTROL Templates]：**&#x200B;打开现有投放模板列表。 要从模板自动填充定位设置，请执行以下操作：

1. 执行以下任一操作：

   * 要重用模板中的所有目标，请选中模板名称旁边的复选框。

   * 要重用模板中的各个目标类型，请展开模板名称并选中要重用的目标类型旁边的复选框。

1. 单击&#x200B;**[!UICONTROL Apply]**。

**[!UICONTROL Ad specs for forecast]：** （仅限视频广告格式）广告持续时间和/或广告规范，用于计算右侧的预测投影。 这些字段因广告类型而异。

**[!UICONTROL Environment]：** （仅限通用视频广告格式）要作为投放位置目标的设备环境（桌面、移动设备、连接电视）。 请至少指定一个。

在自定义报表中，放置级别维度“设备环境”表示目标环境。

**[!UICONTROL Placement tags]：** （可选）关键字或昵称可帮助您找到此位置。

## 目标

**[!UICONTROL Package]：**（可选）位置已分配到的包。 单击![编辑](/help/dsp/assets/edit.png)以选择现有包或创建包。 将投放位置分配给资源包后，[!UICONTROL Goals]部分会使用资源包中的投放日期、投放目标和预算进行更新。

**[!UICONTROL Flight Dates]：**&#x200B;投放位置的开始日期和结束日期。 当投放位置处于活动状态并分配给活动包或营销活动时，批准的广告有资格在投放过程中运行。

默认情况下，会自动填充资源包（如果适用）或营销活动的日期。

>[!NOTE]
>
>* 投放日期必须包含在营销活动投放日期和包投放日期中。

### 分配给具有包级别步调的包的位置

**[!UICONTROL Placement Funding]：**&#x200B;如何为投放位置编列预算：

* *[!UICONTROL Optimize based on performance]：*&#x200B;控制包级别的预算。
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]：*&#x200B;允许您设置最小和/或最大置入预算。 至少指定一种预算类型：

   * *[!UICONTROL Maximum Budget]*：输入值和持续时间(*[!UICONTROL All time]*、*[!UICONTROL Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*)。

   * *[!UICONTROL Minimum Budget]*：最小预算占包预算的百分比。 当指定间隔上限时，最小预算值始终计算为间隔上限的百分比。 否则，它将计算为包预算的百分比。

**[!UICONTROL Max Bid]：**&#x200B;为1000次展示支付的最大值。

**[!UICONTROL Min Bid]：** （仅用于私人和[!DNL On-Demand]交易）基于库存类型的最低出价。 选择一个选项：

* *[!UICONTROL None]*：没有任何库存类型的最低出价。 如果计算的竞价小于目标交易的固定/底价，则DSP不竞价。 这可能会影响规模。

* *[!UICONTROL Fixed/floor price for Private deals only]*： DSP至少对定向私人交易的固定/底价出价，即使算法计算的出价较少。 这可能会影响性能。

* *[!UICONTROL Fixed/floor price for On-demand deals only]*： DSP至少对目标[!DNL On-Demand]交易的固定/底价出价，即使算法计算的出价较少。 这可能会影响性能。

* *[!UICONTROL Fixed/floor price for both Private and On-demand deals]*： DSP至少对定向私有和[!DNL On-Demand]交易的固定/底价出价，即使算法计算的出价较少。 这可能会影响性能。

**[!UICONTROL Placement Pre-bid Filters]：**&#x200B;最多必须满足五个KPI阈值（例如最低可见性量度或点进率）才能进行竞价。 您可以将预竞价筛选器用作优化策略，但请注意，每个规则都可能会限制此投放位置可以竞价的机会。 添加或编辑筛选器：

1. 单击![编辑](/help/dsp/assets/edit.png)。
1. 执行以下任一操作：
   * 要添加过滤器，请执行以下操作：
      1. 单击&#x200B;**[!UICONTROL Add Filter]**。
      1. 在&#x200B;**[!UICONTROL Only bid if]**&#x200B;旁边，选择一个量度，然后输入一个值。
   * 要删除筛选器，请单击筛选器行中的&#x200B;**[!UICONTROL X]**。
1. 单击&#x200B;**[!UICONTROL Save]**。

查看“[位置级别预竞价筛选器”上每个预竞价筛选器的说明及其使用方法](/help/dsp/optimization/optimization-pre-bid-filters.md)。

### 所有其他版面

**[!UICONTROL Budget Goal]：**&#x200B;总预算上限和预算间隔(*[!UICONTROL All time]*、*[!UICONTROL Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*)。

**[!UICONTROL Gross Budget Goal]：** （仅具有利润管理的营销活动中的投放位置）总预算上限和预算间隔(*[!UICONTROL All time]*、*[!UICONTROL Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*)。

**[!UICONTROL Optimization Goal]：**&#x200B;包的优化目标。 请参阅“[优化目标以及如何使用它们](/help/dsp/optimization/optimization-goals.md)”上的每个优化目标的说明。

**[!UICONTROL Target Goal]：**&#x200B;目标目标，用于跟踪性能。

>[!NOTE]
>
>此字段只是一个基准，不用于决策。

**[!UICONTROL Pace on]：**&#x200B;步调的基础：

* **[!UICONTROL Budget goal]：** （默认）此选项在分配的预算内尽可能多地提供展示次数。

* **[!UICONTROL Impressions]：**&#x200B;此选项会一直提供展示次数，直到在指定时间间隔内达到指定的数量为止。 选择此选项时，请指定展示次数和间隔： *[!UICONTROL All time]、* *[!UICONTROL Daily]、* *[!UICONTROL Monthly]、*&#x200B;或&#x200B;*[!UICONTROL Weekly]*。

**[!UICONTROL Max Bid]：**&#x200B;为1000次展示支付的最大值。

**[!UICONTROL Flight pacing]：** （仅具有投放级别步调的投放）如何安排广告投放的步调：

* *[!UICONTROL Even]：*（默认）在每个航班中均匀安排投放，目标是在航班的前半段投放的50%。

* *[!UICONTROL Slightly Ahead]：* （默认）加快投放，使其在飞行持续时间的半程完成55-65%。

* *[!UICONTROL Frontload]：*&#x200B;加速投放，使其在飞行中途完成65-75%。

* *[!UICONTROL Aggressive Frontload]：*&#x200B;加速投放，使其在飞行中途完成75-85%。

**[!UICONTROL Intraday pacing]：** （仅具有投放级别步调的投放）如何在投放过程中的每一天安排广告投放的步调：

* *[!UICONTROL Even]：*（默认）根据库存可用性来缩放投放。 通常，在拍卖量较高的白天，每小时会投放更多广告，而在早上和晚上投放的广告会更少。

* *[!UICONTROL ASAP]：* （默认）将投放速度加快到&#x200B;*Even*&#x200B;的两倍。

  >[!CAUTION]
  >
  >此选项可能会对性能产生负面影响。 仅在您完全优先考虑投放并花费超过性能优化的时间时才使用它。

**[!UICONTROL Placement Pre-bid Filters]：**（可选）最多必须满足五个筛选器才能进行竞价。 您可以将预竞价筛选器用作优化策略，但请记住，每个规则可能会限制此投放位置可以竞价的机会。 添加或编辑筛选器：

1. 单击![编辑](/help/dsp/assets/edit.png)。
1. 执行以下任一操作：
   * 要添加过滤器，请执行以下操作：
      1. 单击&#x200B;**[!UICONTROL Add Filter]**。
      1. 在&#x200B;**[!UICONTROL Only bid if]**&#x200B;旁边，选择一个量度，然后输入一个值。
   * 要删除筛选器，请单击筛选器行中的&#x200B;**[!UICONTROL X]**。
1. 单击&#x200B;**[!UICONTROL Save]**。

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]：**（可选）要在投放位置中包含或排除广告的特定位置。 如果不指定任何位置，则会定向所有位置。

>[!NOTE]
>
>城市和DMA位置不适用于Roku投放。

要指定位置，请执行以下操作：

1. 单击![编辑](/help/dsp/assets/edit.png)。
1. 执行以下任一操作：
   * 要包含或排除国家、州、市、DMA、联邦立法区或州立法区，请执行以下操作：
      1. 在左列中选择位置类型。
      1. （根据需要）单击某个位置以展开该位置。
      1. 在该位置旁边，单击&#x200B;*[!UICONTROL Include]*&#x200B;以将其作为目标包含，或单击&#x200B;*[!UICONTROL Exclude]*&#x200B;以将其作为目标排除。
   * 要搜索邮政编码并包含或排除所有选定的结果，请执行以下操作：
      1. 单击&#x200B;**[!UICONTROL Search Postal Code]**。
      1. 选择国家/地区。
      1. 输入城市名称，然后单击![编辑](/help/dsp/assets/search.png)。
      1. 单击正确的搜索结果。
      1. 单击&#x200B;*[!UICONTROL Include All]*&#x200B;可包含所有位置作为目标，单击&#x200B;*[!UICONTROL Exclude All]*&#x200B;可排除所有位置作为目标。
   * 要输入或粘贴邮政编码，并包含或排除所有邮政编码，请执行以下操作：
      1. 单击&#x200B;**[!UICONTROL Paste Postal Code]**。
      1. 选择国家/地区。
      1. 输入或粘贴最多1000个邮政编码。
每行包括一个邮政编码，或者输入多个值，以逗号或制表符分隔。
      1. 单击&#x200B;*[!UICONTROL Include All]*&#x200B;可包含所有位置作为目标，单击&#x200B;*[!UICONTROL Exclude All]*&#x200B;可排除所有位置作为目标。
   * 要从[!UICONTROL Included]或[!UICONTROL Excluded]列表中删除位置，请单击右列位置旁边的&#x200B;**[!UICONTROL X]**。
1. 单击&#x200B;**[!UICONTROL Done]**。

>[!NOTE]
>
>* 并非所有国家/地区都有省/市/自治区或邮政编码位置。
>* DMA（指定市场区域）、联邦立法区和州立法区仅适用于美国地区。

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]：**&#x200B;要作为目标包含或排除的清单源。 对于大多数置入类型，默认情况下包括所有库存类型以及每种类型的所有来源。 对于[!DNL Roku]投放位置，必须指定库存类型和源。 您可以从以下库存类型中进行选择：

* [!UICONTROL Public]： （除Roku之外的所有放置类型）DSP有权访问的所有未结Exchange库存。 您可以包含和排除公共清单。

  您可以按源或信息源查看列表。 在按信息源查看列表时，您可以按信息源名称、信息源密钥或选定的特征标记进行搜索。

* [!UICONTROL Private] | [!UICONTROL Roku Private]：您与在DSP中设置的发布商的现有私人交易（或用于[!DNL Roku]投放位置的现有私人[!DNL Roku]交易），以及您现有的[私人交易列表](/help/dsp/inventory/lists-deals-manage.md)。 您可以包括（但不排除）公共库存。

  在[!UICONTROL Deals]选项卡中，您可以按关键字、密钥、交易ID或自定义标记搜索列表。 在[!UICONTROL Deal Lists]选项卡中，您可以按交易列表名称或交易列表ID搜索列表。

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]：您已在[中订阅的所有[!UICONTROL On Demand]高级、不保证的](/help/dsp/inventory/on-demand-inventory-about.md)库存[!UICONTROL On Demand]（或[!DNL Roku]投放位置的[!DNL Roku] [!DNL DSP]交易）。 您可以包含和排除[!UICONTROL On Demand]清单。

  您可以按源或信息源查看列表。 在按信息源查看列表时，您可以按信息源名称、信息源键或选定的发布者区域、类别标记或特征标记进行搜索。

要指定库存定位，请执行以下操作：

* 要排除清单类型，请清除名称旁边的复选框。
* 要定位库存类型，请执行以下操作：
   1. 选中清单类型名称旁边的复选框。
   1. （可选）更改源以包括：
      1. 单击![编辑](/help/dsp/assets/edit.png)。
      1. （[!UICONTROL Public]和[!UICONTROL On Demand]清单）单击&#x200B;**[!UICONTROL View by Source]**&#x200B;或&#x200B;**[!UICONTROL View by Feed]**&#x200B;以更改源的列出方式。
      1. （适用时）根据需要筛选库存。
      1. 指定要包含和排除的源：
         * 对于[!UICONTROL Public]或[!UICONTROL On Demand]清单：
            * 要包含源，请单击源名称旁边的&#x200B;**[!UICONTROL Include]**。
            * 要排除源，请单击源名称旁边的&#x200B;**[!UICONTROL Exclude]**。
         * 对于[!UICONTROL Private]库存：
            * 在[!UICONTROL Deals]选项卡上：
               * 要在交易中包含所有库存，请单击交易名称旁边的&#x200B;**[!UICONTROL Include all]**。
               * 要包含单个库存来源，请展开交易名称，然后单击来源名称旁边的复选框。
            * 在[!UICONTROL Deal Lists]选项卡上，单击交易列表名称旁边的复选框。
   1. （可选）要将包含定向信息的CSV文件下载到浏览器的下载位置，请单击&#x200B;**[!UICONTROL Export]**。
   1. 单击&#x200B;**[!UICONTROL Save]**。

>[!TIP]
>
>如果您订阅了[!UICONTROL On Demand]清单，但找不到要定位的发布者或交易，请检查交易的状态。 有关状态的详细信息，请参阅[关于 [!DNL On Demand] 高级库存](/help/dsp/inventory/on-demand-inventory-about.md)。

**[!UICONTROL Video targeting]：**&#x200B;按库存属性列出的目标（但不排除）库存。 为同一视频属性定位多个值时，可以定位任何选定的属性（例如，\[播放器大小=大或播放器大小=高清\]）。 定位多个属性时，必须存在指定的每个属性（例如，\[持续时间= 30-60分钟]和\[播放器大小=大或播放器大小= HD\]）。

* **[!UICONTROL Player size]：**&#x200B;按播放器大小列出的目标（但不排除）库存。 该设置适用于适用于桌面和移动设备环境的预置广告投放、移动设备标准预置广告投放和通用视频投放。 默认情况下，会定向所有大小。 若要缩小目标范围，请选择特定目标大小和/或&#x200B;*未知*。

* **[!UICONTROL Playback mode]：**&#x200B;按播放启动方式列出的目标（但不排除）清单。 该设置适用于适用于桌面和移动设备环境的预置广告投放、移动设备标准预置广告投放和通用视频投放。 默认情况下，会定位所有模式。 若要缩小目标范围，请选择特定的目标模式和/或&#x200B;*未知*。

* **[!UICONTROL Skippability]：**&#x200B;目标（但不排除）清单（根据它是否可跳过）。 该设置适用于所有VAST/VPAID投放位置，包括前置广告、移动设备标准前置广告、连接电视和通用视频投放位置。 默认情况下，会定向所有选项。 要缩小目标范围，请选择特定目标和/或&#x200B;*未知*。

**[!UICONTROL Position targeting]：**&#x200B;按广告位置列出的目标（但不排除）库存。 该设置适用于所有VAST/VPAID投放位置，包括前置广告、移动设备标准前置广告、连接电视和通用视频投放位置。 默认情况下，所有职位都是定向的。 若要缩小目标范围，请选择特定目标位置和/或&#x200B;*未知*。

## [!UICONTROL Site or App and Keyword Targeting]

**[!UICONTROL Traffic type]：**&#x200B;目标流量的类型。 选项包括&#x200B;**[!UICONTROL Websites]**&#x200B;和&#x200B;**[!UICONTROL Apps]**。

**[!UICONTROL Tier]：** （在&#x200B;**[!UICONTROL Toggle for Sites or Apps Tiering]**&#x200B;为&#x200B;*[!UICONTROL On]*&#x200B;时可用）要定位的流量的质量。 第1层至第3层均符合品牌安全要求，并已获得DSP映射团队的批准。

* *[!UICONTROL Tier 1]：*&#x200B;可在全国范围内识别的高级网站和应用程序。

* *[!UICONTROL Tier 2]：*&#x200B;定位第1层以及比第1层知名度低的质量站点和应用程序。

* *[!UICONTROL Tier 3]：*&#x200B;定位第1层至第2层以及符合小众受众需求的合法且品牌安全的站点和应用程序。 使用第3层进行覆盖或数据定位购买。

* *[!UICONTROL All Sites or Apps]：*&#x200B;定位第1-3层以及尚未进行筛选或分类的新库存，您可以将这些库存用于访问。

>[!NOTE]
>
>库存特定于投放位置中的广告单元。

>[!TIP]
>
>对于性能营销活动，最佳实践是选择&#x200B;*[!UICONTROL All Sites]*。

**[!UICONTROL Site or App Categories]：**（可选）选定流量类型中的站点类别和（指定后）要包含或排除（但不能同时包含和排除）作为目标的站点层。 从DSP已根据主题映射的垂直网站列表中进行选择：

1. 单击![编辑](/help/dsp/assets/edit.png)。
1. 指定要包含或排除的站点类别：
   * 要包含站点类别，请执行以下操作：
      1. 单击&#x200B;**[!UICONTROL Include categories]**。
      1. 选中每个要定位的类别旁边的复选框。
   * 要排除站点类别，请执行以下操作：
      1. 单击&#x200B;**[!UICONTROL Exclude categories]**。
      1. 选中要排除的每个类别旁边的复选框。
1. （可选）要将包含定向信息的CSV文件下载到浏览器的下载位置，请单击&#x200B;**[!UICONTROL Export]**。
1. 单击&#x200B;**[!UICONTROL Save]**。

**[!UICONTROL Exclude Sites or Apps]：** （可选；当&#x200B;**[!UICONTROL Toggle for Sites or Apps Tiering]**&#x200B;为&#x200B;*[!UICONTROL On]*&#x200B;时可用）要排除的站点/应用和[URL列表](/help/dsp/resources/lists-url-manage.md)。 在[!UICONTROL Paste URL]选项卡中，您可以搜索和选择站点，或者输入或粘贴域名。 从[!UICONTROL URL Lists]选项卡中，您可以选择URL列表。

1. 单击![编辑](/help/dsp/assets/edit.png)。
1. 指定站点：
   * 从[!UICONTROL Paste URL]选项卡：
      * 要搜索站点：
         1. 单击&#x200B;**[!UICONTROL Search]**。
         1. 输入关键字、选择站点层和/或选择站点类别。
         1. 在搜索结果中，选择要排除的站点：
            * 要排除单个站点，请选中相邻复选框。
            * （当可用结果超过50个时）要排除前50个结果，请单击&#x200B;**[!UICONTROL Exclude these 50]**。 要排除所有搜索结果，请单击&#x200B;**[!UICONTROL Exclude these \<*NN *\>]**。
      * 要输入域名，请执行以下操作：
         1. 单击&#x200B;**[!UICONTROL Paste]**。
         1. 在单独行中输入一个或多个域名。
         1. 单击&#x200B;**[!UICONTROL Exclude All]**。
   * 从[!UICONTROL URL Lists]选项卡：
      1. （可选）通过在搜索字段中输入全部或部分列表名称来搜索URL列表。
      1. 选中要排除的每个URL列表旁边的复选框。
1. 完成后，单击&#x200B;**[!UICONTROL Done]**。

>[!NOTE]
>
>* 除了DSP [全局阻止的站点列表](/help/dsp/introduction/features/brand-safety-media-quality.md)之外，还会应用帐户级别和广告商级别的阻止的站点列表，该列表包括被视为不安全的广告站点。
>* 阻止的站点列表始终覆盖目标站点和站点列表。 如果投放位置同时排除并包含广告的相同目标，则排除该目标。

**[!UICONTROL Context of Sites or App]：**（可选）要定位或排除的上下文目标区段。 从以下列表中选择

* **[!UICONTROL Marketplace]**&#x200B;选项卡：列出按指定费用对所有用户可用的[!DNL Peer39]区段。

* **[!UICONTROL Custom Segments]**&#x200B;选项卡：列出您组织的[!DNL Peer39]自定义区段。

* **[!UICONTROL Paste Segments]**&#x200B;选项卡： (其组织具有[!DNL Comscore]伙伴关系的广告商；从您的Adobe客户团队激活后可用)为组织的[!DNL Comscore]上下文区段输入一个或多个区段ID或区段名称。 用逗号分隔多个值（如Segment1、Segment2、Segment3）。

**[!UICONTROL Language]：**（可选）目标单一语言。

**[!UICONTROL Site or app list preview]：** （只读；在&#x200B;**[!UICONTROL Toggle for Sites or Apps Tiering]**&#x200B;为&#x200B;*[!UICONTROL On]*&#x200B;时可用）所有针对该投放位置定位和阻止的站点/应用程序，包括帐户级别、广告商级别以及DSP全局阻止的站点列表中的站点/应用程序。

您可以选择将目标和阻止站点的列表导出为逗号分隔值(CSV)文件。 要导出列表，请单击&#x200B;**[!UICONTROL Export full site list]**，然后按照浏览器的正常过程打开或保存文件。

**[!UICONTROL Allow unscreened sites]：** （仅限标准显示投放位置）在未审核的网站上启用广告投放。 当投放以私人库存为目标时，此选项可能会在阻止的网站上投放广告。

**[!UICONTROL Toggle for Sites or Apps Tiering]：**&#x200B;允许您指定要定位或排除的站点或应用程序层。

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]：**&#x200B;投放位置的任何受众目标，包括[第三方区段、第一方区段、Adobe区段、自定义区段和保存的受众](/help/dsp/audiences/audience-settings.md)。 此外，还会显示所有选定区段和已保存受众中经过重复数据删除的总受众大小和活动受众大小。 您可以选择现有受众，创建以后可以重复使用的受众，或者选择特定的受众区段：

* 要选择现有受众，请单击![旁边的](/help/dsp/assets/chevron-down.png)选择[!UICONTROL Included Audiences]，然后选择受众。
* 要创建受众，请单击![旁边的](/help/dsp/assets/chevron-down.png)选择[!UICONTROL Included Audiences]，然后选择&#x200B;**[!UICONTROL + Create Audience]**。 有关说明，请参阅从步骤3开始的[创建可重复使用的受众](/help/dsp/audiences/reusable-audience-create.md)。
* 要选择特定的受众区段，请单击&#x200B;**[!UICONTROL Select segments for this placement only]**。 选择区段逻辑；有关说明，请参阅“[创建可重用受众](/help/dsp/audiences/reusable-audience-create.md)”中的步骤6。 完成后，单击&#x200B;**保存**。

>[!NOTE]
>
>未附加到活动、计划或暂停放置的第一方RampID区段将被暂停。 该区段在区段列表中标记为“自动暂停”。

**[!UICONTROL Excluded Audiences]：**&#x200B;要排除以进行投放的任何受众，包括具有[第三方区段、第一方区段、Adobe区段、自定义区段和已保存受众的受众](/help/dsp/audiences/audience-settings.md)。 此外，还会显示所有已排除受众中经过重复数据删除的总受众人数和活动受众人数。 您可以选择现有受众，也可以创建一个以后可以重复使用的新受众：

* 要选择现有受众，请单击![旁边的](/help/dsp/assets/chevron-down.png)选择[!UICONTROL Excluded Audiences]，然后选择受众。

* 要创建受众，请单击![旁边的](/help/dsp/assets/chevron-down.png)选择[!UICONTROL Excluded Audiences]，然后选择&#x200B;**+创建受众**。 有关说明，请参阅从步骤3开始的[创建可重复使用的受众](/help/dsp/audiences/reusable-audience-create.md)。

**[!UICONTROL Targeting]：**&#x200B;要定位的用户ID类型。 在投放开始后（即，在投放开始后），无法更改此设置。

当您同时选择旧版ID和通用ID时，会为通用ID提供竞价偏好设置。

* *[!UICONTROL Legacy IDs (Cookies, MAIDS, CTV)]*：（默认）根据用户的Cookie、移动广告ID或连接的电视(CTV) ID定位用户。 根据浏览器、应用程序内或CTV清单选择ID。

* *[!UICONTROL Universal ID Beta]*：定位注重隐私的用户ID；选择一种ID类型。 可用选项由[!UICONTROL Geo-Targeting]部分中的所选地理目标决定。 与直接导入到DSP[[!DNL RampID] 的](/help/dsp/audiences/sources/source-import-liveramp-segments.md)区段、DSP将您的PII转换为通用ID的[区段](/help/dsp/audiences/sources/source-about.md)或跟踪通用ID的[自定义区段](/help/dsp/audiences/custom-segment-create.md)一起使用。

   * *[!UICONTROL ID5]*：目标[!DNL ID5] ID是根据电子邮件地址和其他信号概率创建的。<!-- What countries/geos are these available for? Everywhere?--> ID5 ID免费提供。 **注意：** [!DNL Eyeota]中的第三方区段可能包含ID5 ID。

   * *[!UICONTROL RampID]*：目标[!DNL LiveRamp] [!DNL RampIDs]用户使用其电子邮件地址登录到您的网站。<!-- Verify --> [!DNL RampIDs]适用于北美洲、澳大利亚和新西兰的用户。

   * *[!UICONTROL Unified ID2.0]*：已使用用户的电子邮件地址登录到您的网站的目标[!DNL Unified ID2.0] (UID2) ID。<!-- Verify -->[!DNL UID2 IDs]不适用于欧洲经济区和其他一些国家/地区的用户。 查看[禁止的国家/地区列表](/help/policies/universal-id-policy.md#prohibited-countries-uid2)。

  **[!UICONTROL Terms of service]**：使用通用ID的服务协议条款。 您或DSP帐户中的其他用户必须接受一次这些条款，然后才能将数据转换为新的ID类型。 对于签订托管服务合同的客户，您的Adobe客户团队将代表贵组织获得您的同意并接受条款。 若要阅读术语，请单击&#x200B;**>**。 要接受条款，请滚动到条款的底部并单击&#x200B;**[!UICONTROL Accept]**。

**[!UICONTROL Cross Device Targeting]：** (为基于人员的跨设备定位配置[营销活动时](/help/dsp/campaign-management/campaigns/campaign-settings.md)可用，您仅定位旧版ID（非通用ID），并且您至少选择一个区段或受众。 允许您将定位扩展到用户的所有已知设备（根据促销活动设置中指定的设备图），甚至扩展到不在指定区段中的设备。 根据为营销活动指定的图表，可能会收取相关费用。 设备图数据仅在北美地区可用。

**[!UICONTROL Placement Cap]：**（可选）从投放位置为唯一设备、通用ID或人员（取决于为营销活动指定的[!UICONTROL Cross Device Level]和投放位置的[!UICONTROL Targeting]设置）提供广告的次数。 选项包括&#x200B;*[!UICONTROL Unlimited]*&#x200B;或每天、每周或每月的特定金额。

>[!NOTE]
>
> 您可以在营销活动、包和投放级别设置频率上限。 DSP遵循营销活动层级中最严格的频率限制。

**[!UICONTROL Secondary Cap]：** （可选，当您包含数字[!UICONTROL Placement Cap]时可用）主版面限制范围内的附加限制。 选择展示次数和时间段（例如，每12小时3次）。

**[!UICONTROL Day Parting]：**（可选）广告在一周中的特定日期和时间运行。 要指定时段间隔，请执行以下操作：

1. 单击![编辑](/help/dsp/assets/edit.png)。
1. 选择适用的时区。
1. 指定间隔：
   * 要选择预设间隔，请单击其中一个间隔按钮。 选项包括&#x200B;*[!UICONTROL Weekends]**、*[!UICONTROL Weekdays]*、*[!UICONTROL Morning]*、*[!UICONTROL Lunch]*、*[!UICONTROL Dinner]*&#x200B;或&#x200B;*[!UICONTROL Prime]* (primetime)。
   * 要手动选择间隔，请单击单元格内部，也可以拖动以选择间隔。
1. 单击&#x200B;**[!UICONTROL Save]**。

**[!UICONTROL Topic Targeting]：** （可选，适用于配置了[!DNL Proximic by Comscore]区段的广告商）要作为目标包含的[!DNL Proximic by Comscore]中的特定区段名称或ID。 此功能可能需要额外付费。 要激活此功能并设置主题区段，请联系您的Adobe客户团队。

要指定主题定位，请执行以下操作：

1. 单击![编辑](/help/dsp/assets/edit.png)。
1. 指定要定位的区段：
   1. 在左列中，选择合作伙伴： (*[!UICONTROL Comscore]*)。
   1. 在输入字段中输入区段名称或区段ID。
1. （可选）要将包含主题信息的CSV文件下载到浏览器的下载位置，请单击&#x200B;**[!UICONTROL Export]**。
1. 单击&#x200B;**[!UICONTROL Save]**。

>[!TIP]
>
>* 主题定位限制了投放位置可以竞价的库存，因此使用主题定位仅占您总体购买的一小部分。
>
>* 在[!DNL Proximic by Comscore]上的区段内设置任何负面定位。

**[!UICONTROL Device Targeting]：**（可选）要作为目标包含和排除的特定设备信息，包括设备类型、制造商、操作系统、浏览器和连接类型。 类型因放置类型而异。 要指定设备定位，请执行以下操作：

1. 单击![编辑](/help/dsp/assets/edit.png)。
1. 指定要包含和排除的设备详细信息：
   1. 在左列中，选择类别。
   1. 指定定位：
      * 要包含值，请单击值名称旁边的&#x200B;**[!UICONTROL Include]**。
      * 要排除值，请单击值名称旁边的&#x200B;**[!UICONTROL Exclude]**。
1. （可选）要将包含设备定向信息的CSV文件下载到浏览器的下载位置，请单击&#x200B;**[!UICONTROL Export]**。
1. 单击&#x200B;**[!UICONTROL Save]**。

**[!UICONTROL ISP Targeting]：** （可选）特定的Internet服务提供商(ISP)，要包含或排除（但不能同时包含和排除）作为目标。 要指定ISP定位，请执行以下操作：

1. 单击![编辑](/help/dsp/assets/edit.png)。
1. 指定要包含或排除的ISP：
   * 要包括ISP，请执行以下操作：
      1. 单击&#x200B;**[!UICONTROL Include ISPs]**。
      1. （可选）按关键字筛选列表。
      1. 选中每个要定位的ISP旁边的复选框。
   * 要排除ISP：
      1. 单击&#x200B;**[!UICONTROL Exclude ISPs]**。
      1. （可选）按关键字筛选列表。
      1. 选中要排除的每个ISP旁边的复选框。
1. （可选）要将包含ISP定位信息的CSV文件下载到浏览器的下载位置，请单击&#x200B;**[!UICONTROL Export]**。
1. 单击&#x200B;**[!UICONTROL Save]**。

## [!UICONTROL Brand Safety and Media Quality]

**[!UICONTROL DoubleVerify ABS segment ID]：** （可选；仅[!DNL DoubleVerify]客户；仅适用于桌面前置式广告、标准广告和点播显示，以及仅限本机显示和视频投放位置；不支持[交易的默认程序化保证投放位置](/help/dsp/inventory/programmatic-guaranteed-about.md)） [!DNL DoubleVerify Authentic Brand Safety]区段ID与组织的[!DNL DoubleVerify]帐户关联以用于投放位置。 使用为指定区段ID配置的自定义品牌安全规则指定ID会阻止竞价后的展示次数。 DSP按区段ID的使用情况向帐户收费。

ID必须以“51”开头并且由八位数字组成。 默认情况下，如果在广告商帐户设置中指定了区段ID，则会输入广告商级别的ID，但您可以将该ID更改为使用其他区段，或删除该ID以禁用该功能。

**[!UICONTROL Contextual filtering]：** （适用于桌面和移动设备Web显示、原生和视频广告）要应用的[!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science]和[!DNL Peer39]上下文筛选器的类型。 为新投放位置选择了广告商级别的默认值，但您可以更改设置：

<!-- Looks like we didn't rename this:
**[!UICONTROL Brand Safety categories]:** Types of [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], and [!DNL Peer39] brand safety category filters to apply. The advertiser-level defaults are selected for new placements, but you can change the settings:
-->

* [!UICONTROL DoubleVerify]：

   * **[!UICONTROL Block sites that are]：**（可选）默认情况下阻止一个或多个类型的库存上下文。 可能需额外付费。

* [!UICONTROL Peer 39]：

   * **目标站点：**（可选）默认情况下要定位一种或多种类型的库存属性。 可能需额外付费。

* [!UICONTROL ComScore]：

   * **阻止以下站点：**（可选）默认情况下阻止一个或多个类型的清单属性。 可能需额外付费。

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]：** （可选）默认情况下阻止广告的成人内容程度： *[!UICONTROL Do Not Block]* （默认值）、*[!UICONTROL Standard]*&#x200B;或&#x200B;*[!UICONTROL Strict]*。 可能需额外付费。

   * **[!UICONTROL Alcohol Content]：**（可选）默认情况下阻止广告的酒精含量程度： *[!UICONTROL Do Not Block]*（默认值）、*[!UICONTROL Standard]*&#x200B;或&#x200B;*[!UICONTROL Strict]*。 可能需额外付费。

**[!UICONTROL Pre-bid fraud blocking]：**&#x200B;要基于通过[!DNL DoubleVerify]、[!DNL Integral Ad Science]和[!DNL Peer39]测量的欺诈性流量和可疑活动阻止的站点类型。 为新投放位置选择了广告商级别的默认值，但您可以更改设置：

* [!UICONTROL DoubleVerify]： （适用于桌面和移动设备Web显示、本机、视频和标准连接的电视广告）

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]：**&#x200B;默认情况下，会阻止所有100%无效的流量（包括被劫持设备上的流量）用于新放置。 可能需额外付费。

   * **[!UICONTROL Also block sites with]：**（可选）额外级别的欺诈和无效流量导致DSP默认阻止广告： *[!UICONTROL None]*（默认值，它不会阻止额外流量）、*[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*、*[!UICONTROL >4% Average Fraud/IVT levels]*、*[!UICONTROL >6% Average Fraud/IVT levels]*、*[!UICONTROL >10% Average Fraud/IVT levels]*&#x200B;或&#x200B;*[!UICONTROL >25% Average Fraud/IVT levels]*。 可能需额外付费。

* [!UICONTROL Peer 39]： （适用于桌面和移动设备Web显示、本机广告和视频广告）

   * **[!UICONTROL Block sites that are]：**（可选）一种或多种类型的欺诈会导致DSP默认阻止广告： *[!UICONTROL Fraud]*（会阻止所有网站进行欺诈行为）、*[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*&#x200B;和/或&#x200B;*[!UICONTROL Fraud: Zero Ads]*。 可能需额外付费。

* [!UICONTROL Integral Ad Science]： （适用于桌面和移动设备Web显示、本机广告和视频广告）

   * **[!UICONTROL Block sites that are]：**（可选）一种可疑DSP阻止广告的网站或应用程序活动类型： *[!UICONTROL None]*（默认值，不阻止基于可疑活动的广告）、*[!UICONTROL Suspicious Activity - High Risk]*&#x200B;或&#x200B;*[!UICONTROL Suspicious Activity - High or Moderate Risk]*。 可能需额外付费。

**[!UICONTROL Pre-bid viewability]：** （适用于桌面和移动设备Web显示、原生和视频广告）按[!DNL DoubleVerify]和[!DNL Integral Ad Science]筛选的预竞价可见性以申请投放位置。 为新投放位置选择了广告商级别的默认值，但您可以更改设置。 可能需额外付费。

**[!UICONTROL Ads.txt filtering]：** （适用于桌面和移动设备Web显示、本机、视频和音频广告）通过应用每个发布者的授权数字卖家列表来使用[Ads.txt](https://iabtechlab.com/ads-txt-about/)预竞价筛选的级别。 为新投放位置选择了广告商级别的默认值，但您可以更改设置：

* *[!UICONTROL Opt out of ads.txt (default)]*：从所有卖家购买库存。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*：优先从域的授权直销商和经销商处购买库存。
* *[!UICONTROL Ads.txt sellers only]*：仅从域的授权直销商和经销商购买库存。
* *[!UICONTROL Ads.txt sellers only]*：仅从域的授权直销人员购买库存。

**[!UICONTROL Attention Targeting]：** （适用于桌面和移动设备Web显示、视频和标准连接的电视广告）基于指定的站点、格式和广告大小，以特定关注级别（高、中或低）为目标[!DNL Adelaide]预竞价区段。 区段每周更新一次。 **注意：**&#x200B;使用[!DNL Adelaide]区段进行定位将导致[!DNL Adelaide]关注定位提供的每次展示产生CPM费用；此费用与[关注测量](/help/dsp/campaign-management/campaigns/campaign-settings.md)的费用分开。 对于交互式前置投放，您只需为VAST展示付费。

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>（[!DNL Roku]个投放位置） [!DNL Roku]批准的第三方跟踪供应商包括[!DNL Acxiom]、[!DNL Comscore]、[!DNL Data Plus Math]、[!DNL Experian]、[!DNL Factual]、[!DNL Kantar]、[!DNL Marketing Evolution]、[!DNL Neustar]、[!DNL Nielsen]、[!DNL Nielsen Catalina Solutions]、[!DNL NinthDecimal]、[!DNL Oracle]、[!DNL Placed]、[!DNL Polk]和[!DNL Research Now]。

**[!UICONTROL Event Pixels]：**（可选）默认情况下附加到投放位置中所有新广告的第三方事件跟踪像素。 要指定事件像素，请执行以下操作：

1. 单击![编辑](/help/dsp/assets/edit.png)。
1. 执行以下任一操作：
   * 要选择现有像素，请选中像素行中的复选框。
   * 要创建像素，请执行以下操作：
      1. 单击&#x200B;**[!UICONTROL Create]**。
      1. 输入以下信息：
         * **[!UICONTROL Pixel name]：**&#x200B;像素名称；最大长度为500个字符。 使用有助于您轻松识别像素的名称。
         * **[!UICONTROL Pixel event fires on]：**&#x200B;触发像素触发的事件。 可用的事件因广告类型而异。
         * **[!UICONTROL Pixel type]：**&#x200B;像素是&#x200B;*[!UICONTROL IMG URL]* （1x1像素图像文件）、*[!UICONTROL HTML]*&#x200B;还是&#x200B;*[!UICONTROL JavaScript URL]*。
         * **[!UICONTROL Pixel URL]：**&#x200B;像素图像的URL。
      1. 单击&#x200B;**[!UICONTROL Create and attach]**。
   1. 单击&#x200B;**[!UICONTROL Save]**。

**[!UICONTROL Conversion Pixels]：**（可选）默认情况下附加到投放位置中所有新广告的转化跟踪像素。 要指定转换像素，请执行以下操作：

1. 单击![编辑](/help/dsp/assets/edit.png)。
1. 执行以下任一操作：
   * 要选择现有像素，请选中像素行中的复选框。
   * 要创建像素，请执行以下操作：
      1. 单击&#x200B;**[!UICONTROL Create]**。
      1. 输入以下信息：
         * **[!UICONTROL Conversion pixel name]：**&#x200B;像素名称；最大长度为500个字符。 使用有助于您轻松识别像素的名称。
         * **[!UICONTROL Conversion category]：**&#x200B;转换的类型。
         * **[!UICONTROL Impression conversion window]：**&#x200B;广告展示发生后，该展示可归因于转化的天数。 默认值为30天。
         * **[!UICONTROL Click conversion window]：**&#x200B;广告点击发生后可归因于转化的天数。 默认值为30天。
         * **[!UICONTROL Notes]：**（可选）有关像素的描述或其他信息。
      1. 单击&#x200B;**[!UICONTROL Create and attach]**。
      1. 在相关网页上实施转换像素：
         1. 在主菜单中，转到&#x200B;**[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]**。
         1. 在像素行中，单击&#x200B;**[!UICONTROL edit]**。
         1. 根据需要复制[!UICONTROL HTML Tag]和[!UICONTROL Flash Tag]字段中的值以提供给广告商或网站联系人。

            广告商的IT部门或其他组可能需要计划标记部署或通知标记部署。
   1. 单击&#x200B;**[!UICONTROL Save]**。

**[!UICONTROL 3rd-party Fees]：**（可选）要作为每1000次展示的不可记帐成本跟踪的静态第三方费率。 除非输入其他值，否则系统会自动为新投放位置应用包级别默认值（如果适用）。

>[!NOTE]
>
>可记帐费用反映在[!UICONTROL Net CPM]指标中。

>[!MORELIKETHIS]
>
>* [关于版面管理](placement-about.md)
>* [创建版面](placement-create.md)
>* [编辑版面](placement-edit.md)
>* [管理投放位置的竞价乘数](placement-manage-bid-multipliers.md)
>* [查看投放位置的更改日志](placement-change-log.md)
>* [键盘快捷键](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* 有关营销活动管理的[常见问题解答](/help/dsp/campaign-management/faq-campaign-management.md)
