---
title: 使用电子表格查看和编辑包设置
description: 了解如何使用电子表格查看和编辑关键包设置。
feature: DSP Packages
source-git-commit: 230a169611aa3094365a877476f2e5e1c6b3cb9b
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 0%

---

# 使用电子表格查看和编辑包设置

您可以以XLSX （[!DNL Microsoft Excel]电子表格）格式下载一个或多个包的设置以供审阅。 电子表格包括一个单独的选项卡，其中包含航班信息。 然后，您可以进行更改以选择两个选项卡中的字段，并一次性将数据上载回DSP。 可编辑字段包含大多数通常可编辑的设置。

>[!TIP]
>
>要编辑一个或多个包的多个字段，请参阅“[编辑包](/help/dsp/campaign-management/packages/package-edit.md)”。

## 一个或多个包的下载设置

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 单击营销活动的名称。

1. 在子菜单中，单击&#x200B;**[!UICONTROL Packages]**。

1. 选中要下载其设置的每个包旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download Edit in Excel Sheet]**。

该文件将自动保存到浏览器的“下载”文件夹中。 有关包含的列的列表，请参阅已下载/已上传电子表格](#qa-sheet-columns-packages)中的[包列。

## 一个或多个包的上载设置

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 单击营销活动的名称。

1. 在子菜单中，单击&#x200B;**[!UICONTROL Packages]**。

1. 选中要上载其设置的每个包旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Upload Edit in Excel Sheet]**。

1. 在[!UICONTROL Edit in Excel]对话框中：

   1. 将文件拖放到框中，或者单击框内部以从设备或网络中选择文件。

   1. 单击&#x200B;**[!UICONTROL Upload]**。

1. （可选）要验证是否已处理更新，请单击顶部菜单栏右侧的![作业](/help/dsp/assets/downloads.png)。

## 包设置已下载/已上传电子表格中的列{#qa-sheet-columns-packages}

>[!TIP]
>
> 在下载的电子表格中，所有可编辑的列都以蓝色突出显示。

### [!UICONTROL Package]选项卡

| 部分 | 列 | 描述 | 可编辑？ |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | 程序包的数值ID。 | — |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | 程序包的名称。 | 是 |
| [!UICONTROL Basic details] | [!UICONTROL Status] | 程序包状态： *[!UICONTROL active]*&#x200B;或&#x200B;*[!UICONTROL inactive]*。 | 是 |
| [!UICONTROL Basic details] | [!UICONTROL Description] | 程序包的可选说明。 | 是 |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | 作为每1000次展示的不可记帐成本跟踪的静态第三方费率（如果适用）。 | 是 |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | 第三方费率的可选描述（如果适用）。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | 包的开始日期。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | 包的结束日期。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | 在包中占位和限制投放位置的级别： *[!UICONTROL Package]*&#x200B;或&#x200B;*[!UICONTROL Placement]*。 | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | 包预算。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | 预算间隔： &lt;i[!UICONTROL >Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*&#x200B;或&#x200B;*[!UICONTROL All Time]*。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | 可选预算间隔上限。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | 可选预算间隔上限的间隔： &lt;i[!UICONTROL >Daily]*、*[!UICONTROL Weekly]*、*[!UICONTROL Monthly]*&#x200B;或&#x200B;*[!UICONTROL All Time]*。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | 程序包的目标。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | 目标的目标值。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | （仅限具有“[!UICONTROL Highest Return on Ad Spend]”和“[!UICONTROL Lowest Cost per Acquisition]”优化目标的包）包含用于计算CPA或ROAS量度的收入或转化事件的[自定义目标](/help/dsp/optimization/custom-goal.md)。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | （可选；仅具有“[!UICONTROL Highest Return on Ad Spend]”和“[!UICONTROL Lowest Cost per Acquisition]”优化目标的包）要用于计算广告支出回报率或每次收购成本的最终转化事件或收入事件/销售金额。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | （仅限具有自定义优化目标的包）包的用途，有助于确定如何优化包： *[!UICONTROL Prospecting]*、*[!UICONTROL Retargeting]*&#x200B;或&#x200B;*[!UICONTROL Other]*。 | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | （仅限具有自定义优化目标的包）另一个包的包ID，其历史数据用作优化包的输入。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | （仅限具有自定义优化目标的包）另一个包，其历史数据用作优化包的输入。 | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | 程序包是走向&#x200B;*[!UICONTROL budget]*&#x200B;还是&#x200B;*[!UICONTROL primary_goal]*（用于展示次数）。 | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | （当按展示次数排列包时）指定时间间隔内的目标展示次数。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | （当您按展示次数排列程序包时）目标展示次数的时间间隔。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | 包的外部测试版步调策略： *[!UICONTROL Even]*、*[!UICONTROL slightly ahead]*、*[!UICONTROL frontload]*&#x200B;或&#x200B;*[!UICONTROL aggressive frontload]*。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | 包的当天步调策略： *[!UICONTROL Even]*&#x200B;或&#x200B;*[!UICONTROL ASAP]*。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | 在指定的[!UICONTROL Frequency Cap Interval]期间包的主频率上限。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | 主频率上限的间隔： *[!UICONTROL Day]*、*[!UICONTROL Week]*&#x200B;或&#x200B;*[!UICONTROL Month]*。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | 主[!UICONTROL Frequency Cap]适用的周数、天数、小时数或分钟数。 例如，如果主上限为每月12次展示，则此处值将为`12`。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | 在指定的[!UICONTROL Secondary Frequency Cap Interval]期间包的次频率上限 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | 辅助频率上限的间隔类型： *[!UICONTROL Week]*、*[!UICONTROL Day]*、*[!UICONTROL Hour]*&#x200B;或&#x200B;*[!UICONTROL Minute]*。 [!UICONTROL Secondary Frequency Cap Interval Value]指明了适用的周数、天数、小时数或分钟数。 | 是 |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | [!UICONTROL Secondary Frequency Cap]适用的周数、天数、小时数或分钟数。 例如，如果次要展示次数上限是每六小时三次展示，则此处的值将为`6`。 | 是 |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | 是否为包&#x200B;*T* (true)或&#x200B;*F* (false)创建非偶数步调航班。 启用自定义灯光并保存包后，您既无法禁用自定义灯光，也无法编辑包的开始日期。 | — |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | （仅在启用[!UICONTROL Activate Custom Flighting]选项时可用）是否自动将上一个航班的任何剩余预算添加到下一个航班的现有预算中： *T* (true)或&#x200B;*F* (false)。 | 是 |
| [!UICONTROL Error] | [!UICONTROL Error] | 任何相关错误。 | — |

### [!UICONTROL Package_Flights]选项卡

| 部分 | 列 | 描述 | 可编辑？ |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | 程序包的数值ID。 | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | 航班的数值ID。 | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] | 航班的第一个日期。 | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | 飞行的最终日期。 | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | 航班的目标支出目标。 | — |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | （未启用“[!UICONTROL Automatically rollover remaining flight budget to next flight]”选项的现有包）要添加到下一个航班的潜在未用预算金额。 | — |

>[!MORELIKETHIS]
>
>* [编辑包](/help/dsp/campaign-management/packages/package-edit.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
