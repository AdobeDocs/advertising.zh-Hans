---
title: 關於從受眾來源啟用已驗證的區段
description: 瞭解如何從客戶資料平台擷取第一方區段。
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: 68095fc77659826fae43f2453d17022ef1880807
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 2%

---

# 關於從受眾來源啟用已驗證的區段

<!-- Doesn't specifically explain what you can do in our UI -->

DSP可以內嵌第一方區段(由客戶資料平台(CDP)內建立的已驗證訊號所組成)。 您可以使用擷取的區段作為版位目標。

## [!DNL Adobe Real-Time Customer Data Profile]

DSP已與 [此 [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=zh-Hans)，是Adobe Experience Platform的一部分。

在 [!DNL Real-time CDP]， *目的地* 是與外部資料平台的連線，可順暢地啟用資料。 例如，您可以使用目的地來針對各種DSP支援的數位格式的目標廣告啟用已知的客戶關係（例如雜湊電子郵件地址）。

如需目的地的詳細資訊，請參閱Experience Platform [目的地指南](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html)，包括產品概觀，說明 [建立目的地工作區](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) 和 [建立目的地連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html)、和 [啟用目的地資料](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

### 搭配使用DSP整合的工作流程 [!DNL Real-time CDP] {#workflow-sources}

1. [允許DSP將客戶資料區段轉譯為 [!DNL LiveRamp RampIDs]](source-durable-id.md) 在競標環境中可辨識的專案。<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your Adobe Account Team will perform this configuration. -->

1. [建立對象來源](source-create.md) 將受眾匯入您的DSP帳戶或廣告商帳戶。

1. [設定 [!DNL Real-Time CDP] Experience Platform中的目的地連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).

如需其他支援，請聯絡您的Adobe客戶團隊或 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [從持久ID合作夥伴啟用已驗證的區段](source-durable-id.md)
>* [建立受眾來源以啟用第一方受眾](source-create.md)
>* [對象來源設定](source-settings.md)
>* [AdobeAdvertising DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [目的地目錄概觀](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [關於對象管理](/help/dsp/audiences/audience-about.md)

