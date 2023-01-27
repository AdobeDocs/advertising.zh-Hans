---
title: 设置效果促销活动的最佳实践
description: 了解设置注重效果的促销活动的最佳实践，包括针对最低CPA或最高ROAS优化的版面。
feature: DSP Optimization, DSP Best Practices
exl-id: bc297796-0c89-4d91-87aa-0668462526ae
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '1247'
ht-degree: 0%

---

# 设置效果促销活动的最佳实践

DSP可以通过最低的每次客户获取成本(CPA)或最高的广告支出回报(ROAS)，为投放优化注重效果的促销活动。

请参阅以下效果促销活动的最佳实践：

* 步骤1 — 定义目标
* 步骤2 — 定义策略
* 步骤3 — 创建资源包
* 步骤4 — 创建版面结构
* 步骤5 — 使用正确的创意资产

## 步骤1 — 定义目标

了解营销活动的目标是实现尽可能高的ROAS还是尽可能低的CPA，这一点很重要。 对于营销活动中的每个包，您将相应地指定目标目标，如 *[!UICONTROL Highest ROAS - Custom Goal]* 或 *[!UICONTROL Lowest CPA - Custom Goal]*.

![优化目标](/help/dsp/assets/optimization-goals.png)

您还需要确定将导致整体目标的成功事件，并相应地创建自定义目标。 对于每个包，您将指定一个自定义目标，以与使用的报表和算法优化的整体优化目标一起使用 [!DNL Adobe Sensei]. 有关创建自定义目标的更多信息，请参阅 [构建自定义目标的最佳实践](custom-goal-best-practices.md).

![自定义目标](/help/dsp/assets/objective-goals.png)

## 步骤2 — 定义策略

### 潜在客户策略

上漏斗包包括具有非常广泛定位以接触到净新客户的位置。

#### 潜在客户推荐的放置策略

* 使用以下策略查找可能进行转化的新受众：

   * 从数据管理平台(DMP)(如Adobe Audience Manager)进行相似人群拓展建模。
   * 使用第三方数据的行为定位。
   * 情境定位。
   * 网站/类别定位。

* 使用网络(RON)定位：在没有受众定位和广泛库存定位的情况下运行网络投放非常重要。 这允许 [!DNL Adobe Sensei] 算法来查找可能拥有尚未分类到受众的较新cookie的有价值用户。

### 重定位策略

较低的漏斗包包括定位已访问广告商网页或广告商拥有CRM数据的用户的位置。

#### 用于重定位的推荐版面策略

* 如果广告商是Adobe Analytics或Adobe Audience Manager客户，则您可以构建第一方区段（例如主页访客、产品页面或购物车放弃者），并将它们用作DSP中的版面目标。

* 避免为定向受众的版面分配过多预算。 一般情况下，每月每1 000个用户预算30美元。

## 步骤3 — 创建资源包

最佳做法是为上漏斗潜在客户和下漏斗重定位创建单独的包。 优化在包级别进行，以便池化包内所有版面的性能数据。 因此，可将版面分组到具有相似预期效果的包中。

![用于发现客户和重新定位的单独包示例](/help/dsp/assets/p-r.png)

此外，还可以使用以下设置。

### 目标和预算

* **步调和上限：** 要选择CPA或ROAS优化目标，包必须使用包级别步调。 这可确保优化包内的所有版面，以根据绩效和规模来分配支出，从而达到选定的目标。

* **投放日期：** （潜在客户包）当您的营销活动运行时间超过25天时，请使用 [!UICONTROL Activate Custom Flighting] 功能。 首先，将前10天的定制航班定为所需每日预算的75%左右，以减少在 *学习阶段*. 然后在预算的剩余时间设置第二次自定义飞行。

   例如，如果您有$100,000的时间在30天内花费，则将第1次飞行（第1-10天）的预算设置为$25,000(75% x 100,000/30天= $2,500每天)。 用剩余预算75 000美元用于2号航班（第11-30天）。

* **预算：** DSP将始终尝试在包中的所有版面之间平均分配100%的包预算。 如果职位安排的支出较低或没有支出，我们建议为职位安排设置预算上限，以允许将更多预算按比例分配给职位安排。 允许24-48小时进行预算更改校准。

* **优化目标：** 使用以下两个性能优化目标之一： *[!UICONTROL Highest ROAS]* 或 *[!UICONTROL Lowest CPA]*，具体取决于包目标。 这些目标可分别针对最高ROAS或最低CPA版面自动优化资源包。

* **自定义目标：**
   * 如果新包的目标与现有包相同，则可以选择链接现有包，以便算法可以使用现有的机器学习数据。
   * 输入相应的 [!UICONTROL Target CPA] 或 [!UICONTROL Target ROAS].

