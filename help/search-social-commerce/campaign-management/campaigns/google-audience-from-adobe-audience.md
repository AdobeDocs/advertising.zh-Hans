---
title: 创建 [!DNL Google Ads] 客户匹配受众来自 [!DNL Adobe] 受众
description: 了解如何创建 [!DNL Google Ads] 客户匹配来自您现有Adobe Analytics和Audience Manager受众的受众。
exl-id: 17cf0729-bc13-4ec3-918e-039ecdc91a41
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 创建 [!DNL Google Ads] 客户匹配Adobe Analytics受众和Audience Manager受众

*[!DNL Google Ads]仅符合客户匹配条件的客户*

*仅具有Adobe Advertising-Adobe Audience Manager或Adobe Advertising-Adobe Analytics集成的广告商*

选择加入的广告商可以创建 [!DNL Google Ads] 客户使用来自的用户ID匹配受众) [!DNL Analytics] 与Adobe Experience Cloud共享的区段，以及b)Audience Manager将“搜索”、“社交”和“商务”作为目标的区段，包括 [!DNL Analytics] 发布到Adobe Experience Cloud的区段和使用Adobe Experience Cloud受众库创建的区段。 搜索、Social和Commerce会自动推送 [!DNL Google] 跟踪URL回到 [!DNL Analytics] 或Audience Manager区段，以便 [!DNL Google] 可以跟踪受众。

每个 [!DNL Adobe] 受众只能用于一个 [!DNL Google] 受众。

每个新 [!DNL Google] 受众与原始受众具有相同的名称 [!DNL Adobe] 受众。 [!DNL Google] 确定目标受众必须有多大。

>[!TIP]
>
>对于实时分段，请使用Audience Manager创建的受众。 在中创建的区段 [!DNL Analytics] 且同步到Adobe Experience Cloud的用户数量可能会减少，因为它们每天都只会进行同步；在第二天之前，符合区段条件的冲浪者可能不会包含在区段中。 区段来源 [!DNL Analytics] 具有数据源“报告包 — ”。

>[!NOTE]
>
>Search、Social和Commerce不会存储您网站上的 [!DNL Adobe] 用于创建或编辑 [!DNL Google] 受众。

1. 根据需要完成先决条件：

   1. （创建用户ID再营销列表受众） [!DNL Adobe] 管理员用户或帐户管理员必须选择广告商级别的设置以启用客户匹配受众。 设置因具有Audience Manager的广告商和具有 [!DNL Analytics] 仅限。

   1. 实施 [Adobe Experience Platform Identity服务](https://experienceleague.adobe.com/docs/id-service/using/home.html) 版本2.0或更高版本。

   1. 在广告商的网页上尽可能高地部署以下标记，应从中跟踪受众

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      位置 `Advertising_Cloud_UserID` 是分配给广告商的唯一用户ID。 示例：  `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. （如果尚未完成）授权用户必须将广告商帐户配置为 [与Adobe Experience Cloud中广告商的组织帐户同步](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. 在数据表上方的工具栏中，单击 ![创建](/help/search-social-commerce/assets/add.png "创建").

1. 选择广告网络和帐户名称，然后单击 **[!UICONTROL Continue]**.

1. 指定受众信息：

   1. 在 **[!UICONTROL Data Source]** 菜单，选择 **[!UICONTROL Adobe Audience]**.

   1. 选择 [!UICONTROL Adobe Audience] 作为基础 [!DNL Google] 受众。

      >[!NOTE]
      >
      >[!DNL Adobe] 已用于其他受众的受众 [!DNL Google] 受众不可用。

      您可以选择搜索包含至少三个字符的特定文本字符串的受众。 对于任何匹配的受众，单击 **[!UICONTROL Include]** 以选择它。

      如果您选择多个 [!DNL Adobe] 受众，然后是单独的 [!DNL Google] 将为每个创建受众。

   1. 选择 **[!UICONTROL Audience Type]** 要创建： **[!UICONTROL Customer List_User ID]**.

      广告商的 [!DNL Google Ads] 帐户必须 [符合自定义匹配条件](https://support.google.com/adspolicy/answer/6299717) 并选择加入 [用户ID再营销](https://support.google.com/google-ads/answer/9199250).

   1. 选中该复选框以表示您同意 [!DNL Adobe] 和广告网络隐私政策。

   1. 指定数量 **[!UICONTROL Membership Days]**，即用户的Cookie在受众中保留的天数。

      使用您希望广告与用户相关的时间长度。 再营销列表的最长持续时间为540天。 客户列表没有最长的持续时间；要指示Cookie永不过期，请输入10000。

   1. 单击 **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] 处理该文件可能需要24小时。
>
>* 请参阅 [[!DNL Google Ads] 有关客户匹配的工作方式和限制的文档](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [关于受众](audience-about.md)
>* [创建 [!DNL Google Ads] Adobe Campaign电子邮件列表中的客户匹配受众](google-audience-from-campaign-email-list.md)
>* [使用客户数据列表管理客户匹配受众](audience-from-customer-data-list.md)
>* [管理动态二次营销受众](audience-dynamic-remarketing-manage.md)
