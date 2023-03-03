---
title: 跨设备解决方案
description: 了解有关跨设备功能的更多信息。
feature: DSP Introduction
exl-id: d21917ef-5cac-46f8-8222-099667797683
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# 跨设备解决方案

Advertising DSP与集成 [!DNL LiveRamp] 允许您将受众扩展到用户的所有已知设备，而不仅仅是品牌跟踪的设备。 该集成还跨所有设备提供频率上限和归因测量。

当您使用受支持的基于人员的设备图时，您可以：

* 跨渠道和设备匹配受众以将广告投放给用户和家庭，而不是设备。
* 通过了解和限制个人之间的频率来平衡和接触风险。
* 测试跨渠道或设备公开与转化受众的策略。

## 的好处 [!DNL LiveRamp] 设备图

* 提供确定性数据池，包括离线客户数据

* 在Cookie ID和移动设备ID之间提供均匀覆盖

* 包括主要来自美国的数据

* 免费用于频率限定和归因测量

* 扩展展示的定价为$0.35 CPM(仅通过使用 [!DNL LiveRamp] 设备图，而不是在目标受众区段内找到的设备上)

   费率会反映在您的帐户费率卡上。

## 基于人员的频率管理

通过基于人员的频率管理，您可以在人员级别（而不是设备级别）指定频率上限，以控制真正的媒体曝光。

### 激活基于人员的频率管理

* **促销活动：** 创建新营销活动时，您可以指定 [!UICONTROL Cross-Device Level] 设置。 启用&#39;&#39;[!UICONTROL Same Device]“ -> ”[!UICONTROL People]、”并选择设备图。 指定的设备图既可用于投放级别上的跨设备定位，也可用于营销活动、包和投放级别基于人员的频率管理。 频度上限适用于个人的所有已知设备。

有关更多信息，请参阅 [Campaign设置](/help/dsp/campaign-management/campaigns/campaign-settings.md).

保存营销活动后，便无法更改其 [!UICONTROL Cross Device Level] 设置。

* **包：**  您可以选择在包级别设置其他频率限制。 DSP将遵循营销活动层次结构中最严格的频率限制。

* **投放位置：** 您可以选择在版面级别设置其他频率限制。 DSP将遵循营销活动层次结构中最严格的频率限制。

## 基于人员的定位

通过基于人员的定位，您可以在桌面和移动设备中查找客户。

### 激活基于人员的定位

* **促销活动：** 创建新营销活动时，您可以指定 [!UICONTROL Cross-Device Level] 设置。 启用&#39;&#39;[!UICONTROL Same Device]“ -> ”[!UICONTROL People]、”并选择设备图。 指定的设备图既可用于投放级别的跨设备定位，也可用于基于人员的频率管理。

有关更多信息，请参阅 [Campaign设置](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **投放位置：** 当您在具有指定设备图的营销活动中为投放选择受众目标时， [!UICONTROL Cross-Device Targeting] 选项允许您将定位扩展至人员的所有已知设备（根据campaign设置中指定的设备图），甚至扩展未在指定区段中的设备。

### 为基于人员的定位设置报表

您可以在自定义报表中包含以下量度：

* **扩展展示：** (在 [!UICONTROL Build Your Report] 部分在 [!UICONTROL Metrics] > [!UICONTROL Std. Metrics])利用设备图提供的增量展示量（在原始受众区段中找不到）。 此量度还用于计算与使用第三方设备图相关的适用费用。

   要确定某个时间段内展示次数的成本，请运行包含 [!UICONTROL Extended Impressions] 列，然后将总展示次数乘以$0.00035（$0.35/1000展示次数）。

   总成本亦计入综合成本及累计开支。 [!UICONTROL Billable Other Net Spend] 列（在下） [!UICONTROL Metrics] > [!UICONTROL Spend])，不过该量度还包括您可能已添加的其他促销活动费用。

* **设备图：** (在 [!UICONTROL Build Your Report] 部分在 [!UICONTROL Dimensions] > [!UICONTROL Campaign])特定营销活动、包或投放位置的选定设备图。

## 基于人员的归因测量

*仅具有Adobe广告转化跟踪的广告商*

使用基于人员的归因，您可以归因发生媒体曝光的设备以外的设备上发生的转化。 基于人员的归因测量可在DSP中使用， [!DNL Adobe Advertising Creative]、和 [!DNL Adobe Advertising Search] 适用于在其网站上实施Adobe广告转化像素的广告商。

### 启用基于人员的归因测量

如果要激活跨设备归因测量，请联系您的Adobe客户团队。

### 设置跨设备转化归因的转化报表

#### 转化报表设置

为归因测量启用设备图后， [!UICONTROL Conversion] 报告包括 [!UICONTROL Cross-Device Breakout] 设置，允许您为每个转化量度最多包含三个单独的列，包括：

* &lt;*转化*>[!UICONTROL (tp)]：包括总转化次数（总人员数），其中包括同设备转化次数和跨设备转化次数（如果适用）。 在报告中， ”[!UICONTROL (tp)]&quot;会附加到转化路径中的转化量度名称、规则类型和转化类型(例如，&quot;Responses(le)(tl)(tp))。

* &lt;*转化*>[!UICONTROL (sd)]：（可选）仅包含转化路径中只跟踪单个设备的转化。 在报告中， ”[!UICONTROL (sd)]&quot;会附加到转化路径中的转化量度名称、规则类型和转化类型(例如，&quot;Responses(le)(tl)(sd))。

* &lt;*转化*>[!UICONTROL (xd)]：（可选）仅包含在转化路径中跟踪了多个设备的转化。 在报告中， ”[!UICONTROL (xd)]&quot;会附加到转化路径中的转化量度名称、规则类型和转化类型(例如，&quot;Responses(le)(tl)(xd))。

#### 如何解释转化报表

如果您对跨设备总转化百分比进行排序([!UICONTROL (xd)]/[!UICONTROL (tl)])从高到低，您会了解是什么在推动跨设备转化率高于平均水平。 您可以利用这一点来指导创意或定位策略以匹配报文传送并引导投资与用户行为。

* 包 — 查看哪些包促进的总转化率最高，以及哪些包的跨设备转化率较高。 这可以帮助您了解在哪里集中支出。

* 投放位置 — 比较投放位置性能和归因（例如，移动Web广告可能会促进桌面设备上的转化）。 如果没有用于归因的设备图，您可能会错过移动Web投放对桌面转换的影响，或者，如果大多数用户在桌面而不是移动Web上转换，则可能会淹没移动Web投放。

* 广告 — 了解哪些广告可带来更高的转化率，并量化其价值以及跨Web浏览器和移动应用程序环境的影响。

* 站点 — 跨站点优化，而不是手动完全排除站点。 如果网站推动跨设备转换，那么您可以查看在哪些设备上发生此行为。

* 交易 — 通过验证哪些库存交易实现了跨设备转化，然后决定是否应扩大定位范围以在这些交易中包含更多设备和渠道，从而改进手动优化。

>[!MORELIKETHIS]
>
>* [报表设置](/help/dsp/reports/report-settings.md)
>* [Campaign设置](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
>* [置入设置](/help/dsp/campaign-management/placements/placement-settings.md)

