---
title: 管理Google Ads共享标注扩展
description: 了解如何创建、编辑和删除Google Ads共享的标注扩展。
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
source-wordcount: '685'
ht-degree: 0%
---
# 管理[!DNL Google Ads]共享标注扩展

仅&#x200B;*[!DNL Google Ads]个帐户*

标注扩展是有关您的网站提供的产品、服务或促销的信息性文本，其中显示有文本广告。 广告网络可能显示带有广告的2-4个标注。

您为[同步的Google广告帐户](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md)在帐户级别创建共享标注文本和设置。 库中的标注，只有在您将它们与搜索网络上支持的活动或广告组关联后，才会与广告一起使用。

要使您的广告符合显示标注的条件，请为每个活动或广告组至少分配两个标注。 广告组级别的标注会覆盖营销活动级别的标注。

## 关于[!UICONTROL Callouts]和[!UICONTROL Associations]查看 {#callout-view-about}

在&#x200B;**[!UICONTROL Library]>[!UICONTROL Extensions]**&#x200B;中，**[!UICONTROL Callouts]**&#x200B;选项卡列出了您的帐户级共享标注。 **[!UICONTROL Associations]**&#x200B;选项卡列出了扩展和帐户实体之间的关联。

查看这些选项卡需要[!UICONTROL View Extensions]权限。 创建、编辑和删除注解以及创建或删除关联需要[!UICONTROL Edit Extensions]权限。

有关每个帐户的最大扩展数量，请参阅[Google广告文档](https://support.google.com/google-ads/answer/6372658)，了解帐户限制。

### 可用操作

* [创建共享标注](#callout-create)

* [编辑共享的标注设置](#callout-edit)

* [删除共享标注](#callout-delete)

* [将共享标注(H)与营销活动和广告组关联](ad-extension-association-manage.md#callout-associate)

* [删除扩展关联](ad-extension-association-manage.md#association-delete)

* [将选定行中的所有数据复制到剪贴板](#copy-to-clipboard)

## 创建共享标注 {#callout-create}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Library]>[!UICONTROL Extensions]**，然后单击&#x200B;**[!UICONTROL Callouts]**&#x200B;选项卡。

1. 单击&#x200B;**[!UICONTROL Create Callout]**。

1. 在&#x200B;**[!UICONTROL Basic Settings]**&#x200B;中，选择[!DNL Google Ads]和帐户。

1. 输入[共享标注设置](#shared-callout-settings)。

1. 单击&#x200B;**[!UICONTROL Review and Save]**。

1. 查看设置。 要更改设置，请单击适用部分中的&#x200B;**[!UICONTROL Edit]**。

1. 单击&#x200B;**[!UICONTROL Create]**。

创建标注后，[将其与营销活动或广告组关联](ad-extension-association-manage.md#callout-associate)。

## 编辑共享的标注设置 {#callout-edit}

一次可以编辑一个共享标注。 创建后无法更改其开始日期。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Library]>[!UICONTROL Extensions]**，然后单击&#x200B;**[!UICONTROL Callouts]**&#x200B;选项卡。

1. 选中一个注解旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Edit]**。

1. 编辑[共享的标注设置](#shared-callout-settings)。

1. 单击&#x200B;**[!UICONTROL Review and Save]**，查看设置，然后单击&#x200B;**[!UICONTROL Update]**。

## 删除共享标注 {#callout-delete}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Library]>[!UICONTROL Extensions]**，然后单击&#x200B;**[!UICONTROL Callouts]**&#x200B;选项卡。

1. 选中要删除的每个共享编号说明旁边的复选框。

   有关选择多行的信息，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。

要删除关联而不从库中删除共享标注，请改为删除关联[&#128279;](ad-extension-association-manage.md#association-delete)。

## 将选定行中的所有数据复制到剪贴板 {#copy-to-clipboard}

根据应用的筛选条件和视图中可见的列，复制选定行中的可见信息。 信息将另存为制表符分隔值(TSV)。

1. 选中要复制其数据的每一行旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Copy]**。

## 共享注解设置 {#shared-callout-settings}

有关取消批准标注的其他策略和原因，请参阅[Google广告标注要求](https://support.google.com/adspolicy/answer/1054212)。

**[!UICONTROL Callout Text]：**&#x200B;要显示的文本。 它最多可包含25个单字节字符或12个双字节字符。 它不能包含感叹号或标点符号。

**[!UICONTROL Start Date]：** （可选；仅限创建）标注可能显示的第一个日期。 默认值为当天。 要指定将来的日期，请以YYYY/MM/DD格式输入日期或使用日期选取器。 现有注解的开始日期是只读的。

**[!UICONTROL End Date]：** （可选）标注可能显示的最后日期。 默认情况下，注解可能会无限期显示。 要指定结束日期，请以YYYY/MM/DD格式输入或使用日期选取器。

**[!UICONTROL Mobile Preference]：**（可选）允许[!DNL Google Ads]尝试向移动设备用户显示扩展，而不是向桌面或平板电脑用户显示。 否则，该扩展将显示在任何设备类型上。 [!DNL Google Ads]不保证会在首选设备类型上显示扩展。

## 标注的性能数据 {#callout-performance}

搜索、Social和Commerce将广告扩展的单击次数和生成的转化率映射到与显示扩展的广告关联的关键字。 扩展级别的成本和点击数据在搜索、社交和Commerce中不可用。

您可以在[!DNL Google Ads]界面中查看扩展级成本并单击数据。

>[!MORELIKETHIS]
>
>* [管理共享站点链接扩展](sitelink-extension-manage.md)
>* [管理广告扩展关联](ad-extension-association-manage.md)
