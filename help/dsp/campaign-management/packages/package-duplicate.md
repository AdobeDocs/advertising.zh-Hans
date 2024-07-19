---
title: 复制包
description: 了解如何复制包。
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '246'
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

>[!MORELIKETHIS]
>
>* [关于包管理](package-about.md)
>* [创建包](package-create.md)
>* [编辑包](package-edit.md)
>* [查看包的更改日志](package-change-log.md)
>* [包设置](package-settings.md)
