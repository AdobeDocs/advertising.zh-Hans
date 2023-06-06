---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---
# 帐户和营销活动设置中的重定向类型字段

**[!UICONTROL Redirect Type]：** (对于 [!UICONTROL EF Redirect] 仅限于)将最终用户重定向到最终URL或目标URL的方法。 所选选项适用于帐户或营销活动中的所有广告、关键词和投放位置。 默认帐户级别设置继承自广告商的跟踪设置，默认营销活动级别设置继承自帐户设置。

* *[!UICONTROL Standard]：* 仅将最终用户重定向到指定的URL。

* *[!UICONTROL Token]：* 要将最终用户重定向到URL，并记录点击的搜索、社交和商务ID(`ef_id`)作为查询字符串参数，用作令牌。 如果要报告离线交易，希望Search、Social和Commerce与Adobe Analytics交换数据，或者希望跟踪中发生的所有转化，请选择此选项 [!DNL Apple Safari] 浏览器。

**注释：**

* 如果您从 [!UICONTROL Standard] 到 [!UICONTROL Token]，反之亦然，则必须为帐户重新生成跟踪URL。
* 您可以在营销策划级别覆盖帐户级别设置。
