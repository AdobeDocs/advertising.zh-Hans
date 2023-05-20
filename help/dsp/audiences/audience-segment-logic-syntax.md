---
title: 對象區段邏輯的語法
description: 參考可用來定義對象區段邏輯的語法。
feature: DSP Audiences
exl-id: fb73f35f-1f65-463b-b93c-90804a8d19a9
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# 對象區段邏輯的語法

建立可重複使用的對象時，您可以使用英數字元區段ID （索引鍵）及下列語法來手動定義區段邏輯：

* ()表示群組
* `||` 的 [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp;&amp; for [!DNL AND]
* ！ 的 [!DNL NOT] （排除）

>[!NOTE]
>
>* 所有指定的區段群組都會包括在內，除非其前面有！ （會將其排除）。
>* 您可以 [尋找對象的區段ID](reusable-audience-clipboard.md) 從 [!UICONTROL Audiences] > [!UICONTROL All audiences].


例如，下列邏輯：

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

表示（純英文）

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>在版位設定中，您可以使用儲存的對象作為要明確鎖定的對象，或作為單獨的對象來從目標中排除。 請確定您的區段邏輯反映您使用對象的目的。

>[!MORELIKETHIS]
>
>* [將可重複使用對象的區段金鑰複製到剪貼簿](reusable-audience-clipboard.md)
>* [關於對象管理](audience-about.md)
>* [建立可重複使用的對象](reusable-audience-create.md)
>* [對象設定](audience-settings.md)
>* [可用的第三方資料提供者](third-party-data-providers.md)

