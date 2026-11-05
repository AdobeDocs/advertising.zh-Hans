---
title: 管理共享站点链接扩展
description: 了解如何创建、编辑和删除共享站点链接扩展。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 10d7adc3b3ced812ee1281139a23a573df2beeef
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 0%
---
# 管理共享站点链接扩展

仅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户*

站点链接是文本广告列表中的额外文本链接。 使用站点链接将用户直接引导至您网站上的特定页面。 广告网络根据站点链接与广告的相关性确定要显示的站点链接。

您可以选择为每个站点链接包含描述性文本。 当与站点链接高度相关时，广告网络还可能会显示帐户中现有广告的副本。 [!DNL Google Ads]可能会在桌面广告中显示2-6个站点链接，在移动广告中最多显示4个站点链接。 [!DNL Microsoft Advertising]可能显示有描述的2个、4个或6个站点链接，也可能显示无描述的4到6个站点链接。

在帐户级别为[同步的广告网络帐户](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md)创建共享站点链接文本和设置。 库中的站点链接不会与广告一起使用，直到您将它们与帐户实体关联为止。

## 关于[!UICONTROL Sitelinks]和[!UICONTROL Associations]查看 {#sitelink-view-about}

在&#x200B;**[!UICONTROL Library]>[!UICONTROL Extensions]**&#x200B;中，**[!UICONTROL Sitelinks]**&#x200B;选项卡列出了帐户级别的共享站点链接。 **[!UICONTROL Associations]**&#x200B;选项卡列出了扩展和帐户实体之间的关联。

查看这些选项卡需要[!UICONTROL View Extensions]权限。 创建、编辑和删除站点链接以及创建或删除关联需要[!UICONTROL Edit Extensions]权限。

