---
title: 在 [!DNL Freewheel]中设置PG交易的概述
description: 了解在 [!DNL Freewheel]上为发布者的程序化保证交易运行广告所需的先决条件和额外步骤。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: b9c60248-8104-42ef-8afb-2f9db67b33b0
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# 在[!DNL Freewheel]中设置计划性保证交易的概述

在[!DNL Freewheel]上与发布者设置编程性保证交易需要额外的权限和步骤。

>[!PREREQUISITES]
>
>请与您的Adobe帐户团队合作，确保您的[!DNL DSP]帐户具有以下权限：
>
>* 使用[!DNL FreeWheel]计划性保证工作流的权限，该工作流是向[!DNL FreeWheel]提交计划性保证交易的广告所必需的。
>
>* （如果您与英国出版商合作，他们需要每个广告都有[!DNL Clearcast]个时钟编号），则可以在广告中包含时钟编号。

## 工作流

1. 使用交易中指定的媒体类型创建广告。

   对于某些英国出版商，您的广告必须包含[!DNL Clearcast]时钟编号。

1. [接受您已经使用“交易ID收件箱”与[!DNL Freewheel]上的发布者协商的交易ID](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)。

   接受交易后，按照提示操作，1)选择要用于交易的广告，2)创建用于投放广告的编程性保证默认投放位置。

1. [将广告提交至 [!DNL Freewheel]](freewheel-submit.md)

   广告必须先提交并批准，然后才能运行。

1. [检查广告提交状态](freewheel-check-status.md)。

>[!MORELIKETHIS]
>
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [向 [!DNL Freewheel]](freewheel-submit.md)提交计划性保证交易的广告
>* [检查 [!DNL FreeWheel] 计划性保证交易的广告状态](freewheel-check-status.md)
>*  [!DNL Freewheel] 广告提交的[错误代码](freewheel-error-codes.md)
