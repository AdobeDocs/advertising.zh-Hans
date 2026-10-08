---
title: 将[!DNL Last Event Service] JavaScript库与[!DNL Web SDK]一起使用
description: 了解从使用[!DNL Analytics] [!DNL visitorAPI]库切换到[!DNL Analytics for Advertising]实施的[!DNL Experience Platform] [!DNL Web SDK]库的步骤。
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
TQID: 'https://experienceleague.adobe.com/zT1lQV1yotCfJJdzTBGzSspsNEKQEB5ulxYE0qyWa9Q'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: f2860a4b-f905-4545-bead-1bbc92564592
    internal-label: Advertising integrations
subfeature_v2:
  - id: cfd751d4-ee56-4323-8fd1-dc174b031709
    internal-label: Analytics integration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%
---
# 在Adobe Experience Platform [!DNL Web SDK]中使用[!DNL Last Event Service] JavaScript库

*仅集成Adobe Advertising-Adobe Analytics的广告商*

如果您的组织使用旧版Adobe Analytics `visitorAPI.js`库进行数据收集，则可以选择转为使用[Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hans)库(`alloy.js`)，这允许您通过[!DNL Edge Network]与各种Adobe CX Enterprise服务进行交互。

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
>*  [!DNL Analytics for Advertising]&#x200B;[&#128279;](/help/integrations/analytics/javascript.md)的JavaScript代码
