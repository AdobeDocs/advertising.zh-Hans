---
title: 从Adobe Campaign电子邮件列表创建 [!DNL Google Ads] 客户匹配受众
description: 了解如何从现有Adobe Campaign电子邮件列表创建 [!DNL Google Ads] 客户匹配受众。
exl-id: 92812af2-ac31-48cd-badf-ea287799bddb
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/tEiqvHt1QzxhstsKGUsvKGgwm1JYIkv7mGr-Z8kPd0g
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 669
ht-degree: 0%

---

# 从Adobe Campaign电子邮件列表创建[!DNL Google Ads]个客户匹配受众

仅符合客户匹配条件的&#x200B;*[!DNL Google Ads]帐户*

您可以在[!DNL Google Ads]中设置帐户链接和工作流，从而从Adobe Campaign中的电子邮件列表创建[!DNL Campaign]客户匹配受众。

为此，您需要具有对[!DNL Campaign]实例的访问权限以及包含所需工作流的XML文件，您的Adobe客户团队将为您提供该工作流。 说明可能会因不同版本的[!DNL Campaign]而异。 如有必要，您的Adobe客户团队可以帮助您在[!DNL Campaign]中设置工作流。

1. 获取Advertising Search、Social和Commerce提供的SFTP帐户的凭据。

1. 在[!DNL Campaign]中，设置将电子邮件列表传递到Advertising Search、Social和Commerce：

   1. 创建一个[外部帐户](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html?lang=zh-Hans)以关联您的搜索、社交和Commerce提供的SFTP帐户：

      1. 从左侧菜单中，转到&#x200B;**\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]**。

      1. 单击![创建帐户](/help/search-social-commerce/assets/campaign-create-account.png "创建帐户")。

      1. 输入帐户的标签并选择&#x200B;**[!UICONTROL SFTP]**&#x200B;作为帐户类型。

      1. 输入[!DNL Adobe] SFTP服务器的URL和端口号，以及广告商的文件夹名称、用户名和密码。

      1. 单击&#x200B;**[!UICONTROL Save]**。

   1. 在[!DNL Campaign Client]中，安装包含发送电子邮件数据所需的工作流的数据包：

      1. 从菜单栏转到&#x200B;**[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]**。

      1. 选择&#x200B;**[!UICONTROL Install a package from a file]**，然后单击&#x200B;**[!UICONTROL Next]**。

      1. 在设备或网络上找到数据包文件(`AMO_Workflow.xml`)，然后单击&#x200B;**[!UICONTROL Next]**。

      1. 单击&#x200B;**[!UICONTROL Start]**&#x200B;并等待工作流安装。

   1. 编辑已安装的工作流，以选择性地编辑数据查询的过滤器，并识别新受众名称和外部SFTP帐户：

      1. 转到&#x200B;**[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]**&#x200B;并打开包。

      1. （可选）编辑数据的任意过滤器：

         * 在工作流中，双击查询活动（如ForkTransition 1）。

         * 编辑过滤器表达式。

         * 单击&#x200B;**[!UICONTROL Finish]**。

      1. 命名区段：

         * 在工作流中，双击活动&#x200B;**[!UICONTROL Data extraction (File)]**。

         * 在&#x200B;**[!UICONTROL Data extraction (File)]**&#x200B;选项卡的&#x200B;**[!UICONTROL File name]**&#x200B;字段中，输入扩展名为“`.added`”的区段名称（如PaidSubscribers.added）。

           区段名称不得已存在。 区段名称区分大小写，且必须包含ASCII字符，但不能包含下划线(`_`)。

           但是，如果要将区段添加到特定的[!DNL Google Ad]帐户，请为区段名称附加下划线和[!UICONTROL User SE Account ID]（[!DNL Google Ads]帐户的搜索、社交和Commerce的ID，而不是网络的帐户ID）：

           `_<User SE Account ID>`

           示例： Paid_Subscribers_1234.added

           >[!NOTE]
           >
           >这是禁止在文件名中使用下划线的规则的例外。

           否则，该区段将添加到为广告商同步Search、Social和Commerce的所有[!DNL Google Ads]帐户。

         * 将选项保留为&#x200B;**[!UICONTROL Generate an outbound transition]**&#x200B;选定。

         * 单击&#x200B;**[!UICONTROL Ok]**。

      1. 指定要向其发送数据的外部帐户：

         * 在工作流中，双击活动&#x200B;**[!UICONTROL File Transfer]**。

         * 在&#x200B;**[!UICONTROL File Transfer]**&#x200B;选项卡的&#x200B;**[!UICONTROL Remote server]**&#x200B;部分中，选择&#x200B;**[!UICONTROL Use an external account]**&#x200B;的选项。

         * 在&#x200B;**[!UICONTROL External account]**&#x200B;字段中，选择您在步骤2中创建的外部帐户的标签。

         * 在&#x200B;**[!UICONTROL Server folder]**&#x200B;字段中，为外部帐户选择[!UICONTROL Account]字段的值。

         * （可选）在&#x200B;**[!UICONTROL Schedule]**&#x200B;选项卡上，为文件传输指定其他计划。

           默认情况下，工作流在00:00 （午夜）运行，这将确保处理所有记录。 为了最大程度地减少延迟，请计划工作流在不晚于18:00的日期运行。

         * 单击&#x200B;**[!UICONTROL Ok]**。

搜索、Social和Commerce每30分钟检查一次目录（在广告商所在时区的NN:30和NN:59），并将其找到的任何文件移动到其他位置，然后自动从数据创建受众并在22:00 （晚上10:00）将其推送到Google。 搜索、Social和Commerce仍会每隔30分钟检查一次电子邮件列表是否有更新（添加和减少），并相应地每天22[!DNL Google Ads]更新:00上的受众。

>[!NOTE]
>
>* 如果在处理周期之间上载文件的多个版本，则使用最新文件。
>
>* Search、Social和Commerce不会存储您的电子邮件列表中用于创建或编辑[!DNL Google Ads]受众的任何客户数据。
>
>* [!DNL Google Ads]可能需要一段时间来处理受众的更新。
>
>* 请参阅[[!DNL Google Ads] 文档，了解客户匹配的工作方式和限制](https://support.google.com/displayvideo/answer/9539301)。

>[!MORELIKETHIS]
>
>* [关于受众](audience-about.md)
>* [创建来自 [!DNL Google Ads] 受众的 [!DNL Adobe] 客户匹配受众](google-audience-from-adobe-audience.md)
>* [使用客户数据列表管理客户匹配受众](audience-from-customer-data-list.md)
>* [管理动态再营销受众](audience-dynamic-remarketing-manage.md)
