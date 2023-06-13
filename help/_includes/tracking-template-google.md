---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---
# Google Ads实体的“跟踪模板”字段

<!-- Search CRUD and bulk edit of Google entity settings -->

**[!UICONTROL Tracking Template]：** （可选）跟踪模板或跟踪URL，用于指定所有离登陆域重定向和跟踪参数，并将最终/登陆页面URL嵌入到 [!DNL ValueTrack] 参数。 示例： `{lpurl}?source={network}&id=5` 或 `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` 以包含重定向。

对于Adobe广告转化跟踪，当促销活动设置包括&#39;&#39;时应用[!UICONTROL EF Redirect]“ ”和“ ”[!UICONTROL Auto Upload]，”当您保存记录时，Search、Social和Commerce会自动为自己的重定向和跟踪代码添加前缀。

* 有关嵌入最终URL的支持参数，请参阅 [[!DNL Google Ads] documentation for the supported [!DNL ValueTrack] 格式](https://support.google.com/google-ads/answer/6305348). (转到“可用”部分中的“仅限跟踪模板”参数 [!DNL ValueTrack] 参数。”)

* 您可以选择包括URL参数和为促销活动定义的任何自定义参数，各个参数之间以&amp;号分隔，例如 {lpurl}？matchtype={matchtype}设备(&amp;D){device}.

* 您可以选择添加第三方重定向和跟踪。

>[!NOTE]
>
>* 避免使用宏，宏不会替代来自启用并行跟踪的源的点击。 如果广告商必须使用宏，则Adobe帐户团队应与客户支持或实施团队合作来添加宏。
>* 最精细级别的跟踪模板将覆盖所有更高级别的值。 例如，如果帐户设置和关键词设置都包含一个值，则会应用关键词值。
>* 如果您在广告、站点链接或关键词级别更新跟踪模板，则会重新提交相关广告以供审阅。 您可以在帐户、营销活动或广告组级别更新跟踪模板，而无需重新提交广告以供审批。
