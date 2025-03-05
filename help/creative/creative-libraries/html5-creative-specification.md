---
title: HTML5创作规范
description: 参考适用于Advertising Creative的HTML5创意规范。
feature: Creative Standard Creatives
exl-id: 06d29442-d688-4fb8-ad6f-cba0a897fde0
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---

# 适用于Advertising Creative的HTML5创作规范

本文档概述了[!DNL Creative]中对HTML5创意人员的要求和API支持。 该API允许开发HTML5创意，其属性可以在创意交付时配置。

## 范围

[!DNL Creative]支持带有非富媒体创意内容的HTML5横幅，这些横幅显示在页面的设置边框内。 您可以使用以下类型的HTML5创意：

<!--Remove to simplify:

* **Simple HTML5:** Supports a single landing page URL that can be configured during creative creation and trafficking.

* **Static HTML5:** Supports up to 5 landing page URLs that can be configured during creative creation and trafficking.

-->

* **HTML5：**&#x200B;支持最多5个可在创意创建和贩运期间配置的登陆页面URL。

* **灵活的HTML5：**&#x200B;支持最多5个可在创意创建和贩运期间配置的登陆页面URL，还允许在创意创建和贩运期间修改创意属性。

## 要求

### 文件夹和压缩要求

* 创意内容必须打包为ZIP文件（.ZIP格式）。 不支持嵌套的ZIP文件，因此不要在外部压缩文件夹中包含压缩文件夹。

* ZIP文件必须至少包含一个HTML文件(主HTML显示文件)，其中包括对[!DNL Creative] JavaScript库的引用。 主HTML文件可以在根文件夹或子文件夹中。

* 主HTML文件可以命名任何内容，只要它不包含特殊字符即可，但建议使用`index.html`。

* 呈现最终创意所需的所有支持资源必须位于与HTML显示文件相同的文件夹中，或者位于主文件夹的子文件夹中。

* 请勿在创意内容中包含创意内容未引用的任何文件。

### 包括Advertising Creative JavaScript文件

主HTML文件（不包含其他文件）必须包含对JavaScript文件`AMOLibrary.js`的引用。 使用以下地址调用`<head>`部分第一行中的文件：

`https://ads.everesttech.net/ads/static/local/AMOLibrary.js`

此文件包含的函数可确保对退出事件进行本地测试不会出现任何问题。

<!-- Remove to simplify:

### Simple HTML5 creative requirements

#### Support for click-through URLS in simple HTML5

The `<head>` section of the main HTML file must include a JavaScript variable name `clickTag` or `clickTAG`. The value of the variable should be the landing page URL. See the following example.

```
<script type=”text/javascript”>
var clickTag = “http://www.example.com”;
</script>
```

>[!NOTE]
>
>The static URL you include in the HTML5 creative is used for local testing purposes only and will be overwritten. When you upload an HTML5 creative, you'll define the default landing page for the `clickTag` variable. When you assign an uploaded HTML5 creative to an ad experience, you can optionally override the default landing page for the `clickTag` variable, and [!DNL Creative] adds click tracking to the URL when you save the experience.

-->

<!-- Renamed to simplify:
### Static HTML5 creative requirements
-->

### HTML5创意要求

#### 在静态HTML5中支持点进URL

##### `amo.registerClick(clkVar, clkUrl)`

注册点进URL和用于引用每个URL的相关参数（称为`clickTag`）。 此API会通知[!DNL Creative]广告服务器在何处添加点击跟踪。 您可以使用此API最多注册五个点击标记变量，每个变量有一个对应的登陆页面URL。

>[!NOTE]
>
>您在HTML5创意中包含的静态URL仅用于本地测试，并将被覆盖。 在上传HTML5创意时，您为每个`clickTag`变量定义默认登陆页面。 将上传的HTML5创意内容分配给广告体验时，您可以选择覆盖每个`clickTag`变量的默认登陆页面，并且[!DNL Creative]会在您保存体验时向URL添加点击跟踪。

###### 参数

* `clkVar` — click变量的名称（通常为“clickTag”），用双引号括起来。

* `clkUrl` — 此Click变量的登陆页面URL，用双引号括起来。

###### 使用情况

在主HTML文件的`<head>`部分中调用`amo.registerClick()`。

###### 示例

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

触发退出事件，这会将用户重定向到为`clickTag`配置的登陆页面。 在本地测试期间，此函数会提醒开发人员传递给函数的URL是否已注册。

###### 参数

* `clkTag` — 使用`amo.registerClick()`函数分配登陆页面URL时所使用的点击变量的名称，用单引号括起来。

* `event` — （可选）JavaScript“点击”事件对象。 这会记录点击的坐标，可进一步用于分析创意效果。

###### 使用情况

