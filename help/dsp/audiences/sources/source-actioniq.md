---
title: “转换用户ID [!DNL ActionIQ] 到通用ID”
description: “了解如何使DSP能够摄取 [!DNL ActionIQ] 第一方客户细分。”
feature: DSP Audiences
source-git-commit: 729098f01fb9d076efb2b945be4011df9ab1c905
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# 转换用户ID [!DNL ActionIQ] 到通用ID

*Beta版功能*

将DSP与集成 [!DNL ActionIQ] 客户数据平台，用于将经过哈希处理的电子邮件地址转换为通用ID以进行定向广告。

有 <!-- NN --> 共享数据的步骤 [!DNL ActionIQ] 使用DSP：

1. [在DSP中创建受众源](#source-create).

1. ？

## 步骤1：在DSP中创建受众源 {#source-create}

1. [创建受众源](source-manage.md) 要将受众导入您的DSP帐户或广告商帐户，请指定 [通用ID](source-about.md) 要将用户标识符转换为的用户标识符。

1. 创建受众源后，请使用以下对象共享源代码密钥 [!DNL ActionIQ] 用户。

1. 完成所有步骤后，在受众库中验证（在从创建或编辑受众时可用） [!UICONTROL Audiences] > [!UICONTROL All Audiences] 区段会在24小时内填充的区段。 将通用ID的数量与原始经过哈希处理的电子邮件地址的数量进行比较。

   经过哈希处理的电子邮件地址到通用ID的转换率应大于90%。 例如，如果您从客户数据平台发送100个经过哈希处理的电子邮件地址，则应将其转换为90个以上的通用ID。 90%或更低的翻译率是一个问题。 有关区段计数如何变化的更多信息，请参阅&quot;[电子邮件ID与通用ID之间的数据差异原因](#universal-ids-data-variances)“

   有关故障排除支持，请联系您的Adobe客户团队或 `adcloud-support@adobe.com`.

区段每24小时刷新一次。

## 第2步：

>[!MORELIKETHIS]
>
>* [关于第一方受众源](/help/dsp/audiences/sources/source-about.md)
>* [管理受众源以激活通用ID受众](source-manage.md)
>* [受众源设置](source-settings.md)
>* [转换用户ID [!DNL Adobe Real-Time CDP] 到通用ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [转换用户ID [!DNL Tealium] 到通用ID](/help/dsp/audiences/sources/source-tealium.md)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)

<!--
>* [Convert User IDs from [!DNL Optimizely] to Universal IDs](/help/dsp/audiences/sources/source-optimizely.md)
-->
