---
title: 原生顯示廣告設定
description: 請參閱原生顯示廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: 64ce1946-072d-4ca9-b3a8-348987580403
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# 原生顯示廣告設定

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]：** （唯讀）您正在建立的廣告型別，與可附加廣告的位置型別相對應。

**[!UICONTROL Ad Name]：** 廣告名稱。 預設會使用廣告型別，但您可以變更名稱。

>[!TIP]
>
> 當您在下列位置將廣告附加至位置時，請使用容易找到的名稱： [!UICONTROL Ads] 檢視，以及在報表中。 例如，說明單位型別和某些關鍵屬性（例如Holiday Product Preview： 15sec Native&quot;）。

**[!UICONTROL Native Creative]：** 1200x627的影像，可最大化行動庫存的傳遞。 按一下 **[!UICONTROL Browse]** 並在您的裝置或網路上找到檔案，然後按一下 **[!UICONTROL Upload]**.

**[!UICONTROL Title]：** 吸引目光的標題可吸引檢視者。

**[!UICONTROL Description]：** 廣告內文。 長度上限為100個字元。

**[!UICONTROL Landing Page]：** 檢視者按一下廣告時所登陸的URL。

**[!UICONTROL Final Landing Page]：** 此 [!UICONTROL Landing Page] 具有必要的URL [Advertising DSP追蹤巨集](/help/dsp/campaign-management/macros.md) 已插入（如果適用）。

**[!UICONTROL Sponsored By (Advertiser Name)]：** 廣告商。

**[!UICONTROL Call to Action]：** （選用）觀看者看到此廣告後，所要採取的步驟。

**[!UICONTROL Advertiser Logo]：** （選用）廣告中應包含1:1比例的標誌，以獲得更多品牌認知度。 按一下 **[!UICONTROL Browse]** 並在您的裝置或網路上找到檔案，然後按一下 **[!UICONTROL Upload]**.

### [!UICONTROL Pixel]

會自動附加位置的所有現有事件追蹤畫素。 您可以根據個別廣告的追蹤需求，分離現有畫素並根據需要建立新畫素。

下列設定會套用至您建立或編輯的每個畫素。

**[!UICONTROL Integration Event]：** 觸發畫素觸發的事件。 對於此廣告型別，唯一選項為 *[!UICONTROL Impression]*.

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

