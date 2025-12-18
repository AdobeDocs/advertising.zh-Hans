---
title: 查看警报
description: 了解如何查看营销活动和营销活动组件的警报和建议解决方案。
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
exl-id: 667bf1c3-3bad-4a1a-b907-0c9bfe5362a9
source-git-commit: 9ab8d3345659f48d1d131c3c6c1e1b87f0b0a0e6
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# 查看警报

DSP可帮助您识别任何促销活动或促销活动组件何时出现问题。 对于每个问题，DSP都会创建一个带有时间戳的警报，以及解决此问题的建议操作。 警报的原因包括配置问题（例如，当投放位置没有附加广告或交易设置错误时）、广告拒绝和活动运行状况问题（例如广告投放或性能不佳）。 警报在营销活动、包、投放位置、广告和交易级别可用。

警报在以下位置提供：

* [!UICONTROL Pulse Panel]、[!UICONTROL Campaigns]和包详细信息、[!UICONTROL Packages]和[!UICONTROL Placements]视图中的[!UICONTROL Ads]图标指示该视图中的项目是否有任何警报可用。 当图标具有蓝色圆点（![警报可用时的Pulse面板图标](/help/dsp/assets/alerts-panel.png "警报可用时的Pulse面板图标")）时，警报可用。 当没有点可见(![无可用警报时的Pulse Panel图标](/help/dsp/assets/alerts-panel-empty.png "无可用警报时的Pulse Panel图标"))时，没有可用警报。

* 相同视图中的数据表包含一列“[!UICONTROL Alerts]”，该列指示项（或其组件）何时出现问题。 警报指示器包括“严重”（![严重](/help/dsp/assets/indicator-critical.png "严重")）、“警告”(![警告](/help/dsp/assets/indicator-warning.png "警告"))和“信息”（![信息](/help/dsp/assets/indicator-information.png "信息")）。

您可以打开任何警报的相关促销活动管理视图，以便根据需要编辑设置来解决问题。

您还可以选择忽略单个警报，这样会将其从[!UICONTROL Pulse]面板中删除。

当基础问题得到解决时，警报和警报指示器会自动消失。

## 在[!UICONTROL Pulse Panel]中查看警报

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 执行以下任一操作：

   * （适用于视图的所有警报）在任何营销活动管理视图的工具栏右侧，单击警报可用时的![Pulse面板图标](/help/dsp/assets/alerts-panel.png "警报可用时的Pulse面板图标")。

   * （对于特定营销活动的所有警报）单击营销活动行的警报指示器，然后单击&#x200B;**[!UICONTROL View in Pulse panel]**。

   * （针对特定包、投放位置或广告的所有警报）执行以下操作：

      1. 单击营销活动名称。

      1. 在子菜单中，单击&#x200B;**[!UICONTROL Packages]**、**[!UICONTROL Placements]**&#x200B;或&#x200B;**[!UICONTROL Ads]**&#x200B;以打开相关的营销活动组件视图。

      1. 单击程序包、投放位置或广告行的警报指示器，然后单击&#x200B;**[!UICONTROL View in Pulse Panel]**。

   列出与促销活动及其组件关联的所有警报，包括目标交易。 默认情况下，首先列出严重预警。

1. (使用Advertising Creative的广告商；可选)单击&#x200B;**[!UICONTROL Creative]**&#x200B;选项卡以查看包含Advertising Creative体验的投放位置警报。

1. （可选）要根据警报的第一个检测日期对警报进行分组，或按警报状态、组件状态、组件类型或使用特定营销活动名称对警报进行筛选，请单击面板右上角的![筛选按钮](/help/dsp/assets/filter.png)，选择筛选选项，然后单击&#x200B;**[!UICONTROL Apply]**。

1. 要查看特定警报类型的所有受影响营销活动组件的列表，请单击警报名称，如“[!UICONTROL Package: No Active Placement (*N*)]”。 要查看每个受影响组件的详细信息（包括建议的操作），请单击[!UICONTROL EXPAND ALL]或单击组件名称。 若要打开任何受影响组件的相关促销活动管理视图，以便进行建议的更改，请将光标悬停在组件名称上，然后单击“转到”以查看![“转到”以查看](/help/dsp/assets/go-to-view.png "。")

1. （可选）要忽略（隐藏）警报，请将光标悬停在组件名称上，单击![忽略](/help/dsp/assets/alert-ignore.png "忽略")，然后单击&#x200B;**[!UICONTROL Ignore alert till next check]**、**[!UICONTROL Ignore alert for 3 days]**&#x200B;或&#x200B;**[!UICONTROL Ignore indefinitely]**。

在忽略警报后几秒钟内即可撤消该操作。 选项消息关闭后，无法取消操作。

1. （可选）要检索已忽略的警报，请筛选警报以显示[!UICONTROL Alert Status]个“[!UICONTROL All]”或“[!UICONTROL Ignored]”。 要取消忽略警报，请将光标悬停在组件名称上，然后单击![取消忽略](/help/dsp/assets/alert-un-ignore.png "取消忽略")。

## 关闭[!UICONTROL Pulse Panel]

* 单击工具栏右侧的![警报可用时Pulse面板图标](/help/dsp/assets/alerts-panel.png "警报可用时Pulse面板图标")或![无可用警报时的Pulse Panel图标](/help/dsp/assets/alerts-panel-empty.png "无可用警报时的Pulse Panel图标")。

>[!MORELIKETHIS]
>
>* 营销活动管理视图中的[性能报表类型](campaign-reports-about.md)
