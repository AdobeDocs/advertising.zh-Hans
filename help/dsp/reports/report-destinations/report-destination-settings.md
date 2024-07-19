---
title: 报表目标设置
description: 按目标类型查看报表目标所需的详细信息。
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# 报表目标设置

非电子邮件报表目标所需的详细信息因目标类型而异。

>[!NOTE]
>
> 您还可以将自定义报表发送给不需要保存报表目标的电子邮件收件人。 您可以在报表设置中指定电子邮件收件人，而不是保存的目标。

## [!UICONTROL S3]

**[!UICONTROL Name]：**&#x200B;帮助您识别目标的名称。

**[!UICONTROL S3 Bucket URL]：**&#x200B;报告上传到的[!DNL Amazon Simple Storage Service] (S3)存储段上的文件夹的完整路径。 示例： `s3://dsp_account/reports`

**[!UICONTROL Access Key ID]：** ([!DNL Amazon S3])存储段的访问密钥ID （由[!DNL Amazon]提供）。

**[!UICONTROL Secret Access Key]：** ([!DNL Amazon S3])存储段的访问密钥（由[!DNL Amazon]提供）。

## [!UICONTROL FTP]

**[!UICONTROL Name]：**&#x200B;帮助您识别目标的名称。

**[!UICONTROL Server]：**&#x200B;服务器的主机名。

**[!UICONTROL Port]：**&#x200B;要在服务器上使用的端口号。 默认值为&#x200B;*[!UICONTROL 21]*。

**[!UICONTROL Username]：**&#x200B;要登录到服务器的用户名。

**[!UICONTROL Password]：**&#x200B;用于登录到服务器的密码。

**[!UICONTROL Path (Optional)]：**&#x200B;文件上载到的服务器路径。

## [!UICONTROL SFTP]

**[!UICONTROL Name]：**&#x200B;帮助您识别目标的名称。

**[!UICONTROL Server]：**&#x200B;服务器的主机名。

**[!UICONTROL Port]：**&#x200B;要在服务器上使用的端口号。 默认值为&#x200B;*[!UICONTROL 21]*。

**[!UICONTROL Username]：**&#x200B;要登录到服务器的用户名。

**[!UICONTROL Password]：**&#x200B;用于登录到服务器的密码。

**[!UICONTROL Path (Optional)]：**&#x200B;文件上载到的服务器路径。

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]：**&#x200B;帮助您识别目标的名称。

**[!UICONTROL Server]：**&#x200B;服务器的主机名。

**[!UICONTROL Port]：**&#x200B;要在服务器上使用的端口号。 默认值为&#x200B;*[!UICONTROL 21]*。

**[!UICONTROL Username]：**&#x200B;要登录到服务器的用户名。

**[!UICONTROL Password]：**&#x200B;用于登录到服务器的密码。

**[!UICONTROL Path (Optional)]：**&#x200B;文件上载到的服务器路径。

>[!MORELIKETHIS]
>
>* [关于[!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [创建[!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [编辑[!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [删除[!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-delete.md)
