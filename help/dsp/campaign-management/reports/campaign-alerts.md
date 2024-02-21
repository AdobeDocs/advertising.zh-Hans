---
title: 查看警报
description: 了解如何查看营销活动和营销活动组件的警报和建议解决方案。
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
source-git-commit: 70592355207ba43341eb208750dcd3fc00db51c1
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---

# 查看警报

*Beta版功能*

DSP可帮助您识别任何促销活动或促销活动组件何时出现问题。 对于每个问题，DSP都会创建一个带有时间戳的警报，以及解决此问题的建议操作。 警报的原因包括配置问题（例如，当投放位置没有附加广告或交易设置错误时）、广告拒绝和活动运行状况问题（例如广告投放或性能不佳）。 警报在营销活动、包、投放位置、广告和交易级别可用。

警报在以下位置提供：

* A [!UICONTROL Pulse Panel] 图标 [!UICONTROL Campaigns]， [!UICONTROL Packages] 和包详细信息， [!UICONTROL Placements]、和 [!UICONTROL Ads] 视图指示该视图中的项目是否有任何警报。 图标具有蓝色圆点时(![警报可用时的Pulse Panel图标](/help/dsp/assets/alerts-panel.png "警报可用时的Pulse Panel图标"))，则警报可用。 当没有点可见时(![无可用警报时的Pulse Panel图标](/help/dsp/assets/alerts-panel-empty.png "无可用警报时的Pulse Panel图标"))，没有可用警报。

* 相同视图中的数据表包括&#39;&#39;[!UICONTROL Alerts]指示项目（或其组件）何时出现问题的“列。 警报指示器包括“严重”(![关键](/help/dsp/assets/indicator-critical.png "关键"))，“警告”(![警告](/help/dsp/assets/indicator-warning.png "警告"))和“信息”(![信息](/help/dsp/assets/indicator-information.png "信息"))。

您可以打开任何警报的相关促销活动管理视图，以便根据需要编辑设置来解决问题。

您还可以选择忽略单个警报，这样会将其从 [!UICONTROL Pulse] 面板。

当基础问题得到解决时，警报和警报指示器会自动消失。

## 在中查看警报 [!UICONTROL Pulse Panel]

1. 在主菜单中，单击 **[!UICONTROL Campaigns]**.

1. 执行以下任一操作：

   * （对于适用于该视图的所有警报）在任何营销活动管理视图的工具栏右侧，单击 ![警报可用时的Pulse Panel图标](/help/dsp/assets/alerts-panel.png "警报可用时的Pulse Panel图标").

   * （对于特定营销活动的所有警报）单击营销活动行的警报指示器，然后单击 **[!UICONTROL View in Pulse panel]**.

   * （针对特定包、投放位置或广告的所有警报）执行以下操作：

      1. 单击营销活动名称。

      1. 在子菜单中，单击 **[!UICONTROL Packages]**， **[!UICONTROL Placements]**，或 **[!UICONTROL Ads]** 以打开相关的营销活动组件视图。

      1. 单击包、投放位置或广告行的警报指示器，然后单击 **[!UICONTROL View in Pulse Panel]**.

   列出与促销活动及其组件关联的所有警报，包括目标交易。 默认情况下，首先列出严重预警。

1. （可选）要根据警报的第一个检测日期对警报进行分组，或者按警报状态、组件状态、组件类型或使用特定促销活动名称对警报进行过滤，请单击 ![“筛选器”按钮](/help/dsp/assets/filter.png) 在面板的右上角，选择过滤器选项，然后单击 **[!UICONTROL Apply]**.

1. 要查看特定警报类型的所有受影响营销活动组件的列表，请单击警报名称，例如“[!UICONTROL Package: No Active Placement (*N*)]“。 要查看每个受影响组件的详细信息（包括建议的操作），请单击 [!UICONTROL EXPAND ALL] 或单击组件名称。 要打开任何受影响组件的相关促销活动管理视图，以便进行建议的更改，请将光标悬停在组件名称上，然后单击 ![转到视图](/help/dsp/assets/go-to-view.png "转到视图").

1. （可选）要忽略（隐藏）警报，请将光标悬停在组件名称上，然后单击 ![忽略](/help/dsp/assets/alert-ignore.png "忽略")，然后单击 **[!UICONTROL Ignore indefinitely]**.  <!-- **[!UICONTROL Ignore alert for three days]**, **[!UICONTROL Ignore alert until next check]**, or **[!UICONTROL Ignore indefinitely] -->

在忽略警报后几秒钟内即可撤消该操作。 选项消息关闭后，无法取消操作。

1. （可选）要检索已忽略的警报，请筛选警报以显示 [!UICONTROL Alert Status] / &quot;[!UICONTROL All]”或“[!UICONTROL Ignored]“ 要取消忽略警报，请将光标悬停在组件名称上，然后单击 ![取消忽略](/help/dsp/assets/alert-un-ignore.png "取消忽略").

## 关闭 [!UICONTROL Pulse Panel]

* 在工具栏的右侧，单击 ![警报可用时的Pulse Panel图标](/help/dsp/assets/alerts-panel.png "警报可用时的Pulse Panel图标") 或 ![无可用警报时的Pulse Panel图标](/help/dsp/assets/alerts-panel-empty.png "无可用警报时的Pulse Panel图标").

>[!MORELIKETHIS]
>
>* [Campaign Management视图中的性能报表类型](campaign-reports-about.md)
