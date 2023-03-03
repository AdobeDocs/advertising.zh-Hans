---
title: 将PG交易的广告提交到 [!DNL FreeWheel]
description: 了解如何在上与出版商一起请求批准计划性保证交易的广告 [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# 将计划性保证交易的广告提交到 [!DNL Freewheel]

*具有的帐户 [!DNL FreeWheel] 仅限程序化保证权限*

一旦您 [接受与FreeWheel上的发布者达成的程序化保证交易](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)，包括选择广告和创建用于交易的程序化保证默认投放位置，您必须将广告提交到 [!DNL Freewheel] 以待批准。

>[!PREREQUISITES]
>
>与您的Adobe客户团队合作，确保 [!DNL DSP] 帐户具有使用 [!DNL FreeWheel] 有程序保证的工作流。

1. 复制与一起使用的广告的广告密钥 [!DNL Freewheel] 交易：

   1. 单击营销活动的名称。

   1. 在子菜单中，单击 **[!UICONTROL Ads]**.

   1. 单击  **[!UICONTROL ...]** > **[!UICONTROL Edit]** 在广告名称旁边。

   1. 打开广告设置后，复制浏览器地址栏中显示的URL中的字母数字广告键。

      例如，在以下URL中，广告键是 `3NtNC5ZbaGZtqbei8jD3`

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. 将广告提交到 [!DNL Freewheel]：

   1. 执行以下任一操作：

      * 在广告名称旁边，单击  **[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**.

      * 在主菜单中，单击 **[!UICONTROL Inventory]** > **[!UICONTROL Deals]**. 在交易行中，单击 ![“选项”菜单](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**.
   1. 验证交易ID，输入 **[!UICONTROL Ad Key]** 您在步骤1中复制了，然后单击 **[!UICONTROL Submit]**.

   广告必须先提交并批准，然后才能运行。

1. [检查广告提交状态](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [在中设置程序化保证交易概述 [!DNL Freewheel]](freewheel-overview.md)
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [检查广告的状态 [!DNL FreeWheel] 计划性保证交易](freewheel-check-status.md)
>* [错误代码 [!DNL Freewheel] 广告提交](freewheel-error-codes.md)

