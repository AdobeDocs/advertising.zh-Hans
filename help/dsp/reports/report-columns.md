---
title: 可用报表列
description: 请参阅自定义报表中可用列的描述。
feature: DSP Custom Reports
exl-id: 6dc30603-8a45-4188-aca6-591f3422b74a
source-git-commit: b62d6f412c53536b4d3d156117b82f6a912ba366
workflow-type: tm+mt
source-wordcount: '2045'
ht-degree: 0%

---

# 可用报表列

| 量度类型 | 子类型 | 列名称 | 描述 |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad External ID] | 由外部广告服务器分配的广告ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad ID] | DSP中广告的唯一标识符。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Name] | 由用户分配的广告名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Type] | 广告的格式。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Status] | 由用户更改或由日期输入表示的广告分类： *[!UICONTROL live]*, *[!UICONTROL scheduled]*, *[!UICONTROL completed]*&#x200B;或 *[!UICONTROL archived]*. |
| [!UICONTROL Dimension] | [!UICONTROL Advertiser] | [!UICONTROL Advertiser Name] | 广告商的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Budget] | 用户为营销活动分配的总预算。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign End Date] | 营销活动的结束日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign ID] | DSP中促销活动的唯一标识符。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign Name] | 由用户分配的营销活动名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign Start Date] | 营销活动的第一个日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Day (YYYY-MM-DD)] | 年、月和日。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | 日 [!UICONTROL of Week] | 具体日期，例如 [!UICONTROL Monday] 或 [!UICONTROL Tuesday]. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Hour (YYYY-MM-DD HH)] | 年、月、日和小时。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Month (YYYY-MM)] | 月和年。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Time of Day] | 时间到小时，从0到23。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Week (YYYY-MM-DD to YYYY-MM-DD)] | 相关周的日期范围（从星期日到星期六）。 示例：2021-02-18至2021-03-07。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser Vendor] | 显示广告的浏览器的供应商(如Google或Mozilla)。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser Version] | 显示广告的浏览器的版本(例如 [!UICONTROL Safari 4.3] 或 [!UICONTROL Chrome 7.0])。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser] | 显示广告的浏览器(例如 [!UICONTROL Chrome] 或 [!UICONTROL Firefox])。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Environment] | 广告是否显示在 *[!UICONTROL sites]* 或 *[!UICONTROL Apps]*. |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Hardware] | 显示广告的设备类型(例如 [!UICONTROL Set Top Box] 或 [!UICONTROL Mobile Phone])。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Manufacturer] | 显示广告的设备的制造商(例如 [!UICONTROL Samsung], [!UICONTROL Lenovo]或 [!UICONTROL Apple])。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Model] | 显示广告的设备的型号(例如 [!UICONTROL iPhone XS] 或 [!UICONTROL Galaxy Note 7])。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System Vendor] | 显示广告的操作系统的供应商(例如 [!UICONTROL Microsoft] 或 [!UICONTROL Apple])。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System Version] | 显示广告的操作系统的版本(例如 [!UICONTROL Windows 10] 或 [!UICONTROL iOS Mojave]) |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System] | 显示广告的操作系统(例如 [!UICONTROL Apple iOS] 或 [!UICONTROL Android])。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Deal ID] | 通过外部供应合作伙伴分配给交易的唯一标识符。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Feed Name] | 在DSP中输入的交易的用户分配名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Feed Source] | 提供库存的供应方合作伙伴。 它通常是发布者，但也可以是SSP。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Inventory Type] | 库存分类： *[!UICONTROL Private],* *[!UICONTROL On Demand],* 或 *[!UICONTROL Public]*. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL SSP] | 将媒体归因到的供应方合作伙伴(SSP)。 |
| [!UICONTROL Dimension] | [!UICONTROL Frequency] | [!UICONTROL Frequency] | 设备收到广告的次数，基于唯一的Cookie或设备ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL City] | 报告数据归因到的城市。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL Country] | 报告数据归因到的国家/地区。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL DMA] | 将报告数据归因到的指定市场区域(DMA)。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL State] | 报告数据归因到的状态。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Audience] | 观众。 报表最多支持10个独特受众。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Campaign] | 营销活动。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Creative Length] | 创意的长度。 报表最多支持10个唯一的创作时长。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Device] | 设备。 报表最多支持10个独特设备。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Feed Type] | 馈送的类型。 报表最多支持10种唯一馈送类型。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Media Type] | 媒体类型。 报表最多支持10种独特媒体类型。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Publisher] | 出版商。 该报表最多支持10个独特发布者。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Package] | 包。 <!-- Note: The Package dimensions include another dimension called Package Name. --> |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Placement] | 版面。<!-- Note: The Placement dimensions include another dimension called Placement Name --> |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Site/Apps] | 提供广告展示的网站或应用程序。 报表最多支持10个独特网站或应用程序。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Tags] | 用作版面自定义标识符的版面标记。 报表最多支持10个唯一版面标记。 <!-- Note: The Placement dimensions include another dimension called Placement Tags. --> |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package End Date] | 包的结束日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Goal Type] | 包的步调目标量。 此金额以“支出”或“展示次数”计。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package ID] | DSP中包的唯一标识符。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Name] | 包的名称 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Start Date] | 包开始日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Placement End Date] | 版面结束日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Pixel] | [!UICONTROL Conversion ID] | （已弃用）由DSP分配给旧版的转化ID [!DNL TubeMogul] 转化事件。 |
| [!UICONTROL Dimension] | [!UICONTROL Pixel] | [!UICONTROL Conversion Name] | （已弃用）分配给旧版的转化名称 [!DNL TubeMogul] 转化事件。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement ID] | DSP中版面的唯一标识符。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Name] | 由用户分配的版面名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Budget] | 版面预算。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Max Bid] | 版面的最高竞价。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Device Environment] | 放置所定向的设备环境：(*[!UICONTROL Desktop]*, *[!UICONTROL Mobile]*&#x200B;和/或 *[!UICONTROL Connected TV])*. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement End Date] | 版面结束日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Start Date] | 版面开始日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Tags] | 用作版面自定义标识符的版面标记。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Description] | 与可计费区段关联的描述。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Key] | 与可计费区段关联的唯一键值。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Name] | 计费区段的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Description] | 与区段关联的描述，由数据提供商提供。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Key] | 与区段关联的唯一键值。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Name] | 区段的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Provider Name] | 与区段关联的数据提供程序的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Site ID] | DSP中网站或应用程序的唯一标识符。 |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Site Name] | 网站的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video Duration] | 视频长度，上传后会进行处理。 |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video ID] | DSP中视频创作的唯一标识符。 |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video Name] | 用户分配的创作元素的名称。 |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL % Distinct Uniques] | 的 [!UICONTROL App/Site Distinct Uniques] 除以 [!UICONTROL App/Site Uniques]. |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL App/Site Distinct Uniques] | 仅在此应用程序上访问的设备总数。 此值中不包含在多个发布者中对广告公开的查看者。 |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Cost per Distinct Unique] | 的 [!UICONTROL Total Spend] 除以 [!UICONTROL App/Site Distinct Uniques]. |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Cost per Unique] | 的 [!UICONTROL Total Spend] 除以 [!UICONTROL App/Site Uniques]. |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Estimated % Reached] | 接受接触的目标家庭群体的估计百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Estimated Average Frequency] | 显示给独特访客的平均展示次数。 对于某些内容库，发布者不会传递设备标识符，并且这些展示次数未包含在此值中。 中有一个类似的量度 [!UICONTROL Frequency (by App/Site)] 报表，但该量度无法估计。 |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Estimated Impressions (Device/Browser)] | (包含在 [!UICONTROL Frequency (by Impression)] 报表)给定频率分组的预计展示次数。 DSP估计基于展示次数的示例。 对于某些内容库，发布者不会传递设备标识符，并且这些展示次数未包含在此值中。 中有一个类似的量度 [!UICONTROL Frequency (by App/Site)] 报表，但该量度无法估计。 |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Estimated Uniques (Device/Browser)] | (包含在 [!UICONTROL Frequency (by Impression)] 报表)按给定频率记录的独特浏览器或设备的数量。 DSP估计基于展示次数的示例。 对于某些内容，请勿传递设备标识符，并且这些展示次数未包含在此值中。 中有一个类似的量度 [!UICONTROL Frequency (by App/Site)] 报表，但该量度无法估计。 |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Estimated Universe] | DSP（拍卖）在日期范围内看到的独特家庭总数。 |
| [!UICONTROL Metric] | [!UICONTROL Frequency] | [!UICONTROL Extended Impressions] | 使用设备图进行基于人员的跨设备定位所产生的总展示次数。 |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Frequency] | 每个家庭的展示次数。 |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Frequency Overlap] | 仅按报告维度到达家庭的频率，包括维度最多三个值的交集。 例如，如果您使用 [!UICONTROL Placement] 维度，则可以查看单个版面实现的频率、任意两个版面组合实现的频率以及任意三个版面组合实现的频率。 |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Incremental Household Reached] | 仅按报告维度到达的家庭数量，计算方式为 [仅报告维度所到达的IP地址] - [任何其他维度到达的IP地址]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL % Incremental Household Reached] | 仅按报告维度达到的家庭百分比，计算方式为 [维度所达到的IP地址百分比] - [任何其他维度所达到的IP地址百分比]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Impressions] | 提供的广告展示总数。 |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Measurable Impressions] | 根据可见性，能够测量的展示总次数。 |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Measurable Impressions (Overlap)] | 仅由报告的维度提供的可测展示次数总数，包括维度最多三个值的交集。 例如，如果您使用 [!UICONTROL Placement] 维度中，则可以查看各个版面获得的可测展示次数、任意两个版面组合获得的可测展示次数，以及任意三个版面组合获得的可测展示次数。 |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Total Media Spend] | 总支出。 |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Unique Household Reached] | 达到的独特家庭总数（不同的IP地址）。 |
| [!UICONTROL Metric] | [!UICONTROL Household] | [!UICONTROL Unique Household (Overlap)] | 仅由报告的维度达到的唯一家庭总数（不同的IP地址），包括维度最多三个值的交集。 例如，如果您使用 [!UICONTROL Placement] 维度中，您可以看到通过个人安置实现的独特家庭、通过任何两个安置组合实现的普通家庭以及通过任何三个安置组合实现的普通家庭。 |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Gross CPA] | 每次收购之平均总成本，按 [!UICONTROL Gross Spend] / [!UICONTROL Custom Goal]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Gross CPC] | 每次广告点击的平均总成本，计算方式为 [!UICONTROL Gross Spend] / [!UICONTROL Total Ad Clicks]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Gross CPCV] | 每次完成视频查看的平均成本，计算方式为 [!UICONTROL Gross Spend] / [!UICONTROL 100% Completions]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Gross CPM] | 每1000次展示的平均成本，计算方法为 [!UICONTROL Gross Spend] / [!UICONTROL Impressions] x 1000</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Gross CPV] | 每次视频查看的平均成本，计算方式为 [!UICONTROL Gross Spend] / [!UICONTROL Views]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Gross vCPM] | 每1000个可查看展示次数的平均成本，计算方法为 [!UICONTROL Gross Spend] / [!UICONTROL Viewable Impressions] x 1000</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Net CPC] | 每次广告点击的平均净成本，计算方式为 [!UICONTROL Net Spend] / [!UICONTROL Total Ad Clicks]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Net CPCV] | 每个已完成视频查看的平均净成本，计算方式为 [!UICONTROL Net Spend] / [!UICONTROL 100% Completions]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Net CPM] | 每1000次展示的平均净成本，计算方式为 [!UICONTROL Net Spend] / [!UICONTROL Impressions] x 1000</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Net CPV] | 每次视频查看的平均净成本，计算方式为 [!UICONTROL Net Spend] / [!UICONTROL Views]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Total Data eCPM] | 每1000次展示的平均净数据成本，计算方法为 [!UICONTROL Net Spend (Data)] / [!UICONTROL Impressions] x 1000</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Total Media CPM] | 每1000次展示的平均净媒体成本，计算方法为 [!UICONTROL Net Spend (Media)] / [!UICONTROL Impressions] x 1000</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Total Other eCPM] | 其他费用的每1000次展示的平均净成本，计算方法为 [!UICONTROL Net Spend (Other)] / [!UICONTROL Impressions] x 1000</code>. |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL % bid at Max CPM] | 在最高CPM下竞价的总竞价的百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Performance] | [!UICONTROL Unique Users Bid On] | DSP竞价版面的不同用户数。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Billable Data Net Spend] | 通过DSP计费的受众区段数据费用的净成本总额。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Billable Media Net Spend] | 通过DSP计费的可计费媒体的净成本总额，包括技术费用。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Billable Other Net Spend] | 通过DSP计费的其他服务费（第三方验证合作伙伴、广告服务等）的总成本。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Data] | 第三方受众区段和数据服务的预计税。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Media] | 媒体估计税项，包括适用于DSP中媒体成本重新计费及技术费用服务的税项。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Other] | 通过DSP计费的其他服务费用的估计税（包括第三方验证合作伙伴、主题定位等）。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Margin %] | （激活边距管理时）边距百分比，计算方式为([!UICONTROL Gross Spend] - [!UICONTROL Net Spend])/ [!UICONTROL Gross Spend]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Media Cost] | 不可计费和可计费的媒体成本总和，无需支付任何技术费用。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Net vCPM] | 每1000次可查看展示次数的平均净成本，计算方法为 [!UICONTROL Net Spend] / [!UICONTROL Viewable Impressions] x 1000</code>. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Data Net Spend] | 未通过DSP计费的受众区段数据费用的净成本总额。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Media Fees] | 不可计费媒体的净成本总额，包括技术费用，不通过DSP计费。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Other Net Spend] | 未通过DSP计费的其他服务费用（第三方验证合作伙伴、广告服务等）的总成本。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Profit] | [!UICONTROL Gross Spend] - [!UICONTROL Net Spend] |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Data Net Spend] | 受众区段数据费用的净成本总额。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Media Net Spend] | 媒体净成本总额，包括技术费用。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Net Spend] | 的总和 [!UICONTROL Net Spend (Media)], [!UICONTROL Net Spend (Data)]和 [!UICONTROL Net Spend (Other)]. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Non-Billable Net Spend] | 的总和 [!UICONTROL Non-billable Spend (Media)], [!UICONTROL Non-billable Spend (Data)]和 [!UICONTROL Non-billable Spend (Other)]. |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Other Net Spend] | 其他服务费用的净成本总额（第三方验证合作伙伴、广告服务等）。 |
| [!UICONTROL Metric] | [!UICONTROL Spend] | [!UICONTROL Total Billable Net Spend] | 的总和 [!UICONTROL Billable Spend (Media)], [!UICONTROL Billable Spend (Data)]和 [!UICONTROL Billable Spend (Other)]. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Completion Rate] | 观看了广告整个的查看次数百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Completions] | 观看了广告整个的查看次数。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Viewable Completion (%)] | 观看整个广告的可查看展示次数的百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 25% Completion Rate] | 观看了广告至少四分之一的查看次数的百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 25% Completions] | 观看了广告至少四分之一的查看次数。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Completion Rate] | 观看了广告至少两个四分位点的查看次数百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Completions] | 观看了广告至少两个四分位点的查看次数。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Viewable Completion (%)] | 观看了广告至少两个四分位点的可见展示次数的百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 75% Completion Rate] | 观看了广告至少三个四分位点的查看次数百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL 75% Completions] | 观看了广告至少三个四分位点的查看次数。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Avg Percent Viewed] | 观看至结束的广告的平均百分比，包括所有查看。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Banner and Overlay Clicks] | 广告叠加图和横幅的点击次数。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Click Through Rate] | 点击次数除以广告展示次数的百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks Per View Rate] | 点击次数除以视频查看次数的百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion Clicks] | 伴随横幅的点击次数。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion CTR] | 点击次数除以伴随横幅展示次数的百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion Impressions] | 伴随横幅展示次数。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Connection] | 用于查看广告的Internet连接类型（如Wifi或4g LTE）。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | 已投放广告的交互次数。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | 广告展示总次数。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Play Rate] | 产生视频查看次数的展示次数百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Playtime per View] | 视频查看的平均持续时间，以秒为单位。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Total Ad Clicks] | 广告的所有点击总和。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Viewed Minutes] | 视频广告被查看的总分钟数。 |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Views] | 视频广告查看的总次数。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Avg. Player Width x Height] | 平均播放器宽度和高度。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Measurable Impressions] | 根据可见性，能够测量的展示总次数。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Measurable Rate (%)] | 能够根据可见性测量的展示次数百分比，计算方式为 [!UICONTROL Measurable Impressions] x 1000 / [!UICONTROL Impressions]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - iFrame (%)] | 由于iFrame不兼容，因此无法衡量可视性的展示次数百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - Not Supported (%)] | 由于广告单元上不支持的可视性跟踪，因此无法测量可视性的展示次数。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - Other (%)] | 由于其他原因，无法衡量可见性的展示次数百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable Impressions] | 广告展示次数无法衡量是否可见。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable Rate (%)] | 广告展示次数的百分比无法衡量是否可见。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable rate (Not supported)] | 由于此广告单元上不支持的可视性跟踪，因此无法衡量可视性的展示次数百分比。 |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Viewability Rate (%)] | 可查看展示次数在所有可衡量展示次数中所占的百分比，计算方式为 [!UICONTROL Viewable Impressions] / [!UICONTROL Measurable Impressions]</code>. |
| [!UICONTROL Metric] | [!UICONTROL Viewability] | [!UICONTROL Viewable Impressions] | 被视为可查看的广告展示次数。 |
| [!UICONTROL Conversion Metrics] | [在报表设置中按广告商分组] | [特定于广告商的转化] | 特定于广告商的转化量度或Adobe Analytics事件的总计。 |
| [!UICONTROL Custom Goals] | [在报表设置中按广告商分组] | [广告商特定的自定义目标] | 指定 [自定义目标](/help/dsp/optimization/custom-goal-about.md). |

{style="table-layout:auto"}

<!-- |Omitted|[!UICONTROL Performance]|Custom Goal CPA|The average cost per acquisition, calculated by <code>Gross Spend / Custom Goal</code> | -->
<!-- |Omitted|[!UICONTROL Performance]|Custom Goal ROAS|The average return on ad spend, calculated by <code>Custom goal / Gross spend</code> |-->

>[!MORELIKETHIS]
>
>* [关于自定义报表](/help/dsp/reports/report-about.md)
>* [创建自定义报表](/help/dsp/reports/report-create.md)
>* [复制自定义报表](/help/dsp/reports/report-copy.md)
>* [编辑自定义报表](/help/dsp/reports/report-edit.md)
>* [自定义报表设置](/help/dsp/reports/report-settings.md)

