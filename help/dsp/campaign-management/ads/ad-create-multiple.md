---
title: 创建多个第三方广告
description: 了解如何同时创建多个第三方广告。
feature: DSP Ads
exl-id: be7c1cc4-3c17-4e37-aae7-c8601d2222a0
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# 创建多个第三方广告

您可以通过上传指向在第三方广告服务器上托管的创意资产的标记，一次最多创建500个第三方广告。 您可以为广告包含跟踪像素。<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

您可以上传 [!DNL DoubleClick] 和 [!DNL Flashtalking] 标签工作表或使用提供的模板手动填充的文件。

>[!TIP]
>
> 最佳实践是使用通过HTTPS安全地提供的第三方广告。 使用HTTPS提供的URL以“https”开头。

1. 在主菜单中，单击 **[!UICONTROL Campaigns]**.

1. 单击要包含广告的营销活动的名称。

1. 在数据表的上方，单击 **[!UICONTROL Create]**. 在菜单的广告类型部分中，单击 **[!UICONTROL Bulk upload ads]**.

1. 选择广告所在的广告服务器： *[!UICONTROL DoubleClick]*， *[!UICONTROL Flashtalking]*，或 *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] 和 [!DNL Flashtalking] 广告)选择要用于每个视频资源和每个显示资源的标记类型。 可用选项因广告服务器而异。

1. (所有广告服务器上的广告，除 [!DNL DoubleClick] 和 [!DNL Flashtalking])单击 **[!UICONTROL Download this template]** 在中下载模板 [!DNL Microsoft Excel] 电子表格(XLSX)格式，可填充广告数据并在本地保存。 必需的列包括 [!UICONTROL Ad Name]， [!UICONTROL VAST/VPAID URL or Ad Tag]、和 [!UICONTROL Ad Types].

1. 单击 **[!UICONTROL Upload]** 并从设备或网络中选择一个.xlsx或.xls格式的文件。

   对象 [!DNL DoubleClick] 和 [!DNL Flashtalking] 广告，从广告服务器上传未编辑的标记表。 对于其他广告服务器，请使用在步骤3中下载的模板。

1. 上传完成后，单击 **[!UICONTROL Start Building Ads]**.

1. 查看每个广告的详细信息和状态：

   1. (使用的通用视频广告 [!DNL Google] 或 [!DNL Flashtalking] 标签)单击 **[!UICONTROL Ad Type]** 字段并选择 **[!UICONTROL Universal Video]**.

   1. （通用视频广告）对于每个新广告，单击 ![编辑](/help/dsp/assets/edit.png)，选择 [适用的视频格式](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)，然后单击 **保存**.

   1. 查看每个广告的状态，该状态基于对上传标记的验证检查。

   1. （可选）为每个广告执行以下任一操作：

      * 要预览广告，请单击 ![play](/help/dsp/assets/play.png) 在广告行中。

      * 要编辑广告详细信息，请单击 ![编辑](/help/dsp/assets/edit.png)，编辑详细信息，然后单击 **保存**.

      * 要删除广告，请单击 **[!UICONTROL X]** 在广告行中。

1. 单击 **[!UICONTROL Create *N *广告]**.

1. 执行以下操作之一：

   * 单击 **[!UICONTROL Done]**.

   * （如果广告被拒绝；可选）要编辑广告记录并重新提交广告以供审阅，请执行以下操作：

      1. 单击广告名称。

      1. 编辑广告设置。

      1. 单击 **[!UICONTROL Save & submit for review]**.

>[!NOTE]
>
>通用视频广告只能附加到通用视频投放位置。

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [广告规范](ad-specs.md)
>* [创建单个广告](ad-create.md)
>* [视频：如何批量上传第三方广告标记](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)
>* [关于通用视频的常见问题解答](/help/dsp/campaign-management/faq-universal-video.md)
