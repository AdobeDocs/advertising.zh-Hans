---
title: 将用户ID从 [!DNL ActionIQ] 转换为通用ID
description: 了解如何使DSP能够摄取您的 [!DNL ActionIQ] 第一方区段。
feature: DSP Audiences
source-git-commit: 658c8a10c4085690ce4dd7e791883dbf31f1cb10
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# 将用户ID从[!DNL ActionIQ]转换为通用ID

*Beta功能*

使用DSP与[!DNL ActionIQ]客户数据平台的集成，将经过哈希处理的电子邮件地址转换为通用ID以进行定向广告。

要与DSP共享<!-- NN -->中的数据，需要执行[!DNL ActionIQ]个步骤：

1. [在DSP中创建受众源](#source-create)。

1. ？

## 步骤1：在DSP中创建受众源 {#source-create}

1. [创建受众源](source-manage.md)以将受众导入您的DSP帐户或广告商帐户，并指定要将用户标识符转换为的[通用ID格式](source-about.md)。

1. 创建受众源后，与[!DNL ActionIQ]用户共享源代码密钥。

## 第2步：

## 步骤3：

1. 验证您的受众库（在从[!UICONTROL Audiences] > [!UICONTROL All Audiences]创建或编辑受众时或在版面设置内创建或编辑受众时可用）中是否正在填充区段，并将通用ID的数量与原始经过哈希处理的电子邮件地址的数量进行比较。

   这些区段应在24小时内可在DSP中使用。 DSP收到区段数据后，该受众规模应在九(9)小时内可见。 有关可接受的ID转换率以及区段计数发生变化原因的信息，请参阅[电子邮件ID与通用ID之间的数据差异](#universal-ids-data-variances)。

区段每24小时刷新一次。

## 故障排除

若要解决翻译速率和用户计数问题，请参阅“[激活通用ID的支持](/help/dsp/audiences/universal-ids.md)”。

要排查转换过程的问题，请联系您的Adobe客户团队或`adcloud-support@adobe.com`。

>[!MORELIKETHIS]
>
>* [关于第一方受众源](/help/dsp/audiences/sources/source-about.md)
>* [管理受众源以激活通用ID受众](source-manage.md)
>* [将用户ID从 [!DNL Adobe Real-Time CDP] 转换为通用ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [将用户ID从 [!DNL Tealium] 转换为通用ID](/help/dsp/audiences/sources/source-tealium.md)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
