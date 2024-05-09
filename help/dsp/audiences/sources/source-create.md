---
title: 创建受众源以激活第一方受众
description: 了解如何创建源以将受众导入您的帐户或广告商帐户。
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# 创建受众源以激活第一方受众

<!-- Will this remain for admin users/Adobe Account Team users only? -->

在DSP中创建来源以将第一方受众导入您的DSP帐户或广告商帐户。

有关从特定客户数据平台摄取区段所需的其他步骤，请参阅 [特定于受众的激活工作流](source-about.md)

1. 在主菜单中，单击 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. 单击 **[!UICONTROL Add Source]**.

1. 在 [!UICONTROL Select a Type] 菜单，选择源类型。

   * *[!UICONTROL RT-CDP]*： [此 [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   <!-- * *[!UICONTROL ActionIQ]*: The [[!DNL ActionIQ] customer data platform](source-about.md). -->

   * *[!UICONTROL Tealium CDP]*：和 [[!DNL Tealium] 客户数据平台](source-about.md).

1. 指定 [!UICONTROL Data Visibility Level]： *[!UICONTROL Advertiser]* 或 *[!UICONTROL Account]*.

1. 输入其余的 [源设置](source-settings.md).

   保留 [!UICONTROL Source Key] 即会生成。 稍后您需要该值。

1. 单击 **[!UICONTROL Save]**.

>[!NOTE]
>
>为客户数据平台创建源后，必须完成其他步骤。 请参阅 [激活工作流 [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> 和 [激活工作流 [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [受众源设置](source-settings.md)
>* [关于从受众源激活经过身份验证的区段](source-about.md)
>* [从通用ID合作伙伴激活经过身份验证的区段](source-universal-id.md)<!-- title?-->
>* [Adobe Advertising Cloud DSP连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
