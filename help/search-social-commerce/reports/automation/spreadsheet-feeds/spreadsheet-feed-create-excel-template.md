---
title: 创建 [!DNL Excel] 电子表格报表馈送模板
description: 了解如何创建特别格式化的电子表格模板。
exl-id: d675cb8c-b7a9-4d7b-8435-5dd662d151a3
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# 创建 [!DNL Excel] 电子表格报表馈送模板

*仅用于基本报表和模型准确性报表*

要创建电子表格馈送，您必须首先创建特别格式化的馈送 [!DNL Microsoft® Excel] 电子表格模板。 您可以选择自定义 [!DNL Excel] 电子表格以包含其他列和图形。

1. 在 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**，使用生成所需的报表类型 [!UICONTROL Date Aggregation] “”的单位[!UICONTROL Daily]”和所有其他所需的数据参数，将报表另存为模板。

   >[!NOTE]
   >
   > * 您可以为创建电子表格馈送 [!UICONTROL Portfolio]， [!UICONTROL Search Engine]， [!UICONTROL Search Engine Account]， [!UICONTROL Campaign]， [!UICONTROL Ad Group]， [!UICONTROL Ad Variation]， [!UICONTROL Keyword]、和 [!UICONTROL Forecast Accuracy] 报表。 如果您使用 [!UICONTROL Ad Group Report]，限制包含的广告组数量以更快地获得结果。
   > * 此 [!UICONTROL Date Range] 不使用模板中定义的设备。 稍后配置电子表格馈送时，您将定义刷新数据的日期。

1. 生成报告后，转到 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** 并将报表输出的TSV或XLS版本导出到文件。

1. 在 [!DNL Excel]，为报表创建自定义模板：

   1. 在中打开报表文件 [!DNL Excel].

   1. 准备工作簿：

      1. 删除显示报表参数的顶行。 对于XLS文件，也删除&#39;&#39;[!UICONTROL Total]”行。 您可以选择删除某些数据行，但应保留a)数据标题行，其中所有列均按原始顺序排列和b)至少一个数据行。 请勿手动添加任何数据。

         >[!NOTE]
         >
         > 最后一列必须包含非零值。

      2. 按开始日期升序对数据进行排序（从最早到最新）。

      3. 将工作表标签名称从&#39;&#39;更改[!UICONTROL Sheet1]从“ ”到“[!UICONTROL RAW]“

         此特定选项卡名称允许刷新数据。

      4. （可选）根据需要，在报表模板中的列右侧添加自定义列。

   1. （可选）在单独的工作表上创建一个数据透视表。 完成后，右键单击数据透视表的任意单元格并选择 **[!UICONTROL Pivot Table Options]**，单击 **[!UICONTROL Data]** 选项卡，然后选择 **[!UICONTROL Refresh data when opening the file]**.

   1. 将文件另存为 [!DNL Excel] .XLSX格式的电子表格。

>[!MORELIKETHIS]
>
>* [关于电子表格报表源](spreadsheet-feed-about.md)
>* [创建电子表格报表源](spreadsheet-feed-create.md)
>* [编辑电子表格报表馈送设置](spreadsheet-feed-edit.md)
>* [电子表格报表馈送设置](spreadsheet-feed-settings.md)
>* [查看或保存电子表格报表源文件](spreadsheet-feed-view-or-save.md)
>* [手动刷新电子表格报表馈送](spreadsheet-feed-refresh.md)
>* [删除电子表格报表源](spreadsheet-feed-delete.md)
