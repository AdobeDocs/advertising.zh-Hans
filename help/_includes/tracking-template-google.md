---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---
# Google Ads实体的“跟踪模板”字段

<!-- Search CRUD and bulk edit of Google entity settings -->

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
