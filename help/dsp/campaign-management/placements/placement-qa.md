---
title: 使用电子表格查看和编辑版面设置
description: 了解如何使用电子表格查看和编辑关键位置设置。
feature: DSP Placements
exl-id: 2de4407d-eb3b-44ff-893c-9fdf6921d4b3
source-git-commit: 230a169611aa3094365a877476f2e5e1c6b3cb9b
workflow-type: tm+mt
source-wordcount: '1433'
ht-degree: 0%

---

# 使用电子表格查看和编辑版面设置

您可以以XLSX （[!DNL Microsoft Excel]电子表格）格式下载一个或多个投放位置或营销活动中所有投放位置的设置以供审阅。 使用此功能可快速查看以下详细信息：

* 营销活动定位哪些受众。
* 投放位置开始投放的时间，以及停止的时间。
* 哪些广告附加到了投放位置。

然后，您可以进行更改以选择字段，并将它们一次上载回DSP。 可编辑的字段包括投放位置名称、状态、竞价、预算、步调策略和频度上限。

>[!TIP]
>
>要编辑一个或多个版面的多个字段，请参阅“[编辑版面](/help/dsp/campaign-management/placements/placement-edit.md)”。

## 营销活动中所有版面的下载设置

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 执行以下任一操作：

   * 在营销活动名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download Excel QA sheet]**。

   * 单击促销活动名称可查看促销活动详细信息。 单击右上角的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download Excel QA sheet]**。

   通知消息指示文件何时可供下载。

1. 执行以下任一操作：

   * 在通知消息中，单击&#x200B;**[!UICONTROL Download].**

   * 单击顶部菜单栏右侧的![作业](/help/dsp/assets/downloads.png)。 单击作业旁边的&#x200B;**[!UICONTROL Download]**。

   该文件将保存到浏览器的“下载”文件夹中。 有关包含的列的列表，请参阅[已下载/上传电子表格中的版面列](#qa-sheet-columns)。

## 一个或多个投放位置的下载设置

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 单击营销活动的名称。

1. 在子菜单中，单击&#x200B;**[!UICONTROL Placements]**。

1. 选中要下载其设置的每个版面旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download Edit in Excel Sheet]**。

该文件将自动保存到浏览器的“下载”文件夹中。 有关包含的列的列表，请参阅[已下载/上传电子表格中的版面列](#qa-sheet-columns)。

## 上传营销活动中所有版面的设置

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 执行以下任一操作：

   * 在营销活动名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Upload Excel QA sheet]**。

   * 单击促销活动名称可查看促销活动详细信息。 单击右上角的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Upload Excel QA sheet]**。

1. 在[!UICONTROL Edit in Excel]对话框中：

   1. 将文件拖放到框中，或者单击框内部以从设备或网络中选择文件。

   1. 单击&#x200B;**[!UICONTROL Upload]**。

1. （可选）要验证是否已处理更新，请单击顶部菜单栏右侧的![作业](/help/dsp/assets/downloads.png)。

## 一个或多个投放位置的上载设置

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 单击营销活动的名称。

1. 在子菜单中，单击&#x200B;**[!UICONTROL Placements]**。

1. 选中要上载其设置的每个版面旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Upload Edit in Excel Sheet]**。

1. 在[!UICONTROL Edit in Excel]对话框中：

   1. 将文件拖放到框中，或者单击框内部以从设备或网络中选择文件。

   1. 单击&#x200B;**[!UICONTROL Upload]**。

1. （可选）要验证是否已处理更新，请单击顶部菜单栏右侧的![作业](/help/dsp/assets/downloads.png)。

## 放置设置已下载/已上传电子表格中的列{#qa-sheet-columns}

>[!TIP]
>
> 在下载的电子表格中，所有可编辑的列都以蓝色突出显示。

### 营销活动级别的电子表格

