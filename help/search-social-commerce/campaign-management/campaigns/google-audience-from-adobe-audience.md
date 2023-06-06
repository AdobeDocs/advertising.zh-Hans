---
title: 创建 [!DNL Google Ads] 客户匹配受众来自 [!DNL Adobe] 受众
description: 了解如何创建 [!DNL Google Ads] 客户与您现有Adobe Analytics受众和Audience Manager受众中的受众相匹配。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# 创建 [!DNL Google Ads] 客户匹配Adobe Analytics受众和Audience Manager受众

*[!DNL Google Ads]仅符合客户匹配条件的客户*

*仅具有AdobeAdvertising-Adobe Audience Manager或AdobeAdvertising-Adobe Analytics集成的广告商*

选择加入的广告商可以创建 [!DNL Google Ads] 客户使用来自的用户ID匹配受众) [!DNL Analytics] 与Adobe Experience Cloud共享的区段，以及b)将Search、Social和Commerce作为目标的Audience Manager区段，包括 [!DNL Analytics] 发布到Adobe Experience Cloud的区段和使用Adobe Experience Cloud受众库创建的区段。 搜索、Social和Commerce会自动推送 [!DNL Google] 跟踪URL回到 [!DNL Analytics] 或Audience Manager区段，以便 [!DNL Google] 可以跟踪受众。

每个 [!DNL Adobe] 受众只能用于一个 [!DNL Google] 受众。

每个新 [!DNL Google] 受众具有与原始受众相同的名称 [!DNL Adobe] 受众。 [!DNL Google] 确定目标受众必须有多大。

>[!TIP]
>
>对于实时分段，请使用Audience Manager创建的受众。 在中创建的区段 [!DNL Analytics] 并且同步到Adobe Experience Cloud的用户数可能会更少，因为它们每天才同步；只有在第二天之前，符合区段条件的冲浪者才会包含在区段中。 区段自 [!DNL Analytics] 具有数据源“报告包 — ”。

>[!NOTE]
>
>Search、Social和Commerce不会存储来自您的的任何客户数据 [!DNL Adobe] 用于创建或编辑 [!DNL Google] 受众。

1. 根据需要完成先决条件：

   1. （创建用户ID再营销列表受众） [!DNL Adobe] 管理员用户或帐户管理员必须选择广告商级别的设置以启用客户匹配受众。 设置因具有Audience Manager的广告商和具有 [!DNL Analytics] 仅此而已。

   1. 实施 [Adobe Experience Platform Identity服务](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en) 版本2.0或更高版本。

   1. 在广告商的网页上尽可能高地部署以下标记，应从中跟踪受众

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      位置 `Advertising_Cloud_UserID` 是分配给广告商的唯一用户ID。 示例：  `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. （如果尚未完成）授权用户必须将广告商帐户配置为 [在Adobe Experience Cloud中与广告商的组织帐户同步](/help/search-social-commerce/admin/sync-adobe-audiences.md).

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

      广告商的 [!DNL Google Ads] 帐户必须 [符合自定义匹配的条件](https://support.google.com/adspolicy/answer/6299717) 并选择加入 [用户ID再营销](https://support.google.com/google-ads/answer/9199250).

   1. 选中该复选框以表示您同意 [!DNL Adobe] 和广告网络隐私政策。

   1. 指定数量 **[!UICONTROL Membership Days]**，即用户的Cookie在受众中保留的天数。

      使用您希望广告与用户相关的时间长度。 再营销列表的最长持续时间为540天。 客户列表没有最长的持续时间；要指示Cookie永不过期，请输入10000。

   1. 单击 **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] 处理该文件可能需要24小时。
>
>* 参见 [[!DNL Google Ads] 有关客户匹配的工作方式和限制的文档](https://support.google.com/displayvideo/answer/9539301).


>[!MORELIKETHIS]
>
>* [关于受众](audience-about.md)
>* [创建 [!DNL Google Ads] Adobe Campaign电子邮件列表中的客户匹配受众](google-audience-from-campaign-email-list.md)
>* [使用客户数据列表管理客户匹配受众](audience-from-customer-data-list.md)
>* [管理动态再营销受众](audience-dynamic-remarketing-manage.md)

