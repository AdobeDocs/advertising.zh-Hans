---
title: 从Advertising DSP促销活动中收集点击和展示数据
description: 了解如何使用Audience Manager像素从Advertising DSP广告中捕获基于Cookie的展示和点击事件
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# 从Advertising DSP Campaigns收集媒体接触数据

*仅使用Advertising DSP的广告商*

*仅具有Adobe Advertising-Adobe Audience Manager集成的广告商*

本文档介绍如何使用Audience Manager像素标记Advertising DSP广告以捕获基于Cookie的展示和点击事件，以及使用数据所需的其他任务。

事件像素不会捕获在无Cookie环境中发生的事件，例如移动应用程序和连接的TV (CTV)。

## 步骤1：在Audience Manager中设置数据源 {#set-up-data-source}

在Audience Manager中，创建 [数据源](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) DSP展示和点击数据的。 包括数据源ID [在每个事件标记中](#implement-dsp-pixels) 以便所有跟踪的事件都归属于数据源。

>[!NOTE]
> 可以在单个数据源中收集在多个DSP上运行的广告促销活动的所有展示和点击数据。

## 步骤2：在网页上实施展示和点击事件像素 {#implement-dsp-pixels}

广告商可以为自己的品牌创建和实施事件标记。 如有必要，请联系您的Adobe Audience Manager顾问或Adobe客户团队寻求支持。

>[!NOTE]
>
>如果您的组织使用 [!DNL Analytics] 之后，您可能不需要Audience Manager点击跟踪。 Adobe Analytics可捕获点击信号，并可将其发送给Audience Manager [服务器端转发](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

### 像素语法

事件像素必须包含以下参数。

**展示跟踪像素：**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

替换为 [可选的其他参数](#parameters) 前置词 `&`

**点击跟踪像素：**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

替换为 [可选的其他参数](#parameters) 前置词 `&`

其中：

* `[Audience Manager customer domain]` 是将展示或点击事件发送到的域名 [!DNL Adobe].

* `[source id]` 是的ID [数据源](#set-up-data-source) 其中您将跟踪DSP展示和点击数据。

* `[redirect URL]` 是经过双重编码的重定向URL。 如果您使用的是联机编码工具(如www.urlencoder.org)，则通过编码器运行字符串并重新编码结果。

* `${TM_CAMPAIGN_ID_NUM}` 是DSP中的数字促销活动ID。 如果要对单个促销活动ID进行硬编码，而不使用DSP宏，请在促销活动设置中找到该ID。

* 每个 [参数](#key-value-pairs) 前缀 `&` 并且采用格式 `d_parameter=parameter_id`，其中 `parameter` 被新字段的键值对替换。 示例： `&d_placement=${TM_PLACEMENT_ID_NUM}`

### 键值对形式的参数 {#parameters}

**格式：**  `d_parameter=parameter_id`

    其中：
    
    *参数的前缀为“&amp;”
    
    *“parameter”被新字段的键值对替换
    
    示例： &#39;&amp;d_placement=${TM_PLACEMENT_ID_NUM}’

这两种类型的像素都可以包含其他参数，如 *键值对* 收集特征或为其他报表提供营销活动元数据（例如投放位置名称或营销活动名称）。 键值对由两个相关元素组成： *键*，定义数据集的常量，以及 *值*，这是属于该集的变量。

在键值对中，值变量可以是硬编码ID或 *宏*，这是自包含代码的一个小单元，当加载广告标记以进行促销活动和用户跟踪时，它会动态替换为相应的值。 对于与促销活动相关的参数，您可以使用 [DSP宏](/help/dsp/campaign-management/macros.md) 而不是使用Audience Manager宏在所有广告中使用单个像素将促销活动属性与相应的展示次数或点击数据一起发送到Audience Manager。 插入到事件像素中的DSP宏必须是包含在像素中的键值对的相应值。 例如，对于 `d_placement` 键，您将使用DSP宏 `${TM_PLACEMENT_ID_NUM}` 作为值来捕获Adobe Advertising宏生成的版面ID。

有关Audience Manager支持展示事件像素的宏列表，请参阅“[通过像素调用捕获营销活动展示数据](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs)“

有关Audience Manager支持点击事件像素的宏列表，请参阅“[通过像素调用捕获营销活动点击数据](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html)“

>[!TIP]
>
>* 最佳实践是包含营销活动、投放、创意（广告）和网站ID，以便您可以使用营销活动属性创建Audience Manager特征。
>* 要创建Audience Optimization报表，还需要其他参数。
>* 在键值对中，将值替换为相关的 [DSP宏](/help/dsp/campaign-management/macros.md) 因此，您可以在所有促销活动的所有广告中使用单个像素。 例如，更改 `d_campaign=[%campaignID%]`到 `d_campaign=${TM_CAMPAIGN_ID_NUM}` 捕获Adobe Advertising宏生成的促销活动ID。
>* 如果需要，您可以使用硬编码值创建自己的参数。 示例： `d_DSP=AdCloud`

展示事件像素示例：

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### 添加像素的位置

#### 展示跟踪像素

将展示事件跟踪像素附加到中的所有广告 [!DNL DSP] 营销活动。 您可以在以下任意位置执行此操作：

* 在版面级别，默认将像素应用于版面中的所有广告。 在版面设置的“跟踪”部分中，将像素添加到 [[!UICONTROL Event pixels] 字段](/help/dsp/campaign-management/placements/placement-settings.md).

* 在广告级别，将覆盖任何投放位置级别的事件像素。 在广告设置中， [在上创建事件像素 [!UICONTROL Pixel] 选项卡](/help/dsp/campaign-management/ads/ad-edit.md).

* （对于第三方广告服务器上的广告）在广告服务器上的广告级别。

#### 点击跟踪像素

在广告服务器中，将点击事件像素（追加了编码的URL）插入广告的点进URL正常插入的位置。

## 步骤3：实施后任务

实施事件标记后，数据将流入Audience Manager数据收集服务器。 请先完成以下任务，然后才能在报表中使用数据。

### 创建 [!DNL Amazon S3] 存储段和数据源

一旦您的数据在Audience Manager服务器上，您必须创建 [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3])存储桶，然后是一个数据源，所有像素数据都会发送到该数据源。 请联系您的Audience Manager顾问或 [客户关怀](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) 如果您需要支持。

### 创建Audience Manager特征和区段

Audience Manager您的事件数据将作为 [未使用的信号](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html). 手动创建 [基于规则的特征](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) 并从摄取的数据中创建 [区段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) 使用这些特征，您才能在报表中使用数据。

为在DSP中向特定创意展示的用户填充用户级数据的特征示例：

1. 将事件识别为 `d_event = imp`.
1. 识别DSP促销活动中的创意ID，然后将其映射到特征，如下所示 `d_creative=[Creative ID]`.

![特征创建屏幕](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [DSP宏](/help/dsp/campaign-management/macros.md)
>* [将DSP媒体曝光数据发送到Adobe Audience Manager概述](overview.md)
>* [用例](use-cases.md)
