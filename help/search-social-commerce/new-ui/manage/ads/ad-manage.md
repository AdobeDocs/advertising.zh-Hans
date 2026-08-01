---
title: 管理广告
description: 了解如何创建和管理广告，包括可用的广告类型。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 730b474b83ae4df47c18f93adfec62b1dc9b8a16
workflow-type: tm+mt
source-wordcount: 1732
ht-degree: 0%

---

# 管理广告

*Beta功能*

仅&#x200B;*[!DNL Google Ads]、[!DNL LY Ads]、[!DNL Microsoft Advertising]、[!DNL Yandex]和现有[!DNL Baidu]帐户*

广告属于一个广告组，包含向用户显示的内容，例如标题、描述、图像或其他创意元素，具体取决于广告网络和广告类型。

一旦您[使广告网络帐户可通过API连接访问](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)，并且Search、Social和Commerce已将帐户数据与广告网络同步，您即可为[支持的营销活动类型](/help/search-social-commerce/introduction/supported-inventory.md)创建广告。 您还可以编辑和更改广告的状态。

有关每个广告网络可用功能的详细信息，请参阅[支持的清单](/help/search-social-commerce/introduction/supported-inventory.md)。

## 关于[!UICONTROL Ads]视图 {#ad-view-about}

[!UICONTROL Manage] > [!UICONTROL Ads]视图在筛选视图中列出了选定广告商帐户的所有广告。

### 可用操作

