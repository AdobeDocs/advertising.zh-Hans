---
title: Customer Journey Analytics中的Adobe Advertising数据疑难解答
description: 了解如何对Customer Journey Analytics中的Adobe Advertising数据问题进行故障排除和解决。
feature: Integration with Adobe Customer Journey Analytics
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: b1904d5c8dad3e935245b45ff4b1a8104fc897dd
workflow-type: tm+mt
source-wordcount: 716
ht-degree: 0%

---

# Customer Journey Analytics中的Adobe Advertising数据疑难解答

以下是潜在的数据问题及其原因。

## 摘要报告

+++ Customer Journey Analytics中没有可用于Advertising DSP或Advertising Search、Social和Commerce的摘要报表数据。

验证以下内容：

* Customer Journey Analytics Workspace引用了正确的数据视图。

* 从Adobe Advertising到Customer Journey Analytics的信息源已启用。 请与您的Adobe客户团队核实。

* 您的Adobe Advertising维度/分类/查找数据集和摘要数据集包含在您的Customer Journey Analytics连接中。

* 您的Adobe Advertising维度和摘要量度包含在您的Customer Journey Analytics数据视图中。

如果您已验证上述所有设置，但仍看不到摘要数据，请在[https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support)为您的组织打开支持工单。

+++

+++ 摘要报表数据在Customer Journey Analytics中可用于广告商1，但不能用于广告商2。

验证以下内容：

* 已为广告商2启用从Adobe Advertising到Customer Journey Analytics的馈送。 请与您的Adobe客户团队核实。

* 在Customer Journey Analytics连接中，为三个数据集（维度/分类/查找、摘要和事件量度）启用了设置“[!UICONTROL Backfill all existing data]”。

如果您验证了上述所有条件，但仍看不到摘要数据，请在[https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support)为您的组织打开支持工单。

+++

+++ （搜索、社交和Commerce用户）汇总报表数据在Customer Journey Analytics中可用于一个[!DNL Google Ads]、[!DNL Meta Ads]或[!DNL Microsoft Advertising]帐户，但不能用于另一个帐户。

验证是否已为特定的广告网络帐户启用从Adobe Advertising到Customer Journey Analytics的馈送。 请与您的Adobe客户团队核实。

如果为某个帐户启用了信息源，但仍看不到摘要数据，请在[https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support)为您的组织打开支持工单。 包含广告网络帐户的[!UICONTROL Account ID]。

+++

+++ Customer Journey Analytics Workspace中的摘要报表数据不同于Advertising DSP或Advertising Search、Social和Commerce中的数据，或者缺少某些营销活动和营销活动实体的摘要数据。

验证以下内容：

* 您在[!DNL Workspace]和Adobe Advertising报表中使用相同的日期范围。

* 在[!DNL Workspace]和Adobe Advertising报表中应用的任何过滤器和区段都不会导致数据差异。

* Customer Journey Analytics数据视图的[!UICONTROL Time Zone]与您的Advertising DSP帐户[&#128279;](help/dsp/admin/user-own-profile-edit.md)的[!UICONTROL Default Timezone]匹配。

* 在Customer Journey Analytics连接中，为三个数据集（维度/分类/查找、摘要和事件量度）启用了设置“[!UICONTROL Backfill all existing data]”。

如果确定数据不一致，请在[https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support)为您的组织打开支持工单。 包含广告网络帐户的[!UICONTROL Account ID]。. 包括屏幕截图和电子表格，以显示差异的证据。 如果需要，您的Adobe客户团队可以追溯修复数据馈送以解决差异。

+++

## 事件级报告

+++ 在CJA Customer Journey Analytics Workspace中，转化数据（如`Page Views`）不可用于报表维度（如`Campaign`）。

验证以下内容，从验证障碍最少的物品开始：

* 您使用了正确的数据视图。

* 适用的转化量度是Web/在线事件，Adobe Advertising可将这些事件归因于维度。

* Adobe Advertising正在跟踪适用网站上的点进和显示点进。<!-- Link to validation instructions in the user guide -->

* 在分类数据集的Customer Journey Analytics连接中，[!DNL Key]和[!DNL Matching Key]设置的值正确： [!DNL Key]： `Tracking Code` (_customername.adLens2.trackingCode)，[!DNL Matching Key]： `Tracking Code` (event._experience.adcloud.conversionDetails.trackingCode)

* [!DNL Adobe Advertising]服务已添加到Adobe Experience Platform数据流，数据流的映射架构为`XDM ExperienceEvent Schema`，字段组`Adobe Advertising Cloud ExperienceEvent Full Extension`已添加到`XDM ExperienceEvent`架构中。

* 已在WebSDK扩展中正确配置并发布Adobe Advertising设置。

如果您已验证上述所有设置，但仍看不到转化数据，请在[https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support)为您的组织打开支持工单。 包含广告网络帐户的[!UICONTROL Account ID]。

+++


<!--

+++ Question

Answer

+++

+++ Question

Answer

+++

+++ Question

Answer

+++

-->

>[!MORELIKETHIS]
>
>* [概述](overview.md)
>*  [!DNL Customer Journey Analytics][&#128279;](ids.md)使用的Adobe Advertising ID
>* [先决条件](prerequisites.md)
>* [设置数据收集、数据传输和报告](set-up.md)
>* Customer Journey Analytics中的[Adobe Advertising指标和维度](advertising-data-in-cja.md)
>* （Adobe Analytics用户） [收集AMO ID和EF ID的历史数据以用于Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md)。
