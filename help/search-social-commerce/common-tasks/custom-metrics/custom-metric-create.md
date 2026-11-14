---
title: 创建自定义量度
description: 了解如何配置自定义量度，这些量度通过标准量度计算。
exl-id: a9ce503a-67ee-477e-8f79-31b4a9c6e51a
feature: Search Common Tasks, Search Custom Metrics
TQID: 'https://experienceleague.adobe.com/g-J8AlulQ20I-vxQrPkPaP-Ap66bBIng0eKDPqhV9U4'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: a1695a4d-41fb-5bb6-a22a-9e7a1b3222d7
    internal-label: Search Custom Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 9837cac1a920b1b3b88b04b150cb604832209eaf
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%
---
# 创建自定义量度

## （新UI）从管理视图创建自定义量度

*在[!UICONTROL Manage]菜单的大多数实体视图中可用，<!-- [!UICONTROL Plan] > [!UICONTROL Simulations],--> [!UICONTROL Setup] > [!UICONTROL Label Classifications]，[!UICONTROL Goals] > [!UICONTROL Objectives]和[!UICONTROL Constraints]，以及[!UICONTROL Targeting] > [!UICONTROL Placements]*

1. 在数据表上方，执行以下任一操作：

   * 单击当前应用的视图的名称（![视图](/help/search-social-commerce/assets/view.png "视图")）。 将光标悬停在任何可编辑视图的名称上，然后单击![编辑](/help/search-social-commerce/assets/edit-new.png "编辑")以打开视图设置。

     您创建的自定义量度将在所有视图中均可用。

   * 单击![自定义列](/help/search-social-commerce/assets/custom-columns-new.png "自定义列")以打开列配置设置。

1. 在打开的列列表下方，单击![创建自定义量度](/help/search-social-commerce/assets/add.png "创建自定义量度") **[!UICONTROL Create Custom Metric]**。

1. 指定[自定义量度设置](custom-metric-settings.md)。

1. 单击&#x200B;**[!UICONTROL Create]**。

## （新UI）根据报表或报表模板设置创建自定义量度 {#create-from-report-settings}

1. 在报表或报表模板设置中，转到&#x200B;**[!UICONTROL Columns]**&#x200B;步骤。

1. 在&#x200B;**[!UICONTROL Custom Metrics]**&#x200B;部分中，指定量度设置：

   * **[!UICONTROL Custom Metric Name]：**&#x200B;输入指标的名称。

   * **[!UICONTROL Format]：**&#x200B;选择&#x200B;**[!UICONTROL Currency]**、**[!UICONTROL Number to 2 Decimal Places]**、**[!UICONTROL Number to 3 Decimal Places]**、**[!UICONTROL Number w/out Decimal Places]**&#x200B;或&#x200B;**[!UICONTROL Percentage]**。

   * **[公式输入字段]：**&#x200B;通过从&#x200B;**[!UICONTROL Insert Metric]**&#x200B;中选择量度并单击运算符按钮（`+`、`-`、`*`、`/`、`(`和`)`）生成公式。 您也可以手动输入公式。 将光标放在要插入每个量度或运算符的位置。

1. 单击&#x200B;**[!UICONTROL Add Metric]**。

   成功创建量度后，可用列列表将按量度名称进行过滤。 创建指标不会自动将其包含在报表中。

1. 若要在报表中包含该量度，请在可用列列表中选择该量度，然后单击![向右箭头](/help/search-social-commerce/assets/arrow-right-customize.png "向右箭头")将其移动到选定列列表中。

## （旧版UI）从营销活动管理视图创建自定义量度

1. 在数据表上方，执行以下任一操作：

   * 单击默认视图或自定义视图的名称以打开视图设置。

   * 单击![自定义列](/help/search-social-commerce/assets/custom-columns.png "自定义列")以打开列配置设置。

1. 在打开的列列表下方，单击![新建自定义量度](/help/search-social-commerce/assets/add.png "新建自定义量度") **[!UICONTROL Create New Custom Metric]**。

1. 指定[自定义量度设置](custom-metric-settings.md)。

1. 单击&#x200B;**[!UICONTROL Save]**。

## （旧版UI）从报表或报表模板表单创建自定义量度

1. 在报表或报表模板表单中，转到&#x200B;**[!UICONTROL Columns]**&#x200B;选项卡。

1. 在右部分中，单击&#x200B;**[!UICONTROL Create]**。

1. 指定[自定义量度设置](custom-metric-settings.md)。

1. 单击&#x200B;**[!UICONTROL Submit]**。

## （旧版UI）从[!UICONTROL Portfolios]视图创建自定义量度

1. 在数据表上方，单击![编辑选定视图](/help/search-social-commerce/assets/view-settings.png "编辑选定视图")。

1. 单击&#x200B;**[!UICONTROL Columns]**&#x200B;选项卡。

1. 在右部分中，单击&#x200B;**[!UICONTROL Create]**。

1. 指定[自定义量度设置](custom-metric-settings.md)。

1. 单击&#x200B;**[!UICONTROL Submit]**。

>[!MORELIKETHIS]
>
>* [关于自定义量度](custom-metric-about.md)
>* [编辑自定义量度](custom-metric-edit.md)
>* [删除自定义量度](custom-metric-delete.md)
>* [自定义量度设置](custom-metric-settings.md)
