---
title: 更改管理视图和报告中的可用转化量度
description: 了解如何在管理视图和报告中使用转化量度。
feature: Conversions
exl-id: de3d288a-5fec-4479-92cf-7754390e21bb
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# 更改管理视图和报告中的可用转化量度

当Adobe Advertising跟踪 [转化](/help/search-social-commerce/glossary.md#c-d) 量度对于广告商而言，它最初不在项目组合目标、报表和管理视图中。 要使转化量度可见，您必须明确使其可用，然后根据需要更改默认显示名称（即显示的名称）。 唯一的例外是所跟踪的转化 [!DNL Google Ads]， [!DNL Google Analytics]、和 [!DNL Microsoft Advertising] 通用事件跟踪标记自动可用和可见。

同样，您可以在项目组合目标、报表和管理视图中隐藏转化量度。 当您隐藏以前可见的转化量度时，它会从包含该转化量度的任何派生量度中删除。

从可用的转化量度列表中，每个有权访问广告商数据的用户都可以自定义他们看到的管理视图和报表的量度，包括或忽略他们选择的特定量度。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   将列出为广告商收集的所有转化量度，以及已指定用于显示的任何不同名称。

1. （可选）筛选列表：

   * 要搜索特定的量度名称或显示名称，请单击 ![Search](/help/search-social-commerce/assets/search.png "Search")，在输入字段中输入单词或字符串，然后按 **[!DNL Enter]** 键。

     您可以搜索出现在短语中任意位置的字符串（例如第一个字母或最后三个字母），而搜索词不是 [区分大小写](/help/search-social-commerce/glossary.md#c-d).

   * 要按转化量度在管理视图和报告中的可用性搜索转化量度，请单击 ![筛选](/help/search-social-commerce/assets/filter.png "筛选")，然后选择过滤器 **[!UICONTROL Show in UI and Reports]**. 然后选择以下任一选项 **[!UICONTROL Show]** （查看可包含在报表和管理视图中的转化量度）或 **[!UICONTROL Hide]** （查看报表和管理视图中不可用的转化量度）。

1. 更改可用于管理视图和报表的转化量度：

   * 要显示或隐藏单个量度，请单击 **[!UICONTROL Show in UI and Reports]** 列以更改设置。

   * 要显示或隐藏多个量度，请执行以下操作：

      1. 选中每个转化量度旁边的复选框。

         有关选择多行的提示，请参阅&quot;[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)“

      1. 在数据表上方的工具栏中，单击 ![显示](/help/search-social-commerce/assets/show.png "显示") 显示量度或 ![隐藏](/help/search-social-commerce/assets/hide.png "隐藏") 以隐藏量度。

      1. （要隐藏量度）在确认消息中，单击 **[!UICONTROL Yes]** 以隐藏量度，包括从包含这些量度的任何派生量度中删除这些量度。

1. （可选） [更改列标题中显示的名称](conversion-metric-edit-display-name.md) 用于任何转化量度。

   每个可见转化量度的默认显示名称是检索数据中拼写的量度名称。

>[!NOTE]
>
>如果Adobe Advertising收集了新转化指标的数据，则这些新指标（跟踪的转化除外） [!DNL Google Ads]， [!DNL Google Analytics]、和 [!DNL Microsoft Advertising] 通用事件跟踪标记 — 自动从管理视图和报告中排除，直到将其包含为止。 由跟踪的新转化 [!DNL Google Ads]， [!DNL Google Analytics]、和 [!DNL Microsoft Advertising] 通用事件跟踪标记始终自动可用。

>[!MORELIKETHIS]
>
>* [关于管理广告商的转化量度](conversion-metric-about.md)
>* [查看为广告商跟踪的转化量度](conversion-metric-view-tracked.md)
>* [更改转化量度的显示名称](conversion-metric-edit-display-name.md)
