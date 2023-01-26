---
title: 设置程序化保证交易
description: 了解如何设置您与出版商协商的程序化保证(PG)交易。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# 设置程序化保证交易

*[仅支持的供应端平台](programmatic-guaranteed-about.md)*

在您与受支持的发布者协商程序化保证(PG)交易后，您可以使用 [!DNL Deal ID inbox] 或手动输入交易详细信息。

>[!NOTE]
>
> 对于PG交易，发布者会处理所有预算步调、预算上限和定位。 所有允许PG通过DSP的SSP都确认发布者可以设置预算上限。
>
> 在 [!DNL FreeWheel] 需要额外的权限和步骤。 请参阅“[在中设置程序化保证交易概述 [!DNL FreeWheel]](freewheel-overview.md)“ ”以了解详细信息。

## 使用 [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

以下方法是 [!DNL FreeWheel], [!DNL Google Authorized Buyers]和 [!DNL Magnite DV+].

1. [接受交易](deal-id-inbox-accept.md).

1. 在保存交易后，选择将用于交易的广告，并根据提示创建一个程序化保证(PG)默认投放。

   为交易创建默认的PG位置是交付100%购买内容的必备条件。 此类版面没有定位，因此DSP可以向发布者的每个竞价请求返回竞价。

   * 如果您接受单笔交易，则会自动重定向到PG默认版面创建工作流。

      全部 [!DNL FreeWheel] 交易被提议为单笔交易。

   * 如果您接受具有多个PG交易ID的建议书，请确定您需要创建的每个PG默认版面。 创建所有必需的版面后，将启用“继续”按钮。

1. （可选）通过单击 ![“选项”菜单](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   交易可以针对支持媒体类型任意组合（如连接的电视、桌面和音频）的多个投放。

## 手动设置程序化保证交易

对所有其他SSP使用此方法。

1. [手动设置交易ID详细信息](deal-id-create.md).

1. 保存交易后，选择将用于交易的广告，并根据提示创建一个PG默认版面。

   为交易创建PG默认版面，是交付100%购买内容的必备条件。 此类版面没有定位，因此DSP可以向发布者的每个竞价请求返回竞价。

1. （可选）通过单击 ![“选项”菜单](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   交易可以针对支持媒体类型任意组合（如连接的电视、桌面和音频）的多个投放。

>[!MORELIKETHIS]
>
>* [关于程序化保证交易](programmatic-guaranteed-about.md)
>* [谈判程序化保证交易的提示](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [为程序化保证交易提交广告 [!DNL FreeWheel]](freewheel-submit.md)
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [手动创建交易ID详细信息](deal-id-create.md)
>* [SSP合作伙伴](ssp-partners.md)
>* [库存功能概述](inventory-overview.md)

