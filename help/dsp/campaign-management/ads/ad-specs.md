---
title: 广告规范
description: 参考常规和特定于发布者的广告规范。
feature: DSP Ads
exl-id: 133dfc0d-d839-4e06-a819-21e3e630830c
source-git-commit: a6f9bb2d714e7ddb22f74c9c614772eca30f9e40
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 0%

---

# 支持的广告类型的规范

## 视频广告（前置广告、CTV和通用视频）

### 支持的Screens

默认情况下，在台式机、移动设备和连接的电视设备上投放广告。 设备定位可用于调整投放。

### 支持的第三方广告服务器

您可以使用来自[!DNL DCM]、[!DNL Flashtalking]、[!DNL Innovid]和[!DNL Sizmek]的标记工作表。 有关支持的供应商的完整列表，请参阅“[认证广告服务合作伙伴](certified-ad-servers.md)”。

### 高清视频Assets的要求

**视频标记类型：** VPAID 2.0 JavaScript或VAST (CTV)。 所有VPAID广告单位都必须遵循Interactive Advertising局(IAB)定义的[VPAID 2.0规范](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf)。

**视频编解码器：** MP4/H.264

**分辨率：** 1280x720,720p；1920x1080,1080p

**比特率：** 720p为1500-2500 kbps，1080p为2500-3500 kbps

**H.264配置文件/级别：**&#x200B;配置文件，级别3.1(720p)；配置文件，级别4.0(1080p)

**视频帧速率：** 29.970 fps（通常称为30 fps）（对于NTSC国家/地区），25 fps（对于PAL国家/地区），23.976 fps（通常称为24 fps）（对于电影外观内容）

**视频颜色空间：** 4:2:0 YUV色度子取样

**视频交错：**&#x200B;渐进式扫描，即非交错。 无场内移动（混合帧）或交错。

不允许&#x200B;**个引线(Slate)：**

**音频编解码器：** AAC-LC或HE-AACv1

**音频比特率：** 128-192 kbps（对于AAC-LC），64-128 kbps（对于HE-AACv1）

**声道：**&#x200B;双声道立体声混音

**音频采样速率：** 44.1 kHz或48 kHz（根据源材料）

**音频级别：** 24 LKFS (+/- 2.0 dB)（根据ATSC A/85）；23 LUFS (+/- 1.0)（根据EBU R128）

#### 已连接电视广告的附加发布者要求

* **A+E网络：**&#x200B;查看A+E网络的[广告规范](/help/dsp/assets/a-e-networks-tve-video-ad-specs.pdf)

* **发现：**&#x200B;查看发现的[广告规范](/help/dsp/assets/discovery-networks-ad-specs.pdf)。

* **迪士尼(包括 Hulu)：**&#x200B;查看迪士尼的[广告规范](https://www.disneyadvertising.com/mediakit/#specifications)。

* **HBO Max：**&#x200B;查看HBO Max的[广告规范](/help/dsp/assets/hbo-max-ad-specs-2022.xlsx)。

