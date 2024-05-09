---
title: 创建投放位置
description: 了解如何创建投放位置。
feature: DSP Placements
exl-id: 28a328b1-0839-442e-a245-f586a7042f41
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# 创建投放位置

>[!TIP]
>
>根据特定的活动目标或报告需求创建投放位置。

1. 在主菜单中，单击 **[!UICONTROL Campaigns]**.

1. 单击要包含投放位置的营销活动的名称。

1. 在数据表的上方，单击 **[!UICONTROL Create]**. 在 [!UICONTROL Placement Types] 在菜单的部分中，单击放置类型。

   投放位置类型确定投放位置可包含的广告类型。

1. 输入 [投放设置](placement-settings.md)：

   1. 指定 [!UICONTROL Placement Basics] 设置。

   1. 在 [!UICONTROL Goals] 部分，指定 [!UICONTROL Gross Budget] 和（可选）指定其他放置目标。

      某些字段具有可以覆盖的默认值。

      如果为版面分配了程序包具有程序包级别的步调，则您的目标和步调设置将反映程序包设置。

   1. （可选）在 [!UICONTROL Geo-Targeting] 部分，缩小包含或排除的位置。

      如果您不识别特定位置，则会定位所有位置。

      >[!NOTE]
      >
      >城市和DMA位置不适用于Roku投放。

   1. 在 [!UICONTROL Inventory Targeting] 部分，缩小要包含或排除的清单源。

      对于大多数置入类型，默认情况下包括所有库存类型以及每种类型的所有来源。 对象 [!DNL Roku] 投放位置，您必须指定库存类型和来源。

   1. （可选）在 [!UICONTROL Site Targeting] 部分，缩小要定位的站点，并指定要排除的任何站点。

   1. （可选）在 [!UICONTROL Audience Targeting] 部分：

      1. 缩小受众范围。 这包括选择要在投放位置中定位的受众区段。

         对象 [!DNL Roku] 投放位置，您可以利用 [DSP独特受众匹配对象 [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) 添加一个或多个可与 [!DNL Roku] （选择启用）确定性数据集。

      1. （对于具有人员级别跨设备定位的营销活动；可选）当投放位置面向一个或多个特定受众时，请为投放位置启用基于人员的跨设备定位。

         基于人员的跨设备定位由以下人员提供 [!DNL LiveRamp] 仅使用美国数据。 所有广告商都可使用此服务，其CPM价格为$0.35，这样便可通过使用 [!DNL LiveRamp] 设备图（即，对于在目标受众区段中未找到设备的设备）。

   1. （可选）在 [!DNL Brand Safety and Media Targeting] 部分，对投放位置应用品牌安全限制。

   1. （可选）在 [!DNL Tracking] 部分，为投放位置中的广告输入第三方事件像素或转化像素。

      >[!NOTE]
      >
      >([!DNL Roku] 投放)第三方像素供应商已获批准 [!DNL Roku] include [!DNL Acxiom]， [!DNL comScore]， [!DNL Data Plus Math]， [!DNL Experian]， [!DNL Factual]， [!DNL Kantar]， [!DNL Marketing Evolution]， [!DNL Neustar]， [!DNL Nielsen]， [!DNL Nielsen Catalina Solutions]， [!DNL NinthDecimal]， [!DNL Oracle]， [!DNL Placed]， [!DNL Polk]、和 [!DNL Research Now].

1. 单击 **[!UICONTROL Create Placement]**.

1. （可选）将广告附加到投放位置：

   1. 单击 **[!UICONTROL Attach an ad]**.

   1. 执行以下任一操作：

      * 要创建新广告：

         1. 单击 **[!UICONTROL Create a New Ad].**

         1. 指定广告设置 [音频广告](/help/dsp/campaign-management/ads/ad-settings-audio.md)， [已连接电视](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)， [展示广告](/help/dsp/campaign-management/ads/ad-settings-display.md)， [移动广告](/help/dsp/campaign-management/ads/ad-settings-mobile.md)， [原生广告](/help/dsp/campaign-management/ads/ad-settings-native.md)， [前置广告](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)，或 [通用视频广告](/help/dsp/campaign-management/ads/ad-settings-universal-video.md).

        >[!NOTE]
        >
        >通用视频投放位置只能包含通用视频广告。

         1. 单击 **[!UICONTROL Save & Submit for Review]**.

         1. （可选）对于要为投放位置创建的每个其他广告，单击 **[!UICONTROL Attach Another Ad]**，然后重复步骤1-3。

         1. 如果不附加任何现有广告，请单击 **[!UICONTROL I'm done for now]**.

      * 要在营销活动中附加现有广告，请执行以下操作：

      1. 单击 **[!UICONTROL Select an Ad]**.

      1. 执行以下任一操作：

         * 要一次添加一个广告，请执行以下操作：

            1. 在广告名称旁边，单击 **[!UICONTROL Select].**

            1. （可选）对于要附加的每个其他广告，单击 **[!UICONTROL Attach Another Ad]**，然后重复该过程。

         * 要一次最多添加20个广告，请执行以下操作：

            1. 选中广告列表上方的复选框。

            1. 选中要添加的每个广告旁边的复选框。

            1. 单击 **[!UICONTROL Attach]**.

            1. 在广告名称旁边，单击 **[!UICONTROL Select]**.

      1. （可选）要覆盖投放位置中特定广告的默认投放期限和广告轮换，请执行以下操作：

         1. 单击 **[!UICONTROL Custom Schedule Ads]**.

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
>* [编辑版面](placement-edit.md)
>* [管理投放位置的竞价乘数](placement-manage-bid-multipliers.md)
>* [编辑投放的广告计划](placement-edit-ad-schedule.md)
>* [暂停或激活投放位置](placement-pause-activate.md)
>* [查看投放位置的更改日志](placement-change-log.md)
>* [投放设置](placement-settings.md)
>* [查看职位安排预测报表](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [关于通用视频的常见问题解答](/help/dsp/campaign-management/faq-universal-video.md)
>* [键盘快捷键](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [性能疑难解答](/help/dsp/optimization/troubleshooting-performance.md)
>* [视频：如何创建标准展示投放位置](https://video.tv.adobe.com/v/340454)
