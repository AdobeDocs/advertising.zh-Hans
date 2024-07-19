---
title: 生成Adobe Advertising转化跟踪标记
description: 了解如何创建Adobe Advertising转化标记以跟踪您的转化事件。
exl-id: 02492162-96a0-4a91-8896-dd0f72199f79
feature: Search Tools, Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 0%

---

# 生成Adobe Advertising转化跟踪标记

*仅跟踪Adobe Advertising转化情况的广告商*

为要跟踪的每个量度集创建单独的转化标记，并为广告商或代理机构提供要插入每个量度的网页列表。

>[!NOTE]
>
>此功能不会将图像标记或[!DNL JavaScript]标记添加到广告商的网页。 必须按照广告商更新网页的正常过程添加标记。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**。

1. 指定[转换标记设置](#conversion-tag-settings)。

1. 生成标记：

   * 如果网站使用HTTP，请单击&#x200B;**[!UICONTROL Generate Conversion Tag]**。

   * 如果网站在安全服务器(HTTPS)上运行，请单击&#x200B;**[!UICONTROL Generate Secure Conversion Tag]**。

1. 复制对话框中的标记，并根据需要将其粘贴到相应的网页中。

>[!NOTE]
>
>新转化标记中的每个量度都会自动列在[!UICONTROL Admin] > [!UICONTROL Conversions]中，即使它未实施或它所处的网页未收到任何点击也是如此。 此行为不同于手动或其他位置创建的标记中的量度行为，这些标记不会在[!UICONTROL Admin] > [!UICONTROL Conversions]中列出，直到其所在的某个网页收到点击为止。 但是，在所有情况下，每个量度最初都从项目组合目标、报表和视图中排除，直到您明确提供它们。 但是，在将量度添加到项目组合目标之前，请考虑先使量度可用，并将它们添加到报表以验证它们何时收到点击量。

## Adobe Advertising转换标记设置 {#conversion-tag-settings}

**[!UICONTROL Tag Type]：**&#x200B;要创建的标记类型：

* *[!UICONTROL Image]：*&#x200B;创建图像标签以在网页上显示1像素x 1像素透明图像（像素），最终用户看不到该图像。 最佳实践是，仅在网站有禁止使用JavaScript标记的政策时才使用图像标记。

* *[!UICONTROL JavaScript]：*&#x200B;创建JavaScript标记。

有关标记类型之间差异的更多信息，请参阅有关Adobe Advertising转化和页面查看跟踪标记的[常见问题解答](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)。

**[!UICONTROL Tag Properties]：**&#x200B;当最终用户查看包含转化标记的页面时要跟踪的一个或多个转化量度。 若要向列表添加量度，请在“[!UICONTROL Add new property]”字段中输入量度名称，然后单击&#x200B;**[!UICONTROL Add]**。

跟踪多个量度时，标记中的与号(`&`)将联合这些量度，如`ev_Property1=<Property1>&ev_Property2=<Property2>`。

>[!NOTE]
>
>添加到此列表的量度未保存在任何位置，也未与[!UICONTROL Admin]选项卡上的客户端[!UICONTROL Conversions]列表集成。 但是，一旦Adobe Advertising实际收集某个量度的数据，就会自动将量度添加到客户端的[!UICONTROL Conversions]列表中，当转化标记在某个页面上实现，并且最终用户完成打开该页面的事务时，就会发生这种情况。

**[!UICONTROL Include unique transaction IDs]：**（可选）在标记中包含交易ID属性(`ev_transid=<transid>`)。 默认情况下会选中该选项。

选择此选项时，广告商必须在交易完成时为`<transid>`生成唯一值（例如，实际订单ID），并将其传递回Adobe Advertising，如`ev_transid=0123`。 Adobe Advertising使用交易ID来消除具有相同交易ID和属性值的重复交易。 事务ID不能包含作为参数分隔符保留的&amp;符号(`&`)。 交易ID包含在[的[!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)中，您可以使用该ID验证Search、Social和Commerce中的数据与广告商的数据。

如果数据不包括每个交易的唯一ID，则Adobe Advertising仍会根据交易时间生成一个ID。

>[!NOTE]
>
>如果您发送带有离线转换转换转换数据的[交易ID馈送](/help/search-social-commerce/tracking/feed-transaction-id.md)，则必须在交易的离线部分馈送数据中提交交易的在线部分交易ID (`ev_transid`)。

**[!UICONTROL Page is inside FB app]：**&#x200B;已过时

**[!UICONTROL Segment users]：**&#x200B;已过时

**[!UICONTROL JS Version]：** （仅限[!DNL JavaScript]个标记）要创建的[!DNL JavaScript]标记的版本： *[!UICONTROL v2]* （默认值）或&#x200B;*[!UICONTROL v3]*。

请参阅有关Adobe Advertising转化和页面查看跟踪标记的[常见问题解答](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)。 以了解关于这些差异的更多信息。

>[!MORELIKETHIS]
>
>* [关于Adobe Advertising转化跟踪标记](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [关于用于创建和解码跟踪标记的工具](tracking-tools-about.md)
>* 有关转化和页面查看跟踪标记的[常见问题解答](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript转换跟踪标记版本3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [JavaScript转换跟踪标记版本2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)的格式
>* [图像转换跟踪标记的格式](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Adobe AdvertisingJavaScript转换映射标记](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [关于管理广告商的转化量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
