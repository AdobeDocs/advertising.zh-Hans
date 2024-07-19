---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---
# 帐户和营销活动设置中的重定向类型字段

**[!UICONTROL Redirect Type]：** （仅适用于[!UICONTROL EF Redirect]）将最终用户重定向到最终URL或目标URL的方法。 所选选项适用于帐户或营销活动中的所有广告、关键词和投放位置。 默认帐户级别设置继承自广告商的跟踪设置，默认营销活动级别设置继承自帐户设置。

* *[!UICONTROL Standard]：*&#x200B;仅将最终用户重定向到指定的URL。

* *[!UICONTROL Token]：*&#x200B;要将最终用户重定向到URL，并将点击(`ef_id`)的Search、Social和Commerce ID记录为查询字符串参数，该参数用作令牌。 如果要报告离线交易，希望Search、Social和Commerce与Adobe Analytics交换数据，或者希望跟踪[!DNL Apple Safari]浏览器内发生的所有转化，请选择此选项。

**注释：**

* 如果您从[!UICONTROL Standard]切换到[!UICONTROL Token]，或者反之，则必须重新生成帐户的跟踪URL。
* 您可以在营销策划级别覆盖帐户级别设置。
