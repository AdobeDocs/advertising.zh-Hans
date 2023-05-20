---
title: 封裝設定
description: 請參閱可用封裝設定的說明。
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: 32d74703d9aecbddc5a5f3e0526a2cefbf1f2266
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 0%

---

# 封裝設定

## [!UICONTROL Basic Details]

**[!UICONTROL Name]：** 封裝名稱。 長度上限為60個字元。

**[!UICONTROL Description]：** （選用）封裝的說明。

**[!UICONTROL 3rd Party Billed Fees]：** （選用）作為不可開立帳單成本追蹤的靜態第三方費用：

>[!NOTE]
>
>可記帳費用會反映在 [!UICONTROL Net CPM] 量度。
* **[!UICONTROL CPM]：** 每1000次曝光的成本(CPM)。

* **[!UICONTROL CPM Description]：** CPM費用的說明。

您可以在以下位置覆寫套件層級設定： [位置層級](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]：** （現有套件的唯讀）在哪個層級調整並限制套件的位置：

* **[!UICONTROL Package level pacing]：** 此步調策略的運作方式是調整所有包含的刊登版位，並將其設為 *群組*. 此策略可確保指定封裝內的所有版位都經過整體最佳化，根據效能和規模將支出分配到選定的關鍵效能指標(KPI)。

* **[!UICONTROL Placement level pacing]：**  此步調策略的運作方式是調整所有包含版位的步調和上限 *個別*. 最佳實務是僅將此策略用於執行有保證的私人市集交易。

**[!UICONTROL Flight Dates]：** 套件的開始日期和結束日期。

若要選擇為套件建立非偶數步調航班，請選取 *[!UICONTROL *Activate Custom Flighting]**並在以下位置設定自訂航班： [!UICONTROL Flighting] 區段底下。 啟用自訂照明並儲存封裝後，您就無法停用自訂照明。

>[!NOTE]
>
>* 投放日期必須包含在行銷活動投放日期中。 此外，指派給此封裝的所有刊登版位的投放日期必須包含在這些日期中。
> * 啟用自訂熒光時，您無法編輯封裝開始日期。


**[!UICONTROL Budget]：** （僅具有套件層級步調的套件）總預算上限和預算間隔。

對於具有自訂燈光的封裝，預算間隔一律為 *[!UICONTROL All time]*. 對於沒有自訂燈光的封裝，請指定預算間隔： *[!UICONTROL All time]，* *[!UICONTROL Daily]，* *[!UICONTROL Monthly]，* 或 *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]：** （僅具有套件層級步調和動態利潤管理的套件）套件持續期間的毛預算上限。

**[!UICONTROL Optimization Goal]：** （僅具有套件層級步調的套件）套件的最佳化目標。 如需每個最佳化目標的說明，請參閱： [最佳化目標及使用方式](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goals]：** （僅具有自訂最佳化目標的套件） [自訂目標](/help/dsp/optimization/custom-goal-about.md) 適用於此封裝。 如需自訂目標的最佳實務和使用這些最佳實務的詳細資訊，請參閱  [建立自訂目標的最佳實務](/help/dsp/optimization/custom-goal-best-practices.md) 和 [設定效能行銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md).

**[!UICONTROL Package Goal Type]：** （僅具有自訂最佳化目標的套件）套件的用途。 此設定可協助判斷如何最佳化套件：

* *[!UICONTROL Prospecting]：* 潛在客戶套件著重於爭取新客戶。

* *[!UICONTROL Retargeting]：* 重新目標定位套件著重於重新公開先前的訪客或客戶。

* *[!UICONTROL Other]：* 所有其他用途。

**[!UICONTROL Linked Package for Optimization Learnings Carryover]：** （僅限具有自訂最佳化目標的套件）另一個套件，其歷史資料會作為最佳化套件的輸入。

**[!UICONTROL Target]：** （僅限套件層級步調的套件）用於追蹤效能的目標目標。

>[!NOTE]
>
>此欄位僅是基準，不用於決策。

**[!UICONTROL Frequency Cap]：** （僅限具有套件層級步調的套件）不重複裝置或個人的次數(取決於指定的 [!UICONTROL Cross Device Level] （適用於促銷活動）可從套件中提供廣告。 選項包括 *[!UICONTROL Unlimited]* 或每日、周或月的特定金額。

>[!NOTE]
>
>* 您可以在行銷活動、套件和位置層級設定頻率上限。 DSP遵循行銷活動階層中最嚴格的頻率上限。
>* 最佳實務是在套件層級設定潛在客戶與重新目標定位的頻率上限。
> * 頻率上限越高，支出和曝光率越高，但觸及率越低。 頻率上限越低，支出和曝光率就越低，但觸及率卻越高。


**[!UICONTROL Pace on]：** （僅限套件層級步調的套件）步調基準：

* *[!UICONTROL Budget]：* （預設）此選項會在配置的套件預算內提供儘可能多的曝光次數。

* *[!UICONTROL Impressions]：* 此選項會傳送曝光次數，直到在指定的間隔內達到指定的數量為止。 選取此選項時，請指定曝光次數和間隔： *所有時間，* *[!UICONTROL Daily]，* *[!UICONTROL Monthly]，* 或 *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]：** （僅具有套件層級步調的套件）如何在整個航班中步調和傳遞：

* *[!UICONTROL Even]：* 每個航班的傳送進度都相同，目標是在航班的前半段50%的傳送。

* *[!UICONTROL Slightly Ahead]：* （預設）加快傳遞，使其在飛行期間的中途完成55-65%。

* *[!UICONTROL Frontload]：* 加速傳遞，讓整個行程的中途完成65-75%。

* *[!UICONTROL Aggressive Frontload]：* 加速傳遞，讓整個行程的中途完成75-85%。

**[!UICONTROL Intraday pacing]：** （僅含套件層級步調的套件）如何在飛行中每天進行廣告投放步調：

* *[!UICONTROL Even]：* （預設）根據存貨可用性調整交貨規模。 通常，當拍賣量較高時，白天每小時會傳送更多廣告，而早上和晚上會傳送較少廣告。

* *[!UICONTROL ASAP]：* 將傳送速度加快至兩倍 *平均*.

   >[!CAUTION]
   >
   >此選項可能會對效能造成負面影響。 只有在您完全排定傳遞的優先順序，且花費在效能最佳化之上，才使用它。

## [!UICONTROL Flighting]

(具有套件層級步調和具有&quot;[!UICONTROL Activate Custom Flighting]&quot;已啟用)整體內的自訂投放期間 [!UICONTROL Flight Dates] 指定於 [!UICONTROL Goals & Budget] 區段。

針對每個航班，輸入開始日期、結束日期和目標曝光次數。 若要新增其他航班，請按一下 **[!UICONTROL Add Flight]**.

>[!MORELIKETHIS]
>
>* [關於封裝管理](package-about.md)
>* [建立套裝](package-create.md)
>* [編輯套裝](package-edit.md)
>* [將位置附加至封裝](package-attach-placement.md)
>* [檢視套裝程式的變更記錄](package-change-log.md)
>* [Campaign Management常見問題集](/help/dsp/campaign-management/faq-campaign-management.md)

