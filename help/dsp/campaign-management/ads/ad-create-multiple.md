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

您可以通过上传指向在第三方广告服务器上托管的创意资产的标记，一次最多创建500个第三方广告。 您可以包含广告的跟踪像素。<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

您可以使用提供的模板上传[!DNL DoubleClick]和[!DNL Flashtalking]标记工作表或手动填充的文件。

>[!TIP]
>
> 最佳实践是使用通过HTTPS安全地提供的第三方广告。 使用HTTPS提供的URL以“https”开头。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 单击要包含广告的营销活动的名称。

1. 在数据表上方，单击&#x200B;**[!UICONTROL Create]**。 在菜单的广告类型部分中，单击&#x200B;**[!UICONTROL Bulk upload ads]**。

1. 选择承载广告的广告服务器： *[!UICONTROL DoubleClick]*、*[!UICONTROL Flashtalking]*&#x200B;或&#x200B;*[!UICONTROL Other]*。

1. （[!DNL DoubleClick]和[!DNL Flashtalking]广告）选择要用于每个视频资源和每个显示资源的标记类型。 可用选项因广告服务器而异。

1. （除[!DNL DoubleClick]和[!DNL Flashtalking]之外的所有广告服务器上的广告）单击&#x200B;**[!UICONTROL Download this template]**&#x200B;以下载[!DNL Microsoft Excel]电子表格(XLSX)格式的模板，您可以使用该模板填充广告数据并在本地保存。 所需的列包括[!UICONTROL Ad Name]、[!UICONTROL VAST/VPAID URL or Ad Tag]和[!UICONTROL Ad Types]。

1. 单击&#x200B;**[!UICONTROL Upload]**&#x200B;并从设备或网络中选择一个.xlsx或.xls格式的文件。

   对于[!DNL DoubleClick]和[!DNL Flashtalking]广告，请从广告服务器上传未编辑的标记表。 对于其他广告服务器，请使用在步骤3中下载的模板。

1. 上传完成后，单击&#x200B;**[!UICONTROL Start Building Ads]**。

1. 查看每个广告的详细信息和状态：

   1. （使用[!DNL Google]或[!DNL Flashtalking]标记的通用视频广告）单击&#x200B;**[!UICONTROL Ad Type]**&#x200B;字段并选择&#x200B;**[!UICONTROL Universal Video]**。

   1. （通用视频广告）对于每个新广告，单击![编辑](/help/dsp/assets/edit.png)，选择[适用的视频格式](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)，然后单击&#x200B;**保存**。

   1. 查看每个广告的状态，该状态基于对上传标记的验证检查。

   1. （可选）为每个广告执行以下任一操作：

      * 要预览广告，请单击广告行中的![播放](/help/dsp/assets/play.png)。

      * 要编辑广告详细信息，请单击![编辑](/help/dsp/assets/edit.png)，编辑详细信息，然后单击&#x200B;**保存**。

      * 要删除广告，请单击广告行中的&#x200B;**[!UICONTROL X]**。

1. 单击&#x200B;**[!UICONTROL Create *N *个广告]**。

1. 执行以下操作之一：

   * 单击&#x200B;**[!UICONTROL Done]**。

   * （如果广告被拒绝；可选）要编辑广告记录并重新提交广告以供审阅，请执行以下操作：

      1. 单击广告名称。

      1. 编辑广告设置。

      1. 单击&#x200B;**[!UICONTROL Save & submit for review]**。

>[!NOTE]
>
>通用视频广告只能附加到通用视频投放位置。

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [广告规范](ad-specs.md)
>* [创建单个Ad](ad-create.md)
>* [视频：如何批量上传第三方广告标记](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html?lang=zh-Hans)
>* 有关通用视频的[常见问题解答](/help/dsp/campaign-management/faq-universal-video.md)
