---
title: 關於 [!UICONTROL Deal ID Inbox]
description: 瞭解 [!UICONTROL Deal ID inbox] 功能，可讓您接受已與發佈商議定的私人交易 [!DNL FreeWheel], [!DNL Google Authorized Buyers] (先前稱為 [!DNL AdX]), and [!DNL Magnite DV+] (先前稱為 [!DNL Rubicon])。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# 關於 [!UICONTROL Deal ID Inbox]

Advertising DSP [!UICONTROL Deal ID inbox] 可讓您快速設定DSP透過供應端平台(SSP)從發佈者匯入的交易，因此您不必手動設定每個交易。 您可以接受已與發佈商商議的已保證和未保證私人詳細目錄交易 [!DNL FreeWheel]， [!DNL Google Authorized Buyers] (先前稱為 [!DNL AdX])，以及 [!DNL Magnite DV+] (先前稱為 [!DNL Rubicon])從 [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising DSP是第一個與整合的DSP [!DNL FreeWheel] API。

在 [!UICONTROL Deal ID inbox]，您可以在發行者看到交易詳細資訊時檢視這些資訊，加速交易設定，並避免手動輸入錯誤。

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.

You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP每天於東部標準時間凌晨4:30自動重新整理所有交易細節。 它也會重新整理所有 [!DNL FreeWheel] 交易和更新來自的現有交易 [!DNL Google] 和 [!DNL Magnite DV+] 每小時。 您也可以隨時手動重新整理交易詳細資料，以填入新交易。

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>針對程式化預留交易，透過 [!DNL Google Authorized Buyers]，您必須交付至少90%的預算，否則您的帳戶將無法存取 [!DNL Google] 中的交易 [!UICONTROL Deal ID inbox].

## 實作 [!UICONTROL Deal ID Inbox]

若要在中接收您的交易 [!UICONTROL Deal ID inbox]，您的SSP帳戶必須將您組織的DSP帳戶對應至您的SSP帳戶。 DSP會與相關SSP共用組織的帳戶名稱。 如需指示，請聯絡您的Adobe客戶團隊。

在交易洽談期間，請告訴發行者將交易傳送給您的購買者，而不是傳送給上層DSP帳戶。 交易識別碼可以是名稱或ID，具體取決於SSP。

## 您可以對交易採取的動作

* **檢閱交易** 確認SSP已傳送正確的發佈者、航班日期、CPM和其他交易詳細資料。 如果發行者發生錯誤，請在DSP外部聯絡他們，以便他們更正並重新傳送交易。

* **接受交易** 檢閱後，這些區段將不再出現在 [!UICONTROL Deal ID inbox]. 接受的交易列於 [!UICONTROL Inventory] > [!UICONTROL Deals] 並準備好在廣告商的位置內鎖定目標。

* **忽略交易** 不需要或未經請求的物件。 忽略的交易會移至 [!UICONTROL Ignored Deals] 標籤內的 [!UICONTROL Deal ID inbox]，可作為封存。 當您忽略交易時，DSP不會提醒SSP和發佈者。

* **修改已接受交易的詳細資料** 從 [!UICONTROL Inventory] > [!UICONTROL Deals] (不在 [!UICONTROL Deal ID inbox])。 同樣地，當發佈商傳送變更至交易時，廣告商負責實作這些變更 [!UICONTROL Inventory] > [!UICONTROL Deals] 因為 [!UICONTROL Deal ID inbox] 在設定交易後，不會同步來自SSP的變更。

## 無法接受哪些型別的交易？

當交易清單不包含 ![Accept](/help/dsp/assets/accept.png) 圖示或 [!UICONTROL Accept] 按鈕，則無法從 [!UICONTROL Deal ID inbox]. 反之，您可以 [手動建立交易識別碼詳細資料](/help/dsp/inventory/deal-id-create.md).

您無法接受下列交易型別：

* [!DNL Google] 非美元交易。

* [!DNL Magnite DV+] 非美元交易

* [!DNL FreeWheel] 不是以您帳戶貨幣計值的交易。

* 結束日期早於今天的交易。

* 舊 [!DNL Magnite DV+] 標籤為「多種媒體型別」的交易。

交易詳細資訊包括無法接受交易的原因。

>[!MORELIKETHIS]
>
>* [在交易ID收件匣中接受交易](deal-id-inbox-accept.md)
>* [庫存功能概要](inventory-overview.md)

