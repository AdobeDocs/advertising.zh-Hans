---
title: 使用 [!DNL Roku] 库存
description: 了解DSP与的合作伙伴关系 [!DNL Roku]，包括库存选项、经批准的第三方跟踪供应商以及 [!DNL Roku]特定于投放位置。
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: e7a1aa80-d7f0-4a4e-96b1-6b362a32106e
source-git-commit: 9b3d6893e004b16714bf50f1334424d50fac7c91
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# 使用 [!DNL Roku] 库存

Advertising DSP在以下位置提供广告的独特功能： [!DNL Roku].

## DSP和 [!DNL Roku] 伙伴关系

Roku和DSP具有独特的合作伙伴关系，符合您的 [!DNL DSP] 受众到 [!DNL Roku] 1:1确定性受众定位的ID [!DNL Roku] 库存。

在Roku自己的DSP (OneView)之外，Advertising DSP可以单独访问这些定位功能。 Advertising DSP也是唯一有权测量的DSP [!DNL Roku] 在连接至所有其它电视(CTV)的库存旁边提供。 因为 [!DNL Roku] 不共享所有标准RTB和印象像素信号，任何其他DSP都不能跨Roku销售的CTV源定位或测量。

## [!DNL Roku] 清单选项

您可以执行以下操作之一：a)直接使用设置私有交易ID [!DNL Roku] 然后将交易ID数据输入DSP或b)访问 [!DNL On Demand] 要订阅的图库 [!DNL Roku] 用户档案：

>[!NOTE]
>
>[!DNL Roku] 库存在开放的市场和交易所不可用。

* 对于你的私人交易， [在DSP中设置有关交易ID的信息](/help/dsp/inventory/deal-id-create.md) 然后定位”[!UICONTROL Roku Network – Audience]”和“[!UICONTROL The Roku Channel – Audience]“ within [!DNL Roku] 投放位置。<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* 您可以 [订阅以下内容 [!DNL Roku] 中的库存 [!DNL On Demand] 图库](/help/dsp/inventory/on-demand-inventory-subscribe.md)，然后在中定位任何批准的交易 [!DNL Roku] 投放位置：

   * &quot;[!UICONTROL Roku Network – Audience]”用于跨以下区域进行清点 [!DNL Roku] 与优质内容合作伙伴建立的生态系统，例如 [!DNL The CW]， [!DNL ABC]、和 [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel – Audience]“（表示） [!DNL Roku] 自有和运营(O&amp;O)应用程序内容。

### 使用自定义私有市场的优势 [!DNL Roku]

私人交易允许您根据自己的需求自定义交易参数。

* **议定价格：** 使用 [!DNL Roku] 销售团队商议并安排符合您的活动需求的交易。

* **缩放优先级：** 私有市场(PMP)比始终在线交易获得更高的优先级(例如 [!DNL On Demand] 交易)。

* **频率管理：** 此 [!DNL Roku] 默认频率上限是每个用户每30分钟出现一(1)个广告，但您可以按小时、日、周、月或整个飞行时段自定义上限。<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]数据定位：** [!DNL Roku] 受众构建自 [!DNL Roku] 设备和电视信号，数据由 [!DNL The Roku Channel] （例如，电视流亲和力、流媒体电视行为以及有线电视订阅状态），以及来自 [!DNL Roku] 客户关系管理(CRM)系统。

* **[!DNL Roku]内容定位：** 私人交易可以按类型、应用程序阻止列表、季节和舞台活动，以及在以下内容中展示来定位应用程序： [!DNL The Roku Channel] 仅限。

## [!DNL Roku] 版面

在DSP营销活动中， [创建 [!DNL Roku]特定于投放位置](/help/dsp/campaign-management/placements/placement-create.md) 使用投放位置类型»[!UICONTROL Connected TV (Roku)]“ 包括 [!DNL Roku] 中的投放位置 [!DNL Roku]具有已定义目标的特定资源包。

每个 [!DNL Roku] 投放位置必须至少定向一个 [!DNL Roku] 交易或来源。 要将DSP独特受众匹配与 [!DNL Roku]，包括一个或多个可与匹配的受众区段 [!DNL Roku] （选择启用）确定性数据集。

### [!DNL Roku] — 批准的第三方跟踪供应商

[!DNL Roku] 投放位置可以包括来自以下供应商的第三方事件像素和转化像素：  [!DNL Acxiom]， [!DNL Comscore]， [!DNL Data Plus Math]， [!DNL Experian]， [!DNL Factual]， [!DNL Kantar]， [!DNL Marketing Evolution]， [!DNL Neustar]， [!DNL Nielsen]， [!DNL Nielsen Catalina Solutions]， [!DNL NinthDecimal]， [!DNL Oracle]， [!DNL Placed]， [!DNL Polk]、和 [!DNL Research Now].

### 按投放策略列出的最佳实践

以下是建议的做法 [!DNL Roku]特定于投放位置。

要最大限度地扩大增量范围，请执行以下操作：

* 禁止显示受众 [!DNL Roku O&O] 方式是排除您已使用访问的受众 [!DNL The Roku Channel].

* 禁止显示受众 [!DNL All Roku] 通过排除您已经访问过的受众， [!DNL Roku] 平台。

要获得最快的设置：

* 将现有、始终在线的交易定位为 [!DNL The Roku Channel] 在 [[!DNL On Demand] 库存](/help/dsp/inventory/on-demand-inventory-subscribe.md) 以快速访问 [!DNL Roku] 自有及经营存货。
* 将现有、始终在线的交易定位为 [!DNL Roku Network] 在 [[!DNL On Demand] 库存](/help/dsp/inventory/on-demand-inventory-subscribe.md) 以快速实现横向扩展 [!DNL Roku] 平台。

要达到最大比例：

* 自定义 [!DNL Roku] 优先访问的专用市场 [!DNL Roku] 议价供应。

>[!MORELIKETHIS]
>
>* [手动创建交易ID详细信息](/help/dsp/inventory/deal-id-create.md)
> * [订阅和请求访问 [!DNL On Demand] 高级库存交易](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [创建投放位置](/help/dsp/campaign-management/placements/placement-create.md)
