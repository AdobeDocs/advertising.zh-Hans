---
title: 行動廣告設定
description: 請參閱行動廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: 45e8da8c-d6a2-4c42-8932-4cf551f6f899
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# 行動廣告設定

## [!UICONTROL Insert Ad Tag]

*僅限新的行動視訊廣告格式*

**[!UICONTROL URL]** 或 **[!UICONTROL Ad Tag]**：包含創意資產和追蹤畫素的第三方VAST廣告標籤或廣告標籤

**[!UICONTROL Ad Title]** 或 **[!UICONTROL Title]**：用於「 」的廣告名稱 [!UICONTROL Ads] 檢視和報告。

>[!TIP]
>
> 若要檢查VAST標籤的有效性，請將其貼到瀏覽器中並按一下 **[!UICONTROL Enter]** 金鑰。 如果標籤有效，您會看到包含的XML檔案 `<VAST>` 靠近頂端。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]：行動顯示廣告

**[!UICONTROL Ad Type]：** （唯讀）您正在建立的廣告型別，與可附加廣告的位置型別相對應。

**[!UICONTROL Ad Name]：** 廣告名稱。 預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 在廣告檢視和報表中，使用將廣告附加至版位時容易找到的名稱。 例如，說明單位型別和某些關鍵屬性（例如Holiday Product Preview： 300x250 Gamer」）。

**\[廣告來源\]**：（唯讀） *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]：** 第三方創意資產的URL。 任何 [timestamp] 和[[timestamp]]引數將被實際值取代。

**[!UICONTROL Final Display Code]：** 協力廠商創意資產的URL，帶有必要的 [Advertising DSP追蹤巨集](/help/dsp/campaign-management/macros.md) 已插入（如果適用）。

### [!UICONTROL Basic]：視訊廣告

**[!UICONTROL Ad Type]：** （唯讀）您正在建立的廣告型別，與可附加廣告的位置型別相對應。

**[!UICONTROL Ad Name]：** 廣告名稱。 預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 在廣告檢視和報表中，使用將廣告附加至版位時容易找到的名稱。 例如，說明單位型別和某些關鍵屬性（例如Holiday Product Preview： 30sec Phone Preroll）。

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]：** 整個廣告單位的寬度。 此選項可能會根據您選取的廣告單位型別而鎖定。

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]：** 整個廣告單位的高度。 此選項可能會根據您選取的廣告單位型別而鎖定。

**[!UICONTROL Player X]：** 廣告單位的X座標。 保留預設設定。

**[!UICONTROL Player Y]：** 廣告單位的Y座標。 保留預設設定。

**[!UICONTROL Player Width]：** 整個廣告單位的寬度。 此選項可能會根據您選取的廣告單位型別而鎖定。

這與 **[!UICONTROL Width]** 欄位。

**[!UICONTROL Player Height]：** 整個廣告單位的高度。 此選項可能會根據您選取的廣告單位型別而鎖定。

這與 **[!UICONTROL Height]** 欄位。

**[!UICONTROL Show Controls]：** 在何處加入廣告的視訊控制項： *[!UICONTROL Under]*， *[!UICONTROL Over]*， *[!UICONTROL Bottom]*，或 *[!UICONTROL None]* （預設）。

**[!UICONTROL Preserve Aspect Ratio]：** 是否要保持視訊的寬度和高度比例(*[!UICONTROL Yes]*)或延伸視訊以填滿可用空間(*[!UICONTROL No]*)。

**[!UICONTROL Close Button Delay]：** （部分廣告型別）延遲關閉按鈕出現的秒數。

**[!UICONTROL VAST Tag]：** （僅使用VAST標籤的廣告；唯讀）您輸入作為創意資產的第三方VAST標籤。

**[!UICONTROL Final VAST Tag]：** （僅使用VAST標籤的廣告；唯讀）您輸入為創意資產的第三方VAST標籤，且具備必要 [Advertising DSP追蹤巨集](/help/dsp/campaign-management/macros.md) 已插入（如果適用）。

**[!UICONTROL Wmode]：** （部分廣告型別）視窗模式： *[!UICONTROL window]*， *[!UICONTROL transparent]*，或 *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

會自動附加位置的所有現有事件追蹤畫素。 您可以根據個別廣告的追蹤需求，分離現有畫素並根據需要建立新畫素。

下列設定會套用至您建立或編輯的每個畫素。

**[!UICONTROL Integration Event]：** 觸發畫素觸發的事件。 對於此廣告型別，請使用在 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]：** 畫素是否為 *[!UICONTROL IMG URL]* （1x1畫素影像檔案）， *[!UICONTROL HTML]*，或 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]：** 畫素影像的URL，以指定的適當格式顯示 [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]：** 畫素名稱。 使用可協助您輕鬆識別畫素的名稱。

**[!UICONTROL Pixel Provider]：** 畫素提供者： *[!UICONTROL None]*， *[!UICONTROL Nielsen]*，或 *[!UICONTROL Comscore]*.

### [!UICONTROL Sharing]

已棄用

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立單一廣告](ad-create.md)
>* [列出與廣告相關的版位](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [廣告規格](ad-specs.md)
>* [DSP巨集](/help/dsp/campaign-management/macros.md)

