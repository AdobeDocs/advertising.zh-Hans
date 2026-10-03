---
title: 受众区段逻辑语法
description: 引用可用于定义受众区段逻辑的语法。
feature: DSP Audiences
exl-id: fb73f35f-1f65-463b-b93c-90804a8d19a9
TQID: 'https://experienceleague.adobe.com/FPci9npdKrFxwge6tw41Fhx4XAC9VqYFc-RZhLhILLo'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: b4dc2b3d-fdb5-55cd-9190-f1076d8563e4
    internal-label: DSP Audiences
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%
---
# 受众区段逻辑语法

在创建可重用受众时，您可以使用字母数字区段ID（键）和以下语法手动定义区段逻辑：

* ()表示组
* [!DNL OR]的`||`<!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* [!DNL AND]的&amp;
* ! 针对[!DNL NOT] （排除）

>[!NOTE]
>
>* 包括所有指定的区段组，除非它们前面有！ （不包括他们）。
>* 您可以从[!UICONTROL Audiences] > [!UICONTROL All audiences]中[找到受众](reusable-audience-clipboard.md)的区段ID。

例如，以下逻辑：

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

意思（用简单的英语来说）

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>在投放设置中，您可以将保存的受众用作要明确定向的受众，或用作要从定向中排除的单独受众。 确保区段逻辑反映使用受众的目的。

>[!MORELIKETHIS]
>
>* [将可重用受众的区段密钥复制到剪贴板](reusable-audience-clipboard.md)
>* [关于受众管理](audience-about.md)
>* [创建可重复使用的受众](reusable-audience-create.md)
>* [受众设置](audience-settings.md)
>* [可用的第三方数据提供程序](third-party-data-providers.md)
