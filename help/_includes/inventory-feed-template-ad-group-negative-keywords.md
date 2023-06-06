---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---
# 文本广告模板 — 广告组级别负关键字设置

**[!UICONTROL Delete negative keywords when omitted from list]：** （除Yandex之外的所有广告网络；可选）删除以前使用未在以下列表中指定的模板创建的现有广告组级别负关键字。 **注意：** 使用其他方法创建的负关键字(例如，在普通批量处理工作表中， [!UICONTROL Campaigns] 使用模板时，不会删除任何视图（或广告网络的广告编辑器中的）。

**[!UICONTROL Apply these negatives]：** (所有广告网络，除 [!DNL Yandex]；可选)要添加的任何静态广告组级别的负关键字。 要为同一关键字指定多个关键字或多个匹配类型，请在单独的行中输入它们。 使用以下语法，不带减号：

* 负值广泛匹配： `keyword` (不支持 [!DNL Microsoft Advertising])
* 负片语匹配： `"keyword"`
* 负精确匹配： `[keyword]`

在通过模板传播馈送数据时生成的批量工作表中使用了短语和精确匹配类型的习惯语法。 **注意：** 您在中看不到负关键字 [!UICONTROL Keywords] 选项卡或中的 [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 视图。
