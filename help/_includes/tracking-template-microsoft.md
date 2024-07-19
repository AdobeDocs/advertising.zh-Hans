---
source-git-commit: 38d6d70d03c12aab1a7caee6e589a2fdeaf78ad4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---
# Microsoft Advertising实体的“跟踪模板”字段

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]：** （可选，不适用于所有实体）跟踪模板或跟踪URL，它指定所有登入外域重定向和跟踪参数，并将最终/登陆页面URL嵌入到参数中。 示例： `{lpurl}?source={network}&id=5`或`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`以包含重定向。

对于Adobe Advertising转化跟踪（在Campaign设置包括&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot;时应用），Search、Social和Commerce会在您保存记录时自动为其自己的重定向和跟踪代码添加前缀。

* 有关嵌入最终URL所支持的参数，请参阅有关参数的[[!DNL Microsoft Advertising] 文档，以指示最终URL](https://help.ads.microsoft.com/#apex/3/en/56799)。

* 您可以选择包含URL参数和为该营销活动定义的任何自定义参数，以&amp;号(&amp;)分隔，如{lpurl}？matchtype={matchtype}&amp;device={device}。

* 您可以选择添加第三方重定向和跟踪。

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* 最细粒度级别的跟踪模板将覆盖所有更高级别的值。 例如，如果帐户设置和关键字设置都包含一个值，则应用关键字值。
>* 您可以在任何级别更新跟踪模板，而无需重新提交广告以供审批。
