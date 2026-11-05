---
title: （新UI）管理报表模板
description: 了解如何创建、查看、编辑和删除计划报表和按需报表的可重用报表模板。
feature: Search Reports
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
source-git-commit: eb12699872b7c89240f5340cd3b0a251c9c08366
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%
---
# （新UI）管理报表模板

报告模板是预定义的报告布局，可在生成大多数报告时重复使用。 如果您希望使用非默认参数、运行同一报告的变体或按照常规计划运行同一报告，则使用模板可节省时间。 在&#x200B;**[!UICONTROL Reports]>[!UICONTROL Reports]**&#x200B;的&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡上提供了已保存的模板。

一次最多可以维护100个模板。

查看数据需要[!UICONTROL View Scheduled Reports]权限。 创建、复制、编辑、运行和删除模板以及复制行数据需要[!UICONTROL Edit Scheduled Reports]权限。 您只能编辑您创建的模板。

## 可用操作

* [创建报告模板](#template-create)作为新模板或基于现有模板。

* [在不更改原始报表模板的情况下查看报表模板的设置](#template-view)。

* [编辑报表模板](#template-edit)，包括其计划。

* [根据需要运行指定模板的报告](#template-run)。

* [删除报告模板](#template-delete)。

* [将选定行中的所有数据复制到剪贴板](#copy-to-clipboard)。

## 创建报表模板 {#template-create}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Reports]**。

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 执行以下任一操作：

   * 要创建新模板，请单击&#x200B;**[!UICONTROL Create Template]**。 在&#x200B;**[!UICONTROL Create a New Template]**&#x200B;面板中，选择报告类别和报告类型，然后单击&#x200B;**[!UICONTROL Proceed]**。

   * 要基于现有模板创建模板，请将光标悬停在模板行上，然后单击![模板设置](/help/search-social-commerce/assets/settings-new.png "模板设置") **[!UICONTROL Template Settings]**&#x200B;或&#x200B;**[!UICONTROL ...]>[!UICONTROL Duplicate]**。

1. 输入模板的唯一&#x200B;**[!UICONTROL Report Name]**，并确保已启用&#x200B;**[!UICONTROL Save as Template]**。

   以&#x200B;**[!UICONTROL Create Template]**&#x200B;开头时，默认启用该设置。 如果禁用该功能，则最终操作将更改为&#x200B;**[!UICONTROL Run Report]**，这将生成报告而不是保存模板。

1. 配置[基本和高级报告](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md)、[协助报告](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-settings.md)、[模型准确性报告](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-settings.md)或[专业报告](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-settings.md)的报告设置。

   单击&#x200B;**[!UICONTROL Next]**&#x200B;可在设置部分之间移动。

1. （可选）要自动生成报表，请在&#x200B;**[!UICONTROL Scheduling]**&#x200B;中配置&#x200B;**[!UICONTROL Frequency]**&#x200B;和投放设置。

1. 单击&#x200B;**[!UICONTROL Create]**。

您还可以在从“最新报告”选项卡[&#128279;](/help/search-social-commerce/new-ui/reports/management/report-manage.md)创建报告时保存模板，方法是在提交报告设置之前启用&#x200B;**[!UICONTROL Save as Template]**。

## 查看报表模板的设置 {#template-view}

要检查设置而不更改原始模板，请打开一个重复项。 这需要[!UICONTROL Edit Scheduled Reports]权限。 打开重复项不会保存新模板。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Reports]**。

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 将光标悬停在模板行上并单击![模板设置](/help/search-social-commerce/assets/settings-new.png "模板设置") **[!UICONTROL Template Settings]**。

1. 查看报表设置。

1. 完成后，单击&#x200B;**[!UICONTROL Cancel]**。 如果提示放弃安装，请单击&#x200B;**[!UICONTROL Discard]**。

要保存副本，请按照[模板创建过程](#template-create)操作。

## 编辑报告模板 {#template-edit}

您可以更改所创建的任何模板的设置和计划。 这些更改适用于将来从模板生成的报告。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Reports]**。

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 选中您创建的一个模板旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Edit]**。

   选择多个模板或所选模板由其他用户创建时，[!UICONTROL Edit]不可用。

1. 更改报表设置。 要添加、更改或删除计划，请在&#x200B;**[!UICONTROL Scheduling]**&#x200B;中编辑&#x200B;**[!UICONTROL Frequency]**。

   为计划报告选择每日、每周或每月的频率。 要删除定期计划，请选择&#x200B;**[!UICONTROL Now]**。

   编辑现有模板时，**[!UICONTROL Save as Template]**&#x200B;和&#x200B;**[!UICONTROL Type]**&#x200B;为只读。 您无需再次启用[!UICONTROL Save as Template]。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 根据需要运行指定模板的报表 {#template-run}

您可以随时为一个或多个模板运行报告。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Reports]**。

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 执行以下任一操作：

   * （运行单个模板）：

     1. 打开模板行的菜单并选择&#x200B;**[!UICONTROL Run]**。

     1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。

   * （运行一个或多个模板）：

     1. 选中要运行的每个模板旁边的复选框。

     1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Run]**。

     1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。

您还可以在编辑模板时通过单击&#x200B;**[!UICONTROL Run Report]**，然后单击&#x200B;**[!UICONTROL Confirm]**&#x200B;来运行模板。 首先保存所有更改；此操作运行保存的模板。

## 删除报表模板 {#template-delete}

您可以删除任何可用的报表模板。 当您删除包含计划的模板时，将来不会生成该报告。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Reports]**。

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 执行以下任一操作：

   * （删除单个模板）：

     1. 打开模板行的菜单并选择&#x200B;**[!UICONTROL Delete]**。

     1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。

   * （要删除一个或多个模板）：

     1. 选中要删除的每个模板旁边的复选框。

     1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Delete]**。

     1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。

## 将选定行中的所有数据复制到剪贴板 {#copy-to-clipboard}

根据应用的筛选条件和视图中可见的列，复制选定行中的可见信息。 信息将另存为制表符分隔值(TSV)。

1. 选中要复制其数据的每一行旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Copy]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。
