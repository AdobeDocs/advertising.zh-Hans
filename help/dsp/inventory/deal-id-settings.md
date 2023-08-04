---
title: 手动交易标识设置
description: 请参阅手动输入的交易ID的设置说明。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 9d3417cb-8b44-4f1c-afc4-eea6a2e5b9d7
source-git-commit: badf6a1d7059b9e7e261165b19e00f09573b9e53
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# 手动交易标识设置

| 部分 | 参数 | 描述 | 必填 | 可编辑 |
|---------|-----------|-------------|----------|----------|
| [交易详细信息] | [!UICONTROL Deal name] | 用于标识 [!UICONTROL Deal ID] 在Advertising DSP中。 输入名称或选择 **[!UICONTROL Auto-name]** 让DSP根据交易详细信息生成名称。<br><br>自动生成名称的示例： `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | 是 | 是 |
| | [!UICONTROL External deal ID] | 您的发布者和SSP用于标识此交易的ID。 | 是 | 否 |
| | [!UICONTROL Publisher] | 销售此库存的发布者的名称。 | 是 | 否 |
| | [!UICONTROL SSP] | 此交易运行的供应方平台(SSP)。 | 是 | 否 |
| | [!UICONTROL Media type] | 通过此交易购买的媒体类型： *[!UICONTROL Desktop video]*， *[!UICONTROL Mobile video]*， *[!UICONTROL Connected TV]*， *[!UICONTROL Display]*， *[!UICONTROL Audio]*，或 *[!UICONTROL Publisher Managed]*. 选项因SSP而异。<br><br> 如果交易允许多种媒体类型，请在创建交易时为默认投放位置选择媒体类型。 稍后，您可以更改值，或者只需 [附加带有附加介质类型的新版面](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | 是 | 否 |
| | [!UICONTROL Deal type] | 交易承诺与定价结构：<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*：您和发布者尚未提交固定数量的展示投放。 该交易指定存货的最低价格，尽管可转换债券会因市况而波动及增加。</li><li>*[!UICONTROL Non guaranteed (fixed)]*：您和发布者尚未提交固定数量的展示投放。 定价乃按议定固定息率进行。</li><li>*[!UICONTROL Guaranteed (fixed)]*：您和发布者已同意预定义的展示次数、定位、投放日期和固定价格。<br><br><b>注意：</b> 有保证的交易需要投放日期和指定数量的展示 [!UICONTROL Tracking] 部分。 您还必须为交易创建默认的计划性保证(PG)投放位置，并且您可以选择将交易用于其他投放位置。</li></ul> | 是 | 否 |
| | [!UICONTROL CPM] | 每1000次展示的议定成本(CPM)。 | 是 | 是 |
| | [货币] | 交易的货币。<br><br>所有SSP都接受美元交易。 当SSP接受您的DSP帐户的货币时，该货币也可用。 | 是 | 否 |
| | [!UICONTROL Billing method] | 所有交易ID [!DNL Adobe]融资和发票。 DSP会根据使用情况向所有可用的媒体供应商付款，管理与供应商的不一致，并向该帐户发送一张合并发票。 此选项会产生额外费用，如帐户的费率卡中所述。 | 是 | 否 |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | 可以访问交易的用户帐户的电子邮件地址。 | 否 | 是 |
| | [!UICONTROL Advertisers that can access this deal] | 帐户中可访问此交易的特定广告商。<br><br><b>注意：</b> 您可以从以下位置的其他帐户与广告商共享该交易： [!UICONTROL Deals] 视图。 在交易行中，单击 **[!UICONTROL #]**，单击 **[!UICONTROL share]**，然后使用电子邮件地址共享交易。 | 是 | 是 |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | 使用此交易的流量的开始和结束日期。 这些日期仅用于跟踪目的，不影响广告投放。<br><br><b>提示：</b> 在 [!UICONTROL Inventory] > [!UICONTROL Deals] 视图， [!UICONTROL Pacing & Budget] 列显示了交易如何步调到指定的投放日期和展示目标。 如果投放速度不佳或超速，请与您的出版商联系以调整通过交易发送的数量。 | 有保证的交易：有<br>无担保交易：否 | 是 |
| | [!UICONTROL Impressions] | （对于非保证交易是可选的）您预计使用此交易运行的预计展示次数。 此值仅用于跟踪目的；发布者控制广告投放。 | 有保证的交易：有<br>无担保交易：否 | 是 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [手动创建交易ID详细信息](deal-id-create.md)
>* [SSP合作伙伴](ssp-partners.md)
>* [关于专用清单](private-inventory-about.md)
