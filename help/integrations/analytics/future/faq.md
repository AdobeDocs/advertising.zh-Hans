---
title: 常見問答
description: xxx
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# 常見問題集xxx

## 標題

https://adobeadcloud.zendesk.com/agent/tickets/14214依預設，Adobe Analytics會報告每個報告中所有擷取的事件。 &quot;[!UICONTROL Unspecified]「事件代表未連線至Adobe廣告的表單完成事件。 例如，在Ad Platform報表中，電子郵件促銷活動驅動的有機轉換或轉換會屬於「未指定」。

您可以使用此篩選器，移除勾選記號(「包含未指定（無）」)選項)，從報表中移除未指定的事件。 <!-- Not sure if this is in DSP or in Analytics Workspace -->

## 標題

https://adobeadcloud.zendesk.com/agent/tickets/24323將Analytics事件標籤放在與Ad Cloud畫素相同的位置，以確保XXX相符。

## 標題

https://adobeadcloud.zendesk.com/agent/tickets/24323

問：在內部安全性稽核期間，當我們將Ad Cloud整合至現有的Adobe Analytics安裝時，某些功能會被標籤為已啟用的安全性疑慮。

有問題的整合是AdCloud與Adobe Audience Manager之間的整合。 此功能可提高AdCloud與Adobe Audience Manager之間訪客ID的符合率。 其做法是傳送網路要求至pagead.l.doubleclick.net、star-mini.c10r.facebook.com和pug88000nf.pubmatic.com，以判斷這些服務是否有可運用之訪客的現有ID。 這些網路請求已標籤為安全性風險，並正在發生於所有網站訪客。

我們的稽核人員要求我們停用此功能。 如果我們封鎖這些網路要求會發生什麼事？

答：我們檢查了產品，他們提到有問題的畫素是為了提高Ad Cloud、特定詳細目錄/SSP合作夥伴(關於DSP)和AAM之間的Cookie匹配率。  如果移除這些畫素，客戶可能會發現AAC/AAM與庫存合作夥伴之間個別畫素適用的匹配率有所降低，但他們不會預期這會相當嚴重。

對於Ad Cloud搜尋，我們確實看到廣告商的Experience Cloud組織ID已針對Mathworks設定，但我們的產品團隊沒有看到Mathworks設定以在Ad Cloud中啟用對象。 您是否使用Adobe Audience Manager將受眾傳送至Ad Cloud Search？ 如果沒有，移除這些專案將不會對目前的工作流程造成影響。 如果您不想讓這些畫素被引發，AAM客戶服務可協助您移除這些畫素。

