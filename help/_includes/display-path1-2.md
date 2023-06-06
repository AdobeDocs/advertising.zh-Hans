---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---
# 在某些广告设置中，“显示路径1”和“显示路径2”字段

**[!UICONTROL Display Path 1]**， **[!UICONTROL Display Path 2]：** （可选）添加到显示URL的文本，将自动从最终URL中提取。 URL中的每个路径前面都有一个正斜杠(`/`)。 路径不能包含正斜杠(`/`)或换行符(`\n`)个字符。 每个路径的最大长度为15个字符或7个双字节字符。

要插入广告自定义项，请使用以下格式，其中 `Default text` 是一个可选值，可在信息源文件不包含有效值时插入：

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

例如，如果显示路径1为“deals”，而显示路径2为“local”，则显示URL将为 `<display URL>/deals/local`，如www.example.com/deals/local。
