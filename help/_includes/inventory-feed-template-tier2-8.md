---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---
# 第2层 — 购物广告模板中的第8层字段

**[!UICONTROL Tier  2 - Tier 8]：**（添加产品组层时）用于定位产品的产品属性类型，以及所选属性类型的资格条件（例如，Brand=Acme或Condition=New）。 这些值按层次应用，以确定符合条件的产品。 选择属性类型并输入限定条件。 禁止使用的字符包括： `[ ] < > >>`（两个连续的“大于”符号），用于指定模板中的列名称、模板中的修饰符名称以及批量处理工作表中[!UICONTROL Parent Product Grouping]列中的层分隔符。

您最多可以包含八层（级别）产品组，包括“[!UICONTROL All Products]”（第1层）。 每一层可以包含多个产品组，但它们必须属于相同的属性类型（例如“条件”）。

>[!NOTE]
>
>* （仅限[!DNL Google Ads]） [!UICONTROL Channel]的可能值为“[!UICONTROL Local]”或“[!UICONTROL Online]”，[!UICONTROL ChannelExclusivity]的可能值为“[!UICONTROL SingleChannel]”和“[!UICONTROL MultiChannel]”。
>* 当您从[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]视图中的[!UICONTROL Product Groups]选项卡为广告组创建第二层（子）产品组时，名为“[!UICONTROL Everything Else]”的其他产品组将使用默认广告组竞价自动创建。 但是，使用库存馈送模板时，排除了&quot;[!UICONTROL Everything Else]&quot;产品组。
>* 如果包括多个层，且最终（编号最高的）层没有可用值，则次高层将用作可竞价的产品组。 例如，如果您包括五层，而第5层没有可用值，则第4层将用作可竞价的产品组（单位）。 但是，如果中间层没有可用值，则会忽略该行。 例如，如果您包括五层，而第5层具有值，但第4层没有，则会忽略第4行。
