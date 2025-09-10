---
source-git-commit: 56c27461cf0e1d7111de9d35d9e38fa980af4c52
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---
# EF ID格式

>[!NOTE]
>
>EF ID区分大小写。 如果[!DNL Analytics]或Customer Journey Analytics实施强制将URL跟踪转换为小写，则Adobe Advertising不会识别EF ID。 这会影响Adobe Advertising竞价和报表，但对[!DNL Analytics]或Customer Journey Analytics中的Adobe Advertising报表没有影响。

#### [!DNL Google Ads]个搜索广告

```
{gclid}:G:s
```

其中：

* `gclid`是[!DNL Google Click ID] (GCLID)。
* `s`是网络类型（“s”用于搜索）。

#### [!DNL Microsoft Advertising]个搜索广告

```
{msclkid}:G:s
```

其中：

* `msclkid`是[!DNL Microsoft Click ID] (MSCLKID)。
* `s`是网络类型（“s”用于搜索）。

#### 在其他搜索引擎上显示广告和搜索广告

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

其中：

* &lt;*Adobe Advertising访客ID*>是每位访客的唯一标识（如UhKVaAABCkJ0mDt）。 也调用了&#x200B;*冲浪者ID*。

* &lt;*timestamp*>是格式为YYYYYMMDDHHMMSS的时间(例如，20190821192533用于2019年、月08、日21、时间19:25:33)。

* &lt;*渠道类型*>是负责点击或曝光的渠道类型：

   * `d`点击DSP显示广告（显示点进）
   * 针对DSP显示广告（显示显示显示到达）的展示的`i`
   * `s`搜索广告的点击（搜索点进）。

示例`EF ID: WcmibgAAAHJK1RyY:1551968087687:d`
