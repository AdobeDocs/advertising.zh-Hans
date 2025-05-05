---
title: 从Advertising DSP Campaigns收集点击和展示数据
description: 了解如何使用Audience Manager像素从Advertising DSP广告中捕获基于Cookie的展示和点击事件
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# 从Advertising DSP Campaigns收集媒体接触数据

*仅使用Advertising DSP的广告商*

*仅具有Adobe Advertising-Adobe Audience Manager集成的广告商*

本文档介绍如何使用Audience Manager像素为Advertising DSP广告添加标签以捕获基于Cookie的展示和点击事件，以及使用数据所需的其他任务。

事件像素不会捕获在无Cookie环境中发生的事件，例如移动应用程序和连接的TV (CTV)。

## 步骤1：在Audience Manager中设置数据Source {#set-up-data-source}

在Audience Manager中，为DSP展示创建一个[数据源](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html)并单击数据。 在每个事件标记[&#128279;](#implement-dsp-pixels)中包含数据源ID ，以便所有跟踪的事件都归属于该数据源。

>[!NOTE]
> 可以在单个数据源中收集在多个DSP上运行的广告促销活动的所有展示和点击数据。

## 步骤2：在网页上实施展示和点击事件像素 {#implement-dsp-pixels}

广告商可以为自己的品牌创建和实施事件标记。 如有必要，请联系您的Adobe Audience Manager顾问或Adobe客户团队寻求支持。

>[!NOTE]
>
>如果您的组织使用[!DNL Analytics]跟踪，则您可能不需要Audience Manager点击跟踪。 Adobe Analytics可捕获点击信号，并可通过[服务器端转发](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html)将其发送到Audience Manager。

### 像素语法

事件像素必须包含以下参数。

**展示跟踪像素：**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

带有以`&`为前缀的[可选附加参数](#parameters)

**点击跟踪像素：**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

带有以`&`为前缀的[可选附加参数](#parameters)

其中：

* `[Audience Manager customer domain]`是将展示或点击事件发送到[!DNL Adobe]的域名。

* `[source id]`是您跟踪DSP展示和点击数据的[数据源](#set-up-data-source)的ID。

* `[redirect URL]`是双重编码的重定向URL。 如果您使用的是联机编码工具(如www.urlencoder.org)，则通过编码器运行字符串并重新编码结果。

* `${TM_CAMPAIGN_ID_NUM}`是DSP中的数字营销活动ID。 如果要对单个促销活动ID进行硬编码，而不使用DSP宏，请在促销活动设置中找到该ID。

* 每个[参数](#key-value-pairs)的前缀为`&`，格式为`d_parameter=parameter_id`，其中`parameter`被新字段的键值对替换。 示例： `&d_placement=${TM_PLACEMENT_ID_NUM}`

### 键值对形式的参数 {#parameters}

**格式：** `d_parameter=parameter_id`

    其中：
    
    *参数的前缀为“&amp;”
    
    *“parameter”被新字段的键值对替换
    
    示例：“&amp;d_placement=${TM_PLACEMENT_ID_NUM}”

这两种类型的像素都可以包含其他参数作为&#x200B;*键值对*，用于收集特征或为其他报表提供促销活动元数据（如版面名称或促销活动名称）。 键值对由两个相关元素组成：一个是定义数据集的常量&#x200B;*键*，另一个是属于数据集的变量&#x200B;*值*。

在键值对中，值变量可以是硬编码ID或&#x200B;*宏*，宏是自包含代码的一个小单位，当加载广告标记以进行促销活动和用户跟踪时，它会被动态替换为相应的值。 对于与促销活动相关的参数，您可以使用[DSP宏](/help/dsp/campaign-management/macros.md)而不是Audience Manager宏来发送促销活动属性以及相应的展示，或者使用单个像素在所有广告中进行Audience Manager的点击数据。 插入到事件像素中的DSP宏必须是包含在像素中的键值对的相应值。 例如，对于`d_placement`键，您将使用DSP宏`${TM_PLACEMENT_ID_NUM}`作为值来捕获Adobe Advertising宏生成的版面ID。

有关Audience Manager支持展示事件像素的宏列表，请参阅“[通过像素调用捕获营销活动展示数据](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs)”。

有关Audience Manager支持点击事件像素的宏列表，请参阅“[通过像素调用捕获营销活动点击数据](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html)”。

>[!TIP]
>
>* 最佳实践是包含营销活动、投放、创意（广告）和网站ID，以便您可以使用营销活动属性创建Audience Manager特征。
>* 要创建Audience Optimization报表，还需要其他参数。
>* 在键值对中，将这些值替换为相关的[DSP宏](/help/dsp/campaign-management/macros.md)，以便您可以在所有促销活动的所有广告中使用单个像素。 例如，将`d_campaign=[%campaignID%]`更改为`d_campaign=${TM_CAMPAIGN_ID_NUM}`以捕获Adobe Advertising宏生成的促销活动ID。
>* 如果需要，您可以使用硬编码值创建自己的参数。 示例： `d_DSP=AdCloud`

展示事件像素示例：

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### 添加像素的位置

#### 展示跟踪像素

将展示事件跟踪像素附加到您的[!DNL DSP]营销活动中的所有广告。 您可以在以下任意位置执行此操作：

* 在版面级别，默认将像素应用于版面中的所有广告。 在版面设置的“跟踪”部分中，在[[!UICONTROL Event pixels]字段](/help/dsp/campaign-management/placements/placement-settings.md)中添加像素。

* 在广告级别，将覆盖任何投放位置级别的事件像素。 在广告设置中，[在[!UICONTROL Pixel]选项卡](/help/dsp/campaign-management/ads/ad-edit.md)上创建事件像素。

* （对于第三方广告服务器上的广告）在广告服务器上的广告级别。

#### 点击跟踪像素

在广告服务器中，将点击事件像素（追加了编码的URL）插入广告的点进URL正常插入的位置。

## 步骤3：实施后任务

实施事件标记后，数据将流入Audience Manager数据收集服务器。 请先完成以下任务，然后才能在报表中使用数据。

### 创建[!DNL Amazon S3]存储段和数据Source

一旦您的数据位于Audience Manager服务器上，您必须创建一个[!DNL Amazon Simple Storage Service] ([!DNL Amazon S3])存储段，然后创建一个数据源，所有像素数据都会发送到该数据源。 如果您需要支持，请联系您的Audience Manager顾问或[客户关怀](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html)。

### 创建Audience Manager特征和区段

您的事件数据作为[未使用的信号](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html)流入Audience Manager。 从摄取的数据中手动创建[基于规则的特征](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html)，然后使用这些特征创建[区段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html)，之后才能在报表中使用这些数据。

为在DSP中向特定创意展示的用户填充用户级数据的特征示例：

1. 将事件标识为`d_event = imp`。
1. 识别DSP促销活动中的创意ID，然后将其映射到特征作为`d_creative=[Creative ID]`。

![特征创建屏幕](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [DSP宏](/help/dsp/campaign-management/macros.md)
>* [将DSP媒体曝光数据发送到Adobe Audience Manager的概述](overview.md)
>* [用例](use-cases.md)