| 部分 | 列 | 描述 | 可编辑？ |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | 投放位置的数值ID。 | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | 投放位置的名称。 | 是 |
| [!UICONTROL Basic] | [!UICONTROL Labels] | 任何应用的标签，用于报告。 | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | 在“编辑”模式下打开投放位置的链接。 | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | 位置状态： *[!UICONTROL active]*&#x200B;或&#x200B;*[!UICONTROL inactive]*。 | 是 |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | 投放类型。 | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | 父包的名称（如果适用）。 | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | 投放的开始日期。 | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | 投放的结束日期。 | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | 分时段是&#x200B;*[!UICONTROL ON]*&#x200B;还是&#x200B;*[!UICONTROL OFF]*。<br><b>注意：</b>若要检查实际的播出时间表，请在DSP中打开版面设置。 | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | 职位安排预算（如果有）。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | 预算间隔： &lt;i[!UICONTROL >Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*&#x200B;或&#x200B;*[!UICONTROL All Time]*。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | 程序包的目标。 | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | 目标的目标值。 | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | 投放位置是面向&#x200B;*[!UICONTROL Budget]*&#x200B;还是&#x200B;*[!UICONTROL Impressions]*。 | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | 投放位置的最高出价。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | 投放位置的外部测试版步调策略： *[!UICONTROL Even]*、*[!UICONTROL slightly ahead]*、*[!UICONTROL frontload]*&#x200B;或&#x200B;*[!UICONTROL aggressive frontload]*。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | 投放的当天步调策略： *[!UICONTROL Even]*&#x200B;或&#x200B;*[!UICONTROL ASAP]*。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | 要应用的任何预竞价筛选条件。 | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | 竞价规则（已弃用）是&#x200B;*[!UICONTROL ON]*&#x200B;还是&#x200B;*[!UICONTROL OFF]*。 | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | 在指定[!UICONTROL Frequency Cap Interval]期间的投放位置的主频率上限。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | 主频率上限的间隔： *[!UICONTROL Day]*、*[!UICONTROL Week]*&#x200B;或&#x200B;*[!UICONTROL Month]*。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | 在指定[!UICONTROL Secondary Frequency Cap Interval]期间投放的次频率上限 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | 辅助频率上限的间隔类型： *[!UICONTROL Week]*、*[!UICONTROL Day]*、*[!UICONTROL Hour]*&#x200B;或&#x200B;*[!UICONTROL Minute]*。 [!UICONTROL Secondary Frequency Cap Interval Value]指明了适用的周数、天数、小时数或分钟数。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | [!UICONTROL Secondary Frequency Cap]适用的周数、天数、小时数或分钟数。 例如，如果次要展示次数上限是每六小时三次展示，则此处的值将为`6`。 | 是 |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | 目标地理位置&#x200B;*[!UICONTROL All]*&#x200B;或&#x200B;*[!UICONTROL None]*&#x200B;的数量。 | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | 目标地理位置，用分号或&#x200B;*[!UICONTROL All Locations]*&#x200B;分隔。 | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | 排除的地理位置数或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | 排除的地理位置，用分号或&#x200B;*[!UICONTROL None]*&#x200B;分隔。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | 已指定目标公共库存交易数（*[!UICONTROL All]*&#x200B;或&#x200B;*[!UICONTROL None]*）。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | 已指定排除的公共库存交易的数量（如果有），或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | 已指定目标专用清单交易的数量（*[!UICONTROL All]*&#x200B;或&#x200B;*[!UICONTROL None]*）。 | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | 已指定排除的私有库存交易数（如果有），或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | 已指定的目标[!UICONTROL On-Demand Inventory]交易的数量（*[!UICONTROL All]*&#x200B;或&#x200B;*[!UICONTROL None]*）。 | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | 排除的按需清单交易数（如果指定了任何交易）或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | 流量的目标类型： *[!UICONTROL Website]*&#x200B;和/或&#x200B;*[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | 用于排除出流流量的清单定位选项是&lt;i[!UICONTROL >ON]*还是&#x200B;*[!UICONTROL OFF]*。<br>流输出广告通常以弹出窗口的形式出现在内容上，或者填充到内容中（在本机体验中），而不是在视频播放器中作为常规视频广告。 | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | 要定位的网站的质量： *[!UICONTROL Tier 1]*、*[!UICONTROL Tier 2]*、*[!UICONTROL Tier 3]*&#x200B;或&#x200B;*[!UICONTROL All Sites]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | 目标网站类别数（如果指定了任何类别），或&#x200B;*[!UICONTROL All]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | 已指定排除的站点类别（如果有）的数量，或&#x200B;*[!UICONTROL All]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | 已指定排除的站点（如果有）或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | 目标站点语言。 | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | （仅限标准显示投放位置）是否允许在未经审核的站点上投放广告： *[!UICONTROL ON]*&#x200B;或&#x200B;*[!UICONTROL OFF]*。 当投放以私人库存为目标时，此选项可能会在阻止的网站上投放广告。 | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | 已指定目标站点的数量（如果有），或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | 已指定目标受众（如果有）或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | 已指定排除的受众（如果有）或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | 是否为投放位置（以及营销活动中的其他投放位置）启用了[!DNL Comscore]人口统计区段：*[!UICONTROL ON]*&#x200B;或&#x200B;*[!UICONTROL OFF]*。 只能为[!DNL Nielsen]和/或[!DNL Comscore]启用了[!DNL Audience Verification]功能的营销活动启用此功能。  它会产生额外费用。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | 是否跨设备扩展广告定位： *[!UICONTROL ON]*&#x200B;或&#x200B;*[!UICONTROL OFF]*。 跨设备定位可根据营销活动设置中指定的设备图，将您的定位扩展到用户的所有已知设备。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] — 已包括# | 指定的目标主题代码数（如果有），或&#x200B;*[!UICONTROL All]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | 已指定排除的主题代码数（如果有）或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | 已指定的目标设备目标数（如果有），或&#x200B;*[!UICONTROL All]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | 排除的设备目标数（如果已指定），或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | 已指定目标ISP提供商的数量（如果有）或*[!UICONTROL All]/i>。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | 已指定排除的ISP提供商的数量（如果有），或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | 已应用的品牌安全筛选器的数量（如果有的话），或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | 应用了预竞价欺诈阻止过滤器的数量（如果指定），或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | 应用的预竞价可视性筛选器的数量（如果指定了任何筛选器）或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | 是否启用了站点安全块： *[!UICONTROL ON]*&#x200B;或&#x200B;*[!UICONTROL OFF]*。<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | 附加到投放位置的第三方事件跟踪像素数，或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | 附加到投放位置的转化跟踪像素数，或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | 作为每1000次展示的不可记帐成本跟踪的静态第三方费率（如果适用）。 | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | 附加到投放位置的广告数（如果有），或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | 附加到投放位置的任何广告的名称，或&#x200B;*[!UICONTROL None]*。 | — |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | 附加到投放位置的任何广告的DSP生成的唯一Ad ID，用分号分隔。 要从[!UICONTROL Ads]视图下载广告名称和关联的广告ID列表，请创建包含[!UICONTROL Ad ID]量度的自定义视图，然后[导出数据](/help/dsp/campaign-management/reports/campaign-export-data.md)。 | 是 |

