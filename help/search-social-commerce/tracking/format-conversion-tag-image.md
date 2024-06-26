---
title: 图像转换跟踪标记的格式
description: 引用图像转换跟踪标记的格式。
exl-id: e23107e1-b719-4572-a471-13e51387465d
feature: Search Tracking
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# 图像转换跟踪标记的格式

>[!NOTE]
>
>有关何时使用图像标记与JavaScript标记的信息，请参阅 [关于跟踪标记的常见问题解答](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

* 具有HTTP的网站的非安全标记：

  `<img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

* 使用HTTPS的网站的安全标记：

  `<img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

其中：

* `<ef-userid>` 是Search、Social和Commerce分配给广告商的唯一数字用户ID。

* `<propertyname>` 是要跟踪的转换。 例如，如果您跟踪名为“注册”的转化，则标记将包括参数 `ev_registration=<registration>`，并且您需要传递每个交易的实际收入(例如 `ev_registration=1`)。 跟踪多个属性时，将使用&amp;符号(`&`)，例如 `ev_registration=<registration>&ev_sale=<sale>` (例如， `ev_registration=1&ev_sale=12.99`)。 **注意：**  属性名称不能包含特殊字符。

* `<transid>` 是广告商为标识交易而生成和传递的唯一交易ID（例如实际订单ID）。 仅当&quot;[!UICONTROL Include unique transaction IDs]已选中“ ”选项。

  搜索、Social和Commerce使用交易ID来消除具有相同交易ID和属性值的重复交易。 交易ID包含在 [!UICONTROL Transaction Report]，可用于验证包含广告商数据的Adobe Advertising中的数据。 **注意：** 如果广告商的数据不包括每次交易的唯一ID，则Search、Social和Commerce仍会根据交易时间生成一个ID。

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [关于Adobe Advertising转化跟踪标签](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [生成Adobe Advertising转换标记](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [有关转化和页面查看跟踪标记的常见问题解答](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript转换跟踪标记版本2的格式](format-conversion-tag-jsv2.md)
>* [JavaScript转换跟踪标记版本3的格式](format-conversion-tag-jsv3.md)
