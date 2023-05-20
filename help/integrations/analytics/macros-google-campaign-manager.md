---
title: 附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Google Campaign Manager 360] 廣告標籤
description: 瞭解新增原因和方式 [!DNL Analytics for Advertising] 巨集加入您的 [!DNL Google Campaign Manager 360] 廣告標籤
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# 附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Google Campaign Manager 360] 廣告標籤

*僅具有AdobeAdvertising-Adobe Analytics整合的廣告商*

*僅適用於Advertising DSP*

如果您使用來自的廣告標籤 [!DNL Google Campaign Manager 360] 若為您的Advertising DSP廣告，請附加 [!DNL Analytics for Advertising] 引數至您的登陸頁面URL，使用 [`%p` 巨集](https://support.google.com/campaignmanager/table/6096962). 引數記錄 `s_kwcid` 和 `ef_id` 登陸頁面URL中的查詢字串引數，可讓Adobe廣告將廣告的點選資料傳送至Adobe Analytics。

將巨集用於 [!DNL Campaign Manager 360] 適用於下列型別的顯示廣告和視訊廣告 [!DNL Analytics for Advertising] 實作：

* **使用的廣告商 [!DNL Adobe] [!DNL Analytics for Advertising] 在其網站上實作的JavaScript程式碼**：JavaScript程式碼已記錄 `s_kwcid` 和 `ef_id` 查詢字串引數。 不過，當不支援第三方Cookie時，使用巨集可延伸追蹤以包含點選型轉換。 最佳實務是將下列各節中的巨集新增至廣告標籤，以擷取未透過JavaScript程式碼擷取的其他點進資料。

>[!NOTE]
>
>JavaScript程式碼是僅在Cookie仍可用時用於點選追蹤的解決方案。 一旦Cookie停止使用，便需要實作下列巨集。

* **其網站未使用的廣告商 [!DNL Analytics for Advertising] JavaScript程式碼，並改為依賴 [!DNL Analytics] 僅限點進資料的伺服器端轉送** （沒有任何瀏覽資料）：需要下列巨集來報告網站上由您透過Adobe廣告購買的廣告驅動的點選活動。

## 將巨集附加至 [!DNL Google Campaign Manager 360] 廣告

範圍 [!DNL Google Campaign Manager 360]，將下列引數附加至每個顯示廣告和影片廣告的登陸頁面URL： `%pamo=!;`

您可以透過數種方式指定登入頁面URL。 以下小節包含每個選項的指示。

以下範例為尾碼格式化的登入頁面URL。

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>
>* 如果登陸頁面URL包含雜湊符號(#)，這是不常見的，請放置 `amo` 雜湊符號前的引數。
>* 如果之後未包含其他引數 `amo` 引數，然後新增引數（例如&amp;a=b）。 範例：`https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`


### 設定廣告商層級的登陸頁面URL尾碼

1. 請參閱 [開啟廣告商屬性的指示](https://support.google.com/campaignmanager/answer/2829344).
1. 在 [!UICONTROL Landing page URL suffix] 設定，包括 `%pamo!;` 在 [!UICONTROL URL suffix] 欄位。

### 設定行銷活動層級的登陸頁面URL尾碼

1. 請參閱 [開啟行銷活動屬性的指示](https://support.google.com/campaignmanager/answer/2838056#set).
1. 在 [!UICONTROL Landing page URL suffix] 設定，包括 `%pamo!;` 在 [!UICONTROL URL suffix] 欄位。

### 設定創意層級登陸頁面URL尾碼

1. 開啟創意內容。
1. 在 [!UICONTROL Click tags] 設定，包含 `%pamo!;` 在 [!UICONTROL Landing page] 點按標籤的欄。

## 如何 [!DNL Analytics for Advertising] 在DSP中展開巨集

在DSP中，當您建立包含 [!DNL Analytics for Advertising] 引數(`amo`)， `ef_id` 和 `s_kwcid` 巨集會自動附加至點選URL。 最佳實務是檢查DSP中的標籤，以確保 `ef_id` 和 `s_kwcid` 有巨集存在。

以下範例為 [!DNL Google Campaign Manager 360] [ins標籤](https://support.google.com/campaignmanager/answer/6080468) 在DSP中顯示的內容。

```
<ins class='dcmads' style='display:inline-block;width:160px;height:600px'
data-dcm-placement='N6482.2155306TUBEMOGUL/B23486129.261313631'
data-dcm-rendering-mode='iframe'
data-dcm-https-only
data-dcm-resettable-device-id=''
data-dcm-app-id='' data-dcm-click-tracker='${TM_CLICK_URL}'
data-dcm-param-amo='ef_id=${TM_USER_ID}:${TM_DATETIME}:d&s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}'>
<script src='https://www.googletagservices.com/dcm/dcmads.js'></script>
</ins>
```

當使用者按一下廣告， [!DNL Google Campaign Manager 360] 看到 `%pamo` URL尾碼中的值，並動態插入 `amo` 引數放入URL中。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [使用的Adobe廣告ID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤](macros-flashtalking.md)

