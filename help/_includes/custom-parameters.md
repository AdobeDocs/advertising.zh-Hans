---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---
# GGL和MS Campaign设置、MS广告组设置以及MS多媒体和响应式广告设置中的自定义参数字段

**[!UICONTROL Custom Parameters]：** (可选；仅适用于受众营销活动 [!DNL Microsoft Advertising])最多三个自定义参数的名称和值对。 名称的最大长度为16个字母数字字符；值的最大长度为200个字符，包括嵌入的参数。

可在实体及其子实体的跟踪模板中包含自定义参数名称。 当用户单击相关广告时，广告网络会将参数名称替换为定义的参数值。 例如，如果您创建客户参数 `{_color}=red` 您的跟踪模板包括 `http://tracker.example.com/?color={_color}&u={lpurl}`，则当用户单击广告时，color参数中会插入“红色”。

广告组的自定义参数或([!DNL Microsoft Advertising] 仅限)广告级别覆盖具有相同名称的促销活动级别自定义参数。
