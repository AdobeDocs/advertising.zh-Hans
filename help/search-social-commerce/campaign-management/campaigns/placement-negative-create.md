---
title: 创建负面投放位置
description: 了解如何为创建负面投放 [!DNL Google Ads] 营销活动和广告组。
exl-id: 8bddfc12-de95-46c3-aa2d-bcce2a5e0de9
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---

# 为创建 [!DNL Google Ads] 负面投放位置

*[!DNL Google Ads]仅限帐户*

您可以为创建负版面 [!DNL Google Ads] 以显示网络为目标的营销活动中的广告组。 负面投放位置是指显示网络中不会触发广告的网站。

>[!NOTE]
>您还可以在以下位置创建和编辑负版面： [广告组设置](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) 和 [campaign设置](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

>[!TIP]
>要一次创建多个负面投放位置，请使用 [营销活动批量处理工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Negatives]**.

1. 在数据表上方的工具栏中，单击 ![创建](/help/search-social-commerce/assets/add.png "创建")，然后单击 **[!UICONTROL Campaign]** 创建营销活动级别的负面投放位置或 **[!UICONTROL Ad Group]** 创建广告组级别的负版面。

1. 选择广告网络、帐户、营销活动和（如果相关）广告组，然后单击 **[!UICONTROL Continue]**.

1. 输入负网站URL。

   要指定多个字符串，请用逗号分隔它们，或者在单独的行中输入它们。 有效格式包括：

   * 网站：输入有效的URL，如www.example.com。 请参阅https://support.google.com/google-ads/answer/2454012上“如何添加排除项URL”中允许的格式。

   * 主题、类别或垂直文档。 请参阅 [[!DNL Google Ads] 准则](https://support.google.com/google-ads/editor/answer/30517) 和 [所有垂直的列表](https://developers.google.com/adwords/api/docs/appendix/verticals). 示例： `category::Industries > Energy & Utilities > Oil & Gas`.

1. 单击 **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [关于版面](placement-about.md)
>* [管理可竞价投放](placement-manage.md)
>* [更改投放位置和负面投放位置的状态](placement-status-edit.md)
