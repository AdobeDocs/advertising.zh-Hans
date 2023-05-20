---
title: 自訂報表設定
description: 請參閱自訂報表設定的說明。
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: 2e0240ff1b342d5a0564e01ebec3ee313b488b59
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 0%

---

# 自訂報表設定

**[!UICONTROL Name]** 報表名稱。 長度上限為180個字元。

**[!UICONTROL Report Type]** 報表型別： *[!UICONTROL Custom]* （包括最可用的選項）、 *[!UICONTROL Billing]*， *[!UICONTROL Conversion]*， *[!UICONTROL Device]*， *[!UICONTROL Frequency (by Impression)]*，  *[!UICONTROL Frequency (by App/Site)]*， *[!UICONTROL Geo]*， *[!UICONTROL Margin]*， *[!UICONTROL Media Performance]*，  *[!UICONTROL Segment]*， *[!UICONTROL Site]*，或 *[!UICONTROL Household]*.

## [!UICONTROL Apply Filters] 章節

**[!UICONTROL Timezone]：** 報表的時區。

**[!UICONTROL Observe Daylight Savings Time]：** 考量報告時間中的日光節約時間。

**\[日期範圍\]：** 要產生資料的日期範圍。 可用天數因報表和所選維度而異。 選擇一項：

* **[!UICONTROL Previous N days]：** 包含今天之前特定天數的資料。

* **[!UICONTROL Custom]：** 包含特定開始和結束日期之間的資料。 若要報告前一天的資料，請選取 **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]：** 包含上一個日曆月的資料。

**[!UICONTROL Add Filters]：** （選用）篩選資料所依據的其他維度，無論這些維度是否作為欄包含在報表中。 可用的篩選器因報告型別而異，可能包括： *[!UICONTROL Account]*\*， *[!UICONTROL Ad Type]*， *[!UICONTROL Ads]*， *[!UICONTROL Advertiser]*， *[!UICONTROL Campaign]*， *[!UICONTROL Country]*， * *[!UICONTROL Package]*， *[!UICONTROL Placement]*， *[!UICONTROL Video]*、和 *[!UICONTROL Video Duration]*.

\* *[!UICONTROL Account]* 只有當您的組織設定為時，才可用於以下報表型別 [跨帳戶報告](report-about.md#cross-account-reporting)：  [!UICONTROL Custom]， [!UICONTROL Site]， [!UICONTROL Segment]， [!UICONTROL Geo]， [!UICONTROL Device]， [!UICONTROL Frequency (by Impression)]、和 [!UICONTROL Conversion]. 如需跨帳戶報告的詳細資訊，請聯絡您的Adobe客戶團隊。

若要套用一或多個篩選器，請執行下列動作：

* 選取維度，然後選取運運算元(*等於* 或 *不等於*)，然後選取適用的值。 例如，若只要傳回前段廣告的資料，請指定&quot;[!UICONTROL Ad Type equals Preroll].」
* （選用）將其他條件新增至篩選器。
* （選用）新增其他篩選器，每個篩選器一或多個條件。

## [!UICONTROL Build Your Report] 章節

**[!UICONTROL Select To Add As Report Headers]：**  要納入報表中的資料欄或標題。 若要新增欄，請展開類別並選取欄名稱旁的核取方塊。 可用欄會因報告而異，並且所有無法使用的量度都會停用。 可用的資料類別包括：

* [!UICONTROL Dimensions]

   >[!NOTE]
   >
   > 此 [!UICONTROL Household] 報表只能包含一個維度。

* [!UICONTROL Metrics]

   >[!NOTE]
   >
   >此 [!UICONTROL Household] 報表可包含重疊量度或非重疊量度，但不能同時包含兩者。

* [!UICONTROL Conversion Metrics] （依廣告商排序）

* [!UICONTROL Custom Goals] （依廣告商排序）

請參閱「[可用的報告欄](report-columns.md)」以取得所有選項的說明。

**[!UICONTROL Drag to Re-Order Report Headers Below]：** 欄標題的順序。 您可以拖放任何欄來自訂順序。

## [!UICONTROL Multi-Touch Conversion Options] 章節

**[!UICONTROL Format]：** 是否在中產生報表 *[!UICONTROL CSV]* （逗號分隔值）或 *[!UICONTROL Tab]* （以Tab分隔的值）格式。

**[!UICONTROL Report Headers]：** 是否要 *[!UICONTROL Include]* 或 *[!UICONTROL Do Not Include]* 欄標題。

**[!UICONTROL Attribution Rule Settings]：** (全部 [!UICONTROL Custom]， [!UICONTROL Conversion]， [!UICONTROL Device]， [!UICONTROL Geo]， [!UICONTROL Segment]、和 [!UICONTROL Site] 報告 [!UICONTROL Conversion Metrics] 或 [!UICONTROL Custom Goals] 欄；僅具有Adobe廣告轉換追蹤的廣告商)在報表中，如何將轉換資料歸因於一連串導致轉換的事件。 如果要比較規則之間的差異，您可以選擇多個規則。

>[!NOTE]
>
>轉換路徑包含廣告商曝光次數或點按回顧期間內的任何曝光次數和點按，這些設定於 [!DNL Advertising Search, Social, & Commerce]. 在轉換歸因期間，點按次數會優先於曝光次數。 根據歸因規則，轉換路徑中的任何點按都會獲得完整評價。 只有轉換路徑中未追蹤任何點選時，曝光次數才會獲得評分。

* *[!UICONTROL Last Event]：* 將轉換歸因於轉換路徑中的最後點按或印象。

* *[!UICONTROL Weight Last More]：* 將轉換歸因於轉換路徑中的所有事件，但給予最後一個事件最多的權重，並連續給予前一個事件較少的權重。

* *[!UICONTROL Even Distribution]：* 將轉換同等地歸因於轉換路徑中的每個事件。

* *[!UICONTROL Weight First More]：* 將轉換歸因於轉換路徑中的所有事件，但給予第一個事件最多的權重，並連續給予以下事件較少的權重。

* *[!UICONTROL First Event]：* 將轉換歸因於轉換路徑中的第一次點按或印象。

* *[!UICONTROL U-shaped]：* 將轉換歸因於轉換路徑中的所有事件，但給予第一個和最後一個事件的權重最大，連續給予轉換路徑中間事件的權重較小。

* *[!UICONTROL Display Only]：*  將轉換歸因於轉換路徑中的上次DSP點按或印象。 這包括視訊和連線電視廣告，並排除點按 [!DNL Advertising Search, Social, & Commerce] 廣告。

* *[!UICONTROL Social Only]：* 已過時

<!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

**[!UICONTROL Paths as Columns]：**  (全部 [!UICONTROL Custom]， [!UICONTROL Conversion]， [!UICONTROL Device]， [!UICONTROL Geo]， [!UICONTROL Segment]、和 [!UICONTROL Site] 報告 [!UICONTROL Conversion Metrics] 或 [!UICONTROL Custom Goals] 欄)相同裝置上發生先前事件時要報告的轉換型別。 您最多可以包含三種型別。 對於每個選取的型別，每個轉換量度都會有一個單獨的欄，並附加指定的尾碼([!UICONTROL (tl)]， [!UICONTROL (ct)]，或 [!UICONTROL (vt)])：

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]：* 包含歸因於點按次數（點進為CT）和曝光數（點進為VT）的轉換。 歸屬於曝光的轉換次數會乘以指定的瀏覽權數。 預設的閱覽權重為100%，這表示歸屬於曝光的轉換會計算為歸屬於點按的轉換值的100%。

