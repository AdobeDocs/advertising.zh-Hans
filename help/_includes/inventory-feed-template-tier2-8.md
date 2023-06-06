---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---
# 第2层 — 购物广告模板中的第8层字段

**[!UICONTROL Tier  2 - Tier 8]：** （在添加产品组层时）作为产品定位依据的产品属性类型，以及选定属性类型的资格标准（例如，Brand=Acme或Condition=New）。 这些值按层次应用，以确定符合条件的产品。 选择属性类型并输入合格标准。 禁止使用的字符包括： `[ ] < > >>` （两个连续的“大于”符号），用于指定模板中的列名称、模板中的修饰符名称以及 [!UICONTROL Parent Product Grouping] 批量处理工作表中的列。

您最多可以包含八层（级别）产品组，包括“[!UICONTROL All Products]&quot;（第1层）。 每一层可以包含多个产品组，但它们必须属于相同的属性类型（例如“条件”）。

>[!NOTE]
>
>* ([!DNL Google Ads] 仅限)的可能值 [!UICONTROL Channel] 为“[!UICONTROL Local]“或”[!UICONTROL Online]，”和的可能值 [!UICONTROL ChannelExclusivity] 为“[!UICONTROL SingleChannel]“ ”和“ ”[!UICONTROL MultiChannel].”
>* 当您从为广告组创建第二层（子）产品组时 [!UICONTROL Product Groups] 在中选项卡 [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 视图，另一个产品组，名为“[!UICONTROL Everything Else]，”使用默认广告组竞价自动创建。 但是，使用库存馈送模板”[!UICONTROL Everything Else]排除了“产品组。
>* 如果包括多个层，且最终（编号最高的）层没有可用值，则次高层将用作可竞价产品组。 例如，如果您包括五层，而第5层没有可用值，则第4层将用作可竞价产品组（单位）。 但是，如果中间层没有可用值，则会忽略该行。 例如，如果您包括五个层，而第5层具有一个值，但第4层没有，则会忽略第4行。

