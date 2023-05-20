---
title: Campaign Management常見問題集
description: 進一步瞭解行銷活動管理，包括變更的延遲期間，以及您在飛行期間變更預算時會發生什麼情況。
feature: DSP Packages, DSP Placements
exl-id: 8a443543-ebb1-4273-a007-afef07d32d8c
source-git-commit: 2fb3f227d74d8c8893a3cb042ea91121a0fae7c0
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Campaign Management常見問題集

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## 設定變更的延遲

* 當您變更位置或封裝設定時，變更何時生效？

   設定變更通常會立即生效，但最多可能需要12小時。

   如果這是交付的最後一天，請在當天早些時候進行變更，以便DSP有充足的時間根據變更重新校準套件。 例如，如果您從偶數步調變更為前載步調，DSP需要重新評估在整個飛行剩餘時間內它將如何分配支出。 如果您在航班的最後一天只剩一小時可送達，請勿進行這類變更。

## 飛行中間的預算更新

* 若您變更版位，DSP需要多久的時間重新分配套件預算？

   預算配置是以位置績效為基礎，評估方式為平均14天。 只有當位置變更在14天平均時間內導致績效變更時，才會導致預算配置變更。

   當發生效能變更時，DSP會在下一個預算最佳化週期(大約在行銷活動時區的午夜(00:00))期間，在版位之間相應地重新分配套件預算。

* 從套件中移除版位並新增至另一個套件時，如何重新分配預算？

   位置的整個花費歷史記錄會附加於位置，並隨位置在不同封裝之間移動。

   當您從套件中移除版位時，套件不再具有任何版位支出的歷史記錄。 套件預算將變成（套件預算 — 移除版位預算）/剩餘投放時間間隔。 然後，套件預算會分配至套件中剩餘的版位。

   同樣地，如果您將相同版位新增至不同的套件，DSP會在為新套件中的所有版位分配預算時，考量版位的支出歷史記錄。

* 套件步調在飛行最後一天會有何改變？

   在航班的最後一天，該日會從24小時縮短為23小時，這樣就不會超出套件預算。 此外，套件的步調填充策略會自動變更為&quot;[!UICONTROL Frontload]，」，即使它設定為「[!UICONTROL even].」 這表示每日預算的65%應在東部標準時間上午11:30前交付。

>[!MORELIKETHIS]
>
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [設定效能行銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md)

