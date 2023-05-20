---
title: 使用 [!DNL Last Event Service] JavaScript程式庫，搭配 [!DNL Web SDK]
description: 瞭解從使用的切換步驟 [!DNL Analytics] [!DNL visitorAPI] 資料庫至 [!DNL Experience Platform] [!DNL Web SDK] 您的資料庫 [!DNL Analytics for Advertising] 實作。
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# 使用 [!DNL Last Event Service] 使用Adobe Experience Platform的JavaScript資料庫 [!DNL Web SDK]

*僅具有AdobeAdvertising-Adobe Analytics整合的廣告商*

如果您的組織使用舊版Adobe Analytics `visitorAPI.js` 資料收集程式庫，您可以選擇使用 [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) 資料庫(`alloy.js`Experience Cloud )，可讓您透過 [!DNL Edge Network].

此 [!DNL Analytics for Advertising] [!DNL Last Event Service] JavaScript程式庫（依現狀）會記錄檢視和點進事件，並使用補充ID (`SDID`)。 此 [!DNL Web SDK] 然而，程式庫不提供 [!DNL stitch ID]. 若要使用 [!DNL Web SDK] 的 [!DNL Analytics for Advertising]，您需要修改1) [!DNL Last Event Service] 標籤您用於網頁上，以及2)您的 [!DNL Web SDK] `sendEvent` 命令相應。

## 步驟1：編輯您的 [!DNL Last Event Service] 標籤以產生 `[!DNL StitchID]`

在 [!DNL Analytics for Advertising] [!DNL Last Event Service] 標籤您使用的網頁，新增程式碼以產生 `[!DNL StitchID]` 使用隨機ID產生器（隨附於程式庫中）。

**舊版標籤：**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

**新標籤：**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

## 步驟2：使用 [!DNL Web SDK] 傳送 [!DNL StitchID] 作為XDM資料 [!DNL Analytics]

將下列屬性插入 [!DNL Web SDK] `sendEvent` 命令以傳送 [!DNL StitchID] 至 [!DNL Experience Edge] 作為 [!DNL Experience Data Model] (XDM)資料 [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] 會使用值做為 `SDID`.

**要新增的屬性：**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**範例：**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript程式碼 [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)

