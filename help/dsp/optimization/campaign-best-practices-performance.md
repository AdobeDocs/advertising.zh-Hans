---
title: 设置效果活动的最佳实践
description: 了解设置以性能为中心的活动的最佳实践，其中包括针对最低CPA或最高ROAS而优化的投放位置。
feature: DSP Optimization, DSP Best Practices
exl-id: bc297796-0c89-4d91-87aa-0668462526ae
source-git-commit: 802c75920bb11f262cbe0d76d2554971aaf35831
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 0%

---

# 设置效果活动的最佳实践

DSP可以优化以性能为中心的促销活动。 请参阅以下效果促销活动的最佳实践：

* 步骤1 — 定义目标
* 第2步 — 定义您的策略
* 步骤3 — 创建包
* 步骤4 — 创建投放结构
* 步骤5 — 使用正确的Creative Assets

## 步骤1 — 定义目标

了解活动的目标很重要，例如实现尽可能最高的ROAS或尽可能最低的CPA。 性能营销活动具有[优化目标](/help/dsp/optimization/optimization-goals.md)“[!UICONTROL Highest Return on Ad Spend (ROAS)"]”或“[!UICONTROL Lowest Cost per Acquisition (CPA)]”。 对于营销活动中的每个资源包，相应地指定优化目标。

![优化目标](/help/dsp/assets/optimization-goals.png)

您还需要确定导致整体目标的成功事件并相应地创建自定义目标。 对于每个包，指定要与使用[!DNL Adobe Sensei]的报表和算法优化的总体优化目标一起使用的自定义目标。 有关创建自定义目标（包括最佳实践）的更多信息，请参阅[自定义目标](custom-goal.md)。

## 第2步 — 定义您的策略

### 潜在客户发现策略

上层漏斗包中包含投放位置，具有非常广泛的定位以吸引净新消费者。

#### 建议的潜在客户放置策略

* 使用以下策略查找可能转化的新受众：

   * 从数据管理平台(DMP)(如Adobe Audience Manager)进行相似人群拓展建模。
   * 使用第三方数据的行为定位。
   * 上下文定位。
   * 站点/类别定位。

* 使用网络运行(RON)定位：一定要包括没有受众定位和广泛库存定位的网络放置运行。 这允许[!DNL Adobe Sensei]算法查找有价值用户，这些用户可能拥有尚未分类到受众的较新Cookie。

### 重新定位策略

下层漏斗包包括定向已访问过广告商网页或广告商具有CRM数据的用户的投放位置。

#### 推荐的重新定位放置策略

* 如果广告商是Adobe Analytics或Adobe Audience Manager客户，则您可以在DSP中构建第一方区段（例如主页访客、产品页面或购物车放弃者）并将它们用作投放目标。

* 避免为面向受众的投放分配过多的预算。 一般来说，每月每1,000个用户预算为30美元。

## 步骤3 — 创建包

最佳实践是为上部漏斗探矿和下部漏斗重新定位创建单独的包。 优化在包级别进行，因此来自包中所有版面的性能数据都将汇集在一起。 因此，会将投放分组到具有相似预期性能的包中。

![用于发现客户和重新定位的单独包示例](/help/dsp/assets/p-r.png)

此外，请使用以下设置。

### 目标和预算

* **步调和上限：**&#x200B;要选择CPA或ROAS优化目标，包必须使用包级别的步调。 这可确保优化包中的所有版面，以根据性能和规模将支出分配到选定的目标。

* **投放日期：** （潜在客户包）当您的营销活动运行超过25天时，请使用[!UICONTROL Activate Custom Flighting]功能。 首先，将前10天的自定义航班设置为所需每日预算的大约75%，以减少&#x200B;*学习阶段*&#x200B;期间的支出。 然后，为剩余预算设置第二个自定义航班。

  例如，如果您在30天内有$100,000的支出，则将航班1的预算（第1-10天）设置为$25,000（75% x $100,000/30天=每天$2,500）。 将剩余预算75,000美元用于航班2（第11-30天）。

* **预算：** DSP始终尝试在包中的所有版面之间平均分配100%的包预算。 如果投放位置支出较少或没有支出，我们建议为投放位置设置预算上限，以允许将更多预算按比例分配给投放位置。 允许24-48小时对预算更改进行校准。

* **优化目标：**&#x200B;使用两个性能优化目标之一，*[!UICONTROL Highest Return on Ad Spend]*&#x200B;或&#x200B;*[!UICONTROL Lowest Cost per Acquisition]*，具体取决于包目标。 这些目标分别自动优化包以实现ROAS最高版位或是CPA最低版位。

* **自定义目标：**
   * 如果新资源包与现有资源包具有相同的目标，则可以选择链接现有资源包，以便算法可以使用现有的机器学习数据。
   * 输入相应的[!UICONTROL Target CPA]或[!UICONTROL Target ROAS]。

* **Flight步调和Intraday步调：**&#x200B;对于这两种类型的步调，请选择&#x200B;*[!UICONTROL Even]*&#x200B;以通过全天和全天统一步调来最大化您的性能目标。

  >[!CAUTION]
  >
  >仅当您完全优先考虑投放并花费而非性能优化时，才使用&#x200B;*[!UICONTROL FrontLoad]*&#x200B;和&#x200B;*[!UICONTROL Aggressive Front Load]*&#x200B;进行飞行步调和&#x200B;*[!UICONTROL ASAP]*&#x200B;进行当天步调，因为这些策略可能会对您所需的性能KPI产生负面影响。

## 步骤4 — 创建投放结构

少即是多。 如果每个资源包可以设置的版面少于六个，则可用预算可以最轻松地动态转移到性能最佳的版面。

此外，请确保将每个投放位置添加到包目标类型为&#x200B;*[!UICONTROL Prospecting]*&#x200B;或&#x200B;*[!UICONTROL Retargeting]*&#x200B;的包中（如果适用）。

以下是推荐的性能营销活动版面设置。

### 目标

您必须在包级别配置CPA或ROAS优化（请参阅步骤3 — 创建包），但您可以添加其他版面级别设置。

* **最高出价：**
   * 对于潜在客户投放位置，请使用较低的最高出价（5美元）。
   * 要重新定位投放位置，请使用最高出价（12美元）。

* **预竞价筛选器：**&#x200B;最小化或最好避免设置妨碍投放达到规模的积极预竞价筛选器。 最佳实践包括：

   * 为每个投放位置使用一(1)个预竞价过滤器。 使用多个预竞价筛选器需要同时满足这两个条件，这会缩小规模。

   * 在应用了其他定位（如受众、地理和网站定位）的情况下，请考虑设置更宽松的预竞价过滤器。

查看有关[位置级别预竞价筛选器何时使用每个预竞价筛选器的说明以及如何使用它们](/help/dsp/optimization/optimization-pre-bid-filters.md)。

### 库存

若要最大化规模，请使用[!UICONTROL Public] (Open Exchange)和[!UICONTROL On Demand]清单。

### 网站定位

* **[!UICONTROL Traffic Type]**：仅[!UICONTROL Websites]
* **[!UICONTROL Site Tier]**： [!UICONTROL All sites]

### 受众定位

<!-- Say something about limiting unnecessary constraints/limitations, including dayparting, which limit your chances for ad exposure. Use only when it's required for your audience. -->

* **[!UICONTROL Included Audiences]：**
   * 对于潜在客户投放位置，将类似的受众类别和类似的受众规模分组到一个投放位置中。 然后，根据性能，执行下列操作之一：
      * 从现有投放位置中删除性能不佳的受众。
      * 将表现最好的受众转移到单独的投放位置以更好地控制预算。
   * 对于重新定位投放位置，理想情况下，您应在每个投放位置包含一个受众区段，以轻松控制竞价和预算。

>[!NOTE]
>
>如果只能通过一次投放联系用户，则广告的效果最佳。 不同投放位置的用户之间存在大量重叠，这可能会导致竞争，从而产生一个竞价不断增加的循环，从而提高每位用户的成本。 因此，如果您包含多个受众，请确保它们不包含重叠的用户/受众成员。
>
> 您可以通过在层中创建受众来避免受众重叠，这样您就可以根据需要从投放位置中禁止更高且更包容的层。

* **[!UICONTROL Frequency Capping]：**
   * 对于潜在客户投放位置，请使用严格的频率限制（每天一次展示）。
   * 对于重定向投放位置，将主投放上限设置为每天6-10次展示，将次上限设置为每小时1次展示。

* **[!UICONTROL Device Targeting]**：
   * 包括[!UICONTROL Computer]、[!UICONTROL Mobile]和[!UICONTROL Tablet]。
   * 由于定位和测量限制，请勿定位[!UICONTROL Firefox]和[!UICONTROL Safari]。 有关[!DNL Safari ITP]的[!DNL Adobe]支持的更多详细信息，请与您的Adobe客户团队联系。
   * 如果您要定位移动Web流量，请禁用除[!UICONTROL Chrome]和[!UICONTROL Edge]之外的所有移动浏览器。

### 品牌安全和媒体质量

使用上下文过滤、出价前欺诈阻止和/或[!UICONTROL Ads.txt]过滤会限制投放的规模，但会根据需要使用它们。

## 步骤5 — 使用正确的Creative Assets

* 最佳实践是包含尽可能多的唯一广告大小，以最大限度地扩大范围。 通用显示模板允许您上传任何标准显示广告大小。
* 确保所有投放位置都至少包含&#x200B;*1&rbrace;所有主显示广告大小（300x250、728x90、160x600、300x600、320x50和300x50）。*
* 经常更新创意内容以防止创意疲劳。

>[!MORELIKETHIS]
>
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
>* [位置设置](/help/dsp/campaign-management/placements/placement-settings.md)
> * [DSP如何优化您的营销活动](optimization-how-dsp-optimizes-campaigns.md)
>* [优化目标及其使用方式](optimization-goals.md)
>* [投放位置级别预竞价筛选器及其使用方式](optimization-pre-bid-filters.md)
>* [营销活动启动项核对清单](/help/dsp/campaign-management/campaign-launch-checklist.md)
