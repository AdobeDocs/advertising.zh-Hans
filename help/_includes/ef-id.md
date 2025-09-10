---
source-git-commit: d1e2e92532b1f930420436c66c687676a2b7de6a
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---
# ADOBE ADVERTISING EF ID

EF ID是一个唯一令牌，Adobe Advertising使用该令牌将活动与单个浏览器或设备级别的在线点击或广告展示相关联。 EF ID主要用作将[!DNL Analytics]数据和Customer Journey Analytics数据发送到Adobe Advertising以在Adobe Advertising中优化报表和竞价的密钥。

对于[!DNL Analytics]，EF ID存储在[an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)或[!DNL rVar] （保留的[!DNL eVar]）维度(Adobe Advertising EF ID)中。

对于Customer Journey Analytics，EF ID存储在`trackingIdentities`对象的`conversionDetails`属性中，该对象是[!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]的一部分。
