---
source-git-commit: 0cf325946fdc3852b8b94acb29678bf6c47227a0
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---
# ADOBE ADVERTISING EF ID

## ADOBE ADVERTISING EF ID

EF ID是一个唯一令牌，Adobe Advertising使用该令牌将活动与单个浏览器或设备级别的在线点击或广告展示相关联。 EF ID主要用作将[!DNL Analytics]数据和Customer Journey Analytics数据发送到Adobe Advertising以在Adobe Advertising中优化报表和竞价的密钥。

对于[!DNL Analytics]，EF ID存储在[an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)或[!DNL rVar] （保留的[!DNL eVar]）维度(Adobe Advertising EF ID)中。

对于Customer Journey Analytics，EF ID存储在`trackingIdentities`对象的`conversionDetails`属性中，该对象是[ [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension)的一部分。

### EF ID格式 {#ef-id-formats}

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
