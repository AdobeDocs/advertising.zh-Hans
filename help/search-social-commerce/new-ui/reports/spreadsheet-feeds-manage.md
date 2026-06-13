---
title: （新UI）管理电子表格报表源
description: 了解如何创建、配置、刷新、查看和删除以自定义格式电子表格形式提供每日性能数据的电子表格报表馈送。
feature: Search Reports
source-git-commit: 38ee8dfbaf82d8f1d212a931956398444e61060f
workflow-type: tm+mt
source-wordcount: '1492'
ht-degree: 0%

---

# （新UI）管理电子表格报表源

*仅用于基本报告和模型准确性报告*

<!-- Update link to notifications once available -->

电子表格馈送以[!DNL Microsoft Excel] XLSX中的自定义电子表格格式为所有基本报表和模型准确性报表提供每日性能数据。 您可以使用从常规报表模板创建的特定格式的[!DNL Excel]电子表格模板来设置电子表格馈送。 每天，电子表格都会在指定的时间自动刷新，并包含每天汇总的新原始数据。 原始数据会填充电子表格模板中包含的任何列和图形。 在电子表格馈送文件可用或文件生成失败后，报表模板中的每个电子邮件收件人会根据用户为报表](/help/search-social-commerce/notifications/notification-about.md)配置的[通知设置接收通知。

您可以将馈送配置为刷新最近90天的数据，并且所有以前现有的数据都会继续累积。

[!UICONTROL Reports] > [!UICONTROL Spreadsheets Feeds]视图列出了您创建的所有电子表格馈送。 在此视图中，您可以创建电子表格馈送、手动刷新馈送或删除馈送。

## 可用操作

* [为电子表格报表源创建 [!DNL Excel] 模板](#spreadsheet-feed-create-excel-template)

* [创建电子表格报表源](#spreadsheet-feed-create)

* [编辑电子表格报表馈送设置](#spreadsheet-feed-edit)

* [查看或保存电子表格报表源文件](#spreadsheet-feed-view-or-save)

* [手动刷新电子表格报表馈送](#spreadsheet-feed-refresh)

* [删除电子表格报表源](#spreadsheet-feed-delete)

## 为电子表格报表源创建[!DNL Excel]模板 {#spreadsheet-feed-create-excel-template}

<!-- Add x-refs when available -->

要创建电子表格馈送，您必须首先使用常规报表模板创建特别格式化的[!DNL Microsoft Excel]电子表格模板。 您可以选择自定义[!DNL Excel]电子表格以包含其他列和图。

1. 在&#x200B;**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**&#x200B;中，使用“[!UICONTROL Daily]”的[!UICONTROL Date Aggregation]单位并使用所有其他所需的数据参数生成所需的报告类型，并将报告另存为模板。

   >[!NOTE]
   >
   > * 您可以为[!UICONTROL Portfolio]、[!UICONTROL Search Engine]、[!UICONTROL Search Engine Account]、[!UICONTROL Campaign]、[!UICONTROL Ad Group]、[!UICONTROL Ad Variation]、[!UICONTROL Keyword]和[!UICONTROL Forecast Accuracy]报告创建电子表格馈送。 如果使用[!UICONTROL Ad Group Report]，请限制包含的广告组数，以便更快地获得结果。
   > * 未使用模板中定义的[!UICONTROL Date Range]单位。 稍后配置电子表格馈送时，您将定义刷新数据的日期。

1. 生成报告后，转到&#x200B;**[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**&#x200B;并将报告输出的TSV或XLS版本导出到文件。

1. 在[!DNL Excel]中，为报告创建自定义模板：

   1. 在[!DNL Excel]中打开报告文件。

   1. 准备工作簿：

      1. 删除显示报表参数的顶行。 对于XLS文件，也删除“[!UICONTROL Total]”行。 您可以选择删除某些数据行，但应保留a)数据标题行，其中所有列均按原始顺序排列和b)至少一个数据行。 请勿手动添加任何数据。

         >[!NOTE]
         >
         > 最后一列必须包含非零值。

      1. 按开始日期升序对数据进行排序（从最早到最新）。

      1. 将工作表选项卡名称从“[!UICONTROL Sheet1]”更改为“[!UICONTROL RAW]”。

         此特定选项卡名称允许刷新数据。

      1. （可选）根据需要，在报表模板中的列右侧添加自定义列。

   1. （可选）在单独的工作表上创建一个数据透视表。 完成后，右键单击数据透视表的任意单元格并选择&#x200B;**[!UICONTROL Pivot Table Options]**，单击&#x200B;**[!UICONTROL Data]**&#x200B;选项卡，然后选择&#x200B;**[!UICONTROL Refresh data when opening the file]**。

   1. 将文件另存为.XLSX格式的[!DNL Excel]电子表格。

## 创建电子表格报表源 {#spreadsheet-feed-create}

1. [创建 [!DNL Excel] 模板以使用报表数据填充](#spreadsheet-feed-create-excel-template)。

1. 创建电子表格信息源：

   1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**。

   1. 单击右上角的&#x200B;**[!UICONTROL Create Spreadsheet]**。

   1. 在&#x200B;**[!UICONTROL Create Spreadsheet Feed]**&#x200B;对话框中，指定[电子表格馈送设置](#spreadsheet-feed-settings)。

   1. 单击&#x200B;**[!UICONTROL Submit]**。

   1. （可选）信息源的[!UICONTROL Update Status]为&#x200B;*[!UICONTROL Finished]*&#x200B;后，单击信息源旁边的&#x200B;**[!UICONTROL XLSX]**，然后按照浏览器的正常过程打开或保存文件。

      >[!NOTE]
      >
      >如果稍后删除与信息源关联的报表模板，则也会删除信息源。

      电子表格馈送在每天配置的[!UICONTROL Schedule Time]自动刷新。 如果报表模板包含任何电子邮件收件人的地址，则这些地址会在电子表格刷新后接收通知。

## 编辑电子表格报表馈送设置 {#spreadsheet-feed-edit}

>[!NOTE]
>
> 如果您编辑报表模板中的列，或者使用新的或更新后的报表模板，则必须相应地更新[!DNL Excel]模板并重新上传。

1. （可选）要更新用于电子表格馈送的报表模板或[!DNL Excel]模板：

   * （可选）若要为信息源使用其他或更新的报表模板，请[为报表模板](#spreadsheet-feed-create-excel-template)创建新的 [!DNL Excel] 模板。

     您将在后续步骤中上载报表模板和新的[!DNL Excel]文件。

   * （可选）要简单地向[!DNL Excel]模板添加自定义列，请在报表模板中列的右侧插入列，然后将该文件另存为.XLSX格式的[!DNL Excel]电子表格。 您需要在下一步中上传新的[!DNL Excel]文件。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**。

1. 更改电子表格馈送设置：

   1. 选中电子表格馈送名称旁边的复选框。

   1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Edit]**。

   1. 在[!UICONTROL Create Spreadsheet Feed]<!-- sic -->对话框中，更改[电子表格馈送设置](#spreadsheet-feed-settings)。

   1. 单击&#x200B;**[!UICONTROL Submit]**。

   1. （可选）信息源的[!UICONTROL Update Status]为&#x200B;*[!UICONTROL Finished]*&#x200B;后，单击信息源旁边的&#x200B;**[!UICONTROL XLSX]**，然后按照浏览器的正常过程打开或保存文件。

   >[!NOTE]
   >
   > 如果稍后删除与信息源关联的报表模板，则也会删除信息源。

   电子表格馈送在广告商所在时区的每天的08:00自动刷新。 如果报表模板包含任何电子邮件收件人的地址，则这些地址会在电子表格刷新后接收通知。

## 电子表格报表馈送设置 {#spreadsheet-feed-settings}

| 字段 | 描述 |
|---|---|
| [!UICONTROL Feed Name] | 电子表格馈送的名称。 |
| [!UICONTROL Report Template] | 指定所需报表数据的报表模板；选择用于创建[!DNL Excel]模板的报表模板。 列出了所有基本报告模板。<br><br><b>注意：</b>如果更改用于该报告的报告模板，或更新该模板中的列，则必须创建并上载新的[!DNL Excel]模板。 |
| [!UICONTROL Excel Template] | 您以.XLSX格式创建的特别格式化的[!DNL Excel]模板，应用于报表模板中指定的数据。 通过输入完整路径和文件名或单击<b>[!UICONTROL Browse]</b>在设备或网络上查找文件来指定要上传的文件。 |
| [!UICONTROL Back Fill From] | [!UICONTROL RAW]选项卡上现有数据刷新的开始日期，用过去的天数表示。 输入一个最多90天的值；默认值为七(7)天。<br><br>例如，如果值为7，而今天为3月7日，则[!UICONTROL RAW]选项卡上从3月1日开始的现有数据将刷新（直到[!UICONTROL Back Fill Until]参数指定的结束日期）。 不会删除3月1日之前日期的现有数据行，但不会刷新这些行。 |
| [!UICONTROL Back Fill Until] | [!UICONTROL RAW]选项卡上现有数据刷新的结束日期，用过去的天数表示。 默认值为一(1)天。<br><br>例如，如果此值为1，今天为3月7日，则[!UICONTROL RAW]选项卡上的现有数据将刷新到3月6日（并且从[!UICONTROL Back Fill From]参数指定的开始日期开始）。 如果此值为1，[!UICONTROL Back Fill Until]参数为7，而今天为3月7日，则[!UICONTROL RAW]选项卡上的现有数据将从3月1日至3月6日刷新。 在这两个示例中，不会删除3月6日之后日期的现有数据行，但不会刷新这些行。 |
| [!UICONTROL Email Recipients] | 每次刷新报告时或每次运行报告时发送通知的电子邮件地址（当模板包含计划时）。 默认情况下，会输入用户帐户的地址。 要指定多个地址，请用逗号、空格或新行分隔它们。 |
| [!UICONTROL Schedule Time] | 刷新电子表格馈送的时间：在08:00或在广告商时区的10:00到23:00之间的任何时间。 新电子表格馈送的默认值为10:00。<br><br><b>注意：</b>出于性能考虑，当生成其他报表时，您无法在09:00刷新电子表格馈送。 |
| [!UICONTROL Email Notification] | （当指定电子邮件收件人时）要包含在发送给任何指定地址的电子邮件通知中的内容：<ul><li><i>[!UICONTROL Attach feed]</i>  — 以XLSX格式发送已完成报表的副本。 如果文件大于10 MB，则通知不包含附件。</li><li><i>[!UICONTROL Notification Only]</i> （默认） — 仅发送报告完成或失败的通知，其中包含指向报告的链接。</li></ul> |

## 查看或保存电子表格报表源文件 {#spreadsheet-feed-view-or-save}

您可以查看任何生成的电子表格馈送或将其保存到文件。 电子表格馈送文件为[!DNL Microsoft Excel] XLSX格式。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**。

1. 单击信息源旁边的&#x200B;**[!UICONTROL XLSX]**，然后按照浏览器的正常过程打开或保存该文件。

## 手动刷新电子表格报表馈送 {#spreadsheet-feed-refresh}

>[!NOTE]
>
>电子表格馈送将在本地时区的每天08:00自动刷新。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**。

1. 选中要刷新的每个馈送旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Run Spreadsheet]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。

1. （可选）在信息源的[!UICONTROL Update Status]为&#x200B;*[!UICONTROL Finished]*&#x200B;后，单击该信息源旁边的&#x200B;**[!UICONTROL XLSX]**，然后按照浏览器的正常过程打开或保存文件。

## 删除电子表格报表源 {#spreadsheet-feed-delete}

>[!NOTE]
>
>如果删除了与馈送关联的报表模板，则会自动删除馈送。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**。

1. 选中要删除的每个馈送旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。
