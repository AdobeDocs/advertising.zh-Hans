---
title: 使用 [!DNL Marketing Channels] 使用Adobe廣告資料
description: 瞭解如何在中使用Adobe廣告資料 [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 522c7f01-1138-477d-8018-36030caab55e
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 0%

---

# 使用 [!DNL Analytics Marketing Channels] 使用Adobe廣告資料

*僅具有AdobeAdvertising-Adobe Analytics整合的廣告商*

同時使用Adobe廣告和 [!DNL Analytics Marketing Channels] 報表中，您可以取得數位媒體如何影響網站活動的寶貴見解。

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

下圖顯示Adobe廣告與網站的 [!DNL Marketing Channels] 追蹤組成一個訪客歷程的個別造訪。 Adobe廣告報表 [!DNL Analytics] 僅限於使用AMO ID透過Adobe廣告販運的付費顯示、搜尋、社交和商務管道廣告。 不過， [!DNL Marketing Channels] 追蹤中設定的所有管道 [!DNL Marketing Channels] 處理規則。

![如何Adobe廣告和 [!DNL Marketing Channels] 追蹤訪客歷程中的個別造訪](/help/integrations/assets/a4adc-mc-sample-journey2.png)

在第一次造訪中，使用者透過電子郵件行銷活動進入網站，執行了十次頁面檢視，然後離開。 在第二次造訪中，使用者透過顯示廣告進入網站，執行了十次頁面檢視，然後離開。 在第三次造訪中，使用者透過免費搜尋進入網站、執行了五個頁面檢視、執行了$250的轉換，最後進入左側。 請注意兩者在追蹤上的差異 [!DNL Marketing Channels] 和Adobe廣告。 此歷程中AdobeAdvertising追蹤的唯一管道是 [!UICONTROL Display]. Adobe廣告追蹤 [!UICONTROL Display] 管道造訪和將後續參與資料（例如頁面檢視）和轉換歸因於該廣告的影響。 [!DNL Marketing Channels]另一方面，會提供所有色版的完整檢視。

由於AMO ID會在訪客的歷程中持續存在，因此您可以使用AMO ID資料來瞭解Adobe廣告如何影響其他行銷管道。 AMO ID [預設會持續60天](/help/integrations/analytics/overview.md)，但您可以視需要設定持續性。

## 如何結合Adobe廣告和行銷管道資料來分析媒體效能

範圍 [!DNL Analytics]，您可以結合Adobe廣告持續付費廣告資料和 [!DNL Marketing Channels] 完整的造訪資料，以便更妥善分析您的媒體效能，進而更能影響客戶歷程。

以下分析使用Adobe廣告資料來顯示不同版本的顯示廣告如何影響網站轉換。 所有三欄都使用相同的轉換量度，但每欄講述的故事不同：

* 欄1會檢視在訪客歷程中持續儲存的AMO ID資料。 欄1指出641應用程式啟動曾透過瀏覽或點進事件，與Adobe廣告連結在一起。 此檢視不採用任何其他檢視 [!DNL Marketing Channels] 歸因。

* 在 [!DNL Marketing Channels] 不過，641應用程式啟動歸因於其他行銷管道。 最後兩欄採用「641應用程式啟動」，並將資料限製為 [!UICONTROL Display Click-Through] 和 [!UICONTROL Display View-Through] 管道，顯示上次接觸歸因模型中發生的轉換。

![顯示廣告如何影響網站轉換的範例](/help/integrations/assets/a4adc-mc-display-impact.png)

您可以進一步執行此分析。 您可以透過行銷管道進一步劃分「Adobe廣告」列，以檢視Adobe廣告轉換歸因於641應用程式啟動的位置。 您已經知道其中五個轉換歸因於「上次接觸顯示點進」，19個則歸因於「上次接觸顯示檢視」。 如此仍會將617應用程式開始歸因於其他行銷管道。 您可以將「上次接觸管道」維度拖放至Advertising DSP條列專案上方，以顯示其他應用程式啟動的管道歸因，並顯示「顯示」管道的跨管道影響。

![如何新增「上次接觸管道」維度](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

現在您可以檢視剩餘的應用程式啟動數的歸因方式。 357個上次接觸應用程式開始的電子郵件會獲得評分，其中AMO ID持續存在。 使用此型別的分析，您可以檢視Adobe廣告顯示廣告對所有頻道的影響。 由於只有一個資料集和歸因模型，因此無法提供這類深入分析。

![顯示管道的跨管道影響範例](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

若棧疊圖表設為「100%棧疊」，則可進一步改善分析，以顯示一段時間內的趨勢資料。 此視覺效果可讓您更輕鬆地監視哪些上次接觸行銷管道受到您的顯示行銷活動的影響更大。

![顯示管道的趨勢化跨管道影響範例](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [的基礎知識 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [使用Adobe廣告ID來建立 [!DNL Marketing Channels] 處理規則](mc-ids.md)
>* [為何管道資料可能因Adobe廣告和以下內容而異 [!DNL Marketing Channels]](mc-data-variances.md)
>* [影片：使用 [!DNL Marketing Channels] 適用於Adobe廣告報表](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [概述 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)

