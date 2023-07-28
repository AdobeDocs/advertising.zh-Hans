---
title: 同步 [!DNL Adobe] 受众
description: 了解如何为您的同步元数据、层次结构数据和独特受众数据 [!DNL Adobe] 受众。
exl-id: 7d4a3c66-5013-412f-8937-d64c336751e3
feature: Search Admin
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# 同步 [!DNL Adobe] 受众

*[!DNL Direct Access]仅限客户端管理者和管理员*

*仅具有Adobe Advertising-Adobe Audience Manager或Adobe Advertising-Adobe Analytics集成的广告商*

您可以允许Search、Social和Commerce拉入所有广告商或代理的元数据、层次结构数据和独特受众数据 [!DNL Adobe] 受众进入 [!UICONTROL Campaigns] > [!UICONTROL Audiences] 视图。 此信息包括以下项的数据：

* Adobe Audience Manager区段

* 发布到Adobe Experience Cloud的Adobe Analytics区段

* 使用Adobe Experience Cloud创建的区段 [!DNL Audience Library]

广告商或代理机构必须执行 [Adobe Experience Platform Identity服务](https://experienceleague.adobe.com/docs/id-service/using/home.html) 并提供其组织ID(以前称为 [!DNL IMS Org ID])。

初始同步大约需要24小时。 之后，数据实时同步，延迟为1到2秒。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Audience Manager Setup]**.

1. 输入广告商的Adobe Experience Cloud帐户的唯一组织ID，然后单击 **[!UICONTROL Submit]**.

   如果您不知道广告商的组织ID，请在 **[!UICONTROL IMS Org ID]** 位于的广告商设置中的字段 [!UICONTROL Admin] > [!UICONTROL Manage Client].

>[!MORELIKETHIS]
>
>* [关于受众](/help/search-social-commerce/campaign-management/campaigns/audience-about.md)
>* [与Adobe Experience Cloud解决方案和服务集成](/help/search-social-commerce/introduction/integrations.md)
