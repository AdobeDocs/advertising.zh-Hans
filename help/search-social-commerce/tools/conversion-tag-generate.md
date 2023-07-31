---
title: 生成Adobe Advertising转化跟踪标记
description: 了解如何创建Adobe Advertising转化标记以跟踪您的转化事件。
exl-id: 617cd808-c4ba-4413-89e4-0f52cb44f44b
feature: Search Tools, Search Tracking
source-git-commit: b730716565dfae9cb32556eaede1c3f29f316ac7
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# 生成Adobe Advertising转化跟踪标记

*仅具有Adobe Advertising转化跟踪的广告商*

为要跟踪的每个量度集创建单独的转化标记，并为广告商或代理机构提供要插入每个量度的网页列表。

>[!NOTE]
>
>此功能不会添加图像标记或 [!DNL JavaScript] 标记到广告商的网页。 必须按照广告商更新网页的正常过程添加标记。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. 指定 [转化标记设置](#conversion-tag-settings).

1. 生成标记：

   * 如果网站使用HTTP，请单击 **[!UICONTROL Generate Conversion Tag]**.

   * 如果网站在安全服务器(HTTPS)上运行，请单击 **[!UICONTROL Generate Secure Conversion Tag]**.

1. 复制对话框中的标记，并根据需要将其粘贴到相应的网页中。

>[!NOTE]
>
>新转化标记中的每个量度都会自动列在 [!UICONTROL Admin] > [!UICONTROL Transaction Properties]，即使未实施或者所在的网页未收到任何点击。 此行为与手动或其他位置创建的标记中的量度行为不同，这些标记未列在 [!UICONTROL Admin] > [!UICONTROL Transaction Properties] 直到其所在的一个网页收到点击为止。 但是，在所有情况下，每个量度最初都从项目组合目标、报表和视图中排除，直到您明确提供它们。 但是，在将量度添加到项目组合目标之前，请考虑先使量度可用，并将它们添加到报表以验证它们何时收到点击量。

## Adobe Advertising转换标记设置 {#conversion-tag-settings}

**[!UICONTROL Tag Type]：** 要创建的标记类型：

* *[!UICONTROL Image]：* 创建图像标签以在网页上显示1像素x 1像素的透明图像（像素），最终用户看不到该图像。 最佳实践是，仅当网站制定了禁止使用JavaScript标记的策略时，才使用图像标记。

* *[!UICONTROL JavaScript]：* 创建JavaScript标记。

有关标记类型之间差异的更多信息，请参阅&quot;[关于Adobe Advertising转化和页面查看跟踪标记的常见问题解答](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)“

**[!UICONTROL Tag Properties]：** 当最终用户查看包含转化标记的页面时要跟踪的一个或多个转化量度。 要向列表中添加量度，请在“”中输入量度名称[!UICONTROL Add new property]”字段并单击 **[!UICONTROL Add]**.

跟踪多个量度时，将使用&amp;符号(`&`)，例如 `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>添加到此列表的量度不会保存在任何位置，也不会与客户端的 [!UICONTROL Conversions] 列表 [!UICONTROL Admin] 选项卡。 但是，量度会添加到客户端的 [!UICONTROL Conversions] 当Adobe Advertising实际收集某个指标的数据后自动列出，当转化标记在某个页面上实施并且最终用户完成打开该页面的事务处理时，会发生这种情况。

**[!UICONTROL Include unique transaction IDs]：** （可选）包含交易ID属性(`ev_transid=<transid>`)。 默认情况下会选中该选项。

选择此选项时，广告商必须生成的唯一值 `<transid>` （例如，实际的订单ID）在交易完成时传递回Adobe Advertising，例如 `ev_transid=0123`. Adobe Advertising使用交易ID来消除具有相同交易ID和属性值的重复交易。 事务ID不能包含&amp;符号(`&`)，保留为参数分隔符。 交易ID包含在中 [该 [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)，可用来使用广告商数据验证Search、Social和Commerce中的数据。

如果数据不包括每个交易的唯一ID，则Adobe Advertising仍会根据交易时间生成一个ID。

>[!NOTE]
>
>如果您发送 [交易ID馈送](/help/search-social-commerce/tracking/feed-transaction-id.md) ，然后您必须提交交易ID (`ev_transid`)对于交易离线部分馈送数据中的在线部分。

**[!UICONTROL Page is inside FB app]：** 已过时

**[!UICONTROL Segment users]：** 已过时

**[!UICONTROL JS Version]：** ([!DNL JavaScript] 仅限标记)的哪个版本 [!DNL JavaScript] 标记以创建： *[!UICONTROL v2]* （默认）或 *[!UICONTROL v3]*.

请参阅&quot;[关于Adobe Advertising转化和页面查看跟踪标记的常见问题解答](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)“ 以了解关于这些差异的更多信息。

>[!MORELIKETHIS]
>
>* [关于Adobe Advertising转化跟踪标签](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [关于创建和解码跟踪标记的工具](tracking-tools-about.md)
>* [有关转化和页面查看跟踪标记的常见问题解答](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript转换跟踪标记版本3的格式](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [JavaScript转换跟踪标记版本2的格式](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [图像转换跟踪标记的格式](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Adobe AdvertisingJavaScript转换映射标记](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [关于管理广告商的交易记录属性](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md)
