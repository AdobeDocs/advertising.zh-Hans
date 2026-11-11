---
title: （新UI）查看项目组合的更改历史记录和竞价更改历史记录
description: 了解如何在Adobe Advertising Search、Social和Commerce中查看项目组合更改和竞价更改历史记录、更改日期范围、筛选项目组合更改，以及生成、下载和删除历史记录报告。
feature: Search Portfolios, Search Optimization
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
source-git-commit: e7e0221adbb72127a9e6d2354b6a235b233a4a76
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%
---
# （新UI）查看项目组合的更改历史记录和竞价更改历史记录

*Beta功能*

您可以查看项目组合在任何日期范围内的更改日志。 记录的操作包括项目组合创建、对项目组合设置的所有更改、项目组合的所有分配或未分配的促销活动、项目组合中竞价单位的所有应用限制或从竞价单位中删除的所有限制、项目组合中已过期的竞价单位的所有限制以及影响项目组合的其他操作。

[!UICONTROL Change History]对话框包括组合更改的[!UICONTROL Portfolio Change History]选项卡和竞价历史记录的[!UICONTROL Portfolio Bid Change History]选项卡。 默认情况下，这两个选项卡显示最近180天，昨天结束。

您可以按类别筛选项目组合更改，并更改任一选项卡的日期范围。 您也可以将数据下载到电子表格文件。

## 查看项目组合的更改历史记录 {#portfolio-change-history}

每个更改的信息包括[!UICONTROL Change Date]、[!UICONTROL Changed By]、[!UICONTROL Change Type]和[!UICONTROL Description]。 将列出从最新到最旧的更改。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Portfolios]**。

1. 将光标悬停在项目组合行上并单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Change History]**。

1. 在[!UICONTROL Change History]对话框中，查看&#x200B;**[!UICONTROL Portfolio Change History]**&#x200B;选项卡。

1. （可选）更改显示的信息：

   * 单击![日历](/help/search-social-commerce/assets/calendar-new.png "日历")以更改报告的日期范围。

   * 单击![筛选器](/help/search-social-commerce/assets/filter-new.png "筛选器")以按类别筛选数据： [!UICONTROL All]、[!UICONTROL Objective]、[!UICONTROL Campaign]、[!UICONTROL Target]、[!UICONTROL Constraints]、[!UICONTROL Optimization Levers]或[!UICONTROL Others]。

## 查看项目组合的竞价更改历史记录 {#portfolio-bid-change-history}

1. [打开项目组合的更改历史记录](#portfolio-change-history)。

1. 单击&#x200B;**[!UICONTROL Portfolio Bid Change History]**&#x200B;选项卡。

1. （可选）单击![日历](/help/search-social-commerce/assets/calendar-new.png "日历")以更改日期范围。

1. （可选）单击日期列标题以按日期升序或降序对列表进行排序。

要查看单个竞价单位的历史记录，请[打开组合性能详细信息中的竞价单位详细信息](portfolio-details.md#bid-unit-history)。 当[!UICONTROL Bid Unit ID]列可用时，您还可以从[!UICONTROL Keywords]视图[&#128279;](/help/search-social-commerce/new-ui/manage/keywords/keyword-manage.md#bid-unit-history)中打开竞价单位历史记录。

## 管理项目组合更改历史记录报告

您可以将项目组合更改历史记录的其他信息下载到[!DNL Microsoft Excel]工作簿（XLSX文件）格式的文件。 报表包括数值更改ID、新旧值、更改类型（如“已添加”或“已修改”）、操作类型（如“预算”或“Portfolio名称”）和子类型（如果适用）、时间和用户名。

您还可以从[!UICONTROL Portfolio Bid Change History]选项卡生成、下载和删除报告。 报表设置的标题为项目组合更改的[!UICONTROL Portfolio History]和竞价历史记录的[!UICONTROL Portfolio Bid History]。

### 生成具有已过滤数据行的报告

1. [打开项目组合的更改历史记录](#portfolio-change-history)，然后单击要下载其数据的选项卡。

1. 单击右上角的![下载报告](/help/search-social-commerce/assets/download.png "下载报告")。

1. 在[!UICONTROL Portfolio History]或[!UICONTROL Portfolio Bid History]设置中，接受默认报表名称或输入唯一报表名称，然后单击&#x200B;**[!UICONTROL Generate]**。

   默认情况下，报表名称包含历史记录类型以及`YYYYMMDD_HHmm`格式的日期和时间，如“portfolioChangeHistory_20260402_1326”。 如果名称已存在，则会添加数字后缀。

   文件已添加到[!UICONTROL Recently Generated]列表。

1. （可选）要在文件完成后下载文件，请单击文件名旁边的![下载](/help/search-social-commerce/assets/download.png "下载")。

   将按照浏览器的正常过程下载文件。

### 下载已完成的报表

1. [打开项目组合的更改历史记录](#portfolio-change-history)，然后单击从中生成报告的选项卡。

1. 单击右上角的![下载报告](/help/search-social-commerce/assets/download.png "下载报告")。

1. 在[!UICONTROL Portfolio History]或[!UICONTROL Portfolio Bid History]设置的[!UICONTROL Recently Generated]列表中，单击文件名旁边的![下载](/help/search-social-commerce/assets/download.png "下载")。

   将按照浏览器的正常过程下载文件。

### 删除已完成的报告

1. [打开项目组合的更改历史记录](#portfolio-change-history)，然后单击从中生成报告的选项卡。

1. 单击右上角的![下载报告](/help/search-social-commerce/assets/download.png "下载报告")。

1. 在[!UICONTROL Portfolio History]或[!UICONTROL Portfolio Bid History]设置的[!UICONTROL Recently Generated]列表中，单击文件名旁边的![删除](/help/search-social-commerce/assets/delete-new.png "删除")。

>[!MORELIKETHIS]
>
>* [创建项目组合](portfolio-create.md)
>* [（新UI）编辑项目组合](portfolio-edit.md)
>* [（新UI）查看项目组合性能详细信息](portfolio-details.md)
>* [（新UI）下载[!UICONTROL Portfolios]视图中的数据](portfolio-view-report.md)
>* [关于项目组合](portfolio-about.md)
