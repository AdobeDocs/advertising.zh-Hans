---
title: 复制营销活动
description: 了解如何复制营销活动。
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
source-git-commit: 4085c1b21c0fe84653978e449321868921841367
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# 复制营销活动

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

复制营销活动以使用类似设置创建新营销活动。 您可以：

* 为原始广告商或其他广告商复制营销活动
* （可选）复制原始包和投放位置
* 修改新营销活动的投放日期

有关未复制的版面设置列表，请参阅“[未复制的内容](#campaign-not-duplicated)”。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 在营销活动名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Duplicate]**。

1. 指定新的Campaign设置：

   1. 输入新的营销活动名称和结束投放日期。

   1. （可选）更改默认设置。

      默认情况下，新促销活动会分配给原始广告商，其航班时刻表从当天开始，并包括原始包和投放位置。

1. 单击&#x200B;**[!UICONTROL Submit]**。

## 未复制的内容 {#campaign-not-duplicated}

原始投放位置中的所有设置都将重复，但以下情况除外：

* 试验设置
* （如果更改投放日期）自定义广告计划
* （如果不附加广告）自定义广告权重和计划
* [!UICONTROL Simple Ad Serving]个交易的计划性保证(PG)交易的默认投放位置和投放位置
* （如果将投放位置复制到其他营销活动）：
   * 地理目标
   * 事件像素
   * 广告
   * 位置级别[!DNL DoubleVerify Authentic Brand Safety]区段（覆盖广告商级别区段）

>[!MORELIKETHIS]
>
>* [关于Campaign Management](campaign-about.md)
>* [创建营销活动](campaign-create.md)
>* [编辑营销活动](campaign-edit.md)
>* [查看营销活动的更改日志](campaign-change-log.md)
>* [营销活动设置](campaign-settings.md)
