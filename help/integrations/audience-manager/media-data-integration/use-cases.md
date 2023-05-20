---
title: 使用案例
description: 瞭解與Audience Manager共用您的Advertising DSP媒體資料的使用案例
feature: Integration with Adobe Audience Manager
exl-id: 1d961799-b8be-499a-8db6-b59762d96bf1
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# 在Adobe Audience Manager中擷取媒體曝光資料的使用案例

*僅使用Advertising DSP的廣告商*

*僅具有AdobeAdvertising-Adobe Audience Manager整合的廣告商*

以下是擷取Advertising DSP媒體曝光度資料可讓您受益的一些方式 <!-- ad impression data? --> 在Audience Manager中。

## 造訪間隔和頻率管理

擷取Audience Manager中的曝光資料，可讓您建立已接觸到特定廣告或行銷活動的使用者區段，藉此增強頻率管理。 如果您想要提高頻率，可以使用這些區段進行廣告目標定位，或者如果您想要限制頻率，則可以使用這些區段進行廣告隱藏。

此外，透過Audience Manager [!DNL Segment Builder]，您可以套用 [造訪間隔和頻率控制項](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) 至任何 [規則型特徵](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) 包含可操作訊號的。 舉例來說，這可讓您限制在媒體行銷活動中向使用者展示特定創意內容的次數。 讀取»[即時跨裝置隱藏](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)」以瞭解如何執行此操作。<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## 順序訊息

透過擷取曝光資料，您可以建立已曝光於行銷活動或廣告的使用者區段，並使用此區段進行循序傳訊或隱藏。 例如，您可以重新鎖定看到創意內容的使用者 `123` 但並未藉由顯示創意來點選或轉換 `456`.

若要以Audience Manager執行此範例，請遵循下列步驟：<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. 建立特徵以擷取看過該創意內容的使用者。

   例如，為特徵命名 `Creative Trait 123`，使用下列特徵規則：

   ```
   d_creative == 123 AND d_event == imp
   ```

1. 建立特徵以擷取點選或轉換的使用者。

   例如，若要命名此特徵 `Click and Converter`，使用下列特徵規則：

   ```
   d_event == click OR d_event=conv
   ```

1. 建立名為的區段 `Retarget Users` 填入看到創意的使用者 `123` 但未點按或轉換。 使用下列特徵規則：

   ```
   Creative Trait 123 AND NOT Click and Converter
   ```

1. 對應區段 `Retarget Users` 至目的地，並透過創意以目的地中的使用者為目標 `456`.

## [!DNL Adobe Audience Analytics] 和行銷活動曝光度資料

在Audience Manager中可以使用行銷活動的曝光次數和點選次數資料後，您就可以建立接觸或互動特定行銷活動或策略的使用者特徵和區段。 使用 [[!DNL Audience Analytics] 整合](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)，您的Audience Manager區段可以與 [!DNL Analytics] 以進一步分析。 潛在的使用案例包括：

* **DSP與之間的互動分析 [!DNL Advertising Search, Social, & Commerce] 廣告：** 標準 [[!DNL Analytics for Advertising] 整合](/help/integrations/analytics/overview.md) 不會提供有關DSP和之間互動的深入分析 [!DNL Search, Social, & Commerce] 因為兩個管道使用的AMO ID都遵循AMO ID歸因規則，搜尋點按可覆寫顯示檢視。 在Audience Manager中建立DSP曝光度區段，即可使用 [!DNL Audience Analytics] 分析DSP與之間的互動 [!DNL Search, Social, & Commerce] 中的廣告 [!DNL Analytics].

* **頻率分析：** 您可以根據使用者接觸到特定廣告或行銷活動的次數，在Audience Manager中建立區段。 接著，您可以分析Analytics中的不同曝光區段，瞭解使用者行為如何根據DSP曝光次數而改變。

## [!DNL Audience Optimization Reports]

您可以善用 [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) 找出行銷活動中區段的潛在效能機會。 這些報表結合促銷活動曝光次數、點按次數和轉換資料與區段量度，以提供以區段為中心的最佳化和有效頻道組合資訊。

### 相關Audience Optimization報表的型別

| 報告 | 描述 |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] 報告](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | 依曝光次數和轉換率來比較對應和未對應的區段。 |
| [[!UICONTROL Trend Analysis and Volume Analysis] 報表]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | 針對廣泛的廣告維度，傳回曝光數、點進率和轉換率的資料。 |
| [[!UICONTROL Optimal Frequency] 報告](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | 協助您在提供的曝光次數和轉換次數之間找到最佳平衡。 它可讓您在開始看到遞減的傳回之前，先調整要顯示的曝光次數。 |
| [[!UICONTROL Unique User Reach] 報告](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | 泡泡圖，其中每個泡泡的大小均與您所選維度的不重複使用者人數成正比。 |

### 考量事項

* 若 [!DNL Audience Optimization Reports] 使用者擁有角色型存取控制(RBAC)，然後 [!DNL Adobe Customer Care] 必須在廣告商ID與組織的Audience Manager資料來源整合代碼之間設定對應。 然後，管理員使用者可以向不同使用者提供RBAC許可權。

* 中的轉換報表 [!DNL Audience Optimization Reports] 需要一般使用者進行一些設定。 使用者必須填入中繼資料檔案。

* [!DNL Audience Optimization Reports] 不支援變更行銷活動中繼資料（例如行銷活動名稱或位置名稱）。

* 搜尋廣告的點選數包含在 [!DNL Audience Optimization Reports] 唯有與曝光次數相關時才行。 換言之，搜尋點按會被視為閱聽後的轉換。 因此，許多搜尋點按可能不會包含在 [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [傳送DSP Media Exposure資料至Adobe Audience Manager概述](overview.md)
>* [收集來自Advertising DSP Campaigns的點選和曝光資料](collect.md)

