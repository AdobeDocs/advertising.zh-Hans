---
title: （新UI）管理 [!DNL Google Ads] 转化值规则
description: 了解如何在Search、Social和Commerce中查看和管理 [!DNL Google Ads] 转化值规则。
feature: Conversions
feature_v2:
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: a2f79fa9-a8fe-4c1c-961e-75dc3c47f954
source-git-commit: e36a2b66a8dc4c485c7139b44eaf375615826b2b
workflow-type: tm+mt
source-wordcount: 1854
ht-degree: 0%

---

# （新UI）管理[!DNL Google Ads]转化值规则

*Beta功能*

[!DNL Google Ads] [转化值规则](https://support.google.com/google-ads/answer/10518330)允许您根据用户信息（包括设备类型、位置和受众区段）调整转化事件的值。 通过Google智能竞价，您可以在搜索、显示、购物和性能最大化营销活动中使用基于价值的竞价规则。 对于具有尽可能提高转化次数和目标ROAS竞价策略的营销活动，[!DNL Google Ads]算法将开始偏好具有较高值的转化。

营销活动级别的转化值规则将覆盖帐户级别的规则。 当转化满足多个转化值规则时，将仅应用其中一个规则。 通常应用最具体的规则，但请参阅[[!DNL Google Ads] 有关不同规则条件类型](https://support.google.com/google-ads/answer/10520348)的优先级的文档。

## [!UICONTROL Conversion Value Rules]视图和功能

Search、Social和Commerce会自动同步[!DNL Google Ads]帐户中的转化值规则。 在[!DNL Google Ads]界面中创建的所有规则将在24小时内同步，并可在[!UICONTROL Goals] > [!UICONTROL Conversion Value Rules]视图中找到。

某些帐户可以管理其转化值规则：

* 对于在个人帐户或营销活动级别跟踪转化的帐户，您可以[创建](#google-conversion-value-rule-create)、[编辑](#google-conversion-value-rule-edit)和[更改帐户级别和营销活动级别规则的状态](#google-conversion-value-rule-change-status)。

  这些帐户可以链接到[[!DNL Google Ads] 经理帐户](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md)，但它们不能使用跨帐户转化跟踪（针对此跟踪，将跨经理帐户中的所有帐户跟踪转化）。

* 在使用跨帐户转化跟踪的帐户中，帐户级别和营销活动级别的规则继承自经理帐户，并且是只读的。

## 包含搜索、社交和Commerce项目组合的转化值规则

当广告商帐户配置为将Search、Social和Commerce目标上传到[!DNL Google Ads]，并且您在具有目标的项目组合中包含使用转化值规则的营销活动时，[!DNL Google Ads]会将转化值规则应用于目标中指定的原始转化值。 因此，搜索、社交和Commerce中的转化数据与[!DNL Google Ads]中的转化数据不同。

例如，假设目标使用单个转化量度“潜在客户”，并将来自移动设备的转化权重为10，将来自非移动设备的转化权重为10。 Search、Social和Commerce将任一设备类型的事件计为一(1)次转化，并将转化值计为10。 但是，假设该组合中的某个营销活动使用转化值规则“如果设备是移动设备，则乘以2。” 在跟踪该营销活动的移动潜在客户事件时，[!DNL Google Ads]还会将转化计数计为一(1)，但转化值会计为(10 x 2) = 20。

要查看有关规则的更多信息，包括应用规则之前的原始转化值，请参阅 [!DNL Google Ads][&#128279;](https://support.google.com/google-ads/answer/10519848)中的转化值规则报告。

## 创建[!DNL Google Ads]转化值规则 {#google-conversion-value-rule-create}

您可以在[!DNL Google Ads]帐户中创建帐户级别和营销活动级别的转化值规则，在个人帐户级别或更低级别跟踪这些帐户的转化。 您不能为在主帐户层跟踪的具有跨帐户转换的帐户创建规则。

每个规则最多包括两个条件，以及当满足条件时要应用的转换值调整。 帐户中的所有规则必须使用相同类型的主条件和（可选）辅助条件。 例如，如果规则1包含主要条件“Audience”和次要条件“Location”，则帐户中的所有其他规则必须具有主要条件“Audience”。 当其他规则包含次要条件时，它必须是“位置”。

您可以为每个营销活动创建多个营销活动级别的规则。 但是，当帐户级别规则已存在时，[!DNL Google Ads]尚不提供在[!DNL Google Ads]编辑器之外创建新帐户级别规则的功能。 要创建其他帐户级别的规则，请直接登录到[!DNL Google Ads]并使用[!DNL Google Ads]编辑器。

**注意：**&#x200B;营销活动级别的转化值规则将覆盖帐户级别的规则，并且只能将一个规则应用于转化。 有关详细信息，请参阅[当转换满足多个规则的条件时，如何 [!DNL Google Ads] 确定将哪个规则应用于转换](https://support.google.com/google-ads/answer/10520348)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**。

   默认情况下，选择&#x200B;**[!UICONTROL Campaign]**&#x200B;选项卡以显示所有营销活动级别的规则。

1. （可选）要创建帐户级别的规则，请单击&#x200B;**[!UICONTROL Account]**&#x200B;选项卡。

1. 在工具栏中，单击&#x200B;**[!UICONTROL Create Campaign Rule]** （从[!UICONTROL Campaign]选项卡）或&#x200B;**[!UICONTROL Create Account Rule]** （从[!UICONTROL Account]选项卡）。

1. 选择广告网络和帐户。 对于营销活动级别的规则，还应选择营销活动。 然后单击&#x200B;**[!UICONTROL Next]**。

1. 配置[转换规则设置](#google-ads-conversion-value-rule-settings)。

   必须配置主要条件和值调整。 您可以选择配置辅助条件。

   在一个条件内，使用布尔运算符`OR`连接多个目标或排除项，以便满足任何选项以启动值调整。 当您包含辅助条件时，辅助条件使用布尔运算符`ALL`与主条件相连，因此必须同时满足这两个条件才能启动值调整。 示例：如果\[Location is Alignalia OR Tunity\]和\[Device is Mobile OR Tablet\]，则添加1.5。

   **注意：**&#x200B;帐户中的所有规则必须使用相同类型的主条件和（可选）辅助条件。 例如，如果规则1包含主要条件“Audience”和次要条件“Location”，则帐户中的所有其他规则必须具有主要条件“Audience”。 当其他规则包含次要条件时，它必须是“位置”。

1. 单击&#x200B;**[!UICONTROL Review and Save]**&#x200B;以查看设置。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 编辑[!DNL Google Ads]转化值规则 {#google-conversion-value-rule-edit}

对于在个人帐户或更低级别跟踪转化的帐户/营销活动，您可以编辑其中的转化值规则。 您无法编辑在主帐户级别跟踪的具有跨帐户转化的帐户的规则。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**。

   默认情况下，选择&#x200B;**[!UICONTROL Campaign]**&#x200B;选项卡以显示所有营销活动级别的规则。

1. （可选）若要改为查看所有帐户级别的规则，请单击&#x200B;**[!UICONTROL Account]**&#x200B;选项卡。

1. 选中规则旁边的复选框。

1. 在批量操作工具栏中，单击（/help/search-social-commerce/assets/edit-new.png“编辑”）。

1. 编辑[转换规则设置](#google-ads-conversion-value-rule-settings)。

   您不能编辑现有规则的条件类型，但可以编辑条件和值调整。

   必须配置主要条件和值调整。 您可以选择配置辅助条件。

   **注意：**&#x200B;如果添加辅助条件，则它必须与帐户中的其他规则是相同的条件类型。 例如，如果帐户中的规则1其他规则具有辅助条件“Location”，则当其他规则包括辅助条件时，辅助条件必须为“Location”。 当您包含辅助条件时，辅助条件使用布尔运算符`ALL`与主条件相连，因此必须同时满足这两个条件才能启动值调整。

1. 单击&#x200B;**[!UICONTROL Review and Save]**&#x200B;以查看设置。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 更改[!DNL Google Ads]转换值规则的状态 {#google-conversion-value-rule-change-status}

对于在个人帐户级别跟踪转化的帐户和营销活动，您可以暂停、激活或删除其中的转化值规则。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**。

   默认情况下，选择&#x200B;**[!UICONTROL Campaign]**&#x200B;选项卡以显示所有营销活动级别的规则。

1. （可选）若要改为查看所有帐户级别的规则，请单击&#x200B;**[!UICONTROL Account]**&#x200B;选项卡。

1. 选中每行旁边的复选框以进行更改。

1. 在批量操作工具栏中，

   * 要激活（启用）暂停的规则，请单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Activate]**。

   * 要暂停活动规则，请单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Pause]**。

   * 要删除活动或暂停的规则，请单击![删除](/help/search-social-commerce/assets/delete.png "删除")。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**。

## [!DNL Google Ads]转换值规则设置 {#google-conversion-value-rule-settings}

| 部分 | 参数 | 描述 |
|---|---|---|
| [!UICONTROL Select Campaign] | [!UICONTROL Network] | 广告网络。 |
| | [!UICONTROL Account] | 广告网络帐户。 |
| | [!UICONTROL Campaign] | （仅限促销活动级别的转化值规则）广告促销活动。 |
| [!UICONTROL Conditions] > [!UICONTROL Primary Condition] | \[条件类型\] | （现有规则只读）触发值调整必须满足的条件类型：<ul><li>*[!UICONTROL Device]：*&#x200B;定位所有或特定的设备类型。</li><li>*[!UICONTROL Location]：*&#x200B;定位所有国家和地区，或定位并排除特定位置。</li><li>*[!UICONTROL Audiences]：*&#x200B;定位所有或特定受众</li></ul>**注意：**&#x200B;帐户中的所有规则必须使用相同类型的主条件和（可选）辅助条件。 例如，如果规则1包含主要条件“Audience”和次要条件“Location”，则帐户中的所有其他规则必须具有主要条件“Audience”。 当其他规则包含次要条件时，它必须是“位置”。 |
| | \[条件类型\] > [!UICONTROL Device]和[!UICONTROL Device Level] | （仅限设备条件）要定位的设备类型：<ul><li>*[!UICONTROL All devices]：**定向所有设备类型。</li><li>*[!UICONTROL Select devices]：*&#x200B;要指定一个或多个要定位的设备类型： *[!UICONTROL Desktop]：*、*[!UICONTROL Mobile]*&#x200B;和&#x200B;*[!UICONTROL Tablet]：*。</li></ul>在一个条件内，使用布尔运算符`OR`连接多个目标，以便满足任何选项以启动值调整。 示例：如果\[Device is Mobile OR Tablet\]，则添加1.5。 |
| | \[条件类型\] > [!UICONTROL Location]和[!UICONTROL Location Level] | （仅限位置条件）位置目标和排除项：<ul><li>*[!UICONTROL All countries and territories]：*&#x200B;定位所有国家和位置，或定位并排除特定位置。</li><li>*[!UICONTROL Enter a location]：*&#x200B;定位和排除特定位置。</li></ul><ul><li>要展开某个位置或子位置，请单击名称后面的`>`。</li><li>要添加目标，请选择目标一次，以显示绿色复选标记。</li><li>要排除某个目标，请再次选择该目标以显示红色的&#x200B;**[!UICONTROL X]**。</li><li>要删除目标或排除项，请执行下列操作之一：<ul><li>单击[!UICONTROL Selections]列中该项旁边的![删除](/help/search-social-commerce/assets/delete.png "删除")。</li><li>选择目标，直到没有复选标记或[!UICONTROL X]显示。</li></ul></li></ul>在一个条件内，使用布尔运算符`OR`连接多个目标或排除项，以便满足任何选项以启动值调整。 示例：如果\[Location is Alignalia OR Tunities\]，则添加1.5。 |
| | \[条件类型\] > [!UICONTROL Audience]和[!UICONTROL Audience Level] | （仅限受众条件）受众目标：<ul><li>*[!UICONTROL All audience segments]：*&#x200B;定位所有[!DNL Google Ads]受众区段。</li><li>*[!UICONTROL Enter audience segments]：*&#x200B;定位特定的[!DNL Google Ads]受众区段。</li></ul><ul><li>要将某个类别或子类别展开到其区段中，请单击名称后面的`>`。</li><li>要添加目标，请选择该目标。</li><li>要删除目标，请取消选择该目标或单击[!UICONTROL Selection]列中该项旁边的![删除](/help/search-social-commerce/assets/delete.png "删除")。</li></ul>在一个条件中，多个目标或排除项使用布尔运算符OR进行连接，以便满足任何选项来启动值调整。 示例：如果\[受众是廉价旅行者或家庭度假者\]，则添加1.5。<br><br>**注意：**&#x200B;保存受众目标后，您可以添加其他受众，但无法在[!DNL Google Ads]编辑器之外删除这些受众。 如果需要删除受众目标，请直接登录[!DNL Google Ads]并使用[!DNL Google Ads]编辑器。 |
| [!UICONTROL Conditions] > [!UICONTROL Secondary Condition] | \[条件类型\] | （可选，对于现有规则为只读）触发值调整必须满足的条件类型。 当您包含辅助条件时，辅助条件使用布尔运算符`ALL`与主条件相连，因此必须同时满足这两个条件才能启动值调整。 示例：如果\[Location is Alignalia OR Tunizis\]和\[Device is Mobile OR Tablet\]，则添加1.5。<br><br>有关说明，请查看主要条件的条目。<br><br>**注意：**&#x200B;帐户中的所有规则必须使用相同类型的主要条件和（可选）次要条件。 例如，如果规则1包含主要条件“Audience”和次要条件“Location”，则帐户中的所有其他规则必须具有主要条件“Audience”。 当其他规则包含次要条件时，它必须是“位置”。 |
| [!UICONTROL Value Adjustment] | [!UICONTROL Adjustment Operation]和[!UICONTROL Adjustment Value] | 指定调整类型，然后输入一个正值：<ul><li>*[!UICONTROL Add]：*&#x200B;将指定的值添加到传递的转换值。 该值必须大于零(0)。</li><li>*[!UICONTROL Multiply]：*&#x200B;将传递的转换值乘以指定的值。 该值必须介于0.5和10之间。</li></ul> |

<!--
>[!MORELIKETHIS]
>
>* 
-->
