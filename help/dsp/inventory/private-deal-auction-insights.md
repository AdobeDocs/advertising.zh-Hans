---
title: 查看私人交易的拍卖分析
description: 了解如何使用拍卖见解分析私人交易的交易组成。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: bbb99f6a-0276-4eb8-9607-75500d5634d9
source-git-commit: 61ca25565e09bbce505d6f5cb0e5e8b7214eb1e0
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# 查看私人交易的拍卖分析

Auction Insights是一种故障排除工具，可用于分析有保证的和无保证的私人交易的交易组成。 通过使用数据可视化，此工具显示针对以下各项接收的值的趋势和相对比例 [关键拍卖属性](#auction-attributes) 在特定时间段内。

1. 在主菜单中，单击 **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. 在交易行中，单击  **[!UICONTROL ...]** > **[!UICONTROL Auction Insights]**.

>[!NOTE]
>
>Auction Insights也可通过投放位置获取 [!UICONTROL Inspector] 工具。 要打开它们， [打开投放位置 [!UICONTROL Inspector]](/help/dsp/campaign-management/reports/placement-details-view.md) 到 [!UICONTROL Inventory tab]，然后单击 **[!UICONTROL ...]** > **[!UICONTROL Auction Insights]** 在交易大战中。

## 拍卖属性 {#auction-attributes}

面积图可用于以下拍卖属性：

* **广告类型：** 拍卖中请求的广告类型（如“显示”或“音频”）。

* **浏览器：** 拍卖源自的浏览器（如Chrome或Firefox）。

* **操作系统：** 拍卖源自的操作系统(OS)(例如Android或iOS)。

* **设备类型：** 拍卖源自的设备（例如手机或桌面）。

* **广告持续时间：** 拍卖中请求的最大广告持续时间（例如15秒或30秒）。

* **安全：** 表示拍卖是否需要安全的HTTPS URL创意资产。 值： <i>安全</i> 或 <i>不安全</i>.

* **Mime类型：** 拍卖中请求的广告创意MIME类型（如mp4或mov）。

![拍卖见解](/help/dsp/assets/auction-insights.png)

>[!NOTE]
>
>您可以为特定属性值应用过滤器以缩小结果范围。

>[!MORELIKETHIS]
>
>* [关于专用清单](private-inventory-about.md)
>* [指定交易ID的投放位置和广告](deal-id-attach-placements.md)
>* [查看交易的详细报告](deal-view-report.md)
>* [关于Campaign Management视图中的性能报表](/help/dsp/campaign-management/reports/campaign-reports-about.md)
