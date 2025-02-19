---
title: 关于[!UICONTROL Deal ID Inbox]
description: 了解[!UICONTROL Deal ID inbox]功能，该功能允许您接受已在 [!DNL FreeWheel], [!DNL Google Authorized Buyers] (以前称为 [!DNL AdX]), and [!DNL Magnite DV+] （以前称为 [!DNL Rubicon]）)上与发布者协商的私人交易。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: 394a281c9b9d7eeab939f4c58508ec1f34eba67c
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# 关于[!UICONTROL Deal ID Inbox]

Advertising DSP [!UICONTROL Deal ID inbox]允许您快速设置DSP通过供应方平台(SSP)从出版商导入的交易，因此您不必手动设置每个交易。 您可以接受已在[!UICONTROL Deal ID inbox]的[!DNL FreeWheel]、[!DNL Google Authorized Buyers] （以前称为[!DNL AdX]）和[!DNL Magnite DV+] （以前称为[!DNL Rubicon]）上与发布者协商的有保证和未保证的私有库存交易。

>[!NOTE]
>
>Advertising DSP是第一个与[!DNL FreeWheel] API集成的DSP。

在[!UICONTROL Deal ID inbox]中，您可以看到出版商看到的交易详细信息，从而加快交易设置速度，避免手动输入错误。

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.

You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP每天凌晨4:30（东部标准时间）自动刷新所有交易详细信息。 它还每小时刷新所有[!DNL FreeWheel]交易并更新[!DNL Google]和[!DNL Magnite DV+]中的现有交易。 您还可以随时手动刷新交易详细信息以填充新交易。

<!-- MC: I'm not sure where I got the following. Is this currently true? -->

>[!NOTE]
>
>对于通过[!DNL Google Authorized Buyers]进行的计划性保证交易，您必须交付至少90%的预算，否则您的帐户将无法访问[!UICONTROL Deal ID inbox]中的[!DNL Google]交易。

## 实施[!UICONTROL Deal ID Inbox]

若要在[!UICONTROL Deal ID inbox]中接收您的交易，您的SSP帐户必须将贵组织的DSP帐户映射到您的SSP帐户。 DSP可以与相关SSP共享组织的帐户名称。 有关说明，请联系您的Adobe客户团队。

在交易协商过程中，请让出版商将交易发送给您的买方，而不是发送给父DSP帐户。 交易标识符可以是名称或ID，具体取决于SSP。

## 您可以对交易执行的操作

* **审查交易**，以验证SSP是否发送了正确的发布者、投放日期、CPM和其他交易详细信息。 如果发布者出了错，请在DSP之外联系他们，以便他们纠正并重新发送交易。

* 审阅后&#x200B;**接受交易**，这些交易不再出现在[!UICONTROL Deal ID inbox]中。 已接受的交易在[!UICONTROL Inventory] > [!UICONTROL Deals]中列出，并准备好在广告商的投放位置中定位。

* **忽略不需要或未经请求的交易**。 已忽略的交易被移至[!UICONTROL Deal ID inbox]内的[!UICONTROL Ignored Deals]选项卡，该选项卡用作存档。 当您忽略交易时，DSP不会提醒SSP和发布者。

* 从[!UICONTROL Inventory] > [!UICONTROL Deals] （不在[!UICONTROL Deal ID inbox]中）修改已接受交易的详细信息&#x200B;**。**&#x200B;同样，当发布者将更改发送到交易时，广告商负责在[!UICONTROL Inventory] > [!UICONTROL Deals]中实施这些更改，因为[!UICONTROL Deal ID inbox]在交易设置后不会从SSP同步更改。

## 哪些类型的交易不能被接受？

当交易列表不包含![接受](/help/dsp/assets/accept.png)图标或[!UICONTROL Accept]按钮时，您无法从[!UICONTROL Deal ID inbox]接受该列表。 您可以[手动](/help/dsp/inventory/deal-id-create.md)创建交易ID详细信息。

您不能接受以下类型的交易：

* [!DNL Google]个非美元交易。

* [!DNL Magnite DV+]个非美元交易

* [!DNL FreeWheel]个交易未使用您的帐户货币。

* 结束日期早于今天的交易。

* 标记为“多种媒体类型”的旧[!DNL Magnite DV+]交易。

交易细节包括交易无法接受的原因。

>[!MORELIKETHIS]
>
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [清单功能概述](inventory-overview.md)
