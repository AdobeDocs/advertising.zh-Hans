---
title: 设置效果活动的最佳实践
description: 了解设置以性能为中心的活动的最佳实践，其中包括针对最低CPA或最高ROAS而优化的投放位置。
feature: DSP Optimization, DSP Best Practices
exl-id: bc297796-0c89-4d91-87aa-0668462526ae
source-git-commit: eda0459472c1e4a8297daf69454de0fcb3d4f8ca
workflow-type: tm+mt
source-wordcount: '1255'
ht-degree: 0%

---

# 设置效果活动的最佳实践

DSP可以针对具有最低每次购买成本(CPA)或最高广告支出回报率(ROAS)的投放位置优化以性能为中心的促销活动。

请参阅以下效果促销活动的最佳实践：

* 步骤1 — 定义目标
* 第2步 — 定义您的策略
* 步骤3 — 创建包
* 步骤4 — 创建投放结构
* 步骤5 — 使用正确的创意资产

## 步骤1 — 定义目标

了解活动的目标很重要，例如实现尽可能最高的ROAS或尽可能最低的CPA。 性能营销活动具有 [优化目标](/help/dsp/optimization/optimization-goals.md) 结尾是&quot;[!UICONTROL - Custom Goal]“(如”[!UICONTROL Highest ROAS - Custom Goal]“)。 对于营销活动中的每个资源包，您将相应地指定目标目标。

![优化目标](/help/dsp/assets/optimization-goals.png)

您还需要确定将带来整体目标的成功事件并相应地创建自定义目标。 对于每个包，您将指定一个自定义目标，以便与报告和算法优化的整体优化目标一起使用 [!DNL Adobe Sensei]. 有关创建自定义目标的更多信息，请参阅 [构建自定义目标的最佳实践](custom-goal-best-practices.md).

![自定义目标](/help/dsp/assets/objective-goals.png)

## 第2步 — 定义您的策略

### 潜在客户发现策略

上层漏斗包中包含投放位置，具有非常广泛的定位以吸引净新消费者。

#### 建议的潜在客户放置策略

* 使用以下策略查找可能转化的新受众：

   * 从数据管理平台(DMP)(如Adobe Audience Manager)进行相似人群拓展建模。
   * 使用第三方数据的行为定位。
   * 上下文定位。
   * 站点/类别定位。

* 使用网络运行(RON)定位：一定要包括没有受众定位和广泛库存定位的网络放置运行。 这允许 [!DNL Adobe Sensei] 算法，用于查找具有价值、可能拥有较新Cookie但尚未分类到受众中的用户。

### 重新定位策略

下层漏斗包包括定向已访问过广告商网页或广告商具有CRM数据的用户的投放位置。

#### 推荐的重新定位放置策略

* 如果广告商是Adobe Analytics或Adobe Audience Manager客户，则您可以在DSP中构建第一方区段（例如主页访客、产品页面或购物车放弃者）并将它们用作投放目标。

* 避免为面向受众的投放分配过多的预算。 一般来说，每月每1,000个用户预算为30美元。

## 步骤3 — 创建包

最佳实践是为上部漏斗探矿和下部漏斗重新定位创建单独的包。 优化在包级别进行，因此来自包中所有版面的性能数据都将汇集在一起。 因此，会将投放分组到具有相似预期性能的包中。

![用于发现客户和重新定位的单独软件包示例](/help/dsp/assets/p-r.png)

此外，请使用以下设置。

### 目标和预算

* **步调和上限：** 要选择CPA或ROAS优化目标，包必须使用包级别的步调。 这可确保优化包中的所有版面，以根据性能和规模将支出分配到选定的目标。

* **投放日期：** （潜在客户资源包）当营销活动运行超过25天时，请使用 [!UICONTROL Activate Custom Flighting] 功能。 首先，将前10天的自定义航班设定为所需每日预算的大约75%，以减少 *学习阶段*. 然后，为剩余预算设置第二个自定义航班。

  例如，如果您在30天内有$100,000的支出，则将航班1的预算（第1-10天）设置为$25,000（75% x $100,000/30天=每天$2,500）。 将剩余预算75,000美元用于航班2（第11-30天）。

* **预算：** DSP将始终尝试在包中的所有版面之间平均分配100%的包预算。 如果投放位置支出较少或没有支出，我们建议为投放位置设置预算上限，以允许将更多预算按比例分配给投放位置。 允许24-48小时对预算更改进行校准。

* **优化目标：** 使用两个性能优化目标之一， *[!UICONTROL Highest ROAS]* 或 *[!UICONTROL Lowest CPA]*，具体取决于资源包目标。 这些目标分别自动优化包以实现ROAS最高版位或是CPA最低版位。

* **自定义目标：**
   * 如果新资源包与现有资源包具有相同的目标，则可以选择链接现有资源包，以便算法可以使用现有的机器学习数据。
   * 输入相应的 [!UICONTROL Target CPA] 或 [!UICONTROL Target ROAS].

