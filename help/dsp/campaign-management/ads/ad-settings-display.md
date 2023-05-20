---
title: 顯示廣告設定
description: 請參閱顯示廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# 顯示廣告設定

下列設定適用於標準顯示廣告。

## [!UICONTROL Ad Options]

### 基本

**[!UICONTROL Ad Type]：** （唯讀）您正在建立的廣告型別，與可附加廣告的位置型別相對應。 其預設值為 *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]：** 廣告名稱。 預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 當您在下列位置將廣告附加至位置時，請使用容易找到的名稱： [!UICONTROL Ads] 檢視，以及在報表中。 例如，說明單位型別和某些關鍵屬性（例如Holiday Product Preview： 300x250 Gamer」）。

**\[廣告來源\]**：（唯讀） *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]：** （僅限協力廠商廣告）指出廣告是可展開的橫幅廣告。 相關的擴充設定會決定要購買哪個存貨，因此請確定它們反映了廣告行為。

**[!UICONTROL Expansion Method]：** （僅限協力廠商可展開的橫幅廣告）橫幅是否展開於 *[!UICONTROL Click]* 或 *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]：** （僅限協力廠商可展開的橫幅廣告）廣告展開的方向： *[!UICONTROL Up]*， *[!UICONTROL Down]*， *[!UICONTROL Left]*，或 *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]：** （僅限協力廠商可展開的橫幅廣告）提供廣告的認證廠商： *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers])， *[!UICONTROL Flashtalking]*， *[!UICONTROL Sizmek]*，或 *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]：** （僅限第三方廣告）第三方創意資產的URL。 任何 [timestamp] 和[[timestamp]]引數將被實際值取代。

**[!UICONTROL Final Display Code]：** （僅限協力廠商廣告）協力廠商創意資產的URL，帶有必要的 [Advertising DSP追蹤巨集](/help/dsp/campaign-management/macros.md) 已插入（如果適用）。

**[!UICONTROL Ad Size]：** 廣告的寬度和高度。 它必須是 [支援的標準顯示廣告大小](ad-specs.md). 您可以在上傳廣告前手動輸入廣告大小，或輸入 [!UICONTROL Display Code]. 如果您未輸入廣告大小，上傳的廣告或廣告標籤的維度會自動輸入為唯讀。 請注意，如果尺寸不在標準顯示範圍內，顯示廣告不會儲存為大小 — 例如301x250而不是300x250廣告大小。

>[!IMPORTANT]
>
> 在寬度和高度欄位中宣告的廣告大小將與傳入的競標要求相符。 如果廣告的維度不符合宣告的廣告大小，您可能會遇到傳送問題。

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
>* [列出與廣告相關的版位](ad-list-placements.md)
>* [廣告規格](ad-specs.md)
>* [DSP巨集](/help/dsp/campaign-management/macros.md)

