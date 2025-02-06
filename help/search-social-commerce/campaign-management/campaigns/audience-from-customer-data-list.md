---
title: 使用客户数据列表管理客户匹配受众
description: 了解如何从您的客户数据列表中创建和编辑 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 客户匹配受众。
exl-id: 594a7ee0-4ac9-4970-b53e-d4624fd7b70c
feature: Search Campaign Management
source-git-commit: 46d736c3e14bf407c513c5cb6a153a578aa65121
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# 使用客户数据列表管理[!DNL Google Ads]和[!DNL Microsoft Advertising]客户匹配受众

您可以从客户数据列表中创建[!DNL Google Ads]和[!DNL Microsoft Advertising]客户匹配受众。 您还可以更新任何[!DNL Google Ads]或[!DNL Microsoft Advertising]客户匹配受众，但从[!DNL Adobe]受众创建的[!DNL Google Ads]受众除外。

## 从客户数据列表创建客户匹配受众

符合客户资格的&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户仅匹配*

您可以从从客户关系管理(CRM)系统生成的数据文件中创建[!DNL Google Ads]或[!DNL Microsoft Advertising]基于客户数据的列表。

对于[!DNL Microsoft Advertising]帐户，该文件可以包含电子邮件地址。 对于[!DNL Google Ads]帐户，该文件可以包括电子邮件地址、邮寄地址或电话号码、用户ID或来自您的CRM的移动设备ID。

>[!NOTE]
>
>Search、Social和Commerce不会存储您上传的任何客户数据，也不会存储用于创建或编辑[!DNL Google Ads]或[!DNL Microsoft Advertising]受众的[!DNL Adobe]区段中的客户数据。