* **飞行步调和当天步调：** 对于这两种步调类型，请选择 *[!UICONTROL Even]* 通过在每天和整个飞行中都以一致的步调来最大限度地实现您的性能目标。

   >[!CAUTION]
   >
   >使用 *[!UICONTROL FrontLoad]* 和 *[!UICONTROL Aggressive Front Load]* 飞行步调和 *[!UICONTROL ASAP]* 只有在您完全确定交付优先级并将精力花在性能优化上时，才会开始进行当天的步调调整，因为这些策略可能会对您期望的性能KPI产生负面影响。

## 步骤4 — 创建版面结构

少就是多。 如果您每个包的版面数量少于6个，则可用预算可以最轻松地动态转移到性能最佳的版面。

此外，请确保将每个版面添加到包中，其包目标类型为 *[!UICONTROL Prospecting]* 或 *[!UICONTROL Retargeting]*，视情况而定。

以下是效果促销活动的推荐版面设置。

### 目标

您将在包级别配置CPA或ROAS优化（请参阅步骤3 — 创建包），但可以添加其他版面级别设置。

* **最高竞价：**
   * 要寻找潜在客户，请使用低的最高竞价（5美元）。
   * 对于重定位投放，请使用高最高竞价（12美元）。

* **竞价前过滤器：** 最大限度地减少或最好地避免设置激进的预出价过滤器，从而阻止投放达到规模。 最佳实践包括：

   * 在每次投放中使用一(1)个竞价前过滤器。 多个竞价前过滤器要求同时满足这两个条件，这降低了规模。

   * 如果应用了其他定位（如受众、地域和网站定位），请考虑设置不那么严格的竞价前过滤器。

请参阅有关何时在 [版面级别的预竞价过滤器及其使用方法](/help/dsp/optimization/optimization-pre-bid-filters.md).

### 库存

要实现最大规模，请使用 [!UICONTROL Public] (Open Exchange)和 [!UICONTROL On Demand] 库存。

### 网站定位

* **[!UICONTROL Traffic Type]**: [!UICONTROL Websites] 仅
* **[!UICONTROL Site Tier]**: [!UICONTROL All sites]

### 受众定位

<!-- Say something about limiting unnecessary constraints/limitations, including dayparting, which limit your chances for ad exposure. Use only when it's required for your audience. -->

* **[!UICONTROL Included Audiences]:**
   * 对于潜在客户投放，将相似受众类别和相似受众规模分组到一个位置。 然后，根据性能，执行以下操作之一：
      * 从现有版面中删除表现不佳的受众。
      * 将表现最佳的受众移入单独的版面，以更好地控制预算。
   * 对于重定位投放，理想情况下，您应该在每个投放中包含一个受众区段，以便轻松控制竞价和预算。

>[!NOTE]
>
>如果用户只能通过一次版面访问，则您的广告效果最佳。 不同版面中用户的大量重叠可能会导致竞争，从而产生一个不断增加竞价的周期，从而提高每个用户的成本。 因此，如果您包含多个受众，请确保这些受众不是由重叠的用户/受众成员组成。
>
> 您可以通过在层中创建受众来避免重叠的受众，以便根据需要从版面中抑制更高、更包容的层。

* **[!UICONTROL Frequency Capping]:**
   * 要寻找潜在客户，请使用严格的频率上限（每天一次展示）。
   * 对于重定位版面，请将主要版面的上限设置为每天6-10次展示次数，将次要上限设置为每小时一次展示次数。

* **[!UICONTROL Device Targeting]**:
   * 包括 [!UICONTROL Computer], [!UICONTROL Mobile]和 [!UICONTROL Tablet].
   * 不定位 [!UICONTROL Firefox] 和 [!UICONTROL Safari] 因为定位和测量限制。 联系您的 [!DNL Adobe] 帐户团队以了解有关 [!DNL Adobe] 支持 [!DNL Safari ITP].
   * 如果您定位移动Web流量，则应禁用除 [!UICONTROL Chrome] 和 [!UICONTROL Edge].

### 品牌安全与媒体质量

使用情境过滤、投标前欺诈阻止和/或 [!UICONTROL Ads.txt] 筛选将限制您的投放规模，但会根据需要使用。

## 步骤5 — 使用正确的创意资产

* 最佳做法是尽可能多地包含独特广告大小，以最大限度地扩大访问范围。 通用显示模板允许您上传任何标准的显示广告大小。
* 确保所有版面都包含 *至少* 所有主显示广告大小（300x250、728x90、160x600、300x600、320x50和300x50）。
* 经常更新创意内容，以防止创作疲劳。

>[!MORELIKETHIS]
>
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
>* [版面设置](/help/dsp/campaign-management/placements/placement-settings.md)
> * [DSP如何优化您的营销活动](optimization-how-dsp-optimizes-campaigns.md)
>* [优化目标及其使用方法](optimization-goals.md)
>* [版面级别的预竞价过滤器及其使用方法](optimization-pre-bid-filters.md)
>* [营销活动启动核对清单](/help/dsp/campaign-management/campaign-launch-checklist.md)

