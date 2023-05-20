---
title: 建立自訂目標的最佳實務
description: 瞭解建立自訂目標以定義成功事件的最佳實務。
feature: DSP Optimization, DSP Best Practices
exl-id: 8b1247cd-083d-4c8c-8588-9e8c03c4cc67
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# 建立自訂目標的最佳實務

## 具有單一屬性的自訂目標

下列範例說明如何設定以單一屬性（量度）為目標的目標。

### 具有「」的行銷活動範例[!UICONTROL Highest ROAS - Custom Goal]&quot;最佳化目標

如果您的行銷活動目標是收入([!UICONTROL Highest ROAS - Custom Goal])，則您的自訂目標（目標）將包含&quot;[!UICONTROL Revenue]權重為1 (1)的&quot;屬性。

![具有單一屬性的ROAS自訂目標範例](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] 對於所追蹤的每個$1收入，其中一個等於一個值。
>
> 例如，權重為1的$250轉換回報為$250。 如果轉換量度的權重為0.5，則Adobe廣告中的$250轉換會報告為$125 （$250轉換* 0.5） [!UICONTROL Property Weight] = $125)。

### 具有「」的行銷活動範例[!UICONTROL Lowest CPA - Custom Goal]&quot;最佳化目標

如果您的行銷活動目標是每次贏取的最低成本(CPA)，而且只需要一個成功事件，則您將包含一個量度（在以下範例中，「應用程式提交」）。 最佳實務是將權重設定為一(1)。

![具有單一屬性的CPA自訂目標範例](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] 對於所追蹤的每次轉換，一個ID就等於一個ID。
>
> 例如，如果追蹤10個「應用模組提交」轉換，則會報告10個「應用模組提交」轉換。  如果轉換量度的權重為0.5，則10次轉換在Adobe廣告中會報告為5 (5) （10次轉換* 0.5） [!UICONTROL Property Weight] = 5)。

## 具有多個屬性的自訂目標

在兩種情況下，您都可以在自訂目標中使用多個屬性：

* 您的行銷活動目標有多個成功事件。 例如，您可能正在針對多個網站上的動作進行廣告，而所有動作都歸因於您的CPA目標。 以下範例目標包含三個不同的屬性(PDF下載、聯絡我們和電子郵件註冊)，每個屬性的權重為1 (1)，這說明 [!DNL Adobe Sensei] 每個屬性具有相同重要性的演演算法。 如果您包含具有不同成本或重要性的屬性，則可以相應地調整其相對權重。

   ![具有多個屬性的自訂目標範例](/help/dsp/assets/custom-goal-multiple-properties.png)

* 自訂目標中的單一屬性未達到最佳化效能所需的最少每天10次轉換。 發生此狀況的原因可能是每天的套件支出極低或自然轉換次數有限。 將其他支援屬性新增至自訂目標可協助您達到每日10次轉換的臨界值。 10個支援事件可協助套件達到10/天臨界值，即使每個事件的權重低於一(1)也是如此。 但您不一定需要新增那麼多事件。

   將支援屬性新增至自訂目標時，請根據支援屬性對主要成功事件的相對重要性為其加權，並牢記資料點的數量。 這可讓Adobe Sensei演演算法平衡多個屬性，並針對您的目標最佳化。

   下列範例目標包含三個屬性，每個屬性都有不同的權重：應用模組提交= 1、應用模組開始= 0.1、廣告商登陸頁面= 0.01。這表示每個「應用程式提交」轉換對您的企業而言與平均10個「應用程式開始」轉換和100個「廣告商」登陸頁面轉換具有相同的值。

   ![具有多個屬性的自訂目標範例](/help/dsp/assets/custom-goal-multiple-properties2.png)

   反之，如果您將應用程式提交的登陸頁面造訪次數平均加權，則原本較高的登陸頁面造訪次數可能會壓倒您的目標，並扭曲至登陸頁面造訪次數。<!--reword-->

>[!MORELIKETHIS]
>
>* [關於自訂目標](custom-goal-about.md)
>* [建立自訂目標](custom-goal-create.md)
>* [最佳化目標及使用方式](optimization-goals.md)
>* [封裝設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何最佳化您的行銷活動](optimization-how-dsp-optimizes-campaigns.md)

