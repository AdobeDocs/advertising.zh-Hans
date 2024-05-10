---
title: 手动同步广告网络数据
description: 了解如何为支持的广告网络手动触发营销活动结构和营销活动实体的同步。
exl-id: 185c6a01-c2e8-4bbb-a9dd-0a8200eb4792
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# 手动同步广告网络数据

*[!DNL Google Ads]， [!DNL Microsoft Advertising] (以前称为 [!DNL Bing Ads])， [!DNL Yahoo! Japan Ads]， [!DNL Yandex]，并且现有 [!DNL Baidu] 仅限帐户*

同步是Search、Social和Commerce收集每个广告商的已连接广告网络帐户的最新信息的过程。 [支持的广告网络](/help/search-social-commerce/introduction/supported-inventory.md). 此数据包括广告商的营销活动结构和营销活动实体，包括其在“搜索”、“社交”和“Commerce”中管理或报告的大多数属性。 它不包括点击数据，也不包括在搜索、社交和Commerce之外输入的竞价和竞价修饰符，这些数据是单独收集的。

Search、Social和Commerce每天与您的广告网络帐户自动同步（同步）一次，每次检测到您的某个广告网络上有新促销活动时也是如此。 此外，它还会立即将从Search、Social和Commerce内对促销活动数据所做的所有更改发送到广告网络。

您可以手动请求同步指定帐户或特定活动和暂停营销活动中的所有活动和暂停营销活动。 此任务会收集广告网络中新增或已更改的实体。

对于具有&quot;[!UICONTROL Auto Upload]”选项时，同步操作还会生成并发布跟踪模板或目标URL中缺少或需要更改的跟踪代码。 URL是根据帐户设置或营销策划的跟踪设置中的参数生成的。 如果相关项目存在跟踪URL，则不会重新生成这些URL，除非需要新的URL（例如，如果关键词匹配类型、创意文本或帐户的跟踪参数已更改）。

>[!NOTE]
>
>任何时候 [创建批量工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)，您可以选择在创建批量处理工作表之前与广告网络同步。

1. 在主菜单中，单击 **[!UICONTROL Search]>[!UICONTROL Campaigns]**. 在子菜单中，选择 **[!UICONTROL Accounts]** 同步特定帐户中的所有促销活动，或者 **[!UICONTROL Campaigns]** 以同步特定营销活动。

1. （可选）筛选列表以包含特定帐户或营销活动。

1. 选中要同步的每个帐户或营销活动旁边的复选框。 一次最多可以同步50个营销活动。 如果一次同步超过五个帐户，则该作业将划分为多个批次，每个批次最多包含五个帐户。

1. 单击 **![更多](/help/search-social-commerce/assets/more.png "更多")** 工具栏中的，然后选择 **[!UICONTROL Sync]**.

您可以关注中同步作业的状态 [!UICONTROL Workspace] 视图。 作业可能需要一个小时或更长时间才能显示。

>[!MORELIKETHIS]
>
>* [下载/创建批量处理工作表文件](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
