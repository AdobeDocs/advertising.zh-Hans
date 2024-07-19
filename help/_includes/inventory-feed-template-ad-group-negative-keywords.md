---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---
# 文本广告模板 — 广告组级别负关键字设置

**[!UICONTROL Delete negative keywords when omitted from list]：** （除Yandex之外的所有广告网络；可选）删除以前使用未在以下列表中指定的模板创建的现有广告组级别负关键字。 **注意：**&#x200B;绝不会使用模板删除通过其他方式创建的负关键字（例如在纯批量处理工作表、[!UICONTROL Campaigns]视图或广告网络的广告编辑器中）。

**[!UICONTROL Apply these negatives]：** （除[!DNL Yandex]之外的所有广告网络；可选）要添加的任何静态广告组级别负关键字。 要为同一关键字指定多个关键字或多个匹配类型，请在单独的行中输入它们。 使用以下语法，不带减号：

* 负广泛匹配： `keyword` （不受[!DNL Microsoft Advertising]支持）
* 负面短语匹配： `"keyword"`
* 完全匹配的负值： `[keyword]`

在批量工作表中使用短语和精确匹配类型的习惯语法，批量工作表是在您通过模板传播馈送数据时生成的。 **注意：**&#x200B;在[!UICONTROL Keywords]选项卡或[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]视图中看不到负关键字。
