---
title: 收集要在Adobe Customer Journey Analytics中使用的AMO ID和EF ID的历史数据
description: 了解如何在Adobe Analytics中收集保留变量的历史数据，以便将来在Adobe Customer Journey Analytics中使用
feature: Integration with Adobe Analytics
exl-id: 1f8fa139-f146-426b-b0c4-079f8e2de56c
source-git-commit: c1701505be0a1efa6db15edcf21adf80880bad8b
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 0%

---

# 收集要在Adobe Customer Journey Analytics中使用的AMO ID和EF ID的历史数据

*仅包含[!DNL Analytics for Advertising]和Adobe Customer Journey Analytics的广告商*

<!-- Solution built but not tested. Move to the CJA chapter once it's available?  If so, then create a redirect. -->

如果使用保留变量捕获[集成的](ids.md)AMO ID和EF ID[!DNL Analytics for Advertising]，则可以通过尽快将保留的AMO ID和EF ID变量复制到[standard](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview)[!DNL analytics]中，为Adobe Advertising与[Adobe Customer Journey Analytics [!DNL eVars]&#x200B;(Adobe的新一代](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/evar)解决方案)之间的集成准备数据。 这样一来，您便可以在完成任务后立即收集AMO ID和EF ID的历史数据。 如果您使用保留的变量并且需要完成此任务，您的Adobe客户团队将告知您。

<!-- You can also do the same for any other reserved variables you use for your [!DNL Analytics for Advertising] implementation. -->

<!-- This will allow Adobe Experience Platform, which supplies data to Customer Journey Analytics, to begin collecting historical data for your [!DNL rVars] as soon as you complete the task. -->

## 为什么需要收集Customer Journey Analytics的历史数据？

Customer Journey Analytics允许您将数据从Adobe Experience Platform同步到[!DNL Workspace]。 目前，发送到Experience Platform的[!DNL Analytics Data Connector]不会将保留变量的数据从[!DNL Analytics]发送到Experience Platform。 因此，由保留变量捕获的AMO ID和EF ID数据在Customer Journey Analytics中不可用。 <!-- Instead, XXXXXXXXXX what exactly? -->.<!-- Does the Analytics for Advertising implementation use the Analytics Data Connector in particular (why would it use anything?), and we're planning to implement the Web SDK to do it instead in the future? -->

Adobe Advertising正在构建一个解决方案，以自动将数据发送到Customer Journey Analytics。 发布解决方案后，Adobe Advertising将开始发送您的AMO ID和EF ID的数据以供在Customer Journey Analytics中使用，但发布日期之前的历史数据将不存在。

但是，您可以通过创建一个简单的<!-- [!DNL rVars] -->处理规则[[!DNL Analytics] 来立即将您的AMO ID和EF ID ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules)复制到<!-- [!DNL rVars] -->中，从而更快地开始收集AMO ID和EF ID [!DNL eVars]的数据。 一旦创建处理规则，您就会开始为AMO ID和EF ID <!-- [!DNL rVars] -->在跟踪新事件时积累数据。 解决方案可用后，历史数据即可在Customer Journey Analytics中使用。

>[!NOTE]
>
>* 截至2025年2月28日，此过程会跟踪点进数据，但不跟踪点进数据。
>* 处理规则仅应用于收到的新数据。 它们不能回溯收集过去的数据。

## 将您为AMO ID和EF ID保留的变量复制到[!DNL eVars]

此步骤是手动的，并且必须为跟踪您预计将来与Adobe Advertising集成的AMO ID和EF ID <!-- [!DNL rVars] -->的每个报表包完成。

1. [使用以下设置创建处理规则](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules)：

   * 选择要将AMO ID和EF ID <!-- [!DNL rVar] -->数据迁移到Experience Platform以供Customer Journey Analytics使用的报表包。

   * 对于[!UICONTROL Rule Title]，请使用描述性名称，如“将AMO ID和EF ID复制到eVar”。

   * 在[!UICONTROL Always Execute]部分中，添加两个操作以创建新的eVar：

      * 对于`AMO ID`：

         1. 选择&#x200B;**覆盖**&#x200B;的值。
         1. 选择&#x200B;*\&lt;新的/未使用的eVar\>*。
         1. 选择&#x200B;**查询字符串参数**。
         1. 输入`s_kwcid`。

        示例： ```Overwrite the value of rVar10 with Query String Parameter s_kwcid```

      * 对于`EF ID`：

         1. 选择&#x200B;**覆盖**&#x200B;的值。
         1. 选择&#x200B;*\&lt;新的/未使用的eVar\>*。
         1. 选择&#x200B;**查询字符串参数**。
         1. 输入`ef_id`。

        示例： `Overwrite the value of rVar11 with Query String Parameter ef_id`

   * 对于[!UICONTROL Reason for rule]，请使用描述性说明，如“将通过Adobe Analytics Connector将AMO ID和EF ID传输到AEP”。

1. 验证保存的处理规则。

   保存处理规则后，`AMO ID`和`AMO EF ID` <!-- the existing reserved variables -->的数据应与它们复制到的两个新eVar的数据相同。

   例如，如果新eVar `eVar142`映射到`amo.s_kwcid(Context Data)`，则`eVar142`和`AMO ID`的数据应相同。

有关如何应用处理规则的更多信息，请参阅[处理规则的工作方式](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/processing-rules-about)。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