* **NBCUniversal：**

   * [数字视频](https://together.nbcuni.com/nbcu-creative-guidelines/digital-video/)

   * [实时流](https://together.nbcuni.com/nbcu-creative-guidelines/livestream/)

   * [孔雀](https://together.nbcuni.com/nbcu-creative-guidelines/peacock/)

* **派拉蒙：**&#x200B;请参阅派拉蒙的[广告规范](https://www.paramount.com/digital-ads)。

## 显示广告

### 支持的Screens

默认情况下，广告会在桌面和移动设备上交付。 设备定位可用于调整投放。

### 支持的文件类型

**图像：** GIF、JPG/JPEG、PNG

**HTML5：**&#x200B;图像文件类型：GIF、JPG/JPEG、PNG、SVG

### 图像Assets的要求

支持通用显示。

**推荐的广告大小：** 120x60、160x600、180x150、300x50、300x100、300x1050、300x250、300x600、320x50、320x480、480x60、 640x480， 88x31， 728x90， 970x250， 970x90

**支持的第三方广告服务器：**&#x200B;您可以使用来自[!DNL DCM]、[!DNL Flashtalking]、[!DNL Innovid]和[!DNL Sizmek]的标记表。 有关支持的供应商的完整列表，请参阅“[认证广告服务合作伙伴](certified-ad-servers.md)”。

## 音频广告

### 支持的Screens

台式机、移动设备、平板电脑、智能扬声器和联网电视

### 支持的第三方广告服务器

您可以使用来自[!DNL DCM]、[!DNL Flashtalking]、[!DNL Innovid]和[!DNL Sizmek]的标记工作表。 有关支持的供应商的完整列表，请参阅“[认证广告服务合作伙伴](certified-ad-servers.md)”。

### Audio Assets的要求

**文件类型：** MP3、OGG、AAC

不允许&#x200B;**个领导者（板）：**

**最大文件大小：** 2MB

**比特率：** 128

**文件长度：** 0-60秒

#### 其他发布者要求

* **[!DNL iHeartRadio]**
   * 长度：5、15、30或60秒
   * 文件类型：MP3
   * 最大文件大小：320 kbps
   * 音量：44.1千赫

* **[!DNL Pandora]**
   * 长度：15或30秒
   * 文件类型：MP4（应用程序内）、MP3（桌面）
   * 最大文件大小：2.2 MB

* **[!DNL SoundCloud]**
   * 长度：6、15或30秒
   * 文件类型：MP3
   * 最大文件大小：5 MB

* **[!DNL Spotify]**
   * 长度：最多30秒
   * 文件类型： OGG
   * 最大文件大小：500MB
   * 卷：RMS规范化为–14；dBFS峰值规范化为–0.2 dBFS

* **[!DNL TargetSpot]**
   * 长度：15、30或60秒
   * 文件类型：MP3

* **[!DNL TuneIn]**
   * 长度：10、15或30秒
   * 文件类型：MP3、OGG
   * 音量：44.1千赫

### 随附横幅广告的要求（可选）

**支持的大小：** 300x250、500x500、640x640、1024x1024

#### 其他发布者要求

* **[!DNL iHeartRadio]：**
   * 文件类型：JPEG、JPG、PNG、GIF、SWF、HTML
   * 最大文件大小：2.2 MB
   * 尺寸：300x250

* **[!DNL Pandora]：**
   * 文件类型：JPEG、GIF
   * 最大文件大小：大小：100 KB
   * 尺寸：300x250（移动设备或台式机）或500x500（台式机）

* **[!DNL SoundCloud]：**
   * 文件类型：静态JPG、PNG
   * 最大文件大小：小于400 KB
   * 尺寸：1024x1024

* **[!DNL Spotify]：**
   * 文件类型：静态JPG、PNG
   * 最大文件大小：200 KB
   * 尺寸：300x250

* **[!DNL TuneIn]：**
   * 文件类型：JPEG、JPG、PNG、GIF、HTML
   * 最大文件大小：2 MB
   * 尺寸：300x250

## 原生显示广告

每个广告都可以包含静止图像或移动GIF（电影胶片）。

### 支持的Screens

默认情况下，广告会在桌面和移动设备上交付。 设备定位可用于调整投放。

### 所有本机信息源格式均需要Assets

#### 图像资产

**分辨率：**&#x200B;最小为600x600px；建议的最小为1200x627px

**文件类型：** JPEG （图像广告或视频广告封面图像）、GIF (cinemograph)

**文件大小：**&#x200B;小于1 MB（图像应不含文本。）

#### 广告商徽标

**分辨率：**&#x200B;最小为80x80px；建议的最小为300x300px

**文件类型：** JPEG或PNG。

**宽高比：** 1x1比

>[!NOTE]
>
>根据它将覆盖的图像，在浅色或深色徽标资产之间进行选择。

#### 文本/复制

**标题：**&#x200B;最多200个字符；建议使用25个字符

**题注：**&#x200B;最多200个字符；建议使用100个字符

**赞助者：**&#x200B;最多200个字符；建议30个字符

**Call to action （仅限MoPub）：**&#x200B;最多15个字符

>[!NOTE]
>
>最终布局由发布器在运行时定义。 如果广告超出建议的字符数，则某些库存提供商可能无法投放广告，或者发布者或SSP可能会截断文本。

#### 登陆页面URL

带有可选点击跟踪器的点进URL。

点击跟踪器的要求：

* 第三方印象跟踪像素：仅1x1图像URL格式

* 可见性JavaScript跟踪器：仅支持IAS；1x1图像仅采用JS.append格式

* 第三方点击跟踪像素：必须重定向到URL中嵌入的登陆页面（HTTP 302重定向）

* 不支持具有200个或更多响应的数据管理平台(DMP)点击跟踪器。

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建单个Ad](ad-create.md)
>* [创建多个第三方广告](ad-create-multiple.md)
>* [编辑广告](ad-edit.md)
