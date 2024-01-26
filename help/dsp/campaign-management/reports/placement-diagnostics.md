---
title: 查看放置诊断报告
description: 了解如何诊断投放位置设置和步调的问题。
feature: DSP Placements
exl-id: 95e88c9c-09f2-44f1-9d6c-3fe533963f9a
source-git-commit: 61ca25565e09bbce505d6f5cb0e5e8b7214eb1e0
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# 查看放置诊断报告

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

活动开始后，以下工具可以帮助您诊断投放位置设置和步调问题：

* **[!UICONTROL Change Log]：** 显示对关键位置设置（如名称、状态和最高出价）的更改。 每个条目都包含进行更改的人员的日期和用户名。
* **[!UICONTROL Ad Approvals]：** 显示广告是已被清单提供商批准或拒绝。 您可以选择更改任何广告的状态（例如，暂停被拒绝的广告）或打开广告设置。
* **[!UICONTROL Non Bids]：** 显示DSP未对投放位置竞价的原因。

1. 打开“Diagnostics（诊断）”报告：
   1. 打开版面设置：
      1. 在主菜单中，单击 **[!UICONTROL Campaigns]**.
      1. 单击营销活动的名称，然后单击 **[!UICONTROL Placements]**.
      1. 在版面名称旁边，单击  **[!UICONTROL ...]** > **[!UICONTROL Edit]**.
   1. 在右上角，单击 ![投放位置诊断](/help/dsp/assets/placement-diagnostics.png).
1. 执行以下任一操作：
   * 要查看更改日志，请执行以下操作：
      1. 单击 **[!UICONTROL Change Log]**.
      1. （可选）筛选报表结果：
         * 在日期菜单中，将报告期间从默认的“最近14天”更改为另一个期间(*[!UICONTROL Last 30 days]，* *[!UICONTROL Last 60 days]，* *[!UICONTROL Last 90 days]，* 或 *[!UICONTROL Last 1 year]*)。
         * 在左侧菜单中，按特定用户名筛选报表。
         * 在右侧菜单中，按特定放置设置筛选报表。
   * 要查看广告审批的状态，请执行以下操作：
      1. 在右上角，单击 **[!UICONTROL Ad Approvals]**.
      1. （可选）要暂停或激活广告，请单击状态切换(![状态切换](/help/dsp/assets/status-switch.png))。
      1. （可选）要打开广告设置，请单击 **[!UICONTROL View Ad]** 在广告旁边。
   * 要了解DSP为什么没有对投放位置出价：
      1. 在右上角，单击 **[!UICONTROL Non Bids]**.
      1. （可选）要更改日期范围，请单击日期字段，然后选择不同的日期或日期范围。

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* [关于Campaign Management视图中的性能报表](campaign-reports-about.md)
>* [查看职位安排预测报表](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [投放设置](/help/dsp/campaign-management/placements/placement-settings.md)
