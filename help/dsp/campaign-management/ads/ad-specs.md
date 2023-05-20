---
title: 廣告規格
description: 參考一般和發佈商特定的廣告規格。
feature: DSP Ads
exl-id: 133dfc0d-d839-4e06-a819-21e3e630830c
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# 支援的廣告型別規格

## 影片廣告（前段廣告、CTV和通用視訊）

### 支援的畫面

廣告預設會在桌上型電腦、行動裝置和連線的電視裝置上傳送。 裝置鎖定目標可用於調整傳送。

### 支援的協力廠商廣告伺服器

您可以從以下位置使用標籤表： [!DNL DCM]， [!DNL Flashtalking]， [!DNL Innovid]、和 [!DNL Sizmek]. 如需支援廠商的完整清單，請參閱「[認證廣告服務合作夥伴](certified-ad-servers.md).」

### 高解析度視訊資產的需求（必要）

**視訊標籤型別：** VPAID 2.0 JavaScript或VAST (CTV)。 所有VPAID廣告單位都必須遵守 [VPAID 2.0規格](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf) 如互動廣告局(IAB)所定義。

**視訊轉碼器：** MP4/H.264

**解析度：** 720p為1280x720,1080p為1920x1080

**位元速率：** 720p設定1500-2500 kbps，1080p設定2500-3500 kbps

**H.264設定檔/層級：** 高設定檔，720p為3.1級；1080p為4.0級，高設定檔

**視訊影格速率：** NTSC國家/地區為29.970 fps （通常稱為30 fps），PAL國家為25 fps，影片外觀內容為23.976 fps （通常稱為24 fps）

**視訊色域：** 4:2:0 YUV色度次取樣

**視訊交錯：** 漸進式掃描，亦即非交錯式。 沒有場內移動（混合影格）或交錯。

**導線（石板）：** 不允許

**音訊轉碼器：** AAC-LC或HE-AACv1

**音訊位元速率：** AAC-LC為128-192 kbps，HE-AACv1為64-128 kbps

**音訊頻道：** 2聲道立體聲混音

**音訊取樣速率：** 44.1 kHz或48 kHz （依來源材料而定）

**音訊等級：** 根據ATSC A/85，美國為24個LKFS (+/- 2.0 dB)；根據EBU R128，歐盟為23個LUFS (+/- 1.0)

#### 連線電視廣告的其他發佈者需求

* **A+E網路：** 請參閱A+E網路的 [廣告規格](/help/dsp/assets/a-e-networks-tve-video-ad-specs.pdf)

* **探索：** 請參閱探索的 [廣告規格](/help/dsp/assets/discovery-networks-ad-specs.pdf).

