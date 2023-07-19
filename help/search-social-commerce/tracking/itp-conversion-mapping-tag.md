---
title: Adobe广告转化映射标记
description: 了解适用于ITP 2.2的基于JavaScript的转化映射标记，该标记允许Adobe广告跟踪在非登陆页面上发生的转化事件。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---

# Adobe广告JavaScript转换映射标记

*仅具有Adobe广告转化跟踪的广告商*

除了Adobe广告JavaScript v2或v3转化跟踪标记之外，广告基于JavaScript的转化映射标记也可使用，它允许Adobe广告跟踪在非登录Adobe上发生的转化事件。 ITP 2.2解决方案将用户的Cookie存储在广告商拥有的iFrame中的本地存储中。 然后，本地存储可以将Cookie值从点击下游保留到转换页面。

使用转化映射标记确保Adobe广告可以跟踪Apple Safari和Mozilla Firefox浏览器内发生的所有转化，从而限制第一方Cookie的持久性。 <!-- For all requirements to track conversions from Safari, see "Track Conversions from Apple Safari Browsers." -->

要使用转换映射标记，请执行以下操作：

1. [部署转换映射标记](#deploy-conversion-mapping-tag).

1. 如果您的组织使用多个Adobe Experience Cloud Identity Service组织ID（以前称为IMS组织ID），则 [更新您的转化标记](#update-conversion-tags) 以包含组织ID。

1. [验证标记部署](#validate-conversion-mapping).

## 为ITP 2.2部署JavaScript转换映射标记 {#deploy-conversion-mapping-tag}

>[!NOTE]
>
>如果您使用ITP 2.0的JavaScript转换映射标记，则使用下列标记之一替换所有转换页面中的现有标记。<!-- any other instructions, too? Point them to the other page on Track Conversions from Safari...." -->

* 如果您的组织使用单个组织ID（用于您的搜索、社交和商务帐户），则请使用以下标记：

   `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" userid="{AMO User ID}"></script>`

   替换的位置 `{AMO User ID}` 具有搜索、社交和商务帐户的唯一用户ID。

* 如果您的组织使用多个组织ID，请使用以下标记：

   `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="{xxxxxx@AdobeOrg}" userid="{AMO User ID}"></script>`

   其中：

   * 替换值 `{xxxxxx@AdobeOrg}` ，其中包含要跟踪其页面转化的组织ID。 对所有转化页面使用相同的组织ID。

   * 您替换了 `{AMO User ID}` 具有搜索、社交和商务帐户的唯一用户ID。

* 如果您使用的标签管理系统不支持添加 `imsorgid` 变量到脚本标记中，然后改用以下代码：

   *如果您的组织使用单个组织ID：

   ```
   <script>
   window.ad_cloud = window.ad_cloud || {};
   window.ad_cloud.userid = "{AMO User ID}"
   </script>
   <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
   ```

   替换的位置 `{AMO User ID}` 具有搜索、社交和商务帐户的唯一用户ID。

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

      * 替换值 `{xxxxxx@AdobeOrg}` ，其中包含要跟踪其页面转化的组织ID。 对所有转化页面使用相同的组织ID。

      * 您替换了 `{AMO User ID}` 具有搜索、社交和商务帐户的唯一用户ID。

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

### 在何处添加标记

将标记添加到任何可通过搜索单击而成为登陆页面的页面中（理想情况下，在所有页面上，因为登陆页面可能会随着时间的推移而发生变化）。 必须在AdobeAdvertising JavaScript v3转化跟踪标记之前加载它。

如果将其放置在iframe或容器标记中，则：

* iframe应与顶级域位于同一级别。

* 转换映射标记应该只比顶级域低一(1)级。

## 更新JavaScript转化标记 {#update-conversion-tags}

如果您的组织使用多个组织ID，则将跟踪其页面转化的组织ID添加到您现有的JavaScript转化标记。

如果您的组织使用一个组织ID，则无需执行此步骤。

### JavaScript V2标记

在转换脚本标记的开头添加以下字符串：

`ef_imsorgid="{xxxxxx@AdobeOrg}";`

替换值 `{xxxxxx@AdobeOrg}` ，其中包含要跟踪其页面转化的组织ID。

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

### JavaScript V3标记

晚于 `window.EF` 定义，添加以下字符串：

`window.EF.imsorgid = "{xxxxxx@AdobeOrg}";`

替换值 `{xxxxxx@AdobeOrg}` ，其中包含要跟踪其页面转化的组织ID。

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