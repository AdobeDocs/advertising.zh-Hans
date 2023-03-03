---
title: 在中设置PG交易的概述 [!DNL Freewheel]
description: 了解在上与出版商进行计划性保证交易的广告所需的先决条件和额外步骤 [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: b9c60248-8104-42ef-8afb-2f9db67b33b0
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# 在中设置程序化保证交易概述 [!DNL Freewheel]

与出版商建立计划性保证交易 [!DNL Freewheel] 需要额外的权限和步骤。

>[!PREREQUISITES]
>
>与您的Adobe客户团队合作，确保 [!DNL DSP] 帐户具有以下权限：
>
>* 使用 [!DNL FreeWheel] 计划性保证工作流，它需要向提交计划性保证交易的广告 [!DNL FreeWheel].
>
>* (如果您与英国出版商合作，这些出版商需要 [!DNL Clearcast] 每个广告的时钟编号)允许在广告中包含时钟编号。


## 工作流

1. 使用交易中指定的媒体类型创建广告。

   对于某些英国出版商，您必须包含 [!DNL Clearcast] 你的广告的时钟号。

1. [接受交易编号](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) 您已在以下日期与出版商进行协商： [!DNL Freewheel] 使用交易ID收件箱。

   接受交易后，按照提示操作，1)选择要用于交易的广告，2)创建一个程序化的保证默认投放位置以提供广告。

1. [将广告提交到 [!DNL Freewheel]](freewheel-submit.md)

   广告必须先提交并批准，然后才能运行。

1. [检查广告提交状态](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [将计划性保证交易的广告提交到 [!DNL Freewheel]](freewheel-submit.md)
>* [检查广告的状态 [!DNL FreeWheel] 计划性保证交易](freewheel-check-status.md)
>* [错误代码 [!DNL Freewheel] 广告提交](freewheel-error-codes.md)

