---
title: 实施Adobe Advertising Creative概述
description: 了解实施 [!DNL Creative]的基本工作流程。
feature: Creative Introduction
source-git-commit: fbd85ce99ab177c70b95bae42166265ef9053034
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 0%

---

# 实施Adobe Advertising Creative概述

*已关闭的测试版*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

[!DNL Creative]运营团队与每个广告商一起设置其创意和创意体验，或者在DSP中将广告体验作为广告实施，或者向团队提供第三方广告标签以进行自实施，并验证初始成本、点击和转化数据。

Adobe客户团队、代理团队或广告商(取决于service level agreement的条款)需要持续监控每次体验，并根据需要对其进行编辑以实现广告商的目标。

## [!DNL Creative]体验的初始设置任务

实施团队和/或您的机构将与您合作执行以下操作：

1. 定义您的个性化目标（例如，您是否要个性化广告以便潜在客户或重新定位）；所有可用的第一方、第二方和第三方数据，包括创意资源和受众区段；以及实现目标的策略。<!-- and CRM data? used how/where? -->

1. （新广告商帐户）设置管理帐户：

   1. 为[!DNL Creative]设置广告商帐户，并在Advertising Search、Social和Commerce中创建帐户。

      [!DNL Creative]帐户设置位于Advertising DSP中，即使广告商不使用DSP的其余部分也是如此。

      同样，即使广告商不是[!DNL Search, Social, & Commerce]客户，[!DNL Search, Social, & Commerce]帐户仍用于创建转化跟踪标记并在[!DNL Creative]中设置转化列。

   1. （如有必要）为广告商创建用户帐户以查看和管理其创意和广告体验并生成报表。

1. （可选）如果要创建第一方受众区段以包含作为创意内容的目标，请通过以下任一方式创建标记：

   * [创建重定位像素](/help/creative/pixels/retargeting-pixel-manage.md)以将广告重定位到具有特定登陆页面或转化页面的特定属性的访客，然后生成标记以插入到相关网页中。

   * (使用DSP的广告商)在DSP中，[创建自定义受众区段](/help/dsp/audiences/custom-segment-create.md)以跟踪特定登陆页面或转化页面的所有访客，然后生成标记以插入相关网页。

   这两种类型的标记都是图像标记，在添加这些标记的网页上显示1像素x 1像素的透明图像（像素），最终用户看不到该图像。 之后，您可以在广告体验中配置创意内容，以定位特定的重定位像素或区段，以便相关的广告元素仅显示给之前访问过与该像素或区段关联的网站页面的用户。

   广告商的IT部门或其他组可能需要计划标记部署或通知标记部署。

   **注意：**&#x200B;您还可以将来自Adobe Audience Manager和Adobe Analytics的第一方受众用作创意目标。 在访客有资格成为从[!DNL Analytics]共享的受众后，该信息即可在大约24-48小时内在[!DNL Creative]中操作。<!--Are times still true? -->

1. 在DSP中设置营销活动层次结构，您将在其中实施广告体验。 使用与广告体验中的定位兼容的定位，您将在营销活动中实施该定位。

   分层定位行为可能因DSP而异。 Advertising DSP对投放级别定位应用广告级别定位，而不是（代替）投放级别定位。 例如，如果投放位置以澳大利亚的用户为目标，而广告以日本的用户为目标，则广告将以体验的“其他各项”分支为目标。 确保仔细考虑整个营销活动结构。

1. 根据您的广告目标设置广告体验：

   * **自动化工作流：** [!DNL Creative]运营团队可以使用广告模板和数据馈送为您的组织创建动态广告。

     有关更多信息，请与您的Adobe客户团队联系。

     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. --><!-- I think this will be automatic based on their IMS organization. But I'm not sure if they need to be logged in via SSO using their Adobe login or if it will also work using their legacy DSP login. -->

   * **手动工作流：**&#x200B;手动设置广告体验：

      1. [设置要在您的体验中使用的标准创意](/help/creative/creative-libraries/creative-add-standard.md)：

         * 对于[!DNL Creative]将托管的创意，请上传它们。 这可以在Adobe Experience Manager帐户中包含图像资源。

         * 对于在受支持的第三方广告服务器上托管的创意内容，请指向创意文件。

      1. （可选）[将创意分组为包](/help/creative/creative-libraries/bundle-manage.md)，以便您一步即可将其附加到目标体验。

      1. 设置[广告体验](/help/creative/experiences/experience-about.md)：

         * 对于[定向广告体验](/help/creative/experiences/experience-create-targeting.md)，序列创意和可选广告目标。

           广告目标可以包括重新定位您在[!DNL Creative]中创建的像素；您在Adobe Experience Cloud中的受众区段(包括在DSP、Audience Manager或[!DNL Analytics]中)；地理目标；或网页上的特定数据触发器(如SKU=01234567890123或Cart=empty)。

         * 对于[非定向广告体验](/help/creative/experiences/experience-create-no-targeting.md)，请创建常规体验设置。

           广告目标可以包括重新定位您在[!DNL Creative]中创建的像素；您在Adobe Experience Cloud中的受众区段(包括在DSP、Audience Manager或[!DNL Analytics]中)；地理目标；或网页上的特定数据触发器(如SKU=01234567890123或Cart=empty)。













1. 为广告体验设置转化跟踪：


设置转化跟踪。 根据实施，这可能涉及添加
广告商网页的转化跟踪标记和/或设置每天
广告商已单独收集的转化数据的馈送拖放区域。


您可以在Adobe Advertising Search、Social和Advertising Commerce中或Adobe动态标签管理器（以前称为动态标签管理器）中生成转化跟踪标签。
注意：您必须使用JavaScript转换标记，而不是图像标记。


广告商的IT部门或其他组可能需要安排或通知您
关于，标记部署。


（可选）在Search、Social和Commerce中进行每次转化（交易属性）
作为数据视图和报告中的单个列集提供。


转化（交易属性）在Search、Social和Commerce中列出，但位于
已跟踪至少一个转化事件。


如果您没有提供特定量度，则会合并所有转化
在一个“转化”列集中。


验证跟踪的数据。


（可选）设置将计划报表传递到指定的电子邮件地址。


有关说明，请参阅有关“报表”的帮助章节。


在Advertising DSP或其他DSP上设置广告营销活动，并提供JavaScript
或广告商广告体验的iframe标记，广告商可以将其实施为
DSP中的第三方广告。


监控已完成的广告体验的性能（查看预定义的）
单个体验或创建自定义性能报表的性能详细信息。


（根据需要）根据性能和更新的消息传递更新广告体验。






>[!MORELIKETHIS]
>
>* [关于Adobe Advertising Creative](/help/creative/introduction/creative-about.md)
>* [用户界面的组织方式](/help/creative/introduction/ui.md)
