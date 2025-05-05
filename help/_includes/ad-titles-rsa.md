---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---
# RSA广告设置中的“广告标题”字段

**[!UICONTROL Ad Titles]：**&#x200B;至少有三个和最多十五个广告标题（标题），带有可选的位置图钉。 广告网络显示最多有三个标题的广告；至少输入三个。 每个标题的最大长度为30个字符，包括任何动态
文本（例如关键字和广告自定义项的值）。

要插入广告自定义项，请使用以下格式，其中`Default text`是当馈送文件不包含有效值时要插入的可选值：

* [!DNL Google Ads]： `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]： `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

要将标题固定到特定位置，请选择固定选项（如&quot;[!UICONTROL Pinned at position 1]&quot;）。 每个职位必须至少有一个标题。 如果将多个标题固定到同一位置，则最终广告始终会在指定位置包含这些标题之一。 固定到位置3的标题不能与广告一起显示。

要添加其他标题，请单击&#x200B;**[!UICONTROL + Add]**。
