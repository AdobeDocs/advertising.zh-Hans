---
title: 将用户ID从 [!DNL Tealium] 转换为通用ID
description: 了解如何使DSP能够摄取您的 [!DNL Tealium] 第一方区段。
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# 将用户ID从[!DNL Tealium]转换为通用ID

*Beta功能*

使用DSP与[!DNL Tealium]客户数据平台的集成，将贵组织的第一方经过哈希处理的电子邮件地址转换为通用ID以进行定向广告。 该进程使用[!DNL Amazon Web Services] (AWS) firehose连接器。 执行以下步骤，与DSP共享来自Tealium的数据：

1. （要将电子邮件地址转换为[!DNL RampIDs]<!-- or [!DNL ID5] IDs -->；广告商具有[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)） [设置跟踪以启用 [!DNL Analytics] 测量](#analytics-tracking)。

1. [在DSP](#source-create)中创建受众源。

1. [准备并共享区段映射数据](#map-data)。

1. [在 [!DNL Tealium] 中创建连接器以共享区段数据](#tealium-connector)。

1. [在 [!DNL Tealium] 中复制现有连接器以继续共享区段](#duplicate-connector)。

1. [将通用ID的数量与经过哈希处理的电子邮件地址的数量进行比较](#compare-id-count)。

## 步骤1：为[!DNL Analytics]测量设置跟踪 {#analytics-tracking}

*广告商与[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

要将电子邮件地址转换为[!DNL RampIDs]或[!DNL ID5] ID，您必须执行以下操作：

1. （如果尚未这样做）完成实施 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md)的所有[先决条件，并确保在您的跟踪URL中填充[AMO ID和EF ID](/help/integrations/analytics/ids.md)。

1. 向通用ID合作伙伴注册，并在您的网页上部署特定于通用ID的代码，以便匹配从桌面和移动Web浏览器（但不包括移动应用程序）上的ID到显示到达次数的转换：

   * **对于[!DNL RampIDs]：**，您必须在网页上部署额外的JavaScript标记，以匹配从桌面和移动网页浏览器（但不包括移动应用程序）上的ID到显示到达次数的转换。 请与您的Adobe客户团队联系，他们将为您提供如何从[!DNL LiveRamp]身份验证流量解决方案注册[!DNL LiveRamp] [!DNL LaunchPad]标记的说明。 注册是免费的，但您必须签署协议。 注册后，您的Adobe客户团队将生成并提供一个唯一标记，供贵组织在网页上实施。

## 步骤2：在DSP中创建受众源 {#source-create}

1. [创建受众源](source-manage.md)以将受众导入您的DSP帐户或广告商帐户。 您可以选择将用户标识符转换为[可用的通用ID格式](source-about.md)中的任意格式。

   源设置将包括自动生成的源密钥，您将使用该密钥来准备区段映射数据。

1. 创建受众源后，与[!DNL Tealium]用户共享源代码密钥。

## 步骤3：准备和共享区段映射数据 {#map-data}

广告商必须准备并共享区段映射数据。

1. 广告商必须在[!DNL Tealium]内准备数据：

   1. 使用SHA-256算法对广告商受众的电子邮件ID进行哈希处理。

   1. 将包含经过哈希处理的电子邮件ID的列映射到访客ID类型的属性。

   1. 创建具有`Tealium_visitor_id`属性的受众。 应用正确的扩充以触发受众。 请参阅[[!DNL Tealium] 有关访客ID属性](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/)的文档。

1. 广告商必须向Adobe客户团队提供区段映射数据，才能在DSP中创建区段。 在逗号分隔的值文件中使用以下列名和值：

   * **外部区段键：**&#x200B;外部区段键，稍后将在[!DNL Tealium]中连接器的操作设置中指定该键。 建议的命名惯例是“`<DSP source key>_<Tealium segment name>`”，如“57bf424dc10_coffee-drinkers”。 对于DSP源密钥，请使用DSP受众源设置中的[!UICONTROL Source Key]。

   * **区段名称：**&#x200B;区段名称。

   * **区段描述：**&#x200B;区段的用途或规则，或同时使用两者。

   * **父ID：**&#x200B;保留为空

   * **视频CPM：** 0

   * **显示CPM：** 0

   * **区段窗口：**&#x200B;区段生存时间。

## 步骤4：在[!DNL Tealium]中创建连接器以共享区段数据 {#tealium-connector}

对于要共享的每个区段，为触发数据更改的每个操作创建一个单独的连接器。 例如，要共享两个各自具有两个触发器的区段，请创建四个连接器。

1. Adobe客户团队为广告商提供AWS firehose连接器凭据。

1. 在[!DNL Tealium]中，[使用以下选项添加连接器](https://docs.tealium.com/server-side/connectors/add/)：

   1. 选择[!DNL AWS Firehose]连接器。

   1. 在源设置中：

      1. 选择要共享的受众区段。

      1. 设置触发器：

         * 对于区段的第一个连接器，选择触发器`Joined Audience`。 这样可以确保在用户加入区段时与DSP共享数据。

         * 对于区段的第二个连接器，选择触发器`Left Audience`。 此连接器用于处理所有选择退出和离开DSP中的区段的用户。

   1. 在配置设置中，指定AWS firehose连接器。 如果尚未添加适用于DSP的firehose连接器，请使用以下信息添加firehose连接器：

      * **名称：**&#x200B;连接器的名称。

      * **访问密钥：** Adobe帐户团队提供的访问密钥。

      * **密钥：** Adobe帐户团队提供的密钥。

      * **地区：**&#x200B;美国东北Virginia (us-east-1)

   1. 在操作设置中，执行以下操作：

      1. 使用以下信息创建“将客户数据发送到投放流（高级）”操作以将数据添加到区段：

         * **操作名称：**&#x200B;操作的名称。

         * **操作类型：**&#x200B;将客户数据发送到投放流（高级）

         * **投放流：** Tealium_CDP_Connector

         * **消息数据：**&#x200B;执行以下操作：

            1. 为区段选择一个属性：

               * 对于Hashed_Email属性，将自定义消息命名为`hashed_email`。

               * 对于Cookie属性，将自定义消息命名为`cookies`。

            1. 在创建自定义字段的选项中，在[!DNL Source Key]字段中，输入上一个过程中[区段映射数据](#map-data)中包含的[!UICONTROL External Segment Key]。

               DSP将使用此密钥填充您的区段。

            1. （推荐）创建更新操作以保持区段刷新。

## 步骤5：复制[!DNL Tealium]中的现有连接器以继续共享区段 {#duplicate-connector}

每个区段只能有一个连接器，每个连接器只能有一个区段。

1. 在[!DNL Tealium]中，复制要为其创建其他区段的区段，然后重命名新区段。

1. 在[!DNL Tealium]中，复制[您在上一步中创建的连接器](#tealium-connector)，并将新连接器从“`<original name>-copy`”重命名为新的区段名称。

## 步骤6：比较通用ID的数量与经过哈希处理的电子邮件地址的数量 {#compare-id-count}

区段应在24小时内可在DSP中使用。 DSP收到区段数据后，受众计数应在九(9)小时内可见。

验证您的受众库（在从[!UICONTROL Audiences] > [!UICONTROL All Audiences]创建或编辑受众时或在版面设置内创建或编辑受众时可用）中是否正在填充区段，并将通用ID的数量与原始经过哈希处理的电子邮件地址的数量进行比较。 有关可接受的ID转换率以及区段计数发生变化原因的信息，请参阅[电子邮件ID与通用ID之间的数据差异](#universal-ids-data-variances)。

区段每24小时刷新一次。 但是，默认情况下，区段中的内容会在30天后过期，或者在客户指定的有效期后过期。 在到期之前从[!DNL Tealium]重新推送区段，以刷新区段。 要请求自定义区段过期，请联系您的Adobe客户团队。

## 故障排除

若要解决翻译速率和用户计数问题，请参阅“[激活通用ID的支持](/help/dsp/audiences/universal-ids.md)”。

若要排除转换过程的问题，请与您的Adobe客户团队或`adcloud-support@adobe.com`联系。

>[!MORELIKETHIS]
>
>* [关于第一方受众源](/help/dsp/audiences/sources/source-about.md)
>* [管理受众源以激活通用ID受众](source-manage.md)
>* [支持激活通用ID](/help/dsp/audiences/universal-ids.md)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
