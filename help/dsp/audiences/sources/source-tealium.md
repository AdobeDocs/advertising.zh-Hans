---
title: 转换用户ID [!DNL Tealium] 到通用ID
description: 了解如何启用DSP以摄取 [!DNL Tealium] 第一方区段。
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 606e721d80f30fa3a3546a14f0f876f4338dd30c
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 0%

---

# 转换用户ID [!DNL Tealium] 到通用ID

*Beta版功能*

将DSP与集成 [!DNL Tealium] 客户数据平台，用于将贵组织的第一方经过哈希处理的电子邮件地址转换为通用ID以进行定向广告。 该流程使用 [!DNL Amazon Web Services] (AWS) firehose连接器。 执行以下步骤，与DSP共享来自Tealium的数据：

1. (要将电子邮件地址转换为 [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->；广告商使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [设置要启用的跟踪 [!DNL Analytics] 测量](#analytics-tracking).

1. [在DSP中创建受众源](#source-create).

1. [准备和共享区段映射数据](#map-data).

1. [在中创建连接器 [!DNL Tealium] 共享区段数据](#tealium-connector).

1. [复制中的现有连接器 [!DNL Tealium] 以继续共享区段](#duplicate-connector).

1. [将通用ID的数量与经过哈希处理的电子邮件地址的数量进行比较](#compare-id-count).

区段应在24小时内可在DSP中使用，并且每24小时刷新一次。

## 步骤1：设置跟踪 [!DNL Analytics] 测量 {#analytics-tracking}

*广告商使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

要将电子邮件地址转换为 [!DNL RampIDs] 或 [!DNL ID5] ID之后，您必须执行以下操作：

1. （如果您尚未这样做）完成所有 [实施的先决条件 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) 并确保 [AMO ID和EF ID](/help/integrations/analytics/ids.md) 将在您的跟踪URL中填充。

1. 向通用ID合作伙伴注册，并在您的网页上部署特定于通用ID的代码，以便匹配从桌面和移动Web浏览器（但不包括移动应用程序）上的ID到显示到达次数的转换：

   * **对象 [!DNL RampIDs]：** 您必须在您的网页上部署一个额外的JavaScript标记，以便匹配从桌面浏览器和移动浏览器（但不是移动应用程序）上的ID到显示到达次数的转换。 请联系您的Adobe客户团队，他们将为您提供注册 [!DNL LiveRamp] [!DNL LaunchPad] 标记自 [!DNL LiveRamp] 身份验证流量解决方案。 注册是免费的，但您必须签署协议。 注册后，您的Adobe客户团队将生成并提供一个唯一标记，供贵组织在网页上实施。

## 步骤2：在DSP中创建受众源 {#source-create}

1. [创建受众源](source-create.md) 将受众导入您的DSP帐户或广告商帐户。 您可以选择将用户标识符转换为 [可用的通用ID格式](source-about.md).

   源设置将包括自动生成的源密钥，您将使用该密钥准备区段映射数据。

1. 创建受众源后，请使用以下对象共享源代码密钥 [!DNL Tealium] 用户。

## 步骤3：准备和共享区段映射数据 {#map-data}

1. 广告商必须准备并共享区段映射数据：

   1. 广告商必须在中准备数据 [!DNL Tealium]：

      1. 使用SHA-256算法对广告商受众的电子邮件ID进行哈希处理。

      1. 将包含经过哈希处理的电子邮件ID的列映射到访客ID类型的属性。

      1. 创建受众，使用 `Tealium_visitor_id` 属性。 应用正确的扩充以触发受众。 请参阅 [[!DNL Tealium] 有关访客ID属性的文档](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

   1. 广告商必须向Adobe客户团队提供区段映射数据，才能在DSP中创建区段。 在逗号分隔的值文件中使用以下列名和值：

      * **外部区段密钥：** 外部区段键，稍后您将在中的连接器的操作设置中指定该键 [!DNL Tealium]. 建议的命名惯例是&#39;&#39;`<DSP source key>_<Tealium segment name>`，例如“57bf424dc10_coffee-drinkers”。 对于DSP源密钥，请使用 [!UICONTROL Source Key] 从DSP受众源设置访问。

      * **区段名称：** 区段名称。

      * **区段描述：** 区段的目的或规则，或同时使用两者。

      * **父级ID：** 保持空白

      * **视频CPM：** 0

      * **显示CPM：** 0

      * **区段窗口：** 区段的存留时间。

## 步骤4：在中创建连接器 [!DNL Tealium] 共享区段数据 {#tealium-connector}

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

            1. 在创建自定义字段的选项中，在 [!DNL Source Key] 字段中，输入 [!UICONTROL External Segment Key] 包含在此 [区段映射数据](#map-data) 在上一个过程中。

               DSP将使用此密钥填充您的区段。

            1. （推荐）创建更新操作以保持区段刷新。

## 步骤5：复制中的现有连接器 [!DNL Tealium] 以继续共享区段 {#duplicate-connector}

每个区段只能有一个连接器，每个连接器只能有一个区段。

1. 在 [!DNL Tealium]，复制要为其创建另一个区段的区段，然后重命名新区段。

1. 在 [!DNL Tealium]，复制 [您创建的连接器](#tealium-connector) ，并从重命名新连接器。`<original name>-copy`”更改为新区段名称。

## 步骤6：比较通用ID的数量与经过哈希处理的电子邮件地址的数量 {#compare-id-count}

完成所有步骤后，在受众库中验证（在从创建或编辑受众时可用） [!UICONTROL Audiences] > [!UICONTROL All Audiences] 区段会在24小时内填充的区段。 将通用ID的数量与原始经过哈希处理的电子邮件地址的数量进行比较。

经过哈希处理的电子邮件地址到通用ID的转换率应大于90%。 例如，如果您从客户数据平台发送100个经过哈希处理的电子邮件地址，则应将其转换为90个以上的通用ID。 90%或更低的翻译率是一个问题。 有关区段计数如何变化的更多信息，请参阅&quot;[电子邮件ID与通用ID之间的数据差异原因](#universal-ids-data-variances)“

区段每24小时刷新一次。 但是，区段中的包含在30天后过期，因此无法确保隐私合规性，因此请从以下位置重新推送受众以刷新受众： [!DNL Tealium] 每30天或更短时间。

有关故障排除支持，请联系您的Adobe客户团队或 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [关于第一方受众源](/help/dsp/audiences/sources/source-about.md)
>* [创建受众源以激活通用ID受众](source-create.md)
>* [受众源设置](source-settings.md)
>* [转换用户ID [!DNL Adobe Real-Time CDP] 到通用ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
