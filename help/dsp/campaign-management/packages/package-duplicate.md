---
title: 复制包
description: 了解如何复制包。
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
source-git-commit: 1fe0d3c026cac52104d54b571fd9c2202cc2384b
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# 复制包

复制包以创建具有类似设置的包。 您可以：

* 在原始广告商和营销策划中或不同的广告商和营销策划中复制包

* （可选）复制包中的投放位置

* （对于原始营销活动中的重复资源包）（可选）重复原始广告和投放级别的事件像素

* 修改新包的投放日期

有关未复制的版面设置列表，请参阅“[未复制的内容](#package-not-duplicated)”。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 单击营销活动的名称以打开[!UICONTROL Packages]视图。

1. 在包名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Duplicate]**。

1. 指定新的包设置：

   1. 输入新包名称。

   1. （可选）更改默认设置。

      默认情况下：

      * 新包将分配给原始广告商和营销策划。

      * 新包将在当天变为活动状态。<!-- and the flight continues for NN  days. -->

      * 原始包中的版面将复制到新包中。

      * 广告和投放位置级别事件像素将不会复制到新包。

1. 单击&#x200B;**[!UICONTROL Submit]**。

## 未复制的内容 {#package-not-duplicated}

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

## 配置新包的最佳实践

>[!TIP]
>
>* 使用批量处理工作表可以[一次对多个营销活动组件进行更改](/help/dsp/campaign-management/campaign-components-review-edit.md)。
>* 使用广告标签页来[上传多个第三方广告](/help/dsp/campaign-management/ads/ad-create-multiple.md)。

* 暂停新包，直到您准备好激活它。

* 请考虑以下事项，并根据需要编辑新包：

   * 该账户是否有足够的资金满足新的一揽子预算？

   * 新方案是否需要与上一个方案不同的预算？

   * 上传创意内容（包括任何必要的自定义广告权重和计划），并将它们附加到投放位置。

   * 根据需要将事件像素附加到投放位置和广告。

   * 包括投放所需的地理目标和投放级别[!DNL DoubleVerify Authentic Brand Safety]区段。

   * 对于程序化保证交易，使用新交易ID并创建默认投放位置。

   * 根据需要为[!UICONTROL Simple Ad Serving]个交易创建新投放位置。

* 对于使用自定义优化目标的包，请使用每个包的[[!UICONTROL Linked Package for Optimization Learnings Carryover]设置](/help/dsp/campaign-management/packages/package-settings.md)，以使用上一个营销活动的历史数据作为优化包的输入。

>[!MORELIKETHIS]
>
>* [关于包管理](package-about.md)
>* [创建包](package-create.md)
>* [编辑包](package-edit.md)
>* [查看包的更改日志](package-change-log.md)
>* [包设置](package-settings.md)
