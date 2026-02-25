---
title: （新用户界面）手动同步广告网络数据
description: 了解如何从新UI手动触发受支持广告网络的营销活动结构和营销活动实体的同步。
feature: Search Campaign Management
source-git-commit: 5e384445a35f81275eefeac660b31c1acdc785f3
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# （新用户界面）通过API连接手动同步广告网络数据

<!-- EDIT ALL -- FROM LEGACY UI -->

仅&#x200B;*[!DNL Google Ads]、[!DNL Microsoft Advertising]（以前为[!DNL Bing Ads]）、[!DNL Yahoo! Japan Ads]、[!DNL Yandex]和现有[!DNL Baidu]帐户*

同步是Search、Social和Commerce收集[支持的广告网络](/help/search-social-commerce/introduction/supported-inventory.md)上每个广告商连接的广告网络帐户的更新信息的过程。 此数据包括广告商的营销活动结构和营销活动实体，包括其在“搜索”、“社交”和“Commerce”中管理或报告的大多数属性。 它不包括点击数据，也不包括在搜索、社交和Commerce之外输入的竞价和竞价修饰符，这些数据是单独收集的。

Search、Social和Commerce每天与您的广告网络帐户自动同步（同步）一次，每次检测到您的某个广告网络上有新促销活动时也是如此。 此外，它还会立即将从Search、Social和Commerce内对促销活动数据所做的所有更改发送到广告网络。

您可以手动请求同步指定帐户<!--Not available as of 2/23:  or in specific active and paused campaigns -->中的所有活动和暂停的营销活动。 此任务会收集广告网络中新增或已更改的实体。

对于具有“[!UICONTROL Auto Update]”选项的营销活动，同步操作还会生成并发布跟踪模板或目标URL中缺失或需要更改的跟踪代码。 URL是根据帐户设置或营销策划的跟踪设置中的参数生成的。 如果相关项目存在跟踪URL，则不会重新生成这些URL，除非需要新的URL（例如，如果关键词匹配类型、创意文本或帐户的跟踪参数已更改）。

>[!NOTE]
>
>每当[创建批量处理工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)时，您都可以选择在创建批量处理工作表之前与广告网络同步。

## 同步广告网络帐户中的营销活动

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 选中帐户名旁边的复选框。

   <!-- As of 2/23, you can sync only one acct at a time:  Select the check box next to each account or campaign that you want to sync. You can sync up to 50 campaigns at a time. If you sync more than five accounts at a time, the job is broken into batches of up to five accounts each. -->

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL ... More Actions]** > **[!UICONTROL Sync]**。

   * 将光标放在帐户名称上，单击&#x200B;**...**，然后单击&#x200B;**[!UICONTROL Edit]**。

您可以在[!UICONTROL Workspace]视图中跟踪同步作业的状态。 作业可能需要
一小时或更长时间。

>[!MORELIKETHIS]
>
>* [下载/创建批量处理工作表文件](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
