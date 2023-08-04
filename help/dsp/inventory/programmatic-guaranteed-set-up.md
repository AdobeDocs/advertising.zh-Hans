---
title: 设置计划性保证交易
description: 了解如何设置您与出版商协商的程式化保证(PG)交易。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
source-git-commit: 60676d8ef022d2ed61467d7254405695d5f106b3
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# 设置计划性保证交易

*[仅支持供应端平台](programmatic-guaranteed-about.md)*

在与受支持的发布者协商计划性保证(PG)交易后，您可以在DSP中通过使用 [!DNL Deal ID inbox] 或通过手动输入交易详细信息。

>[!NOTE]
>
> 对于PG交易，出版商负责处理所有预算步调、预算上限和定位。 所有允许PG通过DSP的SSP都确认发布者可以设置预算上限。
>
> 与发布者建立编程性保证交易 [!DNL FreeWheel] 需要额外的权限和步骤。 请参阅&quot;[在中设置计划性保证交易的概述 [!DNL FreeWheel]](freewheel-overview.md)”以了解更多信息。

## 使用设置计划性保证交易 [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

以下方法是的首选过程 [!DNL FreeWheel]， [!DNL Google Authorized Buyers]、和 [!DNL Magnite DV+].

1. [接受交易](deal-id-inbox-accept.md).

1. 保存交易后，选择将用于交易的广告（或出版商管理的广告的1x1跟踪像素），并根据提示创建程序化保证(PG)默认投放位置。

   为交易创建默认的PG投放位置是交付所有购买内容的必备条件。 此类型的投放位置没有定位，因此DSP可以向发布者的每个竞价请求返回竞价。

   * 如果您接受单笔交易，则会自动将您重定向到PG默认投放创建工作流。

     全部 [!DNL FreeWheel] 这些交易都是以单一交易形式提出的。

   * 如果您接受具有多个PG交易ID的建议，请确定您需要创建的每个PG默认投放位置。 创建所有必需的投放位置后，“继续”按钮即会启用。

1. （可选）通过单击以在其他PG或非PG投放位置定位PG交易 ![“选项”菜单](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   交易可以针对支持任意媒体类型组合（例如连接电视、台式机和音频）的多个投放位置。

## 手动设置计划性保证交易

将此方法用于所有其他SSP。

1. [手动设置交易ID详细信息](deal-id-create.md).

1. 保存交易后，选择将用于交易的广告（或发布商管理的广告的1x1跟踪像素），并根据提示创建PG默认投放位置。

   必须创建交易的PG默认投放位置，才能交付全部购买内容。 此类型的投放位置没有定位，因此DSP可以向发布者的每个竞价请求返回竞价。

1. （可选）通过单击以在其他PG或非PG投放位置定位PG交易 ![“选项”菜单](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   交易可以针对支持任意媒体类型组合（例如连接电视、台式机和音频）的多个投放位置。

>[!MORELIKETHIS]
>
>* [关于程序化保证交易](programmatic-guaranteed-about.md)
>* [谈判计划性保证交易的技巧](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [提交计划性保证交易的广告 [!DNL FreeWheel]](freewheel-submit.md)
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [手动创建交易ID详细信息](deal-id-create.md)
>* [SSP合作伙伴](ssp-partners.md)
>* [清单功能概述](inventory-overview.md)
