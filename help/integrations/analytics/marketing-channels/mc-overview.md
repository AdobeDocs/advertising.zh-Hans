---
title: 的基礎知識 [!DNL Marketing Channels]
description: 瞭解以下的重要資訊： [!DNL Analytics Marketing Channels] 該 [!DNL Analytics for Advertising] 使用者應該瞭解。
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# 的基礎知識 [!DNL Analytics Marketing Channels]

*僅具有AdobeAdvertising-Adobe Analytics整合的廣告商*

此頁面說明下列的重要資訊： [!DNL Analytics Marketing Channels] 該 [!DNL Analytics for Advertising] 使用者需要瞭解。

如需的完整檔案，請參閱 [!DNL Marketing Channels]，請參閱「[開始使用 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html).」

## 概述 [!DNL Marketing Channels]

[!DNL Marketing Channels] 是Adobe Analytics的主要功能。 [!DNL Marketing Channels] 報表會顯示客戶如何透過報告期間到達您的網站，以及每個管道如何影響收入或網站上的行為。

請考量下列跨造訪歷程的範例。 訪客每次造訪您的網站時，都會透過訪客進入的行銷管道表示。 首次造訪（也稱為首次接觸管道）是電子郵件。 「造訪時顯示2」為參與管道，而「免費搜尋」則視為「上次接觸管道」。 如果您使用 [!UICONTROL Last Touch Attribution] 範圍 [!UICONTROL Attribution IQ]，免費搜尋會獲得$250轉換事件的完整評價。 您可以使用Experience CloudID服務，將這些個別造訪連結在一起，以顯示單一訪客的一個歷程。

![行銷管道中的跨造訪轉換歷程範例](/help/integrations/assets/a4adc-mc-sample-journey.png)

透過使用 [!UICONTROL Marketing Channels] 處理規則時，您可以建立邏輯集合來判斷帶動流量的管道，以及在使用者造訪您的網站時追蹤每個管道。 例如， [!UICONTROL Email] 管道將由點按時產生的唯一追蹤代碼指示，若由Adobe Analytics記錄，會將造訪分類為源自電子郵件行銷活動。

## 處理規則及行銷管道的設定方式

每次使用者進入網站時，都會透過他們點按或直接輸入網址列中的URL進行。 當使用者進入網站， [!DNL Analytics] 追蹤可用來判斷造成造訪的管道的資訊。

行銷人員通常會附加查詢字串引數追蹤程式碼至管道URL，以協助追蹤管道對其網站的影響。 您可以設定 [!DNL Marketing Channels] 處理規則來監聽特定追蹤引數和值，以判斷管道，而不需要任何其他追蹤。 例如，如果所有電子郵件促銷活動URL都遵循格式 `www.adobe.com?cid=email…` (其中URL包含查詢字串引數和值 `cid=email`)，然後您可以建立規則來監聽此追蹤程式碼，並將造訪貯存在 [!UICONTROL Email] 頻道。

其他管道沒有可追蹤的URL路徑，需要進一步的識別邏輯。 例如， [!UICONTROL Earned Social]使用者點按另一個使用者在社交網路上有機分享的連結時，這是要追蹤的重要管道。 不過，行銷人員無法將查詢字串引數追蹤程式碼附加至共用的URL。 在這種情況下，您可以建立處理規則來監聽感興趣的社交網路的反向連結網域，以及不存在付費追蹤代碼來判斷頻道。 之後，系統會在行銷管道報表中，將符合這些要求的造訪追蹤為「贏取社交」。

Adobe建議與您的analytics團隊合作，建立一套完整的 [!DNL Marketing Channels] 處理規則來追蹤與您的業務相關的所有管道。 這麼做可讓您建立強大的歸因報表。

若要瞭解Adobe廣告如何對建立自訂行銷管道所需的訊號做出貢獻，請參閱&quot;[使用廣告ID來建立 [!DNL Marketing Channels] 規則](mc-ids.md).」

>[!MORELIKETHIS]
>
>* [使用Adobe廣告ID來建立 [!DNL Marketing Channels] 處理規則](mc-ids.md)
>* [為何管道資料可能因Adobe廣告和以下內容而異 [!DNL Marketing Channels]](mc-data-variances.md)
>* [使用 [!DNL Analytics Marketing Channels] 使用Adobe廣告資料](mc-ac-data.md)
>* [影片：使用 [!DNL Marketing Channels] 適用於Adobe廣告報表](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [概述 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)

