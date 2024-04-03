---
source-git-commit: 92bf7768be91e75f029e1577c7f4e7e790c5a934
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---
# 代码片段

## Google Ads实体的“跟踪模板”字段 {#tracking-template-google}

<!-- Duplicated from include file because one file has multiple occurrences, which ExL doesn't support. -->

**[!UICONTROL Tracking Template]：** （可选）跟踪模板或跟踪URL，用于指定所有登陆域外部重定向和跟踪参数，并将最终/登陆页面URL嵌入到 [!DNL ValueTrack] 参数。 示例： `{lpurl}?source={network}&id=5` 或 `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` 以包含重定向。

用于Adobe Advertising转化跟踪，当促销活动设置包括&#39;&#39;时应用[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]，”在保存记录时，Search、Social和Commerce会自动为自己的重定向和跟踪代码添加前缀。

* 有关嵌入最终URL支持的参数，请参阅 [[!DNL Google Ads] 支持的文档 [!DNL ValueTrack] 格式](https://support.google.com/google-ads/answer/6305348). (转到“可用”部分中的“仅跟踪模板”参数 [!DNL ValueTrack] 参数。”)

* 您可以选择包含URL参数以及为促销活动定义的任何自定义参数，这些参数之间以&amp;号分隔，例如 {lpurl}？matchtype={matchtype}设备(&amp;D)={device}.

* 您可以选择添加第三方重定向和跟踪。

>[!NOTE]
>
>* 避免使用宏，宏不会替代来自启用并行跟踪的源的点击。 如果广告商必须使用宏，则Adobe客户团队应与客户支持或实施团队合作来添加宏。
>* 最细粒度级别的跟踪模板将覆盖所有更高级别的值。 例如，如果帐户设置和关键字设置都包含一个值，则应用关键字值。
>* 如果您在广告、站点链接或关键词级别更新跟踪模板，则会重新提交相关广告以供审阅。 您可以在帐户、营销活动或广告组级别更新跟踪模板，而无需重新提交广告以供审批。

## 跟踪模板字段 [!DNL Microsoft Advertising] 实体 {#tracking-template-microsoft}

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]：** （可选）跟踪模板或跟踪URL，用于指定所有登陆域重定向和跟踪参数，并将最终/登陆页面URL嵌入到参数中。 示例： `{lpurl}?source={network}&id=5` 或 `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` 以包含重定向。

用于Adobe Advertising转化跟踪，当促销活动设置包括&#39;&#39;时应用[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]，”在保存记录时，Search、Social和Commerce会自动为自己的重定向和跟踪代码添加前缀。

* 有关嵌入最终URL支持的参数，请参阅 [[!DNL Microsoft Advertising] 有关指示最终URL的参数的文档](https://help.ads.microsoft.com/#apex/3/en/56799).

* 您可以选择包含URL参数以及为促销活动定义的任何自定义参数，这些参数之间以&amp;号分隔，例如 {lpurl}？matchtype={matchtype}设备(&amp;D)={device}.

* 您可以选择添加第三方重定向和跟踪。

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* 最细粒度级别的跟踪模板将覆盖所有更高级别的值。 例如，如果帐户设置和关键字设置都包含一个值，则应用关键字值。
>* 您可以在任何级别更新跟踪模板，而无需重新提交广告以供审批。

## 文本和模板 — 说明如何插入动态参数的注释 {#inventory-feed-template-insert-dynamic-parameter}

要将列名或修饰符组作为动态参数插入，请在输入字段中单击，然后单击列列表中的列名或 [修饰符名称](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) 在修饰符列表中。 要插入 [!DNL Param1] 或 [!DNL Param2] 变量中，输入值 `{param1:default text}` 或 `{param2:default text}`，其中“默认文本”是当馈送文件中的参数列对于广告行为空时使用的文本。

## 文本广告模板 — 说明如何插入广告自定义程序的注释 {#inventory-feed-template-insert-ad-customizer}

要插入广告自定义项，请使用以下格式，其中 `Default text` 是一个可选值，可在信息源文件不包含有效值时插入：

* [!DNL Google Ads]： `{CUSTOMIZER.AdCustomizerName:Default text}`，例如 `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]： `{CUSTOMIZER.Attribute name:Default text}`，例如 `{CUSTOMIZER.Discount:10%}`
