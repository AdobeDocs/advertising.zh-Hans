---
title: 生成Adobe广告转化跟踪标记
description: 了解如何创建Adobe广告转化标记以跟踪您的转化事件。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---

# 生成Adobe广告转化跟踪标记

*仅具有Adobe广告转化跟踪的广告商*

为要跟踪的每个量度集创建单独的转化标记，并为广告商或代理机构提供要插入每个标记的网页列表。

>[!NOTE]
>
>此功能不会添加图像标记或 [!DNL JavaScript] 标记到广告商的网页。 必须按照广告商更新网页的正常过程添加标签。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. 指定 [转化标记设置](#conversion-tag-settings).

1. 生成标记：

   * 如果网站使用HTTP，请单击 **[!UICONTROL Generate Conversion Tag]**.

   * 如果网站运行在安全服务器(HTTPS)上，请单击 **[!UICONTROL Generate Secure Conversion Tag]**.

1. 从对话框中复制标记，然后根据需要将其粘贴到相应的网页中。

>[!NOTE]
>
>新转化标记中的每个量度都会自动列在 [!UICONTROL Admin] > [!UICONTROL Transaction Properties]，即使尚未实施或者所在的网页未收到任何点击。 此行为与手动或其他位置创建的标记中的量度行为不同，这些标记未列在 [!UICONTROL Admin] > [!UICONTROL Transaction Properties] 直到其所在的一个网页收到点击为止。 但是，在所有情况下，每个指标最初都从项目组合目标、报表和视图中排除，直到您明确规定它们可用。 但是，在将量度添加到项目组合目标之前，请考虑先使量度可用，并将它们添加到报表以验证它们何时收到点击量。

## Adobe广告转化标记设置 {#conversion-tag-settings}

**[!UICONTROL Tag Type]：** 要创建的标记类型：

* *[!UICONTROL Image]：* 创建图像标签以在网页上显示1像素x 1像素的透明图像（像素），最终用户看不到该图像。 最佳实践是，仅当网站制定了禁止使用JavaScript标记的政策时，才使用图像标记。

* *[!UICONTROL JavaScript]：* 创建JavaScript标记。

有关标记类型之间差异的更多信息，请参阅&quot;[关于Adobe广告转化和页面查看跟踪标记的常见问题解答](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).”

**[!UICONTROL Tag Properties]：** 最终用户查看包含转化标记的页面时要跟踪的一个或多个事务属性（量度）。 要向列表中添加指标，请在“”中输入指标名称[!UICONTROL Add new property]”字段并单击 **[!UICONTROL Add]**.

跟踪多个量度时，将使用&amp;符号(`&`)，例如 `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>添加到此列表的量度不会保存在任何位置，也不会与客户端的集成 [!UICONTROL Transaction Properties] 列表于 [!UICONTROL Admin] 选项卡。 但是，量度会添加到客户端的 [!UICONTROL Transaction Properties] 当Adobe广告实际收集某个量度的数据后自动列出，当转化标记在页面上实施并且最终用户完成打开该页面的事务时，会发生这种情况。

**[!UICONTROL Include unique transaction IDs]：** （可选）包含交易ID属性(`ev_transid=<transid>`)。 默认情况下会选中该选项。

选择此选项时，广告商必须生成唯一值 `<transid>` （例如，实际的订单ID）在交易完成时将其传递回Adobe广告，例如 `ev_transid=0123`. Adobe广告使用交易ID来消除具有相同交易ID和属性值的重复交易。 事务ID不能包含&amp;符号(`&`)，保留为参数分隔符。 交易ID包含在 [此 [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)，可用于使用广告商的数据验证Search、Social和Commerce中的数据。

如果数据中不包含每个交易的唯一ID，则Adobe广告仍会根据交易时间生成一个ID。

>[!NOTE]
>
>如果您发送 [交易ID馈送](/help/search-social-commerce/tracking/feed-transaction-id.md) ，则必须提交交易ID (`ev_transid`)对于交易的在线部分，则为交易的离线部分。

**[!UICONTROL Page is inside FB app]：** 已过时

**[!UICONTROL Segment users]：** 已过时

**[!UICONTROL JS Version]：** ([!DNL JavaScript] 仅限标记)的哪个版本 [!DNL JavaScript] 标记以创建： *[!UICONTROL v2]* （默认）或 *[!UICONTROL v3]*.

参见“[关于Adobe广告转化和页面查看跟踪标记的常见问题解答](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).” 以了解关于这些差异的更多信息。

>[!MORELIKETHIS]
>
>* [关于Adobe广告转化跟踪标记](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [关于创建和解码跟踪标记的工具](tracking-tools-about.md)
>* [有关转化和页面查看跟踪标记的常见问题解答](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript转换跟踪标记版本3的格式](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [JavaScript转换跟踪标记版本2的格式](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [图像转换跟踪标记的格式](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Adobe广告JavaScript转换映射标记](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [关于管理广告商的交易属性](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md)

