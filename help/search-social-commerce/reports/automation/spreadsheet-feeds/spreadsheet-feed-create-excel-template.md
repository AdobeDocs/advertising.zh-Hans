---
title: 为电子表格报表源创建 [!DNL Excel] 模板
description: 了解如何创建特别格式化的电子表格模板。
exl-id: 74bf3cdf-7d56-431a-8aff-11ed3840a7cd
feature: Search Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# 为电子表格报表源创建[!DNL Excel]模板

*仅用于基本报告和模型准确性报告*

要创建电子表格馈送，您必须首先使用常规报表模板创建特别格式化的[!DNL Microsoft Excel]电子表格模板。 您可以选择自定义[!DNL Excel]电子表格以包含其他列和图。

1. 在&#x200B;**[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**&#x200B;中，使用“[!UICONTROL Daily]”的[!UICONTROL Date Aggregation]单位并使用所有其他所需的数据参数生成所需的报告类型，并将报告另存为模板。

   >[!NOTE]
   >
   > * 您可以为[!UICONTROL Portfolio]、[!UICONTROL Search Engine]、[!UICONTROL Search Engine Account]、[!UICONTROL Campaign]、[!UICONTROL Ad Group]、[!UICONTROL Ad Variation]、[!UICONTROL Keyword]和[!UICONTROL Forecast Accuracy]报告创建电子表格馈送。 如果使用[!UICONTROL Ad Group Report]，请限制包含的广告组数，以便更快地获得结果。
   > * 未使用模板中定义的[!UICONTROL Date Range]单位。 稍后配置电子表格馈送时，您将定义刷新数据的日期。

1. 生成报告后，转到&#x200B;**[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**&#x200B;并将报告输出的TSV或XLS版本导出到文件。

1. 在[!DNL Excel]中，为报告创建自定义模板：

   1. 在[!DNL Excel]中打开报告文件。

   1. 准备工作簿：

      1. 删除显示报表参数的顶行。 对于XLS文件，也删除“[!UICONTROL Total]”行。 您可以选择删除某些数据行，但应保留a)数据标题行，其中所有列均按原始顺序排列和b)至少一个数据行。 请勿手动添加任何数据。

         >[!NOTE]
         >
         > 最后一列必须包含非零值。

      2. 按开始日期升序对数据进行排序（从最早到最新）。

      3. 将工作表选项卡名称从“[!UICONTROL Sheet1]”更改为“[!UICONTROL RAW]”。

         此特定选项卡名称允许刷新数据。

      4. （可选）根据需要，在报表模板中的列右侧添加自定义列。

   1. （可选）在单独的工作表上创建一个数据透视表。 完成后，右键单击数据透视表的任意单元格并选择&#x200B;**[!UICONTROL Pivot Table Options]**，单击&#x200B;**[!UICONTROL Data]**&#x200B;选项卡，然后选择&#x200B;**[!UICONTROL Refresh data when opening the file]**。

   1. 将文件另存为.XLSX格式的[!DNL Excel]电子表格。

>[!MORELIKETHIS]
>
>* [关于电子表格报表馈送](spreadsheet-feed-about.md)
>* [创建电子表格报表源](spreadsheet-feed-create.md)
>* [编辑电子表格报表源设置](spreadsheet-feed-edit.md)
>* [电子表格报表源设置](spreadsheet-feed-settings.md)
>* [查看或保存电子表格报表源文件](spreadsheet-feed-view-or-save.md)
>* [手动刷新电子表格报表馈送](spreadsheet-feed-refresh.md)
>* [删除电子表格报表馈送](spreadsheet-feed-delete.md)
