---
title: 在Analysis Workspace中Adobe廣告量度
description: 在Analysis Workspace中Adobe廣告量度
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: 5dd3772de945660e76321dac935de5ebcab5979a
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# 在Analysis Workspace中Adobe廣告量度

*僅具有AdobeAdvertising-Adobe Analytics整合的廣告商*

>[!NOTE]
>
>* Adobe Advertising傳遞流量量度和維度至 [!DNL Analytics] 每日。
>* [!DNL Analytics] 即時擷取Adobe廣告點進和檢視點進。
   > 對象 [!DNL Search, Social, & Commerce]，大部分的廣告網路和行銷活動型別都支援此功能。 請參閱「 」中的「支援的詳細目錄」 [!DNL Search, Social, & Commerce] 指南，以取得詳細資訊。<!-- add link when that's published in ExL -->


## Adobe廣告的流量量度

>[!NOTE]
>
>中的所有Adobe廣告流量量度 [!DNL Analytics] 從「AMO」開始。

| 流量量度 | 描述 |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Adobe廣告曝光次數。 |
| [!UICONTROL AMO Clicks] | Adobe廣告點按總數。 |
| [!UICONTROL AMO Cost] | Adobe廣告支出（以報表套裝的貨幣表示）。 |
| [!UICONTROL AMO ID Instance] | Adobe廣告ID的設定次數。 |
| [!UICONTROL AMO Minutes Viewed] | Adobe廣告影片被檢視的分鐘數。 |
| [!UICONTROL AMO Views] | 廣告檢視次數。 當檢視者啟動Adobe廣告視訊時，即會計入檢視。 |
| [!UICONTROL AMO Views 25% Complete] | 觀看了至少25%之Adobe廣告影片的人數。 |
| [!UICONTROL AMO Views 50% Complete] | 觀看了至少50%之Adobe廣告影片的人數。 |
| [!UICONTROL AMO Views 75% Complete] | 觀看至少75%的Adobe廣告影片觀看次數。 |
| [!UICONTROL AMO Views 100% Complete] | 觀看100%Adobe廣告影片的觀看次數。 |
| [!UICONTROL AMO Viewable Impressions] | 根據版位組態測量為可檢視的曝光次數。 |
| [!UICONTROL AMO Not Viewable Impressions] | 判斷為無法檢視的曝光次數。 此值的計算方式為([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable])。 |
| [!UICONTROL AMO Measurable Impressions] | 提供的可檢視度檢測已成功初始化的曝光次數。 此值的計算方式為（檢測的曝光次數 — 無法測量的曝光次數）。 |

## Adobe廣告Dimension

>[!NOTE]
>
>中的所有Adobe廣告維度 [!DNL Analytics] 後面接著「(AMO ID)」。

| Dimension | 適用的Adobe廣告資料 | 描述 |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 廣告DSP或搜尋引擎名稱 |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 帳戶名稱。 |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | RTB ([!DNL DSP])或廣告網路名稱([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 行銷活動名稱。 |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 套件([!DNL DSP])或投資組合([!DNL Search, Social, & Commerce])名稱。 |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] 資料 | 位置名稱。 |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 廣告群組名稱。 |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 關鍵字。 |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 搜尋相符型別。 |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 關鍵字和相符型別。 |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 廣告型別，例如 `text`， `video`， `display`，或 `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 廣告型別([!DNL DSP])或廣告標題([!DNL Search, Social, & Commerce])。 |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 廣告說明([!DNL DSP])或廣告內文([!DNL Search, Social, & Commerce])。 |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 廣告中顯示的URL。 |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 廣告的目的地URL。 |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] 和 [!DNL Search, Social, & Commerce] 資料 | 登入頁面專案是檢視還是點進。 |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] 資料 | 產品清單廣告的產品目標。 |

## 適用於Adobe廣告的自訂計算量度

請考慮為您的Adobe廣告資料建立下列量度。

* 登陸頁面例項的點按次數([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks])：這是點選廣告並進入登陸頁面的人數%。
* 可測量的比率([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* 可檢視的曝光率([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* 每次檢視成本([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* 每次點按成本([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Adobe廣告中的資料](/help/integrations/analytics/analytics-data-in-advertising.md)

