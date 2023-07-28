---
title: 更改管理视图和报告中的可用事务属性
description: 了解如何在管理视图和报告中使用事务属性。
exl-id: a8f3a2d6-4203-42db-96cd-faf02d20d247
feature: Search Admin, Search Transaction Properties
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# 更改管理视图和报告中的可用事务属性

当Adobe Advertising跟踪 [事务属性](/help/search-social-commerce/glossary.md#s-t) 对于广告商，它最初不在项目组合目标、报告和管理视图中。 要使属性可见，必须明确使其可用，然后根据需要更改默认显示名称（即显示的名称）。 唯一的例外是所跟踪的转化 [!DNL Google Ads]， [!DNL Google Analytics]、和 [!DNL Microsoft® Advertising] 通用事件跟踪标记自动可用和可见。

同样，您可以在项目组合目标、报表和管理视图中隐藏资产。 隐藏以前可见的属性时，该属性将从包含该属性的任何派生量度中删除。

从可用的属性列表中，每个有权访问广告商数据的用户都可以自定义他们看到的管理视图和报表属性，包括或忽略他们选择的特定属性。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.

   将列出为广告商收集的所有事务属性以及已指定用于显示的任何不同名称。

1. （可选）筛选列表：

   * 要搜索特定的属性名称或显示名称，请单击 ![Search](/help/search-social-commerce/assets/search.png "Search")，在输入字段中输入单词或字符串，然后按 **[!DNL Enter]** 键。

     您可以搜索出现在短语中任意位置的字符串（例如第一个字母或最后三个字母），而搜索词不是 [区分大小写](/help/search-social-commerce/glossary.md#c-d).

   * 要按属性在管理视图和报告中的可用性搜索属性，请单击 ![筛选](/help/search-social-commerce/assets/filter.png "筛选")，然后选择过滤器 **[!UICONTROL Show in UI and Reports]**. 然后选择以下任一选项 **[!UICONTROL Show]** （查看可包含在报表和管理视图中的属性）或 **[!UICONTROL Hide]** （查看报表和管理视图中不可用的属性）。

1. 更改可用于管理视图和报告的属性：

   * 要显示或隐藏单个属性，请单击 **[!UICONTROL Show in UI and Reports]** 列以更改设置。

   * 要显示或隐藏多个属性，请执行以下操作：

      1. 选中每个属性旁边的复选框。

         有关选择多行的提示，请参阅&quot;[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)“

      1. 在数据表上方的工具栏中，单击 ![显示](/help/search-social-commerce/assets/show.png "显示") 显示属性或 ![隐藏](/help/search-social-commerce/assets/hide.png "隐藏") 以隐藏属性。

      1. （要隐藏属性）在确认消息中，单击 **[!UICONTROL Yes]** 以隐藏属性，包括从包含属性的任何派生指标中删除这些属性。

1. （可选） [更改列标题中显示的名称](transaction-property-edit-display-name.md) 用于任何属性。

   每个可见属性的默认显示名称是检索数据中拼写的属性名称。

>[!NOTE]
>
>如果Adobe Advertising收集新资产的数据，则这些新资产 — 跟踪的转化除外 [!DNL Google Ads]， [!DNL Google Analytics]、和 [!DNL Microsoft® Advertising] 通用事件跟踪标记 — 自动从管理视图和报告中排除，直到将其包含为止。 由跟踪的新转化 [!DNL Google Ads]， [!DNL Google Analytics]、和 [!DNL Microsoft® Advertising] 通用事件跟踪标记始终自动可用。

>[!MORELIKETHIS]
>
* [关于管理广告商的交易记录属性](transaction-property-about.md)
* [查看为广告商跟踪的交易记录属性](transaction-property-view-tracked.md)
* [更改事务属性的显示名称](transaction-property-edit-display-name.md)