* *[!UICONTROL With Clicks (CT)]：* 僅包含歸因於點按的轉換。

* *[!UICONTROL Impressions Only (VT)]：* 僅包含歸屬於曝光次數的轉換，因為轉換路徑中未追蹤任何點按。

**[!UICONTROL Conversion Reporting Based On]：**  如何報告轉換資料：

* *[!UICONTROL Conversion Timestamp]：* （預設）轉換將與轉換日期相關聯。

* *[!UICONTROL Event Timestamp]：* 系統會根據造成轉換的曝光或點按日期（由指定的決定）報告轉換 [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Report Destinations] 章節

**[!UICONTROL Destination Type]：** 選擇下列其中一個目的地型別：

* *[!UICONTROL S3]：* 若要將完成的報表傳送至一或多個 [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3])位置，您會在 **[!UICONTROL Destination Name]** 欄位。
* *[!UICONTROL sFTP]：* 若要將完成的報表傳送至一或多個SFTP位置，您將會在 **[!UICONTROL Destination Name]** 欄位。
* *[!UICONTROL FTP]：* 若要將完成的報表傳送至一或多個FTP位置，您將會在 **[!UICONTROL Destination Name]** 欄位。
* *[!UICONTROL FTP SSL]（目前為測試版）：* 若要將完成的報表傳送至一或多個FTP SSL位置，您將會在 **[!UICONTROL Destination Name]** 欄位。
* *[!UICONTROL Email]：* 若要指定電子郵件位址，以便在報告因錯誤而取消時，將已完成的報告或通知傳送至該位址。 若要指定多個地址，請以逗號或空格加以分隔。

>[!NOTE]
>
> 儲存報表後，就無法變更目的地型別。

**[!UICONTROL Destination Name]：** （僅限S3、FTP、sFTP和FTP SSL目的地型別）自訂報表將傳送到的報表目的地名稱。

* 若要指定現有的目的地，請從清單中選取一個目的地名稱。 您可以分別選取多個目的地名稱。

* 若要建立新的目的地：

   1. 按一下 **新增目的地**.

   1. 輸入 [報表目的地設定](/help/dsp/reports/report-destinations/report-destination-settings.md)，然後按一下 **儲存**.

   1. 返回報表設定，按一下 **重新整理目的地名稱。**

      新目的地現在可從現有目的地的清單中使用，並且您可以選擇將其新增到報表。

**[!UICONTROL Frequency]：** (針對每個 [!UICONTROL Destination Name] 將報表傳送至目的地的頻率： *[!UICONTROL Once]*， *[!UICONTROL Daily]*， *[!UICONTROL Weekly]*，或 *[!UICONTROL Monthly]*.

## [!UICONTROL Save Report] 章節

**[!UICONTROL Send & Save]：** 何時傳送報表： *[!UICONTROL On Schedule]* 或 *[!UICONTROL Run Now]*. 排程報表將於09:00前在帳戶的時區傳送。

>[!NOTE]
>
>您可以 [隨時執行自訂報表](report-run-now.md) 從 [!UICONTROL Reports] 檢視。

>[!MORELIKETHIS]
>
>* [關於自訂報表](/help/dsp/reports/report-about.md)
>* [建立自訂報表](/help/dsp/reports/report-create.md)
>* [複製自訂報表](/help/dsp/reports/report-copy.md)
>* [編輯自訂報告](/help/dsp/reports/report-edit.md)
>* [執行自訂報表](/help/dsp/reports/report-run-now.md)
>* [自訂報表設定](/help/dsp/reports/report-settings.md)
>* [關於報表目的地](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [可用的報告欄](/help/dsp/reports/report-columns.md)

