---
title: 编辑投放位置的广告计划
description: 了解如何更改附加到投放位置的广告的广告计划。
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
source-git-commit: a001d7fbde6ef1346383925db9179d824eb7bb78
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# 编辑投放位置的广告计划

## 编辑一个或多个投放的广告计划

您可以使用更改附加到多个投放位置的广告的计划投放日期和广告轮换 [!DNL Microsoft Excel] 电子表格。 每个广告都可以在多次飞行期间处于活动状态。

1. 在主菜单中，单击 **[!UICONTROL Campaigns]**.

1. 单击营销活动的名称。

1. 在子菜单中，单击 **[!UICONTROL Placements]**.

1. 选中要下载其广告数据的每个投放位置旁边的复选框。

1. 在批量操作工具栏中，单击 **[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]**.

1. 文件可用时，单击 **[!UICONTROL Download]** 在浏览器页面顶部的通知中，根据浏览器的正常过程下载工作表文件（XLSX格式）。

   ![下载就绪通知](/help/dsp/assets/download-ready.png "下载就绪通知")

1. 打开下载的文件，编辑要包含在航班中的每个广告行的航班信息字段，并保存更新的文件：

   * **[!UICONTROL Flight N Start Date]** / **[!UICONTROL Flight N End Date]** (例如 [!UICONTROL Flight 1 Start Date] 和 [!UICONTROL Flight 1 End Date])：航班的第一个日期和最后日期。 对各个日期使用YYYY-MM-DD格式。 任何包含空投放日期字段的广告都被视为非参与广告。

   * **[!UICONTROL Flight N Weight]** (例如 [!UICONTROL Flight 1 Weight])：如何旋转航班广告。 输入值：

      * 要平均旋转航班广告，请输入 `[!UICONTROL Even]`.

      * 要不均匀旋转投放的广告，请输入每个广告旋转的相对权重（百分比）。 航班的总重量必须等于100。

1. 上传已编辑的广告计划模板：

   1. 选中每个适用放置旁边的复选框。

   1. 在批量操作工具栏中，单击 **[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]**，并指定要上传的文件。

## 编辑单个投放的广告计划

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

您可以更改附加到投放位置的广告的计划投放日期和广告轮换。 每个广告都可以在多次飞行期间处于活动状态。

1. 在主菜单中，单击 **[!UICONTROL Campaigns]**.

1. 单击营销活动的名称。

1. 在子菜单中，单击 **[!UICONTROL Placements]**.

1. 在版面名称旁边，单击  **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]**.

   1. 执行以下任一操作：

      * 要添加航班，请单击 **[!UICONTROL Add Flight]**，然后指定开始日期和结束日期。

      * 要将现有航班添加到广告，请单击 **[!UICONTROL +]** 在投放栏的广告行中。

      * 要从广告中删除现有航班，请单击 **[!UICONTROL x]** 在投放栏的广告行中。

      * （当多个广告具有相同投放时间时）要不均匀旋转广告，请单击 **[!UICONTROL Even Rotation]** 在飞行信息中，然后输入每个广告旋转的相对权重（百分比）。

        总重量必须等于100。

   1. 在右上角，单击 **[!UICONTROL Continue]**.

   1. 查看航班详细信息，然后单击 **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [关于版面管理](placement-about.md)
>* [编辑投放位置](placement-edit.md)
>* [查看投放位置的更改日志](placement-change-log.md)
>* [投放设置](placement-settings.md)
