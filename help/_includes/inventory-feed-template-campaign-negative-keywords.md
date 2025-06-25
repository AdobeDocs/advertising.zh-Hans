---
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---
# 文本广告模板 — 营销活动级别的负关键字设置

**[!UICONTROL Delete negative keywords when omitted from list]：** （除Yandex之外的所有广告网络；可选）删除以前使用未在以下列表中指定的模板创建的现有营销活动级别的负关键字。 **注意：**&#x200B;绝不会使用模板删除通过其他方式创建的负关键字（例如在纯批量处理工作表、[!UICONTROL Campaigns]视图或广告网络的广告编辑器中）。

**[!UICONTROL Set negative keywords by campaign name condition]：** （除Yandex之外的所有广告网络；可选）允许您为名称包含指定字符串的营销活动指定负关键字。 选择此选项后，您最多可以添加三个促销活动名称字符串和相应的关键字。

对于每个字符串，单击&#x200B;**[!UICONTROL Add (Up to 3)]**&#x200B;并输入以下信息：

* **[!UICONTROL If campaign name contains]：**&#x200B;在促销活动名称中查找任意位置的文本字符串。 查询区分大小写（例如，“[!DNL Car]”与促销活动名称“[!DNL Car Parts]”匹配，但不匹配“[!DNL INTERIOR CAR ACCESSORIES]”）。

* **[!UICONTROL Apply these negatives]：**&#x200B;要为其名称包含指定字符串的营销活动添加的任何静态营销活动级别的负关键字。 要为同一关键字指定多个关键字或多个匹配类型，请在单独的行中输入它们。 使用以下语法，不带减号：

   * 负广泛匹配： `keyword` （不受[!DNL Microsoft Advertising]支持）
   * 负面短语匹配： `"keyword"`
   * 完全匹配的负值： `[keyword]`

在批量工作表中使用短语和精确匹配类型的习惯语法，批量工作表是在您通过模板传播馈送数据时生成的。 **注意：**&#x200B;在[!UICONTROL Keywords]选项卡或[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]视图中看不到负关键字。

**[!UICONTROL All other campaigns: Apply these negatives]：** （除[!DNL Yandex]之外的所有广告网络；可选）要为名称与指定字符串不匹配的营销活动添加的任何静态营销活动级别的负关键字。 要为同一关键字指定多个关键字或多个匹配类型，请在单独的行中输入它们。 使用以下语法，不带减号：

* 负广泛匹配： `keyword` （不受[!DNL Microsoft Advertising]支持）
* 负面短语匹配： `"keyword"`
* 完全匹配的负值： `[keyword]`

在批量工作表中使用短语和精确匹配类型的习惯语法，批量工作表是在您通过模板传播馈送数据时生成的。 **注意：**&#x200B;在[!UICONTROL Keywords]选项卡或[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]视图中看不到负关键字。
