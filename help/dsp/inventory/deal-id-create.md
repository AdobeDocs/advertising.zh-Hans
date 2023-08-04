---
title: 手动创建交易ID详细信息
description: 了解如何手动输入交易ID的详细信息。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 20a57919-c68f-4c9d-a8e1-f49484f74655
source-git-commit: 60676d8ef022d2ed61467d7254405695d5f106b3
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---

# 手动创建交易ID详细信息

1. 在主菜单中，单击 **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. 在数据表的上方，单击 **[!UICONTROL Create]**，然后选择 **[!UICONTROL Deal ID]**.

1. 输入 [交易设置](deal-id-settings.md)：

   1. 在 [!UICONTROL Deal ID basics] 部分，指定交易详细信息和能够访问交易的广告商。 对于保证交易，您还必须指定计划的投放日期和预计展示次数，仅用于跟踪目的。

      您可以通过在“库存”>“交易”视图中包含“PG展示步调”支出列来跟踪保证交易的步调。

   1. （仅限管理员用户；可选）在 [!UICONTROL Technical] 部分，根据需要编辑默认设置。

   1. 单击 **[!UICONTROL Save]**.

1. （仅限保证交易）选择要用于交易的广告（或发布者管理的广告的1x1像素），并创建默认的程序化保证(PG)投放位置。

   默认PG投放位置可确保您的交易始终返回每个竞价请求的竞价。 如果您没有创建默认的PG投放，则任何以交易为目标的投放都不会投标，除非设置正确。 您应始终创建默认的PG投放位置。 在 [!UICONTROL Placements] 视图，默认PG投放具有 [!UICONTROL Sub-type] “”的列值[!UICONTROL PG Default]“

   您可以选择将交易用作其他投放位置的库存目标，但必须正确设置它们才能投标。

   1. 在 [!UICONTROL Ad & Campaign Selection] 设置，选择将用于交易的广告：

      1. 选择广告商、营销活动和广告类型。 （可选）选择要按其筛选广告的广告状态。

      1. 从可用广告列表中，选中要用于交易的每个广告旁边的复选框。

      1. 对于出版商管理的广告，在选择了广告商和促销活动后，将自动应用1x1跟踪像素。

      1. 单击 **[!UICONTROL Apply]**.

   1. 在版面设置屏幕中：

      1. 输入版面名称。

      1. （可选）编辑 [投放设置](/help/dsp/campaign-management/placements/placement-settings.md)，包括覆盖默认竞价（自动使用交易中的CPM值填充）；更改日期范围；或附加更多广告。

      交易会在“库存目标”部分自动定位。 所有其他定位选项均不适用。

      1. 单击 **[!UICONTROL Create placement]**.

创建交易后，您可以将交易用作多个投放位置的库存目标。

>[!NOTE]
>
> 您无需将交易标记发送给发布者进行验证。

>[!TIP]
>
>* 在 [!UICONTROL Inventory] > [!UICONTROL Deals] 视图， [!UICONTROL Pacing & Budget] 列显示了交易如何步调到指定的投放日期和展示目标。
>
>* 如果投放速度不佳或超速，请与您的出版商联系以调整通过交易发送的数量。

>[!MORELIKETHIS]
>
>* [手动交易标识设置](deal-id-settings.md)
>* [设置计划性保证交易](programmatic-guaranteed-set-up.md)
>* [提交计划性保证交易的广告 [!DNL FreeWheel]](freewheel-submit.md)
>* [关于程序化保证交易](programmatic-guaranteed-about.md)
<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->
