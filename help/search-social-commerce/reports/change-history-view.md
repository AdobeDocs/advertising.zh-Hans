---
title: 查看[!UICONTROL Change History]报告
description: 了解如何查看对广告商帐户的最近更改。
exl-id: f8744da7-cc7a-49c1-aeac-1e601768f992
feature: Search Reports
TQID: https://experienceleague.adobe.com/nRlvKpVQf3wbMd83plf3CQp1pPYpHVJzMVJN54lryYM
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 84eb5f060a696e057f706c0066c18c9afc1511e1
workflow-type: tm+mt
source-wordcount: 546
ht-degree: 0%

---

# 查看[!UICONTROL Change History]报告

（新UI） [!UICONTROL History Logs]和（旧版UI） [!UICONTROL Change History]报告包含过去31天内对广告商帐户所做的更改日志。 报表可以包括对以下对象类型的更改：用户（广告商）、项目组合、促销活动、广告组、广告、关键字、投放位置和产品目标。 您可以按任意列对数据进行排序和过滤。

您可以将有关广告商历史记录日志的其他信息下载到[!DNL Microsoft Excel]工作簿（XLSX文件）格式的文件。 报表包含新旧值以及发生更改的时间。

>[!NOTE]
>
>有关项目组合的更改，另请参阅[项目组合的更改历史记录](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-view-change-history.md)。

## （新UI）查看[!UICONTROL History Logs]报表 {#history-logs-open}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]** > **[!UICONTROL History Logs]**。

1. （可选） [更改视图](/help/search-social-commerce/common-tasks/data-views/data-views-about.md)中包含的数据。

### 管理[!UICONTROL History Logs]的报告下载

#### 生成具有已过滤数据行的报告

1. [打开历史记录日志](#history-logs-open)。

1. 单击右上角的![下载报告](/help/search-social-commerce/assets/download.png "下载报告")。

1. 在[!UICONTROL Grid Reports]设置中，输入唯一的报表名称，然后单击&#x200B;**[!UICONTROL Generate]**。

   默认情况下，该文件名为“allChangeHistory_YYYYMMDD_NNNN”，其中“NNNN”是连续的作业编号（如“allChangeHistory_20260402_1326）。

   文件已添加到[!UICONTROL Recently Generated]列表。

1. （可选）要在文件完成后下载文件，请单击文件名旁边的![下载](/help/search-social-commerce/assets/download.png "下载")。

   将按照浏览器的正常过程下载文件。

#### 下载已完成的报表

1. [打开历史记录日志](#history-logs-open)。

1. 单击右上角的![下载报告](/help/search-social-commerce/assets/download.png "下载报告")。

1. 在[!UICONTROL Grid Reports]对话框的[!UICONTROL Recently Generated]列表中，单击文件名旁边的![下载](/help/search-social-commerce/assets/download.png "下载")。

   将按照浏览器的正常过程下载文件。

#### 删除已完成的报告

1. [打开历史记录日志](#history-logs-open)。

1. 单击右上角的![下载报告](/help/search-social-commerce/assets/download.png "下载报告")。

1. 在[!UICONTROL Grid Reports]对话框的[!UICONTROL Recently Generated]列表中，单击文件名旁边的![删除](/help/search-social-commerce/assets/delete-new.png "删除")。

## （旧版UI）查看[!UICONTROL Change History]报表

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]** > **[!UICONTROL Insights & Reports]** > **[!UICONTROL Change History]**。

1. （可选）通过以下任意方式更改报表中包含的数据：

   * （要显示或隐藏列）单击任意列标题右侧的![向下箭头](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭头")，突出显示&#x200B;**[!UICONTROL Columns]**，然后选中要包含的每个列旁边的复选框，并清除要排除的每个列旁边的复选框。

     列配置将应用于您所有广告商的视图。

   * （要按列值过滤数据）执行以下任一操作：

      * [使用&#x200B;**[!UICONTROL Add Filter]**&#x200B;链接](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)应用筛选器。

      * [从列标题菜单应用筛选器](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)。

   * （要更改报告的日期范围），请执行以下操作：

      1. 在数据表上方，单击当前日期范围。

      1. 指定范围：

         * （对于预设范围） — 从常用时间增量列表中进行选择。 默认值为&#x200B;*[!UICONTROL 2 Days Ago]*。

         * （对于特定范围） — 选择&#x200B;**[!UICONTROL Custom Date Range]**，然后指定开始日期和结束日期。

           以MM/DD/YYYY或MM-DD-YYYY格式输入日期，或单击每个字段旁边的![日历](/help/search-social-commerce/assets/calendar.png "日历")以打开日历并选择日期。 您只能包含之前31天的数据。

      1. 单击&#x200B;**[!UICONTROL Apply]**。

1. （可选）下载报表的副本：

   1. 在数据表上方，单击&#x200B;**[!UICONTROL Download]**。

      报告完成后，它将列在[!UICONTROL Download]菜单中。

   1. （要在文件中打开或保存报告数据）在文件名旁单击![以XLS格式下载报告](/help/search-social-commerce/assets/download-spreadsheet2.png "以XLS格式下载报告")，然后按照浏览器的正常过程打开或保存文件。

      有关详细信息，请参阅浏览器的联机帮助。
