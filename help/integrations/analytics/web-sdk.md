---
title: 将 [!DNL Last Event Service] JavaScript库与 [!DNL Web SDK]一起使用
description: 了解从使用 [!DNL Analytics] [!DNL visitorAPI]库转为使用 [!DNL Analytics for Advertising] 实施的 [!DNL Experience Platform] [!DNL Web SDK]库的步骤。
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# 在Adobe Experience Platform [!DNL Web SDK]中使用[!DNL Last Event Service] JavaScript库

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

如果您的组织使用旧版Adobe Analytics `visitorAPI.js`库进行数据收集，则可以选择使用[Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html)库(`alloy.js`)进行切换，这允许您通过[!DNL Edge Network]与各种Experience Cloud服务进行交互。

[!DNL Analytics for Advertising] [!DNL Last Event Service] JavaScript库按原样记录浏览和点进事件，并使用补充ID (`SDID`)将它们与关联的转化拼合。 但是，[!DNL Web SDK]库不提供[!DNL stitch ID]。 要为[!DNL Analytics for Advertising]使用[!DNL Web SDK]，必须修改1)您在网页上使用的[!DNL Last Event Service]标记和2)相应的[!DNL Web SDK] `sendEvent`命令。

## 步骤1：编辑您的[!DNL Last Event Service]标记以生成`[!DNL StitchID]`

在网页上使用的[!DNL Analytics for Advertising] [!DNL Last Event Service]标记中，添加代码以使用库中捆绑的随机ID生成器生成`[!DNL StitchID]`。

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
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

## 步骤2：使用[!DNL Web SDK]将[!DNL StitchID]作为[!DNL Analytics]的XDM数据发送

在您的[!DNL Web SDK] `sendEvent`命令中插入以下属性，以将[!DNL StitchID]作为[!DNL Analytics].<!-- The library sends the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. -->的[!DNL Experience Data Model] (XDM)数据发送到[!DNL Experience Edge] [!DNL Analytics]将该值用作`SDID`。

要添加的&#x200B;**属性：**

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
>*  [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)的[JavaScript代码
