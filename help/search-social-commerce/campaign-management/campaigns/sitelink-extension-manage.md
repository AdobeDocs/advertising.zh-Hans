---
title: 管理共享站点链接
description: 了解如何创建和管理共享站点链接扩展。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 0%

---

# 管理共享站点链接

*[!DNL Google Ads]和 [!DNL Microsoft Advertising] 仅限*

为任何已同步内容创建和管理帐户级别的共享站点链接 [!DNL Google Ads] 或 [!DNL Microsoft Advertising] 帐户来自 [!UICONTROL Extensions] > [!UICONTROL Sitelinks] 库。

## 创建共享站点链接

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. 在数据表上方的工具栏中，单击 ![创建](/help/search-social-commerce/assets/add.png "创建").

1. 选择广告网络和帐户名称，然后单击 **[!UICONTROL Continue]**.

1. 输入 [共享站点链接设置](#shared-sitelink-settings).

1. 单击 **[!UICONTROL Post]**.

创建站点链接后，您可以 [将其分配给帐户、营销活动或广告组](sitelink-extension-associate.md).

## 编辑共享站点链接设置

您可以一次编辑一个共享站点链接。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. 选中要编辑的站点链接旁边的复选框。

1. 在数据表上方的工具栏中，单击 ![编辑](/help/search-social-commerce/assets/edit.png "编辑").

1. 编辑 [共享站点链接设置](#shared-sitelink-settings).

1. 单击 **[!UICONTROL Post]**.

## 删除共享的站点链接

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. 选中要删除的每个共享站点链接旁边的复选框。

   有关选择多行的提示，请参阅&quot;[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).”

1. 在工具栏中，单击 ![更多](/help/search-social-commerce/assets/more.png "更多") 并选择 **[!UICONTROL Delete]**.

1. 在确认消息中，单击 **[!UICONTROL Delete]**.

## 共享站点链接设置 {#shared-sitelink-settings}

有关站点链接不批准的其他策略和原因，请参阅 [[!DNL Google Ads]](https://support.google.com/adspolicy/answer/1054210) 和 [[!DNL Microsoft Advertising]](https://about.ads.microsoft.com/en-us/resources/policies/ad-extensions-policies) sitelink扩展要求。

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]：** 为链接显示的文本。 它最多可包含25个单字节字符或12个双字节字符。 链接文本在帐户或营销策划中必须是唯一的。

>[!NOTE]
>
>([!DNL Google Ads])现有35个字符的文本在台式机和平板电脑的广告中显示，但不在移动设备上显示。

**[!UICONTROL Status]：** 站点链接的显示状态：  *[!UICONTROL Active]* 或 *[!UICONTROL Deleted]* （仅限现有站点链接）。 新站点链接的缺省值为 *[!UICONTROL Active]*.

**[!UICONTROL Description Line 1]， [!UICONTROL Description Line 2]：** 搜索引擎可能显示在链接文本下方的额外文本。 要包括说明，请为两个说明字段输入值。 每个描述字段最多可包含35个单字节字符或17个双字节字符。

**[!UICONTROL Start Date]：** （仅限具有现有旧版站点链接或没有站点链接的营销活动；可选）在营销活动中可能显示带有广告的站点链接的首次日期。 新站点链接的默认值为当天。 要指定将来的开始日期，请以YYYY/MM/DD或M/D/YYYY格式输入日期，或单击并选择日期。

**[!UICONTROL End Date]：** （可选）在营销活动中可能显示带有广告的站点链接的最后日期。 默认情况下，站点链接可能会无限期显示。 要指定结束日期，请以YYYY/MM/DD或M/D/YYYY格式输入日期，或单击并选择日期。

**[!UICONTROL Mobile Preference]：** （可选）允许网络尝试向移动设备用户（而非桌面或平板电脑用户）显示广告扩展。 默认情况下，该选项未启用，并且广告扩展显示在任何设备类型上。

>[!NOTE]
>
>网络不保证会在首选设备类型上显示广告扩展。

### [!UICONTROL Tracking URLs]

**[!UICONTROL Base URL]** 搜索引擎用户在单击您的广告时进入的登陆页面URL。 包括确定页面内容的任何参数。 如果输入值，则会覆盖广告的基本URL。

保存记录后，基本URL将包含为促销活动或帐户配置的任何附加参数。

>[!NOTE]
>
>* （具有最终URL的帐户）基本URL可能包含登陆页面域或子域内的重定向，但登陆页面域外无重定向。 广告网络从此URL中提取域，并为广告添加任何可选的显示路径，以创建广告的显示URL。
>* ([!DNL Google Ads])营销活动或广告组中的每个站点链接都必须具有一个唯一的登陆页面，并且每个站点链接登陆页面的内容必须具有大约80%的唯一内容。 例如，您不能在同一页面中拥有指向多个锚点的链接的站点链接。
>* ([!DNL Google Ads])避免使用宏，宏不会替代来自启用并行跟踪的源的点击。 如果广告商必须使用宏，则Adobe帐户团队应与客户支持或实施团队合作来添加宏。


**[!UICONTROL Tracking Template]：** （可选）跟踪模板或跟踪URL，用于指定所有登陆域重定向和跟踪参数，并将最终/登陆页面URL嵌入到参数中。 示例： `{lpurl}?source={network}&id=5` 或 `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` 以包含重定向。

* 对于Adobe广告转化跟踪（在营销活动设置包括“EF重定向”和“自动上传”时应用），Search、Social和Commerce会在您保存记录时自动为其自身的点击跟踪代码添加前缀。

* 有关嵌入最终URL的支持参数，请参阅([!DNL Microsoft Advertising] 仅限) [[!DNL Microsoft Advertising] 文档](https://help.ads.microsoft.com/#apex/3/en/56799) 或([!DNL Google Ads] 仅限)中有关“可用ValueTrack参数”的部分中的“仅限跟踪模板”参数。 [[!DNL Google Ads] 文档](https://support.google.com/google-ads/answer/6305348).

* 您可以选择包括URL参数和为促销活动定义的任何自定义参数，各个参数之间以&amp;号分隔，例如 `{lpurl}?matchtype={matchtype}&device={device}`.

* 您可以选择添加第三方重定向和跟踪。

>[!NOTE]
>
>* 当营销活动设置包括“[!UICONTROL EF Redirect]“ ”和“ ”[!UICONTROL Auto Upload]，”当您保存记录时，Search、Social和Commerce会自动为自己的重定向和跟踪代码添加前缀。
>* 最精细级别的跟踪模板将覆盖所有更高级别的值。 例如，如果帐户设置和关键词设置都包含一个值，则会应用关键词值。
>* ([!DNL Google Ads])如果您在站点链接或关键词级别更新跟踪模板，则会重新提交相关广告以供审阅。 您可以在帐户、营销活动或广告组级别更新跟踪模板，而无需重新提交广告以供审批。
>* ([!DNL Microsoft Advertising])您可以在任何级别更新跟踪模板，而无需重新提交广告以供审批。
>* 对象 [!DNL Google Ads]，避免使用宏，宏不会替代来自启用并行跟踪的源的点击。 如果广告商必须使用宏，则Adobe帐户团队应与客户支持或实施团队合作来添加宏。


>[!MORELIKETHIS]
>
>* [关于站点链接扩展](sitelink-extension-about.md)
>* [将共享站点链接与帐户、营销活动和广告组关联](sitelink-extension-associate.md)

