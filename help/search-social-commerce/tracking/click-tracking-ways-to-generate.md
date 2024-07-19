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
| [!DNL Baidu]、[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads]和[!DNL Yandex] | <ul><li>文本广告</li><li>关键字</li><li>（[!DNL Google Ads]个内容营销活动）投放位置</li><li>（[!DNL Google Advertising]和[!DNL Advertising]）站点链接</li></ul> | 当活动营销活动的跟踪设置包含选项“[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]”（在营销活动级别设置或继承自帐户设置）时，您无需为广告组组件生成跟踪URL。 Search、Social和Commerce每次与广告网络同步时，都会自动创建以下类型的跟踪URL并将其上传到广告网络： a)（具有最终URL的帐户）用于跟踪模板的搜索、Social和Commerce跟踪参数以及附加到最终URL的相同参数， b)（具有目标URL的帐户）嵌入了Search、Social和Commerce跟踪代码的新目标URL，以及c) （[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户）登陆页面后缀（最终URL后缀）参数。<br><br>如果[!UICONTROL Auto Upload]选项已禁用，则可以通过以下任一方式为组件生成跟踪URL：<ul><li>（[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Ads]和[!DNL Yandex]）从馈送文件发布广告时，请选择[!UICONTROL Generate Tracking URLs]选项。 您可以选择在将任何批量处理工作表文件发布到广告网络之前，验证其中的跟踪模板字段。</li><li>下载、上载或发布包含该组件的批量处理工作表文件时，请选择[!UICONTROL Generate Tracking URLs]选项。 对于具有目标URL的帐户，您可以选择在将文件发布到广告网络之前验证基本URL/最终URL字段字段</li><li>使用[[!UICONTROL Tracking URLs]工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)生成跟踪URL并将其手动添加到相应的[!UICONTROL Tracking Template]或[!UICONTROL Base URL]字段。 <b>注意：</b>您生成的跟踪模板不包含帐户或营销活动设置中指定的任何其他跟踪参数。<ul><li>Google帐户)转到[[!UICONTROL Tracking URLs]工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)，复制相应[!UICONTROL Tracking Template]字段中的屏幕值，并手动将整个跟踪字符串添加到组件设置。 您必须在`&url=`参数（如`{lpurl}`）之后为最终URL添加[!DNL Google Ads] [!DNL ValueTrack]参数。 有关在跟踪模板中指示最终URL的[!DNL ValueTrack]参数列表，请参阅[[!DNL Google Ads]文档]9https://support.google.com/google-ads/answer/2375447中“可用[!DNL ValueTrack]参数”部分中的“仅跟踪模板”参数。</li><li>（具有最终URL的其他帐户）使用[[!UICONTROL Tracking URLs]工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)生成跟踪URL，并手动将整个跟踪字符串添加到组件设置。 必须在`&url=`参数（如`{lpurl}`）之后为最终URL添加参数。 对于[!DNL Yahoo! Japan Ads]帐户，请使用参数`{lpurl}`。 有关在跟踪模板中指示最终URL的[!DNL Microsoft Advertising]参数列表，请参阅[[!DNL Microsoft Advertising] 文档](https://help.bingads.microsoft.com/#apex/3/en/56799)。</li><li>（具有目标URL的帐户）使用[[!UICONTROL Tracking URLs]工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)生成跟踪URL，并在相应的[!UICONTROL Base URL]字段中手动添加跟踪URL。</li></ul></li></ul><b>注释：</b><br><br><ul><li>（具有最终URL的帐户）使用最细粒度级别的跟踪模板（例如，关键字级别的跟踪模板将覆盖帐户、营销活动和广告组级别的模板，而关键字的跟踪模板和投放位置将覆盖关联广告的跟踪模板）。</li><li>Adobe Advertising将站点链接的点击量和产生的收入映射到与包含站点链接的广告关联的关键字，而不是单独映射。 请参阅“[支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)”。</li></ul><b>提示：</b>（具有最终URL的帐户）如果您仅在所需的最高级别（例如，帐户或营销活动级别的跟踪模板）创建跟踪模板，以将相同的跟踪应用于帐户或营销活动中的所有实体，则最容易管理跟踪。 |
| [!DNL Google Ads] | 电话分机 | 不适用 |
| [!DNL Google Ads]，[!DNL Microsoft Advertising] | 产品广告 | <ul><li>[!DNL Microsoft Merchant Center]帐户：使用购物广告的[跟踪模板格式](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)为[!DNL Microsoft Merchant Center]帐户中的每个产品手动创建跟踪URL，并将其手动添加到帐户、营销活动或产品组设置中的[!UICONTROL Tracking Template]字段。<br><br>或者，您也可以将跟踪URL添加到[!DNL Microsoft Merchant Center account]内的产品数据中。 为此，请在产品信息源](https://help.ads.microsoft.com/#apex/3/en/51084)的[自定义列“[!DNL bingads_redirect]”中包含跟踪URL以及相应的“[!DNL link]”或“[!DNL mobile_link]”字段中的值。 “[!DNL bingads_redirect]”字段中的值替换了“[!DNL link]”和“[!DNL mobile_link]”字段中的值。 使用此方法生成的URL不包含帐户设置中指定的任何跟踪参数。<br><br><b>注意：</b>同步期间用于自动上传跟踪的帐户级别和营销活动级别功能不会为新的[!DNL Microsoft Advertising]产品组生成跟踪。 解决方法是在上传或发布批量处理工作表时生成跟踪。</li><li>[!DNL Google Merchant Center]帐户：使用[[!UICONTROL Tracking URLs]工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)生成跟踪URL，并将其手动添加到帐户、营销活动或产品组设置中的[!UICONTROL Tracking Template]字段。</li></ul> |
| [!DNL Naver] | 关键字 | 您可以通过[批量工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)为所有广告设置点击跟踪。 或者，您也可以手动生成广告的跟踪URL，并使用广告网络的编辑器手动将其添加到广告设置。 请参阅“[实施 [!DNL Naver] 仅跟踪帐户](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)”。 |
| [!DNL Yahoo! Display Network] | 文本和显示广告 | 当活动营销活动的跟踪设置包含选项“[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]”（在营销活动级别设置或继承自帐户设置）时，您无需为广告生成跟踪URL。 Search、Social和Commerce会在每次与广告网络同步时自动创建新的目标URL，并将嵌入了跟踪代码的目标网址上传到广告网络。<br><br>如果[!UICONTROL Auto Upload]选项已禁用，则可以使用[[!UICONTROL Tracking URLs]工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)生成跟踪URL，并使用广告网络的编辑器手动将其添加到广告设置。 |

>[!MORELIKETHIS]
>
>* [使用“跟踪URL”工具生成搜索、社交和Commerce点击跟踪URL](/help/search-social-commerce/tools/click-tracking-url-generate.md)
>* [关于使用批量处理工作表管理营销活动数据](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)
>* [设置基于Cookie的点击跟踪](/help/search-social-commerce/tracking/click-tracking-set-up.md)
