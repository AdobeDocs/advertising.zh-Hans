---
title: 指定私人交易的投放位置和广告
description: 了解如何将私人交易与额外的投放和广告结合使用。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 09119471-429d-413e-8033-e29e1558abb0
TQID: https://experienceleague.adobe.com/ZCFqnc6cQLEqahDoElttE7DzeZCR3IRx2lkyyb3BPMs
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: ac506c20-96f2-48f6-9096-77706e336bdaid: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 3b9845e85cd91cdece195593b43cbaf851368f9e
workflow-type: tm+mt
source-wordcount: 275
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

   1. 从可用广告列表中，选中要用于交易的每个广告旁边的复选框。

   1. 单击&#x200B;**[!UICONTROL Apply]**。

1. 在版面设置屏幕中：

   1. 输入版面名称。

   1. （可选）编辑[位置设置](/help/dsp/campaign-management/placements/placement-settings.md)，包括覆盖默认竞价（自动使用交易中的CPM值填充默认竞价）、更改日期范围或附加更多广告。

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
