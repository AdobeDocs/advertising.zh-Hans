---
title: 音訊廣告設定
description: 請參閱音訊廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# 音訊廣告設定

## [!UICONTROL Insert Ad Tag]

*僅限新廣告*

**[!UICONTROL URL]**：VAST標籤URL。

**[!UICONTROL Title]**：檔案的名稱，用於 [!UICONTROL Ads] 檢視和報告。

>[!TIP]
>
> 若要檢查VAST標籤的有效性，請將其貼到瀏覽器中並按一下 **[!UICONTROL Enter]** 金鑰。 如果標籤有效，您會看到包含的XML檔案 `<VAST>` 靠近頂端。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]：** （唯讀）您正在建立的廣告型別，與可附加廣告的位置型別相對應。 其預設值為 *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]：** 廣告名稱。 預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 當您在下列位置將廣告附加至位置時，請使用容易找到的名稱： [!UICONTROL Ads] 檢視，以及在報表中。 例如，說明單位型別和某些關鍵屬性（例如Holiday Product Preview： 30sec Audio」）。

**[!UICONTROL Ad Duration]：** 音訊檔案的長度。 會自動設定為 [!UICONTROL 15] 或 [!UICONTROL 30]，視選取的廣告單位而定。

此欄位不一定顯示，取決於帳戶許可權。

**[!UICONTROL VAST Tag]：** （僅使用VAST標籤的廣告）第三方廣告來源的URL。 請確定VAST標籤僅包含音訊媒體檔案。

**[!UICONTROL Final VAST Tag]：** （僅使用VAST標籤的廣告）第三方廣告來源的URL及必要的 [Advertising DSP追蹤巨集](/help/dsp/campaign-management/macros.md) 已插入（如果適用）。

**[!UICONTROL Select Rate]：** （僅限具有許可權的使用者）透過Adobe計費的預先議定費率，或您已經議定並將透過供應商計費的費率之一。 若要新增費率，請聯絡您的Adobe客戶團隊。

### 畫素

會自動附加位置的所有現有事件追蹤畫素。 您可以根據個別廣告的追蹤需求，分離現有畫素並根據需要建立新畫素。

下列設定會套用至您建立或編輯的每個畫素。

**[!UICONTROL Integration Event]：** 觸發畫素觸發的事件。 對於此廣告型別，請使用在 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]：** 畫素是否為 *[!UICONTROL IMG UR]L* （1x1畫素影像檔案）， *[!UICONTROL HTML]*，或 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]：** 畫素影像的URL，使用指定畫素型別的適當格式。

**[!UICONTROL Pixel Name]：** 畫素名稱。 使用可協助您輕鬆識別畫素的名稱。

**[!UICONTROL Pixel Provider]：** 畫素提供者： *[!UICONTROL None]*， *[!UICONTROL Nielsen]*，或 *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立單一廣告](ad-create.md)
>* [列出與廣告相關的版位](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [廣告規格](ad-specs.md)
>* [DSP巨集](/help/dsp/campaign-management/macros.md)

