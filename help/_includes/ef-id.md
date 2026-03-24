---
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---
# ADOBE ADVERTISING EF ID

## ADOBE ADVERTISING EF ID

EF ID是一个唯一令牌，Adobe Advertising使用该令牌将活动与单个浏览器或设备级别的在线点击或广告展示相关联。 EF ID主要用作将[!DNL Analytics]数据和Customer Journey Analytics数据发送到Adobe Advertising以在Adobe Advertising中优化报表和竞价的密钥。

对于[!DNL Analytics]，EF ID存储在[an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=zh-Hans)或[!DNL rVar] （保留的[!DNL eVar]）维度(Adobe Advertising EF ID)中。

对于Customer Journey Analytics，EF ID存储在`trackingIdentities`对象的`conversionDetails`属性中，该对象是[&#x200B; [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/xdm/field-groups/event/advertising-full-extension)的一部分。

### EF ID格式 {#ef-id-formats}

请参阅《Adobe Analytics组件指南》中的EF ID维度项[的](https://experienceleague.adobe.com/zh-hans/docs/analytics/components/dimensions/amo-ef-id#dimension-items)格式。

>[!NOTE]
>
>EF ID区分大小写。 如果[!DNL Analytics]或Customer Journey Analytics实施强制将URL跟踪转换为小写，则Adobe Advertising不会识别EF ID。 这会影响Adobe Advertising竞价和报表，但对[!DNL Analytics]或Customer Journey Analytics中的Adobe Advertising报表没有影响。

<!-- Legacy content:

#### [!DNL Google Ads] search ads

```
{gclid}:G:s
```

where:

* `gclid` is the [!DNL Google Click ID] (GCLID).
* `s` is the network type ("s" for search).

#### [!DNL Microsoft Advertising] search ads

```
{msclkid}:G:s
```

where:

* `msclkid` is the [!DNL Microsoft Click ID] (MSCLKID).
* `s` is the network type ("s" for search).

#### Display ads and search ads on other search engines 

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

where:

* <*Adobe Advertising visitor ID*> is a unique ID per visitor (such as UhKVaAAABCkJ0mDt). Also called the *surfer ID*.

* <*timestamp*> is the time in the format YYYYMMDDHHMMSS (such as 20190821192533 for Year 2019, Month 08, Day 21, Time 19:25:33).

* <*channel type*> is the channel type responsible for the click or exposure:

    * `d` for a click on a DSP display ad (display click-through)
    * `i` for an impression of a DSP display ad (display view-through)
    * `s` for a click on a Search ad (search click-through).

Example `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

-->
