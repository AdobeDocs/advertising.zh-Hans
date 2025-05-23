---
title: 批量处理工作表错误
description: 参考每个批量工作表错误的潜在原因。
exl-id: dc3559b0-05c0-4896-b9e9-67084f56ab80
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 0%

---

# 批量处理工作表错误

Search、Social和Commerce在批量处理工作表操作期间生成两种类型的错误文件：

* **SE错误：**&#x200B;当已发布文件但广告网络不接受所有数据时，将创建一个名为`<uploaded file name>_se_errors.<extension used for the bulksheet>`的错误文件。 当接受某些行（而非所有行）时，错误文件会显示未发布的行以及对每个错误的说明，以便您进行更正。 错误包含在“[!UICONTROL SE Error Message]”列中。

>[!NOTE]
>
>如果您发布任何[!DNL Google Ads]个违反广告网络的广告政策，但可能有资格获得劐免的广告，则这些广告将自动重新发布并带有劐免请求。 如果免除请求失败，则错误文件中将包含有关违规的信息。

* **EF错误：**&#x200B;当批量处理工作表操作无法上载或处理文件或文件中的单个行时，它会创建一个名为`<uploaded file name>_ef_errors.<extension used for the bulksheet>`的错误文件。 如果单个行出现问题，则包含这些行，
并解释每个错误，以便您进行更正。 错误包含在“[!UICONTROL EF Error Message]”列中。

## [!UICONTROL SE Error]条消息

[!UICONTROL SE Error]列中的错误直接来自广告网络。

## [!UICONTROL EF Error]条消息

以下错误可能包含在[!UICONTROL EF Errors]文件的[!UICONTROL EF Error]列中。

### 下载/创建错误

