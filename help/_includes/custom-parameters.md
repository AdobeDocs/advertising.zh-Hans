---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---
# GGL和MS Campaign设置、MS广告组设置以及MS多媒体和响应式广告设置中的“自定义参数”字段

**[!UICONTROL Custom Parameters]：** （可选，仅适用于[!DNL Microsoft Advertising]的受众营销活动）最多三个自定义参数的名称和值对。 名称的最大长度为16个字母数字字符；值的最大长度为200个字符，包括嵌入的参数。

您可以在实体及其子实体的跟踪模板中包含自定义参数名称。 当用户单击相关广告时，广告网络会将参数名称替换为定义的参数值。 例如，如果您创建客户参数`{_color}=red`并且跟踪模板包含`http://tracker.example.com/?color={_color}&u={lpurl}`，则当用户单击广告时，颜色参数中会插入“红色”。

广告组或（仅限[!DNL Microsoft Advertising]）广告级别的自定义参数覆盖营销活动级别
具有相同名称的自定义参数。
