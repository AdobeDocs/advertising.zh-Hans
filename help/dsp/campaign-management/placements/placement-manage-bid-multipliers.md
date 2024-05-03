---
title: 管理投放位置的竞价乘数
description: 了解如何创建和编辑指定投放目标的竞价乘数。
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: ae1a58bd0aed430cd2914146dfb2850bc8125025
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 3%

---

# 管理投放位置的竞价乘数

您可以使用此功能更改现有投放目标的竞价乘数。 您可以一次管理一个投放位置的竞价乘数。<!-- remove that line once we can edit multiple -->

要更改投放位置的选定目标，请参阅&quot;[编辑版面](/help/dsp/campaign-management/placements/placement-edit.md)“

<!-- 
## Manage the Bid Multipliers for a Single Placement
-->

1. 在主菜单中，单击 **[!UICONTROL Campaigns]**.

1. 单击营销活动的名称。

1. 在子菜单中，单击 **[!UICONTROL Placements]**.

1. 在版面名称旁边，单击  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. 移到每个 [目标特定选项卡](#bid-multiplier-by-target) ([!UICONTROL Geo]， [!UICONTROL Inventory]， [!UICONTROL Sites]， [!UICONTROL Audience]、和 [!UICONTROL Brand Safety])，并编辑投放目标的现有值。 大多数目标类别在左侧列出子类别。 单击子类别以管理该子类别的竞价乘数（如果适用）。

   默认情况下，目标的竞价倍数为1.00，这意味着不为该目标调整竞价。 值的范围可以是0.10到10.00。例如，竞价修饰符0.5会将竞价从6美元降至3美元(0.5 x 6)。 竞价修饰符绝不会将竞价提高到超过最大竞价。

   当拍卖符合多个竞价修饰符条件时，所有适用的竞价修饰符都将被相乘。

   您可以为设置竞价乘数（值为1.00以外的值） [目标数量有限](#bid-multiplier-limits-by-target).

1. 在右上角，单击 **[!UICONTROL Save]**.

## 符合竞价乘数资格的目标类型 {#bid-multiplier-by-target}

您只能为包括的目标配置竞价修饰符，而不能为排除的目标配置竞价修饰符。

* **地理目标**：地理位置（国家/地区、州和城市）、邮政编码和DMA

* **清单目标**：公共清单和的源及信息源 [!UICONTROL On Demand] 库存

* **站点目标：** 目标（但未排除）站点/应用程序、站点类别

* **受众目标：** 区段、时段、主题

* **ads.txt目标：** （当您选择退出ads.txt时，这允许您从所有销售者处购买库存）ads.txt仅销售者、ads.txt直接销售者和ads.txt销售者以及没有ads.txt的网站 <!-- bid multipliers for the different subsets of inventory; not available when the placement targets only one subset -->

## 按目标类型划分的最大竞价乘数数 {#bid-multiplier-limits-by-target}

您可以为有限数量的目标设置竞价乘数（值为1.00以外的值）。 例如，您最多可以为20个国家/地区目标设置竞价乘数。 下面列出了每种目标类型可以具有竞价倍数的最大目标数。

| 类别 | 参数 | 最大数量 |
| -------- | --------- | ----- |
| 地域 | 国家/地区 | 20 |
| 地域 | 状态 | 100 |
| 地域 | 城市 | 100 |
| 地域 | Metro | 100 |
| 地域 | 邮政编码 | 100 |
| 库存 | 源 | 100 |
| 库存 | 信息源 | 100 |
| 站点 | 站点类别 | 100 |
| 站点 | 站点/应用程序 | 100 |
| 受众 | 区段 | 500 |
| 受众 | 主题 | 100 |
| 品牌安全 | Ads.txt | 不适用 |

>[!MORELIKETHIS]
>
>* [关于版面管理](placement-about.md)
>* [编辑版面](placement-edit.md)
>* [查看投放位置的更改日志](placement-change-log.md)
>* [投放设置](placement-settings.md)
