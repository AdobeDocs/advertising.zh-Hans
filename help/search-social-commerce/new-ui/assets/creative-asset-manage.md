---
title: 查看和创建创意资产
description: 了解如何为 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 帐户级别的资产库查看和创建可重用的图像、视频和文本资产。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47301d06bc2a06c2601107abd988e787114e36bb
workflow-type: tm+mt
source-wordcount: 492
ht-degree: 0%

---


# 查看和创建创意资产

*仅用于[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户*

在[!UICONTROL Assets] > [!UICONTROL Creatives]中，您可以在[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户级别的资产库中查看所有可重用的图像、视频和（仅适用于[!DNL Google Ads]）文本资产。 该列表在启用了[!DNL AI Max]的营销活动中包括[!DNL Google Ads]广告组的AI生成的资源。

您可以为广告网络帐户手动创建新资产，并将其上传到广告网络。 <!-- Verify if you can use the AI-generated ones -->您可以将任何上传的资源用于效果最佳的营销活动。

您还可以从关联广告组中移除AI生成的文本资产。

## 查看您的创意资源

1. 在主菜单中，单击&#x200B;**[!UICONTROL Assets]>[!UICONTROL Creatives]**。

1. 在工具栏中，选择广告网络和帐户。

   默认情况下将打开[!UICONTROL Image]选项卡。

1. &lt;（可选）单击&#x200B;**[!UICONTROL Video]**&#x200B;和&#x200B;**[!UICONTROL Text]**&#x200B;选项卡以查看具有这些格式的资源。

1. （可选）按任何可用条件筛选任何选项卡。

## 创建和上传资源

1. 在主菜单中，单击&#x200B;**[!UICONTROL Assets]>[!UICONTROL Creatives]**。

1. 在工具栏中，选择广告网络和帐户。

1. 单击&#x200B;**[!UICONTROL Upload Creatives]**。

1. 选择&#x200B;**[!UICONTROL Asset Type]**。

1. 上传或输入资源：

   * 对于图像资产：

     1. 单击&#x200B;**[!UICONTROL +]**&#x200B;并从设备或网络中选择图像。

        每个图像最大可以为10 MB。 一次最多可以上传200 MB的图像。

     1. 对于每个图像：

        1. 选择纵横比。

        1. 根据需要拖动并放置裁切框以选择图像的可查看部分，并在可能的情况下调整图像的可查看部分的大小。

        1. （可选）选择其他纵横比，并根据需要为每个选定的纵横比重新定位和调整图像大小。

           为每个选定的纵横比创建一个资源。

        1. 单击&#x200B;**[!UICONTROL Proceed]**。

   * 对于视频资源，请输入长度至少为10秒的[!DNL YouTube]视频的URL。 要添加其他视频资产，请单击&#x200B;**[!UICONTROL + Add video]**&#x200B;并输入其他URL。

     一次最多可以发布10个视频URL。

   * （仅限[!DNL Google Ads]帐户）对于文本资源，请输入文本字符串。 要添加其他文本资源，请单击&#x200B;**[!UICONTROL + Add text]**&#x200B;并输入其他文本字符串。

     每个文本资源最多可包含1000个字符。 一次最多可以上传10个文本资产。

     您可以稍后将文本资产用于所选的任何广告元素（例如标题或简短描述），前提是它们符合该广告元素的字符限制。

1. 单击&#x200B;**[!UICONTROL Upload]**。

## 删除AI生成的创意资源<!-- AI-generated ones also, or any? -->

<!-- Possible in bulksheets, too?  What about manual creation? -->

在启用了[!DNL AI Max]的营销活动中，为广告组自动生成&#x200B;*[!DNL Google Ads]个资源*

已删除的文本资产将不再提供，但性能数据仍然在报表中可用。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Assets]>[!UICONTROL Creatives]**。

1. 在工具栏中，选择广告网络和帐户。

   默认情况下将打开[!UICONTROL Image]选项卡。

1. &lt;（可选）单击&#x200B;**[!UICONTROL Video]**&#x200B;和&#x200B;**[!UICONTROL Text]**&#x200B;选项卡以查看具有这些格式的资源。

1. &lt;根据需要筛选资源。

   启用了[!DNL AI Max]的营销活动中由[!DNL Google Ads]广告组人工智能生成的资源具有[!UICONTROL Source]类型“[!UICONTROL Automatically Created]”。

1. 选中每个要从其广告组中移除的资源旁边的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL Remove]**。

1. &#x200B;<!-- VERIFY -->在确认消息中，单击&#x200B;**[!UICONTROL Remove]**。

>[!MORELIKETHIS]
>
>* [[!DNL Google Ads] 营销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [[!DNL Microsoft Advertising] 营销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
