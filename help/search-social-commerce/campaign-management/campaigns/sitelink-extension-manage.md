---
title: 管理共享的站点链接
description: 了解如何创建和管理共享站点链接扩展。
exl-id: e510f53b-f48c-4129-887c-351a840b8398
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 0%

---

# 管理共享的站点链接

仅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]*

从[!UICONTROL Extensions] > [!UICONTROL Sitelinks]库为任何同步的[!DNL Google Ads]或[!DNL Microsoft Advertising]帐户创建和管理帐户级别的共享站点链接。

## 创建共享站点链接

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**。

1. 在数据表上方的工具栏中，单击![创建](/help/search-social-commerce/assets/add.png "创建")。

1. 选择广告网络和帐户名称，然后单击&#x200B;**[!UICONTROL Continue]**。

1. 输入[共享站点链接设置](#shared-sitelink-settings)。

1. 单击&#x200B;**[!UICONTROL Post]**。

创建站点链接后，您可以[将其分配给帐户、营销活动或广告组](sitelink-extension-associate.md)。

## 编辑共享站点链接设置

您可以一次编辑一个共享站点链接。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**。

1. 选中要编辑的站点链接旁边的复选框。

1. 在数据表上方的工具栏中，单击![编辑](/help/search-social-commerce/assets/edit.png "编辑")。

1. 编辑[共享站点链接设置](#shared-sitelink-settings)。

1. 单击&#x200B;**[!UICONTROL Post]**。

## 删除共享的站点链接

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**。

1. 选中要删除的每个共享站点链接旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在工具栏中，单击![更多](/help/search-social-commerce/assets/more.png "更多")并选择&#x200B;**[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Delete]**。

## 共享站点链接设置 {#shared-sitelink-settings}

有关站点链接不批准的其他策略和原因，请参阅[[!DNL Google Ads]](https://support.google.com/adspolicy/answer/1054210)和[[!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/ext60206)站点链接扩展要求。

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]：**&#x200B;链接要显示的文本。 它最多可包含25个单字节字符或12个双字节字符。 链接文本在帐户或营销策划中必须唯一。

>[!NOTE]
>
>([!DNL Google Ads])在桌面和平板电脑的广告中显示35个字符的现有文本，但在移动设备上不显示。

**[!UICONTROL Status]：**&#x200B;站点链接的显示状态： *[!UICONTROL Active]*&#x200B;或&#x200B;*[!UICONTROL Deleted]* （仅限现有的站点链接）。 新站点链接的默认值为&#x200B;*[!UICONTROL Active]*。

**[!UICONTROL Description Line 1]，[!UICONTROL Description Line 2]：**&#x200B;搜索引擎可能在链接文本下显示的额外文本。 要包括说明，请为两个说明字段输入值。 每个描述字段最多可包含35个单字节字符或17个双字节字符。

**[!UICONTROL Start Date]：** （仅具有现有旧版站点链接或没有站点链接的营销活动；可选）站点链接在营销活动中可能显示广告的第一个日期。 新站点链接的默认值为当天。 要指定将来的开始日期，请以YYYY/MM/DD或M/D/YYYY格式输入日期，或单击   并选择日期。

**[!UICONTROL End Date]：**（可选）在营销活动中可能显示带有广告的站点链接的最后日期。 默认情况下，站点链接可能会无限期显示。 要指定结束日期，请以YYYY/MM/DD或M/D/YYYY格式输入日期，或单击   并选择日期。

**[!UICONTROL Mobile Preference]：** （可选）允许网络尝试向移动设备用户（而非桌面或平板电脑用户）显示广告扩展。 默认情况下，该选项未启用，并且广告扩展显示在任何设备类型上。

>[!NOTE]
>
>网络不保证会在首选设备类型上显示广告扩展。

### [!UICONTROL Tracking URLs]

**[!UICONTROL Base URL]**&#x200B;搜索引擎用户在单击您的广告时将被带入的登陆页面URL。 包括任何用于确定页面内容的参数。 如果输入值，则会覆盖广告的基本URL。

保存记录后，基本URL将包含为促销活动或帐户配置的任何附加参数。

>[!NOTE]
>
>* （具有最终URL的帐户）基本URL可能包含登陆页面域或子域中的重定向，但登陆页面域外部不包含重定向。 广告网络从此URL中提取域，并为广告添加任何可选的显示路径，以创建广告的显示URL。
>* ([!DNL Google Ads])营销活动或广告组中的每个站点链接都必须具有一个唯一的登陆页面，并且每个站点链接登陆页面的内容必须具有大约80%的唯一内容。 例如，不能在同一页面中拥有链接指向多个锚点的站点链接。
>* ([!DNL Google Ads])避免使用宏，宏不会替代来自启用并行跟踪的源的点击。 如果广告商必须使用宏，则Adobe客户团队应与客户支持或实施团队合作来添加宏。

**[!UICONTROL Tracking Template]：**（可选）跟踪模板或跟踪URL，它指定所有登入外域重定向和跟踪参数，并将最终/登陆页面URL嵌入到参数中。 示例： `{lpurl}?source={network}&id=5`或`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`以包含重定向。

* 对于Adobe Advertising转化跟踪（在营销活动设置包括&quot;[!UICONTROL EF Redirect]&quot;和&quot;自动上传&quot;时应用），Search、Social和Commerce会在您保存记录时自动为自己的点击跟踪代码添加前缀。

* 有关嵌入最终URL所支持的参数，请参阅[[!DNL Google Ads] 文档](https://support.google.com/google-ads/answer/6305348)中“可用的[!DNL ValueTrack]参数”部分中的([!DNL Microsoft Advertising]) [[!DNL Microsoft Advertising] 文档](https://help.ads.microsoft.com/#apex/3/en/56799)或([!DNL Google Ads])“仅跟踪模板”参数。

* 您可以选择包含URL参数以及为营销活动定义的任何自定义参数，这些参数以&amp;号分隔，如`{lpurl}?matchtype={matchtype}&device={device}`。

* 您可以选择添加第三方重定向和跟踪。

>[!NOTE]
>
>* 当营销活动设置包括“[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]”时，Search、Social和Commerce会在您保存记录时自动为其自己的重定向和跟踪代码添加前缀。
>* 最细粒度级别的跟踪模板将覆盖所有更高级别的值。 例如，如果帐户设置和关键词设置都包含一个值，则会应用关键词值。
>* ([!DNL Google Ads])如果在站点链接或关键字级别更新跟踪模板，则将重新提交相关广告以供审阅。 您可以在帐户、营销活动或广告组级别更新跟踪模板，而无需重新提交广告以供审批。
>* ([!DNL Microsoft Advertising])您可以在任何级别更新跟踪模板，而无需重新提交广告以供审批。
>* 对于[!DNL Google Ads]，请避免使用宏，这些宏不会替代来自启用并行跟踪的源的点击。 如果广告商必须使用宏，则Adobe客户团队应与客户支持或实施团队合作来添加宏。

>[!MORELIKETHIS]
>
>* [关于站点链接扩展](sitelink-extension-about.md)
>* [将共享站点链接与帐户、营销活动和广告组关联](sitelink-extension-associate.md)
