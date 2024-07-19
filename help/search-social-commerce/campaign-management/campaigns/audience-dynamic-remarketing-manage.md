---
title: 管理 [!DNL Microsoft Advertising] 动态再营销受众
description: 了解如何创建和管理 [!DNL Microsoft Advertising] 动态二次营销受众。
exl-id: 52faab75-e723-4e59-aac6-b4d0c4c1cf60
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# 管理[!DNL Microsoft Advertising]动态再营销受众

仅&#x200B;*[!DNL Microsoft Advertising]个帐户*

在网页上使用搜索引擎的JavaScript转化和受众跟踪标记时，您可以创建[!DNL Microsoft Advertising]动态再营销受众。 每个受众都是使用指定的标记创建的，该标记包含在用户构成受众的网页中。 您可以使用同一跟踪标记创建多个受众。 您还可以更改现有受众的名称和数据源，或删除现有受众。

动态二次营销受众具有受众类型“[!UICONTROL Dynamic Remarketing] \&lt;访客类型\>”（例如“动态二次营销过去的购买者”）。

有关动态再营销以及如何实施必需的JavaScript标记的详细信息，请参阅[[!DNL Microsoft Advertising] 有关动态再营销的文档](https://help.ads.microsoft.com/#apex/ads/en/56910)。

## 创建动态二次营销受众

>[!NOTE]
>
>对于[!DNL Microsoft Advertising]帐户，JavaScript标记必须包含[产品ID和页面类型参数](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85)。

1. 识别将从中创建受众的网页中包含的[!DNL Microsoft Advertising]通用事件跟踪(UET)标记的名称。

   在后续步骤中，您将需要标记名称。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**。

1. 在数据表上方的工具栏中，单击![创建](/help/search-social-commerce/assets/add.png "创建")。

1. 选择广告网络和帐户名称，然后单击&#x200B;**[!UICONTROL Continue]**。

1. 指定受众信息：

   1. 在&#x200B;**[!UICONTROL Data Source]**&#x200B;菜单中选择&#x200B;**[!UICONTROL Dynamic Remarketing List]**。

   1. 输入&#x200B;**[!UICONTROL Audience Name]**。

   1. 从搜索引擎帐户的所有可用标记列表中，选择包含在其用户组成受众的网页中的[!DNL Microsoft Advertising] UET标记的名称。

   1. 选择受众的访客类型，该类型基于相关网页上的访客操作： *[!UICONTROL General Visitors]*、*[!UICONTROL Product Searchers]*、*[!UICONTROL Product Viewers]*、*[!UICONTROL Past Buyers]*&#x200B;或&#x200B;*[!UICONTROL Shopping Cart Abandoners]*。

   1. 指定&#x200B;**[!UICONTROL Membership Days]**&#x200B;的数量，即用户Cookie在受众中保留的天数。 值的范围可以从一(1)到180。

      使用您希望广告与用户相关的时间长度。

1. 单击&#x200B;**[!UICONTROL Post]**。

>[!NOTE]
>
>您的[!DNL Microsoft Advertising]动态再营销列表只要包含至少300名用户，即符合定位条件。

## 编辑动态二次营销受众

您可以更改[!DNL Microsoft Advertising]动态再营销受众的名称和数据源。 您无法编辑[!UICONTROL Membership Days]设置的值。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**。

1. 选中要编辑的受众旁边的复选框。

1. 在数据表上方的工具栏中，单击![编辑](/help/search-social-commerce/assets/edit.png "编辑")。

1. 编辑受众信息：

   1. 在&#x200B;**[!UICONTROL Data Source]**&#x200B;部分中，单击![编辑](/help/search-social-commerce/assets/edit.png "编辑")。

   1. （可选）更改&#x200B;**[!UICONTROL Audience Name]**。

   1. （可选）从广告网络帐户的所有可用标记列表中，更改包含在其用户组成受众的网页中的[!DNL Microsoft Advertising] UET标记的名称。

   1. （可选）更改受众的访客类型，该类型基于相关网页上的访客操作： *[!UICONTROL General Visitors]*、*[!UICONTROL Product Searchers]*、*[!UICONTROL Product Viewers]*、*[!UICONTROL Past Buyers]*&#x200B;或&#x200B;*[!UICONTROL Shopping Cart Abandoners]*。

   1. 单击&#x200B;**[!UICONTROL Post]**。

## 删除动态二次营销受众

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**。

1. （可选）筛选列表以包含特定受众。

1. 选中要删除的每个受众旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Delete]**。

>[!MORELIKETHIS]
>
>* [关于受众](audience-about.md)
>* [创建来自 [!DNL Adobe] 受众的 [!DNL Google Ads] 客户匹配受众](google-audience-from-adobe-audience.md)
>* [从Adobe Campaign电子邮件列表创建 [!DNL Google Ads] 客户匹配受众](google-audience-from-campaign-email-list.md)
>* [使用客户数据列表管理客户匹配受众](audience-from-customer-data-list.md)
