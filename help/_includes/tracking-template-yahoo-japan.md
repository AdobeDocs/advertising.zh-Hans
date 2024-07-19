---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---
# Yahoo！ 日本广告实体

<!-- Search CRUD and bulk edit of Yahoo! Japan Ads entity settings -->

**[!UICONTROL Tracking Template]：**（可选）跟踪模板或跟踪URL，它指定所有登入外域重定向和跟踪参数，并将最终/登陆页面URL嵌入到参数中。 使用参数`!{lpurl}`指示登陆页面URL。 示例： `{lpurl}?source={network}&id=5`或`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`以包含重定向。

您可以选择添加第三方重定向和跟踪。

对于Adobe Advertising转化跟踪（在Campaign设置包括&quot;[!UICONTROL EF Redirect]&quot;和&quot;[!UICONTROL Auto Upload]&quot;时应用），Search、Social和Commerce会在您保存记录时自动为其自己的重定向和跟踪代码添加前缀。

>[!NOTE]
>
>* 最细粒度级别的跟踪模板将覆盖所有更高级别的值。 例如，如果帐户设置和关键字设置都包含一个值，则应用关键字值。
>* 您可以在任何级别更新跟踪模板，而无需重新提交广告以供审批。
