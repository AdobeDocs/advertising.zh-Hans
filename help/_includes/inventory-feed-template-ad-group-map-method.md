---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---
# 文本广告模板 — 广告组映射方法

**[!UICONTROL Map Method]：** （为广告组启用[!UICONTROL Map Only]时；除[!DNL Yandex]之外的所有广告网络）新关键字和广告映射到现有广告组的方法：

* *[!UICONTROL Contains Anywhere]：*&#x200B;将数据添加到其名称包含指定字符串（如果存在）的现有广告组。

* *[!UICONTROL Contains Exactly]：*&#x200B;将数据添加到其名称包含指定字符串（如果存在）的现有广告组。

* *[!UICONTROL Exactly Matches]*（默认）：将数据添加到具有相同名称的现有广告组（如果存在）。

当未找到匹配项时，将忽略广告组的所有数据。 如果馈送中的广告组数据不包含促销活动数据，则广告组会映射到任何促销活动中具有相同名称的广告组（如果存在）。 如果找到多个广告组匹配，则关键词和广告映射到所有关键词。
