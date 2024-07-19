---
title: 使用 [!DNL Roku] 库存
description: 了解DSP与 [!DNL Roku]的合作伙伴关系，包括库存选项、批准的第三方跟踪供应商以及特定于 [!DNL Roku]的投放位置的最佳实践。
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: e7a1aa80-d7f0-4a4e-96b1-6b362a32106e
source-git-commit: f3099c84fe2d6b1610ddf4ca07d59b119718afee
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# 使用[!DNL Roku]清单

Advertising DSP提供在[!DNL Roku]上做广告的功能。

## 受众匹配

[!DNL Roku]和DSP合作关系将您的[!DNL DSP]受众与[!DNL Roku] ID匹配，以获取[!DNL Roku]清单中具有1:1确定性受众定位的信息。

## [!DNL Roku]清单选项

您可以a)直接使用[!DNL Roku]设置私有交易ID，然后将交易ID数据输入到DSP中，或者b)访问[!DNL On Demand]库以订阅[!DNL Roku]配置文件：

>[!NOTE]
>
>[!DNL Roku]库存在公开市场和交易场所中不可用。

* 对于您的私人交易，[在DSP](/help/dsp/inventory/deal-id-create.md)中设置有关交易ID的信息，然后在[!DNL Roku]投放位置中定位“[!UICONTROL Roku Network - Audience]”和“[!UICONTROL The Roku Channel - Audience]”。<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* 您可以[在 [!DNL On Demand] 图库](/help/dsp/inventory/on-demand-inventory-subscribe.md)中订阅以下 [!DNL Roku] 清单，然后在[!DNL Roku]投放位置中定位任何已批准的交易：

   * “[!UICONTROL Roku Network - Audience]”适用于包含高级内容合作伙伴（如[!DNL The CW]、[!DNL ABC]和[!DNL ESPN]）的[!DNL Roku]生态系统中的库存。
   * 针对[!DNL Roku]自有和运营的(O&amp;O)应用程序内容的“[!UICONTROL The Roku Channel - Audience]”。

### 使用[!DNL Roku]自定义专用市场的优势

私人交易允许您根据自己的需求自定义交易参数。

* **议定价格：**&#x200B;与[!DNL Roku]销售团队合作，协商并构建符合您营销活动需求的交易。

* **规模优先级：**&#x200B;私有市场(PMP)接收的优先级高于始终在线交易（如[!DNL On Demand]交易）。

* **频率管理：** [!DNL Roku]默认频率上限是每个用户每30分钟一(1)个广告，但您可以按小时、日、周、月或整个航班时段自定义此上限。<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]数据定位：** [!DNL Roku]受众是从[!DNL Roku]设备和电视信号生成的，[!DNL The Roku Channel]跟踪的数据（如电视流派亲和度、流式电视行为以及有线电视订阅状态）以及来自[!DNL Roku]客户关系管理(CRM)系统的其他数据。

* 列入阻止列表 **[!DNL Roku]内容定位：**&#x200B;私人交易可以按类型、应用程序、季节性和末尾事件来定位应用程序，并且仅在[!DNL The Roku Channel]内显示。

## [!DNL Roku]个投放位置

在DSP营销活动中，[使用版面类型“[!UICONTROL Connected TV (Roku)]”创建 [!DNL Roku]特定的版面](/help/dsp/campaign-management/placements/placement-create.md)。 在具有已定义目标的特定于[!DNL Roku]的包中包含[!DNL Roku]个投放位置。

每个[!DNL Roku]投放位置必须至少面向一个[!DNL Roku]交易或源。 要使用与[!DNL Roku]匹配的DSP受众，请包含一个或多个可与[!DNL Roku]（选择启用）确定性数据集匹配的受众区段。

### [!DNL Roku]批准的第三方跟踪供应商

[!DNL Roku]投放位置可以包括来自以下供应商的第三方事件像素和转化像素： [!DNL Acxiom]、[!DNL Comscore]、[!DNL Data Plus Math]、[!DNL Experian]、[!DNL Factual]、[!DNL Kantar]、[!DNL Marketing Evolution]、[!DNL Neustar]、[!DNL Nielsen]、[!DNL Nielsen Catalina Solutions]、[!DNL NinthDecimal]、[!DNL Oracle]、[!DNL Placed]、[!DNL Polk]和[!DNL Research Now]。

### 按投放策略列出的最佳实践

以下是针对特定于[!DNL Roku]的投放位置的推荐实践。

要最大限度地扩大增量范围，请执行以下操作：

* 通过排除您使用[!DNL The Roku Channel]已访问的受众，禁止在[!DNL Roku O&O]上公开的受众。

* 通过排除已在[!DNL Roku]平台上访问的受众，禁止[!DNL All Roku]上公开的受众。

要获得最快的设置：

* 定位[[!DNL On Demand] 库存](/help/dsp/inventory/on-demand-inventory-subscribe.md)中[!DNL The Roku Channel]的现有、始终开启的交易以快速访问[!DNL Roku]自有运营的库存。
* 定位[[!DNL On Demand] 库存](/help/dsp/inventory/on-demand-inventory-subscribe.md)中[!DNL Roku Network]的现有、始终开启的交易以在[!DNL Roku]平台中快速实现扩展。

要达到最大比例：

* 自定义[!DNL Roku]私有市场以按协议价格优先访问[!DNL Roku]供应。

>[!MORELIKETHIS]
>
>* [手动创建交易ID详细信息](/help/dsp/inventory/deal-id-create.md)
> * [订阅和请求访问 [!DNL On Demand] 高级库存交易](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [创建版面](/help/dsp/campaign-management/placements/placement-create.md)
