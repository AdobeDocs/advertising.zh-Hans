---
title: 在[!UICONTROL Deal ID Inbox]中接受交易
description: 了解如何使用交易ID收件箱接受您已经与 [!DNL FreeWheel], [!DNL Google Authorized Buyers] (以前称为 [!DNL AdX]), and [!DNL Magnite DV+] （以前称为 [!DNL Rubicon]）)上的发布者协商的私人交易。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 7c681ab7-3051-451d-ab83-fc75bdd6eaad
source-git-commit: d5a291c8d1f464e1c22777512d29f4e041bb7988
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# 在[!UICONTROL Deal ID Inbox]中接受交易

*只映射到SSP帐户的DSP帐户中的用户*

使用[!UICONTROL Deal ID inbox]快速接受您已经与[!DNL FreeWheel]、[!DNL Google Authorized Buyers]（以前称为[!DNL AdX]）和[!DNL Magnite DV+]（以前称为[!DNL Rubicon]）的发布者协商的私人交易。

>[!NOTE]
>
>在[!DNL FreeWheel]上与发布者设置编程性保证交易需要额外的权限和步骤。 有关详细信息，请参阅“[在FreeWheel](freewheel-overview.md)中设置计划性保证交易的概述”。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. 在[!UICONTROL Deals]列表上方，单击蓝色条以打开[!UICONTROL Deal ID inbox]。

1. （可选）要刷新交易详细信息，请单击&#x200B;**[!UICONTROL Refresh]**。

   DSP每天凌晨4:30（东部标准时间）自动刷新所有交易详细信息。 它还每小时刷新所有[!DNL FreeWheel]交易并更新[!DNL Google]和[!DNL Magnite DV+]中的现有交易。

1. （如果您之前忽略了交易）单击&#x200B;**[!UICONTROL Ignored Deals]**&#x200B;选项卡。

1. 要复查并确认交易详细信息（如发布者和日期），请将光标悬停在交易行上，然后单击![复查](/help/dsp/assets/review.png)。

1. 执行以下任一操作：

   * 在交易详细信息中，单击&#x200B;**[!UICONTROL Accept]**。

   * 在[!UICONTROL Deal ID inbox]中，将光标悬停在交易行上并单击![接受](/help/dsp/assets/accept.png)。

1. 在交易详情中：
   1. 完成必需的信息： **[!UICONTROL Publisher]**、**[!UICONTROL Media Type]**&#x200B;和&#x200B;**[!UICONTROL Deal Access]**（有权访问交易的广告商）。
   1. （可选）指定要与其共享交易的附加帐户或向交易记录附加标签。

   1. 单击&#x200B;**[!UICONTROL Save]**。

1. （仅限程序化保证交易）按照提示为交易选择广告（或出版商管理的广告的1x1跟踪像素），并创建针对交易的程序化保证默认投放位置。

接受交易后，交易将从[!UICONTROL Deal ID inbox]移至[!UICONTROL Inventory] > [!UICONTROL Deals]视图，并且交易可用作每个投放位置的[!UICONTROL Inventory Targeting]部分中的专用库存源。

>[!MORELIKETHIS]
>
>* [关于交易ID收件箱](deal-id-inbox-about.md)
>* [设置计划性保证交易](programmatic-guaranteed-set-up.md)
>* [提交计划性保证交易的广告 [!DNL FreeWheel]](freewheel-submit.md)
>* [关于计划性保证交易](programmatic-guaranteed-about.md)
>* [清单功能概述](inventory-overview.md)
