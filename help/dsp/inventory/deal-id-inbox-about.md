---
title: 关于 [!UICONTROL Deal ID Inbox]
description: 了解 [!UICONTROL Deal ID inbox] 功能，允许您接受已与出版商协商的私人协议 [!DNL FreeWheel], [!DNL Google Authorized Buyers] (以前称为 [!DNL AdX]), and [!DNL Magnite DV+] (以前为 [!DNL Rubicon])。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# 关于 [!UICONTROL Deal ID Inbox]

Advertising DSP [!UICONTROL Deal ID inbox] 允许您快速设置DSP通过供应方平台(SSP)从出版商导入的交易，因此无需手动设置每个交易。 您可以接受已与出版商协商的有担保和无担保的私人库存交易 [!DNL FreeWheel]， [!DNL Google Authorized Buyers] (以前称为 [!DNL AdX])，以及 [!DNL Magnite DV+] (以前为 [!DNL Rubicon])中的 [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising DSP是第一个与集成的DSP [!DNL FreeWheel] API。

在 [!UICONTROL Deal ID inbox]，您可以在出版商看到交易详细信息时查看这些信息，加快交易设置并避免手动输入错误。

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.

You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP每天凌晨4:30（东部标准时间）自动刷新所有交易详细信息。 它还可以刷新所有 [!DNL FreeWheel] 来自以下项的现有交易和更新 [!DNL Google] 和 [!DNL Magnite DV+] 每小时。 您还可以随时手动刷新交易详细信息以填充新交易。

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>对于计划性保证交易，通过 [!DNL Google Authorized Buyers]，您必须交付至少90%的预算，否则您的帐户将无法访问 [!DNL Google] 中的交易 [!UICONTROL Deal ID inbox].

## 实施 [!UICONTROL Deal ID Inbox]

若要在中接收您的交易，请执行以下操作 [!UICONTROL Deal ID inbox]，则您的SSP帐户必须将贵组织的DSP帐户映射到您的SSP帐户。 DSP将与相关SSP共享组织的帐户名称。 有关说明，请联系您的Adobe客户团队。

在交易协商过程中，请让出版商将交易发送给您的买方，而不是发送给父DSP帐户。 交易标识符可以是名称或ID，具体取决于SSP。

## 您可以对交易执行的操作

* **审查交易** 验证SSP是否发送了正确的发布者、投放日期、CPM和其他交易详细信息。 如果发布者犯了错误，请在DSP之外联系他们，以便他们纠正并重新发送交易。

* **接受交易** 查看后，它们将不再出现在 [!UICONTROL Deal ID inbox]. 已接受的交易将列在 [!UICONTROL Inventory] > [!UICONTROL Deals] 并准备好在广告商投放位置内进行定位。

* **忽略交易** 不需要的或未经请求的。 被忽略的交易将移至 [!UICONTROL Ignored Deals] 选项卡位于 [!UICONTROL Deal ID inbox]，用作存档。 当您忽略交易时，DSP不会提醒SSP和发布者。

* **修改已接受交易的详细信息** 起始日期 [!UICONTROL Inventory] > [!UICONTROL Deals] (不在 [!UICONTROL Deal ID inbox])。 同样，当出版商对交易进行更改时，广告商负责实施这些更改 [!UICONTROL Inventory] > [!UICONTROL Deals] 因为 [!UICONTROL Deal ID inbox] 在设置交易后，不会从SSP同步更改。

## 哪些类型的交易不能被接受？

当交易列表不包含 ![接受](/help/dsp/assets/accept.png) 图标或 [!UICONTROL Accept] 按钮，您无法从 [!UICONTROL Deal ID inbox]. 相反，您可以 [手动创建交易标识详细信息](/help/dsp/inventory/deal-id-create.md).

您无法接受以下类型的交易：

* [!DNL Google] 非美元交易。

* [!DNL Magnite DV+] 非美元交易

* [!DNL FreeWheel] 不是以您帐户货币计价的交易。

* 结束日期早于今天的交易。

* 旧 [!DNL Magnite DV+] 标记为“多种媒体类型”的交易。

交易细节包括交易无法接受的原因。

>[!MORELIKETHIS]
>
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [库存功能概述](inventory-overview.md)

