---
title: 何时以及如何按广告网络和对象生成点击跟踪URL
description: 了解何时自动添加点击跟踪URL，以及何时以及如何为各种促销活动组件手动添加它们。
exl-id: 896de0c1-75ed-450c-b995-893f1a63e5ce
feature: Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# 何时以及如何按广告网络和对象生成点击跟踪URL

下表介绍了如何为各种促销活动组件生成点击跟踪URL。

| 广告网络 | 组件 | 如何生成点击跟踪URL |
| ---- | ---- | ---- |
| [!DNL Baidu]， [!DNL Google Ads]， [!DNL Microsoft Advertising]， [!DNL Yahoo! Japan Ads]、和 [!DNL Yandex] | <ul><li>文本广告</li><li>关键字</li><li>([!DNL Google Ads] 内容营销活动)投放</li><li>([!DNL Google Advertising] 和 [!DNL Advertising])站点链接</li></ul> | 当活动营销活动的跟踪设置包含选项&quot;[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]“”（在营销活动级别设置或从帐户设置继承），您无需为广告组组件生成跟踪URL。 Search、Social和Commerce每次与广告网络同步时，都会自动创建以下类型的跟踪URL并将其上传到广告网络： a)（具有最终URL的帐户）用于跟踪模板的搜索、Social和Commerce跟踪参数以及附加到最终URL的相同参数， b)（具有目标URL的帐户）嵌入了Search、Social和Commerce跟踪代码的新目标URL，以及c) ([!DNL Google Ads] 和 [!DNL Microsoft Advertising] 帐户)登陆页面后缀（最终URL后缀）参数。<br><br>如果 [!UICONTROL Auto Upload] 选项被禁用，则可以通过以下任一方式为组件生成跟踪URL：<ul><li>([!DNL Google Ads]， [!DNL Microsoft Advertising]， [!DNL Yahoo! Ads]、和 [!DNL Yandex])当您从馈送文件发布广告时，请选择 [!UICONTROL Generate Tracking URLs] 选项。 您可以选择在将任何批量处理工作表文件发布到广告网络之前，验证其中的跟踪模板字段。</li><li>下载、上传或发布包含该组件的批量处理工作表文件时，请选择 [!UICONTROL Generate Tracking URLs] 选项。 对于具有目标URL的帐户，您可以选择在将文件发布到广告网络之前验证基本URL/最终URL字段字段</li><li>使用 [[!UICONTROL Tracking URLs] 工具](/help/search-social-commerce/tools/click-tracking-url-generate.md) 以生成跟踪URL并手动将其添加到相应的中 [!UICONTROL Tracking Template] 或 [!UICONTROL Base URL] 字段。 <b>注意：</b> 您生成的跟踪模板不包含帐户或营销活动设置中指定的任何其他跟踪参数。<ul><li>Google帐户)转到 [[!UICONTROL Tracking URLs] 工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)，将屏幕上的值复制到相应的 [!UICONTROL Tracking Template] 字段，并手动将整个跟踪字符串添加到组件设置。 您必须添加 [!DNL Google Ads] [!DNL ValueTrack] 后面的最终URL的参数 `&url=` 参数(例如 `{lpurl}`)。 对于 [!DNL ValueTrack] 用于指示跟踪模板中最终URL的参数，请参阅“可用”部分中的“仅限跟踪模板”参数 [!DNL ValueTrack] 参数”。[!DNL Google Ads] documentation]9https://support.google.com/google-ads/answer/2375447。</li><li>（具有最终URL的其他帐户）使用生成跟踪URL [[!UICONTROL Tracking URLs] 工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)，并手动将整个跟踪字符串添加到组件设置。 您必须在之后为最终URL添加参数 `&url=` 参数(例如 `{lpurl}`)。 对象 [!DNL Yahoo! Japan Ads] 帐户，使用参数 `{lpurl}`. 对于 [!DNL Microsoft Advertising] 参数指示跟踪模板中的最终URL，请参阅 [[!DNL Microsoft Advertising] 文档](https://help.bingads.microsoft.com/#apex/3/en/56799).</li><li>（具有目标URL的帐户）使用生成跟踪URL [[!UICONTROL Tracking URLs] 工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)，并在相应的中手动添加跟踪URL [!UICONTROL Base URL] 字段。</li></ul></li></ul><b>注释：</b><br><br><ul><li>（具有最终URL的帐户）使用最细粒度级别的跟踪模板（例如，关键字级别的跟踪模板将覆盖帐户、营销活动和广告组级别的模板，而关键字的跟踪模板和投放位置将覆盖关联广告的跟踪模板）。</li><li>Adobe Advertising将站点链接的点击量和产生的收入映射到与包含站点链接的广告关联的关键字，而不是单独映射。 请参阅&quot;[支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)“</li></ul><b>提示：</b> （具有最终URL的客户）如果您仅在所需的最高级别（例如，帐户或营销活动级别的跟踪模板）创建跟踪模板，以将相同的跟踪应用于帐户或营销活动中的所有实体，则最易于管理跟踪。 |
| [!DNL Google Ads] | 电话分机 | 不适用 |
| [!DNL Google Ads]， [!DNL Microsoft Advertising] | 产品广告 | <ul><li>[!DNL Microsoft Merchant Center] 帐户：为您中的每个产品手动创建跟踪URL [!DNL Microsoft Merchant Center] 帐户使用 [购物广告的跟踪模板格式](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)，并手动将其添加到 [!UICONTROL Tracking Template] “帐户”、“促销活动”或“产品组”设置中的字段。<br><br>或者，您可以将跟踪URL添加到中的产品数据 [!DNL Microsoft Merchant Center account]. 要实现此目的，请包含跟踪URL以及&quot;[!DNL link]”或“[!DNL mobile_link]”字段（如果适用） [自定义列&#39;&#39;[!DNL bingads_redirect]”在产品信息源中](https://help.ads.microsoft.com/#apex/3/en/51084). “”中的值[!DNL bingads_redirect]”字段替换“”中的值[!DNL link]”和“[!DNL mobile_link]”字段。 使用此方法生成的URL不包含帐户设置中指定的任何跟踪参数。<br><br><b>注意：</b> 同步期间自动上传跟踪的帐户级别和营销活动级别功能不会为新生成跟踪 [!DNL Microsoft Advertising] 产品组。 解决方法是在上传或发布批量处理工作表时生成跟踪。</li><li>[!DNL Google Merchant Center] 帐户：使用 [[!UICONTROL Tracking URLs] 工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)，并手动将它们添加到 [!UICONTROL Tracking Template] 帐户、营销活动或产品组设置中的字段。</li></ul> |
| [!DNL Naver] | 关键字 | 您可以通过以下方式设置所有广告的点击跟踪 [批量工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md). 或者，您也可以手动生成广告的跟踪URL，并使用广告网络的编辑器手动将其添加到广告设置。 请参阅&quot;[实施 [!DNL Naver] 仅跟踪帐户](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)“ |
| [!DNL Yahoo! Display Network] | 文本和显示广告 | 当活动营销活动的跟踪设置包含选项&quot;[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]“”（在促销活动级别设置或从帐户设置继承），您无需为广告生成跟踪URL。 Search、Social和Commerce会在每次与广告网络同步时自动创建新的目标URL，并将嵌入了跟踪代码的目标网址上传到广告网络。<br><br>如果 [!UICONTROL Auto Upload] 选项被禁用，然后您可以使用生成跟踪URL [[!UICONTROL Tracking URLs] 工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)，然后使用广告网络的编辑器手动将它们添加到广告设置。 |

>[!MORELIKETHIS]
>
>* [使用跟踪URL工具生成搜索、社交和Commerce点击跟踪URL](/help/search-social-commerce/tools/click-tracking-url-generate.md)
>* [关于使用批量处理工作表管理营销活动数据](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)
>* [设置基于Cookie的点击跟踪](/help/search-social-commerce/tracking/click-tracking-set-up.md)
