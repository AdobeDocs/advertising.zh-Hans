---
title: 生成并实施Adobe Advertising转化跟踪标记
description: 了解如何创建Adobe Advertising转化标记以跟踪您的转化事件。
exl-id: 02492162-96a0-4a91-8896-dd0f72199f79
feature: Search Tools, Search Tracking
source-git-commit: d92fc3fa1ce218788890c073df22afa336aa9ad1
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 0%

---

# 生成并实施Adobe Advertising转化跟踪标记

*仅具有Adobe Advertising转化跟踪的广告商*

为要跟踪的每组量度创建单独的转化标记。

## 在Search、Social和Commerce中生成并实施转化跟踪标记

>[!NOTE]
>
>此功能不会将图像标记或[!DNL JavaScript]标记添加到广告商的网页。 向广告商或代理机构提供要在其上插入每个标签的网页列表。 必须按照广告商更新网页的正常过程添加标记。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**。

1. 指定[转换标记设置](#conversion-tag-settings)。

1. 生成标记：

   * 如果网站使用HTTP，请单击&#x200B;**[!UICONTROL Generate Conversion Tag]**。

   * 如果网站在安全服务器(HTTPS)上运行，请单击&#x200B;**[!UICONTROL Generate Secure Conversion Tag]**。

1. 复制对话框中的标记，并根据需要将其粘贴到相应的网页中。

>[!NOTE]
>
>新转化标记中的每个量度都会自动列在[!UICONTROL Admin] > [!UICONTROL Conversions]中，即使它未实施或它所处的网页未收到任何点击也是如此。 此行为不同于手动或其他位置创建的标记中的量度行为，这些标记不会在[!UICONTROL Admin] > [!UICONTROL Conversions]中列出，直到其所在的某个网页收到点击为止。 但是，在所有情况下，每个量度最初都从项目组合目标、报表和视图中排除，直到您明确提供它们。 但是，在将量度添加到项目组合目标之前，请考虑先使量度可用，并将它们添加到报表以验证它们何时收到点击量。

### Adobe Advertising转换标记设置 {#conversion-tag-settings}

**[!UICONTROL Tag Type]：**&#x200B;要创建的标记类型：

* *[!UICONTROL Image]：*&#x200B;创建图像标签以在网页上显示1像素x 1像素透明图像（像素），最终用户看不到该图像。 最佳实践是，仅在网站有禁止使用JavaScript标记的政策时才使用图像标记。

* *[!UICONTROL JavaScript]：*&#x200B;创建JavaScript标记。

有关标记类型之间差异的更多信息，请参阅[关于Adobe Advertising转化和页面查看跟踪标记的常见问题解答](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)。

**[!UICONTROL Tag Properties]：**&#x200B;当最终用户查看包含转化标记的页面时要跟踪的一个或多个转化量度。 若要向列表添加量度，请在“[!UICONTROL Add new property]”字段中输入量度名称，然后单击&#x200B;**[!UICONTROL Add]**。

跟踪多个量度时，标记中的与号(`&`)将联合这些量度，如`ev_Property1=<Property1>&ev_Property2=<Property2>`。

>[!NOTE]
>
>添加到此列表的量度未保存在任何位置，也未与[!UICONTROL Conversions]选项卡上的客户端[!UICONTROL Admin]列表集成。 但是，一旦Adobe Advertising实际收集某个量度的数据，量度就会自动添加到客户端的[!UICONTROL Conversions]列表中，这种情况会在转化标记在页面上实施并且最终用户完成打开该页面的事务时发生。

**[!UICONTROL Include unique transaction IDs]：**（可选）在标记中包含交易ID属性(`ev_transid=<transid>`)。 默认情况下会选中该选项。

选择此选项时，广告商必须在交易完成时为`<transid>`生成唯一值（例如，实际订单ID），并将其传递回Adobe Advertising，如`ev_transid=0123`。 Adobe Advertising使用交易ID来消除具有相同交易ID和属性值的重复交易。 事务ID不能包含作为参数分隔符保留的&amp;符号(`&`)。 交易ID包含在[的[!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)中，您可以使用该ID验证Search、Social和Commerce中的数据与广告商的数据。

如果数据中不包含每个交易的唯一ID，则Adobe Advertising仍会根据交易时间生成一个ID。

>[!NOTE]
>
>如果您发送带有离线转换转换转换数据的[交易ID馈送](/help/search-social-commerce/tracking/feed-transaction-id.md)，则必须在交易的离线部分馈送数据中提交交易的在线部分交易ID (`ev_transid`)。

**[!UICONTROL Page is inside FB app]：**&#x200B;已过时

**[!UICONTROL Segment users]：**&#x200B;已过时

**[!UICONTROL JS Version]：** （仅限[!DNL JavaScript]个标记）要创建的[!DNL JavaScript]标记的版本： *[!UICONTROL v2]* （默认值）或&#x200B;*[!UICONTROL v3]*。

请参阅有关Adobe Advertising转化和页面查看跟踪标记的[常见问题解答](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)。 以了解关于这些差异的更多信息。

## 使用Adobe Experience Platform标记实施转化跟踪标记

您可以使用Adobe Experience Platform（以前称为Adobe Experience Platform Launch）中的标记为“搜索”、“社交”和“Commerce”设置转化跟踪。 Adobe Experience Cloud客户可以使用标记作为随附的增值功能来获取这些标记。

从Experience Platform用户界面或Experience Platform数据收集用户界面为Search、Social和Commerce配置转化跟踪标记时，需要执行以下任务。 有关配置标记的完整信息和说明，请参阅Experience Platform标记指南，从“[标记概述](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/tags/home)”和“[快速入门指南](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/tags/get-started/quick-start)”开始。

>[!PREREQUISITES]
>
>要安装所需的标记扩展，请让您的组织管理员访问UI中的数据收集功能，包括`manage_properties`权限。

1. 从[数据收集UI](https://experience.adobe.com/#/data-collection/)，安装Adobe Advertising [扩展](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/tags/ui/extensions/overview)：

   1. 从适用的属性中，打开扩展目录并选择&#x200B;**Adobe Advertising**。

   1. 从下拉菜单中，选择&#x200B;**SSC**（用于Search、Social和Commerce）。

   1. 在&#x200B;**SSC UserID**&#x200B;字段中，输入您组织的Search、Social和Commerce帐户的数字用户ID。

      如果您不知道自己的用户ID，请联系您的Adobe客户团队。

   1. 单击&#x200B;**保存**。

1. 创建新规则（例如“form_completes”）以触发“搜索”、“社交”和“Commerce”转化标记：

   1. 在Event Configuration部分：

      1. 选择以下值：

         **扩展名：**`Core`

         **事件类型：** `Library Loaded (Page Top)`

      1. 单击&#x200B;**保留更改**。

   1. 在条件配置部分中：

      1. 指定以下值：

         **逻辑类型：** `Regular`

         **扩展名：**`Core`

         **条件类型：** `Path Without Query String`

         **如果路径等于：**&#x200B;应跟踪转化的路径（例如，`/form_complete`），则返回true。

      1. 单击&#x200B;**保留更改**。

   1. 在操作配置部分中：

      1. 指定以下值：

         **扩展名：**`Adobe Advertising`

         **操作类型：** `AMO Measurement`

         **转换属性名称：**&#x200B;转换属性的名称（例如，`form_completes`）。

         **值：**&#x200B;转换属性的数值（例如`1`跟踪form_completes），或选择现有的[数据元素](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/tags/ui/data-elements)。

      1. 单击&#x200B;**保留更改**。

   1. 保存规则。

1. 发布更改。

>[!MORELIKETHIS]
>
>* [关于Adobe Advertising转化跟踪标记](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [关于用于创建和解码跟踪标记的工具](tracking-tools-about.md)
>* 有关转化和页面查看跟踪标记的[常见问题解答](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript转换跟踪标记版本3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [JavaScript转换跟踪标记版本2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)的格式
>* [图像转换跟踪标记的格式](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Adobe Advertising JavaScript转换映射标记](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [关于管理广告商的转化量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
