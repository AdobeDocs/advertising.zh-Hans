---
title: 查看投放的网站、广告、频度和库存详细信息
description: 了解如何查看投放的目标网站、广告、频率和库存数据。
feature: DSP Placements
exl-id: b58b442c-2fb8-4a78-9be9-d85aa83136e2
source-git-commit: 0f022babeab6c044949760cedc103323eb0cc950
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# 查看投放的网站、广告、频度和库存详细信息

对于每个投放位置，您可以[打开（详细信息视图[!UICONTROL Inspector]）](placement-details-view.md)，其中列出了投放位置中的所有目标网站、广告和交易。 其中还包括投放的频率数据。 您可以选择从任何选项卡导出数据。

![位置检查器](/help/dsp/assets/placement-inspector.png)

## 投放位置[!UICONTROL Inspector]中的信息 {#placement-inspector}

* **[!UICONTROL Sites]：**&#x200B;投放位置具有展示的所有网站。

  [!UICONTROL Sites]选项卡包括搜索和筛选功能，与主页面上提供的标准和自定义列视图选项相同，每行有一个[!UICONTROL Exclude]按钮，以便您能够从投放位置中快速排除网站。

* **[!UICONTROL Ads]：**&#x200B;投放位置中的所有广告。

  [!UICONTROL Ads]选项卡包括搜索和筛选功能、主页上提供的相同标准和自定义列视图选项以及每行中的快速操作按钮，如[!UICONTROL View Ad Approvals]。

* **[!UICONTROL Frequency]：**&#x200B;投放位置的每个广告频率级别的数据，包括：
   * 广告频率级别（例如“1”，适用于用户一次看到广告的所有实例）
   * 在指定频率级别接收展示的预计设备/浏览器或人员唯一数量（取决于为促销活动指定的[!UICONTROL Cross Device Level]）
   * 指定频率级别的预计展示次数
   * 指定频率级别的估计平均频率。 此值等于（预计展示次数）/（预计独特次数）。

* **[!UICONTROL Inventory]：**&#x200B;有关投放位置定向的所有交易的信息。

  [!UICONTROL Inventory]选项卡通过显示性能统计信息（如[!UICONTROL Auctions]、[!UICONTROL Bids]和[!UICONTROL Win Rate]）启用快速故障排除。 该选项卡包括搜索和筛选功能、主页上提供的相同标准和自定义列视图选项，以及每行中的快速操作按钮，包括[!UICONTROL Edit]、[!UICONTROL View Report]和[[!UICONTROL Auction Insights]，用于进一步排除故障](/help/dsp/inventory/private-deal-auction-insights.md)。

## 打开[!UICONTROL Placement Inspector] {#inspector-open}

1. 打开父营销活动或包的“版面”视图：

   * 查看父营销活动中的所有版面：

      1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

      1. 单击营销活动的名称。

      1. 单击&#x200B;**[!UICONTROL Placements]**&#x200B;选项卡。

   * 查看父包中的所有版面：

      1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

      1. 单击营销活动的名称。

      1. 单击&#x200B;**[!UICONTROL Packages]**&#x200B;选项卡。

      1. 单击父包的名称。

1. 将光标悬停在放置行上，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Analyze]** > **[!UICONTROL Inspector]**。

1. （可选）[根据需要更改列视图](campaign-data-views-manage.md#column-view-change)以查看所需的量度。

1. （可选）要导出任意选项卡上的数据，请单击右上角的![更多](/help/search-social-commerce/assets/more.png "更多")，然后单击&#x200B;**[!UICONTROL Export]**。

   数据以XLSM格式作为报表保存到浏览器的默认下载文件夹中。

## 从[!UICONTROL Placement Inspector]中的投放位置删除广告 {#remove-ads-placement-inspector}

1. [打开[!UICONTROL Placement Inspector]](#inspector-open)。

1. 单击&#x200B;**[!UICONTROL Ads]**&#x200B;选项卡。

1. 在广告名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Detach]**。

## 清单疑难解答

| 问题 | 可能的原因 | 要采取的操作 |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | 发布者尚未开始发送竞价请求。 | 联系发布者以激活交易。 |
| | 交易设置不正确，例如输入错误的外部交易ID。 | 确认交易详细信息并编辑交易。 |
| [!UICONTROL Auctions but no Bids] | 投放位置定位与交易的传入竞价请求不匹配。 <br><br>例如，投放位置可能面向不符合交易条件的地理位置。 | 根据需要编辑投放位置目标，以避免定位不匹配。 |
| | 投放位置没有具有交易所需的媒体类型的活动广告。 | 创建具有正确媒体类型的广告并将其附加到投放位置。 |
| | 该职位预算不足。 | 增加投放预算以允许对传入请求投标。 |
| | 投放投放日期与交易的展示投放日期不重叠。 | 根据需要编辑投放位置的投放日期。 |
| [!UICONTROL Low Win Rate] | 投放位置的最高出价（下限或固定）低于交易要求的最低出价。 | 根据需要增加投放位置的[!UICONTROL Max Bid]。 |
| | 投放位置使用限制竞价的预竞价过滤器。 | 降低预竞价筛选器的阈值以允许进行更多竞价。 |
| | 投放的受众定位过于严格。 | 检查指定的受众目标是否有足够的活动用户，如果可能，请展开受众。 |

>[!MORELIKETHIS]
>
>* 营销活动管理视图中的[性能报表类型](campaign-reports-about.md)
>* [管理您的Campaign数据视图](campaign-data-views-manage.md)
