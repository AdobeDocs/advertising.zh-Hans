---
title: 上传离线帐户数据以进行报告和模拟
description: 了解如何手动上传离线帐户数据或将其上传到 [!DNL Amazon] [!DNL S3]存储段以支持报表和模拟。 日志文件跟踪上载作业的进度。
source-git-commit: bfa5403ff66bed73797fc4c7115b8c043856745d
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# 上传离线帐户数据以进行报告和模拟

*为帐户数据上传启用的广告商*

为不支持API报表和性能模拟的帐户上传促销活动内容和离线成本、点击次数和转化数据。

您可以使用[!UICONTROL Upload Logs]功能跟踪上载作业的进度：

* 查看为帐户上传的每个文件的列表。 有关每个文件上传作业的信息包括文件名、上传渠道（*[!UICONTROL Cloud Storage]*&#x200B;或&#x200B;*[!UICONTROL Drag & Drop]*）、同步日期和状态以及上传不完整的原因。

* 下载包含为任何作业上传的帐户实体和相关量度的文件。 这些文件采用逗号分隔值(CSV)格式。

## 手动上传帐户数据

您可以通过在文件中手动上传数据，使用促销活动内容和成本、点击和转化数据填充帐户。

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 执行以下任一操作：

   * （从[!UICONTROL Accounts]视图）：

      1. 选中帐户名称旁边的复选框，然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Upload]**。

      1. 将文件拖到框中，或单击&#x200B;**[!UICONTROL Browse Files]**&#x200B;并从设备或网络中选择文件。

      1. 单击&#x200B;**[!UICONTROL Upload Files]**。

   * （从帐户设置）：

      1. 通过以下任一方式选择帐户：

         * 将光标放在帐户名称上，单击&#x200B;**...**，然后单击&#x200B;**[!UICONTROL Edit]**。

         * 选中帐户名称旁边的复选框，然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Edit]**。

      1. 单击&#x200B;**[!UICONTROL Upload File]**&#x200B;选项卡。

      1. 将文件拖到框中，或单击&#x200B;**[!UICONTROL Browse Files]**&#x200B;并从设备或网络中选择文件。

      1. 单击&#x200B;**[!UICONTROL Save]**。

&#x200B;# 将帐户数据上传到[!DNL Amazon] [!DNL S3]存储段 {#data-upload-s3}

您可以通过将数据上传到[!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3])分段中的搜索、社交和Commerce分配文件夹，来使用促销活动内容和成本、点击和转化数据填充帐户。

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

>[!PREREQUISITES]
>
>* 请联系您的Adobe客户团队，为您的Search、Social和Commerce广告商帐户启用帐户数据上传。 团队将协助在[!DNL S3]存储桶中创建特定于组织的文件夹，并在完成时通知您。<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
>* 检索您帐户的[!DNL S3]云存储路径、访问密钥ID和访问密钥。 组织的所有数据上传<!-- naming convention?-->帐户均使用相同的访问密钥ID和秘密访问密钥。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 执行以下任一操作：

   * （从[!UICONTROL Accounts]视图）：

      1. 选中帐户名称旁边的复选框，然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Upload]**。

      1. 在[!UICONTROL Cloud Storage Link]框中，单击&#x200B;**[!UICONTROL Go to the Link]**。

      1. 单击&#x200B;**[!UICONTROL Show Access Key and Secret]**。

      1. 在[!UICONTROL Storage Link]字段旁边，单击&#x200B;**[!UICONTROL Copy]**&#x200B;以将链接复制到剪贴板，并将该链接存储在一个安全位置。

      1. 同样，复制并安全存储[!UICONTROL Access Key]和[!UICONTROL Secret Key]值。

      1. 单击&#x200B;**[!UICONTROL Done]**。

   * （从帐户设置）：

      1. 通过以下任一方式选择帐户：

         * 将光标放在帐户名称上，单击&#x200B;**...**，然后单击&#x200B;**[!UICONTROL Edit]**。

         * 选中帐户名称旁边的复选框，然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Edit]**。

      1. 单击&#x200B;**[!UICONTROL Upload File]**&#x200B;选项卡。

      1. 在[!UICONTROL Cloud Storage Link]框中，单击&#x200B;**[!UICONTROL Go to the Link]**。

      1. 单击&#x200B;**[!UICONTROL Show Access Key and Secret]**。

      1. 在[!UICONTROL Storage Link]字段旁边，单击&#x200B;**[!UICONTROL Copy]**&#x200B;以将链接复制到剪贴板，并将该链接存储在一个安全位置。

      1. 同样，复制并安全存储[!UICONTROL Access Key]和[!UICONTROL Secret Key]值。

      1. 单击&#x200B;**[!UICONTROL Done]**。

      1. 单击&#x200B;**[!UICONTROL Save]**。

1. （每个组织一次）设置您的本地AWS环境：

   1. 从以下位置下载并安装[!DNL AWS Command Line Interface] (AWS CLI)： [https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)。

   1. 配置AWS凭据：

      1. 创建纯文本文件并将其命名为`~/.aws/credentials`（不带文件扩展名）。

      1. 在任意文本编辑器中打开文件，然后按如下方式输入组织的访问密钥ID和秘密访问密钥：

         ```
         [default]
         aws_access_key_id = <Access key copied in Step 2>
         aws_secret_access_key = <Secret key copied in Step 2>
         ```

1. 从广告网络下载帐户数据报表并保存。

1. 在AWS CLI中，运行以下命令以将帐户数据上传到[!DNL S3]云位置。

   ```
   aws s3 cp <local-report-file-location <S3-cloud-location-associated-with-your-account>
   ```

   示例： `aws s3 cp filename.txt s3://cloud-location/`

## 查看已上载帐户数据文件的日志

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**。

1. 将光标放在帐户名称上，单击&#x200B;**...**，然后单击&#x200B;**[!UICONTROL Upload Logs]**。

1. （可选）要下载已上传文件的数据，请单击![列中的](/help/search-social-commerce/assets/download.png "下载")下载[!UICONTROL Download]，然后按照浏览器的正常过程下载文件。

## 所需数据

数据必须符合广告网络的数据要求。 每个实体的数据字段可能会因广告网络而异。
