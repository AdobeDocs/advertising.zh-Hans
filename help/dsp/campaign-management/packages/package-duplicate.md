---
title: 复制资源包
description: 了解如何复制资源包。
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# 复制资源包

复制资源包以创建具有类似设置的资源包。 您可以：

* 在原始广告商和营销策划中或在不同的广告商和营销策划中复制资源包
* （可选）复制包中的版面
* （对于原始营销活动中重复的包）（可选）复制原始广告和位置级别的事件像素
* 修改新包的发送日期

请参阅“[未复制的内容](#package-not-duplicated)“ ”，查看未复制的版面设置列表。

1. 在主菜单中，单击 **[!UICONTROL Campaigns]**.

1. 单击营销活动的名称以打开 [!UICONTROL Packages] 中。

1. 在包名称旁边，单击  **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. 指定新包设置：

   1. 输入新包名称。

   1. （可选）更改默认设置。

      默认情况下：

      * 新资源包已分配给原始广告商和营销活动。

      * 新资源包在当天变为活动状态。<!-- and the flight continues for NN  days. -->

      * 原始资源包中的版面将会复制到新资源包中。

      * 广告和位置级别的事件像素将不会复制到新包中。

1. 单击 **[!UICONTROL Submit]**.

## 未复制的内容 {#package-not-duplicated}

原始版面中的所有设置都会复制，但以下各项除外：

* 实验设置
* （如果更改投放日期）自定义广告计划
* （如果不附加广告）自定义广告权重和计划
* 程序化保证(PG)交易的默认版面和 [!UICONTROL Simple Ad Serving] 交易
* （如果您将版面复制到其他营销活动）：
   * 地域目标
   * 事件像素
   * 广告
   * 版面级别 [!DNL DoubleVerify Authentic Brand Safety] 区段（覆盖广告商级别的区段）

>[!MORELIKETHIS]
>
>* [关于包管理](package-about.md)
>* [创建资源包](package-create.md)
>* [编辑资源包](package-edit.md)
>* [查看包的更改日志](package-change-log.md)
>* [包设置](package-settings.md)

