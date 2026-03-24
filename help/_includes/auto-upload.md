---
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---
# 帐户和营销活动设置中的自动上传字段

**[!UICONTROL Auto Upload]：** （仅适用于与[!UICONTROL EF Redirect]同步的营销活动）下次Search、Social和Commerce与其同步时，自动将以下内容上传到广告网络：(a)用于跟踪模板的搜索、Social和Commerce跟踪参数以及附加到最终URL的相同参数，或者(b)嵌入了Search、Social和Commerce跟踪代码的新目标URL。 对于具有[Adobe Advertising-Adobe Analytics集成](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=zh-Hans)和服务器端AMO ID (s_kwcid)配置的广告商，该上传还包括您的[和](https://experienceleague.adobe.com/zh-hans/docs/analytics/components/dimensions/amo-id)帐户的[!DNL Google Ads]AMO ID参数[!DNL Microsoft Advertising]。 默认帐户级别设置继承自广告商的跟踪设置。 您可以在营销策划级别覆盖帐户级别设置。

**注意：**&#x200B;跟踪URL每天只更新不同步的实体（即添加的新实体和属性已更改的现有实体）。 因此，如果您将现有广告商/帐户/营销活动的此设置从“禁用”更改为“启用”，则不会为已同步的现有实体更新跟踪URL。 要将跟踪添加到现有已同步实体的URL，请联系您的Adobe客户团队，并请求执行一次性的手动同步过程。 自动上传流程将处理未来的更改。
