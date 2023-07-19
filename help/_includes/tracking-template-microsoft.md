---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---
# Microsoft Advertising实体的“跟踪模板”字段

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]：** （可选）跟踪模板或跟踪URL，用于指定所有登陆域重定向和跟踪参数，并将最终/登陆页面URL嵌入到参数中。 示例： `{lpurl}?source={network}&id=5` 或 `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` 以包含重定向。

对于Adobe广告转化跟踪，当促销活动设置包括&#39;&#39;时应用[!UICONTROL EF Redirect]“ ”和“ ”[!UICONTROL Auto Upload]，”当您保存记录时，Search、Social和Commerce会自动为自己的重定向和跟踪代码添加前缀。

* 有关嵌入最终URL的支持参数，请参阅 [[!DNL Microsoft Advertising] 有关指示最终URL的参数的文档](https://help.ads.microsoft.com/#apex/3/en/56799).

* 您可以选择包括URL参数和为该营销活动定义的任何自定义参数，以&amp;号分隔，例如{lpurl}？matchtype={matchtype}&amp;device={device}。

* 您可以选择添加第三方重定向和跟踪。

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* 最精细级别的跟踪模板将覆盖所有更高级别的值。 例如，如果帐户设置和关键词设置都包含一个值，则会应用关键词值。
>* 您可以在任何级别更新跟踪模板，而无需重新提交广告以供审批。
