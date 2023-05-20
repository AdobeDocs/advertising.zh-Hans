---
title: 疑難排解效能
description: 參考常見的效能問題，並瞭解如何疑難排解。
feature: DSP Optimization
exl-id: b87f8556-1908-40c1-9f98-fbdc6d9b59b1
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# 疑難排解效能

| 問題 | 可能的原因 | 要採取的動作 |
| --- | --- | --- |
| 投放無需花費 | 位置不包含廣告，和/或廣告未啟用。 | 確認所有預期的廣告皆已附加至投放位置，且已核准及啟用。<br><br>另請參閱投放位置是否包含自訂廣告排程，這可能會限制每個廣告的投放時間。 若要從「版位」檢視中檢視版位的廣告排程，請按一下  **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]** 位置名稱旁邊。 |
|  | 受影響的日期不在設定的投放日期內。 | 檢查投放日期在行銷活動、套件和版位層級是否有效&#x200B;。 |
|  | 預算目標已達成及/或不夠高。 | 檢查行銷活動、套件和版位等級的預算設定。 |
|  | 帳戶沒有足夠的資金。 | 若要檢視您的帳戶是否有足夠的資金，請前往 **[!UICONTROL Settings]** > **[!UICONTROL Account]** 並檢視 [!UICONTROL Usable Funds]. 如果您需要新增更多資金，請聯絡您的Adobe客戶團隊。 |
|  | 沒有可用的詳細目錄。 | 驗證指定的存貨來源([!UICONTROL Public]， [!UICONTROL Private]，或 [!UICONTROL On Demand])為：<ul><li>正確設定。</li><li>透過拍賣啟用和傳送。</li><li>與適用的廣告和版位型別相容。</li></ul><br>如果存貨來源全部有效且有效，則儘可能鎖定其他或所有存貨來源。 |
|  | 沒有可用的使用者。 | 檢查指定的對象目標是否包含足夠的活躍使用者。 如果沒有，請新增更多對象以展開目標。 |
| 投放費用低 | 此 [!UICONTROL Non Bids] 「位置診斷」報表的區段會顯示位置未競標的可能原因。 | [檢閱 [!UICONTROL Non Bids] 報告](/help/dsp/campaign-management/reports/placement-diagnostics.md) 以瞭解位置未競標的原因。  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
|  | 位置使用 [競標前篩選](/help/dsp/campaign-management/placements/placement-settings.md) 限制競標。 | 將競標前篩選器的臨界值降低5%，以評估支出與效能的平衡。 <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>請記住，使用多個位置目標（例如競標前篩選、地理位置、詳細目錄和對象）可能會累積限制競標和支出。 |
|  | 此位置的贏取率很低。 | 增加 [!UICONTROL Max Bid] 以提升獲勝率。<br><br><b>注意：</b> 存貨價格可能會因位置鎖定目標而異。<br><br>10%的獲勝率被認為是健康的。 |
|  | 可用庫存數量低。 | 儘可能鎖定其他或所有存貨來源。<br><br>請記住，使用多個位置目標（例如競標前篩選、地理位置、詳細目錄和對象）可能會累積限制競標和支出。 |
|  | 可用使用者人數少。 | 檢查指定的對象目標是否包含足夠的活躍使用者。 如果沒有，請新增更多對象以展開目標。<br><br>請記住，使用多個位置目標（例如競標前篩選、地理位置、詳細目錄和對象）可能會累積限制競標和支出。 |
|  | 此套件包含大量作用中的位置。 | 請減少套件中的作用中位置數量或增加整體套件預算。<br><br>如果套件有許多版位，但預算不足，DSP可能無法為每個版位分配足夠的預算。 每個位置應有機會每天至少花費2美元。 例如，如果您的套件預算為每天10美元，則最好包含五個或更少的版位。&#x200B;URL |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [Campaign設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)

