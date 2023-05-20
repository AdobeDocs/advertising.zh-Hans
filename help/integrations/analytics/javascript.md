---
title: JavaScript程式碼 [!DNL Analytics for Advertising]
description: JavaScript程式碼 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 96b71e8c99ee30254b4bdc4ef0cb8af359f64c5e
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 0%

---

# JavaScript程式碼 [!DNL Analytics for Advertising]

*僅具有AdobeAdvertising-Adobe Analytics整合的廣告商*

*僅使用Advertising DSP的廣告商*

對於Advertising DSP，請將 [!DNL Analytics for Advertising] 整合會追蹤瀏覽和點進網站互動。 點進造訪會由您網頁上的標準Adobe Analytics程式碼追蹤； [!DNL Analytics] 程式碼會擷取登陸頁面URL中的AMO ID和EF ID引數，並在其各自的保留eVar中追蹤它們。 您可以在網頁中部署JavaScript程式碼片段，以追蹤瀏覽次數。

在造訪網站的第一個頁面檢視上，AdobeAdvertising JavaScript程式碼會檢查訪客是否先前看過或點選過廣告。 如果使用者先前曾透過點進進入網站或尚未看到廣告，則會忽略該訪客。 如果訪客在瀏覽廣告期間未透過點進進入網站 [按一下回顧視窗](/help/integrations/analytics/prerequisites.md#lookback-a4adc) 在Adobe廣告中設定，則Adobe廣告JavaScript程式碼a)會使用 [Experience CloudID服務](https://experienceleague.adobe.com/docs/id-service/using/home.html) 產生補充ID (`SDID`)或b)使用Adobe Experience Platform [!DNL Web SDK] `generateRandomID` 產生的方法 `[!DNL StitchID]`. 其中一個ID都可用來將Adobe廣告中的資料拼接至訪客的Adobe Analytics點選。 Adobe Analytics接著會查詢Adobe廣告，以取得與廣告曝光度相關聯的AMO ID和EF ID。 AMO ID和EF ID會填入各自的eVar中。 這些值會在指定的期間（預設為60天）內持續存在。

[!DNL Analytics] 傳送網站流量量度（例如頁面檢視、造訪和逗留時間）和 [!DNL Analytics] 自訂或標準事件，以EF ID作為索引鍵，每小時AdobeAdvertising。 這些 [!DNL Analytics] 接著透過Adobe廣告歸因系統執行的量度，將轉換連結到點選和曝光歷史記錄。

>[!NOTE]
>
>Adobe廣告JavaScript追蹤邏輯發生在Adobe端，因此對頁面載入時間幾乎沒有影響。
>
>相較之下， [!DNL DCM] 資料聯結器至 [!DNL Analytics] (使用 [!DNL Google Campaign Manager 360])時，Advertising DSP的使用者端會發生。 使用者端彙整會減緩頁面載入速度，並增加資料遺失的風險。 出現此狀況是因為 [!DNL Analytics] JavaScript必須ping [!DNL DoubleClick] 並等待 [!DNL DoubleClick] 將最後點選/曝光資料傳回至 [!DNL Analytics]. 當您的 [!DNL DSP] 團隊設定 [!DNL DCM] 資料聯結器，您必須指定您願意將頁面延遲多久。

## 部署JavaScript程式碼

JavaScript程式庫由兩行組成，允許 [!DNL Analytics] 和Adobe廣告互相溝通。 如果 [!DNL Analytics for Advertising] 整合已在Adobe廣告實作期間完成，則您應已收到此程式碼及其部署說明。

### 程式碼

#### 使用Experience CloudIdentity服務的實作 `visitorAPI.js` 程式碼

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

#### 使用Experience Platform的實作 [!DNL Web SDK] `alloy.js`程式碼

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

### 放置程式碼的位置

此 [!DNL Analytics for Advertising] JavaScript函式必須在Experience CloudID服務之後，但在Analytics App Measurement程式碼之前。 這可確保補充ID (`SDID`)或 `[!DNL StitchID]` 包含在您的Analytics呼叫中。

![程式碼放置](/help/integrations/assets/a4adc-code-placement.png)

### 驗證程式碼部署

您可以使用任何封包Sniffer型別的工具(例如 [!DNL Charles]， [!DNL Fiddler]，或 [!DNL Chrome Developer Tools])，比較前往Adobe廣告的請求與前往的請求之間的四個ID值 [!DNL Analytics]，如下所述。

#### 如何使用確認程式碼 [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. 開啟 [!DNL Chrome Developer Tools] 並按一下 **網路** 標籤。

1. 載入包含 [!DNL Analytics for Advertising] JavaScript。

1. 篩選 [!UICONTROL Network] 定位方式 `last` 並檢閱兩列：

   ![篩選於上次](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * 第一列是對JavaScript程式庫的呼叫，標題為 `last-event-tag-latest.min.js`.
   * 第二列是將請求傳送至Adobe Advertising的呼叫。 其開頭如下： `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      如果您沒有看到對Adobe廣告的呼叫，則它可能不會是您造訪的第一個頁面檢視。 出於測試目的，您可以移除Cookie，讓下一個呼叫成為相應造訪的第一個頁面檢視：
   1. 在應用程式標籤上，找到 `adcloud` Cookie，並確認Cookie包含 `_les_v` （上次造訪）的值為 `y` 以及30分鐘後過期的UTC紀元時間戳記。
      1. 刪除 `ad cloud` Cookie並重新整理頁面。


1. (使用Experience Cloud Identity Service的實作 `visitorAPI.js` 代碼)篩選依據 `/b/ss` 以檢視Analytics點選。

   ![篩選依據 `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (使用Experience Platform的實作 [!DNL Web SDK] `alloy.js`代碼)篩選依據 `/interact` 驗證傳送至Edge Network的要求裝載是否包含 `advertisingStitchID`.

   ![篩選依據 `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. 比較兩個點選之間的ID值。 除了在Analytics點選中的報表套裝ID （即緊接在後面的URL路徑）以外，所有值都會在查詢字串引數中 `/b/ss/`.

   | ID | Analytics引數 | 邊緣網路 | Adobe廣告引數 |
   | --- | --- | --- | --- |
   | Experience CloudIMS組織 | `mcorgid` |  | `_les_imsOrgid` |
   | 補充資料ID | sdid |  | `_les_sdid` |
   | 拼接ID | stitchId | `advertisingStitchID` 在 `_adcloud` 屬性 |  |
   | Analytics報表套裝 | 之後的值 `/b/ss/` |  | `_les_rsid` |
   | Experience Cloud訪客ID | mid |  | `_les_mid` |

   如果ID值相符，則會確認JavaScript實施。 Adobe廣告將傳送 [!DNL Analytics] 伺服器任何點進或檢視追蹤詳細資訊（如果存在）。

#### 如何使用確認程式碼 [!DNL Adobe Experience Cloud Debugger]

1. 開啟 [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) 在您首頁上。
1. 前往 [!UICONTROL Network] 標籤。
1. 在 [!UICONTROL Solutions Filter] 工具列，按一下 [!UICONTROL Adobe Advertising] 和 [!UICONTROL Analytics].
1. 在 [!UICONTROL Request URL – Hostname] 引數列，找出 `lasteventf-tm.everesttech.net`.
1. 在 [!UICONTROL Request – Parameters] 列，稽核產生的訊號，類似於&quot;[如何使用確認程式碼 [!DNL Chrome Developer Tools]](#validate-js-chrome).」
   * (使用Experience Cloud Identity Service的實作 `visitorAPI.js` 代碼)確認 `Sdid` 引數符合 `Supplemental Data ID` 在Adobe Analytics篩選中。
   * (使用Experience Platform的實作 [!DNL Web SDK] `alloy.js`代碼)確認 `advertisingStitchID` 引數符合 `Sdid` 傳送至Experience Platform邊緣網路。
   * 如果程式碼未產生，請檢查以確認AdobeAdvertising Cookie已移除 [!UICONTROL Application] 標籤。 移除後，請重新整理頁面並重複此程式。

   ![稽核 [!DNL Analytics for Advertising] 中的JavaScript程式碼 [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [實作的必要條件和關鍵資訊 [!DNL Analytics for Advertising]](prerequisites.md)

