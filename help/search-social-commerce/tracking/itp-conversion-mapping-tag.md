---
title: Adobe Advertising转换映射标记
description: 了解适用于ITP 2.2的基于JavaScript的转化映射标记，该标记允许Adobe Advertising跟踪在非登陆页面发生的转化事件。
exl-id: cbeaf3cd-f1ab-419d-bba8-58a1c8215352
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Adobe AdvertisingJavaScript转化映射标记

*仅跟踪Adobe Advertising转化情况的广告商*

在与Adobe AdvertisingJavaScript v2或v3转化跟踪标记一起使用时，基于JavaScript的转化映射标记可让Adobe Advertising跟踪在非Adobe Advertising上发生的转化事件。 ITP 2.2解决方案将用户的Cookie存储在广告商拥有的iFrame中的本地存储中。 然后，本地存储可以保留Cookie值（从点击下游到转化页面）。

使用转化映射标记可确保Adobe Advertising可跟踪在Apple Safari和Mozilla Firefox浏览器内发生的所有转化，从而限制第一方Cookie的持久性。<!-- For all requirements to track conversions from Safari, see "Track Conversions from Apple Safari Browsers." -->

要使用转换映射标记，请执行以下操作：

1. [部署转换映射标记](#deploy-conversion-mapping-tag)。

1. 如果贵组织使用多个Adobe Experience Cloud Identity Service组织ID（以前称为IMS组织ID），请[更新转化标记](#update-conversion-tags)以包含组织ID。

1. [验证标记部署](#validate-conversion-mapping)。

## 为ITP 2.2部署JavaScript转化映射标记 {#deploy-conversion-mapping-tag}

>[!NOTE]
>
>如果您正在为ITP 2.0使用JavaScript转化映射标记，请用以下标记之一替换所有转化页面中的现有标记。<!-- any other instructions, too? Point them to the other page on Track Conversions from Safari...." -->

* 如果您的组织使用单个组织ID(用于您的Search、Social和Commerce帐户)，请使用以下标记：

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" userid="{AMO User ID}"></script>`

  其中，您将`{AMO User ID}`替换为搜索、社交和Commerce帐户的唯一用户ID。

* 如果您的组织使用多个组织ID，请使用以下标记：

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="{xxxxxx@AdobeOrg}" userid="{AMO User ID}"></script>`

  其中：

   * 将值`{xxxxxx@AdobeOrg}`替换为要跟踪页面转化的组织ID。 对所有转化页面使用相同的组织ID。

   * 您将`{AMO User ID}`替换为您的搜索、社交和Commerce帐户的唯一用户ID。

* 如果您使用的标记管理系统不支持将`imsorgid`变量添加到脚本标记，请改用以下代码：

  *如果您的组织使用单个组织ID：

  ```
  <script>
  window.ad_cloud = window.ad_cloud || {};
  window.ad_cloud.userid = "{AMO User ID}"
  </script>
  <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
  ```

  其中，您将`{AMO User ID}`替换为搜索、社交和Commerce帐户的唯一用户ID。

   * 如果您的组织使用多个组织ID：

     ```
     <script>
     window.ad_cloud = window.ad_cloud || {};
     window.ad_cloud.imsorgid = "{xxxxxx@AdobeOrg}"
     window.ad_cloud.userid = "{AMO User ID}"
     </script>
     <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
     ```

     其中：

      * 将值`{xxxxxx@AdobeOrg}`替换为要跟踪页面转化的组织ID。 对所有转化页面使用相同的组织ID。

      * 您将`{AMO User ID}`替换为您的搜索、社交和Commerce帐户的唯一用户ID。

如果您不知道组织ID或Search、Social和Commerce用户ID的值，请咨询您的Adobe客户经理。

### 示例

```
<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="abc12345@AdobeOrg" userid="99999"></script>`
```

```
<script>
window.ad_cloud = window.ad_cloud || {};
window.ad_cloud.imsorgid = "abc12345@AdobeOrg"
window.ad_cloud.userid = "99999"
</script>
<script src="//www.everestjs.net/static/amo-conversion-mapper.js"></script>
```

### 添加标记的位置

将标记添加到通过搜索单击而可能成为登陆页面的任何页面中（理想情况下，在所有页面上，因为登陆页面可能会随着时间的推移而发生变化）。 必须在Adobe AdvertisingJavaScript v3转化跟踪标记之前加载该标记。

如果将其放置在iframe或容器标记中，则：

* iframe应与顶级域位于同一级别。

* 转化映射标记应该仅比顶级域低一(1)级。

## 更新JavaScript转化标记 {#update-conversion-tags}

如果贵组织使用多个组织ID，则将要跟踪页面转化的组织ID添加到您现有的JavaScript转化标记中。

如果您的组织使用一个组织ID，则无需执行此步骤。

### JavaScript V2标签

在转换脚本标记的开头添加以下字符串：

`ef_imsorgid="{xxxxxx@AdobeOrg}";`

其中，将值`{xxxxxx@AdobeOrg}`替换为跟踪页面转化的组织ID。

示例：

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
ef_imsorgid = "abc12345@AdobeOrg";
var ef_event_type="transaction";
var ef_transaction_properties = "ev_property name=<property name>&ev_transid=<transid>";
/*
 * Do not modify below this line
 */
var ef_segment = "";
var ef_search_segment = "";
var ef_userid="ef-userid";
var ef_pixel_host="pixel.everesttech.net";
var ef_fb_is_app = 0;
var ef_allow_3rd_party_pixels = 1;
effp();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property name=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

### JavaScript V3标签

定义`window.EF`后，添加以下字符串：

`window.EF.imsorgid = "{xxxxxx@AdobeOrg}";`

其中，将值`{xxxxxx@AdobeOrg}`替换为跟踪页面转化的组织ID。

示例：

```
<script type='text/javascript'>
    (function() {
        var f = function() {
              EF.init({ eventType: "transaction",
                        transactionProperties : "ev_property=<property name>&ev_transid=<transid>",
                        segment : "",
                        searchSegment : "",
                        sku : "",
                        userid : "ef-userid",
                        pixelHost : "pixel.everesttech.net"
                        
                        , allow3rdPartyPixels: 1});
              EF.main();
        };
        window.EF = window.EF || {};
        window.EF.imsorgid ="abc12345@AdobeOrg";
        if (window.EF.main) {
            f();
            return;
        }
        window.EF.onloadCallbacks = window.EF.onloadCallbacks || [];
        window.EF.onloadCallbacks[window.EF.onloadCallbacks.length] = f;
        if (!window.EF.jsTagAdded) {
            var efjs = document.createElement('script'); efjs.type = 'text/javascript'; efjs.async = true;
            efjs.src = 'https://www.everestjs.net/static/st.v3.js';
            var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(efjs, s);
            window.EF.jsTagAdded=1;
        }
    })();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

## 验证标记部署 {#validate-conversion-mapping}

请咨询您的Adobe帐户团队，帮助验证转化映射标记和常规转化标记（如果已更新）。
