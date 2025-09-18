---
title: 编辑投放位置的广告计划
description: 了解如何更改附加到投放位置的广告的广告计划。
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
source-git-commit: 18c68edec80a80d236df138c05fba8d857c9ed9e
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# 编辑投放位置的广告计划

## 编辑一个或多个投放的广告计划

您可以使用[!DNL Microsoft Excel]电子表格更改附加到多个投放位置的广告的计划投放日期和广告轮换。 每个广告都可以在多次飞行期间处于活动状态。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 单击营销活动的名称。

1. 在子菜单中，单击&#x200B;**[!UICONTROL Placements]**。

1. 选中要下载其广告数据的每个投放位置旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]**。

1. 文件可用时，单击浏览器页面顶部通知中的&#x200B;**[!UICONTROL Download]**，按照浏览器的正常过程下载工作表文件（XLSX格式）。

   ![下载就绪通知](/help/dsp/assets/download-ready.png "下载就绪通知")

1. 打开下载的文件，编辑要包含在航班中的每个广告行的航班信息字段，并保存更新的文件：

   * **[!UICONTROL Flight N Start Date]** / **[!UICONTROL Flight N End Date]** （如[!UICONTROL Flight 1 Start Date]和[!UICONTROL Flight 1 End Date]）：航班的第一个和最后一个日期。 对各个日期使用YYYY-MM-DD格式。 任何包含空投放日期字段的广告都被视为非参与广告。

   * **[!UICONTROL Flight N Weight]** （如[!UICONTROL Flight 1 Weight]）：如何旋转航班广告。 输入值：

      * 要平均旋转航班广告，请输入`[!UICONTROL Even]`。

      * 要不均匀旋转航班广告，请输入每个广告旋转的相对权重，以百分比表示（如`40`表示40%）。 航班的总重量必须等于100。

1. 上传已编辑的广告计划模板：

   1. 选中每个适用放置旁边的复选框。

   1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]**，然后指定要上传的文件。

## 编辑单个投放的广告计划

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

您可以更改附加到投放位置的广告的计划投放日期和广告轮换。 每个广告都可以在多次飞行期间处于活动状态。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 单击营销活动的名称。

1. 在子菜单中，单击&#x200B;**[!UICONTROL Placements]**。

1. 在投放位置名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Ads]** > **[!UICONTROL Ad schedule]**。

1. 执行以下任一操作：

   * 要添加航班，请单击&#x200B;**[!UICONTROL Add Flight]**，然后指定开始日期和结束日期。

   * 要将现有航班添加到广告，请单击航班列的广告行中的&#x200B;**[!UICONTROL +]**。

   * 要从广告中删除现有航班，请单击航班列的广告行中的&#x200B;**[!UICONTROL x]**。

      * （当多个广告具有相同的飞行时）要不均匀旋转广告，请在飞行信息中单击&#x200B;**[!UICONTROL Even Rotation]**，然后输入旋转每个广告的相对权重（百分比）。

        总重量必须等于100。

1. 单击右上角的&#x200B;**[!UICONTROL Continue]**。

1. 查看航班详细信息，然后单击&#x200B;**[!UICONTROL Save & Finish]**。

>[!MORELIKETHIS]
>
>* [关于版面管理](placement-about.md)
>* [编辑版面](placement-edit.md)
>* [查看投放位置的更改日志](placement-change-log.md)
>* [位置设置](placement-settings.md)