在主HTML文件的`<body>`部分中调用`amo.onAdClick()`。

###### 示例

`amo.onAdClick('clickTag')`或`amo.onAdClick('clickTag',clickEvt)`

### 灵活的HTML5创意要求

#### 在灵活的HTML5中支持点进URL

##### `amo.registerClick(clkVar, clkUrl)`

注册点进URL和用于引用每个URL的相关参数（称为`clickTag`）。 此API会通知[!DNL Creative]广告服务器在何处添加点击跟踪。 您可以使用此API最多注册五个点击标记变量，每个变量有一个对应的登陆页面URL。

>[!NOTE]
>
>您在HTML5创意中包含的静态URL仅用于本地测试，并将被覆盖。 在上传HTML5创意时，您为每个`clickTag`变量定义默认登陆页面。 将上传的HTML5创意内容分配给广告体验时，您可以选择覆盖每个`clickTag`变量的默认登陆页面，并且[!DNL Creative]会在您保存体验时向URL添加点击跟踪。

###### 参数

* `clkVar` — click变量的名称（通常为“clickTag”），用双引号括起来。

* `clkUrl` — 此Click变量的登陆页面URL，用双引号括起来。

###### 使用情况

在主HTML文件的`<head>`部分中调用`amo.registerClick()`。

###### 示例

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

触发退出事件，这会将用户重定向到为`clickTag`配置的登陆页面。 在本地测试期间，此函数会提醒开发人员传递给函数的URL是否已注册。

###### 参数

* `clkTag` — 使用`amo.registerClick()`函数分配登陆页面URL时所使用的点击变量的名称，用单引号括起来。

* `event` — （可选）JavaScript“点击”事件对象。 这会记录点击的坐标，可进一步用于分析创意效果。

###### 使用情况

在主HTML文件的`<body>`部分中调用`amo.onAdClick()`。

###### 示例

`amo.onAdClick('clickTag')`或`amo.onAdClick('clickTag',clickEvt)`

#### 在灵活的HTML5中支持创意属性

##### `amo.registerAttribute(key, type, value)`

定义创意的属性，这些属性可在创意或体验创建时更改。 您最多可以定义20个创意属性，这些属性可在创意或体验创建时配置。

>[!NOTE]
>
>此方法中定义的值仅用于本地开发，不用于实时广告服务。

###### 参数

* `key` — 属性的字母数字名称。 它必须以字母字符开头。

* `type` — 属性的类型（`TEXT`或`IMAGE`）。

* `value` — 用于测试的属性的值。 对于`IMAGE`类型的属性，该值必须是图像文件的相对路径。

###### 使用情况

在本地模式下进行测试期间，调用`amo.registerAttribute()`以注册一个创意属性、类型和值。 用作示例值的任何图像文件都应与上传的包一起打包到ZIP文件中。

##### `amo.attributes`

用于查询创意属性变量名称和值的JSON对象。 对象键是属性名称，值是这些属性的值。

在本地测试模式下，键值对是通过`amo.registerAttribute` API注册的对。 对于生产，必须在创意创建和贩运时配置创意属性变量名称和值。

### Creative内容要求

Advertising DSP中可用的大多数显示区交换都有以下创意要求：

* 所有广告图像必须周围有纯色边框。

* 不允许展开广告。

* 必须在新窗口中打开登陆页面。

* 登陆页面域及其子域不能超过35个字符。 **注意：**&#x200B;最终登陆页面URL是在DSP中定义的，而不是在HTML5资源本身中定义的。

* 任何对广告产品的免责声明都必须包含在广告本身中，而不仅仅是登陆页面上。

<!-- * (Dynamic HTML5 creatives) Do not use `window.open` to handle clicks in your code. Always use `amo.onDynAdClick` to handle click-throughs. -->

## 作为JSON对象和数组的示例内容

### 作为JSON对象的示例内容

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
}
```

### JSON数组形式的示例内容

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
[{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
},

{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-mobile-720x520.png",
"product_url": "http://adobe.com/"
}

]
```

## HTML5创意示例

### 示例文件夹结构（解压缩后）

* index.html

* /assets（文件夹）

   * bg.jpg(JPG、PNG、SVG或GIF图像)

### 简单的HTML5创作实例的HTML文件(index.html)

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

### 静态HTML5创意内容的示例HTML文件(index.html)

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  amo.registerClick("clickTag2","http://www.example2.com");
  amo.registerClick("clickTag3","http://www.example3.com");
  amo.registerClick("clickTag4","http://www.example4.com");
  amo.registerClick("clickTag5","http://www.example5.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

>[!MORELIKETHIS]
>
>* [将标准创意添加到创意库](/help/creative/creative-libraries/creative-add-standard.md)