* **迪士尼(包括 斛律)：** 觀看Disney的 [廣告規格](https://hulu.disneyadsales.com/ad-products/video-commercial/).

* **HBO Max：** 請參閱HBO Max的 [廣告規格](/help/dsp/assets/hbo-max-ad-specs-2022.xlsx).

* **NBCUuniversal：**

   * [數位視訊](https://together.nbcuni.com/nbcu-creative-guidelines/digital-video/)

   * [直播串流](https://together.nbcuni.com/nbcu-creative-guidelines/livestream/)

   * [孔雀](https://together.nbcuni.com/nbcu-creative-guidelines/peacock/)

* **派拉蒙：** 請參閱派拉蒙的 [廣告規格](https://www.paramount.com/digital-ads).

## 顯示廣告

### 支援的畫面

廣告預設會在桌上型電腦和行動裝置上提供。 裝置鎖定目標可用於調整傳送。

### 支援的檔案型別

**影像：** GIF、JPG/JPEG、PNG

**HTML5：** 影像檔案型別：GIF、JPG/JPEG、PNG、SVG

### 影像資產需求（必要）

支援通用顯示。

**建議的廣告大小：** 120x60、160x600、180x150、300x50、300x100、300x1050、300x250、300x600、320x50、320x480、480x60、640x480、88x31 728x90、970x250、970x90

**支援的第三方廣告伺服器：** 您可以從以下位置使用標籤表： [!DNL DCM]， [!DNL Flashtalking]， [!DNL Innovid]、和 [!DNL Sizmek]. 如需支援廠商的完整清單，請參閱「[認證廣告服務合作夥伴](certified-ad-servers.md).」

## 音訊廣告

### 支援的畫面

桌上型電腦、行動裝置、平板電腦、智慧型喇叭，以及連線電視

### 支援的協力廠商廣告伺服器

您可以從以下位置使用標籤表： [!DNL DCM]， [!DNL Flashtalking]， [!DNL Innovid]、和 [!DNL Sizmek]. 如需支援廠商的完整清單，請參閱「[認證廣告服務合作夥伴](certified-ad-servers.md).」

### 音訊資產需求（必要）

**檔案型別：** MP3、OGG、AAC

**導線（石板）：**  不允許

**檔案大小上限：** 2MB

**位元速率：** 128

**檔案長度：** 0-60秒

#### 其他發行者需求

* **[!DNL iHeartRadio]**
   * 長度：5、15、30或60秒
   * 檔案型別： MP3
   * 檔案大小上限： 320 kbps
   * 音量：44.1千赫

* **[!DNL Pandora]**
   * 長度：15或30秒
   * 檔案型別： MP4 （應用程式內）、MP3 （案頭）
   * 檔案大小上限： 2.2 MB

* **[!DNL SoundCloud]**
   * 長度：6、15或30秒
   * 檔案型別： MP3
   * 檔案大小上限： 5 MB

* **[!DNL Spotify]**
   * 長度：最長30秒
   * 檔案型別： OGG
   * 檔案大小上限： 500MB
   * 磁碟區：RMS已標準化為–14；dBFS峰值已標準化為–0.2 dBFS

* **[!DNL TargetSpot]**
   * 長度：15、30或60秒
   * 檔案型別： MP3

* **[!DNL TuneIn]**
   * 長度：10、15或30秒
   * 檔案型別： MP3、OGG
   * 音量：44.1千赫

### 隨附橫幅廣告的需求（選用）

**支援的大小：** 300x250、500x500、640x640、1024x1024

#### 其他發行者需求

* **[!DNL iHeartRadio]:**
   * 檔案型別：JPEG、JPG、PNG、GIF、SWF、HTML
   * 檔案大小上限： 2.2 MB
   * Dimension：300x250

* **[!DNL Pandora]:**
   * 檔案型別：JPEG、GIF
   * 檔案大小上限：大小： 100 KB
   * Dimension：300x250 （行動或桌上型電腦）或500x500 （桌上型電腦）

* **[!DNL SoundCloud]:**
   * 檔案型別：靜態JPG、PNG
   * 檔案大小上限：400 KB以下
   * Dimension：1024x1024

* **[!DNL Spotify]:**
   * 檔案型別：靜態JPG、PNG
   * 檔案大小上限： 200 KB
   * Dimension：300x250

* **[!DNL TuneIn]:**
   * 檔案型別：JPEG、JPG、PNG、GIF、HTML
   * 檔案大小上限： 2 MB
   * Dimension：300x250

## 原生顯示廣告

每個廣告都可以包含靜態影像或移動GIF（動態靜圖）。

### 支援的畫面

廣告預設會在桌上型電腦和行動裝置上提供。 裝置鎖定目標可用於調整傳送。

### 所有原生摘要格式的必要資產

#### 影像資產

**解析度：** 最低600x600px；建議最低1200x627px

**檔案型別：** JPEG（影像廣告或視訊廣告封面影像）、GIF(cinemograph)

**檔案大小：** 小於1 MB （影像應不含文字。）

#### 廣告商標誌

**解析度：** 最少80x80px；建議的最少300x300px

**檔案型別：** JPEG或PNG。

**外觀比例：**  1x1比例

>[!NOTE]
>
>根據要覆蓋的影像，選擇淺色或深色標誌資產。

#### 文字/複製

**標題：** 最多200個字元；建議使用25個字元

**註解：** 最多200個字元；建議使用100個字元

**贊助者：** 最多200個字元；建議使用30個字元

**呼叫動作（僅限MoPub）：** 最多15個字元

>[!NOTE]
>
>最終版面配置由發行者在執行階段定義。 如果廣告超過建議的字元數，某些詳細目錄提供者可能不會傳送廣告，或發佈者或SSP可能會截斷文字。

#### 登陸頁面URL

具有選擇性點按追蹤器的點進URL。

點選追蹤器的需求：

* 協力廠商曝光追蹤畫素：僅限1x1影像URL格式

* 可見度JavaScript追蹤器：僅支援IAS；僅支援JS.append格式的1x1影像

* 第三方點選追蹤畫素：必須重新導向至內嵌在URL中的登陸頁面（HTTP 302重新導向）

* 不支援具有200或更多回應的資料管理平台(DMP)點選追蹤器。

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立單一廣告](ad-create.md)
>* [建立多個協力廠商廣告](ad-create-multiple.md)
>* [編輯廣告](ad-edit.md)

