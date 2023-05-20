---
title: 建立受眾來源以啟用第一方受眾
description: 瞭解如何建立來源以將受眾匯入您的帳戶或廣告商帳戶。
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 3347bfbaec92bb13428a39207954f895eb4f5d6d
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 3%

---

# 建立受眾來源以啟用第一方受眾

<!-- Will this remain for admin users/Adobe Account Team users only? -->

建立來源以將受眾匯入您的DSP帳戶或廣告商帳戶。 目前，您可以從以下位置匯入對象： [此 [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=zh-Hans).

>[!NOTE]
>
>在您為建立來源之後 [!DNL Real-Time CDP]，您必須啟用 [!DNL Real-Time CDP] 透過AdobeAdvertising DSP目的地內的對象 [!DNL Real-Time CDP] 以開始匯入它們。 另請參閱 [啟動工作流程中的步驟](source-about.md#workflow-sources).

1. 在主功能表中，按一下 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. 单击 [!UICONTROL Add Source].

1. 在 [!UICONTROL Select a Type] 功能表，選取來源型別。

   *[!UICONTROL RT-CDP]*：此來源型別，用於 [此 [!DNL Adobe Real-Time Customer Data Profile]](source-about.md)，是唯一選項。

1. 指定 [!UICONTROL Data Visibility Level]： *[!UICONTROL Advertiser]* 或 *[!UICONTROL Account]*.

1. 輸入其餘的 [來源設定](source-settings.md).

   保留一份 [!UICONTROL Source Key] （即產生）。 您稍後需要該值。

1. 单击 **[!UICONTROL Save]**.

1. 在Experience Platform中，使用建立Advertising DSP目的地連線 [!UICONTROL Source Key] 在DSP來源設定中產生的。

   如需啟用DSP目的地連線、選取區段及存取控制許可權的指示，請參閱&quot;[Adobe Advertising Cloud DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).」

>[!MORELIKETHIS]
>
>* [對象來源設定](source-settings.md)
>* [關於從受眾來源啟用已驗證的區段](source-about.md)
>* [從持久ID合作夥伴啟用已驗證的區段](source-durable-id.md)<!-- title?-->
>* [Adobe Advertising Cloud DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)

