---
title: 管理 [!DNL Microsoft Advertising] 动态二次营销受众
description: 了解如何创建和管理 [!DNL Microsoft Advertising] 动态二次营销受众。
exl-id: 52faab75-e723-4e59-aac6-b4d0c4c1cf60
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# 管理 [!DNL Microsoft Advertising] 动态二次营销受众

*[!DNL Microsoft Advertising]仅限帐户*

您可以创建 [!DNL Microsoft Advertising] 在网页上使用搜索引擎的JavaScript转化和受众跟踪标记时，动态二次营销受众。 每个受众都是使用指定的标记创建的，该标记包含在用户构成受众的网页中。 您可以使用同一跟踪标记创建多个受众。 您还可以更改现有受众的名称和数据源，或删除现有受众。

动态二次营销受众具有受众类型»[!UICONTROL Dynamic Remarketing] \&lt;visitor type=&quot;&quot;>”（例如“动态再营销过去的购买者”）。

有关动态再营销以及如何实施所需JavaScript标记的详细信息，请参阅 [[!DNL Microsoft Advertising] 关于动态再营销的文档](https://help.ads.microsoft.com/#apex/ads/en/56910).

## 创建动态二次营销受众

>[!NOTE]
>
>对象 [!DNL Microsoft Advertising] 帐户，JavaScript标记必须包含 [产品ID和页面类型参数](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85).

1. 标识的名称 [!DNL Microsoft Advertising] 通用事件跟踪(UET)标记，包含在将从中创建受众的网页中。

   在后续步骤中，您将需要标记名称。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. 在数据表上方的工具栏中，单击 ![创建](/help/search-social-commerce/assets/add.png "创建").

1. 选择广告网络和帐户名称，然后单击 **[!UICONTROL Continue]**.

1. 指定受众信息：

   1. 在 **[!UICONTROL Data Source]** 菜单，选择 **[!UICONTROL Dynamic Remarketing List]**.

   1. 输入 **[!UICONTROL Audience Name]**.

   1. 从搜索引擎帐户的所有可用标记列表中，选择 [!DNL Microsoft Advertising] 包含在其用户构成受众的网页中的UET标记。

   1. 选择受众的访客类型，该类型基于相关网页上的访客操作： *[!UICONTROL General Visitors]*， *[!UICONTROL Product Searchers]*， *[!UICONTROL Product Viewers]*， *[!UICONTROL Past Buyers]*，或 *[!UICONTROL Shopping Cart Abandoners]*.

   1. 指定数量 **[!UICONTROL Membership Days]**，即用户的Cookie在受众中保留的天数。 值的范围可以从一(1)到180。

      使用您希望广告与用户相关的时间长度。

1. 单击 **[!UICONTROL Post]**.

>[!NOTE]
>
>您的 [!DNL Microsoft Advertising] 一旦动态二次营销列表包含至少300个用户，则符合定位条件。

## 编辑动态二次营销受众

您可以更改名称和数据源 [!DNL Microsoft Advertising] 动态二次营销受众。 您无法编辑以下项的值： [!UICONTROL Membership Days] 设置。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. 选中要编辑的受众旁边的复选框。

1. 在数据表上方的工具栏中，单击 ![编辑](/help/search-social-commerce/assets/edit.png "编辑").

1. 编辑受众信息：

   1. 在 **[!UICONTROL Data Source]** 部分，单击 ![编辑](/help/search-social-commerce/assets/edit.png "编辑").

   1. （可选）更改 **[!UICONTROL Audience Name]**.

   1. （可选）从广告网络帐户的所有可用标记列表中，更改 [!DNL Microsoft Advertising] 包含在其用户构成受众的网页中的UET标记。

   1. （可选）更改受众的访客类型，该类型基于相关网页上的访客操作： *[!UICONTROL General Visitors]*， *[!UICONTROL Product Searchers]*， *[!UICONTROL Product Viewers]*， *[!UICONTROL Past Buyers]*，或 *[!UICONTROL Shopping Cart Abandoners]*.

   1. 单击 **[!UICONTROL Post]**.

## 删除动态二次营销受众

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. （可选）筛选列表以包含特定受众。

1. 选中要删除的每个受众旁边的复选框。

   有关选择多行的提示，请参阅&quot;[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)“

1. 在确认消息中，单击 **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [关于受众](audience-about.md)
>* [创建 [!DNL Google Ads] 客户匹配受众来自 [!DNL Adobe] 受众](google-audience-from-adobe-audience.md)
>* [创建 [!DNL Google Ads] Adobe Campaign电子邮件列表中的客户匹配受众](google-audience-from-campaign-email-list.md)
>* [使用客户数据列表管理客户匹配受众](audience-from-customer-data-list.md)
