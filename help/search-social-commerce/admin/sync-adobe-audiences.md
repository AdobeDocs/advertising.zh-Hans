---
title: 同步 [!DNL Adobe] 受众
description: 了解如何同步 [!DNL Adobe] 受众的元数据、层次结构数据和独特受众数据。
exl-id: 8b8c3aa0-2aa9-4ad7-a4c0-1b7ba881acd3
feature: Search Admin
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# 同步[!DNL Adobe]受众

仅&#x200B;*[!DNL Direct Access]客户端管理员和管理员*

*仅集成Adobe Advertising-Adobe Audience Manager或Adobe Advertising-Adobe Analytics的广告商*

您可以允许Search、Social和Commerce将广告商或代理机构所有[!DNL Adobe]受众的元数据、层次结构数据和唯一受众数据提取到[!UICONTROL Campaigns] > [!UICONTROL Audiences]视图中。 此信息包括以下项的数据：

* Adobe Audience Manager区段

* 发布到Adobe Experience Cloud的Adobe Analytics区段

* 使用Adobe Experience Cloud [!DNL Audience Library]创建的区段

广告商或代理机构必须实施[Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html)并提供其组织ID（以前称为[!DNL IMS Org ID]），才能符合条件。

初始同步大约需要24小时。 之后，数据实时同步，延迟为1到2秒。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Audience Manager Setup]**。

1. 输入广告商的Adobe Experience Cloud帐户的唯一组织ID，然后单击&#x200B;**[!UICONTROL Submit]**。

   如果您不知道广告商的组织ID，请在[!UICONTROL Admin] > [!UICONTROL Manage Client]处广告商设置的&#x200B;**[!UICONTROL IMS Org ID]**&#x200B;字段中查找它。

>[!MORELIKETHIS]
>
>* [关于受众](/help/search-social-commerce/campaign-management/campaigns/audience-about.md)
>* [与Adobe Experience Cloud解决方案和服务的集成](/help/search-social-commerce/introduction/integrations.md)
