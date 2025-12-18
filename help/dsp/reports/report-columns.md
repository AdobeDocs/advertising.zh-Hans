---
title: 可用报表列
description: 请参阅自定义报表中可用列的说明。
feature: DSP Custom Reports
exl-id: 6dc30603-8a45-4188-aca6-591f3422b74a
source-git-commit: ab5d16d5132be59d2e902533155502c830c04bea
workflow-type: tm+mt
source-wordcount: '2467'
ht-degree: 0%

---

# 可用报表列

<!-- Add when added:

|[!UICONTROL Dimension]|[!UICONTROL Feed]|[!UICONTROL Deal List]|The name of a user-created deal list for which an ad was shown.|

-->

| 量度类型 | 子类型 | 列名称 | 描述 |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad External ID] | 外部广告服务器分配的广告ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad ID] | DSP中广告的唯一标识符。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Name] | 用户分配的广告名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Type] | 广告的格式。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Status] | 用户更改或日期输入表示的广告分类： *[!UICONTROL live]*、*[!UICONTROL scheduled]*、*[!UICONTROL completed]*&#x200B;或&#x200B;*[!UICONTROL archived]*。 |
| [!UICONTROL Dimension] | [!UICONTROL Advertiser] | [!UICONTROL Advertiser Name] | 广告商的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Budget] | 用户为营销活动分配的总预算。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign End Date] | 营销活动的结束日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign ID] | DSP中营销活动的唯一标识符。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign Name] | 用户分配的营销活动的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign Start Date] | 营销活动的第一个日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Title] | 内容/电影标题。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Series] | 内容系列。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Genre] | 内容流派。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL ProdQ] | 由[IAB技术实验室](https://github.com/InteractiveAdvertisingBureau/AdCOM/blob/main/AdCOM%20v1.0%20FINAL.md)定义的生产质量。 值可以`Unknown`、`Professionally Produced`、`Prosumer`或`User Generated`。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Context] | [IAB技术实验室](https://github.com/InteractiveAdvertisingBureau/AdCOM/blob/main/AdCOM%20v1.0%20FINAL.md)定义的内容类型。 值可以包括`Video,` `Game`、`Music`、`Application`、`Text`、`Other`或`Unknown`。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Content Rating] | 内容评级，例如PG或R。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Livestream] | 广告出现在直播流中： `Not Live`还是`Live`。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Content Length (in seconds)] | 内容的长度（以秒为单位）；通常用于视频或音频。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Language (as per ISO 639)] | 使用ISO-639-1-alpha-2的内容的语言。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Day (YYYY-MM-DD)] | 年、月、日。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | 日[!UICONTROL of Week] | 特定日期，如[!UICONTROL Monday]或[!UICONTROL Tuesday]。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Hour (YYYY-MM-DD HH)] | 年、月、日和小时。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Month (YYYY-MM)] | 月和年。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Time of Day] | 从0到23的整点时间。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Week (YYYY-MM-DD to YYYY-MM-DD)] | 相关周的日期范围，从星期日到星期六。 示例： 2021-02-18到2021-03-07。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser Vendor] | 显示广告的浏览器的供应商(例如Google或Mozilla)。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser Version] | 显示广告的浏览器版本（如[!UICONTROL Safari 4.3]或[!UICONTROL Chrome 7.0]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser] | 显示广告的浏览器（如[!UICONTROL Chrome]或[!UICONTROL Firefox]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Environment] | 广告显示于&#x200B;*[!UICONTROL sites]*&#x200B;还是&#x200B;*[!UICONTROL Apps]*。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Hardware] | 显示广告的设备类型（如[!UICONTROL Set Top Box]或[!UICONTROL Mobile Phone]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Manufacturer] | 显示广告的设备的制造商（如[!UICONTROL Samsung]、[!UICONTROL Lenovo]或[!UICONTROL Apple]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Model] | 显示广告的设备的型号（如[!UICONTROL iPhone XS]或[!UICONTROL Galaxy Note 7]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System Vendor] | 显示广告的操作系统的供应商（如[!UICONTROL Microsoft]或[!UICONTROL Apple]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System Version] | 显示广告的操作系统的版本（如[!UICONTROL Windows 10]或[!UICONTROL iOS Mojave]） |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System] | 显示广告的操作系统（如[!UICONTROL Apple iOS]或[!UICONTROL Android]）。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Deal Name] | 在DSP中输入的交易的用户分配名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Deal Type] | 交易是&#x200B;*[!UICONTROL Guaranteed]*&#x200B;还是&#x200B;*[!UICONTROL Non-Guaranteed]*。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Inventory Type] | 库存的分类： *[!UICONTROL Private]、* *[!UICONTROL On Demand]、*&#x200B;或&#x200B;*[!UICONTROL Public]*。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Private Deal ID] | 通过外部供应合作伙伴分配给私人交易的唯一标识符。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Publisher] | 提供库存的供应方合作伙伴。 这通常是发布者，但也可以是SSP。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL SSP] | 介质所属的供应方合作伙伴(SSP)。 |
| [!UICONTROL Dimension] | [!UICONTROL Frequency] | [!UICONTROL Frequency] | 设备收到广告的次数，基于唯一Cookie或设备ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL City] | 报告的数据所属的城市。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL Country] | 报告的数据所属的国家/地区。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL DMA] | 报告数据所属的指定市场区域(DMA)。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL Pin Code] | 报告数据所属的邮政索引号(PIN)代码。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL State] | 报告的数据所属的州/省。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Audience] | 观众。 此报表支持最多10个独特受众。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Campaign] | 营销活动。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Creative Length] | 创意的长度。 报表支持最多10个唯一的创意长度。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Device] | 设备。 此报表最多支持10个独特设备。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Feed Type] | 馈送的类型。 报表支持最多10种独特馈送类型。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Media Type] | 媒体类型。 报表支持多达10种独特的媒体类型。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Publisher] | 发布者。 此报表支持多达10个独特发布者。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Package] | 包。<!-- Note: The Package dimensions include another dimension called Package Name. --> |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Placement] | 投放位置。<!-- Note: The Placement dimensions include another dimension called Placement Name --> |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Site/Apps] | 提供广告展示的网站或应用程序。 报表最多支持10个唯一的网站或应用程序。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Tags] | 用作投放位置的自定义标识符的投放位置标记。 此报表最多支持10个唯一位置标记。<!-- Note: The Placement dimensions include another dimension called Placement Tags. --> |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Audience] | 观众。 |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Campaign] | 营销活动。 |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Creative Length] | 创意的长度。 |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Device] | 设备。 （例如CTV、桌面等） |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Media Type] | 媒体类型。 （如显示、音频等） |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Publisher] | 发布者。 |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Placement] | 投放位置。 |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight Budget] | 包裹航班的预算。 |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight End Date] | 包投放的结束日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight Rollover] | 包航班的任何变换预算。 |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight Start Date] | 程序包投放的开始日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package End Date] | 包的结束日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Goal Type] | 包的步调目标金额。 这一数额要么是支出，要么是印象。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package ID] | DSP中包的唯一标识符。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Name] | 程序包的名称 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Start Date] | 程序包开始日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Placement End Date] | 投放结束日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Pixel] | [!UICONTROL Conversion ID] | （已弃用）由DSP分配给旧版[!DNL TubeMogul]转化事件的转化ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Pixel] | [!UICONTROL Conversion Name] | （已弃用）分配给旧版[!DNL TubeMogul]转化事件的转化名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement ID] | DSP中投放位置的唯一标识符。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Name] | 用户指定的版面的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Budget] | 职位安排预算。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Max Bid] | 投放位置的最高出价。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Device Environment] | 投放目标所在的设备环境： （*[!UICONTROL Desktop]*、*[!UICONTROL Mobile]*&#x200B;和/或&#x200B;*[!UICONTROL Connected TV]）*。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement End Date] | 投放结束日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Start Date] | 投放开始日期。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Tags] | 用作投放位置的自定义标识符的投放位置标记。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Description] | 与计费区段关联的描述。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Key] | 与计费区段关联的唯一键。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Name] | 可计费区段的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Description] | 与区段关联的描述，由数据提供商提供。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Key] | 与区段关联的唯一键值。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Name] | 区段的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Provider Name] | 与区段关联的数据提供程序的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Site ID] | DSP中网站或应用程序的唯一标识符。 |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Site Name] | 站点的名称。 |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video Duration] | 上传后处理的视频长度。 |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video ID] | DSP中视频创意的唯一标识符。 |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video Name] | 用户分配的创意内容的名称。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL % Distinct Uniques] | [!UICONTROL App/Site Distinct Uniques]除以[!UICONTROL App/Site Uniques]。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL App/Site Distinct Uniques] | 仅在此应用程序中访问的设备总数。 此值不包括向多个发布者展示广告的查看器。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Cost per Distinct Unique] | [!UICONTROL Total Spend]除以[!UICONTROL App/Site Distinct Uniques]。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Cost per Unique] | [!UICONTROL Total Spend]除以[!UICONTROL App/Site Uniques]。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated % Reached] | 接受暴露的目标家庭宇宙的估计百分比。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Average Frequency] | 显示给独特数的平均展示次数。 对于某些库存，发布者不会传递设备标识符，并且这些展示不会包含在此值中。 [!UICONTROL Frequency (by App/Site)]报表中存在类似的量度，但未估计该量度。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Impressions (Device/Browser)] | （包含在[!UICONTROL Frequency (by Impression)]报表中）给定频率划分的预计展示次数。 DSP的估计基于一组展示次数。 对于某些库存，发布者不会传递设备标识符，并且这些展示不会包含在此值中。 [!UICONTROL Frequency (by App/Site)]报表中存在类似的量度，但未估计该量度。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Uniques (Device/Browser)] | （包含在[!UICONTROL Frequency (by Impression)]报表中）在给定频率下记录的独特浏览器或设备数。 DSP的估计基于一组展示次数。 对于某些库存，请勿传递设备标识符，并且这些展示不会包含在此值中。 [!UICONTROL Frequency (by App/Site)]报表中存在类似的量度，但未估计该量度。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Universe] | DSP（拍卖）在日期范围内看到的独特家庭总数。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Extended Impressions] | 因使用设备图进行基于人员的跨设备定位而提供的展示总数。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Frequency] | 每个家庭的印象频率。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Frequency Overlap] | 仅按报告的维度到达住户的频率，包括维度最多三个值的交集。 例如，如果使用[!UICONTROL Placement]维度，则可以查看单个投放位置所实现的频率、任意两个投放位置组合所实现的频率以及任意三个投放位置组合所实现的频率。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Incremental Household Reached] | 仅报告维度可访问的家庭数，计算为仅报告维度可访问的<code>[IP地址] - [任何其他维度可访问的IP地址]</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL % Incremental Household Reached] | 仅通过报告的维度实现的家庭百分比，计算为<code>[维度实现的IP地址的百分比] - [任何其他维度实现的IP地址的百分比]</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Impressions] | 提供的广告展示总数。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Measurable Impressions] | 提供的能够测量可见性的展示总数。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Measurable Impressions (Overlap)] | 仅报告维度提供的可测量展示总数，包括最多三个维度值的交集。 例如，如果您使用[!UICONTROL Placement]维度，则可以查看由单个投放位置实现的可测量展示次数、由任意两个投放位置组合实现的可测量展示次数，以及由任意三个投放位置组合实现的可测量展示次数。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Total Media Spend] | 总支出。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Unique Household Reached] | 到达的唯一家庭总数（不同的IP地址）。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Unique Household (Overlap)] | 仅报告维度实现的唯一家庭总数（不同的IP地址），包括维度中最多三个值的交集。 例如，如果您使用[!UICONTROL Placement]维度，则可以查看由单个投放位置到达的唯一家庭、由任意两个投放位置组合到达的共同家庭，以及由任意三个投放位置组合到达的共同家庭。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Cost per Incremental HH] | 总支出除以所实现的增量家庭。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Cost per Unique HH] | 所达到的总支出除以独特家庭。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Frequency] | 每个家庭的印象频率。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Incremental Household Reached] | 仅报告维度可到达的家庭数，计算为仅报告维度[可到达的]IP地址 — 任何其他维度[可到达的]IP地址。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL % Incremental Household Reached] | 仅通过报告的维度实现的家庭百分比，计算为[维度实现的IP地址的百分比] - [任何其他维度实现的IP地址的百分比]。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Impressions] | 提供的广告展示总数。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Measurable Impressions] | 提供的能够测量可见性的展示总数。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Total Media Spend] | 总支出。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Unique Household Reached] | 到达的唯一家庭总数（不同的IP地址）。 |
| [!UICONTROL Metrics] | [!UICONTROL Identifier] | [!UICONTROL Identifier Type] | 定向的ID类型。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL % bid at Max CPM] | 在最大CPM中出价的总数的百分比。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPA] | 每次购置的平均总成本，由<code>[!UICONTROL Gross Spend] / [!UICONTROL conversion metric]计算</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPC] | 每次广告点击的平均总成本，计算方式为<code>[!UICONTROL Gross Spend] / [!UICONTROL Total Ad Clicks]</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPCV] | 每个已完成的视频视图的平均成本，由<code>[!UICONTROL Gross Spend] / [!UICONTROL 100% Completions]计算</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPE] | 每次广告参与的平均总成本，计算方式为<code>[!UICONTROL Gross Spend] / [!UICONTROL Total Ad Engagements]</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPI] | 每次广告展示的平均总成本，计算方式为<code>[!UICONTROL Gross Spend] / [!UICONTROL Total Ad Impressions]</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPM] | 每1000次展示的平均成本，计算方式为<code>[!UICONTROL Gross Spend] / [!UICONTROL Impressions] x 1000</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPV] | 每个视频查看的平均成本，由<code>[!UICONTROL Gross Spend] / [!UICONTROL Views]计算</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross Custom Goal CPA] | <code>[!UICONTROL Gross Spend] / [!UICONTROL Custom Goal]</code>，其中[!UICONTROL Custom Goal]是附加到自定义目标的所有转化的目标权重。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross vCPM] | 每1000个可见展示的平均成本，计算方式为<code>[!UICONTROL Gross Spend] / [!UICONTROL Viewable Impressions] x 1000</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPC] | 每次广告点击的平均净成本，计算方式为<code>[!UICONTROL Net Spend] / [!UICONTROL Total Ad Clicks]</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPCV] | 每个已完成的视频视图的平均净成本，由<code>[!UICONTROL Net Spend] / [!UICONTROL 100% Completions]计算</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPI] | 每次广告展示的平均净成本，计算方式为<code>[!UICONTROL Net Spend] / [!UICONTROL Total Ad Impressions]</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPM] | 每1000次展示的平均净成本，计算方式为<code>[!UICONTROL Net Spend] / [!UICONTROL Impressions] x 1000</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPV] | 每个视频查看的平均净成本，由<code>[!UICONTROL Net Spend] / [!UICONTROL Views]计算</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net vCPM] | 每1000个可见展示的平均净成本，计算方式为<code>[!UICONTROL Net Spend] / [!UICONTROL Viewable Impressions] x 1000</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Unique Users Bid On] | DSP为投放位置竞价的不同用户的数量。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Agency Fee] | 代理服务费。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Creative Spend] | 从Adobe Creative提供的广告的总支出。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Data Spend] | 通过DSP计费的受众区段数据费用总净成本。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Media Spend] | 通过DSP计费的可计费媒体的总净成本，包括技术费用。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Other Spend] | 通过DSP计费的其他服务费用（第三方验证合作伙伴、广告投放等）的总成本。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Creative] | 对Adobe Creative提供的广告的预计税额。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Data] | 第三方受众区段和数据服务的预计税额。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Media] | 对媒体的估计赋税，包括应用于DSP中的媒体成本再计费和技术费用服务的赋税。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Other] | 通过DSP计费的其他服务费的估计税费（包括第三方验证合作伙伴、主题定位等）。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Gross Spend] | 总支出。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Margin %] | （激活利润管理时）利润百分比，由<code>([!UICONTROL Gross Spend] - [!UICONTROL Net Spend]) / [!UICONTROL Gross Spend]计算</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Media Cost] | 不收取任何技术费用的非计费和计费媒体成本的总和。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Net vCPM] | 每1000个可见展示的平均净成本，计算方式为<code>[!UICONTROL Net Spend] / [!UICONTROL Viewable Impressions] x 1000</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non Billable Creative Spend] | 未通过Adobe Creative计费的广告的总支出。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Data Spend] | 未通过DSP计费的受众区段数据费用总净成本。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Media Spend] | 不通过DSP计费的不可计费媒体的总净成本，包括技术费用。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Other Net Spend] | 未通过DSP计费的其他服务费用（第三方验证合作伙伴、广告投放等）的总成本。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Profit] | [!UICONTROL Gross Spend] - [!UICONTROL Net Spend] |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Billable Spend] | [!UICONTROL Billable Spend (Media)]、[!UICONTROL Billable Spend (Data)]和[!UICONTROL Billable Spend (Other)]的总和。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Creative CPM] | 从Adobe Creative提供的广告的每1000次展示的平均净媒体成本。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Creative Spend] | 从Adobe Creative提供的广告的总计可记帐和不可记帐支出。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Data eCPM] | 每1000次展示的平均净数据成本，计算方式为<code>[!UICONTROL Net Spend (Data)] / [!UICONTROL Impressions] x 1000</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Data Spend] | 受众区段数据费用总净成本。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Media CPM] | 每1000次展示的平均净媒体成本，计算方式为<code>[!UICONTROL Net Spend (Media)] / [!UICONTROL Impressions] x 1000</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Media Spend] | 包括技术费用在内的媒体净成本总额。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Net Spend] | [!UICONTROL Net Spend (Media)]、[!UICONTROL Net Spend (Data)]和[!UICONTROL Net Spend (Other)]的总和。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Non-Billable Net Spend] | [!UICONTROL Non-billable Spend (Media)]、[!UICONTROL Non-billable Spend (Data)]和[!UICONTROL Non-billable Spend (Other)]的总和。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Other eCPM] | 按<code>[!UICONTROL Net Spend (Other)] / [!UICONTROL Impressions] x 1000计算的其他费用每1000次展示的平均净成本</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Other Spend] | 其他服务费用（第三方验证合作伙伴、广告服务等）的总净成本。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Completion Rate] | 观看整个广告的查看次数的百分比。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Completions] | 观看整个广告的查看次数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Viewable Completion (%)] | 观看整个广告的可查看展示次数百分比。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 25% Completion Rate] | 观看至少四分之一的广告的查看次数的百分比。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 25% Completions] | 观看至少四分之一的广告的查看次数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Completion Rate] | 至少观看了广告四分位数的观看次数百分比。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Completions] | 至少观看了广告四分位数的观看次数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Viewable Completion (%)] | 观看至少四分位广告的可查看展示次数百分比。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 75% Completion Rate] | 观看至少四分之三广告的查看次数的百分比。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 75% Completions] | 观看至少四分之三广告的查看次数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Avg Percent Viewed] | 广告观看至结束的平均百分比，其中包括所有查看次数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Banner and Overlay Clicks] | 广告叠加和横幅的点击次数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Click Through Rate] | 点击次数百分比除以广告展示次数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks Per View Rate] | 点击次数百分比除以视频查看次数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion Clicks] | 伴随的横幅点击次数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion CTR] | 点击次数百分比除以随附横幅展示次数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion Impressions] | 随附横幅展示次数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Connection] | 用于查看广告的Internet连接类型（如Wifi或4g LTE）。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | 投放广告的交互次数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | 广告展示总数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Play Rate] | 提供并导致视频查看次数的展示次数百分比。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Playtime per View] | 视频查看的平均持续时间，以秒为单位。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Total Ad Clicks] | 广告所有点击次数总和。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Viewed Minutes] | 视频广告被查看的总分钟数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Views] | 视频广告查看总数。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Avg. Player Width x Height] | 平均播放器宽度和高度。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Measurable Impressions] | 提供的能够测量可见性的展示总数。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Measurable Rate (%)] | 提供的能够测量可见性的展示次数百分比，计算为<code>[!UICONTROL Measurable Impressions] x 1000 / [!UICONTROL Impressions]</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - iFrame (%)] | 由于不兼容的iFrame而无法测量可见性的展示次数百分比。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - Not Supported (%)] | 由于广告单元上不支持的可视性跟踪而不可测量的可视性展示次数。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - Other (%)] | 由于其他原因而不可测量的可见性的展示次数百分比。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable Impressions] | 不可测量的可见性的广告展示次数。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable Rate (%)] | 不可测量的可视性广告展示的百分比。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable rate (Not supported)] | 由于此广告单位上不支持的可见性跟踪而无法测量可见性的展示次数百分比。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Viewability Rate (%)] | 所有可衡量的展示次数中的可见展示次数的百分比，计算为<code>[!UICONTROL Viewable Impressions] / [!UICONTROL Measurable Impressions]</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Viewable Impressions] | 被视为可查看的广告展示次数。 |
| [!UICONTROL Conversion Metrics] | [在报告设置中按广告商分组] | [广告商特定转化] | 指定的特定于广告商的转化量度或Adobe Analytics事件的总数。 |
| [!UICONTROL Custom Goals] | [在报告设置中按广告商分组] | [特定于广告商的自定义目标] | 指定[自定义目标](/help/dsp/optimization/custom-goal.md)中包含的所有转化的加权总和。 |

{style="table-layout:auto"}

<!-- |Omitted|[!UICONTROL Performance]|Custom Goal ROAS|The average return on ad spend, calculated by <code>Custom goal / Gross spend</code> |-->

>[!MORELIKETHIS]
>
>* [关于自定义报告](/help/dsp/reports/report-about.md)
>* [创建自定义报告](/help/dsp/reports/report-create.md)
>* [复制自定义报告](/help/dsp/reports/report-copy.md)
>* [编辑自定义报告](/help/dsp/reports/report-edit.md)
>* [自定义报表设置](/help/dsp/reports/report-settings.md)
