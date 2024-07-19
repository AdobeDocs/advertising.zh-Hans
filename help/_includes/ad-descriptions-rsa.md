---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---
# RSA广告设置中的“广告描述”字段

**[!UICONTROL Ad Descriptions]：**&#x200B;至少有两个、最多四个广告描述，带有可选的位置图钉。 广告网络显示的广告最多包含两个描述；至少输入两个。 每个描述的最大长度为90个字符，包括任何动态文本（例如关键字和广告自定义项的值）。

要插入广告自定义项，请使用以下格式，其中`Default text`是当馈送文件不包含有效值时要插入的可选值：

* [!DNL Google Ads]： `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]： `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

要将描述固定到特定位置，请选择固定选项（如&quot;[!UICONTROL Pinned at position 1]&quot;）。 每个职位必须至少有一个描述。 如果将多个描述固定到同一位置，则最终广告始终会在指定位置包含这些描述之一。 固定到位置2的描述可能无法与广告一起显示。

若要添加其他说明，请单击&#x200B;**[!UICONTROL + Add]**。
