---
title: 设置数据收集、数据传输和报告
description: 了解如何设置数据收集、数据传输和报表。
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: ab50a3f60651d52eb0b1e18909891c347aabdb77
workflow-type: tm+mt
source-wordcount: '1797'
ht-degree: 0%

---

# 设置数据收集、数据传输和报告

*Beta功能*

在Customer Journey Analytics中查看Advertising Cloud数据需要执行以下任务。

1. （贵组织的Web分析师；可选）[收集AMO ID和EF ID的历史数据](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}。

   此步骤仅适用于具有[!DNL Analytics for Advertising]的广告商。

1. (贵组织的Adobe Experience Platform网站管理员) [在Experience Platform中设置数据收集并实施转化跟踪标记](#data-collection)。

1. (贵组织的Customer Journey Analytics站点管理员) [在Customer Journey Analytics中创建与Experience Platform数据集的连接](#dataset-connection)。

1. （您组织的Web分析师）[在Customer Journey Analytics中设置数据视图](#cja-data-views)。

1. （您组织的Web分析师） [在Customer Journey Analytics Workspace中设置报告和可视化图表](#cja-reports)。

以下部分包含详细的过程，其中包括集成所需的任务和设置，但并未说明工作流中所有可用的功能。 有关完整信息，请参阅链接的资源。

## 在Adobe Experience Platform中和您的网站上设置数据收集 {#data-collection}

在Experience Platform中设置数据收集并实施转化跟踪标记需要以下任务。 您组织的Experience Platform站点管理员可以执行这些任务，但您组织的IT部门可能需要帮助部署跟踪标记。

### 收集数据并将数据从Adobe Advertising作为数据集发送到Experience Platform Edge Network

1. 在Experience Platform中，[为要使用Experience Data Model (XDM)收集的数据定义手动架构](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas)。

   * 在[!UICONTROL Schema Details]中，选择&#x200B;**[!UICONTROL Experience Event]**&#x200B;作为用于捕获站点事件的架构的基类。 命名您的架构，然后单击&#x200B;**[!UICONTROL Finish]**。

   * 在左侧面板中，添加字段组`Adobe Advertising Cloud ExperienceEvent Full Extension`以添加特定于Adobe Advertising的字段。<!-- Add link once published -->至少包括具有`trackingCode`和`trackingIdentities`属性的conversionDetails对象，这些属性包括[AMO ID和EF ID](ids.md)。 其他字段为可选字段。

   * （可选）根据需要添加其他字段组，以将其他数据字段连接到Adobe Advertising数据。

   **注意：**&#x200B;您可以创建多个架构，但每个数据集和每个数据流只能使用一个架构，您将在以下步骤中创建该架构。

1. [基于架构创建数据集](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create)以存储和管理事件数据集合。

   * 选择&#x200B;**[!UICONTROL Create dataset from schema]**&#x200B;的选项并选择您的架构。

     Adobe Advertising会根据您的事件数据集，为相关的摘要量度数据（如转化值）和查找数据(维度/分类元数据，如Adobe Advertising促销活动名称)创建其他数据集。 数据集的数据每天在Experience Platform中填充。

1. [为架构创建数据流](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)。

   * 对于[!UICONTROL Mapping schema]设置，选择您的架构。

   * 向数据流添加并启用服务`Adobe Advertising`和`Adobe Experience Platform`。

     这些服务允许Edge Network存储数据集并将其路由到Adobe Advertising。

   * 对于[!UICONTROL Event dataset]设置，选择您的数据集。

     每个数据流只能将数据插入一个数据集。

### 将贵组织的网站数据发送到您的Experience Platform数据流：

1. 使用Experience Platform [标记](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home)（以前称为[!DNL Launch]）生成JavaScript标记，以将贵组织的网站数据发送到数据流。

   * 创建标记属性，该属性是标记配置的容器。

   * 对于您的资产，请从扩展目录中[安装“Adobe Experience Platform Web SDK”扩展](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration)。

     此扩展通过Experience Platform Edge Network将数据从Web资产发送到Experience Cloud。

     请勿使用Adobe Advertising扩展。

   * 创建自定义Web SDK内部版本：

      * 在[!UICONTROL Custom build components]部分中，启用&#x200B;**Advertising**&#x200B;组件。

        此组件在标记中包含Adobe Advertising所需的所有JavaScript代码。 它还在标记规则（可选）中添加了“Advertising”设置，以定义如何将广告数据用于归因测量。

        您可以根据需要选择启用其他组件。

      * 在[!UICONTROL SDK Instances]部分中：

         * 在[!UICONTROL Datastreams]设置中，选择要用于每个Web环境（生产、暂存、开发）的数据流。

         * (仅具有Adobe Advertising DSP的组织)在[!UICONTROL Adobe Advertising]设置中：

            * 启用&#x200B;**[!UICONTROL Adobe Advertising DSP]**&#x200B;设置以启用浏览跟踪。

            * 指定要为其启用显示到达跟踪的广告商。

            * （可选）输入贵组织的ID5合作伙伴ID以收集ID。

            * （可选）输入您组织的[!DNL LiveRamp RampID]JavaScript代码(ats.js)的路径以收集ID。

         * 保存内部版本。

   * （可选） [根据需要创建规则](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules)，以确定Web SDK何时应将数据发送到Edge Network。

      * 对于[!UICONTROL Advertising]设置，定义如何将广告数据用于归因测量。 当规则包含一系列多个操作时，此设置非常有用，并且仅在您为自定义生成组件选择“[!UICONTROL Advertising]”组件时可用。 选项包括：

        *自动：*&#x200B;允许使用广告数据根据缓存中的数据测量当前`sendEvent`操作的广告归因。 在这种情况下，广告曝光事件会在获得机会时触发，并且它可能对当前事件不可用。 例如，如果您触发了购买签出事件，但缓存中没有可用的广告曝光数据，则签出事件不会归因于广告曝光。

        *等待：*&#x200B;延迟调用的执行，直到成功从服务器检索广告数据并加以解析，从而确保准确的归因测量。 例如，您可能需要等待广告曝光事件解决后再触发购买签出事件。 **注意：**&#x200B;解析ID可能需要几秒钟的时间，具体取决于浏览器和ID类型。 如果当前`sendEvent`操作可以适应几秒钟的延迟，则使用此选项。

        *已禁用：*（默认）从要触发的请求中排除广告数据，使其不可用于归因或相关跟踪。

        *提供数据元素：*&#x200B;使用数据元素在页面加载期间包含或排除广告数据。 数据元素的解析值可以包括`automatic`、`wait`和`disabled`。 请参阅下一步。

     如果不使用规则配置`sendEvent`操作，则广告数据将作为单独的广告扩充事件发送。

   * 根据需要创建[数据元素](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements)，以将网站上的变量映射到您之前创建的XDM架构的结构。

1. [将标记](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow)发布到测试环境，您可以在其中迭代开发标记。

1. 验证数据集的投放，然后[将标记发布到实时生产环境](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow)。

   您组织的IT部门或其他小组可能需要计划标记部署或通知其相关信息。

## 在Customer Journey Analytics中创建与Experience Platform数据集的连接 {#dataset-connection}

按照以下步骤将Adobe Advertising数据从Experience Platform数据集提取到Customer Journey Analytics中。 您组织的Customer Journey Analytics站点管理员可以执行这些任务。

1. 在Customer Journey Analytics中，[创建一个连接](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection)，其中包含您的Experience Platform数据集和架构。

   **注意：**&#x200B;当前，您必须将所有DSP帐户以及Search、Social和Commerce帐户的数据发送到单个Experience Platform实例和沙盒。

   * 添加Experience Platform事件（指标）数据集、摘要（指标）数据集和维度（分类/元数据）数据集。

     您的团队创建了事件数据集，Adobe Advertising根据您的事件数据集创建了摘要和维度数据集。

     您可以根据需要选择包含其他数据集。

   * 将维度数据集映射到事件数据集：

      1. 打开维度数据集的设置。

         设置页面上的标题为“[!UICONTROL Lookup Dataset]”，这表示您可以将维度数据集与某个特定于指标的数据集连接起来。

      1. 在[!UICONTROL Adobe Advertising Dimensions]部分中，将维度数据集映射到事件数据集：

         1. 对于[!UICONTROL Key]字段，选择要用作维度数据集键的字段： `Adobe Advertising ID` （与架构中的`trackingCode`字段相同）。

         1. 对于[!UICONTROL Matching key]字段，选择要用作事件数据集匹配键的字段。 可用字段名称包括括号中的数据集名称。 例如，如果要将维度数据集映射到事件数据集，请选择`Tracking Code (Event datasets)`。

         稍后，在设置数据视图时，您还将将事件数据集映射到摘要#cja-data-views据集。

1. 几小时后，验证数据在Customer Journey Analytics中是否可用。

   1. 在Customer Journey Analytics中，转到&#x200B;**[!UICONTROL Connections]**&#x200B;并选择您的连接。

   1. 在显示的数据集列表中，验证“[!UICONTROL Number of Records]”报表显示数据已添加。

## 在Customer Journey Analytics中设置数据视图 {#cja-data-views}

在Customer Journey Analytics中，创建一个或多个数据视图以定义用于报表的指标和维度。 Web分析人员可以执行这些任务。

1. 在Customer Journey Analytics中，[创建数据视图](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview)。

1. 配置视图以包含以下信息。

   * 如果您拥有Adobe Analytics帐户，请在[!UICONTROL Time Zone]选项卡的[!DNL Analytics]部分中为您的[!UICONTROL Calendar]帐户使用[!UICONTROL Configure]。

   * 在[!UICONTROL Components]选项卡上：

      * 添加维度、事件和摘要数据集。

      * 从事件（量度）数据集和维度（分类/元数据）数据集中选择要包含在数据视图中的量度。

        您已在在[上一个过程](#dataset-connection)中创建的连接中连接了这两个数据集。

      * 将事件数据集连接到摘要数据集，该数据集尚未连接到任何内容：

         * 对于每个包含希望在Customer Journey Analytics中可用的摘要数据的维度，[创建一个派生字段](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/derived-fields)。

           例如，要查看营销活动的摘要数据，请为维度`Adobe Advertising Campaign`创建一个派生字段。

           您将使用匹配键`trackingCode`(即Adobe Advertising ID的架构字段)链接这两个数据集。

            * 在派生规则生成器的[!UICONTROL Lookup]部分中：

               * 对于&#x200B;**[!UICONTROL Value]**&#x200B;字段，从量度摘要数据集中选择“[!UICONTROL Tracking Code]”。

               * 对于&#x200B;**[!UICONTROL Lookup dataset]**&#x200B;字段，请选择维度数据集(如“Adobe Advertising分类”)。

               * 对于&#x200B;**[!UICONTROL Matching Key]**&#x200B;字段，请从分类数据集中选择“[!UICONTROL Tracking Code]”。

               * 对于&#x200B;**[!UICONTROL Values to return]**&#x200B;字段，请从分类数据集中选择维度（如“[!UICONTROL Adobe Advertising Campaign]”）。

           派生字段名称后附有“(DF)”，如`Adobe Advertising Campaign(DF)`。

         * 对于每个派生字段：

            * 在[!UICONTROL Included components]部分中，添加派生字段。

              现在，同一维度中列出了两个名称(例如，“Adobe Advertising Campaign(DF)”（派生字段）和“Adobe Advertising Campaign”（摘要数据集中的字段）。

            * 在摘要数据集(例如“Adobe Advertising Campaign”)中选择维度，并编辑数据集的设置。

              设置将在右侧打开。

               * 在“摘要数据组”部分中，选择&#x200B;**[!UICONTROL Create grouping]**&#x200B;选项。

               * 对于&#x200B;**[!UICONTROL Dimension]**&#x200B;字段，选择派生的字段(该字段后附有“(DF)”，如“Adobe Advertising Campaign(DF)”)。

               * 选择&#x200B;**[!UICONTROL Hide in reporting]**&#x200B;的选项，这将隐藏Workspace中的派生字段名称。

## 在Customer Journey Analytics Workspace中设置报告和可视化图表 {#cja-reports}

在Customer Journey Analytics Workspace中，按照以下步骤配置报表和可视化图表。 Web分析人员可以执行这些任务。

1. [在Workspace中创建一个项目](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects)，以根据在该数据视图中配置的维度和指标生成报告和可视化图表。

1. （如果您有来自[!DNL Google Ads]或[!DNL Microsoft Advertising]的数据）请使用广告网络特定量度的字段创建发布者跟踪的转化报表，这些字段已分组为`googleConversions`和`microsoftConversions`。

>[!MORELIKETHIS]
>
>* [概述](overview.md)
>* [先决条件](prerequisites.md)
>* [使用的 [!DNL Customer Journey Analytics]](ids.md)Adobe Advertising ID
>* Customer Journey Analytics中的[Adobe Advertising指标和维度](advertising-data-in-cja.md)
>* [收集在Adobe Customer Journey Analytics中使用的AMO ID和EF ID的历史数据](/help/integrations/analytics/rvars-to-evars.md)。
>* [Customer Journey Analytics指南](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)
>* Customer Journey Analytics [适用于Adobe Analytics用户的用户指南](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