1. 以所需格式生成包含客户数据的文件。

   名字、姓氏、电子邮件地址和电话号码必须使用SHA-256算法进行哈希处理。 <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. -->对于[!DNL Google Ads]受众，请参阅有关“[用于上载哈希数据的格式设置准则](https://support.google.com/google-ads/answer/7476159)”的[!DNL Google Ads]文档，以了解允许的联系人信息字段和要求的列表。 对于[!DNL Microsoft Advertising]受众，请参阅[准备客户匹配列表](https://help.ads.microsoft.com/#apex/ads/en/56921)上的[!DNL Microsoft Advertising]文档。 您可以选择下载[!DNL Microsoft Excel]模板以获取联系信息。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**。

1. 在数据表上方的工具栏中，单击![创建](/help/search-social-commerce/assets/add.png "创建")。

1. 选择广告网络和帐户名称，然后单击&#x200B;**[!UICONTROL Continue]**。

1. 指定受众信息：

   1. 在[!UICONTROL Data Source]菜单中选择&#x200B;**[!UICONTROL Customer List]**。

   1. 输入&#x200B;**[!UICONTROL Audience Name]**。

   1. 上传文件：

      1. 选择[!UICONTROL Data Upload Type]： *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*、*[!UICONTROL User IDs]*&#x200B;或&#x200B;*[!UICONTROL Mobile Device IDs]*。

         “用户ID”选项仅适用于已选择加入[用户ID区段](https://support.google.com/google-ads/answer/9199250)的美国[!DNL Google Ads]广告商

      1. （仅限移动设备ID列表）选择&#x200B;**[!UICONTROL OS Type]** （*[!UICONTROL Android™]*&#x200B;或&#x200B;*[!UICONTROL iOS]*），然后输入&#x200B;**[!UICONTROL App ID]**。

         应用程序ID是移动设备操作系统用来允许应用程序连接到Google Play或Apple App Store的唯一标识符：

         * （[!DNL Android™]个应用）[!DNL Google Play]中的[!DNL Android™]包名称，由“`id=<package_name>`”标识。

           例如，在`https://play.google.com/store/apps/details?id=com.example.game`中，包名称为com.example.game。

         * （[!DNL iOS]个应用程序）[!DNL iTunes App Store]中的应用程序ID，由URL末尾的“`<idNNNNNNNNN>`”标识。 [!DNL iOS Developer Console]中也有提供。

           例如，在`https://itunes.apple.com/us/app/id284882215`中，ID是ID284882215。

         您的开发团队有权访问相关平台的[!UICONTROL App ID]。

      1. 在[!UICONTROL Select File]字段中，单击&#x200B;**[!UICONTROL Choose File]**&#x200B;并选择网络或设备上的文件。

      1. 选中此复选框以表示您同意[!DNL Adobe]和广告网络隐私政策的条款。

      1. (广告商创建了在欧洲经济区(EEA)或英国(UK)开展业务的[!DNL Google Ads]受众；可选)如果您已向EEA和英国用户收集同意以将其数据上传用于广告，请选中&#x200B;**[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**&#x200B;旁边的复选框

      [!DNL Google Ads]会忽略未指定同意状态的EEA和英国用户的任何数据。 这可能会导致数据差异和性能问题。

      1. 单击&#x200B;**[!UICONTROL Upload File]**。

   1. 指定&#x200B;**[!UICONTROL Membership Days]**&#x200B;的数量，即用户Cookie在受众中保留的天数。

   使用您希望广告与用户相关的时间长度。 除非您输入值，否则客户列表不会过期。

1. 单击&#x200B;**[!UICONTROL Post]**。

>[!NOTE]
>
>* 广告网络可能需要长达24小时来处理文件。
>* 请参阅[[!DNL Google Ads] 文档，了解客户匹配的工作方式和限制](https://support.google.com/displayvideo/answer/9539301)。

## 使用客户数据列表编辑客户匹配受众

您可以更新任何[!DNL Google Ads]或[!DNL Microsoft Advertising]客户匹配受众，但从[!DNL Adobe]受众创建的[!DNL Google Ads]受众除外。 您可以上传数据，以添加、删除或替换受众的所有现有数据。

该数据必须与原始客户列表（电子邮件地址、邮寄地址、电话号码、用户ID或特定移动操作系统上特定应用程序的移动设备ID）的类型相同。

1. 为现有数据类型以所需格式生成包含客户数据的文件。

名字、姓氏、电子邮件地址和电话号码必须使用SHA-256算法进行哈希处理。 <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. -->对于[!DNL Google Ads]受众，请参阅有关“[用于上载哈希数据的格式设置准则](https://support.google.com/google-ads/answer/7476159)”的[!DNL Google Ads]文档，以了解允许的联系人信息字段和要求的列表。 对于[!DNL Microsoft Advertising]受众，请参阅[准备客户匹配列表](https://help.ads.microsoft.com/#apex/ads/en/56921)上的[!DNL Microsoft Advertising]文档。 您可以选择下载[!DNL Microsoft Excel]模板以获取联系信息。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**。

1. 选中要编辑的受众旁边的复选框。

1. 在数据表上方的工具栏中，单击![编辑](/help/search-social-commerce/assets/edit.png)。

1. 选择操作： *[!UICONTROL Add]* （将上载的数据添加到现有数据，除非现有数据已存在）、*[!UICONTROL Delete]* （从现有数据中删除上载的数据，如果现有数据已存在），或&#x200B;*[!UICONTROL Replace]* （删除所有现有数据并用上载的数据替换）。

1. 上传文件：

   1. 在[!UICONTROL Select File]字段中，单击&#x200B;**[!UICONTROL Choose File]**&#x200B;并选择网络或设备上的文件。

   1. 选中此复选框以表示您同意[!DNL Adobe]和广告网络隐私政策的条款。

   1. 单击&#x200B;**[!UICONTROL Upload File]**。

1. 单击&#x200B;**[!UICONTROL Post]**。

>[!NOTE]
>
>广告网络可能需要一段时间来处理对受众的更新。

>[!MORELIKETHIS]
>
>* [关于受众](audience-about.md)
>* [创建来自 [!DNL Adobe] 受众的 [!DNL Google Ads] 客户匹配受众](google-audience-from-adobe-audience.md)
>* [从Adobe Campaign电子邮件列表创建 [!DNL Google Ads] 客户匹配受众](google-audience-from-campaign-email-list.md)
>* [管理动态再营销受众](audience-dynamic-remarketing-manage.md)
