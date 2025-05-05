---
title: 创建来自 [!DNL Adobe] 受众的 [!DNL Google Ads] 客户匹配受众
description: 了解如何从现有Adobe Analytics和Audience Manager受众创建 [!DNL Google Ads] 客户匹配受众。
exl-id: 7de95ebb-24b0-459f-83c0-7b85b0c0576d
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# 从Adobe Analytics和Audience Manager受众中创建[!DNL Google Ads]个客户匹配受众

仅符合客户匹配条件的&#x200B;*[!DNL Google Ads]帐户*

*仅具有Adobe Advertising-Adobe Audience Manager或Adobe Advertising-Adobe Analytics集成的广告商*

选择加入的广告商可以使用以下用户ID创建[!DNL Google Ads]个客户匹配受众：a) [!DNL Analytics]与Adobe Experience Cloud共享的区段，以及b)将Search、Social和Commerce作为目标的Audience Manager区段，包括发布到Adobe Experience Cloud的[!DNL Analytics]区段和使用Adobe Experience Cloud受众库创建的区段。 Search、Social和Commerce自动将[!DNL Google]跟踪URL推送回每个[!DNL Analytics]或Audience Manager区段，以便[!DNL Google]可以跟踪受众。

每个[!DNL Adobe]受众只能用于一个[!DNL Google]受众。

每个新[!DNL Google]受众与原始[!DNL Adobe]受众具有相同的名称。 [!DNL Google]确定受众必须有多大才能成为目标。

>[!TIP]
>
>对于实时分段，请使用Audience Manager创建的受众。 在[!DNL Analytics]中创建并同步到Adobe Experience Cloud的区段可能具有更少的人口，因为它们仅每天同步；在第二天之前，符合区段条件的冲浪者可能未包含在区段中。 来自[!DNL Analytics]的区段的数据源为“报告包 — ”。

>[!NOTE]
>
>Search、Social和Commerce不存储用于创建或编辑[!DNL Google]受众的[!DNL Adobe]区段中的任何客户数据。

1. 根据需要完成先决条件：

   1. （要创建用户ID再营销列表受众）[!DNL Adobe]管理员用户或帐户管理员必须选择广告商级别的设置以启用客户匹配受众。

   1. 实施[Adobe Experience Platform Identity服务](https://experienceleague.adobe.com/docs/id-service/using/home.html)版本2.0或更高版本。

   1. 在广告商的网页上尽可能高地部署以下标记，应从中跟踪受众

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      其中`Advertising_Cloud_UserID`是分配给广告商的唯一数字用户ID。

      示例： `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. （如果尚未完成）授权用户必须将广告商帐户配置为与Adobe Experience Cloud[&#128279;](/help/search-social-commerce/admin/sync-adobe-audiences.md)中的广告商组织帐户同步。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**。

1. 在数据表上方的工具栏中，单击![创建](/help/search-social-commerce/assets/add.png "创建")。

1. 选择广告网络和帐户名称，然后单击&#x200B;**[!UICONTROL Continue]**。

1. 指定受众信息：

   1. 在&#x200B;**[!UICONTROL Data Source]**&#x200B;菜单中选择&#x200B;**[!UICONTROL Adobe Audience]**。

   1. 选择[!DNL Google]受众所基于的[!UICONTROL Adobe Audience]。

      >[!NOTE]
      >
      >已用于其他[!DNL Google]受众的[!DNL Adobe]受众不可用。

      您可以选择搜索包含至少三个字符的特定文本字符串的受众。 对于任何匹配的受众，单击&#x200B;**[!UICONTROL Include]**&#x200B;以将其选定。

      如果您选择多个[!DNL Adobe]受众，则会为每个受众创建单独的[!DNL Google]受众。

   1. 选择要创建的&#x200B;**[!UICONTROL Audience Type]**： **[!UICONTROL Customer List_User ID]**。

      广告商的[!DNL Google Ads]帐户必须[符合自定义匹配条件](https://support.google.com/adspolicy/answer/6299717)并选择加入[用户ID再营销](https://support.google.com/google-ads/answer/9199250)。

   1. 选中此复选框以表示您同意[!DNL Adobe]和广告网络隐私政策的条款。

   1. 指定&#x200B;**[!UICONTROL Membership Days]**&#x200B;的数量，即用户Cookie在受众中保留的天数。

      使用您希望广告与用户相关的时间长度。 再营销列表的最长持续时间为540天。 客户列表没有最长的持续时间；要指示Cookie永不过期，请输入10000。

   1. 单击&#x200B;**[!UICONTROL Post]**。

>[!NOTE]
>
>* [!DNL Google]可能需要24小时来处理该文件。
>
>* 请参阅[[!DNL Google Ads] 文档，了解客户匹配的工作方式和限制](https://support.google.com/displayvideo/answer/9539301)。

>[!MORELIKETHIS]
>
>* [关于受众](audience-about.md)
>* [从Adobe Campaign电子邮件列表创建 [!DNL Google Ads] 客户匹配受众](google-audience-from-campaign-email-list.md)
>* [使用客户数据列表管理客户匹配受众](audience-from-customer-data-list.md)
>* [管理动态再营销受众](audience-dynamic-remarketing-manage.md)
