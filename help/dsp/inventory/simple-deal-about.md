---
title: 关于[!UICONTROL Simple Ad Serving]
description: 了解使用事件跟踪像素的[!UICONTROL Simple Ad Serving]交易。
feature: DSP Simple Ad Serving
exl-id: 327a2c93-d729-42e1-856f-f0e05efab7ca
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# 关于[!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving]使用单个专用投放位置，为指定发布者和单个广告类型提供有保障、未决策的广告投放和报告。 当您的出版商无法通过交易ID执行您的交易时，请使用[!DNL Simple Ad Serving]。 所有定位、预算步调和上限以及频率上限均由发布者处理。 通过事件跟踪像素执行这些交易。

通过使用[!UICONTROL Simple Ad Serving]，每个广告都由发布者（站点服务器）直接提供，DSP提供了一个事件跟踪像素以发送给发布者，发布者必须实施该像素并流量DSP广告。 根据库存类型，事件像素测量展示次数、点进次数和视频播放事件。

可以使用以下广告类型：

* 桌面标准前置式广告
* 平板电脑和移动设备标准前置广告
* 已连接的电视标准前置式广告
* 显示
* 音频

您可以在[!UICONTROL Inventory] > [!UICONTROL Deals]视图中创建[!UICONTROL Simple Ad Serving]交易。 DSP会自动为广告生成子类型为“[!DNL Simple ad serving]”的版面。 投放位置以交易为目标，但不允许额外的定位、预算或频率上限。 您只能编辑部分交易设置，如交易名称、CPM、展示次数和投放日期。<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving]投放位置不符合帐户的可用资金或营销活动和包预算。 但是，支出会被跟踪并计入这些预算。 即使CPM为$0，也始终跟踪事件数据。

>[!MORELIKETHIS]
>
>* [创建[!UICONTROL Simple Ad Serving]交易](simple-deal-create.md)
>* [编辑[!UICONTROL Simple Ad Serving]交易设置](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving]设置](simple-deal-settings.md)
>* [查看交易的详细报告](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
