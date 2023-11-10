---
title: 使用 [!DNL Last Event Service] JavaScript库与 [!DNL Web SDK]
description: 了解从使用切换的步骤 [!DNL Analytics] [!DNL visitorAPI] 库到 [!DNL Experience Platform] [!DNL Web SDK] 您的库 [!DNL Analytics for Advertising] 实现。
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: 687f146b27765d59f172284e4cff7ab5c0e57b50
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# 使用 [!DNL Last Event Service] JavaScript库和Adobe Experience Platform [!DNL Web SDK]

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

如果您的组织使用旧版Adobe Analytics `visitorAPI.js` 库进行数据收集，您可以选择使用 [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) 库(`alloy.js`Experience Cloud )，从而允许您通过 [!DNL Edge Network].

此 [!DNL Analytics for Advertising] [!DNL Last Event Service] JavaScript库（按原样）记录浏览转化和点进事件，并使用补充ID (`SDID`)。 此 [!DNL Web SDK] 但是，库不提供 [!DNL stitch ID]. 要使用 [!DNL Web SDK] 对象 [!DNL Analytics for Advertising]，您需要修改1) [!DNL Last Event Service] 标记您的网页，以及2) [!DNL Web SDK] `sendEvent` 相应的命令。

## 第1步：编辑您的 [!DNL Last Event Service] 标记以生成 `[!DNL StitchID]`

在 [!DNL Analytics for Advertising] [!DNL Last Event Service] 标记您对网页使用的标记，添加代码以生成 `[!DNL StitchID]` 使用捆绑在库中的随机ID生成器。

**旧标记：**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

**新标记：**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id''rsid').generateRandomId();
</script>
```

## 步骤2：使用 [!DNL Web SDK] 发送 [!DNL StitchID] 作为XDM数据 [!DNL Analytics]

将以下属性插入您的 [!DNL Web SDK] `sendEvent` 命令发送 [!DNL StitchID] 到 [!DNL Experience Edge] 作为 [!DNL Experience Data Model] (XDM)数据用于 [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] 将使用值作为 `SDID`.

**要添加的属性：**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**示例：**

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
>* [JavaScript代码 [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)