* **Flight Pacing和Intraday Pacing：** 对于这两种类型的步调，选择 *[!UICONTROL Even]* 通过在每天和整个飞行期间统一步调，最大限度地实现您的性能目标。

  >[!CAUTION]
  >
  >使用 *[!UICONTROL FrontLoad]* 和 *[!UICONTROL Aggressive Front Load]* 用于飞行步调和 *[!UICONTROL ASAP]* 仅当您完全优先考虑投放并花费而非性能优化时，才考虑当天步调，因为这些策略可能会对您所需的性能KPI产生负面影响。

## 步骤4 — 创建投放结构

少即是多。 如果每个资源包可以设置的版面少于六个，则可用预算可以最轻松地动态转移到性能最佳的版面。

此外，请确保将每个投放位置添加到包目标类型为 *[!UICONTROL Prospecting]* 或 *[!UICONTROL Retargeting]*，视情况而定。

以下是推荐的性能营销活动版面设置。

### 目标

您将在包级别配置CPA或ROAS优化（请参阅步骤3 — 创建包），但您可以添加其他放置级别设置。

* **最高出价：**
   * 对于潜在客户投放位置，请使用较低的最高出价（5美元）。
   * 要重新定位投放位置，请使用最高出价（12美元）。

* **预竞价过滤器：** 最大限度地减少或最好避免设置激进的竞价前筛选条件，这会阻止投放达到规模。 最佳实践包括：

   * 为每个投放位置使用一(1)个预竞价过滤器。 多个预竞价筛选器需要同时满足这两个条件，这会缩小规模。

   * 在应用了其他定位（如受众、地理和网站定位）的情况下，请考虑设置更宽松的预竞价过滤器。

有关何时使用每个预竞价过滤器的说明，请参阅 [投放位置级别预竞价过滤器及其使用方式](/help/dsp/optimization/optimization-pre-bid-filters.md).

### 库存

要最大化规模，请使用 [!UICONTROL Public] (Open Exchange)和 [!UICONTROL On Demand] 库存。

### 网站定位

* **[!UICONTROL Traffic Type]**： [!UICONTROL Websites] 仅限
* **[!UICONTROL Site Tier]**: [!UICONTROL All sites]

### 受众定位

<!-- Say something about limiting unnecessary constraints/limitations, including dayparting, which limit your chances for ad exposure. Use only when it's required for your audience. -->

* **[!UICONTROL Included Audiences]:**
   * 对于潜在客户投放位置，将类似的受众类别和类似的受众规模分组到一个投放位置中。 然后，根据性能，执行下列操作之一：
      * 从现有投放位置中删除性能不佳的受众。
      * 将表现最好的受众转移到单独的投放位置以更好地控制预算。
   * 对于重新定位投放位置，理想情况下，您应在每个投放位置包含一个受众区段，以轻松控制竞价和预算。

>[!NOTE]
>
>如果只能通过一次投放联系用户，则广告的效果最佳。 不同投放位置的用户之间存在大量重叠，这可能会导致竞争，从而产生一个竞价不断增加的循环，从而提高每位用户的成本。 因此，如果您包含多个受众，请确保它们不包含重叠的用户/受众成员。
>
> 您可以通过在层中创建受众来避免受众重叠，这样您就可以根据需要从投放位置中禁止更高且更包容的层。

* **[!UICONTROL Frequency Capping]:**
   * 对于潜在客户投放位置，请使用严格的频率限制（每天一次展示）。
   * 对于重定向投放位置，将主投放上限设置为每天6-10次展示，将次上限设置为每小时1次展示。

* **[!UICONTROL Device Targeting]**:
   * 包括 [!UICONTROL Computer]， [!UICONTROL Mobile]、和 [!UICONTROL Tablet].
   * 不定位 [!UICONTROL Firefox] 和 [!UICONTROL Safari] 因为定位和测量限制。 有关更多详细信息，请联系您的Adobe客户团队 [!DNL Adobe] 支持 [!DNL Safari ITP].
   * 如果定位移动Web流量，则禁用所有移动浏览器，但以下情况除外 [!UICONTROL Chrome] 和 [!UICONTROL Edge].

### 品牌安全和媒体质量

使用上下文过滤、预竞价欺诈阻止和/或 [!UICONTROL Ads.txt] 过滤将限制投放的规模，但会根据需要使用它们。

## 步骤5 — 使用正确的创意资产

* 最佳实践是包含尽可能多的唯一广告大小，以最大限度地扩大范围。 通用显示模板允许您上传任何标准显示广告大小。
* 确保所有版面都包含 *至少* 所有主要显示广告尺寸（300x250、728x90、160x600、300x600、320x50和300x50）。
* 经常更新创意内容以防止创意疲劳。

>[!MORELIKETHIS]
>
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
>* [投放设置](/help/dsp/campaign-management/placements/placement-settings.md)
> * [DSP如何优化活动](optimization-how-dsp-optimizes-campaigns.md)
>* [优化目标及其使用方式](optimization-goals.md)
>* [投放位置级别预竞价过滤器及其使用方式](optimization-pre-bid-filters.md)
>* [营销活动启动检查清单](/help/dsp/campaign-management/campaign-launch-checklist.md)
