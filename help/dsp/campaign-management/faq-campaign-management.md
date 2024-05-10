---
title: 关于Campaign Management的常见问题解答
description: 了解关于营销活动管理的更多信息，包括更改的延迟期以及在投放期间更改预算时将发生的情况。
feature: DSP Packages, DSP Placements
exl-id: 8a443543-ebb1-4273-a007-afef07d32d8c
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# 关于Campaign Management的常见问题解答

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## 设置更改的延迟

* 当您更改投放位置或资源包设置时，更改何时生效？

  设置更改通常立即生效，但最长可能需要12小时。

  如果这是交付的最后一天，请在当天早些时候进行更改，以便DSP有充足的时间根据更改重新校准包。 例如，如果您从偶数步调更改为前载步调，DSP需要重新评估如何在剩余飞行时间中分配支出。 如果在航班的最后一天只剩一小时交付，请不要做出这种改变。

## 中期预算更新

* 当您对投放位置进行更改时，DSP需要多久才能重新分配资源包预算？

  预算分配基于职位安排业绩，该业绩以14天平均数评估。 只有在职位安排更改导致在14天平均时间内的绩效发生变化时，才会导致预算分配更改。

  当发生性能更改时，DSP会在下一个预算优化周期内相应地在投放位置之间重新分配包预算，该周期大约在营销活动时区的午夜(00:00)发生。

* 从资源包中删除投放位置并将其添加到另一个资源包时，如何重新分配预算？

  投放位置的整个支出历史记录会附加到投放位置，并随其从一个包移动到另一个包。

  当您从资源包中删除投放位置时，资源包将不再具有投放位置的任何支出历史记录。 包预算将变为（包预算 — 已删除投放预算）/剩余时间间隔。 然后，将包预算分配给包中剩余的投放位置。

  同样，如果您将同一版面添加到其他资源包，DSP会在为新资源包中的所有版面分配预算时考虑版面的支出历史记录。

* 在航班的最后一天，包裹的步调会有什么变化？

  在飞行的最后一天，时间从24小时缩短到23小时，以免超出包预算。 此外，包的步调填充策略会自动更改为&quot;[!UICONTROL Frontload]，”，即使它设置为“[!UICONTROL even]“ 这意味着65%的每日预算应在东部标准时间上午11:30前交付。

>[!MORELIKETHIS]
>
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
>* [投放设置](/help/dsp/campaign-management/placements/placement-settings.md)
>* [设置效果活动的最佳实践](/help/dsp/optimization/campaign-best-practices-performance.md)
