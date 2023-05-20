---
title: 位置層級的競標前篩選條件及其使用方式
description: 參考可用的位置層級競標前篩選條件，並瞭解其使用方式。
feature: DSP Optimization
exl-id: 34a15666-7ca2-416d-9064-8638ca81e5b3
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# 位置層級的競標前篩選條件及其使用方式

| 競標前篩選 | 描述 | 使用此篩選器的時間 |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | 設定拍賣導致點進的機率的最小預測臨界值。 例如，如果您將臨界值設為0.1%，則除非預測的點按機率大於或等於0.1%，否則將不會在拍賣上競標。<br><br><b>注意：</b> 篩選器會在最佳化目標之前套用。 因此，非常嚴格的篩選條件可以防止支出。 | 若您有最低點進率(CTR)的KPI目標，且當CTR低於臨界值時不想花費預算，請使用。 此篩選器可能相當具限制性，因此設定現實目標很重要。 根據位置的其他限制，03-07%的目標通常是良好的起點。 您可以視需要在網站層級最佳化此專案，以協助改善量度。<br><br>如果您的目標是實現最小CTR和最佳可能的CPM，則建議的設定為合併 [!UICONTROL Click Through Rate] 以最佳化目標篩選»[!UICONTROL Lowest CPM].」 如果您的目標是最大CPM而沒有實際超額實現效益和最小CTR，則配對 [!UICONTROL Click Through Rate] 以最佳化目標篩選»[!UICONTROL Always Max Bid + Highest CTR]「可能更合適。 |
| [!UICONTROL 100% Completion Rate] | 設定您對曝光出價前必須符合的必要最低完成率。 | 當行銷活動的主要目標是完成率時，請使用此篩選器。 其他鎖定目標引數中的因子，但建議起始百分比為65%。 |
| [!UICONTROL Player Size - Adobe] | 使用DSP中的資料設定所需的最小播放器大小。 當下列情況下，您會根據曝光次數投標： [!UICONTROL Player Size] 已符合臨界值。 | 使用可確保您可使用DSP中的資料完成全集播放器詳細目錄。 |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | 使用下列來源的資料，設定所需的最小播放器大小： [!DNL Moat] 或 [!DNL Integral Ad Science] ([!DNL IAS])。 當下列情況下，您會根據曝光次數投標： [!UICONTROL Player Size] 已符合臨界值。 | 使用可確保您透過平台範圍的全集播放器詳細目錄 [!DNL Moat] 或 [!DNL IAS] 資料。<br><br><b>注意：</b> 只有在行銷活動設定為使用時，才使用此篩選器 [!DNL Moat] 或 [!DNL IAS] 資料。 |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | 使用DSP可檢視度數字和測量，設定必要的最小可檢視度百分比。 當符合指定的臨界值時，您會對曝光次數投標。<br><br><b>附註：</b><ul><li>如果行銷活動的 [!UICONTROL Viewability Sensitivity] 設定為&quot;[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]，」然後 [!DNL Media Rating Council] (MRC)可檢視度測量標準用於行銷活動。 如果 [!UICONTROL Viewability Sensitivity] 設定為&quot;[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]，」然後 [!DNL GroupM] 行銷活動會使用可見度測量標準。</li><li>Adobe測量定義與第三方定義不同，因此可能與第三方資料略有差異。</li></ul> | 最佳實務建議將最佳化目標和任何競標前篩選設定與行銷活動的 [!UICONTROL Viewability Sensitivity] 設定。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [DSP如何最佳化您的行銷活動](optimization-how-dsp-optimizes-campaigns.md)
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Campaign設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [最佳化目標及使用方式](optimization-goals.md)

