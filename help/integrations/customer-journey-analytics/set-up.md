---
title: 设置数据收集、数据传输和报告
description: 了解如何设置数据收集、数据传输和报表。
feature: Integration with Adobe Customer Journey Analytics
exl-id: a955e2b0-ea1b-4b5c-937b-f8c66603cd36
TQID: https://experienceleague.adobe.com/u6xL6FuW-TwqAkse3VTS3zcyt-10Cv-ADTZLJTiWWT8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: c62a18194544bcbe98117b86eccb1b5e2740999c
workflow-type: tm+mt
source-wordcount: 1804
ht-degree: 0%

---

# 设置数据收集、数据传输和报告

使用Advertising DSP和&#x200B;[!DNL Advertising Search, Social, & Commerce]*的*&#x200B;广告商

*仅不带[!DNL Analytics for Advertising]的广告商*

使用[Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html)在Adobe Advertising和Customer Journey Analytics之间原生交换数据需要执行以下任务。 数据传输和归因在启动后开始；不包括历史数据。

1. （贵组织的Web分析师；可选）[收集AMO ID和EF ID的历史数据](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}。

   此步骤仅适用于具有[!DNL Analytics for Advertising]的广告商。

2. （贵组织的Adobe Experience Platform网站管理员）[在Experience Platform中设置数据收集并实施转化跟踪标记](#data-collection)。

3. （贵组织的Customer Journey Analytics站点管理员）[在Customer Journey Analytics中创建与Experience Platform数据集的连接](#dataset-connection)。

4. （您组织的Web分析师）[在Customer Journey Analytics中设置数据视图](#cja-data-views)。

5. （您组织的Web分析师） [在Customer Journey Analytics Workspace中设置报告和可视化图表](#cja-reports)。

以下部分包含详细的过程，其中包括集成所需的任务和设置，但并未说明工作流中所有可用的功能。 有关完整信息，请参阅链接的资源。

## 在Adobe Experience Platform中和您的网站上设置数据收集 {#data-collection}

在Experience Platform中设置数据收集并实施转化跟踪标记需要以下任务。 您组织的Experience Platform站点管理员可以执行这些任务，但您组织的IT部门可能需要帮助部署跟踪标记。

### 收集数据并将数据从Adobe Advertising作为数据集发送到Experience Platform Edge Network

此过程包括创建模式。 您可以选择编辑现有架构；在这种情况下，您无需创建数据集或数据流。

1. 在Experience Platform中，[为要使用Experience Data Model (XDM)收集的数据定义手动架构](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas)。

   * 在[!UICONTROL Schema Details]中，选择&#x200B;**[!UICONTROL Experience Event]**&#x200B;作为用于捕获站点事件的架构的基类。 命名您的架构，然后单击&#x200B;**[!UICONTROL Finish]**。

   * 在左侧面板中，添加字段组[Adobe Advertising Cloud ExperienceEvent Full Extension](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension)以添加特定于Adobe Advertising的字段。 至少包括具有`trackingCode`和`trackingIdentities`属性的conversionDetails对象，这些属性包括[AMO ID和EF ID](ids.md)。 其他字段为可选字段。

   * （可选）根据需要添加其他字段组，以将其他数据字段连接到Adobe Advertising数据。

   **注意：**&#x200B;您可以创建多个架构，但每个数据集和每个数据流只能使用一个架构，您将在以下步骤中创建该架构。

1. [基于架构创建数据集](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create)以存储和管理事件数据集合。 这将是您的&#x200B;*事件数据集*。 如果您使用数据集编辑现有架构，则可以跳过此步骤。

   * 选择&#x200B;**[!UICONTROL Create dataset from schema]**&#x200B;的选项并选择您的架构。

     Adobe Advertising会根据您的事件数据集创建两个其他数据集：1\)包含相关摘要数据（例如点击次数和展示次数）的&#x200B;*摘要数据集*&#x200B;和2\)包含&#x200B;*查找数据集*（包含维度/分类元数据，例如Adobe Advertising促销活动名称）。 数据集的数据每天在Experience Platform中填充。

   >[!TIP]
   >
   >在使用生产数据集之前，首先创建虚拟事件数据集以验证数据流。

1. [创建数据流](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)以指定从网站或应用程序发送数据的位置以及如何处理传入数据。

   * 对于[!UICONTROL Mapping schema]设置，选择您的架构。

   * 向数据流添加并启用服务`Adobe Advertising`和`Adobe Experience Platform`。

     [!UICONTROL Adobe Advertising]服务允许将广告公开与有效负载关联，并且[!UICONTROL Adobe Experience Platform]允许Edge Network存储数据集并将其路由到Adobe Advertising。

   * 对于[!UICONTROL Event dataset]设置，选择您的事件数据集。

     每个数据流只能将数据插入一个数据集。

### 将贵组织的网站数据发送到您的Experience Platform数据流

使用Adobe Tags中的Adobe Experience Platform Web SDK扩展将贵组织的网站数据发送到Experience Platform数据流。

>[!NOTE]
>
>仅支持Adobe标记。 不支持独立的Experience Platform Web SDK (`alloy.js`)或第三方标记管理器。

1. 使用Experience Platform [标记](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home)（以前称为[!DNL Launch]）生成JavaScript标记，以将贵组织的网站数据发送到数据流。

   * 创建标记属性，该属性是标记配置的容器。

   * 对于您的资产，请从扩展目录中[安装“Adobe Experience Platform Web SDK”扩展](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration)。

     此扩展通过Experience Platform Edge Network将数据从Web资产发送到Adobe CX Enterprise。

     请勿使用Adobe Advertising扩展。

   * 创建[自定义Web SDK内部版本](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#custom-build)：

      * 在[!UICONTROL Custom build components]部分中，启用&#x200B;**Advertising**&#x200B;组件。

        此组件包含标记中Adobe Advertising所需的所有JavaScript代码，Advertising DSP和Advertising Search、Social和Commerce客户都需要此组件。 该组件还在标记规则（可选）中添加了“Advertising”设置，以定义如何将广告数据用于归因测量。

        您可以根据需要选择启用其他组件。

      * 在[!UICONTROL SDK Instances]部分中：

         * 在[!UICONTROL Datastreams]设置中，选择要用于每个Web环境（生产、暂存、开发）的数据流。

         * （仅具有Adobe Advertising DSP的组织）在[[!UICONTROL Adobe Advertising]设置](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising)中，启用&#x200B;**[!UICONTROL Adobe Advertising DSP]**&#x200B;以允许查看到达跟踪，并指定为其启用查看到达跟踪的广告商。 您可以选择通过添加组织的ID5合作伙伴ID和/或组织的[!DNL LiveRamp RampID] JavaScript代码(ats.js)的路径从通用ID收集ID。

           如果您的广告商未列出，请输入每个广告商的广告商ID。 如果需要，请向您的Adobe客户团队索取ID。

         * 保存内部版本。

   * （可选） [根据需要创建规则](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules)，以确定Web SDK何时应将数据发送到Edge Network。

      * 对于`[sendEvent](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/actions/send-event)`操作，请使用[[!UICONTROL Advertising]设置](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/action-types#advertising)来定义如何将广告数据用于归因测量。 当规则包含一系列多个操作时，此设置非常有用，并且仅在您为自定义生成组件选择“[!UICONTROL Advertising]”组件时可用。

   * 根据需要创建[数据元素](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements)，以将网站上的变量映射到您之前创建的XDM架构的结构。

1. [将标记](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow)发布到测试环境，您可以在其中迭代开发标记。

1. [检查三个数据集中每个数据集的活动](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#view-datasets)以验证投放。

1. [将标记发布到实时生产环境](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow)。

   您组织的IT部门或其他小组可能需要计划标记部署或通知其相关信息。

## 在Customer Journey Analytics中创建与Experience Platform数据集的连接 {#dataset-connection}

按照以下步骤将Adobe Advertising数据从Experience Platform数据集提取到Customer Journey Analytics中。 您组织的Customer Journey Analytics站点管理员可以执行这些任务。

您还可以选择使用相同信息编辑现有连接。

1. 在Customer Journey Analytics中，[创建或编辑包含Experience Platform数据集和架构的连接](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection)。

   <!-- **Note:** You must send data for all DSP and Search, Social, & Commerce accounts to a single Experience Platform instance and sandbox.  -->

   * 确认选择了正确的沙盒。

   * 计算平均每日事件数（大多数组织不足100万）。

   * 添加Experience Platform事件量度数据集（类型： `Event`）、<!-- Adobe Advertising -->事件摘要量度数据集（类型： `Event`）和<!-- Adobe Advertising -->维度（分类/元数据）数据集（类型： `Lookup`）。

     您的团队创建了事件数据集，Adobe Advertising根据您的事件数据集创建了摘要和维度数据集。

     您可以根据需要选择包含其他数据集。

   * 配置数据集设置：

      * 对于[!UICONTROL Event Dataset]设置：

         * **[!UICONTROL Person ID]:** `Identity Map`

         * **[!UICONTROL Use primary identity namespace]：**&#x200B;启用设置

         * **[!UICONTROL Data Source Type]:** `Web Data > Others` <!-- I don't see "Others" in the screen shot example -->

         * **[!UICONTROL Import all new data]：**&#x200B;启用设置

      * 对于[!UICONTROL Lookup Dataset]设置，将维度数据集映射到事件数据集：

         * **[!UICONTROL Key]** （用作维度数据集键的字段）： `Tracking Code` （与架构中的`trackingCode`字段相同）。

         * **[!UICONTROL Matching key]** （用作事件数据集匹配键的字段）： `Tracking Code (Event datasets)`。<!-- verify this Later, you'll also map the events dataset to the summary dataset when you set up your data view(#cja-data-views).  -->

         * **[!UICONTROL Import all new data]：**&#x200B;启用设置

      * 对于[!UICONTROL Metrics Dataset]设置：

         * **[!UICONTROL Person ID]:** `Identity Map`

         * **[!UICONTROL Timestamp]：**&#x200B;确认值

         * **[!UICONTROL Import all new data]：**&#x200B;启用设置

1. 在三个小时内，验证数据在Customer Journey Analytics中是否可用。

   1. 在Customer Journey Analytics中，转到&#x200B;**[!UICONTROL Connections]**&#x200B;并选择您的连接。

   2. 在显示的数据集列表中，验证“[!UICONTROL Number of Records]”报表显示数据已添加。

## 在Customer Journey Analytics中设置数据视图 {#cja-data-views}

在Customer Journey Analytics中，创建一个或多个数据视图以定义用于报表的指标和维度。 Web分析人员可以执行这些任务。

1. 在Customer Journey Analytics中，[创建数据视图](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview)。

1. 配置视图以包含以下信息。

   * 如果您拥有Adobe Analytics帐户，请在[!UICONTROL Configure]选项卡的[!UICONTROL Calendar]部分中为您的[!DNL Analytics]帐户使用[!UICONTROL Time Zone]。

   * 在[!UICONTROL Components]选项卡上：

      * 添加查找数据集（包含维度/分类数据）、事件数据集（包含事件级别数据）和摘要数据集（包含其他量度，例如点击量）。

      * 从事件数据集和查找数据集中选择要包含在数据视图中的量度。

      * 搜索“[!UICONTROL Tracking Code]”（属于架构路径为`_experience.adcloud.conversionDetails.trackingCode`的事件数据集）。<!-- and do what with it? Add it? Or is that what you --> 将&#x200B;**[!UICONTROL Persistence]**&#x200B;设置为&#x200B;*[!UICONTROL Most Recent]*。

<!--

Seems to not be necessary now:


       You already joined these two datasets in the connection that you created in the [last procedure](#dataset-connection).
     
     *  Join the events dataset to the summary dataset, which isn't yet joined to anything:
     
       * For each dimension with summary data that you want to be available in Customer Journey Analytics, [create a derived field](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/derived-fields).

         For example, to view summary data for campaigns, create a derived field for the dimension `Adobe Advertising Campaign`.
         
         You'll link the two datasets using the matching key `trackingCode` (which is the schema field for the Adobe Advertising ID).
       
         * In the [!UICONTROL Lookup] section of the derived rule builder:
         
           * For the **[!UICONTROL Value]** field, select "[!UICONTROL Tracking Code]" from the metrics summary dataset.

           * For the **[!UICONTROL Lookup dataset]** field, select the dimensions dataset (such as "Adobe Advertising Classification").

           * For the **[!UICONTROL Matching Key]** field, select "[!UICONTROL Tracking Code]" from the classification dataset.

           * For the **[!UICONTROL Values to return]** field, select the dimension (such as "[!UICONTROL Adobe Advertising Campaign]")" from the classification dataset.
         
         The derived field name is appended with "(DF)", such as `Adobe Advertising Campaign(DF)`. 
         
       * For each derived field:
       
         * In the [!UICONTROL Included components] section, add the derived field.
         
           Two names are now listed for the same dimension (for example, "Adobe Advertising Campaign(DF)" (the derived field) and "Adobe Advertising Campaign" (the field in the summary dataset)).

         * Select the dimension in the summary dataset (such as "Adobe Advertising Campaign") and edit the settings for the dataset.

           The settings open on the right.

           * In the the Summary Data Group section, select the option to **[!UICONTROL Create grouping]**.

           * For the **[!UICONTROL Dimension]** field, select the derived field (which is appended with "(DF)," such as "Adobe Advertising Campaign(DF)").
         
           * Select the option to **[!UICONTROL Hide in reporting]**, which hides the derived field name in Workspace.

-->

## 在Customer Journey Analytics Workspace中设置报告和可视化图表 {#cja-reports}

在Customer Journey Analytics Workspace中，按照以下步骤配置报表和可视化图表。 Web分析人员可以执行这些任务。

1. [在Workspace中创建一个项目](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects)，以根据在该数据视图中配置的维度和指标生成报告和可视化图表。

您可以在一个自由格式表中使用相同的维度对摘要指标和事件数据进行分类。

1. （如果您有来自[!DNL Google Ads]或[!DNL Microsoft Advertising]的数据）请使用广告网络特定量度的字段创建发布者跟踪的转化报表，这些字段已分组为`googleConversions`和`microsoftConversions`。

>[!TIP]
>
>摘要事件通常会向报表中添加少量额外数据，例如几个额外事件、每天一个额外的会话或每个报表一个额外的人员。与标准Web事件相比，这些添加的内容可以忽略不计。但是，您可以通过排除虚拟人员ID `00000000-0000-0000-0000-000000000000`的数据来过滤掉此额外的摘要事件数据。
>![使用人员ID排除数据的示例](/help/integrations/assets/cja-report-with-person-id.png "使用人员ID排除数据的示例")

![您的数据集在Customer Journey Analytics中的显示方式](/help/integrations/assets/cja-report-example.png "您的数据集在Customer Journey Analytics中的显示方式")

>[!MORELIKETHIS]
>
>* [概述](overview.md)
>* [先决条件](prerequisites.md)
>*  [!DNL Customer Journey Analytics][&#128279;](ids.md)使用的Adobe Advertising ID
>* Customer Journey Analytics中的[Adobe Advertising指标和维度](advertising-data-in-cja.md)
>* [收集AMO ID和EF ID的历史数据以在Adobe Customer Journey Analytics中使用](/help/integrations/analytics/rvars-to-evars.md)。
>* [Customer Journey Analytics指南](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)
>* Customer Journey Analytics [适用于Adobe Analytics用户的用户指南](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
