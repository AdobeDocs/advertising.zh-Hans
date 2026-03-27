---
title: 向 [!DNL FreeWheel]提交PG交易的广告
description: 了解如何在 [!DNL FreeWheel]上与发布者请求批准计划性保证交易的广告。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
source-git-commit: 1e307a95d597f20c97683ee20c0a3b99f662f7fd
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# 向[!DNL FreeWheel]提交计划性保证交易的广告

*仅具有[!DNL FreeWheel]编程性保证权限的*&#x200B;帐户

一旦您[在FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)上接受与发布者的程序化保证交易（包括选择广告和创建用于交易的程序化保证默认投放位置），您必须将广告提交给[!DNL FreeWheel]进行审批。

>[!PREREQUISITES]
>
>与您的Adobe帐户团队合作，确保您的[!DNL DSP]帐户有权使用[!DNL FreeWheel]程序化保证工作流。

1. 复制与[!DNL FreeWheel]交易一起使用的广告的广告密钥：

   1. 单击营销活动的名称。

   1. 在子菜单中，单击&#x200B;**[!UICONTROL Ads]**。

   1. 单击广告名称旁边的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit]**。

   1. 广告设置打开后，复制浏览器地址栏中显示的URL中的字母数字广告键。

      例如，在以下URL中，广告键是`3NtNC5ZbaGZtqbei8jD3`

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. 将广告提交到[!DNL FreeWheel]：

   1. 执行以下任一操作：

      * 在广告名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**。

      * 在主菜单中，单击&#x200B;**[!UICONTROL Inventory]** > **[!UICONTROL Deals]**。 在交易行中，单击![选项菜单](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**。

   1. 验证交易ID，输入您在步骤1中复制的&#x200B;**[!UICONTROL Ad Key]**，然后单击&#x200B;**[!UICONTROL Submit]**。

   广告必须先提交并批准，然后才能运行。

1. [检查广告提交状态](freewheel-check-status.md)。

>[!MORELIKETHIS]
>
>* [在 [!DNL FreeWheel]](freewheel-overview.md)中设置计划性保证交易的概述
>* [在[!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)中接受交易
>* [检查 [!DNL FreeWheel] PG交易的广告状态](freewheel-check-status.md)
>* [ [!DNL FreeWheel] 广告提交的错误代码](freewheel-error-codes.md)
