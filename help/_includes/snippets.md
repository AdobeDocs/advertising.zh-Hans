---
source-git-commit: 92bf7768be91e75f029e1577c7f4e7e790c5a934
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---
# 代码片段

## Google Ads实体的“跟踪模板”字段 {#tracking-template-google}

<!-- Duplicated from include file because one file has multiple occurrences, which ExL doesn't support. -->

**[!UICONTROL Tracking Template]：**（可选）跟踪模板或跟踪URL，它指定所有登入外域重定向和跟踪参数，并将最终/登陆页面URL嵌入到[!DNL ValueTrack]参数中。 示例： `{lpurl}?source={network}&id=5`或`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`以包含重定向。

对于Adobe Advertising转化跟踪（在Campaign设置包括&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot;时应用），Search、Social和Commerce会在您保存记录时自动为其自己的重定向和跟踪代码添加前缀。

* 有关嵌入最终URL所支持的参数，请参阅[[!DNL Google Ads] 文档，以了解支持的 [!DNL ValueTrack] 格式](https://support.google.com/google-ads/answer/6305348)。 （转到“可用[!DNL ValueTrack]参数”部分中的“仅跟踪模板”参数。）

* 您可以选择包含URL参数和为该营销活动定义的任何自定义参数，以&amp;号(&amp;)分隔，如{lpurl}？matchtype={matchtype}&amp;device={device}。

* 您可以选择添加第三方重定向和跟踪。

>[!NOTE]
>
>* 避免使用宏，宏不会替代来自启用并行跟踪的源的点击。 如果广告商必须使用宏，则Adobe客户团队应与客户支持或实施团队合作来添加宏。
>* 最细粒度级别的跟踪模板将覆盖所有更高级别的值。 例如，如果帐户设置和关键字设置都包含一个值，则应用关键字值。
>* 如果您在广告、站点链接或关键词级别更新跟踪模板，则会重新提交相关广告以供审阅。 您可以在帐户、营销活动或广告组级别更新跟踪模板，而无需重新提交广告以供审批。

## [!DNL Microsoft Advertising]实体的跟踪模板字段 {#tracking-template-microsoft}

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]：**（可选）跟踪模板或跟踪URL，它指定所有登入外域重定向和跟踪参数，并将最终/登陆页面URL嵌入到参数中。 示例： `{lpurl}?source={network}&id=5`或`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`以包含重定向。

对于Adobe Advertising转化跟踪（在Campaign设置包括&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot;时应用），Search、Social和Commerce会在您保存记录时自动为其自己的重定向和跟踪代码添加前缀。

* 有关嵌入最终URL所支持的参数，请参阅有关参数的[[!DNL Microsoft Advertising] 文档，以指示最终URL](https://help.ads.microsoft.com/#apex/3/en/56799)。

* 您可以选择包含URL参数和为该营销活动定义的任何自定义参数，以&amp;号(&amp;)分隔，如{lpurl}？matchtype={matchtype}&amp;device={device}。

* 您可以选择添加第三方重定向和跟踪。

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* 最细粒度级别的跟踪模板将覆盖所有更高级别的值。 例如，如果帐户设置和关键字设置都包含一个值，则应用关键字值。
>* 您可以在任何级别更新跟踪模板，而无需重新提交广告以供审批。

## 文本和模板 — 说明如何插入动态参数的注释 {#inventory-feed-template-insert-dynamic-parameter}

要将列名或修饰符组作为动态参数插入，请单击输入字段，然后单击列列表中的列名或修饰符列表中的[修饰符名称](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md)。 要插入[!DNL Param1]或[!DNL Param2]变量，请输入值`{param1:default text}`或`{param2:default text}`，其中“默认文本”是当广告行的馈送文件中的参数列为空时所使用的文本。

## 文本广告模板 — 说明如何插入广告自定义程序的注释 {#inventory-feed-template-insert-ad-customizer}

要插入广告自定义项，请使用以下格式，其中`Default text`是当馈送文件不包含有效值时要插入的可选值：

* [!DNL Google Ads]： `{CUSTOMIZER.AdCustomizerName:Default text}`，如`{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]： `{CUSTOMIZER.Attribute name:Default text}`，如`{CUSTOMIZER.Discount:10%}`
