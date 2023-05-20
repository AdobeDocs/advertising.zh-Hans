---
title: 關於 [!UICONTROL Simple Ad Serving]
description: 瞭解 [!UICONTROL Simple Ad Serving] 使用事件追蹤畫素進行交易。
feature: DSP Simple Ad Serving
exl-id: 327a2c93-d729-42e1-856f-f0e05efab7ca
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# 關於 [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] 為指定的發佈者以及使用單一專用版位的單一廣告型別，提供有保證的非決策廣告傳送和報告。 使用 [!DNL Simple Ad Serving] 當您的發行者無法透過交易ID執行您的交易時。 所有目標定位、預算步調和上限，以及頻率上限都由發佈商處理。 透過事件追蹤畫素執行這些交易。

替換為 [!UICONTROL Simple Ad Serving]，每個廣告會由發佈者（網站服務）直接提供，而DSP會提供事件追蹤畫素以傳送給發佈者，而發佈者必須實作畫素並流量DSP廣告。 視詳細目錄型別而定，事件畫素會測量曝光數、點進次數和視訊播放事件。

可使用下列廣告型別：

* 案頭標準前段廣告
* 平板電腦和行動標準前段廣告
* 連線電視標準前段
* 顯示
* 音訊

您可以建立 [!UICONTROL Simple Ad Serving] 交易於 [!UICONTROL Inventory] > [!UICONTROL Deals] 檢視。 DSP會自動產生具有子型別的位置&quot;[!DNL Simple ad serving]」代表廣告。 位置鎖定交易，但不允許額外的目標定位、預算或頻率上限。 您只能編輯部分交易設定，例如交易名稱、CPM、曝光次數和投放日期。<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving] 刊登版位不符合帳戶的可用資金或行銷活動與套件預算。 但是，支出會被追蹤並計入這些預算。 即使CPM為$0，系統仍會追蹤事件資料。

>[!MORELIKETHIS]
>
>* [建立 [!UICONTROL Simple Ad Serving] 交易](simple-deal-create.md)
>* [編輯 [!UICONTROL Simple Ad Serving] 交易設定](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving] 設定](simple-deal-settings.md)
>* [檢視交易的詳細報告](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
