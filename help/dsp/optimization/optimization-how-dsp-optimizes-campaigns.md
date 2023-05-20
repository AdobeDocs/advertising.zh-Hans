---
title: DSP如何最佳化您的行銷活動
description: 瞭解DSP如何最佳化行銷活動中的套件。
feature: DSP Optimization
exl-id: 92d411cf-4307-4449-97b4-da3817f2a0b4
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Advertising DSP如何最佳化您的行銷活動

本頁面概述DSP最佳化引擎的工作原理，該引擎由 [!DNL Adobe Sensei]，會最佳化行銷活動中的套件。 如需手動最佳化行銷活動的秘訣與技巧，請聯絡您的Adobe客戶團隊。 <!-- add link to trading playbook if we add it to help -->

套件最佳化目標會在兩個層級運作：

* 對於每個套件：DSP會根據套件中每個版位的績效與所選KPI分配預算給該版位。

* 對於套件中的每個刊登版位/拍賣： DSP會計算每個刊登版位中每個拍賣的即時經濟KPI值，然後使用此值來決定出價。

   >[!NOTE]
   >
   >經濟價值會根據投放的花費程度而大幅加權。 如果刊登版位落後於其支出目標，則可購買品質較低的拍賣。 如果刊登版位輕鬆達成其支出目標，則會專注於更高品質的拍賣。

## 套件最佳化

DSP可以透過兩種基本方式將傳送最佳化，並提供20種變數，以符合您的特定效能目標。 您可以選擇：

* 排定效能比率的優先順序

* 優先權平衡成本效益與效能比

另請參閱 [最佳化目標及使用方式](optimization-goals.md) 以判斷哪個最佳化目標可協助您達成KPI。

### 排定效能率優先順序的套件

針對將效能比率排定優先順序的最佳化目標，DSP會預測每個拍賣的效能，並一律以最高出價競標。 適用的最佳化目標範例包括 [!UICONTROL Highest Viewability Rate]， [!UICONTROL Highest Clickthrough Rate]、等等。

此最佳化模式適用於以下情況：

* 您已經知道有效/可接受的CPM層次（例如，歷史基準）。

* 您願意手動調整 [!UICONTROL Max Bid] 如果您在縮放時遇到挑戰，請針對每個位置。

* 您將規模優先於效率。

#### 步調邏輯 {#pacing-logic-performance}

* 如果支出如期進行，出價將更具選擇性，因此您只能在預計具有高績效率的拍賣會上出價。

* 如果支出落後於節奏，競標就會變得較不挑剔，因此您會在預計效能率較低的拍賣會上競標，以趕上節拍目標。

#### 清除價格/競標陰影 {#clearing-price-performance}

DSP執行步調邏輯後，會透過結算價格預測模型執行建議的競標。 如果預測指出出價可以以最低的獲勝率下降而降低，則根據預測，出價會降低。

### 將成本效益與效能比率加以平衡排定優先順序的套件

針對某些最佳化目標，DSP會預測每個拍賣的效能，並自動調整競標價格，而不會超過刊登版位 [!UICONTROL Max Bid]. 適用的最佳化目標範例包括 [!UICONTROL Lowest CPM]， [!UICONTROL Lowest CPA]， [!UICONTROL Lowest Cost per View]， [!UICONTROL Lowest Cost per Click]、等等。

#### 步調邏輯 {#pacing-logic-balanced}

* 如果支出在節奏，DSP就會變得對價格更加敏感，會以較低的價格出價，來權衡節拍計畫的優惠率。

* 如果同時平衡績效量度（所有目標除外） [!UICONTROL Lowest CPM])，則預測的KPI會混合到競標量中。 因此，根據「每筆成本」的預測，競標效能會更高。

* 如果支出跟不上節奏，DSP就會降低價格敏感性，而出價會提高，最高可達 [!UICONTROL Max Bid]，以利用步調計畫來平衡獲勝率。

#### 清除價格/競標陰影 {#clearing-price-balanced}

DSP執行步調邏輯後，會透過結算價格預測模型執行建議的競標。 如果預測指出出價可以以最低的獲勝率下降而降低，則根據預測，出價會降低。

## 位置最佳化

位置競標前篩選是確保強大效能的最嚴格方式。 DSP會策略性地跨不同的廣告型別使用競標前篩選器，以達到每個套件中各個位置的效能目標。 您可以與套件層級最佳化同時或單獨使用競標前篩選器。

>[!NOTE]
>
>可用的競標前篩選器會依廣告型別而異。 例如，對於標準顯示位置，您可以按點進率和可檢視度進行篩選，但不能按完成率進行篩選。

另請參閱 [位置層級的競標前篩選條件及其使用方式](optimization-pre-bid-filters.md) 以判斷哪個競標前篩選器可協助您達成KPI。

>[!MORELIKETHIS]
>
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [位置設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [最佳化目標及使用方式](optimization-goals.md)
>* [位置層級的競標前篩選條件及其使用方式](optimization-pre-bid-filters.md)
>* [疑難排解效能](/help/dsp/optimization/troubleshooting-performance.md)

