---
title: 生成 [!DNL Advertising Insight]
description: 了解如何创建 [!DNL Advertising Insight].
exl-id: 242095c9-25f0-4954-b1a8-5ea3db312afd
feature: Search Advertising Insights
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# 生成 [!DNL Advertising Insight]

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]**.

2. 单击要生成的分析。

3. 指定分析设置：

   1. （某些报表；可选）指定分析的日期范围。

   2. （大部分见解）选择要分析的项目组合。

      通常，包含有效营销活动的所有优化和有效的项目组合均可用。 对于某些见解，您可以筛选项目组合列表以包含 **[!UICONTROL Only Optimized Portfolios]**.

      对象 [!UICONTROL Day of Week] 只有具有足够支出以及在过去两天中还用于定位的项目组合才能获得洞察。

   3. ([!UICONTROL Event Path Beta] 仅限分析)执行以下操作：

      1. 选择 **[!UICONTROL Operation]**： *[!UICONTROL Extract events]* (上传 [!UICONTROL Channel Assist Report] 或 [!UICONTROL Campaign Assist Report] 并将用户事件分类为不同的组以供分析)或 *[!UICONTROL Analyze classified events]* （上传事件组并使用它们生成洞察）。

      1. 单击 **[!UICONTROL Select]** 找到采用XLSX和ZIP（压缩XLSX）格式的文件，然后单击 **[!UICONTROL Upload]**.

   4. ([!UICONTROL Google Account Audit] 仅限分析)执行以下操作：

      1. 输入 **[!UICONTROL Advertiser Name]** 和 **[!UICONTROL Account Name]**.

      1. 选择 **[!UICONTROL Account Currency]**， **[!UICONTROL File Format Region]** (*[!UICONTROL United States]* 或 *[!UICONTROL United Kingdom]*)，以及 **[!UICONTROL Output Language]** (*[!UICONTROL English (USA)]*， *[!UICONTROL French]*，或 *[!UICONTROL German]*)。

      1. 单击 **[!UICONTROL Select]** 要查找从中为帐户下载的促销活动、关键字和更改历史记录报表，请执行以下操作： [!DNL Google Ads] web用户界面以及从下载的帐户批量工作表文件 [!DNL Google Ads Editor] 应用程序。 然后单击 **[!UICONTROL Upload]**.

         所有文件都必须采用CSV、TSV、TXT或ZIP（压缩的CSV、TSV或TXT）格式。

   5. ([!UICONTROL Location Target Performance] 仅限洞察；可选)要每天聚合数据而非作为摘要，请选择 **[!UICONTROL Time Aggregation]** 之 *[!UICONTROL Daily]*.

   6. ([!UICONTROL Normalized Sim (Combined)] 仅限分析)执行以下操作：

      1. 在 **[!UICONTROL Step]** 字段，指定要包括在分析中的目标支出级别或步骤数。 该值可以在三(3)到100之间。

      1. 在 **[!UICONTROL Type]** 字段中，选择模拟类型：

         * *[!UICONTROL Optimized Multi-portfolio]*：使用相同的目标和货币跨多个项目组合生成单个模拟。

         * *[!UICONTROL Individual Normalized]*：为每个选定的项目组合生成单个模拟。 投资组合可能具有不同的目标和货币。

   7. ([!UICONTROL Portfolio Launch] 仅限分析；可选)要指定以后的启动日期，请在 **[!UICONTROL Optional Date]** 字段。

   8. ([!UICONTROL Quality Score] 仅限分析)选择适用的广告网络。

   9. ([!UICONTROL Query Cross Matching] 仅限洞察)在 **[!UICONTROL Google Accounts]** 菜单中，选择帐户。

4. 单击 **[!UICONTROL Generate Insight]**.

   当作业完成或失败时，您将根据您的 [已配置通知设置](/help/search-social-commerce/notifications/notification-edit.md) 对象 [!UICONTROL Advertising Insights].

>[!MORELIKETHIS]
>
>* [关于 [!UICONTROL Advertising Insights]](insight-about.md)
>* [查看或保存 [!DNL Advertising Insight]](insight-view-save.md)
>* [删除 [!DNL Advertising Insight]](insight-delete.md)
