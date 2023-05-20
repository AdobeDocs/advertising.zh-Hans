---
title: 復製版位
description: 瞭解如何複製一或多個版位。
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# 復製版位

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

複製一或多個版位，以使用類似設定建立版位。 您可以：

* 建立多個版位重複專案
* 在原始廣告商和行銷活動內或不同廣告商和行銷活動內復製版位
* （適用於原始行銷活動內的重複版位）可選擇複製原始廣告
* 修改新刊登版位的狀態和投放日期

請參閱「[未複製的內容](#placement-not-duplicated)」以取得未複製的位置設定清單。

1. 在主功能表中，按一下 **[!UICONTROL Campaigns]**.

1. 按一下行銷活動的名稱。

1. 在子功能表中，按一下 **[!UICONTROL Placements]**.

1. 執行下列任一項作業：

   * 若要複製一個版位，請按一下  **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** 位於封裝名稱旁。

   * 若要複製多個版位：

      1. 選取要複製的每個位置旁的核取方塊。

      1. 在大量動作工具列中，按一下 **[!UICONTROL Duplicate]**.

1. 指定新的位置設定：

   1. （單一版位）輸入新版位名稱。

   1. 在 **[!UICONTROL Choose Package (Required)]** 功能表，選取父套件或**[!UICONTROL No package]*.

   1. （選用）變更預設設定。

   這些設定會套用至所有選取的版位。

   依預設，新版位會針對原始廣告型別、指派給原始廣告商和促銷活動、具有從當天開始的航班時刻表、會暫停且不包含原始廣告。

   當您建立多個版位時，新版位名稱會依序附加一個數字，使用的慣例為&lt;*original_placement_name #N*>，例如「我的版位#2」。

1. 单击 **[!UICONTROL Submit]**.

## 未複製的內容 {#placement-not-duplicated}

來自原始版位的所有設定都會重複，除了：

* 實驗設定
* （如果您變更投放日期）自訂廣告排程
* （如果您未附加廣告）自訂廣告權重和排程
* 程式保證(PG)交易的預設刊登版位和刊登版位 [!UICONTROL Simple Ad Serving] 交易
* （如果您將版位複製到其他行銷活動）：
   * 地理目標
   * 事件畫素
   * 廣告
   * 位置層級 [!DNL DoubleVerify Authentic Brand Safety] 區段（覆寫廣告商層級區段）

>[!MORELIKETHIS]
>
>* [關於版位管理](placement-about.md)
>* [建立位置](placement-create.md)
>* [編輯位置](placement-edit.md)
>* [檢視位置的變更記錄](placement-change-log.md)
>* [位置設定](placement-settings.md)