### 置入级别电子表格

| 列 | 描述 | 可编辑？ |
|--------|-------------|-----------|
| [!UICONTROL Placement ID] | 投放位置的数值ID。 | — |
| [!UICONTROL Placement Name] | 投放位置的名称。 | 是 |
| [!UICONTROL Package Name] | 父包的名称（如果适用）。 | — |
| [!UICONTROL Start Date] | 投放的开始日期。 | — |
| [!UICONTROL End Date] | 投放的结束日期。 | — |
| [!UICONTROL Status] | 位置状态： *[!UICONTROL active]*&#x200B;或&#x200B;*[!UICONTROL inactive]*。 | — |
| [!UICONTROL Max Bid] | 投放位置的最高出价。 | 是 |
| [!UICONTROL Budget] | 职位安排预算（如果有）。 | 是 |
| [!UICONTROL Budget Interval] | 预算间隔： &lt;i[!UICONTROL >Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*&#x200B;或&#x200B;*[!UICONTROL All Time]*。 | 是 |
| [!UICONTROL Primary Frequency Cap] | 在指定[!UICONTROL Primary Frequency Cap Interval]期间的投放位置的主频率上限。 | 是 |
| [!UICONTROL Primary Frequency Cap Interval] | 主频率上限的间隔： *[!UICONTROL Day]*、*[!UICONTROL Week]*&#x200B;或&#x200B;*[!UICONTROL Month]*。 | 是 |
| [!UICONTROL Secondary Frequency Cap] | 在指定[!UICONTROL Secondary Frequency Cap Interval]期间投放的次频率上限 | 是 |
| [!UICONTROL Secondary Frequency Cap Interval] | 辅助频率上限的间隔类型： *[!UICONTROL Week]*、*[!UICONTROL Day]*、*[!UICONTROL Hour]*&#x200B;或&#x200B;*[!UICONTROL Minute]*。 [!UICONTROL Secondary Frequency Cap Interval Value]指明了适用的周数、天数、小时数或分钟数。 | 是 |
| [!UICONTROL Secondary Frequency Cap Interval Value] | [!UICONTROL Secondary Frequency Cap]适用的周数、天数、小时数或分钟数。 例如，如果次要展示次数上限是每六小时三次展示，则此处的值将为`6`。 | 是 |
| [!UICONTROL Attached Ad ID] | 附加到投放位置的任何广告的DSP生成的唯一Ad ID，用分号分隔。 要从[!UICONTROL Ads]视图下载广告名称和关联的广告ID列表，请创建包含[!UICONTROL Ad ID]量度的自定义视图，然后[导出数据](/help/dsp/campaign-management/reports/campaign-export-data.md)。 | 是 |

>[!MORELIKETHIS]
>
>* [编辑版面](/help/dsp/campaign-management/placements/placement-edit.md)
>* [位置设置](/help/dsp/campaign-management/placements/placement-settings.md)
