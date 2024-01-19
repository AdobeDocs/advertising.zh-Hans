---
title: 用于将DSP集成与配合使用的工作流 [!DNL Tealium]
description: 了解如何启用DSP以摄取 [!DNL Tealium] 第一方区段。
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: b94541bf8675d535b2f19b26c05235eb56bc6c0b
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# 用于将DSP集成与配合使用的工作流 [!DNL Tealium]

您可以从以下位置共享您组织的第一方数据 [!DNL Tealium] 客户数据平台使用 [!DNL Amazon Web Services] (AWS) firehose连接器。 与DSP共享来自Tealium的数据需要四个步骤：

1. [在DSP中创建受众源](#source-create).

1. [准备和共享区段映射数据](#map-data).

1. [在中创建连接器 [!DNL Tealium] 共享区段数据](#tealium-connector).

1. [复制中的现有连接器 [!DNL Tealium] 以继续共享区段](#duplicate-connector).

## 步骤1：在DSP中创建受众源 {#source-create}

* [创建受众源](source-create.md) 将受众导入您的DSP帐户或广告商帐户，并与共享源代码密钥 [!DNL Tealium] 用户。

## 步骤2：准备和共享区段映射数据 {#map-data}

1. 广告商必须准备并共享区段映射数据：

   1. 广告商必须在中准备数据 [!DNL Tealium]：

      1. 广告商受众的电子邮件ID必须使用SHA-256算法进行哈希处理。

      1. 包含经过哈希处理的电子邮件ID的列必须映射到访客ID类型的属性。

      1. 必须使用创建受众 `Tealium_visitor_id` 属性。 必须应用权限扩充以触发受众。 请参阅 [[!DNL Tealium] 有关访客ID属性的文档](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

   1. 广告商必须向Adobe客户团队提供区段映射数据，才能在DSP中创建区段。 在逗号分隔的值文件中使用以下列名和值：

      * **外部区段密钥：** 外部区段键，稍后您将在中的连接器的操作设置中指定该键 [!DNL Tealium]. 建议的命名惯例是&#39;&#39;`<DSP source key>_<Tealium segment name>`，例如“57bf424dc10_coffee-drinkers”。

      * **区段名称：** 区段名称。

      * **区段描述：** 区段的目的或规则，或同时使用两者。

      * **父级ID：** 保持空白

      * **视频CPM：** 0

      * **显示CPM：** 0

      * **区段窗口：** 区段的存留时间。

## 步骤3：在中创建连接器 [!DNL Tealium] 共享区段数据 {#tealium-connector}

对于要共享的每个区段，为触发数据更改的每个操作创建一个单独的连接器。 例如，要共享两个各自具有两个触发器的区段，请创建四个连接器。

1. Adobe客户团队为广告商提供AWS firehose连接器凭据。

1. 在 [!DNL Tealium]， [添加连接器](https://docs.tealium.com/server-side/connectors/add/)，使用以下选项：

   1. 选择 [!DNL AWS Firehose] 连接器。

   1. 在源设置中：

      1. 选择要共享的受众区段。

      1. 设置触发器：

         * 对于段的第一个连接器，选择触发器 `Joined Audience`. 这样可以确保在用户加入区段时与DSP共享数据。

         * 对于段的第二个连接器，选择触发器 `Left Audience`. 此连接器用于处理所有选择退出和离开DSP中的区段的用户。

   1. 在配置设置中，指定AWS firehose连接器。 如果尚未添加适用于DSP的firehose连接器，请使用以下信息添加firehose连接器：

      * **名称：** 连接器的名称。

      * **访问密钥：** Adobe帐户团队提供的访问密钥。

      * **密钥：** Adobe帐户团队提供的密钥。

      * **区域：** 美国东北弗吉尼亚(us-east-1)

   1. 在操作设置中，执行以下操作：

      1. 使用以下信息创建“将客户数据发送到投放流（高级）”操作以将数据添加到区段：

         * **操作名称：** 操作的名称。

         * **操作类型：** 将客户数据发送到投放流（高级）

         * **投放流：** Tealium_CDP连接器

         * **消息数据：**  执行以下操作：

            1. 为区段选择一个属性：

               * 对于Hashed_Email属性，命名自定义消息 `hashed_email`.

               * 对于Cookie属性，将自定义消息命名为 `cookies`.

            1. 在创建自定义字段的选项中，在 [!DNL Source Key] 字段中，输入 [!UICONTROL External Segment Key] 数据中包含的其他区段映射数据 [步骤2](#map-data).

               DSP将使用此密钥填充您的区段。

            1. （推荐）创建更新操作以保持区段刷新。

## 步骤4：复制中的现有连接器 [!DNL Tealium] 以继续共享区段 {#duplicate-connector}

每个区段只能有一个连接器，每个连接器只能有一个区段。

1. 在 [!DNL Tealium]，复制要为其创建另一个区段的区段，然后重命名新区段。

1. 在 [!DNL Tealium]，复制您在中创建的连接器 [步骤3](#tealium-connector)，并从&#39;&#39;重命名新连接器`<original name>-copy`”更改为新区段名称。

>[!MORELIKETHIS]
>
>* [关于从受众源激活经过身份验证的区段](/help/dsp/audiences/sources/source-about.md)
>* [创建受众源以激活第一方受众](source-create.md)
>* [受众源设置](source-settings.md)
>* [用于将DSP集成与配合使用的工作流 [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
