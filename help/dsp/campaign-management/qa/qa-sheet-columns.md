---
title: 已下载/已上传电子表格中的列
description: 在下载和上传的电子表格中，引用位置设置列。
feature: DSP Placements
exl-id: 698c0d86-cb2e-4d76-89c7-5584b6cdb542
source-git-commit: ad0b5826e6639675f374837a04f9877fd05dd0c7
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 0%

---

# 放置设置已下载/已上传电子表格中的列

<!-- see notes within the table about descriptions that need to be edited -->

>[!TIP]
>
> 在下载的电子表格中，所有可编辑的列都以蓝色突出显示。

## 营销活动级别的电子表格

| 部分 | 列 | 描述 | 可编辑？ |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | 投放位置的数值ID。 | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | 投放位置的名称。 | 是 |
| [!UICONTROL Basic] | [!UICONTROL Labels] | 任何应用的标签，用于报告。 | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | 在“编辑”模式下打开投放位置的链接。 | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | 投放状态： *[!UICONTROL active]* 或 *[!UICONTROL inactive]*. | 是 |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | 投放类型。 | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | 父包的名称（如果适用）。 | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | 投放的开始日期。 | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | 投放的结束日期。 | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | 是否分时段 *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*.<br><b>注意：</b> 要检查实际的播出时间表，请在DSP中打开版面设置。 | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | 职位安排预算（如果有）。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | 预算间隔： &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*， *[!UICONTROL Weekly]*， *[!UICONTROL Monthly]*，或 *[!UICONTROL All Time]*.[!UICONTROL >Daily] | 是 |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | 程序包的目标。 | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | 目标的目标值。 | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | 投放位置是否朝着 *[!UICONTROL Budget]* 或 *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | 投放位置的最高出价。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | 投放的飞行步调策略： *[!UICONTROL Even]*， *[!UICONTROL slightly ahead]*， *[!UICONTROL frontload]*，或 *[!UICONTROL aggressive frontload]*. | 是 |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | 投放的当天步调策略： *[!UICONTROL Even]* 或 *[!UICONTROL ASAP]*. | 是 |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | 要应用的任何预竞价筛选条件。 | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | 竞价规则（已弃用）是否 *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | 在指定期间放置的主频率上限 [!UICONTROL Frequency Cap Interval]. | 是 |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | 主频率上限的间隔： *[!UICONTROL Day]*， *[!UICONTROL Week]*，或 *[!UICONTROL Month]*. | 是 |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | 在指定期间放置的次频率上限 [!UICONTROL Secondary Frequency Cap Interval] | 是 |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | 次频上限的间隔类型： *[!UICONTROL Week]*， *[!UICONTROL Day]*， *[!UICONTROL Hour]*，或 *[!UICONTROL Minute]*. 适用的周数、天数、小时数或分钟数由 [!UICONTROL Secondary Frequency Cap Interval Value]. | 是 |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | 星期数、天数、小时数或分钟数，其中 [!UICONTROL Secondary Frequency Cap] 适用。 例如，如果次要展示次数上限是每六小时展示三次次，则此处的值将为 `6`. | 是 |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | 目标地理位置的数量， *[!UICONTROL All]*，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | 目标地理位置（以分号分隔），或 *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | 排除的地理位置数或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | 排除的地理位置（以分号分隔），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | 已指定的目标公共库存交易数（如果有）， *[!UICONTROL All]*，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | 已指定排除的公共库存交易的数量，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | 已指定的定向私有库存交易数（如果有）， *[!UICONTROL All]*，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | 已指定排除的私有库存交易数（如果有），或者 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | 目标数量 [!UICONTROL On-Demand Inventory] 如果指定了交易， *[!UICONTROL All]*，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | 已指定排除的按需库存交易数（如果有），或者 *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | 目标流量类型： *[!UICONTROL Website]* 和/或 *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | 用于排除出流流量的库存定位选项是否为 &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*或 *[!UICONTROL OFF]*.[!UICONTROL >ON]<br>流输出广告通常以弹出窗口或填充到内容中（在本机体验中）的形式出现，而不是在视频播放器中以常规视频广告的形式出现。 | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | 要定位的站点的质量： *[!UICONTROL Tier 1]*， *[!UICONTROL Tier 2]*， *[!UICONTROL Tier 3]*，或 *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | 已指定的目标站点类别数（如果有），或者 *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | 已指定排除站点类别（如果有）的数量，或者 *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | 已指定排除的站点（如果有），或者 *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | 目标站点语言。 | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | （仅限标准显示投放位置）是否允许在未审核站点上投放广告： *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*. 当投放以私人库存为目标时，此选项可能会在阻止的网站上投放广告。 | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | 已指定目标站点的数量（如果有），或者 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | 已指定目标受众（如果有），或者 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | 已指定排除的受众，或者 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | 是否 [!DNL Comscore] 已为投放位置（和营销活动中的其他投放位置）启用人口统计区段： *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*. 只能为符合以下条件的营销活动启用此功能： [!DNL Audience Verification] 功能已启用 [!DNL Nielsen] 和/或 [!DNL Comscore].  它会产生额外费用。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | 是否跨设备扩展广告定位： *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*. 跨设备定位可根据营销活动设置中指定的设备图，将您的定位扩展到用户的所有已知设备。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting]  — 包含# | 已指定的目标主题代码数（如果有），或者 *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | 已指定排除的主题代码数，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | 已指定的目标设备目标的数量（如果有），或者 *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | 已指定排除的设备目标的数量，或者 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | 已指定目标ISP提供商的数量（如果有），或*[!UICONTROL All]/i>。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | 已指定排除的ISP提供商的数量，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | 已应用的品牌安全过滤器数量（如果有），或者 *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | 应用了预竞价欺诈阻止过滤器的数量（如果有的话），或者 *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | 已应用的预竞价可视性筛选器的数量（如果有），或者 *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | 是否启用站点安全块： *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | 附加到投放位置的第三方事件跟踪像素数，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | 附加到投放位置的转化跟踪像素数，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | 作为每1000次展示的不可记帐成本跟踪的静态第三方费率（如果适用）。 | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | 附加到投放位置的广告数（如果有），或者 *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | 附加到投放位置的任何广告的名称，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | 附加到投放位置的任何广告的DSP生成的唯一Ad ID，用分号分隔。 要从以下位置下载广告名称和关联的广告ID列表： [!UICONTROL Ads] 视图，创建一个自定义视图，该视图包括 [!UICONTROL Ad ID] 量度，然后 [导出数据](/help/dsp/campaign-management/reports/campaign-export-data.md). | 是 |

