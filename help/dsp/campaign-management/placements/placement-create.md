---
title: 建立位置
description: 瞭解如何建立版位。
feature: DSP Placements
exl-id: 28a328b1-0839-442e-a245-f586a7042f41
source-git-commit: 0b8162a757c9695504ffdfdc450ed7254d823825
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 1%

---

# 建立位置

>[!TIP]
>
>根據特定行銷活動目標或報告需求建立刊登版位。

1. 在主功能表中，按一下 **[!UICONTROL Campaigns]**.

1. 按一下將包含版位的行銷活動名稱。

1. 在資料表格上方，按一下 **[!UICONTROL Create]**. 在 [!UICONTROL Placement Types] 區段，按一下位置型別。

   位置型別會決定位置可包含的廣告型別。

1. 輸入 [位置設定](placement-settings.md)：

   1. 指定 [!UICONTROL Placement Basics] 設定。

   1. 在 [!UICONTROL Goals] 區段，指定 [!UICONTROL Gross Budget] 和（可選）指定其他位置目標。

      某些欄位具有您可以覆寫的預設值。

      如果位置指派到的套件具有套件層級的步調，則您的目標和步調設定將反映套件設定。

   1. （選用）在 [!UICONTROL Geo-Targeting] 區段，縮小要包含或排除的位置。

      如果您未識別特定位置，則會鎖定所有位置。

      >[!NOTE]
      >
      >城市和DMA位置不適用於Roku位置。

   1. 在 [!UICONTROL Inventory Targeting] 區段，縮小存貨來源以包含或排除。

      對於大多數版位型態，預設會包含所有存貨型態及每種型態的所有來源。 對象 [!DNL Roku] 版位，您必須指定存貨型態與來源。

   1. （選用）在 [!UICONTROL Site Targeting] 區段，縮小您要鎖定的網站範圍，並指定您要排除的任何網站。

   1. （選用）在 [!UICONTROL Audience Targeting] 區段：

      1. 縮小對象範圍。 這包括選取要定位在位置中的對象區段。

         對象 [!DNL Roku] 位置，您可以善用 [DSP不重複受眾比對 [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) 納入一或多個可比對的對象區段 [!DNL Roku] （選擇加入）確定性資料集。

      1. （適用於具有人物層級跨裝置目標定位的行銷活動；選用）當刊登版位鎖定一個或多個特定對象時，請為刊登版位啟用人物型跨裝置目標定位。

         以人物為基礎的跨裝置目標鎖定是由 [!DNL LiveRamp] 僅使用美國資料。 所有廣告商都可透過以下網址使用此服務： $0.35 CPM以取得曝光數： [!DNL LiveRamp] 裝置圖表（即目標受眾區段中找不到的裝置）。
   1. （選用）在 [!DNL Brand Safety and Media Targeting] 區段，為您的版位套用品牌安全限制。

   1. （選用）在 [!DNL Tracking] 區段，輸入位置中廣告的第三方事件畫素或轉換畫素。

      >[!NOTE]
      >
      >([!DNL Roku] 位置)協力廠商畫素廠商已核准 [!DNL Roku] 包括 [!DNL Acxiom]， [!DNL comScore]， [!DNL Data Plus Math]， [!DNL Experian]， [!DNL Factual]， [!DNL Kantar]， [!DNL Marketing Evolution]， [!DNL Neustar]， [!DNL Nielsen]， [!DNL Nielsen Catalina Solutions]， [!DNL NinthDecimal]， [!DNL Oracle]， [!DNL Placed]， [!DNL Polk]、和 [!DNL Research Now].


1. 单击 **[!UICONTROL Create Placement]**.

1. （選用）在版位中附加廣告：

   1. 单击 **[!UICONTROL Attach an ad]**.

   1. 執行下列任一項作業：

      * 若要建立新廣告：

         1. 单击 **[!UICONTROL Create a New Ad].**

         1. 指定廣告設定 [音訊廣告](/help/dsp/campaign-management/ads/ad-settings-audio.md)， [連線電視](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)， [顯示廣告](/help/dsp/campaign-management/ads/ad-settings-display.md)， [行動裝置廣告](/help/dsp/campaign-management/ads/ad-settings-mobile.md)， [原生廣告](/help/dsp/campaign-management/ads/ad-settings-native.md)， [前段廣告](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)，或 [通用視訊廣告](/help/dsp/campaign-management/ads/ad-settings-universal-video.md).
         >[!NOTE]
         >
         >通用視訊版位只能包含通用視訊廣告。

         1. 单击 **[!UICONTROL Save & Submit for Review]**.

         1. （選用）針對您想要為位置建立的每個額外廣告，按一下 **[!UICONTROL Attach Another Ad]**，然後重複步驟1-3。

         1. 如果您不附加任何現有廣告，請按一下 **[!UICONTROL I'm done for now]**.
      * 若要在行銷活動中附加現有廣告：
      1. 单击 **[!UICONTROL Select an Ad]**.

      1. 執行下列任一項作業：

         * 若要一次新增一個廣告：

            1. 在廣告名稱旁邊，按一下 **[!UICONTROL Select].**

            1. （選用）針對您想要附加的其他廣告，按一下 **[!UICONTROL Attach Another Ad]**，然後重複此程式。
         * 一次最多新增20個廣告：

            1. 選取廣告清單上方的核取方塊。

            1. 選取每個要新增的廣告旁的核取方塊。

            1. 单击 **[!UICONTROL Attach]**.

            1. 在廣告名稱旁邊，按一下 **[!UICONTROL Select]**.
      1. （選用）若要覆寫版位中特定廣告的預設投放期間和廣告輪換：

         1. 单击 **[!UICONTROL Custom Schedule Ads]**.

         1. 執行下列任一項作業：

            * 若要新增航班，請按一下 **[!UICONTROL Add Flight]**，然後指定開始日期和結束日期。

            * 若要將現有航班新增至廣告，請按一下 **[!UICONTROL +]** 小眾測試版欄的廣告列中。

            * 若要從廣告中移除現有航班，請按一下 **[!UICONTROL x]** 小眾測試版欄的廣告列中。

            * （如果有多個廣告具有相同的外觀）若要不平均地旋轉廣告，請按一下 **[!UICONTROL Even Rotation]** 然後輸入旋轉每個廣告的相對權重（以百分比表示）。

               總重量必須等於100。
         1. 在右上角，按一下 **[!UICONTROL Continue]**.

         1. 檢閱航班詳細資料，然後按一下 **[!UICONTROL Save & Finish]**.







>[!MORELIKETHIS]
>
>* [關於版位管理](placement-about.md)
>* [編輯位置](placement-edit.md)
>* [編輯投放的廣告排程](placement-edit-ad-schedule.md)
>* [暫停或啟用位置](placement-pause-activate.md)
>* [檢視位置的變更記錄](placement-change-log.md)
>* [位置設定](placement-settings.md)
>* [關於通用視訊的常見問題集](/help/dsp/campaign-management/faq-universal-video.md)
>* [鍵盤快速鍵](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [疑難排解效能](/help/dsp/optimization/troubleshooting-performance.md)
>* [影片：如何建立標準顯示位置](https://video.tv.adobe.com/v/340454)

