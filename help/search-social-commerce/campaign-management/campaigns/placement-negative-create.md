---
title: 创建负面投放位置
description: 了解如何为 [!DNL Google Ads] 营销活动和广告组创建负面投放位置。
exl-id: 9cc2dd8d-5563-4e02-af8f-6181165494d8
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# 为[!DNL Google Ads]个负面投放位置创建

仅&#x200B;*[!DNL Google Ads]个帐户*

您可以在定位显示网络的营销活动中为[!DNL Google Ads]广告组创建负版面。 负面投放位置是指显示网络中不会触发广告的网站。

>[!NOTE]
>您还可以在[广告组设置](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)和[促销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)中创建和编辑负版面。

>[!TIP]
>若要同时创建多个负面投放位置，请使用[营销活动批量处理工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Negatives]**。

1. 在数据表上方的工具栏中，单击![创建](/help/search-social-commerce/assets/add.png "创建")，然后单击&#x200B;**[!UICONTROL Campaign]**&#x200B;以创建营销活动级别的负面投放位置，或单击&#x200B;**[!UICONTROL Ad Group]**&#x200B;以创建广告组级别的负面投放位置。

1. 选择广告网络、帐户、营销活动和（如果相关）广告组，然后单击&#x200B;**[!UICONTROL Continue]**。

1. 输入负网站URL。

   要指定多个字符串，请用逗号分隔它们，或者在单独的行中输入它们。 有效格式包括：

   * 网站：输入有效的URL，如www.example.com。 请参阅https://support.google.com/google-ads/answer/2454012上“如何添加排除项URL”中允许的格式。

   * 主题、类别或垂直文档。 查看[[!DNL Google Ads] 指南](https://support.google.com/google-ads/editor/answer/30517)和所有垂直的[列表](https://developers.google.com/adwords/api/docs/appendix/verticals)。 示例： `category::Industries > Energy & Utilities > Oil & Gas`。

1. 单击&#x200B;**[!UICONTROL Post]**。

>[!MORELIKETHIS]
>
>* [关于版面](placement-about.md)
>* [管理可出价投放](placement-manage.md)
>* [更改版面和负版面的状态](placement-status-edit.md)
