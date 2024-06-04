---
title: 创建受众源以激活通用ID受众
description: 了解如何创建源以从客户数据平台导入受众，并将它们转换为包含通用ID的区段。
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 16a796e02150b00c77c825d7f54c6e390c85214a
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# 创建受众源以激活通用ID受众

*Beta版功能*

在DSP中为客户数据平台中的每个第一方受众创建一个源，您要将该受众转换为包含指定通用ID类型的区段。 您可以将区段导入到贵组织的DSP帐户或广告商帐户。 根据所选通用ID类型收取数据费用。

需要执行其他步骤才能从每个客户数据平台摄取受众。 请参阅过程末尾的注释。

1. 在主菜单中，单击 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. 单击 **[!UICONTROL Add Source]**.

1. 在 [!UICONTROL Select a Type] 菜单中，选择您的客户数据平台：

   * *[!UICONTROL RT-CDP]*： [此 [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   * *[!UICONTROL ActionIQ]*：和 [[!DNL ActionIQ] 客户数据平台](source-about.md).

   * *[!UICONTROL Tealium CDP]*：（仅限已配置的用户）和 [[!DNL Tealium] 客户数据平台](source-about.md).

1. 指定 [!UICONTROL Data Visibility Level]： *[!UICONTROL Advertiser]* 或 *[!UICONTROL Account]*.

1. 输入其余的 [源设置](source-settings.md).

   保留 [!UICONTROL Source Key] 即会生成。 稍后您需要该值。

1. 单击 **[!UICONTROL Save]**.

>[!NOTE]
>
>在为客户数据平台创建源后，您需要完成其他步骤。 请参阅 [用于从导入受众的工作流 [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> 和 [用于从导入受众的工作流 [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [受众源设置](source-settings.md)
>* [关于第一方受众源](source-about.md)
>* [Adobe Advertising Cloud DSP连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
