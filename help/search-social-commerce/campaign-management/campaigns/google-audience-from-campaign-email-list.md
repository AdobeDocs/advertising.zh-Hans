---
title: 创建 [!DNL Google Ads] Adobe Campaign电子邮件列表中的客户匹配受众
description: 了解如何创建 [!DNL Google Ads] 客户根据现有Adobe Campaign电子邮件列表匹配受众。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# 创建 [!DNL Google Ads] Adobe Campaign电子邮件列表中的客户匹配受众

*[!DNL Google Ads]仅符合客户匹配条件的客户*

您可以创建 [!DNL Google Ads] 通过在Adobe Campaign中设置帐户链接和工作流，从电子邮件列表中匹配受众 [!DNL Campaign].

要执行此操作，您需要访问 [!DNL Campaign] 实例和包含所需工作流的XML文件，您的Adobe客户团队将为您提供该工作流。 说明可能因版本不同而异 [!DNL Campaign]. 如有必要，您的Adobe客户团队可以帮助您在中设置工作流 [!DNL Campaign].

1. 获取由Advertising Search、Social和Commerce提供的SFTP帐户的凭据。

1. In [!DNL Campaign]，设置将电子邮件列表投放到Advertising Search、Social和Commerce：

   1. 创建 [外部帐户](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html) 要关联您的搜索、社交和商务提供的SFTP帐户，请执行以下操作：

      1. 从左侧菜单中，转到 **\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]**.

      1. 单击 ![创建帐户](/help/search-social-commerce/assets/campaign-create-account.png "创建帐户").

      1. 输入帐户的标签并选择 **[!UICONTROL SFTP]** 作为帐户类型。

      1. 输入URL和端口号 [!DNL Adobe] SFTP服务器和广告商的文件夹名称、用户名和密码。

      1. 单击 **[!UICONTROL Save]**.
   1. In [!DNL Campaign Client]，安装数据包，其中包含发送电子邮件数据所需的工作流：

      1. 从菜单栏转到 **[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]**.

      1. 选择 **[!UICONTROL Install a package from a file]**，然后单击 **[!UICONTROL Next]**.

      1. 找到数据包文件(`AMO_Workflow.xml`)，然后单击 **[!UICONTROL Next]**.

      1. 单击 **[!UICONTROL Start]** 并等待工作流安装。
   1. 编辑已安装的工作流，以选择性地编辑数据查询的过滤器，并识别新受众名称和外部SFTP帐户：

      1. 转到 **[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]** 然后打开包裹。

      1. （可选）编辑数据的任意过滤器：

         * 在工作流中，双击查询活动（如ForkTransition 1）。

         * 编辑过滤器表达式。

         * 单击 **[!UICONTROL Finish]**.
      1. 命名区段：

         * 在工作流中，双击活动 **[!UICONTROL Data extraction (File)]**.

         * 转到 **[!UICONTROL Data extraction (File)]** 选项卡，在 **[!UICONTROL File name]** 字段中，输入扩展名为&quot;`.added`“”（例如PaidSubscribers.added）。

            区段名称不得已存在。 区段名称区分大小写，且必须包含ASCII字符，但不能包含下划线(`_`)。

            但是，如果要将区段添加到特定的 [!DNL Google Ad] 帐户，然后为区段名称附加下划线和 [!UICONTROL User SE Account ID] (搜索、社交和商务ID [!DNL Google Ads] 帐户，而不是网络的帐户ID)：

            `_<User SE Account ID>`

            示例： Paid_Subscribers_1234.added

            >[!NOTE]
            >
            >这是禁止在文件名中使用下划线的规则的例外。

            否则，该区段将添加到所有 [!DNL Google Ads] 正在为广告商同步搜索、社交和商务的帐户。

         * 将选项保留为 **[!UICONTROL Generate an outbound transition]** 已选中。

         * 单击 **[!UICONTROL Ok]**.
      1. 指定要向其发送数据的外部帐户：

         * 在工作流中，双击活动 **[!UICONTROL File Transfer]**.

         * 转到 **[!UICONTROL File Transfer]** 选项卡，在 **[!UICONTROL Remote server]** 部分，选择选项以 **[!UICONTROL Use an external account]**.

         * 在 **[!UICONTROL External account]** 字段中，选择您在步骤2中创建的外部帐户的标签。

         * 在 **[!UICONTROL Server folder]** 字段中，选择值 [!UICONTROL Account] 外部帐户的字段。

         * （可选）在 **[!UICONTROL Schedule]** 选项卡，为文件传输指定不同的计划。

            默认情况下，工作流会在00:00（午夜）运行，这可以确保处理所有记录。 要最大限度地减少延迟，请将工作流安排在不晚于18:00运行。

         * 单击 **[!UICONTROL Ok]**.





搜索、Social和Commerce每30分钟检查一次目录（在广告商所在时区的NN：30和NN：59），并将其找到的任何文件移动到另一个位置，然后自动从数据创建受众，并在22:00（晚上10）将其推送到Google。 搜索、Social和Commerce会继续每30分钟检查一次电子邮件列表是否有更新（加减值），并在以下位置更新受众： [!DNL Google Ads] 因此，每天22点。

>[!NOTE]
>
>* 如果在处理周期之间上载文件的多个版本，则会使用最新的文件。
>
>* Search、Social和Commerce不会存储用于创建或编辑电子邮件列表的任何客户数据 [!DNL Google Ads] 受众。
>
>* [!DNL Google Ads] 可能需要一段时间来处理受众的更新。
>
>* 参见 [[!DNL Google Ads] 有关客户匹配的工作方式和限制的文档](https://support.google.com/displayvideo/answer/9539301).


>[!MORELIKETHIS]
>
>* [关于受众](audience-about.md)
>* [创建 [!DNL Google Ads] 客户匹配受众来自 [!DNL Adobe] 受众](google-audience-from-adobe-audience.md)
>* [使用客户数据列表管理客户匹配受众](audience-from-customer-data-list.md)
>* [管理动态再营销受众](audience-dynamic-remarketing-manage.md)

