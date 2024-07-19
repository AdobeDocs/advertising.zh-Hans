---
title: 生成 [!DNL Advertising Insight]
description: 了解如何创建 [!DNL Advertising Insight]。
exl-id: e6b692be-189e-4c6c-a536-e6c78801853d
feature: Search Advertising Insights
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# 生成[!DNL Advertising Insight]

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]**。

2. 单击要生成的分析。

3. 指定分析设置：

   1. （某些报表；可选）指定分析的日期范围。

   2. （大部分见解）选择要分析的项目组合。

      通常，包含有效营销活动的所有优化和有效的项目组合均可用。 对于某些见解，可筛选项目组合列表以包含&#x200B;**[!UICONTROL Only Optimized Portfolios]**。

      对于[!UICONTROL Day of Week]分析，只有具有足够支出以及在过去两天中还支出到目标的项目组合才可用。

   3. （仅限[!UICONTROL Event Path Beta]分析）执行以下操作：

      1. 选择&#x200B;**[!UICONTROL Operation]**： *[!UICONTROL Extract events]* （上传一个[!UICONTROL Channel Assist Report]或[!UICONTROL Campaign Assist Report]并将用户事件分类为不同的组以供分析）或&#x200B;*[!UICONTROL Analyze classified events]* （上传事件组并使用它们生成见解）。

      1. 单击&#x200B;**[!UICONTROL Select]**&#x200B;以找到XLSX和ZIP（压缩XLSX）格式的文件，然后单击&#x200B;**[!UICONTROL Upload]**。

   4. （仅限[!UICONTROL Google Account Audit]分析）执行以下操作：

      1. 输入&#x200B;**[!UICONTROL Advertiser Name]**&#x200B;和&#x200B;**[!UICONTROL Account Name]**。

      1. 选择&#x200B;**[!UICONTROL Account Currency]**、**[!UICONTROL File Format Region]** （*[!UICONTROL United States]*&#x200B;或&#x200B;*[!UICONTROL United Kingdom]*）和&#x200B;**[!UICONTROL Output Language]** （*[!UICONTROL English (USA)]*、*[!UICONTROL French]*&#x200B;或&#x200B;*[!UICONTROL German]*）。

      1. 单击&#x200B;**[!UICONTROL Select]**&#x200B;以查找从[!DNL Google Ads] Web用户界面为帐户下载的促销活动、关键字和更改历史记录报告，以及从[!DNL Google Ads Editor]应用程序为帐户下载的批量处理工作表文件。 然后单击&#x200B;**[!UICONTROL Upload]**。

         所有文件都必须采用CSV、TSV、TXT或ZIP（压缩的CSV、TSV或TXT）格式。

   5. （仅限[!UICONTROL Location Target Performance]分析；可选）要每天聚合数据而不是作为摘要，请选择&#x200B;*[!UICONTROL Daily]*&#x200B;的&#x200B;**[!UICONTROL Time Aggregation]**。

   6. （仅限[!UICONTROL Normalized Sim (Combined)]分析）执行以下操作：

      1. 在&#x200B;**[!UICONTROL Step]**&#x200B;字段中，指定要包括在分析中的目标支出级别或步骤数。 该值可以在三(3)到100之间。

      1. 在&#x200B;**[!UICONTROL Type]**&#x200B;字段中，选择模拟类型：

         * *[!UICONTROL Optimized Multi-portfolio]*：对具有相同目标和货币的多个项目组合生成单个模拟。

         * *[!UICONTROL Individual Normalized]*：为每个选定的项目组合生成单个模拟。 投资组合可能具有不同的目标和货币。

   7. （仅限[!UICONTROL Portfolio Launch]分析；可选）若要指定以后的启动日期，请在&#x200B;**[!UICONTROL Optional Date]**&#x200B;字段中指定日期。

   8. （仅限[!UICONTROL Quality Score]分析）选择适用的广告网络。

   9. （仅限[!UICONTROL Query Cross Matching]分析）在&#x200B;**[!UICONTROL Google Accounts]**&#x200B;菜单中，选择帐户。

4. 单击&#x200B;**[!UICONTROL Generate Insight]**。

   当作业完成或失败时，您将根据[为[!UICONTROL Advertising Insights]配置的通知设置](/help/search-social-commerce/notifications/notification-edit.md)接收通知。

>[!MORELIKETHIS]
>
>* [关于[!UICONTROL Advertising Insights]](insight-about.md)
>* [查看或保存 [!DNL Advertising Insight]](insight-view-save.md)
>* [删除 [!DNL Advertising Insight]](insight-delete.md)
