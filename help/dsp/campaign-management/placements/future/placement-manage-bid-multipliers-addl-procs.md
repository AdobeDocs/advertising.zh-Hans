---
title: 管理投放位置的竞价乘数
description: 了解如何创建和编辑指定投放目标的竞价乘数。
feature: DSP Placements
source-git-commit: ae1a58bd0aed430cd2914146dfb2850bc8125025
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 0%

---

# 管理投放位置的竞价乘数


<!--

See if any of these procedures are implemented; may need to be edited and/or re-worded based on functionality/UI

-->

您可以使用此功能更改现有投放目标的竞价乘数。

要更改投放位置的选定目标，请参阅&quot;[编辑版面](/help/dsp/campaign-management/placements/placement-edit.md)“

## 管理一个或多个投放位置的竞价乘数

对于所有选定的投放位置，您可以手动编辑值或上载包含值的电子表格。

1. 在主菜单中，单击 **[!UICONTROL Campaigns]**.

1. 单击营销活动的名称。

1. 在子菜单中，单击 **[!UICONTROL Placements]**.

1. 选中要管理其竞价倍数的每个投放位置旁边的复选框。

1. 在批量操作工具栏中，单击 **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. 手动或上传包含目标值的CSV文件来调整符合条件的目标的竞价乘数：

   * 要手动调整竞价倍增值，请移至每个特定于目标的选项卡([!UICONTROL Geo]， [!UICONTROL Inventory]， [!UICONTROL Sites]， [!UICONTROL Audience]、和[!UICONTROL Brand Safety])，并编辑投放目标的现有值。

   将对所有选定投放位置进行相同的更改。

   * 要上载包含竞价乘数值并将覆盖现有值的CSV文件，请执行以下操作：

     >[!NOTE]
     >
     >如果将某个字段留空，则会删除该目标类型的所有值。<!-- Verify and re-word if needed. I'm not sure if you'll be able to have multiple data rows (one per placement) or if there will be only one data row applicable for all. -->

      1. 单击 **[!UICONTROL CSV Edit]** 在右上角。

      1. a)单击 **[!UICONTROL Download Template]** 和编辑竞价倍增值，或b)编辑以前下载的模板。 将编辑的文件保存到您的设备或网络。

      1. a)将编辑的文件拖放到框中，或b)单击框以从设备或网络中选择文件。

   1. 单击 **[!UICONTROL Upload]**.

   默认情况下，目标的竞价倍数为1.00，这意味着不为该目标调整竞价。 值的范围可以是0.10到10.00。例如，竞价修饰符0.5会将竞价从6美元降至3美元(0.5 x 6)。 您可以为设置竞价乘数（值为1.00以外的值） [目标数量有限](#bid-multiplier-limits-by-target).

   当拍卖符合多个竞价修饰符条件时，所有适用的竞价修饰符都将被相乘。

   竞价修饰符绝不会将竞价提高到超过最大竞价。

1. 单击 **[!UICONTROL Save]**.

-->

## 上传电子表格以管理单个投放位置的竞价乘数<!-- Is this still going to exist independently, or will you just do this via the "Bid Multiplier" option in the main context menu for placements? If both options, then reword headings for distinction -->

上传文件中的更改会覆盖现有的竞价倍增值。<!-- what if you delete a row? -->

1. 在主菜单中，单击 **[!UICONTROL Campaigns]**.

1. 单击营销活动的名称。

1. 在子菜单中，单击 **[!UICONTROL Placements]**.

1. 在版面名称旁边，单击  **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. 
   <!-- Verify the rest of these steps. -->

1. a)单击 **[!UICONTROL Download Template]** 和编辑竞价倍增值，或b)编辑以前下载的模板。 将编辑的文件保存到您的设备或网络。

   默认情况下，目标的竞价倍数为1.00，这意味着不为该目标调整竞价。 值的范围可以是0.10到10.00。例如，竞价修饰符0.5会将竞价从6美元降至3美元(0.5 x 6)。 您可以为设置竞价乘数（值为1.00以外的值） [目标数量有限](#bid-multiplier-limits-by-target).

   当拍卖符合多个竞价修饰符条件时，所有适用的竞价修饰符都将被相乘。

   竞价修饰符绝不会将竞价提高到超过最大竞价。

1. a)将编辑的文件拖放到框中，或b)单击框以从设备或网络中选择文件。

1. 单击 **[!UICONTROL Upload]**.

1. 单击 **[!UICONTROL Save]**.

## 符合竞价乘数资格的目标类型 {#bid-multiplier-by-target}

没有在这里上当

## 按目标类型划分的最大竞价乘数数 {#bid-multiplier-limits-by-target}

没有在这里上当

<!--

>[!MORELIKETHIS]
>
>* [About Placement Management](placement-about.md)
>* [Edit Placements](placement-edit.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Placement Settings](placement-settings.md)
 -->
