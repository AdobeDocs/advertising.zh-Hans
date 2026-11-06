---
title: 从[!UICONTROL Portfolios]视图运行并下载模拟
description: 了解如何运行自定义模拟以及从项目组合视图中下载每周模拟。
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: 1d0fea65-a874-543d-94c9-b4dbf9e0360a
    internal-label: Search Simulations
source-git-commit: cb2d71e240af5ea1278cb2c00046d80040c914ce
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%
---
# 从[!UICONTROL Portfolios]视图运行并下载模拟

*Beta功能*

您可以为单个[优化或活动的](portfolio-about.md#portfolio-status)项目组合运行自定义模拟，并从[!UICONTROL Portfolios]视图下载多达100个项目组合的自动每周模拟。

运行自定义模拟需要[!UICONTROL Create Simulation]权限。 下载每周模拟需要[!UICONTROL View Simulation]权限。

>[!NOTE]
>
>您也可以[从[!UICONTROL Simulations]视图](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md)创建或重新运行自定义模拟。

## 运行自定义模拟 {#run-simulation}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Portfolios]**。

1. 执行以下任一操作：

   * 将光标悬停在项目组合行上。 在项目组合名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Run Simulation]**。

   * 选中项目组合旁边的复选框。 在批量操作工具栏中，单击&#x200B;**[!UICONTROL More]>[!UICONTROL Run Simulation]**。

1. 指定[自定义模拟设置](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md#custom-simulation-settings)：

   1. 在&#x200B;**[!UICONTROL Basic Settings]**&#x200B;选项卡上，输入唯一的&#x200B;**[!UICONTROL Simulation Name]**&#x200B;并根据需要更改基本参数。

   1. （可选）在&#x200B;**[!UICONTROL Advanced Settings]**&#x200B;选项卡上，更改高级参数。

   所选项目组合的当前设置会用作默认值。 更改模拟设置不会更改项目组合的设置。

1. 单击&#x200B;**[!UICONTROL Next]**。

1. 查看设置并根据需要进行更改。

1. 单击&#x200B;**[!UICONTROL Submit & Run]**。

已提交请求，并打开[!UICONTROL Simulations]视图。 在模拟成功完成之后，您可以[下载模拟](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md)。

## 下载每周模拟 {#download-simulations}

您可以作为[!DNL Microsoft Excel]工作簿（XLSX文件）一次下载一个运行日期的每周模拟。 仅包含具有当日可用模拟报告的有效和优化项目组合。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Portfolios]**。

1. 选中要下载其每周模拟的每个项目组合旁边的复选框。 选择最多100个项目组合。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL More]>[!UICONTROL Download Simulation]**。

1. 在&#x200B;**[!UICONTROL Weekly Simulation]**&#x200B;中，选择一个运行日期。

   默认情况下会选择最近的可用日期。 如果某些选定项目组合没有可用报表，则该对话框会显示将排除的项目组合数量。 如果需要，请选择其他日期。 当所选项目组合中没有该日期可用的模拟时，您无法下载报表。

1. 单击“下载”按钮，其标签包含具有可用报表的项目组合数量（例如，**[!UICONTROL Download 2 portfolios]**）。

   将按照浏览器的正常过程下载文件。 完成消息指示包含的项目组合数量。

要下载自定义模拟或选择个别每周模拟，请使用[[!UICONTROL Simulations]视图](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md)。

>[!MORELIKETHIS]
>
>* [（新UI）查看项目组合性能详细信息](portfolio-details.md)
>* [关于项目组合](portfolio-about.md)
>* [运行或重新运行自定义模拟](/help/search-social-commerce/new-ui/plan/simulations/simulation-create.md)
>* [下载模拟](/help/search-social-commerce/new-ui/plan/simulations/simulation-download.md)
