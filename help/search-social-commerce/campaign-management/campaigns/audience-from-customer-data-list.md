---
title: 使用客户数据列表管理客户匹配受众
description: 了解如何创建和编辑 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 客户从您的客户数据列表中匹配受众。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---

# 管理 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 使用客户数据列表匹配受众

您可以创建 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 客户从您的客户数据列表中匹配受众。 您还可以更新任何 [!DNL Google Ads] 或 [!DNL Microsoft® Advertising] 客户匹配受众，但 [!DNL Google Ads] 受众创建自 [!DNL Adobe] 受众。

## 从客户数据列表创建客户匹配受众

*[!DNL Google Ads]和 [!DNL Microsoft® Advertising] 仅符合客户匹配条件的客户*

您可以创建 [!DNL Google Ads] 或 [!DNL Microsoft® Advertising] 从客户关系管理(CRM)系统生成的数据文件中基于客户数据的列表。

对象 [!DNL Microsoft® Advertising] 帐户，则文件可以包括电子邮件地址。 对象 [!DNL Google Ads] 帐户，则文件可以包括电子邮件地址、邮寄地址或电话号码、用户ID或CRM中的移动设备ID。

>[!NOTE]
>
>Search、Social和Commerce不会存储您上传或来自的任何客户数据 [!DNL Adobe] 用于创建或编辑 [!DNL Google Ads] 或 [!DNL Microsoft® Advertising] 受众。

1. 使用客户数据以所需格式生成文件。

   必须使用SHA-256算法对名字和姓氏、电子邮件地址和电话号码进行哈希处理。 <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> 对象 [!DNL Google Ads] 受众，请参见 [!DNL Google Ads] 有关“”的文档[用于上载哈希数据的格式设置准则](https://support.google.com/google-ads/answer/7476159)”以获取允许的联系信息字段和要求的列表。 对象 [!DNL Microsoft® Advertising] 受众，请参见 [!DNL Microsoft® Advertising] 相关文档 [准备客户匹配列表](https://help.ads.microsoft.com/#apex/ads/en/56921. 您可以选择下载 [!DNL Microsoft® Excel] 联系人信息模板。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. 在数据表上方的工具栏中，单击 ![创建](/help/search-social-commerce/assets/add.png "创建").

1. 选择广告网络和帐户名称，然后单击 **[!UICONTROL Continue]**.

1. 指定受众信息：

   1. 在 [!UICONTROL Data Source] 菜单，选择 **[!UICONTROL Customer List]**.

   1. 输入 **[!UICONTROL Audience Name]**.

   1. 上传文件：

      1. 选择 [!UICONTROL Data Upload Type]： *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*， *[!UICONTROL User IDs]*，或 *[!UICONTROL Mobile Device IDs]*.

         用户ID选项仅适用于 [!DNL Google Ads] 美国选择加入的广告商 [用户标识区段](https://support.google.com/google-ads/answer/9199250)

      1. （仅限移动设备ID列表）选择 **[!UICONTROL OS Type]** (*[!UICONTROL Android™]* 或 *[!UICONTROL iOS]*)，并输入 **[!UICONTROL App ID]**.

         应用程序ID是移动操作系统用来允许应用程序连接到Google Play或Apple App Store的唯一标识符：

         * ([!DNL Android™] 应用程序) [!DNL Android™] 中的包名称 [!DNL Google Play]，由“`id=<package_name>`.”

            例如，在https://play.google.com/store/apps/details?id=com.example.game中，包名称为com.example.game。

         * ([!DNL iOS] 应用程序)中的应用程序ID [!DNL iTunes App Store]，由“`<idNNNNNNNNN>`”进行标记。 它还可在 [!DNL iOS Developer Console].

            例如，在https://itunes.apple.com/us/app/id284882215中，ID为id284882215。
         您的开发团队有权访问 [!UICONTROL App ID] 相关平台。

      1. 在 [!UICONTROL Select File] 字段，请单击 **[!UICONTROL Choose File]** 并选择网络或设备上的文件。

      1. 选中该复选框以表示您同意 [!DNL Adobe] 和广告网络隐私政策。

      1. 单击 **[!UICONTROL Upload File]**.
   1. 指定数量 **[!UICONTROL Membership Days]**，即用户的Cookie在受众中保留的天数。

   使用您希望广告与用户相关的时间长度。 除非您输入值，否则客户列表不会过期。

1. 单击 **[!UICONTROL Post]**.

>[!NOTE]
>
>* 广告网络可能需要长达24小时来处理文件。
>* 参见 [[!DNL Google Ads] 有关客户匹配的工作方式和限制的文档](https://support.google.com/displayvideo/answer/9539301).


## 使用客户数据列表编辑客户匹配受众

您可以更新任何 [!DNL Google Ads] 或 [!DNL Microsoft® Advertising] 客户匹配受众，但 [!DNL Google Ads] 受众创建自 [!DNL Adobe] 受众。 您可以上传数据，以添加、删除或替换受众的所有现有数据。

该数据必须与原始客户列表（电子邮件地址、邮寄地址、电话号码、用户ID或特定移动操作系统上特定应用程序的移动设备ID）的类型相同。

1. 使用现有数据类型的所需格式的客户数据生成文件。

必须使用SHA-256算法对名字和姓氏、电子邮件地址和电话号码进行哈希处理。 <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> 对象 [!DNL Google Ads] 受众，请参见 [!DNL Google Ads] 有关“”的文档[用于上载哈希数据的格式设置准则](https://support.google.com/google-ads/answer/7476159)”以获取允许的联系信息字段和要求的列表。 对象 [!DNL Microsoft® Advertising] 受众，请参见 [!DNL Microsoft® Advertising] 相关文档 [准备客户匹配列表](https://help.ads.microsoft.com/#apex/ads/en/56921. 您可以选择下载 [!DNL Microsoft® Excel] 联系人信息模板。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. 选中要编辑的受众旁边的复选框。

1. 在数据表上方的工具栏中，单击 ![编辑](/help/search-social-commerce/assets/edit.png).

1. 选择操作： *[!UICONTROL Add]* （将上传的数据添加到现有数据，除非现有数据已存在）， *[!UICONTROL Delete]* （从现有数据中删除已上传的数据，如果已存在），或 *[!UICONTROL Replace]* （删除所有现有数据并将其替换为上传的数据）。

1. 上传文件：

   1. 在 [!UICONTROL Select File] 字段，请单击 **[!UICONTROL Choose File]** 并选择网络或设备上的文件。

   1. 选中该复选框以表示您同意 [!DNL Adobe] 和广告网络隐私政策。

   1. 单击 **[!UICONTROL Upload File]**.

1. 单击 **[!UICONTROL Post]**.

>[!NOTE]
>
>广告网络可能需要一段时间来处理对受众的更新。

>[!MORELIKETHIS]
>
>* [关于受众](audience-about.md)
>* [创建 [!DNL Google Ads] 客户匹配受众来自 [!DNL Adobe] 受众](google-audience-from-adobe-audience.md)
>* [创建 [!DNL Google Ads] Adobe Campaign电子邮件列表中的客户匹配受众](google-audience-from-campaign-email-list.md)
>* [管理动态再营销受众](audience-dynamic-remarketing-manage.md)