有关每个[Google Ads帐户](https://support.google.com/google-ads/answer/6372658)和每个[Microsoft Advertising帐户](https://help.ads.microsoft.com/#apex/3/en/52001)的最大扩展数，请参阅广告网络帮助。

### 可用操作

* [创建共享站点链接](#sitelink-create)

* [编辑共享站点链接设置](#sitelink-edit)

* [删除共享的站点链接](#sitelink-delete)

* [将共享站点链接与帐户、营销活动和广告组关联](ad-extension-association-manage.md#sitelink-associate)

* [删除扩展关联](ad-extension-association-manage.md#association-delete)

* [将选定行中的所有数据复制到剪贴板](#copy-to-clipboard)

## 创建共享站点链接 {#sitelink-create}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Library]>[!UICONTROL Extensions]**，然后单击&#x200B;**[!UICONTROL Sitelinks]**&#x200B;选项卡。

1. 单击&#x200B;**[!UICONTROL Create Sitelink]**。

1. 在&#x200B;**[!UICONTROL Basic Settings]**&#x200B;中，选择广告网络和帐户。

1. 输入[共享站点链接设置](#shared-sitelink-settings)。

1. 单击&#x200B;**[!UICONTROL Review and Save]**。

1. 查看设置。 要更改设置，请单击适用部分中的&#x200B;**[!UICONTROL Edit]**。

1. 单击&#x200B;**[!UICONTROL Create]**。

创建站点链接后，[将其与帐户、营销活动或广告组关联](ad-extension-association-manage.md#sitelink-associate)。

## 编辑共享站点链接设置 {#sitelink-edit}

您可以一次编辑一个共享站点链接。 创建后无法更改其开始日期。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Library]>[!UICONTROL Extensions]**，然后单击&#x200B;**[!UICONTROL Sitelinks]**&#x200B;选项卡。

1. 选中一个站点链接旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Edit]**。

1. 编辑[共享站点链接设置](#shared-sitelink-settings)。

1. 单击&#x200B;**[!UICONTROL Review and Save]**，查看设置，然后单击&#x200B;**[!UICONTROL Update]**。

您还可以通过单击站点链接的值，直接在数据表中编辑其&#x200B;**[!UICONTROL Base URL]**&#x200B;或&#x200B;**[!UICONTROL Tracking Template]**。

## 删除共享的站点链接 {#sitelink-delete}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Library]>[!UICONTROL Extensions]**，然后单击&#x200B;**[!UICONTROL Sitelinks]**&#x200B;选项卡。

1. 选中要删除的每个共享站点链接旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。

要删除关联而不从库中删除共享站点链接，请改为删除关联[](ad-extension-association-manage.md#association-delete)。

## 将选定行中的所有数据复制到剪贴板 {#copy-to-clipboard}

根据应用的筛选条件和视图中可见的列，复制选定行中的可见信息。 信息将另存为制表符分隔值(TSV)。

1. 选中要复制其数据的每一行旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Copy]**。

## 共享站点链接设置 {#shared-sitelink-settings}

有关站点链接不批准的其他策略和原因，请参阅[Google广告站点链接要求](https://support.google.com/adspolicy/answer/1054210)和[Microsoft Advertising站点链接要求](https://help.ads.microsoft.com/#apex/ads/en/ext60206)。

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]：**&#x200B;链接要显示的文本。 它最多可包含25个单字节字符或12个双字节字符。 链接文本在帐户或营销策划中必须唯一。

>[!NOTE]
>
>([!DNL Google Ads])在桌面和平板电脑的广告中显示35个字符的现有文本，但在移动设备上不显示。

**[!UICONTROL Status]：**&#x200B;站点链接的显示状态： **[!UICONTROL Active]**&#x200B;或现有站点链接的&#x200B;**[!UICONTROL Deleted]**。 默认情况下，新站点链接处于活动状态。

**[!UICONTROL Description Line 1]，[!UICONTROL Description Line 2]：**&#x200B;广告网络可能在链接文本下显示的额外文本。 要包括说明，请输入这两个字段。 每个字符最多可包含35个单字节字符或17个双字节字符。

**[!UICONTROL Start Date]：** （可选；仅限创建）可以显示站点链接的第一个日期。 默认值为当天。 要指定将来的日期，请以YYYY/MM/DD格式输入日期或使用日期选取器。 现有站点链接的开始日期为只读。

**[!UICONTROL End Date]：** （可选）可能显示站点链接的最后日期。 默认情况下，站点链接可能会无限期显示。 要指定结束日期，请以YYYY/MM/DD格式输入或使用日期选取器。

**[!UICONTROL Mobile Preference]：** （可选）允许网络尝试向移动设备用户（而非桌面或平板电脑用户）显示扩展。 默认情况下，此选项处于未启用状态，并且扩展可以出现在任何设备类型上。 网络不保证会在首选设备类型上显示扩展。

### [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

**[!UICONTROL Tracking Template]：**（可选）跟踪URL，包括登陆域外部重定向和跟踪参数，最终登陆页面URL嵌入在参数中。 例如，`https://www.trackingservice.example.com/?url={lpurl}&source={network}&id=5`。

在此视图中，为[!UICONTROL Base URL]和[!UICONTROL Tracking Template]输入的值必须以`http://`或`https://`开头，且不能包含空格。

* 当营销活动设置包括&#x200B;**[!UICONTROL EF Redirect]**&#x200B;和&#x200B;**[!UICONTROL Auto Upload]**&#x200B;时，Search、Social和Commerce会在您保存记录时自动为其自己的重定向和跟踪代码添加前缀。

* 有关嵌入最终URL的参数，请参阅[Microsoft Advertising文档](https://help.ads.microsoft.com/#apex/3/en/56799)或[Google Ads ValueTrack文档](https://support.google.com/google-ads/answer/6305348)中的“仅跟踪模板”参数。

* 您可以包括URL参数和营销活动级别的自定义参数(以&amp;符号(`&`)分隔)，以及第三方重定向和跟踪。

* 最细粒度级别的跟踪模板将覆盖较高级别的模板。

>[!NOTE]
>
>* 对于具有最终URL的帐户，基本URL可能包含登陆页面域或子域内的重定向，但不会包含登陆页面域外的重定向。 广告网络提取域以创建显示URL。
>* ([!DNL Google Ads])营销活动或广告组中的每个站点链接必须具有约80%的唯一内容的唯一登陆页面。 请勿将指向同一页面上多个锚点的链接用作单独的站点链接登陆页面。
>* ([!DNL Google Ads])在站点链接或关键字级别更新跟踪模板会重新提交相关广告以供审阅。 在帐户、营销活动或广告组级别更新它不会重新提交广告。
>* ([!DNL Microsoft Advertising])您可以更新任何级别的跟踪模板，而无需重新提交广告以供审批。
>* ([!DNL Google Ads])避免使用宏，这些宏不会替代来自启用并行跟踪的源的点击。 如果需要宏，您的Adobe客户团队可与客户支持或实施团队合作来添加它们。

## 站点链接的性能数据 {#sitelink-performance}

搜索、Social和Commerce将广告扩展的单击次数和生成的转化率映射到与显示扩展的广告关联的关键字。 扩展级别的成本和点击数据在搜索、社交和Commerce中不可用。

在[!UICONTROL Transaction Report]中，`sl:<Sitelink text>`的[!UICONTROL Link Type]值（如`sl:See Current Offers`）从站点链接而不是广告本身中标识交易。 请参阅“[交易报告](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)”。

您可以查看扩展级别的成本，然后单击广告网络界面中的数据。

>[!MORELIKETHIS]
>
>* [管理Google Ads共享标注扩展](callout-extension-manage.md)
>* [管理广告扩展关联](ad-extension-association-manage.md)
