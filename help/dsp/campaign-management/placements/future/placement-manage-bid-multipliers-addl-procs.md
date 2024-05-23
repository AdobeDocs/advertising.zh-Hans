---
title: 管理投放位置的竞价乘数
description: 了解xxx
feature: DSP Placements
source-git-commit: c0dd18a3ce8759214813b7303c590a28febf1b37
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# XXX

## 管理单个投放位置的竞价乘数

1. 在主菜单中，单击 **[!UICONTROL Campaigns]**.

1. 单击营销活动的名称。

1. 在子菜单中，单击 **[!UICONTROL Placements]**.

1. 在版面名称旁边，单击  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. 调整合格目标的竞价乘数：

   * 要手动调整竞价倍增值，请移到每个 [目标特定选项卡](#bid-multiplier-by-target) ([!UICONTROL Geo]， [!UICONTROL Inventory]， [!UICONTROL Sites]， [!UICONTROL Audience]、和 [!UICONTROL Brand Safety])，并编辑投放目标的现有值。

     大多数目标类别在左侧列出子类别。 单击子类别以管理该子类别的竞价乘数（如果适用）。

   * 要上传具有竞价倍增值的CSV文件以覆盖所有现有值，请执行以下操作：

      1. 单击 **[!UICONTROL CSV File Edit]** 在右上角。

      1. a)单击 **[!UICONTROL Download Template]** 和编辑文件，或b)编辑以前下载的模板。 将编辑的文件保存到您的设备或网络。

         下载的电子表格中为每个目标类型（如国家/地区、来源和站点类别）包含一个工作表。 只包含值&lt; 1.0或> 1.0的现有竞价乘数。

         * 要为现有目标添加竞价乘数，请使用用户界面中显示的相同语法和对应的竞价乘数值输入目标。

         * 要删除竞价修饰符，请将竞价倍增值设置为1.0或删除行的所有信息。

         ![竞价乘数电子表格文件中的示例行](/help/dsp/assets/bid-multiplier-spreadsheet.png "竞价乘数电子表格文件中的示例行")

      1. 单击 **[!UICONTROL Next]** 以移至 [!UICONTROL Upload File] 部分，然后a)将编辑的文件拖放到框中，或b)在框中单击以从设备或网络中选择文件。

      1. 验证中已上传的数据 [!UICONTROL Review & Submit] 部分，然后单击 **[!UICONTROL Save]**.

## 管理一个或多个投放位置的竞价乘数

<!-- verify all and edit accordingly -->

1. 在主菜单中，单击 **[!UICONTROL Campaigns]**.

1. 单击营销活动的名称。

1. 在子菜单中，单击 **[!UICONTROL Placements]**.

1. 选中要管理其竞价倍数的每个投放位置旁边的复选框。

1. 在批量操作工具栏中，单击 **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

<!-- Check the following this functionality when available in UAT -->

1. 调整合格目标的竞价乘数：

   * 要手动调整竞价倍增值，请移至每个特定于目标的选项卡([!UICONTROL Geo]， [!UICONTROL Inventory]， [!UICONTROL Sites]， [!UICONTROL Audience]、和[!UICONTROL Brand Safety])，并编辑投放目标的现有值。

   相同的更改适用于所有选定的投放位置。

* 要上传具有竞价倍增值的CSV文件以覆盖所有现有值，请执行以下操作：

   1. 单击 **[!UICONTROL CSV File Edit]** 在右上角。

   1. a)单击 **[!UICONTROL Download Template]** 和编辑文件，或b)编辑以前下载的模板。 将编辑的文件保存到您的设备或网络。

      下载的电子表格中为每个目标类型（如国家/地区、来源和站点类别）包含一个工作表。 只包含值&lt; 1.0或> 1.0的现有竞价乘数。

      * 要为现有目标添加竞价乘数，请使用用户界面中显示的相同语法和对应的竞价乘数值输入目标。

      * 要删除竞价修饰符，请将竞价倍增值设置为1.0或删除行的所有信息。

      ![竞价乘数电子表格文件中的示例行](/help/dsp/assets/bid-multiplier-spreadsheet.png "竞价乘数电子表格文件中的示例行")

   1. 单击 **[!UICONTROL CSV Edit]** 在右上角。

   1. a)单击 **[!UICONTROL Download Template]** 和编辑竞价倍增值，或b)编辑以前下载的模板。 将编辑的文件保存到您的设备或网络。

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
