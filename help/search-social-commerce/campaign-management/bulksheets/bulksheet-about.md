---
title: 关于使用批量处理工作表管理营销活动数据
description: 了解广告网络、批量处理工作表工作流和错误处理可用的批量处理工作表功能。
exl-id: 34a16ee3-9eba-4b8b-a5ca-65318f4ee6c5
feature: Search Bulksheets
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 0%

---

# 关于使用批量处理工作表管理营销活动数据

批量工作表是一个文件，其中包含以特定格式显示的促销活动数据，可用于快速创建或修改促销活动和广告组结构数据以及文本广告。 您可以生成（下载）包含一个或多个帐户、特定促销活动和广告组，甚至特定文本广告、投放位置和产品组数据的批量处理工作表。 可使用批量工作表管理大型数据集或进行较小更改。 每个广告网络需要不同的信息列。

您可以使用所需数量的数据生成批量工作表，也可以根据需要手动创建并上传这些数据（请参阅关于“批量工作表中必需/包含的数据”一章）。

创建批量工作表后，您可以标识需要更正的任何损坏的登陆页面，或添加或编辑其他数据。 然后，您可以编辑文件并将其上传到Search、Social和Commerce，可以选择安排立即或稍后将其发布到相关广告网络。 您还可以立即或稍后发布可用的批量处理工作表。

您可以选择将批量工作表文件上传到指定的FTP帐户以进行检索和自动发布。 目录每小时扫描一次，新文件会按接收顺序发布到搜索网络。

所有批量处理工作表、登陆页验证错误文件和其他错误文件都将在创建30天后自动删除，除非您提前删除。

## 按广告网络列出的功能

* **下载、上载和发布：** [!DNL Baidu]、[!DNL Google Ads]、[!DNL Microsoft Advertising]和[!DNL Yandex]帐户

* **仅下载和上传：** [!DNL Naver]帐户

  您可以上传[!DNL Naver]数据以供在Search、Social和Commerce中使用，但无法将其发布到广告网络。 您还可以下载现有（未同步）数据。

* **仅下载数据：** [!DNL Pinterest]、[!DNL Yahoo Native]和[!DNL Yahoo! Display Network]帐户

  您可以下载现有（未同步）数据。

## 使用批量处理工作表概述

将批量工作表用于已同步帐户的标准步骤如下：

<!-- insert image
  [EDIT/RECREATE FILE to replace "search engine"]
-->

1. [将一个或多个帐户、营销活动或广告组的数据下载到批量处理工作表文件中](bulksheet-download.md)。 或者，您也可以手动填充特定于广告网络的批量工作表并上传文件。

1. [验证文件中的基本（最终） URL或目标URL中的登陆页面](bulksheet-validate-landing-pages.md)。

1. 需要添加数据或进行更正时：

   1. [将文件](bulksheet-export.md)导出到桌面，并在[!DNL Microsoft Excel]中进行编辑。

   1. [手动将编辑后的文件](bulksheet-upload.md)上传到Search、Social和Commerce，或者[将文件上传到指定的FTP帐户](bulksheet-ftp-account.md)以自动发布。

1. （对于手动上传的文件）[在上传时或稍后将文件](bulksheet-post.md)发布到广告网络。

1. （如有必要）下载任何新的错误文件，更正行，然后重新发布文件。

## 管理上传和发布营销活动数据时的错误

Search、Social和Commerce会从营销活动批量表中上传和发布尽可能多的数据行，包括它在需要时生成的跟踪URL。

当批量处理工作表操作过程中发生错误时，将生成以下两种错误文件之一：

* **[!UICONTROL EF Errors]：**&#x200B;当无法上载或处理文件或文件中的单个行时，将创建一个名为`<uploaded file name>_ef_errors.<extension used for the bulksheet>`的错误文件。 如果问题出现在单个行中，则会包含这些行，并解释每个错误，以便进行更正。

* **[!UICONTROL SE Errors]：**&#x200B;当已发布文件但广告网络不接受部分或全部数据时，将创建一个名为`<uploaded file name>_se_errors.<extension used for the bulksheet>`的错误文件。 当部分（而非全部）行被接受时，错误文件会显示未发布的行以及每个错误的说明，以便进行更正。 错误消息显示在每行的最后三列中。

>[!NOTE]
>
>如果您发布任何[!DNL Google Ads]个违反广告网络的广告政策，但可能有资格获得劐免的广告，则这些广告将自动重新发布并带有劐免请求。 如果免除请求失败，则错误文件中将包含有关违规的信息。

您可以下载任一类型的错误文件，直接在行中进行更正，然后重新上传并发布文件。

错误文件会在30天后自动删除，除非您提前删除。

## 有关每个文件的信息

所有下载的数据文件、上载的文件和错误文件都可以从[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Bulksheets]获得。

每个文件的信息包括当前任务状态和任务完成的百分比、创建任务的日期、（适用时）将其发布到或将要发布到指定广告网络的日期、计划删除日期以及启动任务的用户的登录名。

>[!MORELIKETHIS]
>
>* [下载/创建批量处理工作表文件](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
>* [上载批量工作表或已更正的错误文件](bulksheet-upload.md)
>* [发布批量工作表或已更正的错误文件](bulksheet-post.md)
>* [导出生成或上载的批量工作表文件](bulksheet-export.md)
