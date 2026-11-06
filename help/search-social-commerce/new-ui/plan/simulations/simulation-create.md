---
title: 运行或重新运行自定义模拟
description: 了解如何为项目组合运行或重新运行自定义模拟。
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 0ee62d04-fdc4-445c-90fb-71d5a40a9ed0
TQID: 'https://experienceleague.adobe.com/DlSJEcKXOxVz6UXVpAjQqaiwDTakgJ4SS6rsQUxkQIE'
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
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: cb2d71e240af5ea1278cb2c00046d80040c914ce
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%
---
# 运行或重新运行自定义模拟

*Beta功能*

您可以为[优化或活动的](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#portfolio-status)项目组合生成自定义模拟。 您还可以在列表中选择一个模拟，以便对同一项目组合运行新模拟，或者使用现有设置重新运行模拟。

创建自定义模拟需要[!UICONTROL Create Simulation]权限。 选择项目组合需要[!UICONTROL View Portfolios]权限。

<!-- You can't run sims for portfolios with legacy keyword-level optimization when they include smart bidding campaigns. Clarify all exceptions so users don't find out via error messages. -->

[!UICONTROL Admin]和[!UICONTROL Account Manager]用户可以查看其他用户创建的模拟。 所有其他用户只能查看他们创建的自定义模拟。

## 创建新模拟 {#simulation-create}

您可以从[!UICONTROL Simulations]视图开始，或从[!UICONTROL Portfolios]视图[&#128279;](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md#run-simulation)运行自定义模拟。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Plan]>[!UICONTROL Simulations]**。

1. 清除所有选定的模拟行，然后单击&#x200B;**[!UICONTROL Run Simulation]**。

1. 选择项目组合：

   1. 单击&#x200B;**[!UICONTROL Select Portfolio]**。

   1. 选择项目组合。

      要搜索包含特定文本字符串的项目组合，请开始在搜索字段中输入文本字符串。 值不区分大小写。

   1. 单击&#x200B;**[!UICONTROL Proceed]**。

1. 指定[自定义模拟设置](#custom-simulation-settings)：

   1. （可选）要更改用于模拟的项目组合，请单击项目组合名称旁边的&#x200B;**[!UICONTROL Change Portfolio]**，选择项目组合，然后单击&#x200B;**[!UICONTROL Proceed]**。

   1. 在[!UICONTROL Basic Settings]选项卡上：

      1. 输入唯一的&#x200B;**[!UICONTROL Simulation Name]**。

      1. （可选）更改模拟的基本参数。

   1. （可选）在[!UICONTROL Advanced Settings]选项卡上，更改模拟的高级参数。

   默认情况下，指定所选项目组合的现有参数。 更改这些值将显示不同参数在不更改项目组合现有参数的情况下生成的结果。

1. 单击&#x200B;**[!UICONTROL Next]**。

1. 查看设置，并根据需要编辑设置。

1. 单击&#x200B;**[!UICONTROL Submit & Run]**。

已提交请求，并打开[!UICONTROL Simulations]视图。 当模拟报告可用时，您和任何其他指定的电子邮件收件人都会收到带有下载链接的通知。 您也可以[从[!UICONTROL Simulations]视图](simulation-download.md)下载模拟。

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## 使用现有设置重新运行模拟 {#rerun-a-simulation-with-the-existing-settings}

使用现有设置，一次最多可重新运行10个模拟。 无法重新运行状态为[!UICONTROL Queued]或[!UICONTROL In Progress]的模拟。 如果选择包括这些模拟，则会跳过它们，并提交其余的模拟。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Plan]>[!UICONTROL Simulations]**。

1. 选中要重新运行的模拟旁边的复选框。

1. 在数据表上方或批量操作工具栏中，单击&#x200B;**[!UICONTROL Re-Run Simulation]**。

提交请求，视图将刷新。

## 对列表中的项目组合运行新模拟 {#edit-the-settings-for-an-existing-simulation-and-rerun-it}

在单击[!UICONTROL Run Simulation]之前选择模拟，会为其项目组合选择新的模拟。 该表单使用项目组合的当前设置，而不是所选模拟的设置。 此操作不会编辑现有模拟。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Plan]>[!UICONTROL Simulations]**。

1. 选中要使用的项目组合模拟旁边的复选框。

   如果选择多个模拟，则它们都必须使用相同的项目组合。 项目组合必须处于活动或优化状态。

1. 在数据表上方，单击&#x200B;**[!UICONTROL Run Simulation]**。

1. 指定[自定义模拟设置](#custom-simulation-settings)，包括唯一&#x200B;**[!UICONTROL Simulation Name]**。 根据需要更改&#x200B;**[!UICONTROL Basic Settings]**&#x200B;和&#x200B;**[!UICONTROL Advanced Settings]**&#x200B;选项卡上的参数。

1. 单击&#x200B;**[!UICONTROL Next]**。

1. 查看设置，并根据需要编辑设置。

1. 单击&#x200B;**[!UICONTROL Submit & Run]**。

已提交请求，并打开[!UICONTROL Simulations]视图。 在模拟成功完成之后，您可以[下载模拟](simulation-download.md)。

## 自定义模拟设置 {#custom-simulation-settings}

有关自定义模拟设置的详细信息，请参阅优化指南，该指南可在Search、Social和Commerce中找到。

>[!MORELIKETHIS]
>
>* [关于模拟](simulation-about.md)
>* [查看模拟详细信息](simulation-view.md)
>* [下载模拟](simulation-download.md)