## 置入级别电子表格

| 列 | 描述 | 可编辑？ |
|--------|-------------|-----------|
| [!UICONTROL Placement ID] | 投放位置的数值ID。 | — |
| [!UICONTROL Placement Name] | 投放位置的名称。 | 是 |
| [!UICONTROL Package Name] | 父包的名称（如果适用）。 | — |
| [!UICONTROL Start Date] | 投放的开始日期。 | — |
| [!UICONTROL End Date] | 投放的结束日期。 | — |
| [!UICONTROL Status] | 投放状态： *[!UICONTROL active]* 或 *[!UICONTROL inactive]*. | — |
| [!UICONTROL Max Bid] | 投放位置的最高出价。 | 是 |
| [!UICONTROL Budget] | 职位安排预算（如果有）。 | 是 |
| [!UICONTROL Budget Interval] | 预算间隔： &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*， *[!UICONTROL Weekly]*， *[!UICONTROL Monthly]*，或 *[!UICONTROL All Time]*.[!UICONTROL >Daily] | 是 |
| [!UICONTROL Primary Frequency Cap] | 在指定期间放置的主频率上限 [!UICONTROL Primary Frequency Cap Interval]. | 是 |
| [!UICONTROL Primary Frequency Cap Interval] | 主频率上限的间隔： *[!UICONTROL Day]*， *[!UICONTROL Week]*，或 *[!UICONTROL Month]*. | 是 |
| [!UICONTROL Secondary Frequency Cap] | 在指定期间放置的次频率上限 [!UICONTROL Secondary Frequency Cap Interval] | 是 |
| [!UICONTROL Secondary Frequency Cap Interval] | 次频上限的间隔类型： *[!UICONTROL Week]*， *[!UICONTROL Day]*， *[!UICONTROL Hour]*，或 *[!UICONTROL Minute]*. 适用的周数、天数、小时数或分钟数由 [!UICONTROL Secondary Frequency Cap Interval Value]. | 是 |
| [!UICONTROL Secondary Frequency Cap Interval Value] | 星期数、天数、小时数或分钟数，其中 [!UICONTROL Secondary Frequency Cap] 适用。 例如，如果次要展示次数上限是每六小时展示三次次，则此处的值将为 `6`. | 是 |
| [!UICONTROL Attached Ad ID] | 附加到投放位置的任何广告的DSP生成的唯一Ad ID，用分号分隔。 要从以下位置下载广告名称和关联的广告ID列表： [!UICONTROL Ads] 视图，创建一个自定义视图，该视图包括 [!UICONTROL Ad ID] 量度，然后 [导出数据](/help/dsp/campaign-management/reports/campaign-export-data.md). | 是 |

>[!MORELIKETHIS]
>
>* [关于使用电子表格更正放置设置](qa-about.md)
>* [下载电子表格中的版面设置](qa-sheet-download.md)
>* [在电子表格中上传版面设置](qa-sheet-upload.md)
>* [投放设置](/help/dsp/campaign-management/placements/placement-settings.md)
