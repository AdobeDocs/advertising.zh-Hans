---
title: 為何管道資料可能因Adobe廣告和以下內容而異 [!DNL Marketing Channels]
description: 瞭解AMO ID所追蹤的管道資料為何與所追蹤的管道資料不同 [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# 為何管道資料可能因Adobe廣告和以下內容而異 [!DNL Marketing Channels]

*僅具有AdobeAdvertising-Adobe Analytics整合的廣告商*

使用者學習Adobe廣告與整合時常見的問題 [!DNL Marketing Channels] 資料集是「造成AMO ID和之間資料差異的原因」 [!DNL Marketing Channels]？」 或者，有時候，「為何資料會中斷？ 我需要所有量度在報告中相符。」 幸運的是，差異並不表示資料已「中斷」，而是預期且甚至是想要的差異。 讓我們來看看為何會以這種方式設計整合。

這兩個資料集的主要使用案例不同：

* [!DNL Marketing Channels]：的主要使用案例 [!DNL Marketing Channels] 是使用常見的歸因模型，比較多個管道的資料。 分析人員可以使用 [!UICONTROL Marketing Channel] 維度，以增進對於管道如何彼此互動的深入分析。 此深入分析可協助您針對每個管道的投資方式做出宏觀決策，並可引導您深入分析每個管道的訪客與網站的互動情形。

   此 [!DNL Analytics] [!UICONTROL Marketing Channel] 因此，維度會設定為擷取及追蹤所有管道。 [!DNL Marketing Channels] 也可以設定為擷取Advertising DSP閱覽和點進，而且是與其他行銷管道相關連結。

* AdobeAdvertising AMO ID： AdobeAdvertising AMO ID資料的主要使用案例是提供進階 [!DNL Adobe Sensei]支援的競標演演算法。 這些演演算法會自動做出每天數以千計的微觀層級競標決定，以將廣告支出最大化，並達成 [!DNL DSP] 行銷活動或 [!DNL Search, Social, & Commerce] 作品集。 演演算法可連結行銷活動的轉換資料越多，演演算法就能越有效做出這些競標決定。

   若要收集此資料，請 [!DNL Analytics for Advertising] 整合會在Adobe Analytics的AMO ID維度中，傳遞可轉譯為點進和瀏覽追蹤程式碼的原始AMO ID，這些AMO ID會儲存為自訂變數(eVar)或保留變數(rVar)。 其他頻道的點進次數未在AMO ID維度中設定，因此AMO ID維度無法追蹤這些其他頻道的登入。 結果是AMO ID會儲存到 [!DNL Marketing Channels] 進入點。

如需有關Adobe廣告追蹤資料與報告之間可能的資料差異的詳細資訊， [!DNL Analytics] — 追蹤的資料，請參閱&quot;[預期資料差異： [!DNL Analytics] 和Adobe廣告](../data-variances.md).」

>[!MORELIKETHIS]
>
>* [預期資料差異： [!DNL Analytics] 和Adobe廣告](/help/integrations/analytics/data-variances.md)
>* [的基礎知識 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [使用Adobe廣告ID來建立 [!DNL Marketing Channels] 處理規則](mc-ids.md)
>* [使用 [!DNL Analytics Marketing Channels] 使用Adobe廣告資料](mc-ac-data.md)
>* [影片：使用 [!DNL Marketing Channels] 適用於Adobe廣告報表](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)

