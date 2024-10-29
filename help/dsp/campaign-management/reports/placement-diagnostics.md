---
title: 查看放置诊断报告
description: 了解如何诊断投放位置设置和步调的问题。
feature: DSP Placements
exl-id: 95e88c9c-09f2-44f1-9d6c-3fe533963f9a
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# 查看放置诊断报告

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

诊断报告可以帮助您诊断投放位置设置和活动开始后的步调问题。

## 放置诊断报告中的信息

* **[!UICONTROL Change Log]：**&#x200B;显示对密钥放置设置的更改，如名称、状态和最高出价。 每个条目都包含进行更改的人员的日期和用户名。

* **[!UICONTROL Ad Approvals]：**&#x200B;显示清单提供商是批准或拒绝广告。 您可以选择更改任何广告的状态（例如，暂停被拒绝的广告）或打开广告设置。

* **[!UICONTROL Non Bids]：**&#x200B;显示DSP未对投放位置出价的原因。

## 打开放置诊断报告

1. 打开“Diagnostics（诊断）”报告：

   1. 打开版面设置：

      1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

      1. 单击营销活动的名称，然后单击&#x200B;**[!UICONTROL Placements]**。

      1. 在投放位置名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit]**。

   1. 单击右上角的![放置诊断](/help/dsp/assets/placement-diagnostics.png)。

1. 执行以下任一操作：

   * 要查看更改日志，请执行以下操作：

      1. 单击&#x200B;**[!UICONTROL Change Log]**。

      1. （可选）筛选报表结果：

         * 在日期菜单中，将报告时段从默认的“最近14天”更改为其他时段（*[!UICONTROL Last 30 days]、* *[!UICONTROL Last 60 days]、* *[!UICONTROL Last 90 days]、*&#x200B;或&#x200B;*[!UICONTROL Last 1 year]*）。

         * 在左侧菜单中，按特定用户名筛选报表。

         * 在右侧菜单中，按特定放置设置筛选报表。

   * 要查看广告审批的状态，请执行以下操作：

      1. 单击右上角的&#x200B;**[!UICONTROL Ad Approvals]**。

      1. （可选）要暂停或激活广告，请单击广告列中的状态开关（![状态开关](/help/dsp/assets/status-switch.png)）。

      1. （可选）要打开广告设置，请单击广告旁边的&#x200B;**[!UICONTROL View Ad]**。

   * 要了解DSP为什么没有对投放位置出价：

      1. 单击右上角的&#x200B;**[!UICONTROL Non Bids]**。

      1. （可选）要按特定的私人交易目标过滤投放位置，请选择该交易。<!-- Admin users only: Optionally filter the deal by one or more regions ([!UICONTROL US-EAST], [!UICONTROL US-WEST]) [!UICONTROL EU-WEST], [!UICONTROL HKG]) by selecting the regions. -->

      1. （可选）要更改日期范围，请单击日期字段，然后选择不同的日期或日期范围。

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* Campaign Management视图中的[性能报告类型](campaign-reports-about.md)
>* [查看投放预测报告](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [位置设置](/help/dsp/campaign-management/placements/placement-settings.md)