* [创建广告](#ad-create)

* [从行中重命名广告](#ad-rename)

* [编辑广告设置](#ad-edit)

* [更改广告的状态或删除广告](#ad-status)

* [从[!UICONTROL Ads]视图管理数据视图报告](#ad-reports)

## 可用广告类型 {#ad-types}

您可以在同步的广告网络帐户中创建和管理广告组支持的广告类型：

* 在针对搜索网络的营销活动中针对广告组&#x200B;**文本广告或扩展文本广告**。 文本广告可以包含覆盖广告组或营销活动级别参数的可选跟踪参数。 根据广告网络，您可以创建扩展/扩展文字广告或标准文字广告。

* 针对[!DNL Microsoft Audience Network]上[!DNL Microsoft Advertising]营销活动的跨设备、本机&#x200B;**受众广告**。 根据促销活动设置，您有两个受众广告选项：

  * 如果促销活动链接到商户中心商店，则让广告网络使用商店的产品信息，自动为促销活动生成基于信息源的广告。 您无需为营销活动创建基于信息源的广告，但必须创建具有用户定位的广告组。

  * 如果促销活动未链接到商家中心帐户，则使用响应式广告格式创建基于图像的受众广告，其中包含多个文本和图像资源。 广告网络使用最有效的广告元素组合来组合广告，并在[!DNL MSN]、[!DNL Outlook.com]和[!DNL Microsoft Edge]等网站上显示它们。

* 搜索网络上[!DNL Google Ads]促销活动的&#x200B;**仅限呼叫的广告**。 仅限呼叫的广告是包含电话号码的文字广告。 您可以选择使用[!DNL Google Ads]分配的转接号码进行高级呼叫报告。

  >[!NOTE]
  >
  >您当前无法创建或编辑仅限呼叫的广告。 您可以查看、更改现有仅限呼叫广告的状态或删除该广告。

* 在搜索促销活动中&#x200B;**扩展了[!DNL Google Ads]和[!DNL Microsoft Advertising]动态搜索广告组的动态搜索广告**（现在在广告网络上仅称为“动态搜索广告”）。 动态搜索广告使用网站中的内容而不是关键字来确定何时显示广告。 广告网络动态生成标题，选择登陆页面URL和显示URL，并自动生成最终URL。

  有关动态搜索广告的更多信息，请参阅[[!DNL Google Ads] 文档](https://support.google.com/google-ads/answer/2471185)和[[!DNL Microsoft Advertising] 文档](https://help.ads.microsoft.com/#apex/ads/en/56794)。

* 针对[!DNL Microsoft Advertising]搜索营销活动的&#x200B;**多媒体广告**。 多媒体广告是以突出的主线和侧栏位置显示的大型图像广告，并且每页只显示一个多媒体广告。 它们可以包括多个文本和图像资产，例如响应式广告，并且广告网络使用最有效的广告元素组合来组合广告。 多媒体广告不会取代文本广告投放。

* 购物网络上&#x200B;**[!DNL Microsoft Advertising]产品（购物）广告**&#x200B;的促销行。 购物广告使用您现有的[!DNL Microsoft Merchant Center]产品信息源中的产品（而不是关键字）来确定显示广告的方式和位置。 广告文案和登陆页面URL是根据信息源中的产品信息自动生成的，但您可以选择设置促销行以将其包含在广告组中。

  有关产品广告的更多信息，请参阅[Microsoft Advertising文档](https://help.ads.microsoft.com/#apex/3/en/51082)。

* 搜索网络中[!DNL Google Ads]和[!DNL Microsoft Advertising]促销活动的&#x200B;**响应式搜索广告**。 该广告网络动态地组合来自一组广告标题和描述的基于文本的响应式搜索广告，从而有利于共同表现良好的组合。 广告最多包含三个标题、两个描述，以及来自基本URL和可选path1和path2字段的可自定义URL。 您可以选择将广告标题和说明固定到特定职位。

  >[!NOTE]
  >
  >[!DNL Google Ads]不在其本机编辑器之外提供有关显示为广告的文本组合的数据。 有关每个文本组合报表的更多信息，请参阅[Google广告文档](https://support.google.com/google-ads/answer/7684791)。

### 广告级别的效果数据

广告级别的数据适用于大多数广告类型。

但是，它不适用于[!DNL Google Ads]动态搜索广告(DSA)、最佳效果、智能购物和[!DNL YouTube]营销活动。 预计营销活动的广告级别数据总数与营销活动数据总数之间存在差异。

| 广告网络/营销活动/广告类型 | 数据可用性 |
|---|---|
| [!DNL Google Ads]动态搜索广告(DSA) | 营销活动、广告组 |
| 最大[!DNL Google Ads]性能 | 营销活动 |
| [!DNL Google Ads]购物，智能购物 | 营销活动、广告组 |
| [!DNL Google Ads] [!DNL YouTube] | 营销活动、广告组 |

## 创建广告 {#ad-create}

<!-- Verify that this note is still applicable -->

>[!NOTE]
>
>* 您不需要为购物营销活动创建产品广告；广告网络会自动创建它们。 但是，对于[!DNL Microsoft Advertising]购物营销活动，您可以选择定义要包含在广告中的促销行。
>* 您无法创建[!DNL Google Ads]仅限呼叫的广告。

>[!TIP]
>
>若要同时创建大量广告，请使用[营销活动批量工作表](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ads]**。

1. 单击&#x200B;**[!UICONTROL Create Ads]**。

1. 在&#x200B;**[!UICONTROL Basic Settings]**&#x200B;步骤中，选择网络、帐户、营销策划、广告组和广告类型。

   有关可用广告类型的详细信息，请参阅[可用广告类型](#ad-types)。

1. 请为[百度文本广告](ad-settings-baidu-text.md)、[Google广告扩展动态搜索广告](ad-settings-google-dsa.md)（在Google广告中仅称为“动态搜索广告”）、[Google广告响应式搜索广告](ad-settings-google-rsa.md)、[Microsoft Advertising扩展动态搜索广告](ad-settings-microsoft-dsa.md)、[Microsoft Advertising多媒体广告](ad-settings-microsoft-multimedia.md)、[Microsoft Advertising产品广告](ad-settings-microsoft-product.md)、[Microsoft响应式广告](ad-settings-microsoft-responsive.md)、[Advertising响应式搜索广告](ad-settings-microsoft-rsa.md)或[Yandex文本广告](ad-settings-yandex-text.md)设置指定其余设置。

   >[!NOTE]
   >
   >（具有Adobe Advertising转化跟踪的促销活动）如果帐户或促销活动设置仅在关键词级别指定跟踪，则Search、Social和Commerce不会生成广告跟踪。

1. 单击&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，请单击![编辑](/help/search-social-commerce/assets/edit-new.png "编辑")**[!UICONTROL Edit]**&#x200B;并更改广告设置。

1. 单击&#x200B;**[!UICONTROL Create]**。

1. &#x200B;<!-- Add link to where to generate this once available to users-->（促销活动中的购物广告具有Adobe Advertising转化跟踪；可选）要跟踪广告的点击量，请手动将跟踪URL添加到帐户、促销活动或产品组设置。

## 重命名广告 {#ad-rename}

快速重命名广告，无需打开完整的广告设置。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ads]**。

1. 将光标悬停在广告行上并单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Rename]**。

1. 编辑名称，然后单击&#x200B;**[!UICONTROL Apply]**。

## 编辑广告设置 {#ad-edit}

>[!NOTE]
>
>* 以下广告类型为&#x200B;*可变*，这意味着您可以更改广告副本或图像并保留相同的广告ID：除动态搜索广告之外的所有[!DNL Google Ads]广告类型以及[!DNL Microsoft Advertising]扩展的文本广告。
>* 所有其他支持的广告均为&#x200B;*不可变*，这意味着更改广告副本或图像将删除现有广告并创建新广告。 当Search、Social和Commerce收集足够的数据以进行优化时，新广告的性能可能会出现几周的波动。
>* 您无法编辑产品广告的内容，但[!DNL Microsoft Advertising]产品广告的促销行除外。 但是，您可以暂停或删除广告。
>* 您无法编辑[!DNL Google Ads]仅限呼叫的广告。 但是，您可以暂停或删除其中一个项目。
>* 您一次只能编辑一个广告。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ads]**。

1. 选中广告旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Edit]**。

1. 在&#x200B;**[!UICONTROL Ad Details]**&#x200B;步骤中，编辑[百度文本广告](ad-settings-baidu-text.md)、[Google广告扩展动态搜索广告](ad-settings-google-dsa.md)（现在在Google广告中仅称为“动态搜索广告”）、[Google广告响应式搜索广告](ad-settings-google-rsa.md)、[Microsoft Advertising扩展动态搜索广告](ad-settings-microsoft-dsa.md)、[Microsoft Advertising多媒体广告](ad-settings-microsoft-multimedia.md)、[Microsoft Advertising产品广告](ad-settings-microsoft-product.md)、[Microsoft响应式广告](ad-settings-microsoft-responsive.md)、[Advertising响应式搜索广告](ad-settings-microsoft-rsa.md)或[Yandex文本广告](ad-settings-yandex-text.md)设置。

1. 单击&#x200B;**[!UICONTROL Review and Save]**。

1. 如有必要，请单击![编辑](/help/search-social-commerce/assets/edit-new.png "编辑")**[!UICONTROL Edit]**&#x200B;并更改广告设置。

1. 单击&#x200B;**[!UICONTROL Update]**。

## 更改广告的状态 {#ad-status}

无需打开完整的广告设置即可快速更改广告状态。

您可以暂停受支持广告网络上的任何活动广告以禁用对该广告的竞价。 您稍后可以通过将状态更改回“活动”来恢复竞价。

您还可以删除任何活动或暂停的广告。 已删除的广告将从广告网络删除。 当您将其包含在数据过滤器中时，它们仍可见，但无法进行更改。

### 激活或暂停广告

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ads]**。

1. 选中广告行的复选框。

1. 在批量操作工具栏中，更改状态：

   * 要激活暂停的广告，请单击&#x200B;**[!UICONTROL Activate]**。

   * 要暂停活动广告，请单击&#x200B;**[!UICONTROL Pause]**。

### 删除广告

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ads]**。

1. 选中广告行的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。

## 从[!UICONTROL Ads]视图管理数据视图报告 {#ad-reports}

生成一份报表，其中包含[!UICONTROL Ads]视图中的一个或多个广告的数据行，然后以Microsoft Excel工作表文件（XLXS格式）的形式下载该报表。 报告包含视图中的所有可见列。

您可以删除任何生成的报表。

另请参阅&quot;[（旧版UI）从营销活动管理视图](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)下载数据&quot;和&quot;[（旧版UI）从[!UICONTROL Downloads]菜单](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)删除性能数据报告或批量处理工作表文件&quot;。

### 生成具有已过滤数据行的报告

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ads]**。

1. 指定要下载其数据的广告：

   * 要下载特定广告的数据，请选中广告旁边的复选框。

   * 要下载所有广告的数据，您无需选中任何复选框。 默认情况下包含所有广告。

1. 在数据表上方的工具栏中，单击![下载报表](/help/search-social-commerce/assets/download.png "下载报表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]设置中，输入唯一的报表名称，然后单击&#x200B;**[!UICONTROL Generate]**。

   默认情况下，该文件名为“ad_YYYYMMDD_NNNN”，其中“NNNN”是顺序作业编号（如“ad_20250402_1326）。

   文件已添加到[!UICONTROL Recently Generated]列表。

1. （可选）要在文件完成后下载文件，请单击文件名旁边的![下载](/help/search-social-commerce/assets/download.png "下载")。

   将按照浏览器的正常过程下载文件。

### 下载已完成的报表

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ads]**。

1. 在数据表上方的工具栏中，单击![下载报表](/help/search-social-commerce/assets/download.png "下载报表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]对话框的[!UICONTROL Recently Generated]列表中，单击文件名旁边的![下载](/help/search-social-commerce/assets/download.png "下载")。

   将按照浏览器的正常过程下载文件。

### 删除已完成的报告

1. 在主菜单中，单击&#x200B;**[!UICONTROL Manage]>[!UICONTROL Ads]**。

1. 在数据表上方的工具栏中，单击![下载报表](/help/search-social-commerce/assets/download.png "下载报表") **[!UICONTROL Reports]**。

1. 在[!UICONTROL Grid Reports]对话框的[!UICONTROL Recently Generated]列表中，单击文件名旁边的![删除](/help/search-social-commerce/assets/delete-new.png "删除")。

>[!MORELIKETHIS]
>
>* [[!DNL Baidu] 文本广告设置](ad-settings-baidu-text.md)
>* [[!DNL Google Ads] 扩展的动态搜索广告设置](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] 响应式搜索广告设置](ad-settings-google-rsa.md)
>* [[!DNL Microsoft Advertising] 扩展的动态搜索广告设置](ad-settings-microsoft-dsa.md)
>* [[!DNL Microsoft Advertising] 多媒体广告设置](ad-settings-microsoft-multimedia.md)
>* [[!DNL Microsoft Advertising] 产品广告设置](ad-settings-microsoft-product.md)
>* [[!DNL Microsoft Advertising] 响应式（受众）广告设置](ad-settings-microsoft-responsive.md)
>* [[!DNL Microsoft Advertising] 响应式搜索广告设置](ad-settings-microsoft-rsa.md)
>* [[!DNL Yandex] 文本广告设置](ad-settings-yandex-text.md)
