---
title: 生成基本报表或高级报表
description: 了解如何生成自定义的基本或高级报表。
exl-id: 529a35f5-517f-4bde-b752-c0afc6346f4b
feature: Search Reports, Search Basic Reports, Search Advanced Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# 生成基本报表或高级报表

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Create Report]**，将光标悬停在&#x200B;**[!UICONTROL Basic Reports]**&#x200B;或&#x200B;**[!UICONTROL Advanced Reports]**&#x200B;上，然后单击[报告类型](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)。

1. （可选）在[!UICONTROL Report Settings]窗口中，更改默认[报表设置](basic-advanced-report-settings.md)：

   1. （可选）为报表和模板（如果将报表另存为模板）输入自定义名称。

   1. （可选）要将报表设置另存为模板，请选中&#x200B;**[!UICONTROL Save as template]**&#x200B;旁边的复选框。

   1. （可选）在&#x200B;**[!UICONTROL Basic Settings]**&#x200B;选项卡上，选择要使用的现有报表模板或更改报表的默认基本设置。

   1. （可选）单击&#x200B;**[!UICONTROL Columns tab]**，然后更改报表中的默认列。

      默认情况下，报表中的所有货币数据均以美元的格式显示（如1,000.00）。 要以正确的货币格式显示值（但不包括CSV和TSV格式中的任何货币符号），请向报表中添加“[!UICONTROL Currency]”列。 如果报表包含使用不同货币的帐户的数据，则任何“[!UICONTROL Total]”货币值都是列中所有数字的总和，而不考虑货币。

   1. （可选；[!UICONTROL Campaign Report]、[!UICONTROL Ad Group Report]、[!UICONTROL Ad Variation Report]、[!UICONTROL Keyword Report]和[!UICONTROL Label Classification Report]）单击&#x200B;**[!UICONTROL Classifications]**&#x200B;选项卡，并将报告结果限制为仅包含特定的标签分类。

   1. （可选）单击&#x200B;**[!UICONTROL Advanced Filters]**&#x200B;选项卡，然后更改默认高级选项。

   1. （可选）单击&#x200B;**[!UICONTROL Attribution]**&#x200B;选项卡，然后更改默认归因规则。

   1. （可选）单击&#x200B;**[!UICONTROL Scheduling and Delivery]**&#x200B;选项卡，然后更改默认计划和提交选项。

1. （可用时可选）要预览报表的前50行，请单击&#x200B;**[!UICONTROL Preview]**。 完成后，单击&#x200B;**[!UICONTROL Back]**&#x200B;以返回报表设置页面。

   >[!NOTE]
   >
   >除[!UICONTROL Campaign Hourly Report]、[!UICONTROL Ad Variation Report]、[!UICONTROL Keyword Report]、[!UICONTROL Domain Referral Report]和[!UICONTROL Transaction Report]之外，预览按钮可用于所有基本报表和高级报表。

1. 单击&#x200B;**[!UICONTROL Create]**。

如果未指定报表计划，则报表将立即运行；否则，报表将按照指定的计划运行。 报告名称已添加到[[!UICONTROL Latest Reports]视图](/help/search-social-commerce/reports/report-about.md)。 如果将报表另存为模板，则它也会添加到[[!UICONTROL Templates]视图](/help/search-social-commerce/reports/report-about.md)中。 报告完成时，文件可用于打开或保存；模板可立即使用。

如果您输入了通知的电子邮件地址，则当报告作业完成或失败时，每个收件人都会根据用户为报告配置的[通知设置](/help/search-social-commerce/notifications/notification-edit.md)收到通知。

>[!MORELIKETHIS]
>
>* [关于基本和高级报告](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [基本和高级报告设置](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [基本和高级报告的报告列](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md)
>* [删除报告](/help/search-social-commerce/reports/management/report-delete.md)
