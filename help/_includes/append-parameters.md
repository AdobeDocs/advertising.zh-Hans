---
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---
# 在帐户和营销活动设置中附加参数字段

**[!UICONTROL Append Parameters]：**（可选）要附加到基本URL的任何其他跟踪参数。<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->。 默认情况下，帐户级别和营销活动级别包含广告商级别的附加参数，但您也可以覆盖任一附加参数。

您可以使用任何静态文本字符串，包括第三方跟踪参数，或者使用任何[支持的跟踪参数](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md)，这些参数可在基本URL中插入适当的数据值。

用逗号或&amp;符号分隔多个参数。 不支持嵌套括号。

**注释：**

* 对附加参数的更改不受[!UICONTROL Auto Upload]选项控制。 如果更改现有基本URL的附加参数，则不会自动生成新的URL。 通过下载帐户或营销策划的批量处理工作表文件、更新[!UICONTROL Base URL/Final URL]字段，然后上传并发布批量处理工作表来添加新参数。

* （具有并行跟踪的广告网络）避免使用宏，宏不会替代来自启用并行跟踪的源的点击。 如果广告商必须使用宏，则Adobe客户团队应与客户支持或实施团队合作来添加宏。

* (具有Adobe Advertising-Adobe Analytics集成的广告商)要包含AMO ID参数以将搜索、社交和Commerce数据发送到[!DNL Analytics]，请参阅[广告网络特定的格式](/help/integrations/analytics/ids.md#amo-id-formats)。 无需为具有服务器端AMO ID实施的[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户手动添加参数。
