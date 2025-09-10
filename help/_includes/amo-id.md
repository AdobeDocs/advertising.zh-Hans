---
source-git-commit: c56a8caf8db4c76a41a96c48cbe3996078924cc6
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---
# ADOBE ADVERTISING AMO ID

## ADOBE ADVERTISING AMO ID {#amo-id}

AMO ID在较低的粒度级别跟踪每个唯一的广告组合，用于[!DNL Analytics]和Customer Journey Analytics数据分类以及从Adobe Advertising引入广告量度（例如展示次数、点击量和成本）。

对于[!DNL Analytics]，AMO ID存储在[eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)或rVar维度(AMO ID)中。

对于Customer Journey Analytics，AMO ID存储在`trackingCode`对象的`conversionDetails`属性中，该对象是[!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]的一部分。

AMO ID也称为`s_kwcid`，有时发音为“[!DNL squid]”。
