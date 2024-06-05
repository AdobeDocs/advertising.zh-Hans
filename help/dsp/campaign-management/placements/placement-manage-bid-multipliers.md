---
title: 管理投放位置的竞价乘数
description: 了解如何创建和编辑投放目标的竞价乘数。
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: 28f1b799daaa4e511abab1102a639e72b3a32d18
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# 管理投放位置的竞价乘数

您可以创建和管理竞价乘数，算法计算的竞价将乘以该乘数以增加或减少您的现有投放位置目标的竞价。 [符合条件的目标类型](#bid-multiplier-by-target). 您可以手动编辑一个版面的竞价倍增值，也可以上载具有一个或多个版面值的电子表格。

默认情况下，目标的竞价倍数为1.00，这意味着不针对该目标调整竞价。 值的范围可以是0.10到10.00。例如，0.5的竞价倍数将竞价6美元降至3美元(0.5 x 6)。 当拍卖符合多个竞价修饰符资格时，所有适用的竞价修饰符都将被相乘。 例如，如果加利福尼亚的竞价倍数为2，而旧金山的竞价倍数为3，则旧金山广告的最终竞价倍数为6。

>[!NOTE]
>
>竞价乘数从不将竞价提高到超过最高竞价。

您可以为设置竞价乘数（值为1.00以外的值） [目标数量有限](#bid-multiplier-limits-by-target).

此功能可与您现有的投放目标配合使用。 要更改投放位置的选定目标，请参阅&quot;[编辑版面](/help/dsp/campaign-management/placements/placement-edit.md)“

## 管理单个投放位置的竞价乘数

您可以手动编辑值或上传单个投放位置的电子表格。

1. 在主菜单中，单击 **[!UICONTROL Campaigns]**.

1. 单击营销活动的名称。

1. 在子菜单中，单击 **[!UICONTROL Placements]**.

1. 在版面名称旁边，单击  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. 调整合格目标的竞价乘数：

   * 要手动调整竞价倍增值，请移到每个 [目标特定选项卡](#bid-multiplier-by-target) ([!UICONTROL Geo]， [!UICONTROL Inventory]， [!UICONTROL Sites]， [!UICONTROL Audience]、和 [!UICONTROL Brand Safety])，并编辑投放目标的现有值。

     大多数目标类别在左侧列出子类别。 单击子类别以管理该子类别的竞价乘数（如果适用）。

   * 要上传具有竞价倍增值的CSV文件以覆盖所有现有值，请执行以下操作：

      1. 单击 **[!UICONTROL CSV File Edit]** 在右上角。

      1. a)单击 **[!UICONTROL Download Template]** 和编辑文件，或b)编辑之前下载的模板。 将编辑的文件保存到您的设备或网络。

         下载的电子表格中为每个目标类型（如国家/地区、来源和站点类别）包含一个工作表。 只包含值&lt; 1.0或> 1.0的现有竞价乘数。

         * 要为现有目标添加竞价乘数，请使用用户界面中显示的相同语法和对应的竞价乘数值输入目标。

         * 要删除竞价修饰符，请将竞价倍增值设置为1.0或删除行的所有信息。

         ![竞价乘数电子表格文件中的示例行](/help/dsp/assets/bid-multiplier-spreadsheet.png "竞价乘数电子表格文件中的示例行")

      1. 单击 **[!UICONTROL Next]** 以移至 [!UICONTROL Upload File] 部分，然后a)将编辑的文件拖放到框中，或b)在框中单击以从设备或网络中选择文件。

      1. 验证中已上传的数据 [!UICONTROL Review & Submit] 部分，然后单击 **[!UICONTROL Save]**.

## 上载一个或多个投放位置的竞价乘数

上载电子表格以将相同的值应用于所有选定的投放位置。

1. 在主菜单中，单击 **[!UICONTROL Campaigns]**.

1. 单击营销活动的名称。

1. 在子菜单中，单击 **[!UICONTROL Placements]**.

1. 选中要管理其竞价倍数的每个投放位置旁边的复选框。

1. 在批量操作工具栏中，单击 **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. 上载具有竞价乘数值的CSV文件以覆盖所有选定版面的所有现有值。

   1. a)单击 **[!UICONTROL Download Template]** 和编辑文件，或b)编辑之前下载的模板。 将编辑的文件保存到您的设备或网络。

      下载的电子表格中为每个目标类型（如国家/地区、来源和站点类别）包含一个工作表。 只包含值&lt; 1.0或> 1.0的现有竞价乘数。

      * 要为现有目标添加竞价乘数，请使用用户界面中显示的相同语法和对应的竞价乘数值输入目标。

      * 要删除竞价修饰符，请将竞价倍增值设置为1.0或删除行的所有信息。

      ![竞价乘数电子表格文件中的示例行](/help/dsp/assets/bid-multiplier-spreadsheet.png "竞价乘数电子表格文件中的示例行")

   1. 单击 **[!UICONTROL Next]** 以移至 [!UICONTROL Upload File] 部分，然后a)将编辑的文件拖放到框中，或b)在框中单击以从设备或网络中选择文件。

   1. 验证中已上传的数据 [!UICONTROL Review & Submit] 部分，然后单击 **[!UICONTROL Save]**.

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
