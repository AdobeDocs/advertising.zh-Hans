---
title: 指定私人交易的投放位置和广告
description: 了解如何将私人交易与额外的投放和广告结合使用。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 09119471-429d-413e-8033-e29e1558abb0
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# 指定私人交易的投放位置和广告

对于非保证交易，您可以从[!UICONTROL Placements]视图将交易指定为新投放位置的库存目标。

对于计划性保证(PG)交易，您可以从[!UICONTROL Deals]视图创建具有指定广告的投放位置。

您还可以随时[将广告](/help/dsp/campaign-management/ads/ad-attach-to-placement.md)附加到与PG和未保证交易关联的投放位置。

## 将非保证交易指定为投放的库存目标

* [从[!UICONTROL Placements]视图](/help/dsp/campaign-management/placements/placement-create.md)创建版面。 在[!UICONTROL Inventory Targeting]设置中，选择私人交易。

## 将投放位置和广告附加到PG交易

1. 在主菜单中，单击&#x200B;**[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. 在交易行中，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Attach New Placement]**。

1. 在[!UICONTROL Ad & Campaign Selection]设置中，选择要用于投放的广告：

       1. 选择广告商、营销活动和广告类型。 （可选）选择要按其筛选广告的广告状态。
       
       1。 从可用广告列表中，选中要用于交易的每个广告旁边的复选框。
       
       1。 单击**[!UICONTROL Apply]**.
   
   1. 在版面设置屏幕中：

      1. 输入版面名称。

      1. （可选）编辑[位置设置](/help/dsp/campaign-management/placements/placement-settings.md)，包括覆盖默认出价（自动使用交易中的CPM值填充默认出价）、更改日期范围或附加更多广告。

      交易会在“库存目标”部分自动定位。 所有其他定位选项均不适用。

      1. 单击&#x200B;**[!UICONTROL Create placement]**。

在发布者激活您的PG交易ID后，该投放位置将开始运行。

>[!NOTE]
>
> 您无需将交易标记发送给发布者进行验证。

>[!MORELIKETHIS]
>
>* [关于专用清单](private-inventory-about.md)
>* [列出私人交易的投放位置和广告](/help/dsp/inventory/private-deal-view-placements.md)
>* [手动创建交易ID详细信息](deal-id-create.md)
>* [手动交易ID设置](deal-id-settings.md)
>* [设置计划性保证交易](programmatic-guaranteed-set-up.md)
