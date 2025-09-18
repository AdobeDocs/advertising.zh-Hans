---
title: 创建投放位置
description: 了解如何创建投放位置。
feature: DSP Placements
exl-id: 28a328b1-0839-442e-a245-f586a7042f41
source-git-commit: 18c68edec80a80d236df138c05fba8d857c9ed9e
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 0%

---

# 创建投放位置

>[!TIP]
>
>根据特定的活动目标或报告需求创建投放位置。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 单击要包含投放位置的营销活动的名称。

1. 在数据表上方，单击&#x200B;**[!UICONTROL Create]**。 在菜单的[!UICONTROL Placement Types]部分中，单击投放位置类型。

   投放位置类型确定投放位置可包含的广告类型。

1. 输入[位置设置](placement-settings.md)：

   1. 指定[!UICONTROL Placement Basics]设置。

   1. 在[!UICONTROL Goals]部分中，指定[!UICONTROL Gross Budget]，并（可选）指定其他放置目标。

      某些字段具有可以覆盖的默认值。

      如果为版面分配了程序包具有程序包级别的步调，则您的目标和步调设置将反映程序包设置。

   1. （可选）在[!UICONTROL Geo-Targeting]部分中，缩小包含或排除的位置。

      如果您不识别特定位置，则会定位所有位置。

      >[!NOTE]
      >
      >城市和DMA位置不适用于Roku投放。

   1. 在[!UICONTROL Inventory Targeting]部分中，缩小要包含或排除的清单源。

      对于大多数置入类型，默认情况下包括所有库存类型以及每种类型的所有来源。 对于[!DNL Roku]投放位置，必须指定库存类型和源。

   1. （可选）在[!UICONTROL Site Targeting]部分中，缩小要定位的站点范围，并指定要排除的任何站点。

   1. （可选）在[!UICONTROL Audience Targeting]部分中：

      1. 缩小受众范围。 这包括选择要在投放位置中定位的受众区段。

         对于[!DNL Roku]投放位置，您可以通过包含一个或多个可与[（选择启用）确定性数据集匹配的受众区段，来利用 [!DNL Roku]](/help/dsp/inventory/roku-inventory.md)DSP与[!DNL Roku]的唯一受众匹配。

         未附加到活动、计划或暂停放置的第一方RampID区段将被暂停。 该区段在区段列表中标记为“自动暂停”。

      1. （对于具有人员级别跨设备定位的营销活动；可选）当投放位置面向一个或多个特定受众时，请为投放位置启用基于人员的跨设备定位。

         [!DNL LiveRamp]仅使用美国数据提供了基于人员的跨设备定位。 所有广告商都可在CPM上使用该服务，其价格为$0.35，借助于[!DNL LiveRamp]设备图提供的展示次数（即在目标受众区段中未找到设备）。

   1. （可选）在[!DNL Brand Safety and Media Targeting]部分中，对投放位置应用品牌安全限制。

   1. （可选）在[!DNL Tracking]部分中，为投放位置中的广告输入第三方事件像素或转化像素。

      >[!NOTE]
      >
      >（[!DNL Roku]个投放位置） [!DNL Roku]批准的第三方像素供应商包括[!DNL Acxiom]、[!DNL Comscore]、[!DNL Data Plus Math]、[!DNL Experian]、[!DNL Factual]、[!DNL Kantar]、[!DNL Marketing Evolution]、[!DNL Neustar]、[!DNL Nielsen]、[!DNL Nielsen Catalina Solutions]、[!DNL NinthDecimal]、[!DNL Oracle]、[!DNL Placed]、[!DNL Polk]和[!DNL Research Now]。

1. 单击&#x200B;**[!UICONTROL Create Placement]**。

1. （可选）将广告附加到投放位置：

   1. 单击&#x200B;**[!UICONTROL Attach an ad]**。

   1. 执行以下任一操作：

      * 要创建新广告：

         1. 单击&#x200B;**[!UICONTROL Create a New Ad].**

         1. 指定[音频广告](/help/dsp/campaign-management/ads/ad-settings-audio.md)、[连接的电视](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)、[显示广告](/help/dsp/campaign-management/ads/ad-settings-display.md)、[移动广告](/help/dsp/campaign-management/ads/ad-settings-mobile.md)、[原生广告](/help/dsp/campaign-management/ads/ad-settings-native.md)、[前置广告](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)或[通用视频广告](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)的广告设置。

        >[!NOTE]
        >
        >通用视频投放位置只能包含通用视频广告。

         1. 单击&#x200B;**[!UICONTROL Save & Submit for Review]**。

         1. （可选）对于要为投放位置创建的每个其他广告，单击&#x200B;**[!UICONTROL Attach Another Ad]**，然后重复步骤1-3。

         1. 如果您不打算附加任何现有广告，请单击&#x200B;**[!UICONTROL I'm done for now]**。

      * 要在营销活动中附加现有广告，请执行以下操作：

         1. 单击&#x200B;**[!UICONTROL Select an Ad]**。

         1. 执行以下任一操作：

            * 要一次添加一个广告，请执行以下操作：

               1. 在广告名称旁边，单击&#x200B;**[!UICONTROL Select]。**

               1. （可选）对于要附加的每个其他广告，单击&#x200B;**[!UICONTROL Attach Another Ad]**，然后重复该过程。

            * 要一次最多添加20个广告，请执行以下操作：

               1. 选中广告列表上方的复选框。

               1. 选中要添加的每个广告旁边的复选框。

               1. 单击&#x200B;**[!UICONTROL Attach]**。

               1. 在广告名称旁边，单击&#x200B;**[!UICONTROL Select]**。

         1. （可选）要覆盖投放位置中特定广告的默认投放期限和广告轮换，请执行以下操作：

            1. 单击&#x200B;**[!UICONTROL Custom Schedule Ads]**。

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
>* [管理投放位置的竞价乘数](placement-manage-bid-multipliers.md)
>* [编辑投放位置的广告计划](placement-edit-ad-schedule.md)
>* [停用或激活投放位置](placement-pause-activate.md)
>* [查看投放位置的更改日志](placement-change-log.md)
>* [位置设置](placement-settings.md)
>* [查看投放预测报告](/help/dsp/campaign-management/reports/placement-forecast.md)
>* 有关通用视频的[常见问题解答](/help/dsp/campaign-management/faq-universal-video.md)
>* [键盘快捷键](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [性能疑难解答](/help/dsp/optimization/troubleshooting-performance.md)
>* [视频：如何创建标准展示投放位置](https://video.tv.adobe.com/v/344997?captions=chi_hans)
