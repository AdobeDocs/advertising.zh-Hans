---
title: 关于受众
description: 了解用于跟踪、创建和管理 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 受众的选项。
exl-id: f85cbc82-ddbc-4ecd-a17b-b4cb4808cfbc
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# 关于管理Search、Social和Commerce中的[!DNL Google Ads]和[!DNL Microsoft Advertising]受众

仅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]*

受众库列出了您的所有[!DNL Google Ads]个基于客户数据的市场内和类似受众，以及[!DNL Microsoft Advertising]再营销和动态再营销、自定义、客户匹配、市场内和类似受众。 您可以将[!DNL Google Ads]受众中的任意受众用作[!DNL Google Ads]营销活动级别和广告组级别的目标和排除项，并将[!DNL Microsoft Advertising]受众中的任意受众用作[!DNL Microsoft Advertising]营销活动级别和广告组级别的目标和（仅限动态二次营销受众）排除项。 您可以添加或编辑任何受众目标的竞价调整。

您还可以使用现有Adobe Experience Cloud受众中的区段或电子邮件列表，以及客户关系管理(CRM)系统中的各种客户数据，来创建和管理受众：

* **Adobe受众区段：**&#x200B;选择启用Adobe Audience Manager或Adobe Analytics帐户的广告商可以从其[!DNL Adobe]区段创建[!DNL Google Ads]客户匹配受众：

   * (具有[!DNL Analytics]个帐户的广告商也不具有Audience Manager)您可以使用与Adobe Experience Cloud共享的[!DNL Analytics]区段中的用户ID创建[!DNL Google Ads]个客户匹配受众。

   * (具有Audience Manager帐户的广告商)您可以使用用户ID创建[!DNL Google Ads]个客户匹配受众，这些Audience Manager来自将Search、Social和Commerce作为目标的用户区段。 这可能包括发布到Adobe Experience Cloud的Adobe Analytics区段和使用Adobe Experience Cloud受众库创建的区段。

  要创建客户匹配受众，广告商的[!DNL Google Ads]帐户必须[符合自定义匹配条件](https://support.google.com/adspolicy/answer/6299717)并选择加入[用户ID区段](https://support.google.com/google-ads/answer/9199250)。 此外，必须将Search、Social和Commerce中的广告商帐户配置为允许创建客户匹配受众。

  基于客户数据的受众的[!DNL Adobe]区段数据和Cookie同步文件每天同步到[!DNL Google Ads]。

* **Adobe Campaign电子邮件列表：**&#x200B;您的Adobe客户团队可以帮助您设置工作流，以从[!DNL Campaign]内的电子邮件列表中创建和更新[!DNL Google Ads]客户匹配受众。

* **客户数据列表：**&#x200B;具有[!DNL Google Ads]或[!DNL Microsoft Advertising]帐户且符合客户匹配条件的广告商可以创建和更新特定于广告网络的基于客户数据的受众&lt;！ — 或动态再营销受众 — 至少对于[!DNL Google Ads]？—>包含在基于客户数据的受众中，方法是上传具有主标识符的CSV文件。

* **动态二次营销列表：**&#x200B;拥有[!DNL Microsoft Advertising]帐户的广告商可以创建和管理动态二次营销受众，您可以使用这些受众通过多种方式之一重新定位最近与您的产品交互的潜在客户（如产品查看者或过去的购买者）。 动态二次营销受众要求您在网页上使用广告网络的JavaScript转化和受众跟踪标记。 将动态再营销列表与搜索和受众网络上的购物营销活动结合使用，通过产品广告重新定位受众，将动态再营销列表与搜索营销活动结合使用，通过文本广告和动态搜索广告重新定位受众。<!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >动态二次营销受众目标的竞价修饰符未在具有“[!UICONTROL Auto-optimize Bid Adjustment Values]”设置的项目组合中进行优化。

>[!NOTE]
>
>Search、Social和Commerce不会存储您上传的任何客户数据，也不会存储用于创建或编辑[!DNL Google Ads]或[!DNL Microsoft Advertising]受众的[!DNL Adobe]区段中的客户数据。

>[!MORELIKETHIS]
>
>* [创建来自 [!DNL Adobe] 受众的 [!DNL Google Ads] 客户匹配受众](google-audience-from-adobe-audience.md)
>* [从Adobe Campaign电子邮件列表创建 [!DNL Google Ads] 客户匹配受众](google-audience-from-campaign-email-list.md)
>* [使用客户数据列表管理客户匹配受众](audience-from-customer-data-list.md)
>* [管理动态再营销受众](audience-dynamic-remarketing-manage.md)
>* [管理营销活动和广告组的受众目标](audience-targets-manage.md)
>* [管理营销活动和广告组的受众排除](audience-exclusions-manage.md)
