---
title: Cross-Device Solutions
description: 了解有关跨设备功能的更多信息。
feature: DSP Introduction
exl-id: d21917ef-5cac-46f8-8222-099667797683
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# Cross-Device Solutions

Advertising DSP与[!DNL LiveRamp]的集成允许您将受众扩展到用户的所有已知设备，而不仅仅是您的品牌所跟踪的设备。 该集成还提供了跨所有设备的频率封顶和归因测量。

当您使用受支持的基于人员的设备图时，您可以：

* 跨渠道和设备匹配受众以将广告投放给人员和家庭，而不是设备。
* 通过了解并限制跨个人的频率来平衡广告曝光。
* 跨渠道或设备公开与转化受众的测试策略。

## [!DNL LiveRamp]设备图的优点

* 提供确定性数据池，包括离线客户数据

* 在Cookie ID和移动设备ID之间提供均匀覆盖

* 包括主要来自美国的数据

* 免费用于频率封顶和归因测量

* 扩展展示次数（仅使用[!DNL LiveRamp]设备图提供的展示次数，而不是在目标受众区段内找到的设备上提供的展示次数）的定价为$0.35 CPM

  费率会反映在您的帐户费率卡上。

## 基于人员的频率管理

基于人员的频率管理允许您在人员级别（而不是设备级别）指定频率上限，以实现真正的媒体曝光控制。

### 激活基于人员的频率管理

* **营销活动：**&#x200B;创建新营销活动时，您可以指定[!UICONTROL Cross-Device Level]设置。 启用“[!UICONTROL Same Device]” — >“[!UICONTROL People]”并选择设备图。 指定的设备图既可用于投放级别上的跨设备定位，也可用于营销活动、包和投放级别基于人员的频率管理。 频度上限适用于用户的所有已知设备。

有关详细信息，请参阅[促销活动设置](/help/dsp/campaign-management/campaigns/campaign-settings.md)。

保存营销活动后，便无法更改其[!UICONTROL Cross Device Level]设置。

* **包：**&#x200B;您可以选择在包级别设置其他频率上限。 DSP遵循营销活动层次结构中最严格的频率限制。

* **投放位置：**&#x200B;您可以选择在投放位置级别设置其他频率上限。 DSP遵循营销活动层次结构中最严格的频率限制。

## 基于人员的定位

通过基于人员的定位，您可以在桌面和移动设备中查找客户。

### 激活基于人员的定位

* **营销活动：**&#x200B;创建新营销活动时，您可以指定[!UICONTROL Cross-Device Level]设置。 启用“[!UICONTROL Same Device]” — >“[!UICONTROL People]”并选择设备图。 指定的设备图既可用于投放级别上的跨设备定位，也可用于基于人员的频率管理。

有关详细信息，请参阅[促销活动设置](/help/dsp/campaign-management/campaigns/campaign-settings.md)。

* **投放位置：**&#x200B;当您在具有指定设备图的促销活动中为投放位置选择受众目标时，[!UICONTROL Cross-Device Targeting]选项允许您跨人员的所有已知设备（根据促销活动设置中指定的设备图）扩展您的定位，甚至可以跨指定区段之外的设备扩展。

### 为基于人员的定位设置报表

您可以在自定义报表中包含以下量度：

* **扩展展示次数：** （在[!UICONTROL Metrics] > [!UICONTROL Std. Metrics]下的[!UICONTROL Build Your Report]部分中）利用设备图交付的增量展示次数（在原始受众区段中找不到）。 此量度还用于计算与使用第三方设备图相关的适用费用。

  要确定某个时间段内扩展展示的成本，请运行包含[!UICONTROL Extended Impressions]列的自定义报表，然后将扩展展示总数乘以$0.00035（$0.35/1000展示次数）。

  汇总成本也包含在[!UICONTROL Billable Other Net Spend]列（[!UICONTROL Metrics] > [!UICONTROL Spend]下）中，但该量度还包括您可能已添加的其他促销活动费用。

* **设备图：** （在[!UICONTROL Dimensions] > [!UICONTROL Campaign]下的[!UICONTROL Build Your Report]部分中）为特定营销活动、包或投放位置选择的设备图。

## 基于人员的归因测量

*仅跟踪Adobe Advertising转化情况的广告商*

使用基于人员的归因，您可以归因发生媒体曝光的设备之外的其他设备上发生的转化。 基于人员的归因测量在DSP、[!DNL Adobe Advertising Creative]和[!DNL Adobe Advertising Search, Social, & Commerce]中可用，适用于在其网站上实施Adobe Advertising转化像素的广告商。

### 启用基于人员的归因测量

如果要激活跨设备归因测量，请联系您的Adobe客户团队。

### 设置跨设备转化归因的转化报表

#### 转化报表设置

为归因测量启用设备图后，[!UICONTROL Conversion]报表将包含[!UICONTROL Cross-Device Breakout]设置，这样您最多可以为每个转化量度包含三个单独的列，包括：

* &lt;*转化*>[!UICONTROL (tp)]：包含总转化（总人数），其中包括同一设备转化和跨设备转化（如果适用）。 在报表中，“[!UICONTROL (tp)]”会附加到转化路径中的转化量度名称、规则类型和转化类型(例如，“Responses(le)(tl)(tp)”)。

* &lt;*转化*>[!UICONTROL (sd)]： （可选）仅包含在转化路径中只跟踪单个设备的转化。 在报表中，“[!UICONTROL (sd)]”会附加到转化路径中的转化量度名称、规则类型和转化类型(例如，“Responses(le)(tl)(sd)”)。

* &lt;*转化*>[!UICONTROL (xd)]： （可选）只包含在转化路径中跟踪了多个设备的转化。 在报表中，“[!UICONTROL (xd)]”会附加到转化路径中的转化量度名称、规则类型和转化类型(例如，“Responses(le)(tl)(xd)”)。

#### 如何解读转化报表

对跨设备([!UICONTROL (xd)]/[!UICONTROL (tl)])的总转化百分比从高到低进行排序，以了解是什么在推动高于平均值的跨设备转化。 您可以利用这一点为创意或定位策略提供信息，以便匹配报文传送并将投资与用户行为导向。

* 包 — 查看哪些包产生的总转化率最高，哪些包的跨设备转化率较高。 这有助于您了解在哪里集中支出。

* 投放位置 — 比较投放位置性能和归因（例如，移动Web广告可能会促进桌面设备上的转化）。 如果没有用于归因的设备图，您可能会错过移动Web投放对桌面转换的影响，或者，如果大多数用户在桌面而不是移动Web上转换，则这些影响可能会被掩盖。

* 广告 — 发现哪些广告可带来更高的转化率，并量化其价值以及在Web浏览器和移动应用程序环境中产生的影响。

* 站点 — 跨站点优化，而不是完全手动排除站点。 如果网站推动跨设备转换，那么您可以查看在哪些设备上发生此行为。

* 交易 — 通过验证哪些库存交易实现了跨设备转化，然后决定是否应扩大您的定位范围以在这些交易中包含更多设备和渠道，从而改进手动优化。

>[!MORELIKETHIS]
>
>* [报告设置](/help/dsp/reports/report-settings.md)
>* [营销活动设置](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
>* [位置设置](/help/dsp/campaign-management/placements/placement-settings.md)
