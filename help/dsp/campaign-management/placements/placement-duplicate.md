---
title: 复制投放位置
description: 了解如何复制一个或多个投放位置。
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
source-git-commit: ae1a58bd0aed430cd2914146dfb2850bc8125025
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# 复制投放位置

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

复制一个或多个投放位置以创建具有相似设置的投放位置。 您可以：

* 生成多个投放位置重复项
* 在原始广告商和营销策划中或不同广告商和营销策划中重复投放位置
* （对于原始营销活动中的重复投放位置）（可选）复制原始广告
* 修改新投放位置的状态和投放日期

有关未复制的版面设置列表，请参阅“[未复制的内容](#placement-not-duplicated)”。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 单击营销活动的名称。

1. 在子菜单中，单击&#x200B;**[!UICONTROL Placements]**。

1. 执行以下任一操作：

   * 要复制一个投放位置，请单击包名称旁边的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Duplicate]**。

   * 要复制多个投放位置，请执行以下操作：

      1. 选中每个要复制的放置旁边的复选框。

      1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Duplicate]**。

1. 指定新的版面设置：

   1. （单个版面）输入新版面名称。

   1. 在&#x200B;**[!UICONTROL Choose Package (Required)]**&#x200B;菜单中，选择父包或**[!UICONTROL No package]*。

   1. （可选）更改默认设置。

   这些设置适用于所有选定的投放位置。

   默认情况下，新投放位置适用于原始广告类型、分配给原始广告商和促销活动、具有从当天开始的航班时刻表、已暂停并且不包含原始广告。

   创建多个版面时，新版面名称将依次使用约定&lt;*original_placement_name #N*>附加一个数字，如“我的版面#2”。

1. 单击&#x200B;**[!UICONTROL Submit]**。

## 未复制的内容 {#placement-not-duplicated}

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
>* [关于版面管理](placement-about.md)
>* [创建版面](placement-create.md)
>* [编辑版面](placement-edit.md)
>* [查看投放位置的更改日志](placement-change-log.md)
>* [位置设置](placement-settings.md)
