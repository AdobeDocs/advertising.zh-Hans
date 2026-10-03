---
title: 关于计划性保证交易
description: 了解计划性保证(PG)交易以及哪些SSP经过认证可提供它们。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 47c89d8a-f45f-4fcb-84a6-031f7d7f580f
TQID: 'https://experienceleague.adobe.com/LJPeIv8z6DiQS-eCe8obWgKkWi5onwpBadIgElLzkXw'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: 20c71a28-1f3b-56af-ad52-f3281489a219
    internal-label: DSP Private Inventory
  - id: 85825b7c-c02c-536d-b821-66dc33454fb8
    internal-label: DSP Deal IDs
  - id: ea1cb503-33dd-595d-833b-f365576083b6
    internal-label: DSP Programmatic Guaranteed Deals
subfeature_v2:
  - id: ac506c20-96f2-48f6-9096-77706e336bda
    internal-label: Private Inventory
  - id: fae3ff5f-9a75-4de1-a100-c90dd8268528
    internal-label: Deal IDs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%
---
# 关于计划性保证交易

计划性保证(PG)交易是通过交易ID（而不是通过广告服务器标记）直接与出版商进行的保证购买。 PG对于您和您的发布者而言更灵活，而且与常规标签购买相比，它可提供更高的透明度。 计费和报告通过DSP进行整合，从而节省了您的时间。

## PG交易功能

* 交易始终通过DSP计费。
* 交易具有固定的价格和数量。
* 发布商或供应方平台(SSP)处理所有预算步调、预算上限和任何定位。
* 通常，交易在发布者的广告服务器中具有更高的优先级。
* 竞价请求不只针对单个交易或购买者。
* 单个交易ID支持多种类型的视频。
* 通过[!DNL Google Authorized Buyers] SSP接受发布者管理的广告。
* SSP和发布者具有投放SLA。

PG交易需要PG默认投放位置和广告（对于出版商管理的广告，需要1x1像素），因此DSP可以向每个竞价请求返回请求，并与SSP达成交付SLA。 设置强制的PG默认投放位置后，还可以在其他投放位置中定位PG交易。

## DSP中针对PG交易认证的SSP

* [!DNL Ambient Digital]
* [!DNL FreeWheel]
* [!DNL Google Authorized Buyers]
* [!DNL Magnite CTV] （以前为[!DNL Telaria]）
* [!DNL Magnite DV+] （以前为[!DNL Rubicon]）
* [!DNL OpenX]
* [!DNL SpotX]

>[!MORELIKETHIS]
>
>* [谈判计划性保证交易的技巧](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [设置计划性保证交易](programmatic-guaranteed-set-up.md)
>* [SSP合作伙伴](ssp-partners.md)
>* [Advertising DSP中的清单功能概述](inventory-overview.md)
