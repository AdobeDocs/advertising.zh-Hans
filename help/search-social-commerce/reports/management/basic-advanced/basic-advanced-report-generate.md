---
title: 生成基本报告或高级报告
description: 了解如何生成自定义的基本或高级报告。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# 生成基本报告或高级报告

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. 在数据表上方的工具栏中，单击 **[!UICONTROL Create Report]**，将光标悬停在上方 **[!UICONTROL Basic Reports]** 或 **[!UICONTROL Advanced Reports]**，然后单击 [报告类型](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md).

1. （可选）在 [!UICONTROL Report Settings] 窗口，更改默认值 [报告设置](basic-advanced-report-settings.md)：

   1. （可选）为报表和模板（如果将报表另存为模板）输入自定义名称。

   1. （可选）要将报表设置另存为模板，请选中旁边的复选框 **[!UICONTROL Save as template]**.

   1. （可选）在 **[!UICONTROL Basic Settings]** 选项卡中，选择要使用的现有报表模板或更改报表的默认基本设置。

   1. （可选）单击 **[!UICONTROL Columns tab]**，并更改报表中的默认列。

      默认情况下，报表中的所有货币数据均以美元的格式显示（如1,000.00）。 要以正确的货币格式显示值（但不包括CSV和TSV格式中的任何货币符号），请添加&quot;[!UICONTROL Currency]”列。 如果报表包含使用不同货币的帐户的数据，则为任意[!UICONTROL Total]“货币值是列中所有数字的总和，不考虑货币。

   1. (可选； [!UICONTROL Campaign Report]， [!UICONTROL Ad Group Report]， [!UICONTROL Ad Variation Report]， [!UICONTROL Keyword Report]、和 [!UICONTROL Label Classification Report] 仅限)单击 **[!UICONTROL Classifications]** 选项卡，并将报表结果限制为仅包含特定的标签分类。

   1. （可选）单击 **[!UICONTROL Advanced Filters]** 选项卡，并更改默认高级选项。

   1. （可选）单击 **[!UICONTROL Attribution]** 选项卡，并更改默认归因规则。

   1. （可选）单击 **[!UICONTROL Scheduling and Delivery]** 选项卡，并更改默认计划和提交选项。

1. （可用时可选）要预览报表的前50行，请单击 **[!UICONTROL Preview]**. 完成后，单击 **[!UICONTROL Back]** 以返回报表设置页面。

   >[!NOTE]
   >
   >“预览”按钮可用于所有基本报表和高级报表，但 [!UICONTROL Campaign Hourly Report]， [!UICONTROL Ad Variation Report]， [!UICONTROL Keyword Report]， [!UICONTROL Domain Referral Report]、和 [!UICONTROL Transaction Report].

1. 单击 **[!UICONTROL Create]**.

如果未指定报表计划，则报表将立即运行；否则，报表将按照指定的计划运行。 报表名称将添加到 [[!UICONTROL Latest Reports] 视图](/help/search-social-commerce/reports/report-about.md). 如果将报表另存为模板，则该模板也会添加到 [[!UICONTROL Templates] 视图](/help/search-social-commerce/reports/report-about.md). 报告完成时，文件可用于打开或保存；模板可立即使用。

如果您输入了通知的电子邮件地址，则当报告作业完成或失败时，每个收件人都会根据用户的 [已配置通知设置](/help/search-social-commerce/notifications/notification-edit.md) 用于报表。

>[!MORELIKETHIS]
>
>* [关于基本报表和高级报表](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [基本和高级报表设置](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [基本报表和高级报表的报表列](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md)
>* [删除报告](/help/search-social-commerce/reports/management/report-delete.md)