| 类别 | 消息 | 描述 |
|----|----|----|
| 常规 | [!UICONTROL Internal Error: Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | 由于未分类或未处理的错误，该操作完全失败。 如果问题仍然存在，请与Adobe客户团队联系以调查原因。 |
| | [!UICONTROL Pre-Sync Failed. Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | 在创建批量工作表之前，搜索、社交和Commerce无法与广告网络同步，因此未创建批量工作表。 如果问题仍然存在，请与您的Adobe客户团队联系。 |

### 上载错误

| 类别 | 消息 | 描述 |
|----|----|----|
| 常规 | [!UICONTROL Internal Error: Please Try Uploading the bulksheet Again. If Problem Persists Contact Customer Care] | 操作完全失败。 如果问题仍然存在，请与您的Adobe客户团队联系。 |
| 所有实体 | [!UICONTROL Invalid Fields.] \[无效字段和错误\] | 指定的数据缺失或无效。 |
|  | [!UICONTROL Invalid Reference Given] | 实体在广告网络中的ID或父实体的ID（例如帐户ID）与搜索、社交和Commerce中的实体不对应。 在批量处理工作表中编辑ID时，可能会发生这种情况。 |
|  | [!UICONTROL &lt;Entity> is deleted or expired] | 实体已过期或已删除，您无法更改其属性。 当有人手动编辑状态时，可能会删除该实体。 |
|  | [!UICONTROL &lt;Entity> status should be Active or Paused] | （新实体）新实体只能为“活动”或“已暂停”。 |
|  | [!UICONTROL Duplicate Entries are present] | 同一实体包含多行，每行都具有不同的属性。 将更改合并为一行。 |
|  | [!UICONTROL Invalid AMO ID given] | 行的AMO ID不存在。 如果您在批量处理工作表中编辑了ID，则可能会发生这种情况。 |
|  | [!UICONTROL Invalid row given] | 行包含的信息不足以确定实体类型。 编辑该行以包含实体类型的所有必填字段。 |
| 帐户 | [!UICONTROL Provide Valid Account Details] | （多个帐户的批量工作表）帐户标识符未包含在所有行中。 为每行输入以下任一列组合的值：a)“[!UICONTROL AMO ID]”或b)“[!UICONTROL Account Name]”和“[!UICONTROL Platform]”。 |
|  | [!UICONTROL Account is disabled. Disabled Accounts cannot be processed] | 搜索、社交和Commerce无法访问广告网络帐户，因此您无法创建或编辑营销活动数据。 确保搜索帐户的凭据正确且帐户已启用。 |
| 营销活动 | [!UICONTROL Invalid Shopping Country specified] | （购物营销活动）“[!UICONTROL Sales Country]”字段中的值无效。 查看 [!DNL Google Ads][&#128279;](https://support.google.com/merchants/answer/160637#countrytable)的有效国家/地区[和 [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/3/en/51083)的有效国家/地区列表。 |
| 所有营销活动组件 | [!UICONTROL Campaign creation failed] | 未创建父营销活动，因此未创建此实体。 确保所有父实体都包含所有必填字段。 |
| 广告组 | [!UICONTROL Campaign Row missing] | 指定的父营销活动不存在，因此未创建广告组。 在新行中创建父营销活动。 |
|  | [!UICONTROL New adgroup has both keywords and placement] | 广告组可以包含关键字或投放位置，但不能同时包含关键字和投放位置。 为关键词和投放位置创建单独的广告组。 |
|  | [!UICONTROL No corresponding keyword for Adgroup] | ([!DNL Yandex])未创建广告组，因为它至少包含一个关键字。 |
|  | [!UICONTROL No corresponding creative for Adgroup] | ([!DNL Yandex])未创建广告组，因为它至少包含一个广告。 |
|  | [!UICONTROL Creative Row Missing] | ([!DNL Yandex])未创建广告组，因为它至少包含一个广告。 |
| 所有广告组组件 | [!UICONTROL Adgroup creation failed] | 未创建父广告组，因此无法创建此实体。 这可能是由于广告组字段中的错误或父营销活动失败所致。 确保所有父实体都包含所有必填字段。 |
|  | [!UICONTROL Adgroup Row Missing] | 指定的父广告组不存在，因此无法创建实体。 在新行中创建父广告组。 |
|  | [!UICONTROL Cannot modify Tracking Template at Keyword / Creative / Site Link level until Account has been migrated to use Upgraded URLs. Please retry after migration] | “[!UICONTROL Tracking Template]”字段仅适用于使用最终/高级URL的帐户。 在迁移帐户以使用最终/高级URL之前，请删除该值。 |
| 广告 | [!UICONTROL Cannot modify attributes other than status code and url for &lt;ad type>] | （除文本、扩展文本、产品、应用程序安装和动态搜索之外的广告类型）您只能编辑此广告类型的状态和URL。 |
|  | [!UICONTROL The number of creatives under an AdGroup should not exceed 50] | 每个广告组最多可包含50个广告，此批量工作表包含的广告超过50个。 减少广告数量。 |
|  | [!UICONTROL Cannot modify an ad which is either deleted/expired or under an deleted/expired campaign] | 广告位于已过期或删除的父实体中，因此无法对其进行编辑。 |
| 关键词 | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | 父营销活动或广告组已删除或已过期，因此您无法更改实体。 |
| 投放位置 | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | 父营销活动或广告组已删除或已过期，因此您无法更改实体。 |
|  | [!UICONTROL Cannot specify placement bids for websites under Display Select enabled Campaign with Search and Display Networks] | (Google广告)您只能在搜索网络上的促销活动中或仅在内容网络上的促销活动中对投放位置进行竞价，但不得在针对搜索和内容网络的促销活动中竞价。 |
| 购物产品组 | [!UICONTROL Cannot delete Everything Else manually. It will be deleted automatically when all Product Group Conditions under the same parent are removed] | 每个级别的产品组必须包含一个“[!UICONTROL Everything Else]”组。 您无法手动删除“[!UICONTROL Everything Else]”组；它在您删除同一级别的所有其他产品组时自动被删除。 |
|  | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | 父营销活动或广告组已删除或已过期，因此您无法更改实体。 |
| 站点链接 | [!UICONTROL Sitelinks Cannot update more than 10 site links per campaign] | （仅限[!DNL Yandex]）消息不准确；每个营销活动最多可以包含四个（而非10个）站点链接，并且此批量工作表包含四个以上。 删除某些站点链接。 |
|  | [!UICONTROL Cannot update sitelinks under deleted/expired campaign] | 父营销活动已过期或已被删除，因此您无法编辑站点链接。 |
|  | [!UICONTROL Creative creation failed] | ([!DNL Yandex])无法创建站点链接，因为未创建广告。 |
| 位置目标 | [!UICONTROL Cannot modify locations under deleted campaigns or adgroups] | 父营销活动或广告组已删除或已过期，因此您无法编辑位置目标。 |
| 排除项 | [!UICONTROL Other than status is modified] | 您只能编辑排除项（“[!UICONTROL Active]”或“[!UICONTROL Deleted]”）的状态。 |
| Google再营销列表目标/受众 | [!UICONTROL Invalid Audience given] | （仅限[!DNL Google Ads]个营销活动）RLSA目标与现有RLSA（受众）不对应。 更正“[!UICONTROL Audience]”和“[!UICONTROL RLSA Target]”列中的值。 |

### 发布错误

仅在[!UICONTROL EF Errors]文件中出现以下错误。 大多数发布错误来自广告网络，并包含在SE错误文件中。

| 类别 | 消息 | 描述 |
|----|----|----|
| 常规 | [!UICONTROL Internal Error: Please Try Posting the bulksheet Again. If Problem Persists Contact Customer Care] | 操作完全失败。 如果问题仍然存在，请与您的Adobe客户团队联系。 |
| 所有实体 | [!UICONTROL Entity]已发布到广告网络 | 实体已发布到广告网络，但未同时同步到Search、Social和Commerce，因此实体数据无法立即在Search、Social和Commerce中可用。 同步过程现在将自动触发。<br><br>当同步大量数据时，数据可能在Search、Social和Commerce中不可用数小时或更长时间。 |
| | [!UICONTROL Skipping &lt;ENTITY> creation since &lt;PARENT ENTITY> creation failed.] | 无法创建父实体，因此未创建此子实体。 |

>[!MORELIKETHIS]
>
>* [关于使用批量处理工作表管理营销活动数据](bulksheet-about.md)
>* [下载/创建批量处理工作表文件](bulksheet-download.md)
>* [验证批量处理工作表文件中的登陆页面](bulksheet-validate-landing-pages.md)
>* [上载批量工作表文件或更正的错误文件](bulksheet-upload.md)
>* [发布批量工作表或已更正的错误文件](bulksheet-post.md)
