---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---
# 文本广告模板 — 营销活动级别的负关键字设置

**[!UICONTROL Delete negative keywords when omitted from list]：** （除Yandex之外的所有广告网络；可选）删除之前使用未在以下列表中指定的模板创建的现有营销活动级别的负面关键词。 **注意：** 使用其他方法创建的负关键字(例如，在普通批量处理工作表中， [!UICONTROL Campaigns] 使用模板时，不会删除任何视图（或广告网络的广告编辑器中的）。

**[!UICONTROL Set negative keywords by campaign name condition]：** （除Yandex之外的所有广告网络；可选）允许您为名称中包含指定字符串的营销活动指定负关键字。 选择此选项后，您最多可以添加3个营销活动名称字符串和相应的关键字。

对于每个字符串，单击 **[!UICONTROL Add (Up to 3)]** 并输入以下信息：

* **[!UICONTROL If campaign name contains]：**  一个文本字符串，可在促销活动名称中的任何位置查找。 查询区分大小写(例如，“ ”[!DNL Car]”匹配营销活动名称“[!DNL Car Parts]”而非“[!DNL INTERIOR CAR ACCESSORIES]“)。

* **[!UICONTROL Apply these negatives]：**  为其名称包含指定字符串的营销活动添加的任何静态营销活动级别的负关键字。 要为同一关键字指定多个关键字或多个匹配类型，请在单独的行中输入它们。 使用以下语法，不带减号：

   * 负值广泛匹配： `keyword` (不支持 [!DNL Microsoft Advertising])
   * 负片语匹配： `"keyword"`
   * 负精确匹配： `[keyword]`

在通过模板传播馈送数据时生成的批量工作表中使用了短语和精确匹配类型的习惯语法。 **注意：** 您在中看不到负关键字 [!UICONTROL Keywords] 选项卡或中的 [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 视图。

**[!UICONTROL All other campaigns: Apply these negatives]：** (所有广告网络，除 [!DNL Yandex]；可选)为名称与指定字符串不匹配的营销活动添加的任何静态营销活动级别的负关键字。 要为同一关键字指定多个关键字或多个匹配类型，请在单独的行中输入它们。 使用以下语法，不带减号：

* 负值广泛匹配： `keyword` (不支持 [!DNL Microsoft Advertising])
* 负片语匹配： `"keyword"`
* 负精确匹配： `[keyword]`

在通过模板传播馈送数据时生成的批量工作表中使用了短语和精确匹配类型的习惯语法。 **注意：** 您在中看不到负关键字 [!UICONTROL Keywords] 选项卡或中的 [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 视图。
