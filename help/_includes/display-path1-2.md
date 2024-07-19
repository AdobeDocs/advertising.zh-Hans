---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---
# 在某些广告设置中，显示“路径1”和“显示路径2”字段

**[!UICONTROL Display Path 1]**，**[!UICONTROL Display Path 2]：** （可选）添加到显示URL的文本，该URL是自动从最终URL中提取的。 URL中的每个路径前面都有一个正斜杠(`/`)。 路径不能包含正斜杠(`/`)或换行符(`\n`)。 每个路径的最大长度为15个字符或7个双字节字符。

要插入广告自定义项，请使用以下格式，其中`Default text`是当馈送文件不包含有效值时要插入的可选值：

* [!DNL Google Ads]： `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]： `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

例如，如果[!UICONTROL Display Path 1]是“deals”，[!UICONTROL Display Path 2]是“local”，则显示URL将是`<display URL>/deals/local`，如www.example.com/deals/local。
