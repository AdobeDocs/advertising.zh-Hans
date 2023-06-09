---
title: 基本报表和高级报表的报表列
description: 了解基本报表和高级报表的可用数据列。
source-git-commit: 7327c91b92b6471fa8da8767fc764de4226b4f91
workflow-type: tm+mt
source-wordcount: '3653'
ht-degree: 0%

---

# 基本报表和高级报表的报表列

| 列 | 描述 |
| ---- | ---- |
| \[特定于广告商的自定义（派生）量度\] | 的值 [您已创建的自定义量度](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) 从现有指标计算得出的中间值。 |
| \[广告商特定的标签分类\] | 当前应用于实体的实体级别的任何标签分类。 多个标签分类使用逗号(，)分隔。 |
| \[广告商特定的事务属性\] | 指定事务属性或网站参与度量的转化次数。 |
| \[Google跟踪的转化/事务属性\] | 请参见“GGL\*、GGL_CT\*和GGL_XD_CT\*”条目。 |
| [!UICONTROL 7-Day Click Accuracy] | ([!UICONTROL Portfolio Report])过去7天（不包括当天，不包括报表指定的日期范围）的点击预测的平均准确性，以百分比表示。 |
| [!UICONTROL 7-Day Cost Accuracy] | ([!UICONTROL Portfolio Report])过去7天（不包括当天，不包括报表指定的日期范围）的成本预测的平均准确性，以百分比表示。 |
| [!UICONTROL 7-Day Revenue Accuracy] | ([!UICONTROL Portfolio Report])过去7天（不包括当天，不包括报表指定的日期范围）的收入预测的平均准确性，以百分比表示。 |
| [!UICONTROL Account] | 帐户名称。 |
| [!UICONTROL Account Status] | Search、Social和Commerce中帐户的状态： <ul><li><i>[!UICONTROL Enabled]：</i> （默认）对于同步的广告网络，Search、Social和Commerce可以登录到广告网络帐户以检索促销活动数据，并且还启用了其他适用的功能，例如优化和跟踪生成。<br><br>对于未同步的广告网络，可以使用优化和/或跟踪生成等适用的功能。</li><li><i>[!UICONTROL Disabled]：</i> 对于同步的广告网络，搜索、社交和商务不会登录到广告网络帐户，因此不会检索促销活动数据，并且其他适用的功能（例如优化和跟踪生成）将被禁用。 虽然仍会存储启用帐户时收集的数据，但您将来创建的所有营销活动管理视图和所有报表都不会包含禁用帐户期间的数据。<br><br>对于未同步的广告网络，不提供适用的功能，例如优化和/或跟踪生成。</li></ul> |
| [!UICONTROL Active Ad Groups] | 活动广告组的数量。 |
| [!UICONTROL Active Ads/Creatives] | 活动广告/创意内容的数量。 |
| [!UICONTROL Active Campaigns] | 活动营销活动的数量。 |
| [!UICONTROL Active Keywords] | 活动关键字的数量。 |
| [!UICONTROL Ad Group] | 广告组。 |
| [!UICONTROL Ad Group ID] | Search、Social和Commerce分配给广告组的数值ID。 |
| [!UICONTROL Ad Group Status] | 广告组状态： <i>[!UICONTROL Active]</i>， <i>[!UICONTROL Paused]</i>，或 <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Type] | 广告组类型，如 <i>[!UICONTROL Audience]</i> （仅适用于受众营销活动）， <i>[!UICONTROL Discovery]</i> （仅适用于发现活动）， <i>[!UICONTROL Display]</i> （仅适用于显示促销活动）， <i>[!UICONTROL Search Dynamic]</i> （仅适用于动态搜索广告）， <i>[!UICONTROL Search Standard]</i> （仅适用于响应式搜索广告和现有的扩展文字广告）， <i>[!UICONTROL Shopping Showcase]</i>， <i>[!UICONTROL Shopping Product]</i> （仅适用于标准购物营销活动），或 <i>[!UICONTROL Shopping Smart]</i> （用于智能购物营销活动）。 对于某些营销活动类型，单个营销活动可以包含多个广告类型。 |
| [!UICONTROL Ad Groups] | 为其分配标签值的广告组的数量。 |
| [!UICONTROL AD Name] | 广告组名称；与的值相同 [!UICONTROL Ad Group]. |
| [!UICONTROL Ad Size] | 广告的维度。 |
| [!UICONTROL AD Strength] | ([!DNL Google Ads] 响应式搜索广告)广告效果： <i>[!UICONTROL average]</i>， <i>[!UICONTROL excellent]</i>， <i>[!UICONTROL good]</i>， <i>[!UICONTROL no_ads]</i>， <i>[!UICONTROL pending]</i>， <i>[!UICONTROL poor]</i>， <i>[!UICONTROL unknown]</i>，或 <i>[!UICONTROL unspecified]</i>. |
| [!UICONTROL Adgroup MBA] | ([!DNL Google Ads]， [!DNL Microsoft Advertising]、和 [!DNL Yahoo! Japan Ads] campaigns)当前广告组级别的移动竞价调整，它确定在移动设备上显示广告时如何调整竞价。 |
| [!UICONTROL Advertiser] | 广告商名称。 |
| [!UICONTROL Advertiser ID] | 广告商的搜索、社交和商务帐户的数值ID。 |
| [!UICONTROL Avg Position] | 指定日期范围内的广告平均位置。<br><br>对象 [!DNL Google Ads] 和 [!DNL Yahoo! Japan Ads] 营销活动，此数据仅在2019年9月之前可用。 对象 [!DNL Microsoft Advertising]，此数据仅在2021年1月22日之前可用。 |
| [!UICONTROL Base URL] | 关键字的基本URL，包括为促销活动或帐户配置的任何附加参数。 它不包括任何搜索、社交和商务重定向和跟踪代码。 |
| [!UICONTROL Bid Strategy] | （大多数广告网络）对于促销活动或促销活动组件，这是促销活动的竞价策略。 对于链接到经理帐户的广告网络帐户，这是跨帐户竞价策略。 可用值因广告网络而异。 |
| [!UICONTROL Business Name] | ([!DNL Microsoft Advertising] 响应式广告)业务名称。 |
| [!UICONTROL Call to Action] | ([!DNL Microsoft Advertising] 响应式广告和多媒体广告)广告中包含的行动号召。 |
| [!UICONTROL Campaign] | 营销活动。 |
| [!UICONTROL Campaign Budget] | 营销活动预算。 |
| [!UICONTROL Campaign MBA] | ([!DNL Google Ads]， [!DNL Microsoft Advertising]、和 [!DNL Yahoo! Japan Ads] campaigns)当前的营销活动级别的移动竞价调整，它确定在移动设备上显示广告时如何调整竞价。 |
| [!UICONTROL Campaign Start Date] | 营销活动投标/投标的第一天。 |
| [!UICONTROL Campaign Status] | 营销活动状态： <i>[!UICONTROL Active]</i>， <i>[!UICONTROL Paused]</i>， <i>[!UICONTROL Ended]</i>，或 <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Campaign Type] | 营销活动类型，如 <i>[!UICONTROL Audience (Image)]</i>， <i>[!UICONTROL Audience (Feed)]</i>， <i>[!UICONTROL Discovery]</i>， <i>[!UICONTROL Search and Display]</i>， <i>[!UICONTROL Standard Display]</i>， <i>[!UICONTROL Standard Performance Max]</i>， <i>[!UICONTROL Standard Search]</i>， <i>[!UICONTROL Standard Shopping]</i>， <i>[!UICONTROL Video]</i>，或 <i>[!UICONTROL Others]</i>. |
| [!UICONTROL Channel Type] | 营销渠道类型： <i>[!UICONTROL Search]</i> 或 <i>[!UICONTROL Content]</i>. 当报告的 [!UICONTROL Search/Content] 报表设置中的设置为&quot;[!UICONTROL Combined].” |
| [!UICONTROL City] | ([!UICONTROL Geo Distribution Report]， [!UICONTROL Transaction Report])产生点击的城市。 根据用户的IP地址确定。 |
| [!UICONTROL Click Match Type] | 关键词与所点击的广告的类型匹配。 这与 [!UICONTROL Listing Match Type] 除了 [!DNL Microsoft Advertising] 具有多个匹配类型的关键字。 对象 [!DNL Microsoft Advertising] 关键字，这是实际点击的匹配类型。 |
| [!UICONTROL Click Value] | ([!UICONTROL Portfolio Report])为项目组合的目标指定的点击值。 |
| [!UICONTROL Click/Impression Time] | ([!UICONTROL Transaction Report])导致转化的点击或展示发生的时间。 |
| [!UICONTROL Clicks] | 在指定日期范围内对广告的点击次数。 |
| [!UICONTROL Client ID1], [!UICONTROL Client Id 1] | ([!UICONTROL Keyword Report]， [!UICONTROL Ad Variation Report]、和 [!UICONTROL Transaction Report]；基于信息源的跟踪实施)在信息源文件中发送的关键字或广告特定于客户端的跟踪ID。 |
| [!UICONTROL Client Id 2] | ([!UICONTROL Keyword Report] 和 [!UICONTROL Transaction Report]；基于信息源的跟踪实施)在信息源文件中发送的关键字或广告特定于客户端的跟踪ID。 |
| [!UICONTROL Client Transaction ID] | ([!UICONTROL Transaction Report])唯一交易ID。 |
| [!UICONTROL Constraint End Date] | ([!UICONTROL Constraint Report])约束处于活动状态的最后一天。 |
| [!UICONTROL Constraint Name] | ([!UICONTROL Constraint Report])约束名称。 |
| [!UICONTROL Constraint Start Date] | ([!UICONTROL Constraint Report])约束处于活动状态的第一天。 |
| [!UICONTROL Constraint Status] | ([!UICONTROL Constraint Report])约束的状态：  <i>[!UICONTROL Active]</i> 或 <i>[!UICONTROL Paused]</i>. |
| [!UICONTROL Constraint Type] | ([!UICONTROL Constraint Report])约束的类型：  <i>[!UICONTROL Bid/Pos Constraint]</i>， <i>[!UICONTROL Bid Shift]</i>， <i>[!UICONTROL Campaign Budget]</i>， <i>[!UICONTROL Context Sensitive Bid]</i>， <i>[!UICONTROL Incremental Bidding]</i>， <i>[!UICONTROL Max CPA]</i>， <i>[!UICONTROL Min Margin]</i>， <i>[!UICONTROL Variable Bid Position]</i>， <i>[!UICONTROL Search Engine Min Bid]</i>，或 <i>[!UICONTROL Variable Position]</i>. |
| [!UICONTROL Constraints] | 图元上任何适用约束的名称，用逗号分隔。 |
| [!UICONTROL Content IS] | 您收到的展示次数/受众网络上广告的展示次数除以您有资格接收的估计展示次数。 In [!DNL Microsoft Advertising]，这称为&quot;[!UICONTROL Audience IS].” |
| [!UICONTROL Content IS Lost (budget)] | 由于每日或每月预算过低，在显示/受众网络上的广告未收到的估计展示次数百分比。 In [!DNL Microsoft Advertising]，这称为&quot;[!UICONTROL Audience lost IS (budget)].” |
| [!UICONTROL Content IS Lost (rank)] | 由于广告排名不佳而未显示在显示/受众网络上的广告的预计展示百分比。 In [!DNL Microsoft Advertising]，这称为&quot;[!UICONTROL Audience lost IS (rank)].” |
| [!UICONTROL Conversion Type] | ([!UICONTROL Transaction Report])转换之前的操作：<ul><li><i>[!UICONTROL Click:]</i> 转换前至少发生一次付费点击。</li><li><i>[!UICONTROL Impression:]</i> 转化之前未发生付费点击，因此转化源自浏览（无任何付费点击的展示）。</li></ul> |
| [!UICONTROL Cost] | 指定日期范围内的广告总成本。 |
| [!UICONTROL Country] | ([!UICONTROL Geo Distribution Report]， [!UICONTROL Keyword Report])发起点击的国家/地区。 根据用户的IP地址确定。 |
| [!UICONTROL CPC] | 指定日期范围内广告的每次点击成本(CPC)。 |
| [!UICONTROL Creative Base URL] | 广告的基本URL，包括为促销活动或帐户配置的任何附加参数。 它不包括任何搜索、社交和商务重定向和跟踪代码。 |
| [!UICONTROL Creative Destination URL] | 广告的最终URL或目标URL（包括任何跟踪参数）。 |
| [!UICONTROL Creative Name] | ([!DNL Yahoo! Japan] 仅限)广告图像名称。 |
| [!UICONTROL Creative Title], [!UICONTROL Creative Title2] - [!UICONTROL Creative Title3] | 广告的标题或标题。 不同的创意类型具有不同的必需标题行和可选标题行数。 查看 [!UICONTROL Creative Title4] 和更高列数 [!DNL Microsoft Advertising] 响应式广告或多媒体广告，包括“[!UICONTROL Creative Titles]”列。 |
| [!UICONTROL Creative Titles] | （仅适用于多媒体和响应式搜索广告）为每个广告的简短标题添加一列(”[!UICONTROL Creative Title]“ — ”[!UICONTROL Creative Title15]“)。 包含此列时，无需包含其他列 [!UICONTROL Creative Title] 列，但编辑 [!UICONTROL Order Results/Limit Rows By] 排序依据部分 [!UICONTROL Creative Titles] 而不是 [!UICONTROL Creative Title]. |
| [!UICONTROL Creative Type] | 广告格式。 以下是可能的值： <i>[!UICONTROL App Install Ad]</i>， <i>[!UICONTROL Call Only Ad]</i>， <i>[!UICONTROL Discovery Ad (single-image ads)]</i>， <i>[!UICONTROL Discovery Carousel Ad]</i> （多图像轮播广告）， <i>[!UICONTROL Display Ad]</i>， <i>[!UICONTROL Dynamic Search Ad]</i>， <i>[!UICONTROL Expanded Dynamic Search Ad]</i>， <i>[!UICONTROL Expanded Text Ad]</i>， <i>[!UICONTROL Legacy Text Ad]</i>， <i>[!UICONTROL Multimedia Ad]</i>， <i>[!UICONTROL Product Ad]</i>， <i>[!UICONTROL Responsive Ad]</i>， <i>[!UICONTROL Responsive Search Ad]</i>，或 <i>[!UICONTROL Text Ad]</i>. |
| [!UICONTROL CTR] | 点进率，即点击次数除以所包含广告的展示次数。 |
| [!UICONTROL Currency] | 适用的货币类型（如“USD”或“GBP”）。<br><br><b>注意：</b> 如果报表包含使用不同货币的帐户的数据，则为任意[!UICONTROL Total]“货币值只是列中所有数字的总和，不考虑货币。 |
| [!UICONTROL Current Bid] | 目标的当前竞价。 |
| [!UICONTROL Current First Page Bid] | ([!DNL Google Ads] 仅限营销活动)在以下情况下，将广告投放到搜索结果第一页时当前所需的预计每次点击成本(CPC)竞价： [!DNL Google] 搜索查询与关键字匹配。<br><br>对于单个关键字和匹配类型组合，此值是该组合当前所需的第一个页面竞价。 在多个营销活动中使用相同的关键词和匹配类型组合时，此值是当前所有实例中所需的最低首页竞价。 |
| [!UICONTROL Current Quality Score] | ([!DNL Google Ads] 和 [!DNL Microsoft Advertising] 仅限营销活动)由广告网络指定的关键词或竞价单位的当前质量分数。 其范围从1（低）到10（完美）。 对于单个关键字和匹配类型组合，此值是该组合的当前分数。 当在多个营销活动中使用相同的关键词和匹配类型组合时，此值是所有实例中的最大当前分数。<br><br>广告网络使用质量分数来确定竞价和广告位置。 根据多种因素计算关键词，包括关键词与其相关广告、用户搜索查询的相关性和登陆页面的质量。 对于中的关键字 [!DNL Google Ads]，则也会考虑关键词的点进率，以及 [!DNL Microsoft Advertising]中，也会考虑登陆页面提供的用户体验。 |
| [!UICONTROL Custom Bid Level] | (仅针对展示网络的Google促销活动)发出竞价的级别：由 <i>[!UICONTROL Ad Group]</i>， <i>[!UICONTROL Age]</i>， <i>[!UICONTROL Gender]</i>， <i>[!UICONTROL Interest and List]</i>， <i>[!UICONTROL Keyword]</i>， <i>[!UICONTROL Placement]</i>， <i>[!UICONTROL Vertical]</i>， <i>[!UICONTROL None]</i>，或 <i>[!UICONTROL Unknown]</i>. |
| [!UICONTROL Description1] - [!UICONTROL Description4] | 广告的正文。 不同的创意类型具有不同的必需和可选描述行数。 查看 [!UICONTROL Description3] 和 [!UICONTROL Description4] 中的列 [!DNL Microsoft Advertising] 响应式广告或多媒体广告，包括“[!UICONTROL Descriptions]”列。 |
| [!UICONTROL Descriptions] | ([!DNL Microsoft Advertising] 响应式广告和多媒体广告)为每个广告的描述行添加一列(&quot;[!UICONTROL Description1]“ — ”[!UICONTROL Description4]“)。 包含此列时，无需包含其他列 [!UICONTROL Description] 列。 |
| [!UICONTROL Device] | ([!DNL Google Ads]， [!DNL Microsoft Advertising]， [!DNL Yahoo! Display Network]， [!DNL Yahoo! Japan Ads]、和 [!DNL Yahoo Native] campaigns)显示广告的设备类型： <i>[!UICONTROL Computers]</i>， <i>[!UICONTROL Mobile]</i>， <i>[!UICONTROL Tablets]</i>， <i>[!UICONTROL Other]</i>，或 <i>[!UICONTROL N/A]</i> （无值）。 其他广告网络的行的值为N/A。<br><br>在搜索营销活动中，如果关键词、广告和/或广告扩展的跟踪模板或目标URL包含按设备跟踪数据的参数(`&ev_dvc={device}&ev_dvm={devicemodel}`)时，转化数据也会包含在每种设备类型的行中。 否则，如果转化数据无法归因于某个设备类型，则会汇总到单独的一行中，其中包含“[!UICONTROL Device]的“ ”值 [!UICONTROL N/A]. |
| [!UICONTROL Display Path 1] | ([!DNL Google Ads] 仅限扩展文本广告)广告的基本URL之后的第一个显示路径。 |
| [!UICONTROL Display Path 2] | ([!DNL Google Ads] 仅限扩展文本广告)广告的基本URL之后的第二个显示路径。 |
| [!UICONTROL Display Type] | 已过时 |
| [!UICONTROL Display URL] | 广告的显示URL，最终用户可在广告中看到此URL。 |
| [!UICONTROL DMA] | ([!UICONTROL Geo Distribution Report]， [!UICONTROL Keyword Report])作为点击来源的指定数字市场区域（例如，751表示丹佛）。 根据用户的IP地址确定。 |
| [!UICONTROL Domain] | ([!UICONTROL Domain Referral Report]， [!UICONTROL Keyword Report])发起点击的域名。 |
| [!UICONTROL eCPM] | 有效CPM，或在指定日期范围内每1000次展示所支付的平均成本。 可以为CPM或CPC营销活动计算eCPM值。 |
| [!UICONTROL EF Campaign ID] | Search、Social和Commerce分配给营销活动的数值ID。 |
| [!UICONTROL EF ID] | ([!UICONTROL Transaction Report])(使用Adobe Advertising转化跟踪服务和&quot;[!UICONTROL EF Redirect]带有令牌的跟踪方法)用于点击或转换的令牌。<ul><li>对象 [!DNL Google Ads] 搜索广告，EF ID为 `{gclid}:G:s`，其中包括Google点击ID (GCLID)和网络类型（搜索中为“s”）。</li><li> 对象 [!DNL Microsoft Advertising] 搜索广告，EF ID为 `{msclkid}:G:s`，其中包括Microsoft点击ID (MSCLKID)和网络类型（搜索中为“s”）。</li><li>对于其他广告网络上的搜索广告，EF ID包括冲浪者ID、点击时间和网络类型。</li><li>对于展示广告，EF ID包括浏览者ID、点击或展示时间以及网络类型。</li></ul> |
| [!UICONTROL EF Pixel Location ID] | ([!UICONTROL Geo Distribution Report]；仅用于搜索、社交和商务)地理位置的内部ID，用于标准化数据。 |
| [!UICONTROL EF Portfolio Group ID] | 项目组合所属的项目组合组的数值ID。 |
| [!UICONTROL EF Search Engine ID] | Search、Social和Commerce分配给广告网络的数值ID：  <i>[!UICONTROL 3]</i> 对象 [!DNL Google Ads]， <i>[!UICONTROL 10]</i> 对象 [!DNL Microsoft Advertising]， <i>[!UICONTROL 45]</i> 对象 [!DNL Meta]， <i>[!UICONTROL 86]</i> 对象 [!DNL Yahoo! Display Network]， <i>[!UICONTROL 87]</i> 对象 [!DNL Naver]， <i>[!UICONTROL 88]</i> 对象 [!DNL Baidu]， <i>[!UICONTROL 90]</i> 对象 [!DNL Yandex]， <i>[!UICONTROL 94]</i> 对象 [!DNL Yahoo! Japan Ads]， <i>[!UICONTROL 105]</i> 对象 [!DNL Yahoo Native] （已弃用），或 <i>[!UICONTROL 106]</i> 对象 [!DNL Pinterest] （已弃用）。 |
| [!UICONTROL End Date] | 报告的最后一天。 |
| [!UICONTROL Engagement Rate] | （视频广告）参与次数除以广告显示次数。 |
| [!UICONTROL Engagements] | （视频广告）用户观看您的广告至少10秒的次数，如果少于10秒，则为完整广告。 |
| [!UICONTROL Est. Clicks] | ([!UICONTROL Geo Distribution Report]；仅限搜索和显示营销活动)广告组/营销活动/项目组合的预估点击次数。 该值可能与广告网络提供的值不同。 |
| [!UICONTROL Estimated Cost] | Search、Social和Commerce跟踪的相关广告的总估计成本。 该值可能与广告网络提供的值不同。 |
| [!UICONTROL Estimated Impressions] | （仅限展示型营销活动）Search、Social和Commerce已跟踪的估计广告展示次数。 此值可能不同于 [!UICONTROL Impressions] 列（可用时），其中显示广告网络提供的值。 |
| [!UICONTROL Exclude (yes/no)] | 是否排除竞价(<i>[!UICONTROL Yes]</i>)或允许竞价(<i>[!UICONTROL No]</i>)表示匹配产品的广告。 |
| [!UICONTROL First Page CPC] | (仅限Google促销活动)指定日期范围内搜索结果第一页上显示的广告的每次点击成本(CPC)。 |
| `GGL*`， `GGL_CT*`、和 `GGL_XD_CT*` [[!DNL Google Ads] — 跟踪的转化/事务属性] | ([!DNL Google Ads] 搜索和购物网络上的营销活动；从为帐户启用该功能之日起可用的数据) [!DNL Google Ads]-tracked转化，每个转化最多有三个单独的事务属性：<ul><li>`GGL*`  — （跟踪时）关键字的转化值总和，以“GGL”前缀开头（例如GGL Purchase）。</li><li>`GGL_CT*`  — 转换次数（计数），以“GGL_CT”前缀（例如GGL_CT_Purchase）开头。</li><li>`GGL_XD_CT*`  — （当可用于转化类型时，当您跟踪它们时）跨设备转化次数（计数），测量依据为 [!DNL Google Ads] 以“GGL_XD_CT_”前缀(例如GGL_XD_CT_Purchase)开头。</li></ul><br>每次转化都按竞价单位和点击日期记录；在事件级别不可用。 如果您将“搜索”、“社交”和“商务”中的数据与中的数据进行比较 [!DNL Google Ads]，使用查看或报告选项查看&quot;[!UICONTROL Conversions by:  Click date]“”（不是交易日期）。<br><br><b>注意：</b>前一天的数据每天提取一次，最迟可在09提供:00-10:00（广告商所在时区）。 [!DNL Google Ads] 单击后可能会继续更新量度长达30天。 有关详情，请参阅 [!DNL Google Ads]-tracked转化，请参阅&quot;[[!DNL Google Ads] 搜索、社交和商务中的转化数据](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).” |
| [!UICONTROL Impr. (Abs. Top) %] | ([!DNL Google Ads] 仅限于)在自然搜索结果上方显示为第一个广告的广告展示次数百分比。 |
| [!UICONTROL Impr. (Top) %] | ([!DNL Google Ads] 仅显示在自然搜索结果上方的广告展示次数百分比。 |
| [!UICONTROL Impressions] | 指定日期范围内的广告展示次数。 |
| [!UICONTROL Interaction Rate] | （视频广告）交互次数除以广告显示次数（视频和缩略图展示次数）。 |
| [!UICONTROL Interactions] | （视频广告）用户观看广告的次数。 |
| [!UICONTROL Is_Click_Objectives] | ([!UICONTROL Portfolio Report]) <i>true</i> 当项目组合包含营销活动时 [!UICONTROL Maximize Clicks] 竞价策略，以及 <i>false</i> 否则。 |
| [!UICONTROL Keyword] | 关键字。<br><br><b>注意：</b> 如果报表在启用了内容的搜索营销活动中包含来自广告组的数据，则此列包含适用的广告组名称，如“（广告组内容）您的广告组名称”。 对于搜索促销活动中的网站定向投放位置，此列没有值。 |
| [!UICONTROL Keyword ID] | Search、Social和Commerce分配给关键字的数值ID。 |
| [!UICONTROL Keyword Status] | 与搜索词匹配的关键字的状态： <i>[!UICONTROL Active]</i>， <i>[!UICONTROL Paused]</i>， <i>[!UICONTROL Deleted]</i>，或 <i>[!UICONTROL Disapproved]</i>. |
| [!UICONTROL Label Classification] | ([!UICONTROL Label Classification Report] 和 [!UICONTROL Label Value Report])标签分类。 |
| [!UICONTROL Label Value] | ([!UICONTROL Label Classification Report] 和 [!UICONTROL Label Value Report])标签分类的值。 |
| [!UICONTROL Language] | （显示营销活动）目标受众语言。 |
| [!UICONTROL Link Type] | ([!UICONTROL Keyword Report]； [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 仅限促销活动；仅当为报告指定的归因规则为“最后一个事件”时，数据才可用)当行报告由于单击广告扩展（而不是广告本身）或产品/购物广告而导致的转化时，此列显示被单击的链接的类型和标题：<ul><li>`pla:*`  — 产品广告列为 `pla:<product ID>`，如“pla：8525822”。</li><li>`sl:*`  — 站点链接列为 `sl:<Sitelink text>`，如“sl：请参阅当前选件”。</li></ul> |
| [!UICONTROL Listing Match Type] | 广告列表的关键字匹配类型， <i>[!UICONTROL Content]</i> 针对内容定位促销活动中的广告，或者 <i>[!UICONTROL Sitecpc]</i> ，以获取针对站点的营销活动中的投放位置。 对象 [!DNL Microsoft Advertising] 关键字，这可以包括多种匹配类型(如&quot;[!UICONTROL Broad]，[!UICONTROL Exact]“)。 |
| [!UICONTROL Location] | （显示营销活动）目标受众位置。 |
| [!UICONTROL Long Creative Title1] - [!UICONTROL Long Creative Title5] | (在已完成的报表行中，用于 [!DNL Microsoft Advertising] 响应式广告和多媒体广告)广告的长标题。 要查看这些列，请包含&quot;[!UICONTROL Long Creative Titles]”列。 |
| [!UICONTROL Long Creative Titles] | (对于 [!DNL Microsoft Advertising] 响应式广告和多媒体广告)为每个广告的长标题添加一列(&quot;[!UICONTROL Long Creative Title1]“ — ”[!UICONTROL Long Creative Title5]“)。 |
| [!UICONTROL Market Type] | 市场类型：  <i>[!UICONTROL search]</i> 或 <i>[!UICONTROL social]</i> |
| [!UICONTROL Max Spend % Target] | (项目组合中的营销活动，具有 [!UICONTROL ROI]， [!UICONTROL CPT]，或 [!UICONTROL Marginal Cost per Transaction] 支出策略)投资组合的最大每日预算目标。 |
| [!UICONTROL Max Spend (%)] | ([!UICONTROL Network Constraint Report])为广告网络配置的投资组合支出的最大百分比。 对于使用约束类型&quot;[!UICONTROL Min-Max]，”这是 [!UICONTROL Max %] 值。 对于使用约束类型&quot;[!UICONTROL Target Spend]，”这是 [!UICONTROL Target Spend] 值。 |
| [!UICONTROL Method ID] | ([!UICONTROL Portfolio Report])  <!-- ???????? Insert value --> |
| [!UICONTROL Metro Code] | ([!UICONTROL Geo Distribution Report]， [!UICONTROL Keyword Report])从中产生展示次数或点击次数的数字城市代码（例如，Denver表示为us-751）。 根据搜索用户的IP地址确定。 |
| [!UICONTROL Min Spend (%)] | ([!UICONTROL Network Constraint Report])为广告网络配置的投资组合的最小支出百分比。 对于使用约束类型&quot;[!UICONTROL Min-Max]，”这是 [!UICONTROL Min %] 值，如果 [!UICONTROL Min %] 已配置。 对于使用约束类型&quot;[!UICONTROL Target Spend]，”这是 [!UICONTROL Target Spend] 值。 |
| [!UICONTROL Network Account ID] | 网络分配的帐户ID。 |
| [!UICONTROL Network Ad Group ID] | 网络分配的广告组ID。 |
| [!UICONTROL Network Campaign ID] | 网络分配的营销活动ID。 |
| [!UICONTROL Objective Name] | 投资组合的目标。 |
| [!UICONTROL Outbound Clicks] | ([!DNL Meta] ads)广告中使人退伍的链接的点击次数 [!DNL Meta]拥有的属性。 |
| [!UICONTROL Parent Product Groupings] | 父产品组的完整层次结构，具有 `>>` 层之间(例如 `All Products>>CategoryL1=Animals`)（如果适用）。 |
| [!UICONTROL Partition Type] | 产品组的类型： <i>[!UICONTROL Sub-Division]</i> （父产品组）或 <i>[!UICONTROL Unit]</i> （具有竞价的子产品组的最低级别）。 |
| [!UICONTROL Path Position] | ([!UICONTROL Transaction Report])事件在转化路径中的位置。 |
| [!UICONTROL Path Total] | ([!UICONTROL Transaction Report])路径位置的事件总数。 |
| [!UICONTROL Portfolio] | 项目组合。 |
| [!UICONTROL Portfolio Count] | ([!UICONTROL Portfolio Report])与目标关联的项目组合数量。 <!-- This count is different than what I see within the Objectives view. --> |
| [!UICONTROL Portfolio Group Name] | 项目组合所属的项目组合组的名称。 |
| [!UICONTROL Portfolio ID] | 数值项目组合ID。 |
| [!UICONTROL Portfolio Spend Strategy] | ([!UICONTROL Portfolio Report])投资组合的支出策略： <i>[!UICONTROL Daily]</i>， <i>[!UICONTROL Weekly]</i>， <i>[!UICONTROL Monthly]</i>， <i>[!UICONTROL ROI]</i>， <i>[!UICONTROL Day of week]</i>， <i>[!UICONTROL Day of month]</i>， <i>[!UICONTROL CPT]</i>， <i>[!UICONTROL Marginal CPT]</i>， <i>[!UICONTROL Google Target CPA]</i>，或 <i>[!UICONTROL Google Target ROAS]</i>. |
| [!UICONTROL Portfolio Status] | 项目组合状态：<ul><li><i>[!UICONTROL Optimize]：</i> 优化能力是收集相关营销活动的点击和收入数据，建模数据以优化竞价，以及优化竞价和/或营销活动预算（取决于优化类型和营销活动竞价策略）。</li><li><i>[!UICONTROL Active]：</i> 优化功能正在收集相关营销活动的点击和收入数据并对数据进行建模，但不是优化竞价或营销活动预算。</li><li><i>[!UICONTROL Inactive]：</i> 优化功能会收集相关营销活动的点击数据以便进行报告，但它不会建模数据，也不会优化竞价或营销活动预算。</li></ul> |
| [!UICONTROL Portfolio Target] | ([!UICONTROL Portfolio Report])投资组合的支出策略的每日目标。 对于每日/每月和一周/月的某一天策略，将显示当天的目标。 |
| [!UICONTROL Preferred Devices] | ([!DNL Google Ads]， [!DNL Microsoft Advertising]、和 [!DNL Yahoo! Japan Ads] campaigns)广告设置是否优先于 <i>[!UICONTROL Mobile ads]</i> 或 <i>[!UICONTROL All ads]</i>. |
| [!UICONTROL Product Group ID] | 广告网络分配给产品组的数值ID。 |
| [!UICONTROL Product Groupings] | 父产品组。 |
| [!UICONTROL Product ID] | ([!UICONTROL Keyword Report]； [!DNL Google Ads] 产品列表广告)与广告一起显示的产品的产品ID。<br><br><b>注意：</b> 仅当产品列表包含跟踪参数时，才会捕获ID `ev_plx=<GMC product ID>`，您必须将其添加在 [!DNL Google Merchant Center]. |
| [!UICONTROL Raw Transaction Data] | ([!UICONTROL Transaction Report]交易财产收入（如1个登记，12个订购12美元）。 如果多个竞价单位具有相同的交易ID，则跟踪ID的收入会根据在指定的点击日期（点击数据可用时）的点击次数进行拆分。 |
| [!UICONTROL Reach] | ([!DNL Meta] ads)查看您的广告至少一次的人数。 注意： [!DNL Meta] 每天删除重复的用户配置文件范围，因此报告的数据来自 [!DNL Meta] 而搜索、社交和商务可能有所不同。 |
| [!UICONTROL Region] | ([!UICONTROL Geo Distribution Report]， [!UICONTROL Keyword Report])展示次数或点击次数源自的区域或美国/加拿大州。 根据用户的IP地址确定。 |
| [!UICONTROL SE Creative ID] | 网络分配的广告ID。 |
| [!UICONTROL Search (Abs. Top) IS] | ([!DNL Google Ads] 和 [!DNL Microsoft Advertising])您从绝对顶部位置接收的展示次数（自然搜索结果上方的第一个广告）除以您有资格从顶部位置接收的预计展示次数。 10%以下的百分比表示为“`<10%`“或”`0.0999`.” |
| [!UICONTROL Search (Top) IS] | ([!DNL Google Ads] 和 [!DNL Microsoft Advertising])您从排名最前的位置收到的展示次数（在免费搜索结果上方）除以您有资格从排名最前的位置收到的预计展示次数。 10%以下的百分比表示为“`<10%`“或”`0.0999`.” |
| [!UICONTROL Search Engine] | 广告网络。 |
| [!UICONTROL Search exact match IS] | 您收到的与关键字完全匹配的搜索展示次数除以您有资格收到的估计完全匹配展示次数。 如果此数字较低，可能是因为您的出价太低或广告质量或相关性太低。 |
| [!UICONTROL Search impr. share] | ([!DNL Google Ads] 仅限)您收到的展示次数除以您有资格收到的预计展示次数。 10%以下的百分比表示为“&lt;10%”，90%以上的百分比表示为“`>90%`.” |
| [!UICONTROL Search lost abs. top IS (budget)] | ([!DNL Google Ads] 和 [!DNL Microsoft Advertising])由于每日或每月预算过低，您的广告不是第一个高于自然搜索结果的广告的时间百分比。 对于Google广告营销活动，超过90%的百分比表示为“`>90%`“或”`0.9001`.” |
| [!UICONTROL Search lost abs. top IS (rank)] | ([!DNL Google Ads] 和 [!DNL Microsoft Advertising])由于广告排名不佳，您的广告不是排名最前的广告，因而排名高于自然搜索结果的时间百分比。 对于Google广告营销活动，超过90%的百分比表示为“`>90%`“或”`0.9001`.” |
| [!UICONTROL Search lost IS (budget)] | ([!DNL Google Ads] （仅限）由于每日或每月预算太低而未显示广告的时间百分比。 此量度仅在营销活动级别可用。 90%以上的百分比表示为“`>90%`“或”`0.9001`.” |
| [!UICONTROL Search lost IS (rank)] | ([!DNL Google Ads] 仅因广告排名不佳而未显示广告的时间百分比。 90%以上的百分比表示为“`>90%`“或”`0.9001`.” |
| [!UICONTROL Search lost top IS (budget)] | ([!DNL Google Ads] 和 [!DNL Microsoft Advertising])由于每日或每月预算太低而未在免费搜索结果上方显示广告的时间百分比。 对象 [!DNL Google Ads] 促销活动，90%以上的百分比表示为“`>90%`“或”`0.9001`.” |
| [!UICONTROL Search lost top IS (rank)] | ([!DNL Google Ads] 和[！DNL [!DNL Microsoft Advertising]])由于广告排名不佳而使广告未显示在自然搜索结果上方的时间百分比。 对于Google广告营销活动，超过90%的百分比表示为“`>90%`“或”`0.9001`.” |
| [!UICONTROL Search Term] | ([!UICONTROL Transaction Report])用户查询的搜索词。 |
| [!UICONTROL SETrackingOnly] | 无论您是在跟踪帐户，还是在不投标： <i>[!UICONTROL TRUE]</i> 或 <i>[!UICONTROL FALSE]</i>. |
| [!UICONTROL Site] | (域反向链接报表和 [!UICONTROL Keyword Report]；面向站点的投放)产生点击的站点。 |
| [!UICONTROL Start Date] | 报告的第一天。 |
| [!UICONTROL State] | (地域分布报表， [!UICONTROL Keyword Report])交易起源的国家/地区。 根据用户的IP地址确定。 |
| [!UICONTROL Surfer ID] | ([!UICONTROL Transaction Report])完成交易的用户的ID。 |
| [!UICONTROL Through Plays] | ([!DNL Meta] 广告)观看整个广告的查看次数。 |
| [!UICONTROL Top of Page CPC] | (仅限Google促销活动)指定日期范围内搜索结果页面顶部出现的广告的每次点击成本(CPC)。 |
| [!UICONTROL Tracking URL] | （仅限以搜索为目标的关键词）跟踪模板或嵌入了（适用时）搜索、社交和商务跟踪代码的目标URL。 |
| [!UICONTROL Transaction Property Name] | ([!UICONTROL Transaction Report])交易贷记到的广告商特定交易属性。 |
| [!UICONTROL Transaction Time] | ([!UICONTROL Transaction Report])记入指定交易属性的时间。 |
| [!UICONTROL User Account Type] | 已过时 |
| [!UICONTROL User SE Account ID] | Search、Social和Commerce分配给广告网络的数值ID。 |
| [!UICONTROL Video Average Play Time] | ([!DNL Meta] ads)视频在一次展示中播放的平均时间，包括重新播放视频所花费的时间。 |
| [!UICONTROL Video Plays] | ([!DNL Meta] 广告)视频开始播放的次数（不包括重播）。 |
| [!UICONTROL VideoQuartile25Rate]， [!UICONTROL VideoQuartile50Rate]， [!UICONTROL VideoQuartile75Rate]、和 [!UICONTROL VideoQuartile100Rate] | （视频广告）播放视频的百分比，即播放完成视频的25%、50%、75%或100%。 |
| [!UICONTROL View Rate] | （视频广告）查看次数或参与次数除以广告显示次数（视频和缩略图展示次数）。 |
| [!UICONTROL Views] | （视频广告）用户观看或参与广告的次数。 |
| [!UICONTROL ViewThroughConversions] | （受众网络上的广告）由一个或多个展示次数产生，但没有点击的转化次数。 |

<table style="table-layout:auto">

<!-- HOW IS MARKET TYPE DIFFERENT FROM CHANNEL TYPE? And what are all possible values for each? -->

>[!MORELIKETHIS]
>
>* [关于基本报表和高级报表](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [生成基本或高级报告](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [基本和高级报表设置](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
