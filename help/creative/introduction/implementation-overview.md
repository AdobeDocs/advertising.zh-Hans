---
title: 实施Adobe Advertising Creative概述
description: 了解实施 [!DNL Creative]的基本工作流程。
feature: Creative Introduction
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# 实施Adobe Advertising Creative概述

*已关闭的测试版*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

[!DNL Creative]运营团队与每个广告商一起设置其创意和创意体验，或者在DSP中将广告体验作为广告实施，或者向团队提供第三方广告标记以进行自实施，并验证初始成本、点击和转化数据。

Adobe客户团队、代理团队或广告商(取决于service level agreement的条款)需要持续监控每次体验，并根据需要对其进行编辑以实现广告商的目标。

## [!DNL Creative]营销活动<!-- Experiences? "Campaigns" may be confusing now. -->的初始设置任务

实施团队和/或您的机构将与您合作执行以下操作：

1. 定义您的个性化目标（例如，您是否要个性化广告以便潜在客户或重新定位）；所有可用的第一方、第二方和第三方数据，包括创意资产、受众区段和CRM数据<!-- used how/where? -->；以及您实现目标的策略。

1. （新广告商帐户）设置管理帐户：

   1. 为[!DNL Creative]<!-- and/or DSP? -->设置广告商帐户，并在Advertising Search中创建帐户。

      [!DNL Creative]帐户设置在Advertising DSP中，即使广告商不是DSP客户也是如此。

      同样，即使广告商不是[!DNL Search]客户，[!DNL Search]帐户仍用于创建转化跟踪标记并在[!DNL Creative]中设置转化列。

   1. （如有必要）为广告商创建用户帐户以查看和管理其创意和广告体验并生成报表。

1. （可选）如果要创建第一方受众区段以包含作为创意内容的目标，请通过以下任一方式创建标记：

   * [创建重定位像素](/help/creative/pixels/retargeting-pixel-manage.md)以将广告重定位到具有特定登陆页面或转化页面的特定属性的访客，然后生成标记以插入到相关网页中。

   * (使用DSP的广告商)在DSP中，[创建自定义受众区段](/help/dsp/audiences/custom-segment-create.md)以跟踪特定登陆页面或转化页面的所有访客，然后生成标记以插入相关网页。

   这两种类型的标记都是图像标记，在添加这些标记的网页上显示1像素x 1像素的透明图像（像素），最终用户看不到该图像。 之后，您可以在广告体验中配置创意内容，以定位特定的重定位像素或区段，以便相关的广告元素仅显示给之前访问过与该像素或区段关联的网站页面的用户。

   广告商的IT部门或其他组可能需要计划标记部署或通知标记部署。

   **注意：**&#x200B;您还可以将来自Adobe Audience Manager和Adobe Analytics的第一方受众用作创意目标。 在访客有资格成为从[!DNL Analytics]共享的受众后，该信息即可在大约24-48小时内在[!DNL Creative]中操作。<!--Still true? And what about AAM and DSP? -->

1. 根据您的广告目标设置广告体验：

   * **自动化工作流：** [!DNL Creative]运营团队可以使用广告模板和数据馈送为您的组织创建动态广告。

     有关更多信息，请与您的Adobe客户团队联系。

     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. -->

   * **手动工作流：**&#x200B;手动设置广告体验：

      1. 设置要在您的体验中使用的创意：

         * 对于[!DNL Creative]将托管的创意，请上传它们。<!-- Add x-ref and reword if necessary to cover all cases -->

         * 对于在受支持的第三方广告服务器上托管的创意，[指向创意文件](/help/creative/creative-libraries/creative-third-party-manage.md)。

      1. （可选）[将创意分组为包](/help/creative/creative-libraries/bundle-manage.md)，您可以一步将这些包附加到体验中。

      1. 将创意和可选广告目标序列为[广告体验](/help/creative/experiences/experience-about.md)。<!-- maybe change x-ref once that chapter is done -->

     广告目标可以包括重新定位您在[!DNL Creative]中创建的像素；您在Adobe Experience Cloud中的受众区段(包括在DSP、Audience Manager或[!DNL Analytics]中)；地理目标；或网页上的特定数据触发器(如SKU=01234567890123或Cart=empty)。&lt;！ — 我看不到可用的受众区段，并且看到Radius目标（不起作用），但看不到其他地理目标 — 请验证所有这些受众区段。—>

1. 为广告体验设置转化跟踪：


设置转化跟踪。 根据实施，这可能涉及添加
广告商网页的转化跟踪标记和/或设置每天
广告商已单独收集的转化数据的馈送拖放区域。


您可以在Advertising Cloud中生成Advertising Cloud转化跟踪标记
在Adobe动态标签管理器（以前称为动态标签管理器）中搜索或。
注意：您必须使用JavaScript转换标记，而不是图像标记。


广告商的IT部门或其他组可能需要安排或通知您
关于，标记部署。


（可选）在Advertising Cloud Search中进行每次转换（事务属性）
作为数据视图和报告中的单个列集提供。


Advertising Cloud Search转换（交易属性）在
已跟踪至少一个转化事件。


如果您没有提供特定量度，则会合并所有转化
在一个“转化”列集中。


验证跟踪的数据。


（可选）设置将计划报表传递到指定的电子邮件地址。


有关说明，请参阅有关“报表”的帮助章节。


在Advertising Cloud DSP或其他DSP上设置广告营销活动，并提供JavaScript
或广告商广告体验的iframe标记，广告商可以将其实施为
DSP中的第三方广告。


监控已完成的广告体验的性能（查看预定义的）
单个体验或创建自定义性能报表的性能详细信息。


（根据需要）根据性能和更新的消息传递更新广告体验。






>[!MORELIKETHIS]
>
>* [关于Adobe Advertising Creative](/help/creative/introduction/creative-about.md)
>* [用户界面的组织方式](/help/creative/introduction/ui.md)
