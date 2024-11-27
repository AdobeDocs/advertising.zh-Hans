---
title: 收集要在Adobe Customer Journey Analytics中使用的AMO ID和EF ID的历史数据
description: 了解如何在Adobe Analytics中收集保留变量的历史数据，以便将来在Adobe Customer Journey Analytics中使用
feature: Integration with Adobe Analytics
source-git-commit: 4cd58fd995b3df9fb7837077108207ce910157c1
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# 收集要在Adobe Customer Journey Analytics中使用的AMO ID和EF ID的历史数据

*仅包含[!DNL Analytics for Advertising]和Adobe Customer Journey Analytics的广告商*

如果您使用保留的变量捕获[AMO ID和EF ID](ids.md)以进行[!DNL Analytics for Advertising]集成，那么通过尽快将您为AMO ID和EF ID保留的变量复制到[standard [!DNL eVars]](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/evar)中，您可以为Adobe Advertising与Adobe的新一代[!DNL analytics]解决方案[Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview)之间的未来集成做准备。 这样一来，您便可以在完成任务后立即收集AMO ID和EF ID的历史数据。 如果您使用保留的变量并且需要完成此任务，您的Adobe客户团队将告知您。

<!-- You can also do the same for any other reserved variables you use for your [!DNL Analytics for Advertising] implementation. -->

<!-- This will allow Adobe Experience Platform, which supplies data to Customer Journey Analytics, to begin collecting historical data for your [!DNL rVars] as soon as you complete the task. -->

## 为何需要收集历史数据以进行Customer Journey Analytics？

通过Customer Journey Analytics，您可以将数据从Adobe Experience Platform同步到Adobe Analytics Analysis Workspace。 目前，要Experience Platform的[!DNL Analytics Data Connector]不将保留变量的数据从[!DNL Analytics]发送到Experience Platform。 因此，由保留变量捕获的AMO ID和EF ID当前在Customer Journey Analytics中不可用。 <!-- Instead, XXXXXXXXXX what exactly? -->.<!-- Does the Analytics for Advertising implementation use the Analytics Data Connector in particular (why would it use anything?), and we're planning to implement the Web SDK to do it instead in the future? -->

Adobe Advertising正在规划未来的Customer Journey Analytics实施。 在发布实施后，您的[!DNL Analytics for Advertising]集成仍需要您使用[!DNL Analytics]跟踪收集点进数据和(DSP用户)浏览数据，但如果您的组织同时拥有这两个产品，则可以同时在1\) [!DNL Analytics] <!-- (Analysis Workspace using data from [!DNL Analytics]) -->和2\)Customer Journey Analytics<!-- (Analysis Workspace using data from Experience Platform)-->中查看您的数据。 在发布该功能后，Experience Platform将开始收集用于Customer Journey Analytics的AMO ID和EF ID数据，但发布日期之前的历史数据将不存在。

但是，您可以通过创建一个简单的[[!DNL Analytics] 处理规则](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules)来立即将您的AMO ID和EF ID <!-- [!DNL rVars] -->复制到[!DNL eVars]中，从而更快地开始收集AMO ID和EF ID <!-- [!DNL rVars] -->的数据。 一旦创建处理规则，您就会开始为AMO ID和EF ID <!-- [!DNL rVars] -->在跟踪新事件时积累数据。 实施完成后，历史数据即可在Customer Journey Analytics中使用。

>[!NOTE]
>
>处理规则仅应用于收到的新数据。 它们不能回溯收集过去的数据。

## 将您为AMO ID和EF ID保留的变量复制到[!DNL eVars]

此步骤是手动的，并且必须为跟踪您预计将来与Adobe Advertising集成的AMO ID和EF ID <!-- [!DNL rVars] -->的每个报表包完成。

1. [使用以下设置创建处理规则](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules)：

   * 选择要将AMO ID和EF ID <!-- [!DNL rVar] -->数据迁移到Experience Platform以供Customer Journey Analytics使用的报表包。

   * 对于[!UICONTROL Rule Title]，请使用描述性名称，如“将AMO ID和EF ID复制到eVar”。

   * 在[!UICONTROL Always Execute]部分中，添加两个操作以创建新的eVar：

      * 对于`AMO ID`： ```Overwrite value of <new/unused eVar> with amo.s_kwcid(Context Data)```

      * 对于`EF ID`： ```Overwrite value of <new/unused eVar> With amo.ef_id(Context Data)```

   * 对于[!UICONTROL Reason for rule]，请使用描述性说明，如“将通过Adobe Analytics Connector将AMO ID和EF ID传输到AEP”。

1. 验证保存的处理规则。

   保存处理规则后，`AMO ID`和`AMO EF ID` <!-- the existing reserved variables -->的数据应与它们复制到的两个新eVar的数据相同。

   例如，如果新eVar`eVar142`映射到`amo.s_kwcid(Context Data)`，则`eVar142`和`AMO ID`的数据应相同。

有关如何应用处理规则的更多信息，请参阅[处理规则的工作方式](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/processing-rules-about)。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)