---
title: 电子表格报表馈送设置
description: 了解电子表格馈送的设置。
exl-id: 88836c15-81fe-4fe7-8321-2c984b4dcb5d
feature: Search Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# 电子表格报表馈送设置

| 字段 | 描述 |
|---|---|
| [!UICONTROL Feed Name] | 电子表格馈送的名称。 |
| [!UICONTROL Report Template] | 指定所需报表数据的报表模板；选择用于创建[!DNL Excel]模板的报表模板。 将列出所有基本报表模板。<br><br><b>注意：</b>如果更改用于报表的报表模板，或者更新模板中的列，则必须创建并上传新的[!DNL Excel]模板。 |
| [!UICONTROL Excel Template] | 您以.XLSX格式创建的特别格式化的[!DNL Excel]模板，应用于报表模板中指定的数据。 通过输入完整路径和文件名或单击<b>[!UICONTROL Browse]</b>在设备或网络上查找文件来指定要上传的文件。 |
| [!UICONTROL Back Fill From] | [!UICONTROL RAW]选项卡上现有数据刷新的开始日期，用过去的天数表示。 输入一个最多90天的值；默认值为七(7)天。<br><br>例如，如果值为7，而今天为3月7日，则[!UICONTROL RAW]选项卡上从3月1日开始的现有数据将刷新（直到[!UICONTROL Back Fill Until]参数指定的结束日期）。 不会删除3月1日之前日期的现有数据行，但不会刷新这些行。 |
| [!UICONTROL Back Fill Until] | [!UICONTROL RAW]选项卡上现有数据刷新的结束日期，用过去的天数表示。 默认值为一(1)天。<br><br>例如，如果此值为1，今天为3月7日，则[!UICONTROL RAW]选项卡上的现有数据将刷新到3月6日（并且从[!UICONTROL Back Fill From]参数指定的开始日期开始）。 如果此值为1，[!UICONTROL Back Fill Until]参数为7，而今天为3月7日，则[!UICONTROL RAW]选项卡上的现有数据将从3月1日至3月6日刷新。 在这两个示例中，不会删除3月6日之后日期的现有数据行，但不会刷新这些行。 |
| [!UICONTROL Email Recipients] | 每次刷新报告时或每次运行报告时发送通知的电子邮件地址（当模板包含计划时）。 默认情况下，会输入用户帐户的地址。 要指定多个地址，请用逗号、空格或新行分隔它们。 |
| [!UICONTROL Schedule Time] | 刷新电子表格馈送的时间：08:00或在广告商时区的10:00到23:00之间的任何时间。 新电子表格馈送的默认值为10:00。<br><br><b>注意：</b>出于性能考虑，生成其他报表时不能在09:00刷新电子表格馈送。 |
| [!UICONTROL Email Notification] | （当指定电子邮件收件人时）要包含在发送给任何指定地址的电子邮件通知中的内容：<ul><li><i>附加馈送</i>  — 以XLSX格式发送已完成报表的副本。 如果文件大于10 MB，则通知不包含附件。</li><li><i>仅通知</i>（默认） — 仅发送报告完成或失败的通知，其中包含指向报告的链接。</li></ul> |

>[!MORELIKETHIS]
>
>* [关于电子表格报表馈送](spreadsheet-feed-about.md)
>* [创建电子表格报表源](spreadsheet-feed-create.md)
>* [为电子表格报表馈送创建 [!DNL Excel] 模板](spreadsheet-feed-create-excel-template.md)
>* [编辑电子表格报表源设置](spreadsheet-feed-edit.md)
>* [查看或保存电子表格报表源文件](spreadsheet-feed-view-or-save.md)
>* [手动刷新电子表格报表馈送](spreadsheet-feed-refresh.md)
>* [删除电子表格报表馈送](spreadsheet-feed-delete.md)
