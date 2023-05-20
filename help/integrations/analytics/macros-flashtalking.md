---
title: 附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤
description: 瞭解新增原因和方式 [!DNL Analytics for Advertising] 巨集加入您的 [!DNL Flashtalking] 廣告標籤
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# 附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤

*僅具有AdobeAdvertising-Adobe Analytics整合的廣告商*

*僅適用於Advertising DSP*

如果您使用來自的廣告標籤 [!DNL Flashtalking] 若為Advertising DSP廣告，請將Analytics for Advertising引數附加至登陸頁面URL。 引數記錄 `s_kwcid` 和 `ef_id` 登陸頁面URL中的查詢字串引數，可讓Adobe廣告將廣告的點選資料傳送至Adobe Analytics。

將巨集用於 [!DNL Flashtalking] 適用於下列型別的顯示廣告和視訊廣告 [!DNL Analytics for Advertising] 實作：

* **使用的廣告商 [!DNL Adobe] [!DNL Analytics for Advertising] 在其網站上實作的JavaScript程式碼**：JavaScript程式碼已記錄 `s_kwcid` 和 `ef_id` 查詢字串引數。 不過，當不支援第三方Cookie時，使用巨集可延伸追蹤以包含點選型轉換。 最佳實務是將下列各節中的巨集新增至廣告標籤，以擷取未透過JavaScript程式碼擷取的其他點進資料。

>[!NOTE]
>
>JavaScript程式碼是僅在Cookie仍可用時用於點選追蹤的解決方案。 一旦Cookie停止使用，便需要實作下列巨集。

* **其網站未使用的廣告商 [!DNL Analytics for Advertising] JavaScript程式碼，並改為依賴 [!DNL Analytics] 僅限點進資料的伺服器端轉送** （沒有任何瀏覽資料）：需要下列巨集來報告網站上由您透過Adobe廣告購買的廣告驅動的點選活動。

## 顯示廣告標籤

在內 [!DNL Flashtalking] 新增標籤設定，將下列巨集附加至中的點進URL結尾 `Clicktag` 欄位：

```html
?[ftqs:[AdobeAMO]]
```

範例：  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

## 影片廣告標籤

在內 [!DNL Flashtalking] 新增標籤設定，將下列巨集附加至中的點進URL結尾 `Clicktag` 欄位：

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

範例：  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [使用的Adobe廣告ID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Google Campaign Manager 360] 廣告標籤](/help/integrations/analytics/macros-google-campaign-manager.md)

