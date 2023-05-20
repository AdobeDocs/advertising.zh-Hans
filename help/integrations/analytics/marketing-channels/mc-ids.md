---
title: 使用Adobe廣告ID來建立 [!DNL Marketing Channels] 規則
description: 瞭解如何使用Adobe廣告ID建立處理規則 [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# 使用Adobe廣告ID來建立 [!DNL Marketing Channels] 處理規則

*僅具有AdobeAdvertising-Adobe Analytics整合的廣告商*

您可以使用Adobe廣告ID ([AMO ID和EF ID](../ids.md))以設定 [!DNL Marketing Channels] Adobe Analytics中的處理規則。 將Adobe廣告ID用於您Adobe廣告行銷活動的特定規則。

## 處理規則中的AMO ID

AMO ID是主要追蹤程式碼，用來報告Adobe廣告資料 [!DNL Analytics]. AMO ID是由Adobe管理的動態值串連，可在中提供精細的報表 [!DNL Analytics]. 儲存在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar維度(AMO ID)。 AMO ID可設定於 [!DNL Analytics] 有兩種方式：

* 點進追蹤：Adobe廣告會將 `s_kwcid` 連結中的查詢字串引數，以及 [!DNL Analytics] 點進發生時，從登陸頁面URL中選取引數。
* 檢視追蹤([!DNL DSP] 僅限)： Last Event Service會偵測伺服器端的瀏覽次數，並將AMO ID傳送至 [!DNL Analytics]. 在此情況下，URL不包含 `s_kwcid` 引數。

AMO ID內的動態值表示所追蹤的行銷管道：

* AMO ID中的前置詞可用來識別內的頂層管道 [!DNL Marketing Channels].

* AMO ID內文中的字元短語表示更具體的促銷活動型別。

* 尾碼「vt」存在於 [!DNL DSP] 檢視流量，並可用來建立個別的點進和檢視 [!DNL DSP] 管道。

可忽略其餘的AMO ID。

| AMO ID | 頻道 | 規則邏輯 |
|--------|---------|--------------------|
| 艾爾！ （前置詞） | [!UICONTROL Paid Search] | 開頭為 |
| AC！ （前置詞） | [!UICONTROL DSP] | 開頭為 |
| ！g！ （內文） | [!UICONTROL Google Search] | 包含 |
| ！s！ （內文） | [!UICONTROL Search Partner] | 包含 |
| ！d！ （內文） | [!UICONTROL Display Network] | 包含 |
| ！u！ （內文） | [!UICONTROL Smart Shopping Campaign] | 包含 |
| ！ytv！ （內文） | [!UICONTROL YouTube Video Ad] | 包含 |
| ！yts！ （內文） | [!UICONTROL YouTube Search Ad] | 包含 |
| ！vp！ （內文） | [!UICONTROL Google Video Partners] | 包含 |
| ！vt （尾碼） | [!UICONTROL DSP View-through] | 結尾為 |

### 使用AMO ID的處理規則範例

此 [!DNL Marketing Channels] 的處理規則 [!UICONTROL Paid Search] 管道可能如下所示：

![範例 [!UICONTROL Paid Search] 規則](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

此 [!DNL Marketing Channels] 的處理規則 [!UICONTROL YouTube Video Ads] 管道可能如下所示：

![範例 [!UICONTROL YouTube Video Ads] 規則](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> 請務必依照特定順序執行規則。 如果以上兩個規則依序執行， [!DNL YouTube] 視訊廣告流量屬於 [!UICONTROL Paid Search] 頻道，因為AMO ID都會以「AL！」開頭 並包含「！ytv！」。

## 處理規則中的EF ID

AMO EF ID (EF ID)是 [!DNL Analytics for Advertising] 整合。 其主要用途是追蹤及通過 [!DNL Analytics] 將事件資料匯入Adobe廣告。 每次點進或檢視發生時，系統都會產生唯一的EF ID，即使同一位訪客擁有完全相同的廣告。 EF ID未用於 [!DNL Analytics] 報表使用者介面，因為它通常會超過中每個變數50萬個不重複值的限制 [!DNL Analytics]，導致其無法用於報表。 Adobe廣告量度和中繼資料不會套用至EF ID，只會套用至AMO ID。 Adobe廣告中的促銷活動最佳化需要新增追蹤的詳細程度，因此兩個ID都是必要的。

雖然EF ID維度不會直接用於 [!DNL Analytics] 報表，EF ID可用於建立行銷管道。 EF ID尾碼會指出頻道（顯示或搜尋），以及造訪是由點進還是檢視所驅動。 EF ID中的分隔符號是冒號，而不是AMO ID中的驚歎號。

| EF ID尾碼 | 頻道 |
|-------|---------|
| ：s | [!UICONTROL Paid Search] |
| ：d | [!UICONTROL Display Click-through] |
| ：i | [!UICONTROL Display View-through] |

### 使用EF ID的處理規則範例

#### 顯示點進規則

僅擷取點進次數，以建立「顯示」點進行銷管道。 由於點進和檢視的AMO ID相同，因此此規則會使用EF ID變數和 `ef_id` 查詢字串引數。

有時會透過URL （預設）追蹤點進。 在其他情況下，點進次數會透過伺服器端的「上次事件服務」進行追蹤，因此URL不包含 `ef_id` 引數。 因此，規則會檢查EF ID變數或 `ef_id` 查詢字串引數結尾是&quot;：d&quot;。 使用&quot;`Any`」運運算元，因為您想要為任一條件觸發此規則。

![顯示點進規則的範例](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### 顯示檢視規則

若要建立「顯示」檢視管道，請建立EF ID結尾為&quot;：i&quot;的規則。 由於訪客未點按廣告，瀏覽追蹤不會包含 `ef_id` 或 `s_kwcid` ，因此規則只需要一個條件。

![顯示瀏覽規則範例](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [的基礎知識 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [為何管道資料可能因Adobe廣告和以下內容而異 [!DNL Marketing Channels]](mc-data-variances.md)
>* [使用 [!DNL Analytics Marketing Channels] 使用Adobe廣告資料](mc-ac-data.md)
>* [影片：使用 [!DNL Marketing Channels] 適用於Adobe廣告報表](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [使用的Adobe廣告ID [!DNL Analytics]](/help/integrations/analytics/ids.md)

