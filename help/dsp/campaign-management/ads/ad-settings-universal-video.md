---
title: 通用視訊廣告設定
description: 請參閱通用視訊廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: 0c9e9c8d2a3444c623568d25262421be53c0c846
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# 通用視訊廣告設定

*開放Beta版功能*

>[!NOTE]
>
>通用視訊廣告只能附加至通用視訊位置。

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
> 當您在下列位置將廣告附加至位置時，請使用容易找到的名稱： [!UICONTROL Ads] 檢視，以及在報表中。 例如，說明單位型別和某些關鍵屬性（例如Holiday Product Preview： 30sec Universal Video）。

**[!UICONTROL Show Controls]：** 在何處加入廣告的視訊控制項： *[!UICONTROL Under]*， *[!UICONTROL Over]*， *[!UICONTROL Bottom]*，或 *[!UICONTROL None]* （預設）。

**[!UICONTROL Preserve Aspect Ratio]：** 是否保持視訊的寬度和高度比例(*[!UICONTROL Yes]*)或延伸視訊以填滿可用空間(*[!UICONTROL No]*)。

**[!UICONTROL VAST Tag]：** （僅使用VAST標籤的廣告；唯讀）您輸入作為廣告來源的第三方VAST標籤。

**[!UICONTROL Final VAST Tag]：** （僅使用VAST標籤的廣告；唯讀）您輸入作為廣告來源的第三方VAST標籤，並具有必要 [Advertising DSP追蹤巨集](/help/dsp/campaign-management/macros.md) 已插入（如果適用）。

**[!UICONTROL Wmode]：** 視窗模式： *[!UICONTROL window]*， *[!UICONTROL transparent]*，或 *[!UICONTROL opaque]*. 如果此設定不適用，請留空。

**[!UICONTROL Video Format]：** 潛在詳細目錄的廣告播放器格式： *[!UICONTROL VPAID]*， *[!UICONTROL VPAID & VAST]*，或 *[!UICONTROL VAST]*. 可檢視度一律會測量 [!UICONTROL VPAID]，但 [!UICONTROL VPAID & VAST] 包含不允許可檢視度測量的詳細目錄。 如果可見度量度對您的行銷活動很重要，請考慮此區別。

使用 [!UICONTROL VAST]，這不允許可檢視度測量，當您鎖定僅嚴格要求VAST格式的連線電視或詳細目錄時(通常來自Google Ad Manager、Appnexus、SpotX和Freewheel等供應來源)。 也請將此選項用於先前與標準前段廣告(VAST)或手機+平板電腦標準前段廣告(VAST)版位/廣告相容的詳細目錄。

**[!UICONTROL Clock Number]**：（僅於英國使用；僅供擁有許可權的使用者使用）唯一識別碼，用於確保廣播正確的廣告。 如果此設定不適用，請留空。

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
>* [關於通用視訊的常見問題集](/help/dsp/campaign-management/faq-universal-video.md)
>* [關於廣告管理](ad-about.md)
>* [建立單一廣告](ad-create.md)
>* [列出與廣告相關的版位](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [廣告規格](ad-specs.md)
>* [DSP巨集](/help/dsp/campaign-management/macros.md)

