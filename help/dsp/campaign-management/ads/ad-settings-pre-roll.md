---
title: 前段廣告設定
description: 請參閱前段廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: d0ba4346-13ae-405c-92b6-a0c32dd09d0a
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# 前段廣告設定

## [!UICONTROL Insert Ad Tag]

*僅限新廣告*

**[!UICONTROL URL]：** VAST標籤URL。

**[!UICONTROL Title]：** 檔案的標題，位於 [!UICONTROL Ads] 檢視和報告。

>[!TIP]
>
> 若要檢查VAST標籤的有效性，請將其貼到瀏覽器中並按一下 **[!UICONTROL Enter]** 金鑰。 如果標籤有效，您會看到包含的XML檔案 `<VAST>` 靠近頂端。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]：** （唯讀）您正在建立的廣告型別，與可附加廣告的位置型別相對應。

**[!UICONTROL Ad Name]：** 廣告名稱。 預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 當您在下列位置將廣告附加至位置時，請使用容易找到的名稱： [!UICONTROL Ads] 檢視，以及在報表中。 例如，說明單位型別和某些關鍵屬性（例如Holiday Product Preview： 30sec Preroll）。

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]：** （僅限標準和可略過的前段廣告）整個廣告單位的寬度。 此選項可能會根據您選取的廣告單位型別而鎖定。

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]：** （僅限標準和可略過的前段廣告）整個廣告單位的高度。 此選項可能會根據您選取的廣告單位型別而鎖定。

**[!UICONTROL Player X]：** 廣告單位的X座標。 保留預設設定。

**[!UICONTROL Player Y]：** 廣告單位的Y座標。 保留預設設定。

**[!UICONTROL Player Width]：** 整個廣告單位的寬度。 此選項可能會根據您選取的廣告單位型別而鎖定。

此欄位與 **[!UICONTROL Width]** 欄位。

**[!UICONTROL Player Height]：** 整個廣告單位的高度。 此選項可能會根據您選取的廣告單位型別而鎖定。

這與 **[!UICONTROL Height]** 欄位。

**[!UICONTROL Show Controls]：** 在何處加入廣告的視訊控制項： *[!UICONTROL Under]*， *[!UICONTROL Over]*， *[!UICONTROL Bottom]*，或 *[!UICONTROL None]* （預設）。

**[!UICONTROL Preserve Aspect Ratio]：** 是否保持視訊的寬度和高度比例(*[!UICONTROL Yes]*)或延伸視訊以填滿可用空間(*[!UICONTROL No]*)。

**[!UICONTROL VAST Tag]：** （僅使用VAST標籤的廣告；唯讀）您輸入作為廣告來源的第三方VAST標籤。

**[!UICONTROL Final VAST Tag]：** （僅使用VAST標籤的廣告；唯讀）您輸入作為廣告來源的第三方VAST標籤，並具有必要 [Advertising DSP追蹤巨集](/help/dsp/campaign-management/macros.md) 已插入（如果適用）。

**[!UICONTROL Wmode]：** （僅限互動式前段）視窗模式： *[!UICONTROL window]*， *[!UICONTROL transparent]*，或 *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]：** （僅限互動式前段廣告）潛在詳細目錄的廣告播放器格式： *[!UICONTROL VPAID]* 或 *[!UICONTROL VPAID & VAST]*. 可檢視度一律以VPAID來測量，但VPAID和VAST包含不允許可檢視度測量的詳細目錄。 如果可見度量度對您的行銷活動很重要，請考慮此區別。

**[!UICONTROL Clock Number]**：（僅限互動式前段廣告；僅於英國使用；僅供擁有許可權的使用者使用）唯一識別碼，用於確保廣播正確的廣告。 如果此設定不適用，請留空。

### [!UICONTROL Pixel]

會自動附加位置的所有現有事件追蹤畫素。 您可以根據個別廣告的追蹤需求，分離現有畫素並根據需要建立新畫素。

下列設定會套用至您建立或編輯的每個畫素。

**[!UICONTROL Integration Event]：** 觸發畫素觸發的事件。 對於此廣告型別，請使用在 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]：** 畫素是否為 *[!UICONTROL IMG URL]* （1x1畫素影像檔案）， *[!UICONTROL HTML]*，或 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]：** 畫素影像的URL，以指定的適當格式顯示 [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]：** 畫素名稱。 使用可協助您輕鬆識別畫素的名稱。

**[!UICONTROL Pixel Provider]：** 畫素提供者： *[!UICONTROL None]*， *[!UICONTROL Nielsen]*，或 *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立單一廣告](ad-create.md)
>* [列出與廣告相關的版位](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [廣告規格](ad-specs.md)
>* [DSP巨集](/help/dsp/campaign-management/macros.md)

