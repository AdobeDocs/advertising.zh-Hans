---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---
# 帐户和营销活动设置中的“跟踪类型”字段

**[!UICONTROL Tracking Type]：**&#x200B;用于生成URL的方法：

* *[!UICONTROL EF Redirect]* （默认）：适用于希望使用Adobe Advertising转换跟踪服务的客户端。 此方法会生成唯一的点击跟踪ID，并将用户重定向到Adobe Advertising服务器以进行跟踪，然后再将其发送到客户端的登陆页面。

  此方法具有默认跟踪选项，您可以选择对这些选项进行自定义，还可以指定要附加到每个URL的参数。

* *[!UICONTROL No EF Redirect]：*&#x200B;适用于只想使用自己的点击跟踪代码的客户端。 搜索、社交和Commerce不提供点击跟踪ID或重定向代码。 对于具有目标URL的帐户，每个目标URL都与基本URL相同。

  **注释：**

   * 只有代理客户经理、Adobe客户经理和管理员用户可以更改此值。
   * 如果更改跟踪方法，则必须为帐户重新生成跟踪URL。
   * 营销活动级别的跟踪选项会覆盖帐户级别的设置。
