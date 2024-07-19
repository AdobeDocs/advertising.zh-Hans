---
title: ' [!DNL FreeWheel] 广告提交的错误代码'
description: 引用向 [!DNL FreeWheel]提交广告时返回的错误代码。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: e48937c2-ced9-4107-9e1d-65a3bac51fff
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 3%

---

# [!DNL FreeWheel]广告提交的错误代码

广告提交失败的错误消息可能来自Advertising DSP或[!DNL FreeWheel]。 错误消息显示在[[!UICONTROL Freewheel Status]对话框](freewheel-check-status.md)的[!UICONTROL API Response]列中。

## Advertising DSP内部错误

| 错误消息 | 描述 | 后续步骤 |
|--- |--- |--- |
| [!DNL Awaiting status response from [!DNL FreeWheel]] | [!DNL FreeWheel]尚未响应提交成功或失败。 | 10分钟后再次检查状态。 |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel]不接受没有分配时钟编号的英国广告。 | 为广告分配时钟编号，然后重新提交广告。 |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | 当您尝试提交广告时，转码器尚未完成广告的转码。 | 等待十分钟，然后重新提交广告。 |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | 提交的交易并未被设定为程序化保证交易。 [!DNL FreeWheel]只接受保证交易。 | 设置交易ID作为程序化保证交易。 当您在交易ID工作流结束时保存程序化保证默认投放位置时，广告会自动提交到[!DNL FreeWheel]。 |
| [!DNL Invalid external_deal_id:] \&lt;deal_id\> | 提交的交易ID不存在或在Adobe端无效。 | 确保交易处于活动状态，然后重新提交广告。 |
| [!DNL \[public_id=]\&lt;deal\>]不存在 | 提交的交易标识在[!DNL FreeWheel]末尾不存在。 | 请联系您的[!DNL FreeWheel]代表以确认交易ID。 |
| [!DNL Ad with identifier] \&lt;*广告名称*\> [!DNL was not found.] | 所提交的广告密钥不存在或在Adobe末尾不是活动的。 | 找到正确的广告密钥，然后重新提交广告。 |
| [!DNL Pending Submission] | 提交仍在等待处理中。 | 刷新页面。 |

{style="table-layout:auto"}

## [!DNL Freewheel] API错误

| 代码 | 含义 | 描述 | 后续步骤 |
|--- |--- |--- |--- |
| 401 | 未授权 | 访问凭据不正确、缺失或无效。 | 请联系您的Adobe客户团队。 |
| 403 | 禁止 | 服务器理解该请求，但拒绝授权。 | 请联系您的Adobe客户团队。 |
| 404 | 未找到 | 您请求的资源不可用。 如果在PUT操作中未找到创作ID，则会返回404。 | 请联系您的Adobe客户团队。 |
| 405 | 不允许使用该方法 | 使用资源不支持的请求方法(例如，使用要求POST发送数据的方法上的GET，或使用只读资源上的PUT)对资源发出请求。 | 请联系您的Adobe客户团队。 |
| 408 | 请求超时 | 处理此请求时发生超时。 超时通常由对特定资源的独占访问并发请求引起。 | 收到此状态后重新提交请求。 如果问题仍然存在，请联系您的Adobe客户团队。 |
| 422 | 无法处理的实体 | 资源无效。 当请求正文无效或创建/更新的资源无效（例如，未找到交易ID）时，会发生此错误。 有关详细信息，请参阅[FreeWheel API 422错误](#freewheel-422-errors)。 | 请联系您的Adobe客户团队。 |
| 500 | 内部服务器错误 | API系统错误。 | 请联系您的Adobe客户团队。 |

{style="table-layout:auto"}

## [!DNL Freewheel] API 422错误 {#freewheel-422-errors}

| 代码 | HTTP代码 | 描述 |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422 | 请求数据的json格式无效。 有关详细信息，请查看错误消息。 |
| DATA_VALIDATION_FAILURE | 422 | 请求数据缺少必填字段或数据类型无效。 有关详细信息，请查看错误消息。 |
| DATA_DEAL_INVALID | 422 | 交易配置不正确或不存在。 有关详细信息，请查看错误消息。 |
| DATA_DEAL_GET失败 | 422 | 未找到交易或其配置有问题。 有关详细信息，请查看错误消息。 |
| DATA_CREATIVE_INGEST_FAILURE | 422 | 创作URL无效。 有关详细信息，请查看错误消息。 |
| DATA_CREATIVE_LINK_FAILURE | 422 | 创意内容未关联到交易的广告单元节点。 有关详细信息，请查看错误消息。 |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | 创意内容未更新。 有关详细信息，请查看错误消息。 |
| DATA_DSP_GET_FAILURE | 422 | 系统中不存在DSP。 |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | 创意内容与广告单元未取消链接。 |
| DATA_CREATIVE_DELETE_FAILURE | 422 | 未删除创意。 |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | 未检测到URL。 |
| DATA_ENTITY_NOT_FOUND | 422 | 创意不存在。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [在 [!DNL Freewheel]](/help/dsp/inventory/freewheel-overview.md)中设置计划性保证交易的概述
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [向 [!DNL Freewheel]](/help/dsp/inventory/freewheel-submit.md)提交计划性保证交易的广告
>* [检查 [!DNL FreeWheel] 计划性保证交易的广告状态](/help/dsp/inventory/freewheel-check-status.md)
