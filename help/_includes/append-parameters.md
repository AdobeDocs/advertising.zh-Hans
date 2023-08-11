---
source-git-commit: ca9425333731ada692c68f08b20f070265eb3409
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---
# 在帐户和营销活动设置中附加参数字段

**[!UICONTROL Append Parameters]：** （可选）要附加到基本URL的任何其他跟踪参数。<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->. 默认情况下，帐户级别和营销活动级别包含广告商级别的附加参数，但您也可以覆盖任一附加参数。

您可以使用任何静态文本字符串，包括第三方跟踪参数，或者 [支持的跟踪参数](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md)，以在基本URL中插入相应的数据值。

用逗号或&amp;符号分隔多个参数。 不支持嵌套括号。

**注释：**

* 对附加参数的更改不受 [!UICONTROL Auto Upload] 选项。 如果更改现有基本URL的附加参数，则不会自动生成新的URL。 通过下载帐户或营销策划的批量处理工作表文件，更新 [!UICONTROL Base URL/Final URL] 字段，然后上传和发布批量处理工作表。

* （具有并行跟踪的广告网络）避免使用宏，宏不会替代来自启用并行跟踪的源的点击。 如果广告商必须使用宏，则Adobe客户团队应与客户支持或实施团队合作来添加宏。

* (具有Adobe Advertising-Adobe Analytics集成的广告商)包含AMO ID参数，以将Search、Social和Commerce数据发送至 [!DNL Analytics]，请参见 [广告网络特定的格式](/help/search-social-commerce/tracking/amo-id-tracking-parameter.md). 无需手动添加以下项的参数： [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 实施服务器端AMO ID的帐户。
